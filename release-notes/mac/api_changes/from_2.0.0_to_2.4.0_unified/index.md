---
id: 07FEEF49-A48B-4406-9186-97F515543615
title: "From 2.0.0 to 2.4.0 unified"
---

# Xamarin.Mac.dll

## Namespace Accounts

### Type Changed: Accounts.ACErrorCode

Added values:

<pre style='color: green'>
	CredentialItemNotExpired = 23,
	CredentialItemNotFound = 22,
</pre>

## Namespace AppKit

### Type Changed: AppKit.NSAnimation

Added constructor:

<pre style='color: green'>
	public NSAnimation (double duration, NSAnimationCurve animationCurve);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual IntPtr Constant (double duration, NSAnimationCurve animationCurve);
```

### Type Changed: AppKit.NSApplication

Removed interface:

<pre style='color: red'>
	INSWindowRestoration
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public static void RestoreWindow (string identifier, Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
```

Added methods:

<pre style='color: green'>
	public virtual void CompleteStateRestoration ();
	public virtual void ExtendStateRestoration ();
	public virtual bool RestoreWindowWithIdentifier (string identifier, Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
</pre>

### Type Changed: AppKit.NSApplicationActivationOptions

Added value:

<pre style='color: green'>
	Default = 0,
</pre>

### Type Changed: AppKit.NSButton

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual nint MaxAcceleratorLevel { get; set; }
</pre>

### Type Changed: AppKit.NSButtonType

Added values:

<pre style='color: green'>
	Accelerator = 8,
	MultiLevelAccelerator = 9,
</pre>

### Type Changed: AppKit.NSCollectionView

Added properties:

<pre style='color: green'>
	public virtual bool AllowsEmptySelection { get; set; }
	public virtual NSView BackgroundView { get; set; }
	public virtual NSCollectionViewLayout CollectionViewLayout { get; set; }
	public virtual INSCollectionViewDataSource DataSource { get; set; }
	public virtual Foundation.NSSet&lt;Foundation.NSIndexPath&gt; IndexPathsForVisibleItems { get; }
	public virtual nint NumberOfSections { get; }
	public virtual Foundation.NSSet SelectionIndexPaths { get; set; }
	public virtual NSCollectionViewItem[] VisibleItems { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DeleteItems (Foundation.NSSet&lt;Foundation.NSIndexPath&gt; indexPaths);
	public virtual void DeleteSections (Foundation.NSIndexSet sections);
	public virtual void DeselectAll (Foundation.NSObject sender);
	public virtual void DeselectItems (Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (Foundation.NSSet&lt;Foundation.NSIndexPath&gt; indexPaths, NSEvent theEvent, ref CoreGraphics.CGPoint dragImageOffset);
	public virtual Foundation.NSIndexPath GetIndexPath (NSCollectionViewItem item);
	public virtual Foundation.NSIndexPath GetIndexPath (CoreGraphics.CGPoint point);
	public virtual Foundation.NSSet GetIndexPaths (string elementKind);
	public virtual NSCollectionViewItem GetItem (Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributes (Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributest (string kind, Foundation.NSIndexPath indexPath);
	public virtual nint GetNumberOfItems (nint section);
	public virtual INSCollectionViewElement GetSupplementaryView (Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public virtual INSCollectionViewElement[] GetVisibleSupplementaryViews (Foundation.NSString elementKind);
	public virtual void InsertItems (Foundation.NSSet&lt;Foundation.NSIndexPath&gt; indexPaths);
	public virtual void InsertSections (Foundation.NSIndexSet sections);
	public virtual NSCollectionViewItem MakeItem (string identifier, Foundation.NSIndexPath indexPath);
	public virtual NSView MakeSupplementaryView (Foundation.NSString elementKind, string identifier, Foundation.NSIndexPath indexPath);
	public virtual void MoveItem (Foundation.NSIndexPath indexPath, Foundation.NSIndexPath newIndexPath);
	public virtual void MoveSection (nint section, nint newSection);
	public virtual void PerformBatchUpdates (System.Action updates, System.Action&lt;bool&gt; completionHandler);
	public void RegisterClassForItem (System.Type itemClass, string identifier);
	public void RegisterClassForSupplementaryView (System.Type viewClass, Foundation.NSString kind, string identifier);
	public virtual void RegisterNib (NSNib nib, string identifier);
	public virtual void RegisterNib (NSNib nib, Foundation.NSString kind, string identifier);
	public virtual void ReloadData ();
	public virtual void ReloadItems (Foundation.NSSet&lt;Foundation.NSIndexPath&gt; indexPaths);
	public virtual void ReloadSections (Foundation.NSIndexSet sections);
	public virtual void ScrollToItems (Foundation.NSSet&lt;Foundation.NSIndexPath&gt; indexPaths, NSCollectionViewScrollPosition scrollPosition);
	public virtual void SelectAll (Foundation.NSObject sender);
	public virtual void SelectItems (Foundation.NSSet indexPaths, NSCollectionViewScrollPosition scrollPosition);
</pre>

### Type Changed: AppKit.NSCollectionViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public virtual bool CanDragItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent);
	public virtual void DisplayingItemEnded (NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public virtual void DisplayingSupplementaryViewEnded (NSCollectionView collectionView, NSView view, string elementKind, Foundation.NSIndexPath indexPath);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession session, CoreGraphics.CGPoint screenPoint, Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent, ref CoreGraphics.CGPoint dragImageOffset);
	public virtual string[] GetNamesOfPromisedFiles (NSCollectionView collectionView, Foundation.NSUrl dropURL, Foundation.NSSet indexPaths);
	public virtual INSPasteboardWriting GetPasteboardWriter (NSCollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual void ItemsChanged (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual void ItemsDeselected (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual void ItemsSelected (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual Foundation.NSSet ShouldChangeItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual Foundation.NSSet ShouldDeselectItems (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual Foundation.NSSet ShouldSelectItems (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual NSCollectionViewTransitionLayout TransitionLayout (NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public virtual void WillDisplayItem (NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (NSCollectionView collectionView, NSView view, Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public virtual bool WriteItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSPasteboard pasteboard);
</pre>

### Type Changed: AppKit.NSCollectionViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool AcceptDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public static bool CanDragItems (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent);
	public static void DisplayingItemEnded (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public static void DisplayingSupplementaryViewEnded (INSCollectionViewDelegate This, NSCollectionView collectionView, NSView view, string elementKind, Foundation.NSIndexPath indexPath);
	public static void DraggingSessionWillBegin (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingSession session, CoreGraphics.CGPoint screenPoint, Foundation.NSSet indexPaths);
	public static NSImage GetDraggingImage (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent, ref CoreGraphics.CGPoint dragImageOffset);
	public static string[] GetNamesOfPromisedFiles (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSUrl dropURL, Foundation.NSSet indexPaths);
	public static INSPasteboardWriting GetPasteboardWriter (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSIndexPath indexPath);
	public static void ItemsChanged (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public static void ItemsDeselected (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public static void ItemsSelected (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public static Foundation.NSSet ShouldChangeItems (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public static Foundation.NSSet ShouldDeselectItems (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public static Foundation.NSSet ShouldSelectItems (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public static NSCollectionViewTransitionLayout TransitionLayout (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public static NSDragOperation ValidateDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public static void WillDisplayItem (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public static void WillDisplaySupplementaryView (INSCollectionViewDelegate This, NSCollectionView collectionView, NSView view, Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public static bool WriteItems (INSCollectionViewDelegate This, NSCollectionView collectionView, Foundation.NSSet indexPaths, NSPasteboard pasteboard);
</pre>

### Type Changed: AppKit.NSCollectionViewItem

Added property:

<pre style='color: green'>
	public virtual NSCollectionViewItemHighlightState HighlightState { get; set; }
</pre>

### Type Changed: AppKit.NSColor

Obsoleted properties:

```
[Obsolete ()]
	public static NSColor UnderPageBackground { get; }
```

### Type Changed: AppKit.NSColorList

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: AppKit.NSComboBox

Added property:

<pre style='color: green'>
	public Foundation.NSObject Item { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
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

### Type Changed: AppKit.NSDraggingInfo

Modified constructors:

```
public protected NSDraggingInfo ()
```

Added property:

<pre style='color: green'>
	public virtual NSSpringLoadingHighlight SpringLoadingHighlight { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ResetSpringLoading ();
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

### Type Changed: AppKit.NSFont

Added methods:

<pre style='color: green'>
	public static NSFont MonospacedDigitSystemFontOfSize (nfloat fontSize, nfloat weight);
	public static NSFont SystemFontOfSize (nfloat fontSize, nfloat weight);
</pre>

### Type Changed: AppKit.NSFontPanel

Removed property:

<pre style='color: red'>
	public virtual bool WorksWhenModal { get; }
</pre>

### Type Changed: AppKit.NSGestureEvent

Modified methods:

```
public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent theEvent, System.AsyncCallback callback, object object)
	public virtual bool Invoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent theEvent)
```

### Type Changed: AppKit.NSGestureRecognizer

Added properties:

<pre style='color: green'>
	public virtual NSPressureConfiguration PressureConfiguration { get; set; }
	public NSGestureEvent ShouldAttemptToRecognize { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void PressureChange (NSEvent pressureChangeEvent);
</pre>

### Type Changed: AppKit.NSGestureRecognizerDelegate

Added method:

<pre style='color: green'>
	public virtual bool ShouldAttemptToRecognize (NSGestureRecognizer gestureRecognizer, NSEvent theEvent);
</pre>

### Type Changed: AppKit.NSGestureRecognizerDelegate_Extensions

Added method:

<pre style='color: green'>
	public static bool ShouldAttemptToRecognize (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSEvent theEvent);
</pre>

### Type Changed: AppKit.NSGraphics

Added methods:

<pre style='color: green'>
	public static void DisableScreenUpdates ();
	public static void DrawWindowBackground (CoreGraphics.CGRect aRect);
	public static void EnableScreenUpdates ();
</pre>

### Type Changed: AppKit.NSLayoutAttribute

Added values:

<pre style='color: green'>
	FirstBaseline = 12,
	LastBaseline = 11,
</pre>

### Type Changed: AppKit.NSLayoutFormatOptions

Added values:

<pre style='color: green'>
	AlignAllFirstBaseline = 4096,
	AlignAllLastBaseline = 2048,
</pre>

### Type Changed: AppKit.NSLayoutManager

Added methods:

<pre style='color: green'>
	public virtual void EnumerateEnclosingRects (Foundation.NSRange glyphRange, Foundation.NSRange selectedRange, NSTextContainer textContainer, NSTextLayoutEnumerateEnclosingRects callback);
	public virtual void EnumerateLineFragments (Foundation.NSRange glyphRange, NSTextLayoutEnumerateLineFragments callback);
	public virtual ushort GetCGGlyph (uint glyphIndex);
	public virtual ushort GetCGGlyph (uint glyphIndex, out bool isValidIndex);
	public virtual NSGlyphProperty GetProperty (uint glyphIndex);
	public virtual Foundation.NSRange GetTruncatedGlyphRangeInLineFragment (uint glyphIndex);
	public virtual void ProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editMask, Foundation.NSRange newCharRange, nint delta, Foundation.NSRange invalidatedCharRange);
	public virtual void SetGlyphs (IntPtr glyphs, IntPtr props, IntPtr charIndexes, NSFont aFont, Foundation.NSRange glyphRange);
</pre>

### Type Changed: AppKit.NSLayoutManagerDelegate

Added methods:

<pre style='color: green'>
	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, CoreGraphics.CGSize oldSize);
	public virtual CoreGraphics.CGRect GetBoundingBox (NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, CoreGraphics.CGRect proposedRect, CoreGraphics.CGPoint glyphPosition, uint charIndex);
	public virtual nfloat GetLineSpacingAfterGlyph (NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public virtual nfloat GetParagraphSpacingAfterGlyph (NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public virtual nfloat GetParagraphSpacingBeforeGlyph (NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public virtual bool ShouldBreakLineByHyphenatingBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual bool ShouldBreakLineByWordBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual uint ShouldGenerateGlyphs (NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, NSFont aFont, Foundation.NSRange glyphRange);
	public virtual NSControlCharacterAction ShouldUseAction (NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
</pre>

### Type Changed: AppKit.NSLayoutManagerDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void DidChangeGeometry (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, CoreGraphics.CGSize oldSize);
	public static CoreGraphics.CGRect GetBoundingBox (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, CoreGraphics.CGRect proposedRect, CoreGraphics.CGPoint glyphPosition, uint charIndex);
	public static nfloat GetLineSpacingAfterGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public static nfloat GetParagraphSpacingAfterGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public static nfloat GetParagraphSpacingBeforeGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, CoreGraphics.CGRect rect);
	public static bool ShouldBreakLineByHyphenatingBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static bool ShouldBreakLineByWordBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static uint ShouldGenerateGlyphs (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, NSFont aFont, Foundation.NSRange glyphRange);
	public static NSControlCharacterAction ShouldUseAction (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
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

### Type Changed: AppKit.NSMenu

Added property:

<pre style='color: green'>
	public virtual NSUserInterfaceLayoutDirection UserInterfaceLayoutDirection { get; set; }
</pre>

### Type Changed: AppKit.NSMutableParagraphStyle

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
</pre>

### Type Changed: AppKit.NSOutlineView

Added method:

<pre style='color: green'>
	public virtual nint GetChildIndex (Foundation.NSObject item);
</pre>

### Type Changed: AppKit.NSOutlineViewDelegate

Obsoleted methods:

```
[Obsolete ()]
	public virtual NSView ViewForTableColumn (NSOutlineView outlineView, NSTableColumn tableColumn, Foundation.NSObject item);
```

### Type Changed: AppKit.NSOutlineViewDelegate_Extensions

Obsoleted methods:

```
[Obsolete ()]
	public static NSView ViewForTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, Foundation.NSObject item);
```

### Type Changed: AppKit.NSParagraphStyle

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; }
</pre>

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

### Type Changed: AppKit.NSPopover

Added property:

<pre style='color: green'>
	public virtual bool Detached { get; }
</pre>

### Type Changed: AppKit.NSPopoverDelegate

Added method:

<pre style='color: green'>
	public virtual void DidDetach (NSPopover popover);
</pre>

### Type Changed: AppKit.NSPopoverDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DidDetach (INSPopoverDelegate This, NSPopover popover);
</pre>

### Type Changed: AppKit.NSResponder

Added method:

<pre style='color: green'>
	public virtual void PressureChange (NSEvent pressureChangeEvent);
</pre>

### Type Changed: AppKit.NSSearchField

Added properties:

<pre style='color: green'>
	public virtual bool CentersPlaceholder { get; set; }
	public INSSearchFieldDelegate Delegate { get; set; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
</pre>

Added events:

<pre style='color: green'>
	public event System.EventHandler SearchingEnded;
	public event System.EventHandler SearchingStarted;
</pre>

Added methods:

<pre style='color: green'>
	public virtual CoreGraphics.CGRect GetRectForCancelButton (bool isCentered);
	public virtual CoreGraphics.CGRect GetRectForSearchButton (bool isCentered);
	public virtual CoreGraphics.CGRect GetRectForSearchText (bool isCentered);
</pre>

### Type Changed: AppKit.NSSegmentedControl

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual NSSegmentSwitchTracking TrackingMode { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual double GetValueForSelectedSegment ();
</pre>

### Type Changed: AppKit.NSSegmentSwitchTracking

Added value:

<pre style='color: green'>
	MomentaryAccelerator = 3,
</pre>

### Type Changed: AppKit.NSSplitView

Added properties:

<pre style='color: green'>
	public virtual NSView[] ArrangedSubviews { get; }
	public virtual bool ArrangesAllSubviews { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddArrangedSubview (NSView view);
	public virtual void InsertArrangedSubview (NSView view, nint index);
	public virtual void RemoveArrangedSubview (NSView view);
</pre>

### Type Changed: AppKit.NSSplitViewController

Added properties:

<pre style='color: green'>
	public static nfloat AutomaticDimension { get; }
	public virtual nfloat MinimumThicknessForInlineSidebars { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ToggleSidebar (Foundation.NSObject sender);
</pre>

### Type Changed: AppKit.NSSplitViewItem

Added properties:

<pre style='color: green'>
	public virtual nfloat AutomaticMaximumThickness { get; set; }
	public virtual NSSplitViewItemBehavior Behavior { get; }
	public virtual nfloat MaximumThickness { get; set; }
	public virtual nfloat MinimumThickness { get; set; }
	public virtual nfloat PreferredThicknessFraction { get; set; }
	public virtual bool SpringLoaded { get; set; }
	public static nfloat UnspecifiedDimension { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSSplitViewItem CreateContentList (NSViewController viewController);
	public static NSSplitViewItem CreateSidebar (NSViewController viewController);
</pre>

### Type Changed: AppKit.NSStackView

Added properties:

<pre style='color: green'>
	public virtual NSView[] ArrangedSubviews { get; }
	public virtual bool DetachesHiddenViews { get; set; }
	public virtual NSStackViewDistribution Distribution { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddArrangedSubview (NSView view);
	public virtual void InsertArrangedSubview (NSView view, nint index);
	public virtual void RemoveArrangedSubview (NSView view);
</pre>

### Type Changed: AppKit.NSTableView

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSIndexSet HiddenRowIndexes { get; }
	public NSTableViewRowActionsGetter RowActions { get; set; }
	public virtual bool RowActionsVisible { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void HideRows (Foundation.NSIndexSet indexes, NSTableViewAnimation rowAnimation);
	public virtual void UnhideRows (Foundation.NSIndexSet indexes, NSTableViewAnimation rowAnimation);
</pre>

### Type Changed: AppKit.NSTableViewDelegate

Added method:

<pre style='color: green'>
	public virtual NSTableViewRowAction[] RowActions (NSTableView tableView, nint row, NSTableRowActionEdge edge);
</pre>

### Type Changed: AppKit.NSTableViewDelegate_Extensions

Added method:

<pre style='color: green'>
	public static NSTableViewRowAction[] RowActions (INSTableViewDelegate This, NSTableView tableView, nint row, NSTableRowActionEdge edge);
</pre>

### Type Changed: AppKit.NSTableViewSource

Removed interface:

<pre style='color: red'>
	INSTableViewSource
</pre>

### Type Changed: AppKit.NSTextAttachment

Added constructor:

<pre style='color: green'>
	public NSTextAttachment (Foundation.NSData contentData, string uti);
</pre>

Added properties:

<pre style='color: green'>
	public virtual CoreGraphics.CGRect Bounds { get; set; }
	public virtual Foundation.NSData Contents { get; set; }
	public virtual string FileType { get; set; }
	public virtual NSImage Image { get; set; }
</pre>

### Type Changed: AppKit.NSTextContainer

Added properties:

<pre style='color: green'>
	public virtual NSBezierPath[] ExclusionPaths { get; set; }
	public virtual NSLineBreakMode LineBreakMode { get; set; }
	public virtual uint MaximumNumberOfLines { get; set; }
	public virtual CoreGraphics.CGSize Size { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSTextContainer FromContainerSize (CoreGraphics.CGSize containerSize);
	public static NSTextContainer FromSize (CoreGraphics.CGSize size);
	public virtual CoreGraphics.CGRect GetLineFragmentRect (CoreGraphics.CGRect proposedRect, uint characterIndex, NSWritingDirection baseWritingDirection, ref CoreGraphics.CGRect remainingRect);
</pre>

### Type Changed: AppKit.NSTextField

Added properties:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
	public virtual nint MaximumNumberOfLines { get; set; }
</pre>

### Type Changed: AppKit.NSTextStorage

Added events:

<pre style='color: green'>
	public event System.EventHandler&lt;NSTextStorageEventArgs&gt; DidProcessEditing;
	public event System.EventHandler&lt;NSTextStorageEventArgs&gt; WillProcessEditing;
</pre>

### Type Changed: AppKit.NSTextStorageDelegate

Added methods:

<pre style='color: green'>
	public virtual void DidProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, Foundation.NSRange editedRange, nint delta);
	public virtual void WillProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, Foundation.NSRange editedRange, nint delta);
</pre>

### Type Changed: AppKit.NSTextStorageDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void DidProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, Foundation.NSRange editedRange, nint delta);
	public static void WillProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, Foundation.NSRange editedRange, nint delta);
</pre>

### Type Changed: AppKit.NSTextTab

Added method:

<pre style='color: green'>
	public static Foundation.NSCharacterSet GetColumnTerminators (Foundation.NSLocale locale);
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

### Type Changed: AppKit.NSUnderlineStyle

Added values:

<pre style='color: green'>
	ByWord = 32768,
	PatternDash = 512,
	PatternDashDot = 768,
	PatternDashDotDot = 1024,
	PatternDot = 256,
	PatternSolid = 0,
</pre>

### Type Changed: AppKit.NSView

Added properties:

<pre style='color: green'>
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public virtual NSLayoutYAxisAnchor FirstBaselineAnchor { get; }
	public virtual nfloat FirstBaselineOffsetFromTop { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public virtual NSLayoutYAxisAnchor LastBaselineAnchor { get; }
	public virtual nfloat LastBaselineOffsetFromBottom { get; }
	public virtual NSLayoutGuide[] LayoutGuides { get; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public static nfloat NoIntrinsicMetric { get; }
	public virtual NSPressureConfiguration PressureConfiguration { get; set; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
</pre>

Modified methods:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes items, NSEvent evnt, INSDraggingSource source)
```

Added methods:

<pre style='color: green'>
	public virtual void AddLayoutGuide (NSLayoutGuide guide);
	public virtual void BeginDocument ();
	public virtual void BeginPage (CoreGraphics.CGRect rect, CoreGraphics.CGPoint placement);
	public virtual void DidCloseMenu (NSMenu menu, NSEvent theEvent);
	public virtual void EndDocument ();
	public virtual void EndPage ();
	public virtual void RemoveLayoutGuide (NSLayoutGuide guide);
	public virtual void WillOpenMenu (NSMenu menu, NSEvent theEvent);
</pre>

### Type Changed: AppKit.NSWindow

Added properties:

<pre style='color: green'>
	public virtual CoreGraphics.CGSize MaxFullScreenContentSize { get; set; }
	public virtual CoreGraphics.CGSize MinFullScreenContentSize { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void PerformWindowDrag (NSEvent theEvent);
</pre>

### Type Changed: AppKit.NSWindowCollectionBehavior

Added values:

<pre style='color: green'>
	FullScreenAllowsTiling = 2048,
	FullScreenDisallowsTiling = 4096,
</pre>

### Type Changed: AppKit.NSWorkspace

Added method:

<pre style='color: green'>
	public virtual bool OpenUrls (Foundation.NSUrl[] urls, string bundleIdentifier, NSWorkspaceLaunchOptions options, Foundation.NSAppleEventDescriptor descriptor);
</pre>

### Removed Type  <span style='color: red'>AppKit.INSTableViewSource</span>

### Removed Type  <span style='color: red'>AppKit.NSTableViewSource_Extensions</span>

### New Type AppKit.INSAlignmentFeedbackToken

<pre style='color: green'>
public interface INSAlignmentFeedbackToken : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.INSCollectionViewDataSource

<pre style='color: green'>
public interface INSCollectionViewDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual NSCollectionViewItem GetItem (NSCollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual nint GetNumberofItems (NSCollectionView collectionView, nint section);
}
</pre>

### New Type AppKit.INSCollectionViewDelegateFlowLayout

<pre style='color: green'>
public interface INSCollectionViewDelegateFlowLayout : INSCollectionViewDelegate, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.INSCollectionViewElement

<pre style='color: green'>
public interface INSCollectionViewElement : INSUserInterfaceItemIdentification, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.INSHapticFeedbackPerformer

<pre style='color: green'>
public interface INSHapticFeedbackPerformer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void PerformFeedback (NSHapticFeedbackPattern pattern, NSHapticFeedbackPerformanceTime performanceTime);
}
</pre>

### New Type AppKit.INSSearchFieldDelegate

<pre style='color: green'>
public interface INSSearchFieldDelegate : INSTextFieldDelegate, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.INSSpringLoadingDestination

<pre style='color: green'>
public interface INSSpringLoadingDestination : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Activated (bool activated, NSDraggingInfo draggingInfo);
	public virtual void HighlightChanged (NSDraggingInfo draggingInfo);
}
</pre>

### New Type AppKit.INSTextAttachmentContainer

<pre style='color: green'>
public interface INSTextAttachmentContainer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual CoreGraphics.CGRect GetAttachmentBounds (NSTextContainer textContainer, CoreGraphics.CGRect lineFrag, CoreGraphics.CGPoint position, uint charIndex);
	public virtual NSImage GetImage (CoreGraphics.CGRect imageBounds, NSTextContainer textContainer, uint charIndex);
}
</pre>

### New Type AppKit.INSTextInputClient

<pre style='color: green'>
public interface INSTextInputClient : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.NSAlignmentFeedbackFilter

<pre style='color: green'>
public class NSAlignmentFeedbackFilter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSAlignmentFeedbackFilter ();
	protected NSAlignmentFeedbackFilter (Foundation.NSObjectFlag t);
	protected NSAlignmentFeedbackFilter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static NSEventMask InputEventMask { get; }
	// methods
	public virtual INSAlignmentFeedbackToken GetTokenForHorizontalMovement (NSView view, nfloat previousX, nfloat alignedX, nfloat defaultX);
	public virtual INSAlignmentFeedbackToken GetTokenForMovement (NSView view, CoreGraphics.CGPoint previousPoint, CoreGraphics.CGPoint alignedPoint, CoreGraphics.CGPoint defaultPoint);
	public virtual INSAlignmentFeedbackToken GetTokenForVerticalMovement (NSView view, nfloat previousY, nfloat alignedY, nfloat defaultY);
	public virtual void PerformFeedback (INSAlignmentFeedbackToken[] tokens, NSHapticFeedbackPerformanceTime performanceTime);
	public virtual void Update (NSEvent theEvent);
	public virtual void Update (NSPanGestureRecognizer panRecognizer);
}
</pre>

### New Type AppKit.NSAlignmentFeedbackToken

<pre style='color: green'>
public class NSAlignmentFeedbackToken : Foundation.NSObject, INSAlignmentFeedbackToken, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSAlignmentFeedbackToken ();
	protected NSAlignmentFeedbackToken (Foundation.NSObjectFlag t);
	protected NSAlignmentFeedbackToken (IntPtr handle);
}
</pre>

### New Type AppKit.NSAttributedString_NSExtendedStringDrawing

<pre style='color: green'>
public static class NSAttributedString_NSExtendedStringDrawing {
	// methods
	public static CoreGraphics.CGRect BoundingRectWithSize (Foundation.NSAttributedString This, CoreGraphics.CGSize size, Foundation.NSStringDrawingOptions options, NSStringDrawingContext context);
	public static void DrawWithRect (Foundation.NSAttributedString This, CoreGraphics.CGRect rect, Foundation.NSStringDrawingOptions options, NSStringDrawingContext context);
}
</pre>

### New Type AppKit.NSCollectionElementCategory

<pre style='color: green'>
[Serializable]
public enum NSCollectionElementCategory {
	DecorationView = 2,
	InterItemGap = 3,
	Item = 0,
	SupplementaryView = 1,
}
</pre>

### New Type AppKit.NSCollectionElementKind

<pre style='color: green'>
public static class NSCollectionElementKind {
	// properties
	public static Foundation.NSString InterItemGapIndicator { get; }
	public static Foundation.NSString SectionFooter { get; }
	public static Foundation.NSString SectionHeader { get; }
}
</pre>

### New Type AppKit.NSCollectionUpdateAction

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

### New Type AppKit.NSCollectionViewDataSource

<pre style='color: green'>
public abstract class NSCollectionViewDataSource : Foundation.NSObject, INSCollectionViewDataSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSCollectionViewDataSource ();
	protected NSCollectionViewDataSource (Foundation.NSObjectFlag t);
	protected NSCollectionViewDataSource (IntPtr handle);
	// methods
	public virtual NSCollectionViewItem GetItem (NSCollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual nint GetNumberofItems (NSCollectionView collectionView, nint section);
	public virtual nint GetNumberOfSections (NSCollectionView collectionView);
	public virtual NSView GetView (NSCollectionView collectionView, Foundation.NSString kind, Foundation.NSIndexPath indexPath);
}
</pre>

### New Type AppKit.NSCollectionViewDataSource_Extensions

<pre style='color: green'>
public static class NSCollectionViewDataSource_Extensions {
	// methods
	public static nint GetNumberOfSections (INSCollectionViewDataSource This, NSCollectionView collectionView);
	public static NSView GetView (INSCollectionViewDataSource This, NSCollectionView collectionView, Foundation.NSString kind, Foundation.NSIndexPath indexPath);
}
</pre>

### New Type AppKit.NSCollectionViewDelegateFlowLayout

<pre style='color: green'>
public class NSCollectionViewDelegateFlowLayout : Foundation.NSObject, INSCollectionViewDelegate, INSCollectionViewDelegateFlowLayout, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewDelegateFlowLayout ();
	protected NSCollectionViewDelegateFlowLayout (Foundation.NSObjectFlag t);
	protected NSCollectionViewDelegateFlowLayout (IntPtr handle);
	// methods
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, nint index, NSCollectionViewDropOperation dropOperation);
	public virtual bool CanDragItems (NSCollectionView collectionView, Foundation.NSIndexSet indexes, NSEvent evt);
	public virtual bool CanDragItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent);
	public virtual void DisplayingItemEnded (NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public virtual void DisplayingSupplementaryViewEnded (NSCollectionView collectionView, NSView view, string elementKind, Foundation.NSIndexPath indexPath);
	public virtual void DraggingSessionEnded (NSCollectionView collectionView, NSDraggingSession draggingSession, CoreGraphics.CGPoint screenPoint, NSDragOperation dragOperation);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession draggingSession, CoreGraphics.CGPoint screenPoint, Foundation.NSIndexSet indexes);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession session, CoreGraphics.CGPoint screenPoint, Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSEvent theEvent, ref CoreGraphics.CGPoint dragImageOffset);
	public virtual string[] GetNamesOfPromisedFiles (NSCollectionView collectionView, Foundation.NSUrl dropURL, Foundation.NSSet indexPaths);
	public virtual INSPasteboardWriting GetPasteboardWriter (NSCollectionView collectionView, Foundation.NSIndexPath indexPath);
	public virtual NSEdgeInsets InsetForSection (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public virtual void ItemsChanged (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual void ItemsDeselected (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual void ItemsSelected (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual nfloat MinimumInteritemSpacingForSection (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public virtual nfloat MinimumLineSpacing (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public virtual string[] NamesOfPromisedFilesDroppedAtDestination (NSCollectionView collectionView, Foundation.NSUrl dropUrl, Foundation.NSIndexSet indexes);
	public virtual INSPasteboardWriting PasteboardWriterForItem (NSCollectionView collectionView, uint index);
	public virtual CoreGraphics.CGSize ReferenceSizeForFooter (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public virtual CoreGraphics.CGSize ReferenceSizeForHeader (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public virtual Foundation.NSSet ShouldChangeItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual Foundation.NSSet ShouldDeselectItems (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual Foundation.NSSet ShouldSelectItems (NSCollectionView collectionView, Foundation.NSSet indexPaths);
	public virtual CoreGraphics.CGSize SizeForItem (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewTransitionLayout TransitionLayout (NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public virtual void UpdateDraggingItemsForDrag (NSCollectionView collectionView, NSDraggingInfo draggingInfo);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref nint dropIndex, ref NSCollectionViewDropOperation dropOperation);
	public virtual void WillDisplayItem (NSCollectionView collectionView, NSCollectionViewItem item, Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (NSCollectionView collectionView, NSView view, Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public virtual bool WriteItems (NSCollectionView collectionView, Foundation.NSIndexSet indexes, NSPasteboard toPasteboard);
	public virtual bool WriteItems (NSCollectionView collectionView, Foundation.NSSet indexPaths, NSPasteboard pasteboard);
}
</pre>

### New Type AppKit.NSCollectionViewDelegateFlowLayout_Extensions

<pre style='color: green'>
public static class NSCollectionViewDelegateFlowLayout_Extensions {
	// methods
	public static NSEdgeInsets InsetForSection (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public static nfloat MinimumInteritemSpacingForSection (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public static nfloat MinimumLineSpacing (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public static CoreGraphics.CGSize ReferenceSizeForFooter (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public static CoreGraphics.CGSize ReferenceSizeForHeader (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, nint section);
	public static CoreGraphics.CGSize SizeForItem (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, Foundation.NSIndexPath indexPath);
}
</pre>

### New Type AppKit.NSCollectionViewElement

<pre style='color: green'>
public class NSCollectionViewElement : Foundation.NSObject, INSCollectionViewElement, INSUserInterfaceItemIdentification, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewElement ();
	protected NSCollectionViewElement (Foundation.NSObjectFlag t);
	protected NSCollectionViewElement (IntPtr handle);
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

### New Type AppKit.NSCollectionViewElement_Extensions

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

### New Type AppKit.NSCollectionViewFlowLayout

<pre style='color: green'>
public class NSCollectionViewFlowLayout : AppKit.NSCollectionViewLayout, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewFlowLayout ();
	public NSCollectionViewFlowLayout (Foundation.NSCoder coder);
	protected NSCollectionViewFlowLayout (Foundation.NSObjectFlag t);
	protected NSCollectionViewFlowLayout (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGSize EstimatedItemSize { get; set; }
	public virtual CoreGraphics.CGSize FooterReferenceSize { get; set; }
	public virtual CoreGraphics.CGSize HeaderReferenceSize { get; set; }
	public virtual CoreGraphics.CGSize ItemSize { get; set; }
	public virtual nfloat MinimumInteritemSpacing { get; set; }
	public virtual nfloat MinimumLineSpacing { get; set; }
	public virtual NSCollectionViewScrollDirection ScrollDirection { get; set; }
	public virtual NSEdgeInsets SectionInset { get; set; }
}
</pre>

### New Type AppKit.NSCollectionViewFlowLayoutInvalidationContext

<pre style='color: green'>
public class NSCollectionViewFlowLayoutInvalidationContext : AppKit.NSCollectionViewLayoutInvalidationContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewFlowLayoutInvalidationContext ();
	protected NSCollectionViewFlowLayoutInvalidationContext (Foundation.NSObjectFlag t);
	protected NSCollectionViewFlowLayoutInvalidationContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool InvalidateFlowLayoutAttributes { get; set; }
	public virtual bool InvalidateFlowLayoutDelegateMetrics { get; set; }
}
</pre>

### New Type AppKit.NSCollectionViewGridLayout

<pre style='color: green'>
public class NSCollectionViewGridLayout : AppKit.NSCollectionViewLayout, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewGridLayout ();
	public NSCollectionViewGridLayout (Foundation.NSCoder coder);
	protected NSCollectionViewGridLayout (Foundation.NSObjectFlag t);
	protected NSCollectionViewGridLayout (IntPtr handle);
	// properties
	public virtual NSColor[] BackgroundColors { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual NSEdgeInsets Margins { get; set; }
	public virtual CoreGraphics.CGSize MaximumItemSize { get; set; }
	public virtual uint MaximumNumberOfColumns { get; set; }
	public virtual uint MaximumNumberOfRows { get; set; }
	public virtual nfloat MinimumInteritemSpacing { get; set; }
	public virtual CoreGraphics.CGSize MinimumItemSize { get; set; }
	public virtual nfloat MinimumLineSpacing { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSCollectionViewItemHighlightState

<pre style='color: green'>
[Serializable]
public enum NSCollectionViewItemHighlightState {
	AsDropTarget = 3,
	ForDeselection = 2,
	ForSelection = 1,
	None = 0,
}
</pre>

### New Type AppKit.NSCollectionViewLayout

<pre style='color: green'>
public class NSCollectionViewLayout : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewLayout ();
	public NSCollectionViewLayout (Foundation.NSCoder coder);
	protected NSCollectionViewLayout (Foundation.NSObjectFlag t);
	protected NSCollectionViewLayout (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSCollectionView CollectionView { get; }
	public virtual CoreGraphics.CGSize CollectionViewContentSize { get; }
	public static ObjCRuntime.Class InvalidationContextClass { get; }
	public static ObjCRuntime.Class LayoutAttributesClass { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void FinalizeAnimatedBoundsChange ();
	public virtual void FinalizeCollectionViewUpdates ();
	public virtual void FinalizeLayoutTransition ();
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingDecorationElement (Foundation.NSString elementKind, Foundation.NSIndexPath decorationIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingItem (Foundation.NSIndexPath itemIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingSupplementaryElement (Foundation.NSString elementKind, Foundation.NSIndexPath elementIndexPath);
	public virtual Foundation.NSSet GetIndexPathsToDeleteForDecorationView (Foundation.NSString elementKind);
	public virtual Foundation.NSSet GetIndexPathsToDeleteForSupplementaryView (Foundation.NSString elementKind);
	public virtual Foundation.NSSet GetIndexPathsToInsertForDecorationView (Foundation.NSString elementKind);
	public virtual Foundation.NSSet GetIndexPathsToInsertForSupplementaryView (Foundation.NSString elementKind);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingDecorationElement (Foundation.NSString elementKind, Foundation.NSIndexPath decorationIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingItem (Foundation.NSIndexPath itemIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingSupplementaryElement (Foundation.NSString elementKind, Foundation.NSIndexPath elementIndexPath);
	public virtual NSCollectionViewLayoutInvalidationContext GetInvalidationContext (CoreGraphics.CGRect newBounds);
	public virtual NSCollectionViewLayoutInvalidationContext GetInvalidationContext (NSCollectionViewLayoutAttributes preferredAttributes, NSCollectionViewLayoutAttributes originalAttributes);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForDecorationView (Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForDropTarget (CoreGraphics.CGPoint pointInCollectionView);
	public virtual NSCollectionViewLayoutAttributes[] GetLayoutAttributesForElements (CoreGraphics.CGRect rect);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForInterItemGap (Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForItem (Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryView (Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public virtual CoreGraphics.CGPoint GetTargetContentOffset (CoreGraphics.CGPoint proposedContentOffset);
	public virtual CoreGraphics.CGPoint GetTargetContentOffset (CoreGraphics.CGPoint proposedContentOffset, CoreGraphics.CGPoint velocity);
	public virtual void InvalidateLayout ();
	public virtual void InvalidateLayout (NSCollectionViewLayoutInvalidationContext context);
	public virtual void PrepareForAnimatedBoundsChange (CoreGraphics.CGRect oldBounds);
	public virtual void PrepareForCollectionViewUpdates (NSCollectionViewUpdateItem[] updateItems);
	public virtual void PrepareForTransitionFromLayout (NSCollectionViewLayout oldLayout);
	public virtual void PrepareForTransitionToLayout (NSCollectionViewLayout newLayout);
	public virtual void PrepareLayout ();
	public void RegisterClassForDecorationView (System.Type itemClass, Foundation.NSString elementKind);
	public virtual void RegisterNib (NSNib nib, Foundation.NSString elementKind);
	public virtual bool ShouldInvalidateLayout (CoreGraphics.CGRect newBounds);
	public virtual bool ShouldInvalidateLayout (NSCollectionViewLayoutAttributes preferredAttributes, NSCollectionViewLayoutAttributes originalAttributes);
}
</pre>

### New Type AppKit.NSCollectionViewLayoutAttributes

<pre style='color: green'>
public class NSCollectionViewLayoutAttributes : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewLayoutAttributes ();
	protected NSCollectionViewLayoutAttributes (Foundation.NSObjectFlag t);
	protected NSCollectionViewLayoutAttributes (IntPtr handle);
	// properties
	public virtual nfloat Alpha { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGRect Frame { get; set; }
	public virtual bool Hidden { get; set; }
	public virtual Foundation.NSIndexPath IndexPath { get; set; }
	public virtual NSCollectionElementCategory RepresentedElementCategory { get; }
	public virtual string RepresentedElementKind { get; }
	public virtual CoreGraphics.CGSize Size { get; set; }
	public virtual nint ZIndex { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static NSCollectionViewLayoutAttributes CreateForDecorationView (Foundation.NSString decorationViewKind, Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForInterItemGap (Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForItem (Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForSupplementaryView (Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSCollectionViewLayoutInvalidationContext

<pre style='color: green'>
public class NSCollectionViewLayoutInvalidationContext : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewLayoutInvalidationContext ();
	protected NSCollectionViewLayoutInvalidationContext (Foundation.NSObjectFlag t);
	protected NSCollectionViewLayoutInvalidationContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGPoint ContentOffsetAdjustment { get; set; }
	public virtual CoreGraphics.CGSize ContentSizeAdjustment { get; set; }
	public virtual bool InvalidateDataSourceCounts { get; }
	public virtual Foundation.NSDictionary InvalidatedDecorationIndexPaths { get; }
	public virtual Foundation.NSSet InvalidatedItemIndexPaths { get; }
	public virtual Foundation.NSDictionary InvalidatedSupplementaryIndexPaths { get; }
	public virtual bool InvalidateEverything { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void InvalidateDecorationElements (Foundation.NSString elementKind, Foundation.NSSet indexPaths);
	public virtual void InvalidateItems (Foundation.NSSet indexPaths);
	public virtual void InvalidateSupplementaryElements (Foundation.NSString elementKind, Foundation.NSSet indexPaths);
}
</pre>

### New Type AppKit.NSCollectionViewScrollDirection

<pre style='color: green'>
[Serializable]
public enum NSCollectionViewScrollDirection {
	Horizontal = 1,
	Vertical = 0,
}
</pre>

### New Type AppKit.NSCollectionViewScrollPosition

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

### New Type AppKit.NSCollectionViewTransitionLayout

<pre style='color: green'>
public class NSCollectionViewTransitionLayout : AppKit.NSCollectionViewLayout, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewTransitionLayout ();
	public NSCollectionViewTransitionLayout (Foundation.NSCoder coder);
	protected NSCollectionViewTransitionLayout (Foundation.NSObjectFlag t);
	protected NSCollectionViewTransitionLayout (IntPtr handle);
	public NSCollectionViewTransitionLayout (NSCollectionViewLayout currentLayout, NSCollectionViewLayout newLayout);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSCollectionViewLayout CurrentLayout { get; }
	public virtual NSCollectionViewLayout NextLayout { get; }
	public virtual nfloat TransitionProgress { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual nfloat GetValue (string key);
	public virtual void UpdateValue (nfloat value, string key);
}
</pre>

### New Type AppKit.NSCollectionViewUpdateItem

<pre style='color: green'>
public class NSCollectionViewUpdateItem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSCollectionViewUpdateItem ();
	protected NSCollectionViewUpdateItem (Foundation.NSObjectFlag t);
	protected NSCollectionViewUpdateItem (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSIndexPath IndexPathAfterUpdate { get; }
	public virtual Foundation.NSIndexPath IndexPathBeforeUpdate { get; }
	public virtual NSCollectionUpdateAction UpdateAction { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSControlCharacterAction

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

### New Type AppKit.NSDataAsset

<pre style='color: green'>
public class NSDataAsset : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSDataAsset (Foundation.NSObjectFlag t);
	protected NSDataAsset (IntPtr handle);
	public NSDataAsset (string name);
	public NSDataAsset (string name, Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSData Data { get; }
	public virtual string Name { get; }
	public virtual Foundation.NSString TypeIdentifier { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSDictionaryController

<pre style='color: green'>
public class NSDictionaryController : AppKit.NSArrayController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSDictionaryController ();
	public NSDictionaryController (Foundation.NSCoder coder);
	protected NSDictionaryController (Foundation.NSObjectFlag t);
	protected NSDictionaryController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string[] ExcludedKeys { get; set; }
	public virtual string[] IncludedKeys { get; set; }
	public virtual string InitialKey { get; set; }
	public virtual Foundation.NSObject InitialValue { get; set; }
	public virtual Foundation.NSDictionary LocalizedKeyDictionary { get; set; }
	public virtual string LocalizedKeyTable { get; set; }
	public virtual NSDictionaryControllerKeyValuePair NewObject { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSDictionaryControllerKeyValuePair

<pre style='color: green'>
public class NSDictionaryControllerKeyValuePair : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSDictionaryControllerKeyValuePair (Foundation.NSObjectFlag t);
	protected NSDictionaryControllerKeyValuePair (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ExplicitlyIncluded { get; }
	public virtual string Key { get; set; }
	public virtual string LocalizedKey { get; set; }
	public virtual Foundation.NSObject Value { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AppKit.NSExtendedStringDrawing

<pre style='color: green'>
public static class NSExtendedStringDrawing {
	// methods
	public static void DrawString (Foundation.NSString This, CoreGraphics.CGRect rect, Foundation.NSStringDrawingOptions options, NSStringAttributes attributes, NSStringDrawingContext context);
	public static CoreGraphics.CGRect GetBoundingRect (Foundation.NSString This, CoreGraphics.CGSize size, Foundation.NSStringDrawingOptions options, NSStringAttributes attributes, NSStringDrawingContext context);
	public static void WeakDrawString (Foundation.NSString This, CoreGraphics.CGRect rect, Foundation.NSStringDrawingOptions options, Foundation.NSDictionary attributes, NSStringDrawingContext context);
	public static CoreGraphics.CGRect WeakGetBoundingRect (Foundation.NSString This, CoreGraphics.CGSize size, Foundation.NSStringDrawingOptions options, Foundation.NSDictionary attributes, NSStringDrawingContext context);
}
</pre>

### New Type AppKit.NSFontWeight

<pre style='color: green'>
public static class NSFontWeight {
	// properties
	public static nfloat Black { get; }
	public static nfloat Bold { get; }
	public static nfloat Heavy { get; }
	public static nfloat Light { get; }
	public static nfloat Medium { get; }
	public static nfloat Regular { get; }
	public static nfloat Semibold { get; }
	public static nfloat Thin { get; }
	public static nfloat UltraLight { get; }
}
</pre>

### New Type AppKit.NSGlyphProperty

<pre style='color: green'>
[Serializable]
public enum NSGlyphProperty {
	ControlCharacter = 2,
	Elastic = 4,
	NonBaseCharacter = 8,
	Null = 1,
}
</pre>

### New Type AppKit.NSHapticFeedbackManager

<pre style='color: green'>
public class NSHapticFeedbackManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSHapticFeedbackManager ();
	protected NSHapticFeedbackManager (Foundation.NSObjectFlag t);
	protected NSHapticFeedbackManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static INSHapticFeedbackPerformer DefaultPerformer { get; }
}
</pre>

### New Type AppKit.NSHapticFeedbackPattern

<pre style='color: green'>
[Serializable]
public enum NSHapticFeedbackPattern {
	Alignment = 1,
	Generic = 0,
	LevelChange = 2,
}
</pre>

### New Type AppKit.NSHapticFeedbackPerformanceTime

<pre style='color: green'>
[Serializable]
public enum NSHapticFeedbackPerformanceTime {
	Default = 0,
	DrawCompleted = 2,
	Now = 1,
}
</pre>

### New Type AppKit.NSHapticFeedbackPerformer

<pre style='color: green'>
public abstract class NSHapticFeedbackPerformer : Foundation.NSObject, INSHapticFeedbackPerformer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSHapticFeedbackPerformer ();
	protected NSHapticFeedbackPerformer (Foundation.NSObjectFlag t);
	protected NSHapticFeedbackPerformer (IntPtr handle);
	// methods
	public virtual void PerformFeedback (NSHapticFeedbackPattern pattern, NSHapticFeedbackPerformanceTime performanceTime);
}
</pre>

### New Type AppKit.NSLayoutAnchor`1

<pre style='color: green'>
public class NSLayoutAnchor`1 : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSLayoutAnchor`1 (Foundation.NSObjectFlag t);
	protected NSLayoutAnchor`1 (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor, nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor, nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (AppKit.NSLayoutAnchor&lt;AnchorType&gt; anchor, nfloat constant);
}
</pre>

### New Type AppKit.NSLayoutDimension

<pre style='color: green'>
public class NSLayoutDimension : AppKit.NSLayoutAnchor`1[AppKit.NSLayoutDimension], Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSLayoutDimension (Foundation.NSObjectFlag t);
	protected NSLayoutDimension (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintEqualToConstant (nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToConstant (nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToAnchor (NSLayoutDimension anchor, nfloat multiplier, nfloat constant);
	public virtual NSLayoutConstraint ConstraintLessThanOrEqualToConstant (nfloat constant);
}
</pre>

### New Type AppKit.NSLayoutGuide

<pre style='color: green'>
public class NSLayoutGuide : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSLayoutGuide ();
	public NSLayoutGuide (Foundation.NSCoder coder);
	protected NSLayoutGuide (Foundation.NSObjectFlag t);
	protected NSLayoutGuide (IntPtr handle);
	// properties
	public virtual NSLayoutYAxisAnchor BottomAnchor { get; }
	public virtual NSLayoutXAxisAnchor CenterXAnchor { get; }
	public virtual NSLayoutYAxisAnchor CenterYAnchor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGRect Frame { get; }
	public virtual NSLayoutDimension HeightAnchor { get; }
	public virtual string Identifier { get; set; }
	public virtual NSLayoutXAxisAnchor LeadingAnchor { get; }
	public virtual NSLayoutXAxisAnchor LeftAnchor { get; }
	public virtual NSView OwningView { get; set; }
	public virtual NSLayoutXAxisAnchor RightAnchor { get; }
	public virtual NSLayoutYAxisAnchor TopAnchor { get; }
	public virtual NSLayoutXAxisAnchor TrailingAnchor { get; }
	public virtual NSLayoutDimension WidthAnchor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type AppKit.NSLayoutXAxisAnchor

<pre style='color: green'>
public class NSLayoutXAxisAnchor : AppKit.NSLayoutAnchor`1[AppKit.NSLayoutXAxisAnchor], Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSLayoutXAxisAnchor (Foundation.NSObjectFlag t);
	protected NSLayoutXAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type AppKit.NSLayoutYAxisAnchor

<pre style='color: green'>
public class NSLayoutYAxisAnchor : AppKit.NSLayoutAnchor`1[AppKit.NSLayoutYAxisAnchor], Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSLayoutYAxisAnchor (Foundation.NSObjectFlag t);
	protected NSLayoutYAxisAnchor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type AppKit.NSPressureBehavior

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

### New Type AppKit.NSPressureConfiguration

<pre style='color: green'>
public class NSPressureConfiguration : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSPressureConfiguration ();
	public NSPressureConfiguration (NSPressureBehavior pressureBehavior);
	protected NSPressureConfiguration (Foundation.NSObjectFlag t);
	protected NSPressureConfiguration (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSPressureBehavior PressureBehavior { get; }
	// methods
	public virtual void Set ();
}
</pre>

### New Type AppKit.NSSearchFieldDelegate

<pre style='color: green'>
public class NSSearchFieldDelegate : Foundation.NSObject, INSSearchFieldDelegate, INSTextFieldDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSSearchFieldDelegate ();
	protected NSSearchFieldDelegate (Foundation.NSObjectFlag t);
	protected NSSearchFieldDelegate (IntPtr handle);
	// methods
	public virtual void Changed (Foundation.NSNotification notification);
	public virtual bool DidFailToFormatString (NSControl control, string str, string error);
	public virtual void DidFailToValidatePartialString (NSControl control, string str, string error);
	public virtual bool DoCommandBySelector (NSControl control, NSTextView textView, ObjCRuntime.Selector commandSelector);
	public virtual void EditingBegan (Foundation.NSNotification notification);
	public virtual void EditingEnded (Foundation.NSNotification notification);
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
	public virtual bool IsValidObject (NSControl control, Foundation.NSObject objectToValidate);
	public virtual void SearchingEnded (NSSearchField sender);
	public virtual void SearchingStarted (NSSearchField sender);
	public virtual bool TextShouldBeginEditing (NSControl control, NSText fieldEditor);
	public virtual bool TextShouldEndEditing (NSControl control, NSText fieldEditor);
}
</pre>

### New Type AppKit.NSSearchFieldDelegate_Extensions

<pre style='color: green'>
public static class NSSearchFieldDelegate_Extensions {
	// methods
	public static void SearchingEnded (INSSearchFieldDelegate This, NSSearchField sender);
	public static void SearchingStarted (INSSearchFieldDelegate This, NSSearchField sender);
}
</pre>

### New Type AppKit.NSSplitViewItemBehavior

<pre style='color: green'>
[Serializable]
public enum NSSplitViewItemBehavior {
	ContentList = 2,
	Default = 0,
	Sidebar = 1,
}
</pre>

### New Type AppKit.NSSpringLoadingDestination

<pre style='color: green'>
public abstract class NSSpringLoadingDestination : Foundation.NSObject, INSSpringLoadingDestination, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSSpringLoadingDestination ();
	protected NSSpringLoadingDestination (Foundation.NSObjectFlag t);
	protected NSSpringLoadingDestination (IntPtr handle);
	// methods
	public virtual void Activated (bool activated, NSDraggingInfo draggingInfo);
	public virtual void DraggingEnded (NSDraggingInfo draggingInfo);
	public virtual NSSpringLoadingOptions Entered (NSDraggingInfo draggingInfo);
	public virtual void Exited (NSDraggingInfo draggingInfo);
	public virtual void HighlightChanged (NSDraggingInfo draggingInfo);
	public virtual NSSpringLoadingOptions Updated (NSDraggingInfo draggingInfo);
}
</pre>

### New Type AppKit.NSSpringLoadingDestination_Extensions

<pre style='color: green'>
public static class NSSpringLoadingDestination_Extensions {
	// methods
	public static void DraggingEnded (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static NSSpringLoadingOptions Entered (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static void Exited (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static NSSpringLoadingOptions Updated (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
}
</pre>

### New Type AppKit.NSSpringLoadingHighlight

<pre style='color: green'>
[Serializable]
public enum NSSpringLoadingHighlight {
	Emphasized = 2,
	None = 0,
	Standard = 1,
}
</pre>

### New Type AppKit.NSSpringLoadingOptions

<pre style='color: green'>
[Serializable]
public enum NSSpringLoadingOptions {
	ContinuousActivation = 2,
	Disabled = 0,
	Enabled = 1,
	NoHover = 8,
}
</pre>

### New Type AppKit.NSStackViewDistribution

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

### New Type AppKit.NSStepperCell

<pre style='color: green'>
public class NSStepperCell : AppKit.NSActionCell, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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

### New Type AppKit.NSStringDrawingContext

<pre style='color: green'>
public class NSStringDrawingContext : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSStringDrawingContext ();
	protected NSStringDrawingContext (Foundation.NSObjectFlag t);
	protected NSStringDrawingContext (IntPtr handle);
	// properties
	public virtual nfloat ActualScaleFactor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual nfloat MinimumScaleFactor { get; set; }
	public virtual CoreGraphics.CGRect TotalBounds { get; }
}
</pre>

### New Type AppKit.NSTableRowActionEdge

<pre style='color: green'>
[Serializable]
public enum NSTableRowActionEdge {
	Leading = 0,
	Trailing = 1,
}
</pre>

### New Type AppKit.NSTableViewRowAction

<pre style='color: green'>
public class NSTableViewRowAction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSTableViewRowAction ();
	protected NSTableViewRowAction (Foundation.NSObjectFlag t);
	protected NSTableViewRowAction (IntPtr handle);
	// properties
	public virtual NSColor BackgroundColor { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual NSTableViewRowActionStyle Style { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static NSTableViewRowAction FromStyle (NSTableViewRowActionStyle style, string title, System.Action&lt;NSTableViewRowAction,System.nint&gt; handler);
}
</pre>

### New Type AppKit.NSTableViewRowActionsGetter

<pre style='color: green'>
public sealed delegate NSTableViewRowActionsGetter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTableViewRowActionsGetter (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSTableView tableView, nint row, NSTableRowActionEdge edge, System.AsyncCallback callback, object object);
	public virtual NSTableViewRowAction[] EndInvoke (System.IAsyncResult result);
	public virtual NSTableViewRowAction[] Invoke (NSTableView tableView, nint row, NSTableRowActionEdge edge);
}
</pre>

### New Type AppKit.NSTableViewRowActionStyle

<pre style='color: green'>
[Serializable]
public enum NSTableViewRowActionStyle {
	Destructive = 1,
	Regular = 0,
}
</pre>

### New Type AppKit.NSTextAttachmentContainer

<pre style='color: green'>
public abstract class NSTextAttachmentContainer : Foundation.NSObject, INSTextAttachmentContainer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NSTextAttachmentContainer ();
	protected NSTextAttachmentContainer (Foundation.NSObjectFlag t);
	protected NSTextAttachmentContainer (IntPtr handle);
	// methods
	public virtual CoreGraphics.CGRect GetAttachmentBounds (NSTextContainer textContainer, CoreGraphics.CGRect lineFrag, CoreGraphics.CGPoint position, uint charIndex);
	public virtual NSImage GetImage (CoreGraphics.CGRect imageBounds, NSTextContainer textContainer, uint charIndex);
}
</pre>

### New Type AppKit.NSTextInputClient

<pre style='color: green'>
public class NSTextInputClient : Foundation.NSObject, INSTextInputClient, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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

### New Type AppKit.NSTextLayoutEnumerateEnclosingRects

<pre style='color: green'>
public sealed delegate NSTextLayoutEnumerateEnclosingRects : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTextLayoutEnumerateEnclosingRects (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CoreGraphics.CGRect rect, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (CoreGraphics.CGRect rect, out bool stop);
}
</pre>

### New Type AppKit.NSTextLayoutEnumerateLineFragments

<pre style='color: green'>
public sealed delegate NSTextLayoutEnumerateLineFragments : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTextLayoutEnumerateLineFragments (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CoreGraphics.CGRect rect, CoreGraphics.CGRect usedRectangle, NSTextContainer textContainer, Foundation.NSRange glyphRange, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (CoreGraphics.CGRect rect, CoreGraphics.CGRect usedRectangle, NSTextContainer textContainer, Foundation.NSRange glyphRange, out bool stop);
}
</pre>

### New Type AppKit.NSTextStorageEditActions

<pre style='color: green'>
[Serializable]
public enum NSTextStorageEditActions {
	Attributes = 1,
	Characters = 2,
}
</pre>

### New Type AppKit.NSTextStorageEventArgs

<pre style='color: green'>
public class NSTextStorageEventArgs : System.EventArgs {
	// constructors
	public NSTextStorageEventArgs (NSTextStorageEditActions editedMask, Foundation.NSRange editedRange, nint delta);
	// properties
	public nint Delta { get; set; }
	public NSTextStorageEditActions EditedMask { get; set; }
	public Foundation.NSRange EditedRange { get; set; }
}
</pre>

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioChannelLayoutTagExtensions

Added method:

<pre style='color: green'>
	public static uint GetNumberOfChannels (AudioChannelLayoutTag inLayoutTag);
</pre>

### Type Changed: AudioToolbox.AudioFormatFlags

Added values:

<pre style='color: green'>
	CafIsFloat = 1,
	CafIsLittleEndian = 2,
</pre>

### Type Changed: AudioToolbox.AudioFormatType

Added value:

<pre style='color: green'>
	EnhancedAES3 = 1700998451,
</pre>

### Type Changed: AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: AudioToolbox.AudioTimeStamp

### Type Changed: AudioToolbox.AudioTimeStamp.AtsFlags

Added field:

<pre style='color: green'>
	public static const AudioTimeStamp.AtsFlags NothingValid;
</pre>

### Type Changed: AudioToolbox.SmpteTime

Added properties:

<pre style='color: green'>
	public SmpteTimeFlags FlagsStrong { get; set; }
	public SmpteTimeType TypeStrong { get; set; }
</pre>

### Type Changed: AudioToolbox.SystemSound

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

### New Type AudioToolbox.MPEG4ObjectID

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

### New Type AudioToolbox.SmpteTimeFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum SmpteTimeFlags {
	TimeRunning = 2,
	TimeValid = 1,
	Unknown = 0,
}
</pre>

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioComponent

Added method:

<pre style='color: green'>
	public AppKit.NSImage GetIcon ();
</pre>

### Type Changed: AudioUnit.AudioComponentFlag

Added values:

<pre style='color: green'>
	CanLoadInProcess = 16,
	IsV3AudioUnit = 4,
	RequiresAsyncInstantiation = 8,
</pre>

### Type Changed: AudioUnit.AudioTypeConverter

Added value:

<pre style='color: green'>
	MultiSplitter = 1836281964,
</pre>

### Type Changed: AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete ()]
	public void SetAudioFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: AudioUnit.AudioUnitPropertyIDType

Added values:

<pre style='color: green'>
	ParametersForOverview = 57,
	RequestViewController = 56,
</pre>

### Type Changed: AudioUnit.ExtAudioFile

Modified properties:

```
public AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

### New Type AudioUnit.AU3DMixerAttenuationCurve

<pre style='color: green'>
[Serializable]
public enum AU3DMixerAttenuationCurve {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
</pre>

### New Type AudioUnit.AU3DMixerRenderingFlags

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

### New Type AudioUnit.AUAudioUnit

<pre style='color: green'>
public class AUAudioUnit : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AUAudioUnit (Foundation.NSObjectFlag t);
	protected AUAudioUnit (IntPtr handle);
	public AUAudioUnit (AudioComponentDescription componentDescription, out Foundation.NSError outError);
	public AUAudioUnit (AudioComponentDescription componentDescription, AudioComponentInstantiationOptions options, out Foundation.NSError outError);
	// properties
	public virtual bool AllParameterValues { get; }
	public static Foundation.NSString AudioComponentInstanceInvalidationNotification { get; }
	public static Foundation.NSString AudioComponentRegistrationsChangedNotification { get; }
	public virtual string AudioUnitName { get; }
	public virtual bool CanProcessInPlace { get; }
	public virtual Foundation.NSNumber[] ChannelCapabilities { get; }
	public override IntPtr ClassHandle { get; }
	public virtual AudioComponent Component { get; }
	public virtual AudioComponentDescription ComponentDescription { get; }
	public virtual string ComponentName { get; }
	public virtual uint ComponentVersion { get; }
	public virtual string ContextName { get; set; }
	public virtual AUAudioUnitPreset CurrentPreset { get; set; }
	public virtual AUAudioUnitPreset[] FactoryPresets { get; }
	public virtual Foundation.NSDictionary FullState { get; set; }
	public virtual Foundation.NSDictionary FullStateForDocument { get; set; }
	public virtual AUAudioUnitBusArray InputBusses { get; }
	public virtual double Latency { get; }
	public virtual string ManufacturerName { get; }
	public virtual uint MaximumFramesToRender { get; set; }
	public virtual bool MusicDeviceOrEffect { get; }
	public virtual AUAudioUnitBusArray OutputBusses { get; }
	public virtual AUParameterTree ParameterTree { get; }
	public virtual bool RenderingOffline { get; set; }
	public virtual nint RenderQuality { get; set; }
	public virtual bool RenderResourcesAllocated { get; }
	public virtual bool ShouldBypassEffect { get; set; }
	public virtual double TailTime { get; }
	public virtual nint VirtualMidiCableCount { get; }
	// methods
	public virtual bool AllocateRenderResources (out Foundation.NSError outError);
	public virtual void DeallocateRenderResources ();
	protected override void Dispose (bool disposing);
	public static void FromComponentDescription (AudioComponentDescription componentDescription, AudioComponentInstantiationOptions options, System.Action&lt;AUAudioUnit,Foundation.NSError&gt; completionHandler);
	public virtual Foundation.NSNumber[] GetParametersForOverview (nint count);
	public static void RegisterSubclass (ObjCRuntime.Class cls, AudioComponentDescription componentDescription, string name, uint version);
	public virtual void RemoveRenderObserver (nint token);
	public virtual void RequestViewController (System.Action&lt;AppKit.NSViewController&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;AppKit.NSViewController&gt; RequestViewControllerAsync ();
	public virtual void Reset ();
	public virtual void SetRenderResourcesAllocated (bool flag);
	public virtual bool ShouldChangeToFormat (AVFoundation.AVAudioFormat format, AUAudioUnitBus bus);

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveAudioComponentInstanceInvalidation (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
		public static Foundation.NSObject ObserveAudioComponentRegistrationsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type AudioUnit.AUAudioUnit_AUAudioInputOutputUnit

<pre style='color: green'>
public static class AUAudioUnit_AUAudioInputOutputUnit {
	// methods
	public static bool CanPerformOutput (AUAudioUnit This);
	public static bool GetCanPerformInput (AUAudioUnit This);
	public static bool IsInputEnabled (AUAudioUnit This);
	public static bool IsOutputEnabled (AUAudioUnit This);
	public static bool SetInputEnabled (AUAudioUnit This, bool enabled);
	public static bool SetOutputEnabled (AUAudioUnit This, bool enabled);
	public static bool StartHardware (AUAudioUnit This, out Foundation.NSError outError);
	public static void StopHardware (AUAudioUnit This);
}
</pre>

### New Type AudioUnit.AUAudioUnitBus

<pre style='color: green'>
public class AUAudioUnitBus : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUAudioUnitBus ();
	protected AUAudioUnitBus (Foundation.NSObjectFlag t);
	protected AUAudioUnitBus (IntPtr handle);
	public AUAudioUnitBus (AVFoundation.AVAudioFormat format, out Foundation.NSError outError);
	// properties
	public virtual AUAudioUnitBusType BusType { get; }
	public override IntPtr ClassHandle { get; }
	public virtual double ContextPresentationLatency { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual AVFoundation.AVAudioFormat Format { get; }
	public virtual uint Index { get; }
	public virtual uint MaximumChannelCount { get; set; }
	public virtual string Name { get; set; }
	public virtual AUAudioUnit OwnerAudioUnit { get; }
	public virtual Foundation.NSNumber[] SupportedChannelCounts { get; set; }
	public virtual Foundation.NSNumber[] SupportedChannelLayoutTags { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool SetFormat (AVFoundation.AVAudioFormat format, out Foundation.NSError outError);
}
</pre>

### New Type AudioUnit.AUAudioUnitBusArray

<pre style='color: green'>
public class AUAudioUnitBusArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AUAudioUnitBusArray (Foundation.NSObjectFlag t);
	protected AUAudioUnitBusArray (IntPtr handle);
	public AUAudioUnitBusArray (AUAudioUnit owner, AUAudioUnitBusType busType);
	public AUAudioUnitBusArray (AUAudioUnit owner, AUAudioUnitBusType busType, AUAudioUnitBus[] busArray);
	// properties
	public virtual AUAudioUnitBusType BusType { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual bool CountChangeable { get; }
	public virtual AUAudioUnit OwnerAudioUnit { get; }
	// methods
	public virtual void AddObserver (Foundation.NSObject observer, string keyPath, Foundation.NSKeyValueObservingOptions options, IntPtr context);
	protected override void Dispose (bool disposing);
	public virtual AUAudioUnitBus GetObject (uint index);
	public virtual void RemoveObserver (Foundation.NSObject observer, string keyPath, IntPtr context);
	public virtual void ReplaceBusses (AUAudioUnitBus[] busArray);
	public virtual bool SetBusCount (uint count, out Foundation.NSError outError);
}
</pre>

### New Type AudioUnit.AUAudioUnitBusType

<pre style='color: green'>
[Serializable]
public enum AUAudioUnitBusType {
	Input = 1,
	Output = 2,
}
</pre>

### New Type AudioUnit.AUAudioUnitPreset

<pre style='color: green'>
public class AUAudioUnitPreset : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUAudioUnitPreset ();
	public AUAudioUnitPreset (Foundation.NSCoder coder);
	protected AUAudioUnitPreset (Foundation.NSObjectFlag t);
	protected AUAudioUnitPreset (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual nint Number { get; set; }
	// methods
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type AudioUnit.AudioComponentConfigurationInfo

<pre style='color: green'>
public static class AudioComponentConfigurationInfo {
	// fields
	public static Foundation.NSString ValidationResult;
}
</pre>

### New Type AudioUnit.AudioComponentInstantiationOptions

<pre style='color: green'>
[Serializable]
public enum AudioComponentInstantiationOptions {
	InProcess = 2,
	OutOfProcess = 1,
}
</pre>

### New Type AudioUnit.AudioComponentValidationParameter

<pre style='color: green'>
public static class AudioComponentValidationParameter {
	// fields
	public static Foundation.NSString ForceValidation;
	public static Foundation.NSString TimeOut;
}
</pre>

### New Type AudioUnit.AudioComponentValidationResult

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

### New Type AudioUnit.AudioUnitBusType

<pre style='color: green'>
[Serializable]
public enum AudioUnitBusType {
	Input = 1,
	Output = 2,
}
</pre>

### New Type AudioUnit.AudioUnitConfigurationInfo

<pre style='color: green'>
public static class AudioUnitConfigurationInfo {
	// fields
	public static Foundation.NSString BusCountWritable;
	public static Foundation.NSString ChannelConfigurations;
	public static Foundation.NSString HasCustomView;
	public static Foundation.NSString IconUrl;
	public static Foundation.NSString InitialInputs;
	public static Foundation.NSString SupportedChannelLayoutTags;
}
</pre>

### New Type AudioUnit.AudioUnitParameterOptions

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

### New Type AudioUnit.AudioUnitSubType

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

### New Type AudioUnit.AUEventSampleTime

<pre style='color: green'>
[Serializable]
public enum AUEventSampleTime {
	Immediate = 0,
}
</pre>

### New Type AudioUnit.AUHostTransportStateFlags

<pre style='color: green'>
[Serializable]
public enum AUHostTransportStateFlags {
	Changed = 1,
	Cycling = 8,
	Moving = 2,
	Recording = 4,
}
</pre>

### New Type AudioUnit.AUParameter

<pre style='color: green'>
public class AUParameter : AudioUnit.AUParameterNode, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUParameter ();
	public AUParameter (Foundation.NSCoder coder);
	protected AUParameter (Foundation.NSObjectFlag t);
	protected AUParameter (IntPtr handle);
	// properties
	public virtual ulong Address { get; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSNumber[] DependentParameters { get; }
	public virtual AudioUnitParameterOptions Flags { get; }
	public virtual float MaxValue { get; }
	public virtual float MinValue { get; }
	public virtual AudioUnitParameterUnit Unit { get; }
	public virtual string UnitName { get; }
	public virtual float Value { get; set; }
	public virtual string[] ValueStrings { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual string GetString (ref float value);
	public virtual float GetValue (string str);
	public virtual void SetValue (float value, IntPtr originator);
	public virtual void SetValue (float value, IntPtr originator, ulong hostTime);
}
</pre>

### New Type AudioUnit.AUParameterGroup

<pre style='color: green'>
public class AUParameterGroup : AudioUnit.AUParameterNode, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUParameterGroup ();
	public AUParameterGroup (Foundation.NSCoder coder);
	protected AUParameterGroup (Foundation.NSObjectFlag t);
	protected AUParameterGroup (IntPtr handle);
	// properties
	public virtual AUParameter[] AllParameters { get; }
	public virtual AUParameterNode[] Children { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type AudioUnit.AUParameterNode

<pre style='color: green'>
public class AUParameterNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUParameterNode ();
	protected AUParameterNode (Foundation.NSObjectFlag t);
	protected AUParameterNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string DisplayName { get; }
	public virtual string Identifier { get; }
	public virtual string KeyPath { get; }
	// methods
	public virtual string GetDisplayName (nint maximumLength);
	public virtual void RemoveParameterObserver (IntPtr token);
}
</pre>

### New Type AudioUnit.AUParameterTree

<pre style='color: green'>
public class AUParameterTree : AudioUnit.AUParameterGroup, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUParameterTree ();
	public AUParameterTree (Foundation.NSCoder coder);
	protected AUParameterTree (Foundation.NSObjectFlag t);
	protected AUParameterTree (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static AUParameterGroup CreateGroup (string identifier, string name, AUParameterNode[] children);
	public static AUParameterGroup CreateGroup (AUParameterGroup templateGroup, string identifier, string name, ulong addressOffset);
	public static AUParameterGroup CreateGroupTemplate (AUParameterNode[] children);
	public static AUParameter CreateParameter (string identifier, string name, ulong address, float min, float max, AudioUnitParameterUnit unit, string unitName, AudioUnitParameterOptions flags, string[] valueStrings, Foundation.NSNumber[] dependentParameters);
	public static AUParameterTree CreateTree (AUParameterNode[] children);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual AUParameter GetParameter (ulong address);
	public virtual AUParameter GetParameter (uint paramID, uint scope, uint element);
}
</pre>

### New Type AudioUnit.AURenderEventType

<pre style='color: green'>
[Serializable]
public enum AURenderEventType {
	Midi = 8,
	MidiSysEx = 9,
	Parameter = 1,
	ParameterRamp = 2,
}
</pre>

### New Type AudioUnit.AUReverbRoomType

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

### New Type AudioUnit.AUScheduledAudioSliceFlags

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

### New Type AudioUnit.AUSpatializationAlgorithm

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

### New Type AudioUnit.AUSpatialMixerAttenuationCurve

<pre style='color: green'>
[Serializable]
public enum AUSpatialMixerAttenuationCurve {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
</pre>

### New Type AudioUnit.AUSpatialMixerRenderingFlags

<pre style='color: green'>
[Serializable]
public enum AUSpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
</pre>

## Namespace AVFoundation

### Type Changed: AVFoundation.AVAsset

Added properties:

<pre style='color: green'>
	public virtual bool CanContainFragments { get; }
	public static Foundation.NSString ChapterMetadataGroupsDidChangeNotification { get; }
	public virtual bool CompatibleWithAirPlayVideo { get; }
	public virtual bool ContainsFragments { get; }
	public static Foundation.NSString ContainsFragmentsDidChangeNotification { get; }
	public static Foundation.NSString DurationDidChangeNotification { get; }
	public static Foundation.NSString MediaSelectionGroupsDidChangeNotification { get; }
	public virtual AVMediaSelection PreferredMediaSelection { get; }
	public virtual int UnusedTrackId { get; }
	public static Foundation.NSString WasDefragmentedNotification { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual AVMetadataItem[] ChapterMetadataGroups (Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
```

Added method:

<pre style='color: green'>
	public virtual AVTimedMetadataGroup[] GetChapterMetadataGroups (Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

### Type Changed: AVFoundation.AVAssetExportSession

Added properties:

<pre style='color: green'>
	public virtual AVMetadataItemFilter MetadataItemFilter { get; set; }
	public static Foundation.NSString Preset1920x1080 { get; }
	public static Foundation.NSString Preset3840x2160 { get; }
	public static Foundation.NSString PresetHighestQuality { get; }
	public static Foundation.NSString PresetLowQuality { get; }
	public static Foundation.NSString PresetMediumQuality { get; }
</pre>

### Type Changed: AVFoundation.AVAssetResourceLoader

Added property:

<pre style='color: green'>
	public virtual bool PreloadsEligibleContentKeys { get; set; }
</pre>

### Type Changed: AVFoundation.AVAssetResourceLoadingDataRequest

Added property:

<pre style='color: green'>
	public virtual bool RequestsAllDataToEndOfResource { get; }
</pre>

### Type Changed: AVFoundation.AVAssetTrack

Added properties:

<pre style='color: green'>
	public static Foundation.NSString SegmentsDidChangeNotification { get; }
	public static Foundation.NSString TimeRangeDidChangeNotification { get; }
	public static Foundation.NSString TrackAssociationsDidChangeNotification { get; }
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual Foundation.NSString GetAssociatedTracksOfType (Foundation.NSString avAssetTrackTrackAssociationType);
```

Added method:

<pre style='color: green'>
	public virtual AVAssetTrack[] GetAssociatedTracks (Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

### Type Changed: AVFoundation.AVAssetWriter

Added properties:

<pre style='color: green'>
	public virtual AVAssetWriterInputGroup[] InputGroups { get; }
	public virtual CoreMedia.CMTime OverallDurationHint { get; set; }
</pre>

### Type Changed: AVFoundation.AVAudioChannelLayout

Added constructor:

<pre style='color: green'>
	public AVAudioChannelLayout (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSSecureCoding
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: AVFoundation.AVAudioEngine

Added methods:

<pre style='color: green'>
	public virtual void Connect (AVAudioNode sourceNode, AVAudioConnectionPoint[] destNodes, uint sourceBus, AVAudioFormat format);
	public virtual AVAudioConnectionPoint InputConnectionPoint (AVAudioNode node, uint bus);
	public virtual AVAudioConnectionPoint[] OutputConnectionPoints (AVAudioNode node, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioEnvironmentNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioFormat

Added constructors:

<pre style='color: green'>
	public AVAudioFormat (CoreMedia.CMAudioFormatDescription formatDescription);
	public AVAudioFormat (Foundation.NSCoder coder);
</pre>

Added interfaces:

<pre style='color: green'>
	Foundation.INSCoding
	Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual CoreMedia.CMAudioFormatDescription FormatDescription { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder encoder);
</pre>

### Type Changed: AVFoundation.AVAudioInputNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioMixerNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioMixInputParameters

Added property:

<pre style='color: green'>
	public virtual Foundation.NSString AudioTimePitchAlgorithm { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: AVFoundation.AVAudioPlayerNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioSessionCategoryOptions

Added value:

<pre style='color: green'>
	InterruptSpokenAudioAndMixWithOthers = 17,
</pre>

### Type Changed: AVFoundation.AVAudioSessionErrorCode

Added value:

<pre style='color: green'>
	CodeResourceNotAvailable = 561145203,
</pre>

### Type Changed: AVFoundation.AVAudioUnit

Added property:

<pre style='color: green'>
	public virtual AudioUnit.AUAudioUnit AUAudioUnit { get; }
</pre>

Added methods:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
	public static void FromComponentDescription (AudioUnit.AudioComponentDescription audioComponentDescription, AudioUnit.AudioComponentInstantiationOptions options, System.Action&lt;AVAudioUnit,Foundation.NSError&gt; completionHandler);
</pre>

### Type Changed: AVFoundation.AVAudioUnitGenerator

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioUnitMidiInstrument

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
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: AVFoundation.AVAudioUnitSampler

Added interfaces:

<pre style='color: green'>
	IAVAudio3DMixing
	IAVAudioMixing
	IAVAudioStereoMixing
</pre>

### Type Changed: AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: AVFoundation.AVComposition

Added property:

<pre style='color: green'>
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; UrlAssetInitializationOptions { get; }
</pre>

### Type Changed: AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: AVFoundation.AVError

Added value:

<pre style='color: green'>
	VideoCompositorFailed = -11858,
</pre>

### Type Changed: AVFoundation.AVFileType

Added properties:

<pre style='color: green'>
	public static Foundation.NSString EnhancedAC3 { get; }
	public static Foundation.NSString ThreeGpp2 { get; }
</pre>

### Type Changed: AVFoundation.AVMediaCharacteristic

Added properties:

<pre style='color: green'>
	public static Foundation.NSString DubbedTranslation { get; }
	public static Foundation.NSString LanguageTranslation { get; }
	public static Foundation.NSString VoiceOverTranslation { get; }
</pre>

### Type Changed: AVFoundation.AVMediaSelectionGroup

Added method:

<pre style='color: green'>
	public static AVMediaSelectionOption[] MediaSelectionOptionsFilteredAndSorted (AVMediaSelectionOption[] mediaSelectionOptions, string[] preferredLanguages);
</pre>

### Type Changed: AVFoundation.AVMetadata

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ID3MetadataKeyCommercial { get; }
	public static Foundation.NSString QuickTimeMetadataKeyContentIdentifier { get; }
</pre>

### Type Changed: AVFoundation.AVMetadataIdentifiers

### Type Changed: AVFoundation.AVMetadataIdentifiers.QuickTimeMetadata

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ContentIdentifier { get; }
	public static Foundation.NSString DetectedFace { get; }
	public static Foundation.NSString VideoOrientation { get; }
</pre>

### Type Changed: AVFoundation.AVMetadataIdentifiers.ID3Metadata

Added property:

<pre style='color: green'>
	public static Foundation.NSString Commercial { get; }
</pre>

### Type Changed: AVFoundation.AVMetadataItem

Added property:

<pre style='color: green'>
	public virtual Foundation.NSDate StartDate { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public static AVMetadataItem GetMetadataItem (AVMetadataItem metadataItem, System.Action&lt;AVMetadataItemValueRequest&gt; handler);
</pre>

### Type Changed: AVFoundation.AVMutableComposition

Added method:

<pre style='color: green'>
	public static AVMutableComposition FromOptions (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; urlAssetInitializationOptions);
</pre>

### Type Changed: AVFoundation.AVMutableCompositionTrack

Obsoleted methods:

```
[Obsolete ()]
	public virtual bool InsertTimeRanges (Foundation.NSValue cmTimeRanges, AVAssetTrack[] tracks, CoreMedia.CMTime startTime, out Foundation.NSError error);
```

Added method:

<pre style='color: green'>
	public virtual bool InsertTimeRanges (Foundation.NSValue[] cmTimeRanges, AVAssetTrack[] tracks, CoreMedia.CMTime startTime, out Foundation.NSError error);
</pre>

### Type Changed: AVFoundation.AVMutableMetadataItem

Added property:

<pre style='color: green'>
	public override Foundation.NSDate StartDate { get; set; }
</pre>

### Type Changed: AVFoundation.AVMutableTimedMetadataGroup

Added interface:

<pre style='color: green'>
	Foundation.INSMutableCopying
</pre>

### Type Changed: AVFoundation.AVMutableVideoComposition

Added method:

<pre style='color: green'>
	public static AVMutableVideoComposition GetVideoComposition (AVAsset asset, System.Action&lt;AVAsynchronousCIImageFilteringRequest&gt; applier);
</pre>

### Type Changed: AVFoundation.AVPlayer

Added properties:

<pre style='color: green'>
	public virtual bool AllowsExternalPlayback { get; set; }
	public virtual string AudioOutputDeviceUniqueID { get; set; }
	public virtual bool ExternalPlaybackActive { get; }
</pre>

### Type Changed: AVFoundation.AVPlayerItem

Added properties:

<pre style='color: green'>
	public virtual bool CanUseNetworkResourcesForLiveStreamingWhilePaused { get; set; }
	public virtual AVMediaSelection CurrentMediaSelection { get; }
</pre>

### Type Changed: AVFoundation.AVPlayerItemTrack

Added properties:

<pre style='color: green'>
	public virtual string VideoFieldMode { get; set; }
	public static Foundation.NSString VideoFieldModeDeinterlaceFields { get; }
</pre>

### Type Changed: AVFoundation.AVPlayerLayer

Added properties:

<pre style='color: green'>
	public CoreVideo.CVPixelBufferAttributes PixelBufferAttributes { get; set; }
	public virtual Foundation.NSDictionary WeakPixelBufferAttributes { get; set; }
</pre>

### Type Changed: AVFoundation.AVTextStyleRule

Obsoleted constructors:

```
[Obsolete ()]
	public AVTextStyleRule ();
```

### Type Changed: AVFoundation.AVTimedMetadataGroup


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSObject</span></span>

 <span style='color:green'>AVFoundation.AVMetadataGroup</span>

Added interface:

<pre style='color: green'>
	Foundation.INSMutableCopying
</pre>

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
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

### Type Changed: AVFoundation.AVVideoComposition

Added method:

<pre style='color: green'>
	public static AVVideoComposition CreateVideoComposition (AVAsset asset, System.Action&lt;AVAsynchronousCIImageFilteringRequest&gt; applier);
</pre>

### New Type AVFoundation.AVAsynchronousCIImageFilteringRequest

<pre style='color: green'>
public class AVAsynchronousCIImageFilteringRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVAsynchronousCIImageFilteringRequest ();
	protected AVAsynchronousCIImageFilteringRequest (Foundation.NSObjectFlag t);
	protected AVAsynchronousCIImageFilteringRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreMedia.CMTime CompositionTime { get; }
	public virtual CoreGraphics.CGSize RenderSize { get; }
	public virtual CoreImage.CIImage SourceImage { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Finish (Foundation.NSError error);
	public virtual void Finish (CoreImage.CIImage filteredImage, CoreImage.CIContext context);
}
</pre>

### New Type AVFoundation.AVAudioCompressedBuffer

<pre style='color: green'>
public class AVAudioCompressedBuffer : AVFoundation.AVAudioBuffer, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVAudioCompressedBuffer (Foundation.NSObjectFlag t);
	protected AVAudioCompressedBuffer (IntPtr handle);
	public AVAudioCompressedBuffer (AVAudioFormat format, uint packetCapacity);
	public AVAudioCompressedBuffer (AVAudioFormat format, uint packetCapacity, nint maximumPacketSize);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IntPtr Data { get; }
	public virtual nint MaximumPacketSize { get; }
	public virtual uint PacketCapacity { get; }
	public virtual uint PacketCount { get; set; }
	public virtual AudioToolbox.AudioStreamPacketDescription PacketDescriptions { get; }
}
</pre>

### New Type AVFoundation.AVAudioConnectionPoint

<pre style='color: green'>
public class AVAudioConnectionPoint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVAudioConnectionPoint ();
	protected AVAudioConnectionPoint (Foundation.NSObjectFlag t);
	protected AVAudioConnectionPoint (IntPtr handle);
	public AVAudioConnectionPoint (AVAudioNode node, uint bus);
	// properties
	public virtual uint Bus { get; }
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioNode Node { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AVFoundation.AVAudioConverter

<pre style='color: green'>
public class AVAudioConverter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVAudioConverter (Foundation.NSObjectFlag t);
	protected AVAudioConverter (IntPtr handle);
	public AVAudioConverter (AVAudioFormat fromFormat, AVAudioFormat toFormat);
	// properties
	public virtual Foundation.NSNumber[] ApplicableEncodeBitRates { get; }
	public virtual Foundation.NSNumber[] ApplicableEncodeSampleRates { get; }
	public virtual Foundation.NSNumber[] AvailableEncodeBitRates { get; }
	public virtual Foundation.NSNumber[] AvailableEncodeChannelLayoutTags { get; }
	public virtual Foundation.NSNumber[] AvailableEncodeSampleRates { get; }
	public virtual nint BitRate { get; set; }
	public virtual string BitRateStrategy { get; set; }
	public virtual Foundation.NSNumber[] ChannelMap { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual bool Dither { get; set; }
	public virtual bool Downmix { get; set; }
	public virtual AVAudioFormat InputFormat { get; }
	public virtual Foundation.NSData MagicCookie { get; set; }
	public virtual nint MaximumOutputPacketSize { get; }
	public virtual AVAudioFormat OutputFormat { get; }
	public virtual AVAudioConverterPrimeInfo PrimeInfo { get; set; }
	public virtual AVAudioConverterPrimeMethod PrimeMethod { get; set; }
	public virtual string SampleRateConverterAlgorithm { get; set; }
	public virtual nint SampleRateConverterQuality { get; set; }
	// methods
	public virtual AVAudioConverterOutputStatus ConvertToBuffer (AVAudioBuffer outputBuffer, out Foundation.NSError outError, AVAudioConverterInputHandler inputHandler);
	public virtual bool ConvertToBuffer (AVAudioPcmBuffer outputBuffer, AVAudioPcmBuffer inputBuffer, out Foundation.NSError outError);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
</pre>

### New Type AVFoundation.AVAudioConverterInputHandler

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

### New Type AVFoundation.AVAudioConverterInputStatus

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterInputStatus {
	EndOfStream = 2,
	HaveData = 0,
	NoDataNow = 1,
}
</pre>

### New Type AVFoundation.AVAudioConverterOutputStatus

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterOutputStatus {
	EndOfStream = 2,
	Error = 3,
	HaveData = 0,
	InputRanDry = 1,
}
</pre>

### New Type AVFoundation.AVAudioConverterPrimeInfo

<pre style='color: green'>
public struct AVAudioConverterPrimeInfo {
	// fields
	public uint LeadingFrames;
	public uint TrailingFrames;
}
</pre>

### New Type AVFoundation.AVAudioConverterPrimeMethod

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterPrimeMethod {
	None = 2,
	Normal = 1,
	Pre = 0,
}
</pre>

### New Type AVFoundation.AVAudioMixing_Extensions

<pre style='color: green'>
public static class AVAudioMixing_Extensions {
	// methods
	public static AVAudioMixingDestination DestinationForMixer (IAVAudioMixing This, AVAudioNode mixer, uint bus);
}
</pre>

### New Type AVFoundation.AVAudioMixingDestination

<pre style='color: green'>
public class AVAudioMixingDestination : Foundation.NSObject, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVAudioMixingDestination (Foundation.NSObjectFlag t);
	protected AVAudioMixingDestination (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioConnectionPoint ConnectionPoint { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
	// methods
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AVFoundation.AVAudioSequencer

<pre style='color: green'>
public class AVAudioSequencer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVAudioSequencer ();
	public AVAudioSequencer (AVAudioEngine engine);
	protected AVAudioSequencer (Foundation.NSObjectFlag t);
	protected AVAudioSequencer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual double CurrentPositionInBeats { get; set; }
	public virtual double CurrentPositionInSeconds { get; set; }
	public virtual bool Playing { get; }
	public virtual float Rate { get; set; }
	public virtual AVMusicTrack TempoTrack { get; }
	public virtual AVMusicTrack[] Tracks { get; }
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; UserInfo { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual double GetBeats (double seconds);
	public virtual double GetBeats (ulong inHostTime, out Foundation.NSError outError);
	public virtual Foundation.NSData GetData (nint smpteResolution, out Foundation.NSError outError);
	public virtual ulong GetHostTime (double inBeats, out Foundation.NSError outError);
	public virtual double GetSeconds (double beats);
	public virtual bool Load (Foundation.NSData data, AVMusicSequenceLoadOptions options, out Foundation.NSError outError);
	public virtual bool Load (Foundation.NSUrl fileUrl, AVMusicSequenceLoadOptions options, out Foundation.NSError outError);
	public virtual void PrepareToPlay ();
	public virtual bool Start (out Foundation.NSError outError);
	public virtual void Stop ();
	public virtual bool Write (Foundation.NSUrl fileUrl, nint resolution, bool replace, out Foundation.NSError outError);
}
</pre>

### New Type AVFoundation.AVAudioUnitComponent

<pre style='color: green'>
public class AVAudioUnitComponent : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVAudioUnitComponent ();
	protected AVAudioUnitComponent (Foundation.NSObjectFlag t);
	protected AVAudioUnitComponent (IntPtr handle);
	// properties
	public virtual string[] AllTagNames { get; }
	public virtual AudioUnit.AudioComponent AudioComponent { get; }
	public virtual AudioUnit.AudioComponentDescription AudioComponentDescription { get; }
	public virtual Foundation.NSNumber[] AvailableArchitectures { get; }
	public override IntPtr ClassHandle { get; }
	public virtual bool HasCustomView { get; }
	public virtual bool HasMidiInput { get; }
	public virtual bool HasMidiOutput { get; }
	public virtual AppKit.NSImage Icon { get; }
	public virtual Foundation.NSUrl IconUrl { get; }
	public virtual string LocalizedTypeName { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual bool PassesAUVal { get; }
	public virtual bool SandboxSafe { get; }
	public static Foundation.NSString TagsDidChangeNotification { get; }
	public virtual string TypeName { get; }
	public virtual string[] UserTagNames { get; set; }
	public virtual uint Version { get; }
	public virtual string VersionString { get; }
	public virtual Foundation.NSDictionary WeakConfigurationDictionary { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool SupportsNumberInputChannels (nint numInputChannels, nint numOutputChannels);

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveTagsDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type AVFoundation.AVAudioUnitComponentFilter

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

### New Type AVFoundation.AVAudioUnitComponentManager

<pre style='color: green'>
public class AVAudioUnitComponentManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVAudioUnitComponentManager ();
	protected AVAudioUnitComponentManager (Foundation.NSObjectFlag t);
	protected AVAudioUnitComponentManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static AVAudioUnitComponentManager SharedInstance { get; }
	public virtual string[] StandardLocalizedTagNames { get; }
	public virtual string[] TagNames { get; }
	// methods
	public virtual AVAudioUnitComponent[] GetComponents (AudioUnit.AudioComponentDescription desc);
	public virtual AVAudioUnitComponent[] GetComponents (AVAudioUnitComponentFilter testHandler);
	public virtual AVAudioUnitComponent[] GetComponents (Foundation.NSPredicate predicate);
}
</pre>

### New Type AVFoundation.AVAudioUnitManufacturerName

<pre style='color: green'>
public static class AVAudioUnitManufacturerName {
	// properties
	public static Foundation.NSString Apple { get; }
}
</pre>

### New Type AVFoundation.AVAudioUnitType

<pre style='color: green'>
public static class AVAudioUnitType {
	// properties
	public static Foundation.NSString Effect { get; }
	public static Foundation.NSString FormatConverter { get; }
	public static Foundation.NSString Generator { get; }
	public static Foundation.NSString MidiProcessor { get; }
	public static Foundation.NSString Mixer { get; }
	public static Foundation.NSString MusicDevice { get; }
	public static Foundation.NSString MusicEffect { get; }
	public static Foundation.NSString OfflineEffect { get; }
	public static Foundation.NSString Output { get; }
	public static Foundation.NSString Panner { get; }
}
</pre>

### New Type AVFoundation.AVBeatRange

<pre style='color: green'>
public struct AVBeatRange {
	// constructors
	public AVBeatRange (double startBeat, double lengthInBeats);
	// fields
	public double Length;
	public double Start;
}
</pre>

### New Type AVFoundation.AVComposition_AVCompositionTrackInspection

<pre style='color: green'>
public static class AVComposition_AVCompositionTrackInspection {
	// methods
	public static AVCompositionTrack GetTrack (AVComposition This, int trackID);
	public static AVCompositionTrack[] GetTracks (AVComposition This, string mediaType);
	public static AVCompositionTrack[] GetTracksWithMediaCharacteristic (AVComposition This, string mediaCharacteristic);
}
</pre>

### New Type AVFoundation.AVDateRangeMetadataGroup

<pre style='color: green'>
public class AVDateRangeMetadataGroup : AVFoundation.AVMetadataGroup, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVDateRangeMetadataGroup ();
	protected AVDateRangeMetadataGroup (Foundation.NSObjectFlag t);
	protected AVDateRangeMetadataGroup (IntPtr handle);
	public AVDateRangeMetadataGroup (AVMetadataItem[] items, Foundation.NSDate startDate, Foundation.NSDate endDate);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSDate EndDate { get; set; }
	public virtual AVMetadataItem[] Items { get; set; }
	public virtual Foundation.NSDate StartDate { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
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

### New Type AVFoundation.AVFragmentedAsset

<pre style='color: green'>
public class AVFragmentedAsset : AVFoundation.AVUrlAsset, IAVFragmentMinding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVFragmentedAsset (Foundation.NSObjectFlag t);
	protected AVFragmentedAsset (IntPtr handle);
	public AVFragmentedAsset (Foundation.NSUrl url, Foundation.NSDictionary options);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVFragmentedAssetTrack[] Tracks { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static AVFragmentedAsset FromUrl (Foundation.NSUrl url, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);
	public virtual bool IsAssociatedWithFragmentMinder ();
}
</pre>

### New Type AVFoundation.AVFragmentedAsset_AVFragmentedAssetTrackInspection

<pre style='color: green'>
public static class AVFragmentedAsset_AVFragmentedAssetTrackInspection {
	// methods
	public static AVFragmentedAssetTrack GetTrack (AVFragmentedAsset This, int trackID);
	public static AVFragmentedAssetTrack[] GetTracks (AVFragmentedAsset This, string mediaType);
	public static AVFragmentedAssetTrack[] GetTracksWithMediaCharacteristic (AVFragmentedAsset This, string mediaCharacteristic);
}
</pre>

### New Type AVFoundation.AVFragmentedAssetMinder

<pre style='color: green'>
public class AVFragmentedAssetMinder : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVFragmentedAssetMinder ();
	protected AVFragmentedAssetMinder (Foundation.NSObjectFlag t);
	protected AVFragmentedAssetMinder (IntPtr handle);
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

### New Type AVFoundation.AVFragmentedAssetTrack

<pre style='color: green'>
public class AVFragmentedAssetTrack : AVFoundation.AVAssetTrack, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVFragmentedAssetTrack (Foundation.NSObjectFlag t);
	protected AVFragmentedAssetTrack (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type AVFoundation.AVFragmentMinding_Extensions

<pre style='color: green'>
public static class AVFragmentMinding_Extensions {
	// methods
	public static bool IsAssociatedWithFragmentMinder (IAVFragmentMinding This);
}
</pre>

### New Type AVFoundation.AVMediaSelection

<pre style='color: green'>
public class AVMediaSelection : Foundation.NSObject, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVMediaSelection ();
	protected AVMediaSelection (Foundation.NSObjectFlag t);
	protected AVMediaSelection (IntPtr handle);
	// properties
	public virtual AVAsset Asset { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual bool CriteriaCanBeAppliedAutomaticallyToMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
	protected override void Dispose (bool disposing);
	public virtual AVMediaSelectionOption GetSelectedMediaOption (AVMediaSelectionGroup mediaSelectionGroup);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type AVFoundation.AVMetadataExtraAttribute

<pre style='color: green'>
public static class AVMetadataExtraAttribute {
	// properties
	public static Foundation.NSString BaseUriKey { get; }
	public static Foundation.NSString InfoKey { get; }
	public static Foundation.NSString ValueUriKey { get; }
}
</pre>

### New Type AVFoundation.AVMetadataGroup

<pre style='color: green'>
public class AVMetadataGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVMetadataGroup ();
	protected AVMetadataGroup (Foundation.NSObjectFlag t);
	protected AVMetadataGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVMetadataItem[] Items { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AVFoundation.AVMetadataItemValueRequest

<pre style='color: green'>
public class AVMetadataItemValueRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVMetadataItemValueRequest ();
	protected AVMetadataItemValueRequest (Foundation.NSObjectFlag t);
	protected AVMetadataItemValueRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVMetadataItem MetadataItem { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Respond (Foundation.NSError error);
	public virtual void Respond (Foundation.NSObject value);
}
</pre>

### New Type AVFoundation.AVMusicSequenceLoadOptions

<pre style='color: green'>
[Serializable]
public enum AVMusicSequenceLoadOptions {
	ChannelsToTracks = 1,
	PreserveTracks = 0,
}
</pre>

### New Type AVFoundation.AVMusicTrack

<pre style='color: green'>
public class AVMusicTrack : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVMusicTrack (Foundation.NSObjectFlag t);
	protected AVMusicTrack (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioUnit DestinationAudioUnit { get; set; }
	public virtual uint DestinationMidiEndpoint { get; set; }
	public virtual double LengthInBeats { get; set; }
	public virtual double LengthInSeconds { get; set; }
	public virtual bool LoopingEnabled { get; set; }
	public virtual AVBeatRange LoopRange { get; set; }
	public virtual bool Muted { get; set; }
	public virtual nint NumberOfLoops { get; set; }
	public virtual double OffsetTime { get; set; }
	public virtual bool Soloed { get; set; }
	public virtual uint TimeResolution { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AVFoundation.AVMutableComposition_AVMutableCompositionTrackInspection

<pre style='color: green'>
public static class AVMutableComposition_AVMutableCompositionTrackInspection {
	// methods
	public static AVMutableCompositionTrack GetTrack (AVMutableComposition This, int trackID);
	public static AVMutableCompositionTrack[] GetTracks (AVMutableComposition This, string mediaType);
	public static AVMutableCompositionTrack[] GetTracksWithMediaCharacteristic (AVMutableComposition This, string mediaCharacteristic);
}
</pre>

### New Type AVFoundation.AVMutableDateRangeMetadataGroup

<pre style='color: green'>
public class AVMutableDateRangeMetadataGroup : AVFoundation.AVDateRangeMetadataGroup, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVMutableDateRangeMetadataGroup ();
	protected AVMutableDateRangeMetadataGroup (Foundation.NSObjectFlag t);
	protected AVMutableDateRangeMetadataGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public override Foundation.NSDate EndDate { get; set; }
	public override AVMetadataItem[] Items { get; set; }
	public override Foundation.NSDate StartDate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type AVFoundation.AVMutableMediaSelection

<pre style='color: green'>
public class AVMutableMediaSelection : AVFoundation.AVMediaSelection, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVMutableMediaSelection ();
	protected AVMutableMediaSelection (Foundation.NSObjectFlag t);
	protected AVMutableMediaSelection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SelectMediaOption (AVMediaSelectionOption mediaSelectionOption, AVMediaSelectionGroup mediaSelectionGroup);
}
</pre>

### New Type AVFoundation.AVStreamingKeyDelivery

<pre style='color: green'>
public static class AVStreamingKeyDelivery {
	// properties
	public static Foundation.NSString ContentKeyType { get; }
	public static Foundation.NSString PersistentContentKeyType { get; }
}
</pre>

### New Type AVFoundation.IAVFragmentMinding

<pre style='color: green'>
public interface IAVFragmentMinding : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## Namespace AVKit

### New Type AVKit.AVKitError

<pre style='color: green'>
[Serializable]
public enum AVKitError {
	None = 0,
	PictureInPictureStartFailed = -1001,
	Unknown = -1000,
}
</pre>

## Namespace CloudKit

### Type Changed: CloudKit.CKContainer

Added property:

<pre style='color: green'>
	public static Foundation.NSString AccountChangedNotification { get; }
</pre>

### Type Changed: CloudKit.CKDiscoveredUserInfo

Added property:

<pre style='color: green'>
	public virtual Contacts.CNContact DisplayContact { get; }
</pre>

### Type Changed: CloudKit.CKNotification

Added properties:

<pre style='color: green'>
	public virtual string Category { get; }
	public virtual string SubscriptionID { get; }
</pre>

### Type Changed: CloudKit.CKNotificationInfo

Added property:

<pre style='color: green'>
	public virtual string Category { get; set; }
</pre>

### Type Changed: CloudKit.CKOperation

Added method:

<pre style='color: green'>
	public virtual ulong ActivityStart ();
</pre>

### Type Changed: CloudKit.CKRecordID

Obsoleted constructors:

```
[Obsolete ()]
	public CKRecordID ();
```

### Type Changed: CloudKit.CKRecordZoneID

Obsoleted constructors:

```
[Obsolete ()]
	public CKRecordZoneID ();
```

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

### Type Changed: CoreAnimation.CAEmitterCell

Added property:

<pre style='color: green'>
	public virtual nfloat ContentsScale { get; set; }
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

### Type Changed: CoreAnimation.CATextLayer

Added property:

<pre style='color: green'>
	public virtual bool AllowsFontSubpixelQuantization { get; set; }
</pre>

### Type Changed: CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### New Type CoreAnimation.CAMetalLayer

<pre style='color: green'>
public class CAMetalLayer : CoreAnimation.CALayer, ICAMediaTiming, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CAMetalLayer ();
	public CAMetalLayer (Foundation.NSCoder coder);
	protected CAMetalLayer (Foundation.NSObjectFlag t);
	protected CAMetalLayer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Metal.IMTLDevice Device { get; set; }
	public virtual CoreGraphics.CGSize DrawableSize { get; set; }
	public virtual bool FramebufferOnly { get; set; }
	public virtual Metal.MTLPixelFormat PixelFormat { get; set; }
	public virtual bool PresentsWithTransaction { get; set; }
	// methods
	public virtual ICAMetalDrawable CreateDrawable ();
	protected override void Dispose (bool disposing);
	public virtual ICAMetalDrawable NextDrawable ();
}
</pre>

### New Type CoreAnimation.CASpringAnimation

<pre style='color: green'>
public class CASpringAnimation : CoreAnimation.CABasicAnimation, ICAAction, ICAMediaTiming, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CASpringAnimation ();
	public CASpringAnimation (Foundation.NSCoder coder);
	protected CASpringAnimation (Foundation.NSObjectFlag t);
	protected CASpringAnimation (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nfloat Damping { get; set; }
	public virtual nfloat InitialVelocity { get; set; }
	public virtual nfloat Mass { get; set; }
	public virtual double SettlingDuration { get; }
	public virtual nfloat Stiffness { get; set; }
	// methods
	public static CABasicAnimation FromKeyPath (string path);
}
</pre>

### New Type CoreAnimation.ICAMetalDrawable

<pre style='color: green'>
public interface ICAMetalDrawable : Metal.IMTLDrawable, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual CAMetalLayer Layer { get; }
	public virtual Metal.IMTLTexture Texture { get; }
}
</pre>

## Namespace CoreBluetooth

### Type Changed: CoreBluetooth.CBError

Added value:

<pre style='color: green'>
	ConnectionLimitReached = 11,
</pre>

### Type Changed: CoreBluetooth.CBPeripheralState

Added value:

<pre style='color: green'>
	Disconnecting = 3,
</pre>

## Namespace CoreData

### Type Changed: CoreData.NSEntityDescription

Added property:

<pre style='color: green'>
	public Foundation.NSObject[][] UniquenessConstraints { get; set; }
</pre>

### Type Changed: CoreData.NSIncrementalStore

Added constructor:

<pre style='color: green'>
	public NSIncrementalStore (NSPersistentStoreCoordinator root, string name, Foundation.NSUrl url, Foundation.NSDictionary options);
</pre>

### Type Changed: CoreData.NSManagedObject

Added property:

<pre style='color: green'>
	public virtual bool HasPersistentChangedValues { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual NSManagedObjectID[] GetObjectIDs (string relationshipName);
</pre>

### Type Changed: CoreData.NSManagedObjectContext

Added property:

<pre style='color: green'>
	public virtual bool ShouldDeleteInaccessibleFaults { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out Foundation.NSError error);
	public static void MergeChangesFromRemoteContextSave (Foundation.NSDictionary changeNotificationData, NSManagedObjectContext[] contexts);
	public virtual void RefreshAllObjects ();
	public virtual bool ShouldHandleInaccessibleFault (NSManagedObject fault, NSManagedObjectID oid, NSPropertyDescription property);
</pre>

### Type Changed: CoreData.NSMergeConflict

Obsoleted constructors:

```
[Obsolete ()]
	public NSMergeConflict ();
```

### Type Changed: CoreData.NSMergePolicy

Obsoleted constructors:

```
[Obsolete ()]
	public NSMergePolicy ();
```

Added methods:

<pre style='color: green'>
	public virtual bool ResolveConstraintConflicts (NSConstraintConflict[] list, out Foundation.NSError error);
	public virtual bool ResolveOptimisticLockingVersionConflicts (NSMergeConflict[] list, out Foundation.NSError error);
</pre>

### Type Changed: CoreData.NSPersistentStore

Obsoleted constructors:

```
[Obsolete ()]
	public NSPersistentStore ();
```

### Type Changed: CoreData.NSPersistentStoreCoordinator

Added methods:

<pre style='color: green'>
	public virtual bool DestroyPersistentStore (Foundation.NSUrl url, string storeType, Foundation.NSDictionary options, out Foundation.NSError error);
	public virtual bool ReplacePersistentStore (Foundation.NSUrl destinationURL, Foundation.NSDictionary destinationOptions, Foundation.NSUrl sourceURL, Foundation.NSDictionary sourceOptions, string storeType, out Foundation.NSError error);
</pre>

### Type Changed: CoreData.NSPersistentStoreRequestType

Added value:

<pre style='color: green'>
	BatchDelete = 7,
</pre>

### New Type CoreData.NSBatchDeleteRequest

<pre style='color: green'>
public class NSBatchDeleteRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSBatchDeleteRequest (NSFetchRequest fetch);
	public NSBatchDeleteRequest (NSManagedObjectID[] objects);
	protected NSBatchDeleteRequest (Foundation.NSObjectFlag t);
	protected NSBatchDeleteRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSFetchRequest FetchRequest { get; }
	public virtual NSBatchDeleteRequestResultType ResultType { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type CoreData.NSBatchDeleteRequestResultType

<pre style='color: green'>
[Serializable]
public enum NSBatchDeleteRequestResultType {
	Count = 2,
	ObjectIDs = 1,
	StatusOnly = 0,
}
</pre>

### New Type CoreData.NSBatchDeleteResult

<pre style='color: green'>
public class NSBatchDeleteResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSBatchDeleteResult ();
	protected NSBatchDeleteResult (Foundation.NSObjectFlag t);
	protected NSBatchDeleteResult (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject Result { get; }
	public virtual NSBatchDeleteRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type CoreData.NSConstraintConflict

<pre style='color: green'>
public class NSConstraintConflict : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSConstraintConflict ();
	protected NSConstraintConflict (Foundation.NSObjectFlag t);
	protected NSConstraintConflict (IntPtr handle);
	public NSConstraintConflict (string[] contraint, NSManagedObject databaseObject, Foundation.NSDictionary databaseSnapshot, NSManagedObject[] conflictingObjects, Foundation.NSObject[] conflictingSnapshots);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSManagedObject[] ConflictingObjects { get; }
	public virtual Foundation.NSDictionary[] ConflictingSnapshots { get; }
	public virtual string[] Constraint { get; }
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; ConstraintValues { get; }
	public virtual NSManagedObject DatabaseObject { get; }
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; DatabaseSnapshot { get; }
	// methods
	protected override void Dispose (bool disposing);
}
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

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGColorSpace

Obsoleted fields:

```
[Obsolete ()]
	public static CGColorSpace Null;
```

Obsoleted methods:

```
[Obsolete ()]
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

### Type Changed: CoreGraphics.CGColorSpaceNames

Added properties:

<pre style='color: green'>
	public static Foundation.NSString AcesCGLinear { get; }
	public static Foundation.NSString AdobeRgb1998 { get; }
	public static Foundation.NSString GenericCmyk { get; }
	public static Foundation.NSString GenericRgb { get; }
	public static Foundation.NSString GenericRgbLinear { get; }
	public static Foundation.NSString GenericXyz { get; }
	public static Foundation.NSString ItuR_2020 { get; }
	public static Foundation.NSString ItuR_709 { get; }
	public static Foundation.NSString RommRgb { get; }
	public static Foundation.NSString Srgb { get; }
</pre>

### Type Changed: CoreGraphics.CGDataProvider

Added constructors:

<pre style='color: green'>
	public CGDataProvider (Foundation.NSData data);
	public CGDataProvider (Foundation.NSUrl url);
</pre>

### Type Changed: CoreGraphics.CGImage

Added property:

<pre style='color: green'>
	public Foundation.NSString UTType { get; }
</pre>

## Namespace CoreImage

### Type Changed: CoreImage.CIAccordionFoldTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAdditionCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineClamp

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAffineTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaAverage

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaHistogram

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaMaximum

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaMaximumAlpha

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaMinimum

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAreaMinimumAlpha

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIAztecCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIBarsSwipeTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendWithAlphaMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBlendWithMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBloom

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBoxBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBumpDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIBumpDistortionLinear

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICheckerboardGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICircleSplashDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICircularScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICircularWrap

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICMYKHalftone


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICmykHalftone</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
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

### Type Changed: CoreImage.CICode128BarcodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIColor

Added constructors:

<pre style='color: green'>
	public CIColor (nfloat red, nfloat green, nfloat blue);
	public CIColor (nfloat red, nfloat green, nfloat blue, nfloat alpha);
</pre>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorBurnBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorClamp

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorControls

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCrossPolynomial

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCube

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorCubeWithColorSpace

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorDodgeBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorInvert

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMap

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMatrix

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorMonochrome

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorPolynomial

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColorPosterize

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIColumnAverage

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIComicEffect

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICompositingFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConstantColorGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIContext

Added properties:

<pre style='color: green'>
	public static int OfflineGPUCount { get; }
	public virtual CoreGraphics.CGColorSpace WorkingColorSpace { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static CIContext FromMetalDevice (Metal.IMTLDevice device);
	public static CIContext FromMetalDevice (Metal.IMTLDevice device, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);
	public static CIContext FromOfflineGpu (int gpuIndex);
	public virtual void Render (CIImage image, Metal.IMTLTexture texture, Metal.IMTLCommandBuffer commandBuffer, CoreGraphics.CGRect bounds, CoreGraphics.CGColorSpace colorSpace);
</pre>

### Type Changed: CoreImage.CIContextOptions

Added property:

<pre style='color: green'>
	public bool? HighQualityDownsample { get; set; }
</pre>

### Type Changed: CoreImage.CIConvolution3X3

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution5X5

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution7X7

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution9Horizontal

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolution9Vertical

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIConvolutionCore

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICopyMachineTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICrop

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CICrystallize

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDarkenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDepthOfField

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDetector

Added properties:

<pre style='color: green'>
	public static Foundation.NSString NumberOfAngles { get; }
	public static Foundation.NSString ReturnSubFeatures { get; }
	public static Foundation.NSString TypeText { get; }
</pre>

Added method:

<pre style='color: green'>
	public static CIDetector CreateTextDetector (CIContext context, CIDetectorOptions detectorOptions);
</pre>

### Type Changed: CoreImage.CIDetectorOptions

Added properties:

<pre style='color: green'>
	public float? NumberOfAngles { get; set; }
	public bool? ReturnSubFeatures { get; set; }
</pre>

### Type Changed: CoreImage.CIDifferenceBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDiscBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDisintegrateWithMaskTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDisplacementDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDissolveTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDistortionFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDivideBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDotScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIDroste

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIEdges

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIEdgeWork

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIEightfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIExclusionBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIExposureAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFaceBalance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFalseColor

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFeature

Added properties:

<pre style='color: green'>
	public static Foundation.NSString TypeQRCode { get; }
	public static Foundation.NSString TypeRectangle { get; }
	public static Foundation.NSString TypeText { get; }
</pre>

### Type Changed: CoreImage.CIFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFilterAttributes

Added properties:

<pre style='color: green'>
	public static Foundation.NSString Available_iOS { get; }
	public static Foundation.NSString Available_Mac { get; }
	public static Foundation.NSString TypeColor { get; }
	public static Foundation.NSString TypeImage { get; }
	public static Foundation.NSString TypeTransform { get; }
</pre>

### Type Changed: CoreImage.CIFilterGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFilterInputKey

Added properties:

<pre style='color: green'>
	public static Foundation.NSString BiasKey { get; }
	public static Foundation.NSString Version { get; }
	public static Foundation.NSString WeightsKey { get; }
</pre>

### Type Changed: CoreImage.CIFilterShape

Removed method:

<pre style='color: red'>
	public virtual CIFilterShape IntersectWithRect (CoreGraphics.CGRect rectangle);
</pre>

Added method:

<pre style='color: green'>
	public virtual CIFilterShape Intersect (CoreGraphics.CGRect rectangle);
</pre>

### Type Changed: CoreImage.CIFlashTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFormat

Obsoleted fields:

```
[Obsolete ()]
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

### Type Changed: CoreImage.CIFourfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFourfoldRotatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIFourfoldTranslatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGammaAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGaussianBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGaussianGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGlassDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGlassLozenge

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGlideReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIGloom

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHardLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHatchedScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHeightFieldFromMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHexagonalPixellate

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHighlightShadowAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHistogramDisplayFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHoleDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHueAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIHueBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIImage

Added constructors:

<pre style='color: green'>
	public CIImage (Metal.IMTLTexture texture, Foundation.NSDictionary options);
	public CIImage (ICIImageProvider provider, uint width, uint height, CIFormat pixelFormat, CoreGraphics.CGColorSpace colorSpace, CIImageProviderOptions options);
</pre>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
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
	public virtual Foundation.NSUrl Url { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static CIImage FromImageBuffer (CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);
	public static CIImage FromMetalTexture (Metal.IMTLTexture texture, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);
	public static CIImage FromProvider (ICIImageProvider provider, uint width, uint height, CIFormat pixelFormat, CoreGraphics.CGColorSpace colorSpace, CIImageProviderOptions options);
</pre>

### Type Changed: CoreImage.CIKaleidoscope

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILanczosScaleTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILenticularHaloGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILightenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearBurnBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearDodgeBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILinearToSRGBToneCurve

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILineOverlay

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILineScreen

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CILuminosityBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaskedVariableBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaskToAlpha

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaximumComponent

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMaximumCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMedianFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMinimumComponent

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMinimumCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIModTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMotionBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMultiplyBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIMultiplyCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CINoiseReduction

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIOpTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIOverlayBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPageCurlTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPageCurlWithShadowTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIParallelogramTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveCorrection

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPerspectiveTransform

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffect

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectChrome

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectFade

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectInstant

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectMono

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectNoir

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectProcess

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectTonal

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPhotoEffectTransfer

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPinchDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPinLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPixellate

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIPointillize

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIQRCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>CoreImage.CIFilter</span></span>

 <span style='color:green'>CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public Foundation.NSData Message { get; set; }
</pre>

### Type Changed: CoreImage.CIRadialGradient

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIRandomGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIRippleTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIRowAverage

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISampler

Obsoleted constructors:

```
[Obsolete ()]
	public CISampler ();
```

### Type Changed: CoreImage.CISamplerOptions

Added property:

<pre style='color: green'>
	public CoreGraphics.CGColorSpace ColorSpace { get; set; }
</pre>

### Type Changed: CoreImage.CISaturationBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIScreenBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIScreenFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISepiaTone

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIShadedMaterial

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISharpenLuminance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISixfoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISixfoldRotatedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISoftLightBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceAtopCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceInCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceOutCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISourceOverCompositing

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISpotColor

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISpotLight

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISRGBToneCurveToLinear

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStarShineGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStraightenFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStretchCrop

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIStripesGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISubtractBlendMode

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISunbeamsGenerator

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CISwipeTransition

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITemperatureAndTint

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITileFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIToneCurve

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITorusLensDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITransitionFilter

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITriangleTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITwelvefoldReflectedTile

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CITwirlDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIUnsharpMask

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVector

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVibrance

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVignette

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVignetteEffect

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIVortexDistortion

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIWhitePointAdjust

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### Type Changed: CoreImage.CIZoomBlur

Added interface:

<pre style='color: green'>
	Foundation.INSSecureCoding
</pre>

### New Type CoreImage.CICmykHalftone

<pre style='color: green'>
public class CICmykHalftone : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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

### New Type CoreImage.CICodeGenerator

<pre style='color: green'>
public abstract class CICodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CICodeGenerator (IntPtr handle);
	public CICodeGenerator (string name);
	// properties
	public Foundation.NSData Message { get; set; }
}
</pre>

### New Type CoreImage.CIColorKernel

<pre style='color: green'>
public class CIColorKernel : CoreImage.CIKernel, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected CIColorKernel (Foundation.NSObjectFlag t);
	protected CIColorKernel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (CoreGraphics.CGRect extent, Foundation.NSObject[] args);
	public static CIColorKernel FromProgramSingle (string coreImageShaderProgram);
}
</pre>

### New Type CoreImage.CIImageProviderOptions

<pre style='color: green'>
public class CIImageProviderOptions : Foundation.DictionaryContainer {
	// constructors
	public CIImageProviderOptions ();
	public CIImageProviderOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSObject TileSize { get; set; }
	public Foundation.NSObject UserInfo { get; set; }
}
</pre>

### New Type CoreImage.CIKernelRoiCallback

<pre style='color: green'>
public sealed delegate CIKernelRoiCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CIKernelRoiCallback (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (int index, CoreGraphics.CGRect rect, System.AsyncCallback callback, object object);
	public virtual CoreGraphics.CGRect EndInvoke (System.IAsyncResult result);
	public virtual CoreGraphics.CGRect Invoke (int index, CoreGraphics.CGRect rect);
}
</pre>

### New Type CoreImage.CILightTunnel

<pre style='color: green'>
public class CILightTunnel : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CILightTunnel ();
	public CILightTunnel (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
	public float Rotation { get; set; }
}
</pre>

### New Type CoreImage.CIPdf417BarcodeGenerator

<pre style='color: green'>
public class CIPdf417BarcodeGenerator : CoreImage.CICodeGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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

### New Type CoreImage.CIPerspectiveTransformWithExtent

<pre style='color: green'>
public class CIPerspectiveTransformWithExtent : CoreImage.CIPerspectiveTransform, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CIPerspectiveTransformWithExtent ();
	public CIPerspectiveTransformWithExtent (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type CoreImage.CISmoothLinearGradient

<pre style='color: green'>
public class CISmoothLinearGradient : CoreImage.CILinearGradient, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CISmoothLinearGradient ();
	public CISmoothLinearGradient (IntPtr handle);
}
</pre>

### New Type CoreImage.CITriangleKaleidoscope

<pre style='color: green'>
public class CITriangleKaleidoscope : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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

### New Type CoreImage.CIWarpKernel

<pre style='color: green'>
public class CIWarpKernel : CoreImage.CIKernel, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected CIWarpKernel (Foundation.NSObjectFlag t);
	protected CIWarpKernel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (CoreGraphics.CGRect extent, CIKernelRoiCallback callback, CIImage image, Foundation.NSObject[] args);
	public static CIWarpKernel FromProgramSingle (string coreImageShaderProgram);
}
</pre>

### New Type CoreImage.ICIFilterConstructor

<pre style='color: green'>
public interface ICIFilterConstructor : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual CIFilter FilterWithName (string name);
}
</pre>

### New Type CoreImage.ICIImageProvider

<pre style='color: green'>
public interface ICIImageProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ProvideImageData (IntPtr data, uint rowbytes, uint x, uint y, uint width, uint height, Foundation.NSObject info);
}
</pre>

## Namespace CoreLocation

### Type Changed: CoreLocation.CLPlacemark

Added property:

<pre style='color: green'>
	public virtual Foundation.NSTimeZone TimeZone { get; }
</pre>

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
	public CMBlockBufferError FillDataBytes (byte fillByte, uint offsetIntoDestination, uint dataLength);
	public static CMBlockBuffer FromBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer FromMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public CMBlockBufferError GetDataPointer (uint offset, out uint lengthAtOffset, out uint totalLength, ref IntPtr dataPointer);
	public bool IsRangeContiguous (uint offset, uint length);
	public CMBlockBufferError ReplaceDataBytes (IntPtr sourceBytes, uint offsetIntoDestination, uint dataLength);
</pre>

### Type Changed: CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: CoreMedia.CMTimebase

Added methods:

<pre style='color: green'>
	public CMClockOrTimebase CopyMaster ();
	public CMClock CopyMasterClock ();
	public CMTimebase CopyMasterTimebase ();
	public CMClock CopyUltimateMasterClock ();
</pre>

### Type Changed: CoreMedia.CMTimeMapping

Added property:

<pre style='color: green'>
	public string Description { get; }
</pre>

Added methods:

<pre style='color: green'>
	public Foundation.NSDictionary AsDictionary ();
	public static CMTimeMapping Create (CMTimeRange source, CMTimeRange target);
	public static CMTimeMapping CreateEmpty (CMTimeRange target);
	public static CMTimeMapping CreateFromDictionary (Foundation.NSDictionary dict);
</pre>

### Type Changed: CoreMedia.CMTimeRange

Obsoleted fields:

```
[Obsolete ()]
	public static CMTimeRange Invalid;
```

Added fields:

<pre style='color: green'>
	public static CMTimeRange InvalidMapping;
	public static CMTimeRange InvalidRange;
</pre>

Added properties:

<pre style='color: green'>
	public static Foundation.NSString TimeMappingSourceKey { get; }
	public static Foundation.NSString TimeMappingTargetKey { get; }
</pre>

### Type Changed: CoreMedia.CMVideoCodecType

Added value:

<pre style='color: green'>
	Hevc = 1752589105,
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

### New Type CoreMedia.LensStabilizationStatus

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
	public static LSResult Open (Foundation.NSUrl url);
	public static LSResult Open (Foundation.NSUrl url, out Foundation.NSUrl launchedUrl);
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

## Namespace CoreText

### Type Changed: CoreText.CTFont

Added method:

<pre style='color: green'>
	public string GetLocalizedName (CTFontNameKey nameKey, out string actualLanguage);
</pre>

### Type Changed: CoreText.CTLine

Added method:

<pre style='color: green'>
	public void EnumerateCaretOffsets (CTLine.CaretEdgeEnumerator enumerator);
</pre>

## Namespace CoreVideo

### Type Changed: CoreVideo.CVImageBuffer

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }
	public static Foundation.NSString ColorPrimaries_P3_D65 { get; }
	public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }
</pre>

### Type Changed: CoreVideo.CVPixelBuffer

Added properties:

<pre style='color: green'>
	public static Foundation.NSString MetalCompatibilityKey { get; }
	public static Foundation.NSString OpenGLTextureCacheCompatibilityKey { get; }
</pre>

Added method:

<pre style='color: green'>
	public void GetExtendedPixels (ref uint extraColumnsOnLeft, ref uint extraColumnsOnRight, ref uint extraRowsOnTop, ref uint extraRowsOnBottom);
</pre>

### Type Changed: CoreVideo.CVPixelBufferPool

Added properties:

<pre style='color: green'>
	public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }
	public static Foundation.NSString ColorPrimaries_P3_D65 { get; }
	public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }
</pre>

Added method:

<pre style='color: green'>
	public void Flush (CVPixelBufferPoolFlushFlags options);
</pre>

### Type Changed: CoreVideo.CVPixelFormatDescription

Added fields:

<pre style='color: green'>
	public static Foundation.NSString ComponentRangeFullRangeKey;
	public static Foundation.NSString ComponentRangeKey;
	public static Foundation.NSString ComponentRangeVideoRangeKey;
	public static Foundation.NSString ComponentRangeWideRangeKey;
</pre>

### Type Changed: CoreVideo.CVReturn

Added value:

<pre style='color: green'>
	Unsupported = -6663,
</pre>

### New Type CoreVideo.CVPixelBufferPoolFlushFlags

<pre style='color: green'>
[Serializable]
public enum CVPixelBufferPoolFlushFlags {
	FlushExcessBuffers = 1,
}
</pre>

## Namespace EventKit

### Type Changed: EventKit.EKErrorCode

Added values:

<pre style='color: green'>
	EventStoreNotAuthorized = 29,
	InvalidEntityType = 27,
	OSNotSupported = 30,
	PriorityIsInvalid = 26,
	ProcedureAlarmsNotMutable = 28,
</pre>

### Type Changed: EventKit.EKEvent

Added properties:

<pre style='color: green'>
	public virtual string BirthdayContactIdentifier { get; }
	public virtual EKStructuredLocation StructuredLocation { get; set; }
</pre>

### Type Changed: EventKit.EKEventStore

Added property:

<pre style='color: green'>
	public virtual EKSource[] DelegateSources { get; }
</pre>

### Type Changed: EventKit.EKParticipant

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSPredicate ContactPredicate { get; }
	public virtual bool IsCurrentUser { get; }
</pre>

### Type Changed: EventKit.EKStructuredLocation

Added method:

<pre style='color: green'>
	public static EKStructuredLocation FromMapItem (MapKit.MKMapItem mapItem);
</pre>

### New Type EventKit.EKParticipantScheduleStatus

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

### New Type EventKit.EKReminderPriority

<pre style='color: green'>
[Serializable]
public enum EKReminderPriority {
	High = 1,
	Low = 9,
	Medium = 5,
	None = 0,
}
</pre>

### New Type EventKit.EKWeekday

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

## Namespace Foundation

### Type Changed: Foundation.NSAffineTransform

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: Foundation.NSAppleEventDescriptor

Added constructor:

<pre style='color: green'>
	public NSAppleEventDescriptor (NSAppleEventDescriptorType type);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual NSObject InitListDescriptor ();
	[Obsolete ()]
	public virtual NSObject InitRecordDescriptor ();
```

### Type Changed: Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public static NSArray From (NSObject[][] items);
	public static NSObject[][] FromArrayOfArray (NSArray weakArray);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: Foundation.NSAttributedString

Added method:

<pre style='color: green'>
	public virtual bool ContainsAttachmentsInRange (NSRange range);
</pre>

### Type Changed: Foundation.NSBundle

Added method:

<pre style='color: green'>
	public virtual bool LoadNibNamed (string nibName, NSObject owner, out NSArray topLevelObjects);
</pre>

### Type Changed: Foundation.NSCocoaError

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

### Type Changed: Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public byte[] DecodeBytes ();
	public virtual IntPtr DecodeBytes (out uint length);
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public virtual NSObject DecodeTopLevelObject (out NSError error);
	public virtual NSObject DecodeTopLevelObject (string key, out NSError error);
	public virtual NSObject DecodeTopLevelObject (Foundation.NSSet&lt;ObjCRuntime.Class&gt; setOfClasses, string key, out NSError error);
	public virtual NSObject DecodeTopLevelObject (ObjCRuntime.Class klass, string key, out NSError error);
	public NSObject DecodeTopLevelObject (System.Type type, string key, out NSError error);
	public NSObject DecodeTopLevelObject (System.Type[] types, string key, out NSError error);
	public virtual void Fail (NSError error);
	public bool TryDecode (string key, out NSObject result);
	public bool TryDecode (string key, out bool result);
	public bool TryDecode (string key, out byte[] result);
	public bool TryDecode (string key, out double result);
	public bool TryDecode (string key, out int result);
	public bool TryDecode (string key, out long result);
	public bool TryDecode (string key, out nint result);
	public bool TryDecode (string key, out float result);
</pre>

### Type Changed: Foundation.NSCompoundPredicate

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (NSCoder encoder);
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

### Type Changed: Foundation.NSDictionary

Added methods:

<pre style='color: green'>
	public bool ContainsKey (ObjCRuntime.INativeObject key);
	public ObjCRuntime.INativeObject ObjectForKey (ObjCRuntime.INativeObject obj);
</pre>

### Type Changed: Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSErrorUserInfoValueProvider GetUserInfoValueProvider (string errorDomain);
	public static void SetUserInfoValueProvider (string errorDomain, NSErrorUserInfoValueProvider provider);
</pre>

### Type Changed: Foundation.NSExpression

Added properties:

<pre style='color: green'>
	public virtual NSExpression FalseExpression { get; }
	public virtual NSExpression TrueExpression { get; }
</pre>

Added method:

<pre style='color: green'>
	public static NSExpression FromConditional (NSPredicate predicate, NSExpression trueExpression, NSExpression falseExpression);
</pre>

### Type Changed: Foundation.NSExpressionType

Added value:

<pre style='color: green'>
	Conditional = 20,
</pre>

### Type Changed: Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, AppKit.NSStringAttributes defaultAttributes);
	public virtual NSAttributedString GetAttributedString (NSObject obj, Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; defaultAttributes);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: Foundation.NSHttpCookieStorage

Added method:

<pre style='color: green'>
	public static NSHttpCookieStorage GetSharedCookieStorage (string groupContainerIdentifier);
</pre>

### Type Changed: Foundation.NSHttpUrlResponse

Added constructor:

<pre style='color: green'>
	public NSHttpUrlResponse (NSUrl url, string mimetype, nint expectedContentLength, string textEncodingName);
</pre>

### Type Changed: Foundation.NSIndexPath

Added properties:

<pre style='color: green'>
	public virtual nint Item { get; }
	public virtual nint Section { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSIndexPath FromItemSection (nint item, nint section);
	public uint[] GetIndexes (NSRange range);
</pre>

### Type Changed: Foundation.NSItemProvider

Added properties:

<pre style='color: green'>
	public virtual CoreGraphics.CGRect ContainerFrame { get; }
	public virtual CoreGraphics.CGSize PreferredPresentationSize { get; }
	public virtual CoreGraphics.CGRect SourceFrame { get; }
</pre>

### Type Changed: Foundation.NSItemProviderErrorCode

Added value:

<pre style='color: green'>
	UnavailableCoercion = -1200,
</pre>

### Type Changed: Foundation.NSKeyedArchiver

Added property:

<pre style='color: green'>
	public bool RequiresSecureCoding { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool GetRequiresSecureCoding ();
</pre>

### Type Changed: Foundation.NSKeyedUnarchiver

Added property:

<pre style='color: green'>
	public bool RequiresSecureCoding { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool GetRequiresSecureCoding ();
	public static NSObject UnarchiveTopLevelObject (NSData data, out NSError error);
</pre>

### Type Changed: Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: Foundation.NSMutableAttributedString

Added methods:

<pre style='color: green'>
	public bool ReadFromUrl (NSUrl url, NSAttributedStringDocumentAttributes options, ref Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; returnOptions, ref NSError error);
	public virtual bool ReadFromUrl (NSUrl url, Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; options, ref Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; returnOptions, ref NSError error);
</pre>

### Type Changed: Foundation.NSMutableDictionary

Added property:

<pre style='color: green'>
	public ObjCRuntime.INativeObject Item { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public void Add (ObjCRuntime.INativeObject key, ObjCRuntime.INativeObject value);
	public bool Remove (ObjCRuntime.INativeObject key);
	public void SetObject (ObjCRuntime.INativeObject value, ObjCRuntime.INativeObject key);
	public bool TryGetValue (ObjCRuntime.INativeObject key, out ObjCRuntime.INativeObject value);
</pre>

### Type Changed: Foundation.NSMutableString

Added constructor:

<pre style='color: green'>
	public NSMutableString (NSCoder coder);
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool ApplyTransform (NSString transform, bool reverse, NSRange range, out NSRange resultingRange);
	public bool ApplyTransform (NSStringTransform transform, bool reverse, NSRange range, out NSRange resultingRange);
	public virtual void EncodeTo (NSCoder encoder);
	public virtual void ReplaceCharactersInRange (NSRange range, NSString aString);
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
[Obsolete ()]
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

### Type Changed: Foundation.NSProgress

Added methods:

<pre style='color: green'>
	public virtual void AddChild (NSProgress child, long pendingUnitCount);
	public static NSProgress FromTotalUnitCount (long unitCount, NSProgress parent, long portionOfParentTotalUnitCount);
	public static NSProgress GetDiscreteProgress (long unitCount);
	public virtual void Resume ();
	public virtual void SetResumingHandler (System.Action handler);
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

### Type Changed: Foundation.NSSet

Modified methods:

```
public NSSet MakeNSObjectSet<T : NSObject T : ObjCRuntime.INativeObject> (T[] values)
	public T[] ToArray<T : NSObject T : ObjCRuntime.INativeObject> ()
```

### Type Changed: Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: Foundation.NSString

Added properties:

<pre style='color: green'>
	public virtual NSString LocalizedCapitalizedString { get; }
	public virtual NSString LocalizedLowercaseString { get; }
	public virtual NSString LocalizedUppercaseString { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual NSString CommonPrefix (NSString aString, NSStringCompareOptions options);
	public virtual NSString GetVariantFittingPresentationWidth (nint width);
	public virtual bool HasPrefix (NSString prefix);
	public virtual bool HasSuffix (NSString suffix);
	public virtual bool LocalizedStandardContainsString (NSString str);
	public virtual NSRange LocalizedStandardRangeOfString (NSString str);
	public virtual NSString TransliterateString (NSString transform, bool reverse);
	public NSString TransliterateString (NSStringTransform transform, bool reverse);
</pre>

### Type Changed: Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (nint seconds);
</pre>

### Type Changed: Foundation.NSUndoManager

Added methods:

<pre style='color: green'>
	public virtual void RegisterUndo (NSObject target, System.Action&lt;NSObject&gt; undoHandler);
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: Foundation.NSUrl

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

### Type Changed: Foundation.NSUrlComponents

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

### Type Changed: Foundation.NSUrlError

Added values:

<pre style='color: green'>
	AppTransportSecurityRequiresSecureConnection = -1022,
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: Foundation.NSUrlSession

Added methods:

<pre style='color: green'>
	public virtual NSUrlSessionStreamTask CreateBidirectionalStream (NSNetService service);
	public virtual NSUrlSessionStreamTask CreateBidirectionalStream (string hostname, nint port);
	public virtual void GetAllTasks (NSUrlSessionAllPendingTasks completionHandler);
	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionTask[]&gt; GetAllTasksAsync ();
</pre>

### Type Changed: Foundation.NSUrlSessionConfiguration

Added property:

<pre style='color: green'>
	public virtual bool ShouldUseExtendedBackgroundIdleMode { get; }
</pre>

### Type Changed: Foundation.NSUrlSessionDataDelegate

Added method:

<pre style='color: green'>
	public virtual void DidBecomeStreamTask (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionStreamTask streamTask);
</pre>

### Type Changed: Foundation.NSUrlSessionDataDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DidBecomeStreamTask (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionStreamTask streamTask);
</pre>

### Type Changed: Foundation.NSUrlSessionResponseDisposition

Added value:

<pre style='color: green'>
	BecomeStream = 3,
</pre>

### Type Changed: Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>Foundation.NSUrlSessionDataTask</span>

### Type Changed: Foundation.NSUserActivity

Added properties:

<pre style='color: green'>
	public virtual bool EligibleForHandoff { get; set; }
	public virtual bool EligibleForPublicIndexing { get; set; }
	public virtual bool EligibleForSearch { get; set; }
	public virtual NSDate ExpirationDate { get; set; }
	public virtual Foundation.NSSet&lt;NSString&gt; Keywords { get; set; }
	public virtual Foundation.NSSet&lt;NSString&gt; RequiredUserInfoKeys { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ResignCurrent ();
</pre>

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
	public static NSString IsNotNilTransformerName { get; }
	public static NSString KeyedUnarchiveFromDataTransformerName { get; }
	public static ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSValueTransformer GetValueTransformer (string name);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
</pre>

### Type Changed: Foundation.RegisterAttribute

Added property:

<pre style='color: green'>
	public bool SkipRegistration { get; set; }
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

### New Type Foundation.INSProgressReporting

<pre style='color: green'>
public interface INSProgressReporting : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type Foundation.INSUrlSessionStreamDelegate

<pre style='color: green'>
public interface INSUrlSessionStreamDelegate : INSUrlSessionDelegate, INSUrlSessionTaskDelegate, ObjCRuntime.INativeObject, System.IDisposable {
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
public class NSCondition : Foundation.NSObject, INSLocking, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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
public class NSConditionLock : Foundation.NSObject, INSLocking, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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
	public virtual void LockWhenCondition (nint condition);
	public virtual bool LockWhenCondition (nint condition, NSDate limit);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (nint condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (nint condition);
}
</pre>

### New Type Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : Foundation.NSRegularExpression, INSCoding, INSCopying, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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

### New Type Foundation.NSDictionary`2

<pre style='color: green'>
public sealed class NSDictionary`2 : Foundation.NSDictionary, INSCoding, INSCopying, INSMutableCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.Collections.Generic.ICollection&lt;System.Collections.Generic.KeyValuePair&lt;NSObject,Foundation.NSObject&gt;&gt;, System.Collections.Generic.ICollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;, System.Collections.Generic.IDictionary&lt;NSObject,Foundation.NSObject&gt;, System.Collections.Generic.IDictionary&lt;TKey,TValue&gt;, System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;NSObject,Foundation.NSObject&gt;&gt;, System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;, System.Collections.ICollection, System.Collections.IDictionary, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSDictionary`2 ();
	public NSDictionary`2 (NSCoder coder);
	public NSDictionary`2 (Foundation.NSDictionary&lt;TKey,TValue&gt; other);
	public NSDictionary`2 (NSUrl url);
	public NSDictionary`2 (string filename);
	public NSDictionary`2 (TKey key, TValue value);
	public NSDictionary`2 (TKey[] keys, TValue[] values);
	// properties
	public TValue Item { get; }
	public TKey[] Keys { get; }
	public TValue[] Values { get; }
	// methods
	public bool ContainsKey (TKey key);
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (object[] objects, object[] keys);
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (NSObject[] objects, NSObject[] keys, nint count);
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (object[] objects, object[] keys, nint count);
	public TKey[] KeysForObject (TValue obj);
	public TValue ObjectForKey (TKey key);
	public TValue[] ObjectsForKeys (TKey[] keys, TValue marker);
	public bool TryGetValue (TKey key, out TValue value);
}
</pre>

### New Type Foundation.NSErrorUserInfoValueProvider

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

### New Type Foundation.NSFileManagerUnmountOptions

<pre style='color: green'>
[Serializable]
public enum NSFileManagerUnmountOptions {
	AllPartitionsAndEjectDisk = 1,
	WithoutUI = 2,
}
</pre>

### New Type Foundation.NSJavaScriptExtension

<pre style='color: green'>
public static class NSJavaScriptExtension {
	// properties
	public static NSString FinalizeArgumentKey { get; }
	public static NSString PreprocessingResultsKey { get; }
}
</pre>

### New Type Foundation.NSLock

<pre style='color: green'>
public class NSLock : Foundation.NSObject, INSLocking, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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

### New Type Foundation.NSMutableArray`1

<pre style='color: green'>
public sealed class NSMutableArray`1 : Foundation.NSMutableArray, INSCoding, INSCopying, INSMutableCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;TValue&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSMutableArray`1 ();
	public NSMutableArray`1 (NSCoder coder);
	public NSMutableArray`1 (uint capacity);
	public NSMutableArray`1 (TValue[] values);
	// properties
	public TValue Item { get; set; }
	// methods
	public void Add (TValue obj);
	public void AddObjects (TValue[] source);
	public bool Contains (TValue obj);
	public virtual System.Collections.Generic.IEnumerator&lt;TValue&gt; GetEnumerator ();
	public uint IndexOf (TValue obj);
	public void Insert (TValue obj, nint index);
	public void InsertObjects (TValue[] objects, NSIndexSet atIndexes);
	public void ReplaceObject (nint index, TValue withObject);
}
</pre>

### New Type Foundation.NSMutableDictionary`2

<pre style='color: green'>
public sealed class NSMutableDictionary`2 : Foundation.NSMutableDictionary, INSCoding, INSCopying, INSMutableCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.Collections.Generic.ICollection&lt;System.Collections.Generic.KeyValuePair&lt;NSObject,Foundation.NSObject&gt;&gt;, System.Collections.Generic.ICollection&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;, System.Collections.Generic.IDictionary&lt;NSObject,Foundation.NSObject&gt;, System.Collections.Generic.IDictionary&lt;TKey,TValue&gt;, System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;NSObject,Foundation.NSObject&gt;&gt;, System.Collections.Generic.IEnumerable&lt;System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt;&gt;, System.Collections.ICollection, System.Collections.IDictionary, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSMutableDictionary`2 ();
	public NSMutableDictionary`2 (NSCoder coder);
	public NSMutableDictionary`2 (Foundation.NSDictionary&lt;TKey,TValue&gt; other);
	public NSMutableDictionary`2 (Foundation.NSMutableDictionary&lt;TKey,TValue&gt; other);
	public NSMutableDictionary`2 (TKey key, TValue value);
	public NSMutableDictionary`2 (TKey[] keys, TValue[] values);
	// properties
	public TValue Item { get; set; }
	public TKey[] Keys { get; }
	public TValue[] Values { get; }
	// methods
	public void Add (TKey key, TValue value);
	public bool ContainsKey (TKey key);
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (object[] objects, object[] keys);
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (NSObject[] objects, NSObject[] keys, nint count);
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (object[] objects, object[] keys, nint count);
	public TKey[] KeysForObject (TValue obj);
	public TValue ObjectForKey (TKey key);
	public TValue[] ObjectsForKeys (TKey[] keys, TValue marker);
	public bool Remove (TKey key);
	public bool TryGetValue (TKey key, out TValue value);
}
</pre>

### New Type Foundation.NSMutableSet`1

<pre style='color: green'>
public sealed class NSMutableSet`1 : Foundation.NSMutableSet, INSCoding, INSCopying, INSMutableCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;NSObject&gt;, System.Collections.Generic.IEnumerable&lt;TKey&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSMutableSet`1 ();
	public NSMutableSet`1 (NSCoder coder);
	public NSMutableSet`1 (Foundation.NSMutableSet&lt;TKey&gt; other);
	public NSMutableSet`1 (Foundation.NSSet&lt;TKey&gt; other);
	public NSMutableSet`1 (nint capacity);
	public NSMutableSet`1 (TKey[] objs);
	// properties
	public TKey AnyObject { get; }
	// methods
	public void Add (TKey obj);
	public void AddObjects (TKey[] objects);
	public bool Contains (TKey obj);
	public TKey LookupMember (TKey probe);
	public static Foundation.NSMutableSet&lt;TKey&gt; op_Addition (Foundation.NSMutableSet&lt;TKey&gt; first, Foundation.NSMutableSet&lt;TKey&gt; second);
	public static Foundation.NSMutableSet&lt;TKey&gt; op_Subtraction (Foundation.NSMutableSet&lt;TKey&gt; first, Foundation.NSMutableSet&lt;TKey&gt; second);
	public void Remove (TKey obj);
	public TKey[] ToArray ();
}
</pre>

### New Type Foundation.NSPersonNameComponent

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

### New Type Foundation.NSPersonNameComponents

<pre style='color: green'>
public class NSPersonNameComponents : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSPersonNameComponents ();
	public NSPersonNameComponents (NSCoder coder);
	protected NSPersonNameComponents (NSObjectFlag t);
	protected NSPersonNameComponents (IntPtr handle);
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
	public virtual void EncodeTo (NSCoder encoder);
}
</pre>

### New Type Foundation.NSPersonNameComponentsFormatter

<pre style='color: green'>
public class NSPersonNameComponentsFormatter : Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSPersonNameComponentsFormatter ();
	public NSPersonNameComponentsFormatter (NSCoder coder);
	protected NSPersonNameComponentsFormatter (NSObjectFlag t);
	protected NSPersonNameComponentsFormatter (IntPtr handle);
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

### New Type Foundation.NSPersonNameComponentsFormatterOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSPersonNameComponentsFormatterOptions {
	Phonetic = 2,
}
</pre>

### New Type Foundation.NSPersonNameComponentsFormatterStyle

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

### New Type Foundation.NSProgressReporting_Extensions

<pre style='color: green'>
public static class NSProgressReporting_Extensions {
	// methods
	public static NSProgress GetProgress (INSProgressReporting This);
}
</pre>

### New Type Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : Foundation.NSObject, INSLocking, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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
public class NSRegularExpression : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
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
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
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

### New Type Foundation.NSSet`1

<pre style='color: green'>
public sealed class NSSet`1 : Foundation.NSSet, INSCoding, INSCopying, INSMutableCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;NSObject&gt;, System.Collections.Generic.IEnumerable&lt;TKey&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSSet`1 ();
	public NSSet`1 (NSCoder coder);
	public NSSet`1 (Foundation.NSMutableSet&lt;TKey&gt; other);
	public NSSet`1 (Foundation.NSSet&lt;TKey&gt; other);
	public NSSet`1 (TKey[] objs);
	// properties
	public TKey AnyObject { get; }
	// methods
	public bool Contains (TKey obj);
	public TKey LookupMember (TKey probe);
	public static Foundation.NSSet&lt;TKey&gt; op_Addition (Foundation.NSSet&lt;TKey&gt; first, Foundation.NSSet&lt;TKey&gt; second);
	public static Foundation.NSSet&lt;TKey&gt; op_Subtraction (Foundation.NSSet&lt;TKey&gt; first, Foundation.NSSet&lt;TKey&gt; second);
	public TKey[] ToArray ();
}
</pre>

### New Type Foundation.NSStringTransform

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

### New Type Foundation.NSUrlSessionAllPendingTasks

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

### New Type Foundation.NSUrlSessionCombinedTasks

<pre style='color: green'>
public class NSUrlSessionCombinedTasks {
	// constructors
	public NSUrlSessionCombinedTasks (NSUrlSessionTask[] tasks);
	// properties
	public NSUrlSessionTask[] Tasks { get; set; }
}
</pre>

### New Type Foundation.NSUrlSessionDataRead

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

### New Type Foundation.NSUrlSessionStreamDataRead

<pre style='color: green'>
public class NSUrlSessionStreamDataRead {
	// constructors
	public NSUrlSessionStreamDataRead (NSData data, bool atEof);
	// properties
	public bool AtEof { get; set; }
	public NSData Data { get; set; }
}
</pre>

### New Type Foundation.NSUrlSessionStreamDelegate

<pre style='color: green'>
public class NSUrlSessionStreamDelegate : Foundation.NSUrlSessionTaskDelegate, INSObjectProtocol, INSUrlSessionDelegate, INSUrlSessionStreamDelegate, INSUrlSessionTaskDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSUrlSessionStreamDelegate ();
	protected NSUrlSessionStreamDelegate (NSObjectFlag t);
	protected NSUrlSessionStreamDelegate (IntPtr handle);
	// methods
	public virtual void BetterRouteDiscovered (NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public virtual void CompletedTaskCaptureStreams (NSUrlSession session, NSUrlSessionStreamTask streamTask, NSInputStream inputStream, NSOutputStream outputStream);
	public virtual void ReadClosed (NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public virtual void WriteClosed (NSUrlSession session, NSUrlSessionStreamTask streamTask);
}
</pre>

### New Type Foundation.NSUrlSessionStreamDelegate_Extensions

<pre style='color: green'>
public static class NSUrlSessionStreamDelegate_Extensions {
	// methods
	public static void BetterRouteDiscovered (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public static void CompletedTaskCaptureStreams (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask, NSInputStream inputStream, NSOutputStream outputStream);
	public static void ReadClosed (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public static void WriteClosed (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
}
</pre>

### New Type Foundation.NSUrlSessionStreamTask

<pre style='color: green'>
public class NSUrlSessionStreamTask : Foundation.NSUrlSessionTask, INSCopying, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	protected NSUrlSessionStreamTask (NSObjectFlag t);
	protected NSUrlSessionStreamTask (IntPtr handle);
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

## Namespace GameController

### Type Changed: GameController.GCController

Added property:

<pre style='color: green'>
	public virtual CoreFoundation.DispatchQueue HandlerQueue { get; set; }
</pre>

### New Type GameController.GCControllerPlayerIndex

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

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>AppKit.NSViewController</span></span>

 <span style='color:green'>GameKit.GKGameCenterViewController</span>

### Type Changed: GameKit.GKLeaderboardViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>AppKit.NSViewController</span></span>

 <span style='color:green'>GameKit.GKGameCenterViewController</span>

### Type Changed: GameKit.GKLocalPlayerListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: GameKit.GKMatch

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GKDataReceivedForRecipientEventArgs&gt; DataReceivedForRecipient;
</pre>

### Type Changed: GameKit.GKMatchDelegate

Added method:

<pre style='color: green'>
	public virtual void DataReceivedForRecipient (GKMatch match, Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: GameKit.GKMatchDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DataReceivedForRecipient (IGKMatchDelegate This, GKMatch match, Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: GameKit.GKPlayer

Added property:

<pre style='color: green'>
	public virtual string GuestIdentifier { get; }
</pre>

Added method:

<pre style='color: green'>
	public static GKPlayer GetAnonymousGuestPlayer (string guestIdentifier);
</pre>

### Type Changed: GameKit.GKTurnBasedEventListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: GameKit.GKTurnBasedEventListener_Extensions

Added method:

<pre style='color: green'>
	public static void WantsToQuitMatch (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete ()]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

### New Type GameKit.GKDataReceivedForRecipientEventArgs

<pre style='color: green'>
public class GKDataReceivedForRecipientEventArgs : System.EventArgs {
	// constructors
	public GKDataReceivedForRecipientEventArgs (Foundation.NSData data, GKPlayer recipient, GKPlayer player);
	// properties
	public Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
	public GKPlayer Recipient { get; set; }
}
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

### New Type GLKit.GLKMesh

<pre style='color: green'>
public class GLKMesh : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GLKMesh (Foundation.NSObjectFlag t);
	protected GLKMesh (IntPtr handle);
	public GLKMesh (ModelIO.MDLMesh mesh, out Foundation.NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public virtual GLKSubmesh[] Submeshes { get; }
	public virtual GLKMeshBuffer[] VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual ModelIO.MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static GLKMesh[] FromAsset (ModelIO.MDLAsset asset, out ModelIO.MDLMesh[] sourceMeshes, out Foundation.NSError error);
}
</pre>

### New Type GLKit.GLKMeshBuffer

<pre style='color: green'>
public class GLKMeshBuffer : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ModelIO.IMDLMeshBuffer, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GLKMeshBuffer (Foundation.NSObjectFlag t);
	protected GLKMeshBuffer (IntPtr handle);
	// properties
	public virtual ModelIO.IMDLMeshBufferAllocator Allocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint GlBufferName { get; }
	public virtual uint Length { get; }
	public virtual ModelIO.MDLMeshBufferMap Map { get; }
	public virtual ModelIO.MDLMeshBufferType Type { get; }
	public virtual ModelIO.IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void FillData (Foundation.NSData data, uint offset);
}
</pre>

### New Type GLKit.GLKMeshBufferAllocator

<pre style='color: green'>
public class GLKMeshBufferAllocator : Foundation.NSObject, Foundation.INSObjectProtocol, ModelIO.IMDLMeshBufferAllocator, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GLKMeshBufferAllocator (Foundation.NSObjectFlag t);
	protected GLKMeshBufferAllocator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (ModelIO.IMDLMeshBufferZone zone, Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (ModelIO.IMDLMeshBufferZone zone, uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBufferZone CreateZone (uint capacity);
	public virtual ModelIO.IMDLMeshBufferZone CreateZone (Foundation.NSNumber[] sizes, Foundation.NSNumber[] types);
}
</pre>

### New Type GLKit.GLKModelError

<pre style='color: green'>
public static class GLKModelError {
	// properties
	public static Foundation.NSString Domain { get; }
	public static Foundation.NSString Key { get; }
}
</pre>

### New Type GLKit.GLKSubmesh

<pre style='color: green'>
public class GLKSubmesh : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GLKSubmesh (Foundation.NSObjectFlag t);
	protected GLKSubmesh (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GLKMeshBuffer ElementBuffer { get; }
	public virtual int ElementCount { get; }
	public virtual GLKMesh Mesh { get; }
	public virtual uint Mode { get; }
	public virtual string Name { get; }
	public virtual uint Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type GLKit.GLKVertexAttributeParameters

<pre style='color: green'>
public struct GLKVertexAttributeParameters {
	// fields
	public bool Normalized;
	public uint Size;
	public uint Type;
	// methods
	public static GLKVertexAttributeParameters FromVertexFormat (ModelIO.MDLVertexFormat vertexFormat);
}
</pre>

## Namespace ImageIO

### Type Changed: ImageIO.CGImageProperties

Added properties:

<pre style='color: green'>
	public static Foundation.NSString PNGCompressionFilter { get; }
	public static Foundation.NSString TIFFTileLength { get; }
	public static Foundation.NSString TIFFTileWidth { get; }
</pre>

### Type Changed: ImageIO.CGImageThumbnailOptions

Added property:

<pre style='color: green'>
	public int? SubsampleFactor { get; set; }
</pre>

### New Type ImageIO.CGImagePropertyPngFilters

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

## Namespace ImageKit

### Type Changed: ImageKit.IKSlideshow

Added property:

<pre style='color: green'>
	public static Foundation.NSString PhotosBundleIdentifier { get; }
</pre>

## Namespace JavaScriptCore

### Type Changed: JavaScriptCore.JSValue

Added properties:

<pre style='color: green'>
	public virtual bool IsArray { get; }
	public virtual bool IsDate { get; }
</pre>

## Namespace LocalAuthentication

### Type Changed: LocalAuthentication.LAContext

Added property:

<pre style='color: green'>
	public virtual Foundation.NSData EvaluatedPolicyDomainState { get; }
</pre>

Added methods:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
	public virtual void EvaluateAccessControl (Security.SecAccessControl accessControl, LAAccessControlOperation operation, string localizedReason, System.Action&lt;System.Boolean,Foundation.NSError&gt; reply);
	public virtual void Invalidate ();
	public virtual bool IsCredentialSet (LACredentialType type);
	public virtual bool SetCredentialType (Foundation.NSData credential, LACredentialType type);
</pre>

### Type Changed: LocalAuthentication.LAPolicy

Added value:

<pre style='color: green'>
	DeviceOwnerAuthentication = 2,
</pre>

### Type Changed: LocalAuthentication.LAStatus

Added values:

<pre style='color: green'>
	AppCancel = -9,
	InvalidContext = -10,
	TouchIDLockout = -8,
</pre>

### New Type LocalAuthentication.LAAccessControlOperation

<pre style='color: green'>
[Serializable]
public enum LAAccessControlOperation {
	CreateItem = 0,
	CreateKey = 2,
	UseItem = 1,
	UseKeySign = 3,
}
</pre>

### New Type LocalAuthentication.LACredentialType

<pre style='color: green'>
[Serializable]
public enum LACredentialType {
	ApplicationPassword = 0,
}
</pre>

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Added property:

<pre style='color: green'>
	public virtual AppKit.NSView DetailCalloutAccessoryView { get; set; }
</pre>

### Type Changed: MapKit.MKDirections

Obsoleted constructors:

```
[Obsolete ()]
	public MKDirections ();
```

### Type Changed: MapKit.MKDirectionsMode

Added value:

<pre style='color: green'>
	Transit = 2,
</pre>

### Type Changed: MapKit.MKDirectionsTransportType

Added value:

<pre style='color: green'>
	Transit = 4,
</pre>

### Type Changed: MapKit.MKETAResponse

Added properties:

<pre style='color: green'>
	public virtual double Distance { get; }
	public virtual Foundation.NSDate ExpectedArrivalDate { get; }
	public virtual Foundation.NSDate ExpectedDepartureDate { get; }
	public virtual MKDirectionsTransportType TransportType { get; }
</pre>

### Type Changed: MapKit.MKMapCamera

Added method:

<pre style='color: green'>
	public static MKMapCamera CameraLookingAtCenterCoordinate (CoreLocation.CLLocationCoordinate2D centerCoordinate, double locationDistance, nfloat pitch, double locationDirectionHeading);
</pre>

### Type Changed: MapKit.MKMapItem

Added property:

<pre style='color: green'>
	public virtual Foundation.NSTimeZone TimeZone { get; set; }
</pre>

### Type Changed: MapKit.MKMapType

Added values:

<pre style='color: green'>
	HybridFlyover = 4,
	SatelliteFlyover = 3,
</pre>

### Type Changed: MapKit.MKMapView

Added property:

<pre style='color: green'>
	public virtual bool ShowsTraffic { get; set; }
</pre>

### Type Changed: MapKit.MKPinAnnotationView

Added constructor:

<pre style='color: green'>
	public MKPinAnnotationView (CoreGraphics.CGRect frame);
</pre>

Added properties:

<pre style='color: green'>
	public static AppKit.NSColor GreenPinColor { get; }
	public virtual AppKit.NSColor PinTintColor { get; set; }
	public static AppKit.NSColor PurplePinColor { get; }
	public static AppKit.NSColor RedPinColor { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

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

## Namespace MobileCoreServices

### Type Changed: MobileCoreServices.UTType

Added properties:

<pre style='color: green'>
	public static Foundation.NSString Alembic { get; }
	public static Foundation.NSString k3dObject { get; }
	public static Foundation.NSString Polygon { get; }
	public static Foundation.NSString Stereolithography { get; }
	public static Foundation.NSString SwiftSource { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static Foundation.NSDictionary GetDeclaration (string uti);
	public static Foundation.NSUrl GetDeclaringBundleURL (string uti);
	public static string GetPreferredTag (string uti, string tagClass);
</pre>

## Namespace NetworkExtension

### Type Changed: NetworkExtension.NEOnDemandRuleInterfaceType

Added value:

<pre style='color: green'>
	Any = 0,
</pre>

### Type Changed: NetworkExtension.NEVpnError

Added values:

<pre style='color: green'>
	ConfigurationReadWriteFailed = 5,
	ConfigurationUnknown = 6,
</pre>

### New Type NetworkExtension.INWTcpConnectionAuthenticationDelegate

<pre style='color: green'>
public interface INWTcpConnectionAuthenticationDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type NetworkExtension.NEAppProxyFlow

<pre style='color: green'>
public abstract class NEAppProxyFlow : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEAppProxyFlow (Foundation.NSObjectFlag t);
	protected NEAppProxyFlow (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual NEFlowMetaData MetaData { get; }
	// methods
	public virtual void CloseRead (Foundation.NSError error);
	public virtual void CloseWrite (Foundation.NSError error);
	protected override void Dispose (bool disposing);
	public virtual void OpenWithLocalEndpoint (NWHostEndpoint localEndpoint, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task OpenWithLocalEndpointAsync (NWHostEndpoint localEndpoint);
}
</pre>

### New Type NetworkExtension.NEAppProxyFlowError

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

### New Type NetworkExtension.NEAppProxyProvider

<pre style='color: green'>
public class NEAppProxyProvider : NetworkExtension.NETunnelProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEAppProxyProvider (Foundation.NSObjectFlag t);
	protected NEAppProxyProvider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void CancelProxy (Foundation.NSError error);
	public virtual bool HandleNewFlow (NEAppProxyFlow flow);
	public virtual void StartProxy (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task StartProxyAsync (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);
	public virtual void StopProxy (NEProviderStopReason reason, System.Action completionHandler);
	public virtual System.Threading.Tasks.Task StopProxyAsync (NEProviderStopReason reason);
}
</pre>

### New Type NetworkExtension.NEAppProxyProviderManager

<pre style='color: green'>
public class NEAppProxyProviderManager : NetworkExtension.NETunnelProviderManager, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEAppProxyProviderManager (Foundation.NSObjectFlag t);
	protected NEAppProxyProviderManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static void LoadAllFromPreferences (System.Action&lt;Foundation.NSArray,Foundation.NSError&gt; completionHandler);
	public static System.Threading.Tasks.Task&lt;Foundation.NSArray&gt; LoadAllFromPreferencesAsync ();
}
</pre>

### New Type NetworkExtension.NEAppProxyTcpFlow

<pre style='color: green'>
public class NEAppProxyTcpFlow : NetworkExtension.NEAppProxyFlow, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEAppProxyTcpFlow (Foundation.NSObjectFlag t);
	protected NEAppProxyTcpFlow (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NWEndpoint RemoteEndpoint { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void ReadData (System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; ReadDataAsync ();
	public virtual void WriteData (Foundation.NSData data, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task WriteDataAsync (Foundation.NSData data);
}
</pre>

### New Type NetworkExtension.NEAppProxyUdpFlow

<pre style='color: green'>
public class NEAppProxyUdpFlow : NetworkExtension.NEAppProxyFlow, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEAppProxyUdpFlow (Foundation.NSObjectFlag t);
	protected NEAppProxyUdpFlow (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NWEndpoint LocalEndpoint { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void ReadDatagrams (NEDatagramRead completionHandler);
	public virtual System.Threading.Tasks.Task&lt;NEDatagramReadResult&gt; ReadDatagramsAsync ();
	public virtual void WriteDatagrams (Foundation.NSData[] datagrams, NWEndpoint[] remoteEndpoints, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task WriteDatagramsAsync (Foundation.NSData[] datagrams, NWEndpoint[] remoteEndpoints);
}
</pre>

### New Type NetworkExtension.NEAppRule

<pre style='color: green'>
public class NEAppRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEAppRule (Foundation.NSCoder coder);
	protected NEAppRule (Foundation.NSObjectFlag t);
	protected NEAppRule (IntPtr handle);
	public NEAppRule (string signingIdentifier);
	public NEAppRule (string signingIdentifier, string designatedRequirement);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string MatchDesignatedRequirement { get; }
	public virtual string[] MatchDomains { get; set; }
	public virtual string MatchPath { get; set; }
	public virtual string MatchSigningIdentifier { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEDatagramRead

<pre style='color: green'>
public sealed delegate NEDatagramRead : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NEDatagramRead (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSData[] datagrams, NWEndpoint[] remoteEndpoints, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSData[] datagrams, NWEndpoint[] remoteEndpoints, Foundation.NSError error);
}
</pre>

### New Type NetworkExtension.NEDatagramReadResult

<pre style='color: green'>
public class NEDatagramReadResult {
	// constructors
	public NEDatagramReadResult (Foundation.NSData[] datagrams, NWEndpoint[] remoteEndpoints);
	// properties
	public Foundation.NSData[] Datagrams { get; set; }
	public NWEndpoint[] RemoteEndpoints { get; set; }
}
</pre>

### New Type NetworkExtension.NEDnsSettings

<pre style='color: green'>
public class NEDnsSettings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEDnsSettings (Foundation.NSCoder coder);
	protected NEDnsSettings (Foundation.NSObjectFlag t);
	protected NEDnsSettings (IntPtr handle);
	public NEDnsSettings (string[] servers);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string DomainName { get; set; }
	public virtual string[] MatchDomains { get; set; }
	public virtual bool MatchDomainsNoSearch { get; set; }
	public virtual string[] SearchDomains { get; set; }
	public virtual string[] Servers { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEEvaluateConnectionRule

<pre style='color: green'>
public class NEEvaluateConnectionRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEEvaluateConnectionRule ();
	public NEEvaluateConnectionRule (Foundation.NSCoder coder);
	protected NEEvaluateConnectionRule (Foundation.NSObjectFlag t);
	protected NEEvaluateConnectionRule (IntPtr handle);
	public NEEvaluateConnectionRule (string[] domains, NEEvaluateConnectionRuleAction action);
	// properties
	public virtual NEEvaluateConnectionRuleAction Action { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string[] MatchDomains { get; }
	public virtual Foundation.NSUrl ProbeUrl { get; set; }
	public virtual string[] UseDnsServers { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEFilterManager

<pre style='color: green'>
public class NEFilterManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEFilterManager (Foundation.NSObjectFlag t);
	protected NEFilterManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ConfigurationDidChangeNotification { get; }
	public virtual bool Enabled { get; set; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedDescription { get; set; }
	public virtual NEFilterProviderConfiguration ProviderConfiguration { get; set; }
	public static NEFilterManager SharedManager { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void LoadFromPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task LoadFromPreferencesAsync ();
	public virtual void RemoveFromPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task RemoveFromPreferencesAsync ();
	public virtual void SaveToPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task SaveToPreferencesAsync ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveConfigurationDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type NetworkExtension.NEFilterManagerError

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

### New Type NetworkExtension.NEFilterProvider

<pre style='color: green'>
public abstract class NEFilterProvider : NetworkExtension.NEProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEFilterProvider ();
	protected NEFilterProvider (Foundation.NSObjectFlag t);
	protected NEFilterProvider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEFilterProviderConfiguration FilterConfiguration { get; }
	public static Foundation.NSString RemediationMapRemediationButtonTexts { get; }
	public static Foundation.NSString RemediationMapRemediationUrls { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void StartFilter (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task StartFilterAsync ();
	public virtual void StopFilter (NEProviderStopReason reason, System.Action completionHandler);
	public virtual System.Threading.Tasks.Task StopFilterAsync (NEProviderStopReason reason);
}
</pre>

### New Type NetworkExtension.NEFilterProviderConfiguration

<pre style='color: green'>
public class NEFilterProviderConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEFilterProviderConfiguration ();
	public NEFilterProviderConfiguration (Foundation.NSCoder coder);
	protected NEFilterProviderConfiguration (Foundation.NSObjectFlag t);
	protected NEFilterProviderConfiguration (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool FilterBrowsers { get; set; }
	public virtual bool FilterSockets { get; set; }
	public virtual Foundation.NSData IdentityReference { get; set; }
	public virtual string Organization { get; set; }
	public virtual Foundation.NSData PasswordReference { get; set; }
	public virtual string ServerAddress { get; set; }
	public virtual string Username { get; set; }
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; VendorConfiguration { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEFlowMetaData

<pre style='color: green'>
public class NEFlowMetaData : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEFlowMetaData ();
	protected NEFlowMetaData (Foundation.NSObjectFlag t);
	protected NEFlowMetaData (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string SourceAppSigningIdentifier { get; }
	public virtual Foundation.NSData SourceAppUniqueIdentifier { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NEIPv4Route

<pre style='color: green'>
public class NEIPv4Route : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEIPv4Route (Foundation.NSCoder coder);
	protected NEIPv4Route (Foundation.NSObjectFlag t);
	protected NEIPv4Route (IntPtr handle);
	public NEIPv4Route (string address, string subnetMask);
	// properties
	public override IntPtr ClassHandle { get; }
	public static NEIPv4Route DefaultRoute { get; }
	public virtual string DestinationAddress { get; }
	public virtual string DestinationSubnetMask { get; }
	public virtual string GatewayAddress { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEIPv4Settings

<pre style='color: green'>
public class NEIPv4Settings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEIPv4Settings (Foundation.NSCoder coder);
	protected NEIPv4Settings (Foundation.NSObjectFlag t);
	protected NEIPv4Settings (IntPtr handle);
	public NEIPv4Settings (string[] addresses, string[] subnetMasks);
	// properties
	public virtual string[] Addresses { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NEIPv4Route[] ExcludedRoutes { get; set; }
	public virtual NEIPv4Route[] IncludedRoutes { get; set; }
	public virtual string[] SubnetMasks { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEIPv6Route

<pre style='color: green'>
public class NEIPv6Route : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEIPv6Route (Foundation.NSCoder coder);
	protected NEIPv6Route (Foundation.NSObjectFlag t);
	protected NEIPv6Route (IntPtr handle);
	public NEIPv6Route (string address, Foundation.NSNumber networkPrefixLength);
	// properties
	public override IntPtr ClassHandle { get; }
	public static NEIPv6Route DefaultRoute { get; }
	public virtual string DestinationAddress { get; }
	public virtual Foundation.NSNumber DestinationNetworkPrefixLength { get; }
	public virtual string GatewayAddress { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEIPv6Settings

<pre style='color: green'>
public class NEIPv6Settings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEIPv6Settings (Foundation.NSCoder coder);
	protected NEIPv6Settings (Foundation.NSObjectFlag t);
	protected NEIPv6Settings (IntPtr handle);
	public NEIPv6Settings (string[] addresses, Foundation.NSNumber[] networkPrefixLengths);
	// properties
	public virtual string[] Addresses { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NEIPv6Route[] ExcludedRoutes { get; set; }
	public virtual NEIPv6Route[] IncludedRoutes { get; set; }
	public virtual Foundation.NSNumber[] NetworkPrefixLengths { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEOnDemandRule

<pre style='color: green'>
public abstract class NEOnDemandRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEOnDemandRule ();
	protected NEOnDemandRule (Foundation.NSCoder coder);
	protected NEOnDemandRule (Foundation.NSObjectFlag t);
	protected NEOnDemandRule (IntPtr handle);
	// properties
	public virtual NEOnDemandRuleAction Action { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string[] DnsSearchDomainMatch { get; set; }
	public virtual string[] DnsServerAddressMatch { get; set; }
	public virtual NEOnDemandRuleInterfaceType InterfaceTypeMatch { get; set; }
	public virtual Foundation.NSUrl ProbeUrl { get; set; }
	public virtual string[] SsidMatch { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEOnDemandRuleConnect

<pre style='color: green'>
public class NEOnDemandRuleConnect : NetworkExtension.NEOnDemandRule, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEOnDemandRuleConnect ();
	public NEOnDemandRuleConnect (Foundation.NSCoder coder);
	protected NEOnDemandRuleConnect (Foundation.NSObjectFlag t);
	protected NEOnDemandRuleConnect (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type NetworkExtension.NEOnDemandRuleDisconnect

<pre style='color: green'>
public class NEOnDemandRuleDisconnect : NetworkExtension.NEOnDemandRule, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEOnDemandRuleDisconnect ();
	public NEOnDemandRuleDisconnect (Foundation.NSCoder coder);
	protected NEOnDemandRuleDisconnect (Foundation.NSObjectFlag t);
	protected NEOnDemandRuleDisconnect (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type NetworkExtension.NEOnDemandRuleEvaluateConnection

<pre style='color: green'>
public class NEOnDemandRuleEvaluateConnection : NetworkExtension.NEOnDemandRule, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEOnDemandRuleEvaluateConnection ();
	public NEOnDemandRuleEvaluateConnection (Foundation.NSCoder coder);
	protected NEOnDemandRuleEvaluateConnection (Foundation.NSObjectFlag t);
	protected NEOnDemandRuleEvaluateConnection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEEvaluateConnectionRule[] ConnectionRules { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NEOnDemandRuleIgnore

<pre style='color: green'>
public class NEOnDemandRuleIgnore : NetworkExtension.NEOnDemandRule, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEOnDemandRuleIgnore ();
	public NEOnDemandRuleIgnore (Foundation.NSCoder coder);
	protected NEOnDemandRuleIgnore (Foundation.NSObjectFlag t);
	protected NEOnDemandRuleIgnore (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type NetworkExtension.NEPacketTunnelFlow

<pre style='color: green'>
public class NEPacketTunnelFlow : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEPacketTunnelFlow ();
	protected NEPacketTunnelFlow (Foundation.NSObjectFlag t);
	protected NEPacketTunnelFlow (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void ReadPackets (System.Action&lt;Foundation.NSData[],Foundation.NSNumber[]&gt; completionHandler);
	public virtual bool WritePackets (Foundation.NSData[] packets, Foundation.NSNumber[] protocols);
}
</pre>

### New Type NetworkExtension.NEPacketTunnelNetworkSettings

<pre style='color: green'>
public class NEPacketTunnelNetworkSettings : NetworkExtension.NETunnelNetworkSettings, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEPacketTunnelNetworkSettings ();
	public NEPacketTunnelNetworkSettings (Foundation.NSCoder coder);
	protected NEPacketTunnelNetworkSettings (Foundation.NSObjectFlag t);
	protected NEPacketTunnelNetworkSettings (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEIPv4Settings IPv4Settings { get; set; }
	public virtual NEIPv6Settings IPv6Settings { get; set; }
	public virtual Foundation.NSNumber Mtu { get; set; }
	public virtual Foundation.NSNumber TunnelOverheadBytes { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NEPacketTunnelProvider

<pre style='color: green'>
public class NEPacketTunnelProvider : NetworkExtension.NETunnelProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEPacketTunnelProvider (Foundation.NSObjectFlag t);
	protected NEPacketTunnelProvider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEPacketTunnelFlow PacketFlow { get; }
	// methods
	public virtual void CancelTunnel (Foundation.NSError error);
	public virtual NWTcpConnection CreateTcpConnection (NWEndpoint remoteEndpoint, bool enableTls, NWTlsParameters tlsParameters, NWTcpConnectionAuthenticationDelegate delegate);
	public virtual NWUdpSession CreateUdpSession (NWEndpoint remoteEndpoint, NWHostEndpoint localEndpoint);
	protected override void Dispose (bool disposing);
	public virtual void StartTunnel (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task StartTunnelAsync (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);
	public virtual void StopTunnel (NEProviderStopReason reason, System.Action completionHandler);
	public virtual System.Threading.Tasks.Task StopTunnelAsync (NEProviderStopReason reason);
}
</pre>

### New Type NetworkExtension.NEProvider

<pre style='color: green'>
public class NEProvider : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEProvider (Foundation.NSObjectFlag t);
	protected NEProvider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NWPath DefaultPath { get; }
	// methods
	public virtual NWTcpConnection CreateTcpConnectionToEndpoint (NWEndpoint remoteEndpoint, bool enableTLS, NWTlsParameters TLSParameters, Foundation.NSObject connectionDelegate);
	public virtual NWUdpSession CreateUdpSessionToEndpoint (NWEndpoint remoteEndpoint, NWHostEndpoint localEndpoint);
	protected override void Dispose (bool disposing);
	public virtual void Sleep (System.Action completionHandler);
	public virtual System.Threading.Tasks.Task SleepAsync ();
	public virtual void Wake ();
}
</pre>

### New Type NetworkExtension.NEProviderStopReason

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

### New Type NetworkExtension.NEProxyServer

<pre style='color: green'>
public class NEProxyServer : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEProxyServer (Foundation.NSCoder coder);
	protected NEProxyServer (Foundation.NSObjectFlag t);
	protected NEProxyServer (IntPtr handle);
	public NEProxyServer (string address, nint port);
	// properties
	public virtual string Address { get; }
	public virtual bool AuthenticationRequired { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Password { get; set; }
	public virtual nint Port { get; }
	public virtual string Username { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEProxySettings

<pre style='color: green'>
public class NEProxySettings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEProxySettings ();
	public NEProxySettings (Foundation.NSCoder coder);
	protected NEProxySettings (Foundation.NSObjectFlag t);
	protected NEProxySettings (IntPtr handle);
	// properties
	public virtual bool AutoProxyConfigurationEnabled { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string[] ExceptionList { get; set; }
	public virtual bool ExcludeSimpleHostnames { get; set; }
	public virtual bool HttpEnabled { get; set; }
	public virtual bool HttpsEnabled { get; set; }
	public virtual NEProxyServer HttpServer { get; set; }
	public virtual NEProxyServer HttpsServer { get; set; }
	public virtual string[] MatchDomains { get; set; }
	public virtual string ProxyAutoConfigurationJavaScript { get; set; }
	public virtual Foundation.NSUrl ProxyAutoConfigurationUrl { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NETunnelNetworkSettings

<pre style='color: green'>
public class NETunnelNetworkSettings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NETunnelNetworkSettings (Foundation.NSCoder coder);
	protected NETunnelNetworkSettings (Foundation.NSObjectFlag t);
	protected NETunnelNetworkSettings (IntPtr handle);
	public NETunnelNetworkSettings (string address);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEDnsSettings DnsSettings { get; set; }
	public virtual NEProxySettings ProxySettings { get; set; }
	public virtual string TunnelRemoteAddress { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NETunnelProvider

<pre style='color: green'>
public class NETunnelProvider : NetworkExtension.NEProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NETunnelProvider (Foundation.NSObjectFlag t);
	protected NETunnelProvider (IntPtr handle);
	// properties
	public virtual NEAppRule[] AppRules { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NEVpnProtocol ProtocolConfiguration { get; }
	public virtual bool Reasserting { get; set; }
	public virtual NETunnelProviderRoutingMethod RoutingMethod { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void HandleAppMessage (Foundation.NSData messageData, System.Action&lt;Foundation.NSData&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; HandleAppMessageAsync (Foundation.NSData messageData);
	public virtual void SetTunnelNetworkSettings (NETunnelNetworkSettings tunnelNetworkSettings, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task SetTunnelNetworkSettingsAsync (NETunnelNetworkSettings tunnelNetworkSettings);
}
</pre>

### New Type NetworkExtension.NETunnelProviderError

<pre style='color: green'>
[Serializable]
public enum NETunnelProviderError {
	Canceled = 2,
	Failed = 3,
	Invalid = 1,
	None = 0,
}
</pre>

### New Type NetworkExtension.NETunnelProviderManager

<pre style='color: green'>
public class NETunnelProviderManager : NetworkExtension.NEVpnManager, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NETunnelProviderManager (Foundation.NSObjectFlag t);
	protected NETunnelProviderManager (IntPtr handle);
	// properties
	public virtual NEAppRule[] AppRules { get; }
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual NETunnelProviderRoutingMethod RoutingMethod { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static void LoadAllFromPreferences (System.Action&lt;Foundation.NSArray,Foundation.NSError&gt; completionHandler);
	public static System.Threading.Tasks.Task&lt;Foundation.NSArray&gt; LoadAllFromPreferencesAsync ();
}
</pre>

### New Type NetworkExtension.NETunnelProviderProtocol

<pre style='color: green'>
public class NETunnelProviderProtocol : NetworkExtension.NEVpnProtocol, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NETunnelProviderProtocol ();
	public NETunnelProviderProtocol (Foundation.NSCoder coder);
	protected NETunnelProviderProtocol (Foundation.NSObjectFlag t);
	protected NETunnelProviderProtocol (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string ProviderBundleIdentifier { get; set; }
	public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; ProviderConfiguration { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NETunnelProviderRoutingMethod

<pre style='color: green'>
[Serializable]
public enum NETunnelProviderRoutingMethod {
	DestinationIP = 1,
	SourceApplication = 2,
}
</pre>

### New Type NetworkExtension.NETunnelProviderSession

<pre style='color: green'>
public class NETunnelProviderSession : NetworkExtension.NEVpnConnection, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NETunnelProviderSession ();
	protected NETunnelProviderSession (Foundation.NSObjectFlag t);
	protected NETunnelProviderSession (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual bool SendProviderMessage (Foundation.NSData messageData, out Foundation.NSError error, System.Action&lt;Foundation.NSData&gt; responseHandler);
	public virtual bool StartTunnel (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, out Foundation.NSError error);
	public virtual void StopTunnel ();
}
</pre>

### New Type NetworkExtension.NEVpnConnection

<pre style='color: green'>
public class NEVpnConnection : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEVpnConnection ();
	protected NEVpnConnection (Foundation.NSObjectFlag t);
	protected NEVpnConnection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSDate ConnectedDate { get; }
	public virtual NEVpnStatus Status { get; }
	public static Foundation.NSString StatusDidChangeNotification { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool StartVpnTunnel (out Foundation.NSError error);
	public bool StartVpnTunnel (NEVpnConnectionStartOptions options, out Foundation.NSError error);
	public virtual void StopVpnTunnel ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type NetworkExtension.NEVpnConnectionStartOptions

<pre style='color: green'>
public class NEVpnConnectionStartOptions : Foundation.DictionaryContainer {
	// constructors
	public NEVpnConnectionStartOptions ();
	public NEVpnConnectionStartOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSString Password { get; set; }
	public Foundation.NSString Username { get; set; }
}
</pre>

### New Type NetworkExtension.NEVpnIke2SecurityAssociationParameters

<pre style='color: green'>
public class NEVpnIke2SecurityAssociationParameters : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEVpnIke2SecurityAssociationParameters ();
	public NEVpnIke2SecurityAssociationParameters (Foundation.NSCoder coder);
	protected NEVpnIke2SecurityAssociationParameters (Foundation.NSObjectFlag t);
	protected NEVpnIke2SecurityAssociationParameters (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NEVpnIke2DiffieHellman DiffieHellmanGroup { get; set; }
	public virtual NEVpnIke2EncryptionAlgorithm EncryptionAlgorithm { get; set; }
	public virtual NEVpnIke2IntegrityAlgorithm IntegrityAlgorithm { get; set; }
	public virtual int LifetimeMinutes { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEVpnManager

<pre style='color: green'>
public class NEVpnManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEVpnManager (Foundation.NSObjectFlag t);
	protected NEVpnManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual NEVpnConnection Connection { get; }
	public virtual bool Enabled { get; set; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedDescription { get; set; }
	public virtual bool OnDemandEnabled { get; set; }
	public virtual NEOnDemandRule[] OnDemandRules { get; set; }
	public virtual NEVpnProtocol Protocol { get; set; }
	public virtual NEVpnProtocol ProtocolConfiguration { get; set; }
	public static NEVpnManager SharedManager { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void LoadFromPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task LoadFromPreferencesAsync ();
	public virtual void RemoveFromPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task RemoveFromPreferencesAsync ();
	public virtual void SaveToPreferences (System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task SaveToPreferencesAsync ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveConfigurationChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type NetworkExtension.NEVpnProtocol

<pre style='color: green'>
public abstract class NEVpnProtocol : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NEVpnProtocol ();
	protected NEVpnProtocol (Foundation.NSCoder coder);
	protected NEVpnProtocol (Foundation.NSObjectFlag t);
	protected NEVpnProtocol (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool DisconnectOnSleep { get; set; }
	public virtual Foundation.NSData IdentityData { get; set; }
	public virtual string IdentityDataPassword { get; set; }
	public virtual Foundation.NSData IdentityReference { get; set; }
	public virtual Foundation.NSData PasswordReference { get; set; }
	public virtual NEProxySettings ProxySettings { get; set; }
	public virtual string ServerAddress { get; set; }
	public virtual string Username { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type NetworkExtension.NEVpnProtocolIke2

<pre style='color: green'>
public class NEVpnProtocolIke2 : NetworkExtension.NEVpnProtocolIpSec, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEVpnProtocolIke2 ();
	public NEVpnProtocolIke2 (Foundation.NSCoder coder);
	protected NEVpnProtocolIke2 (Foundation.NSObjectFlag t);
	protected NEVpnProtocolIke2 (IntPtr handle);
	// properties
	public virtual NEVpnIke2CertificateType CertificateType { get; set; }
	public virtual NEVpnIke2SecurityAssociationParameters ChildSecurityAssociationParameters { get; }
	public override IntPtr ClassHandle { get; }
	public virtual NEVpnIke2DeadPeerDetectionRate DeadPeerDetectionRate { get; set; }
	public virtual bool DisableMobike { get; set; }
	public virtual bool DisableRedirect { get; set; }
	public virtual bool EnablePfs { get; set; }
	public virtual bool EnableRevocationCheck { get; set; }
	public virtual NEVpnIke2SecurityAssociationParameters IKESecurityAssociationParameters { get; }
	public virtual string ServerCertificateCommonName { get; set; }
	public virtual string ServerCertificateIssuerCommonName { get; set; }
	public virtual bool StrictRevocationCheck { get; set; }
	public virtual bool UseConfigurationAttributeInternalIPSubnet { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NEVpnProtocolIpSec

<pre style='color: green'>
public class NEVpnProtocolIpSec : NetworkExtension.NEVpnProtocol, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NEVpnProtocolIpSec ();
	public NEVpnProtocolIpSec (Foundation.NSCoder coder);
	protected NEVpnProtocolIpSec (Foundation.NSObjectFlag t);
	protected NEVpnProtocolIpSec (IntPtr handle);
	// properties
	public virtual NEVpnIkeAuthenticationMethod AuthenticationMethod { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string LocalIdentifier { get; set; }
	public virtual string RemoteIdentifier { get; set; }
	public virtual Foundation.NSData SharedSecretReference { get; set; }
	public virtual bool UseExtendedAuthentication { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NWBonjourServiceEndpoint

<pre style='color: green'>
public class NWBonjourServiceEndpoint : NetworkExtension.NWEndpoint, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NWBonjourServiceEndpoint (Foundation.NSObjectFlag t);
	protected NWBonjourServiceEndpoint (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Domain { get; }
	public virtual string Name { get; }
	public virtual string Type { get; }
	// methods
	public static NWBonjourServiceEndpoint Create (string name, string type, string domain);
}
</pre>

### New Type NetworkExtension.NWEndpoint

<pre style='color: green'>
public abstract class NWEndpoint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected NWEndpoint ();
	protected NWEndpoint (Foundation.NSObjectFlag t);
	protected NWEndpoint (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type NetworkExtension.NWHostEndpoint

<pre style='color: green'>
public class NWHostEndpoint : NetworkExtension.NWEndpoint, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWHostEndpoint ();
	protected NWHostEndpoint (Foundation.NSObjectFlag t);
	protected NWHostEndpoint (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Hostname { get; }
	public virtual string Port { get; }
	// methods
	public static NWHostEndpoint Create (string hostname, string port);
}
</pre>

### New Type NetworkExtension.NWPath

<pre style='color: green'>
public class NWPath : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWPath ();
	protected NWPath (Foundation.NSObjectFlag t);
	protected NWPath (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Expensive { get; }
	public virtual NWPathStatus Status { get; }
	// methods
	public virtual bool IsEqualToPath (NWPath path);
}
</pre>

### New Type NetworkExtension.NWPathStatus

<pre style='color: green'>
[Serializable]
public enum NWPathStatus {
	Invalid = 0,
	Satisfiable = 3,
	Satisfied = 1,
	Unsatisfied = 2,
}
</pre>

### New Type NetworkExtension.NWTcpConnection

<pre style='color: green'>
public class NWTcpConnection : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWTcpConnection ();
	protected NWTcpConnection (Foundation.NSObjectFlag t);
	public NWTcpConnection (NWTcpConnection connection);
	protected NWTcpConnection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NWPath ConnectedPath { get; }
	public virtual NWEndpoint Endpoint { get; }
	public virtual Foundation.NSError Error { get; }
	public virtual bool HasBetterPath { get; }
	public virtual NWEndpoint LocalAddress { get; }
	public virtual NWEndpoint RemoteAddress { get; }
	public virtual NWTcpConnectionState State { get; }
	public virtual Foundation.NSData TxtRecord { get; }
	public virtual bool Viable { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void ReadLength (uint length, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completion);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; ReadLengthAsync (uint length);
	public virtual void ReadMinimumLength (uint minimum, uint maximum, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completion);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; ReadMinimumLengthAsync (uint minimum, uint maximum);
	public virtual void Write (Foundation.NSData data, System.Action&lt;Foundation.NSError&gt; completion);
	public virtual System.Threading.Tasks.Task WriteAsync (Foundation.NSData data);
	public virtual void WriteClose ();
}
</pre>

### New Type NetworkExtension.NWTcpConnectionAuthenticationDelegate

<pre style='color: green'>
public class NWTcpConnectionAuthenticationDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, INWTcpConnectionAuthenticationDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWTcpConnectionAuthenticationDelegate ();
	protected NWTcpConnectionAuthenticationDelegate (Foundation.NSObjectFlag t);
	protected NWTcpConnectionAuthenticationDelegate (IntPtr handle);
	// methods
	public virtual void EvaluateTrust (NWTcpConnection connection, Foundation.NSArray peerCertificateChain, System.Action&lt;Security.SecTrust&gt; completion);
	public virtual System.Threading.Tasks.Task&lt;Security.SecTrust&gt; EvaluateTrustAsync (NWTcpConnection connection, Foundation.NSArray peerCertificateChain);
	public virtual void ProvideIdentity (NWTcpConnection connection, System.Action&lt;Security.SecIdentity,Foundation.NSArray&gt; completion);
	public virtual bool ShouldEvaluateTrust (NWTcpConnection connection);
	public virtual bool ShouldProvideIdentity (NWTcpConnection connection);
}
</pre>

### New Type NetworkExtension.NWTcpConnectionAuthenticationDelegate_Extensions

<pre style='color: green'>
public static class NWTcpConnectionAuthenticationDelegate_Extensions {
	// methods
	public static void EvaluateTrust (INWTcpConnectionAuthenticationDelegate This, NWTcpConnection connection, Foundation.NSArray peerCertificateChain, System.Action&lt;Security.SecTrust&gt; completion);
	public static System.Threading.Tasks.Task&lt;Security.SecTrust&gt; EvaluateTrustAsync (INWTcpConnectionAuthenticationDelegate This, NWTcpConnection connection, Foundation.NSArray peerCertificateChain);
	public static void ProvideIdentity (INWTcpConnectionAuthenticationDelegate This, NWTcpConnection connection, System.Action&lt;Security.SecIdentity,Foundation.NSArray&gt; completion);
	public static bool ShouldEvaluateTrust (INWTcpConnectionAuthenticationDelegate This, NWTcpConnection connection);
	public static bool ShouldProvideIdentity (INWTcpConnectionAuthenticationDelegate This, NWTcpConnection connection);
}
</pre>

### New Type NetworkExtension.NWTcpConnectionState

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

### New Type NetworkExtension.NWTlsParameters

<pre style='color: green'>
public class NWTlsParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWTlsParameters ();
	protected NWTlsParameters (Foundation.NSObjectFlag t);
	protected NWTlsParameters (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint MaximumSslProtocolVersion { get; set; }
	public virtual uint MinimumSslProtocolVersion { get; set; }
	public virtual Foundation.NSSet&lt;Foundation.NSNumber&gt; SslCipherSuites { get; set; }
	public virtual Foundation.NSData TlsSessionID { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type NetworkExtension.NWUdpSession

<pre style='color: green'>
public class NWUdpSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NWUdpSession ();
	protected NWUdpSession (Foundation.NSObjectFlag t);
	public NWUdpSession (NWUdpSession session);
	protected NWUdpSession (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NWPath CurrentPath { get; }
	public virtual NWEndpoint Endpoint { get; }
	public virtual bool HasBetterPath { get; }
	public virtual uint MaximumDatagramLength { get; }
	public virtual NWEndpoint ResolvedEndpoint { get; }
	public virtual NWUdpSessionState State { get; }
	public virtual bool Viable { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void SetReadHandler (System.Action&lt;Foundation.NSArray,Foundation.NSError&gt; handler, uint maxDatagrams);
	public virtual void TryNextResolvedEndpoint ();
	public virtual void WriteDatagram (Foundation.NSData datagram, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task WriteDatagramAsync (Foundation.NSData datagram);
	public virtual void WriteMultipleDatagrams (Foundation.NSData[] datagramArray, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task WriteMultipleDatagramsAsync (Foundation.NSData[] datagramArray);
}
</pre>

### New Type NetworkExtension.NWUdpSessionState

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

### Type Changed: ObjCRuntime.Class

Added method:

<pre style='color: green'>
	public static System.Type Lookup (Class class);
</pre>

### Type Changed: ObjCRuntime.Constants

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

Added values:

<pre style='color: green'>
	iOS_9_0 = 589824,
	Mac_10_10_3 = 2825757768286208,
	Mac_10_11 = 2826844395012096,
</pre>

### Type Changed: ObjCRuntime.PlatformHelper

Added method:

<pre style='color: green'>
	public static bool CheckSystemVersion (int major, int minor);
</pre>

### New Type ObjCRuntime.DesignatedInitializerAttribute

<pre style='color: green'>
public class DesignatedInitializerAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public DesignatedInitializerAttribute ();
}
</pre>

## Namespace OpenTK

### New Type OpenTK.Vector2i

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

### New Type OpenTK.Vector3i

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

### New Type OpenTK.Vector4i

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

Modified methods:

```
public virtual Foundation.NSObject GetAttribute (string attributeKey)
	public virtual void SetAttribute (Foundation.NSObject attribute, string key)
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
[Obsolete ()]
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

### Type Changed: SceneKit.SCNAction

Added methods:

<pre style='color: green'>
	public static SCNAction Hide ();
	public static SCNAction PlayAudioSource (SCNAudioSource source, bool wait);
	public static SCNAction Unhide ();
</pre>

### Type Changed: SceneKit.SCNActionable

Added property:

<pre style='color: green'>
	public virtual string[] ActionKeys { get; }
</pre>

### Type Changed: SceneKit.SCNCamera

Added method:

<pre style='color: green'>
	public static SCNCamera FromModelCamera (ModelIO.MDLCamera modelCamera);
</pre>

### Type Changed: SceneKit.SCNGeometry

Added properties:

<pre style='color: green'>
	public virtual SCNGeometryElement[] GeometryElements { get; }
	public virtual SCNGeometrySource[] GeometrySources { get; }
</pre>

Added method:

<pre style='color: green'>
	public static SCNGeometry FromMesh (ModelIO.MDLMesh mesh);
</pre>

### Type Changed: SceneKit.SCNGeometryElement

Added method:

<pre style='color: green'>
	public static SCNGeometryElement FromSubmesh (ModelIO.MDLSubmesh submesh);
</pre>

### Type Changed: SceneKit.SCNGeometrySource

Modified methods:

```
public SCNGeometrySource FromData (Foundation.NSData data, SCNGeometrySourceSemantics geometrySourceSemantic semantic, nint vectorCount, bool floatComponents, nint componentsPerVector, nint bytesPerComponent, nint offset, nint stride)
```

Added methods:

<pre style='color: green'>
	public static SCNGeometrySource FromMetalBuffer (Metal.IMTLBuffer mtlBuffer, Metal.MTLVertexFormat vertexFormat, Foundation.NSString geometrySourceSemantic, nint vertexCount, nint offset, nint stride);
	public static SCNGeometrySource FromMetalBuffer (Metal.IMTLBuffer mtlBuffer, Metal.MTLVertexFormat vertexFormat, SCNGeometrySourceSemantics semantic, nint vertexCount, nint offset, nint stride);
</pre>

### Type Changed: SceneKit.SCNIKConstraint

Added constructor:

<pre style='color: green'>
	public SCNIKConstraint (SCNNode chainRootNode);
</pre>

### Type Changed: SceneKit.SCNLayer

Added properties:

<pre style='color: green'>
	public virtual AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual Metal.MTLPixelFormat ColorPixelFormat { get; }
	public virtual Metal.IMTLCommandQueue CommandQueue { get; }
	public virtual Metal.IMTLRenderCommandEncoder CurrentRenderCommandEncoder { get; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual Metal.MTLPixelFormat DepthPixelFormat { get; }
	public virtual Metal.IMTLDevice Device { get; }
	public virtual SCNRenderingApi RenderingApi { get; }
	public virtual Metal.MTLPixelFormat StencilPixelFormat { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
	public virtual void PresentScene (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView, System.Action completionHandler);
</pre>

### Type Changed: SceneKit.SCNLight

Added method:

<pre style='color: green'>
	public static SCNLight FromModelLight (ModelIO.MDLLight mdllight);
</pre>

### Type Changed: SceneKit.SCNMaterial

Added properties:

<pre style='color: green'>
	public virtual SCNMaterialProperty AmbientOcclusion { get; }
	public virtual SCNBlendMode BlendMode { get; set; }
	public virtual SCNMaterialProperty SelfIllumination { get; }
</pre>

Added method:

<pre style='color: green'>
	public static SCNMaterial FromMaterial (ModelIO.MDLMaterial material);
</pre>

### Type Changed: SceneKit.SCNNode

Added properties:

<pre style='color: green'>
	public virtual string[] ActionKeys { get; }
	public virtual SCNAudioPlayer[] AudioPlayers { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddAudioPlayer (SCNAudioPlayer player);
	public static SCNNode FromModelObject (ModelIO.MDLObject mdlObject);
	public virtual void RemoveAllAudioPlayers ();
	public virtual void RemoveAudioPlayer (SCNAudioPlayer player);
</pre>

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

### Type Changed: SceneKit.SCNPhysicsBody

Added properties:

<pre style='color: green'>
	public virtual bool AffectedByGravity { get; set; }
	public virtual uint ContactTestBitMask { get; set; }
	public virtual SCNVector3 MomentOfInertia { get; set; }
	public virtual bool UsesDefaultMomentOfInertia { get; set; }
</pre>

### Type Changed: SceneKit.SCNPhysicsShape

Added properties:

<pre style='color: green'>
	public SCNPhysicsShapeOptions Options { get; }
	public virtual Foundation.NSObject SourceObject { get; }
	public virtual Foundation.NSValue[] Transforms { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: SceneKit.SCNProgram

Added properties:

<pre style='color: green'>
	public virtual string FragmentFunctionName { get; set; }
	public virtual Metal.IMTLLibrary Library { get; set; }
	public virtual string VertexFunctionName { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void HandleBinding (string name, SCNBufferFrequency frequency, SCNBufferBindingHandler handler);
</pre>

### Type Changed: SceneKit.SCNProgramDelegate

Removed methods:

<pre style='color: red'>
	public virtual bool BindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public virtual bool IsProgramOpaque (SCNProgram program);
	public virtual void UnbindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
</pre>

### Type Changed: SceneKit.SCNProgramDelegate_Extensions

Removed methods:

<pre style='color: red'>
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
</pre>

### Type Changed: SceneKit.SCNRenderer

Added properties:

<pre style='color: green'>
	public virtual AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual Metal.MTLPixelFormat ColorPixelFormat { get; }
	public virtual Metal.IMTLCommandQueue CommandQueue { get; }
	public virtual Metal.IMTLRenderCommandEncoder CurrentRenderCommandEncoder { get; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual Metal.MTLPixelFormat DepthPixelFormat { get; }
	public virtual Metal.IMTLDevice Device { get; }
	public virtual SCNRenderingApi RenderingApi { get; }
	public virtual Metal.MTLPixelFormat StencilPixelFormat { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static SCNRenderer FromDevice (Metal.IMTLDevice device, Foundation.NSDictionary options);
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
	public virtual void PresentScene (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView, System.Action completionHandler);
	public virtual void Render (double timeInSeconds, CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);
</pre>

### Type Changed: SceneKit.SCNScene

Added method:

<pre style='color: green'>
	public static SCNScene FromAsset (ModelIO.MDLAsset asset);
</pre>

### Type Changed: SceneKit.SCNSceneRenderer

Added properties:

<pre style='color: green'>
	public virtual AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual Metal.MTLPixelFormat ColorPixelFormat { get; }
	public virtual Metal.IMTLCommandQueue CommandQueue { get; }
	public virtual Metal.IMTLRenderCommandEncoder CurrentRenderCommandEncoder { get; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual Metal.MTLPixelFormat DepthPixelFormat { get; }
	public virtual Metal.IMTLDevice Device { get; }
	public virtual SCNRenderingApi RenderingApi { get; }
	public virtual Metal.MTLPixelFormat StencilPixelFormat { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
	public virtual void PresentScene (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView, System.Action completionHandler);
</pre>

### Type Changed: SceneKit.SCNSceneRenderer_Extensions

Added methods:

<pre style='color: green'>
	public static AVFoundation.AVAudioEngine GetAudioEngine (ISCNSceneRenderer This);
	public static AVFoundation.AVAudioEnvironmentNode GetAudioEnvironmentNode (ISCNSceneRenderer This);
	public static SCNNode GetAudioListener (ISCNSceneRenderer This);
	public static Metal.MTLPixelFormat GetColorPixelFormat (ISCNSceneRenderer This);
	public static Metal.IMTLCommandQueue GetCommandQueue (ISCNSceneRenderer This);
	public static Metal.IMTLRenderCommandEncoder GetCurrentRenderCommandEncoder (ISCNSceneRenderer This);
	public static SCNDebugOptions GetDebugOptions (ISCNSceneRenderer This);
	public static Metal.MTLPixelFormat GetDepthPixelFormat (ISCNSceneRenderer This);
	public static Metal.IMTLDevice GetDevice (ISCNSceneRenderer This);
	public static SCNNode[] GetNodesInsideFrustum (ISCNSceneRenderer This, SCNNode pointOfView);
	public static SCNRenderingApi GetRenderingApi (ISCNSceneRenderer This);
	public static Metal.MTLPixelFormat GetStencilPixelFormat (ISCNSceneRenderer This);
	public static void PresentScene (ISCNSceneRenderer This, SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView, System.Action completionHandler);
	public static void SetAudioListener (ISCNSceneRenderer This, SCNNode value);
	public static void SetDebugOptions (ISCNSceneRenderer This, SCNDebugOptions value);
</pre>

### Type Changed: SceneKit.SCNTechnique

Added property:

<pre style='color: green'>
	public Foundation.NSObject Item { get; set; }
</pre>

### Type Changed: SceneKit.SCNView

Added constructor:

<pre style='color: green'>
	public SCNView (CoreGraphics.CGRect frame, SCNRenderingOptions options);
</pre>

Added properties:

<pre style='color: green'>
	public virtual AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual Metal.MTLPixelFormat ColorPixelFormat { get; }
	public virtual Metal.IMTLCommandQueue CommandQueue { get; }
	public virtual Metal.IMTLRenderCommandEncoder CurrentRenderCommandEncoder { get; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual Metal.MTLPixelFormat DepthPixelFormat { get; }
	public virtual Metal.IMTLDevice Device { get; }
	public virtual SCNRenderingApi RenderingApi { get; }
	public virtual Metal.MTLPixelFormat StencilPixelFormat { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
	public virtual void PresentScene (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView, System.Action completionHandler);
</pre>

### New Type SceneKit.ISCNBufferStream

<pre style='color: green'>
public interface ISCNBufferStream : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Length (IntPtr bytes, uint length);
}
</pre>

### New Type SceneKit.SCNActionable_Extensions

<pre style='color: green'>
public static class SCNActionable_Extensions {
	// methods
	public static string[] GetActionKeys (ISCNActionable This);
}
</pre>

### New Type SceneKit.SCNAudioPlayer

<pre style='color: green'>
public class SCNAudioPlayer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SCNAudioPlayer (AVFoundation.AVAudioNode audioNode);
	protected SCNAudioPlayer (Foundation.NSObjectFlag t);
	public SCNAudioPlayer (SCNAudioSource source);
	protected SCNAudioPlayer (IntPtr handle);
	// properties
	public virtual AVFoundation.AVAudioNode AudioNode { get; }
	public virtual SCNAudioSource AudioSource { get; }
	public override IntPtr ClassHandle { get; }
	public virtual System.Action DidFinishPlayback { get; set; }
	public virtual System.Action WillStartPlayback { get; set; }
	// methods
	public static SCNAudioPlayer AVAudioNode (AVFoundation.AVAudioNode audioNode);
	protected override void Dispose (bool disposing);
	public static SCNAudioPlayer FromSource (SCNAudioSource source);
}
</pre>

### New Type SceneKit.SCNAudioSource

<pre style='color: green'>
public class SCNAudioSource : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SCNAudioSource (Foundation.NSCoder coder);
	protected SCNAudioSource (Foundation.NSObjectFlag t);
	public SCNAudioSource (Foundation.NSUrl url);
	protected SCNAudioSource (IntPtr handle);
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
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SCNAudioSource FromFile (string fileName);
	public virtual void Load ();
}
</pre>

### New Type SceneKit.SCNBillboardAxis

<pre style='color: green'>
[Serializable]
public enum SCNBillboardAxis {
	All = 7,
	X = 1,
	Y = 2,
	Z = 4,
}
</pre>

### New Type SceneKit.SCNBillboardConstraint

<pre style='color: green'>
public class SCNBillboardConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SCNBillboardConstraint ();
	public SCNBillboardConstraint (Foundation.NSCoder coder);
	protected SCNBillboardConstraint (Foundation.NSObjectFlag t);
	protected SCNBillboardConstraint (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual SCNBillboardAxis FreeAxes { get; set; }
	// methods
	public static SCNBillboardConstraint Create ();
}
</pre>

### New Type SceneKit.SCNBlendMode

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

### New Type SceneKit.SCNBufferBindingHandler

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

### New Type SceneKit.SCNBufferFrequency

<pre style='color: green'>
[Serializable]
public enum SCNBufferFrequency {
	Frame = 0,
	Node = 1,
	Shadable = 2,
}
</pre>

### New Type SceneKit.SCNDebugOptions

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

### New Type SceneKit.SCNReferenceLoadingPolicy

<pre style='color: green'>
[Serializable]
public enum SCNReferenceLoadingPolicy {
	Immediate = 0,
	OnDemand = 1,
}
</pre>

### New Type SceneKit.SCNReferenceNode

<pre style='color: green'>
public class SCNReferenceNode : SceneKit.SCNNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNActionable, ISCNAnimatable, ISCNBoundingVolume, System.Collections.Generic.IEnumerable&lt;SCNNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SCNReferenceNode (Foundation.NSCoder coder);
	protected SCNReferenceNode (Foundation.NSObjectFlag t);
	public SCNReferenceNode (Foundation.NSUrl referenceUrl);
	protected SCNReferenceNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Loaded { get; }
	public virtual SCNReferenceLoadingPolicy LoadingPolicy { get; set; }
	public virtual Foundation.NSUrl ReferenceUrl { get; set; }
	// methods
	public static SCNReferenceNode CreateFromUrl (Foundation.NSUrl referenceUrl);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void Load ();
	public virtual void Unload ();
}
</pre>

### New Type SceneKit.SCNRenderingApi

<pre style='color: green'>
[Serializable]
public enum SCNRenderingApi {
	Metal = 0,
	OpenGLCore32 = 2,
	OpenGLCore41 = 3,
	OpenGLLegacy = 1,
}
</pre>

### New Type SceneKit.SCNRenderingOptions

<pre style='color: green'>
public class SCNRenderingOptions : Foundation.DictionaryContainer {
	// constructors
	public SCNRenderingOptions ();
	public SCNRenderingOptions (Foundation.NSDictionary dictionary);
	// properties
	public Metal.IMTLDevice Device { get; set; }
	public bool? LowPowerDevice { get; set; }
	public SCNRenderingApi? RenderingApi { get; set; }
}
</pre>

## Namespace ScriptingBridge

### Type Changed: ScriptingBridge.SBElementArray

Added constructor:

<pre style='color: green'>
	public SBElementArray (uint capacity);
</pre>

## Namespace Security

### Type Changed: Security.SecAccessControl

Added interfaces:

<pre style='color: green'>
	ObjCRuntime.INativeObject
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
	protected virtual void Dispose (bool disposing);
</pre>

### Type Changed: Security.SecAccessControlCreateFlags

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

### Type Changed: Security.SecPolicyIdentifier

Added property:

<pre style='color: green'>
	public static Foundation.NSString ApplePayIssuerEncryption { get; }
</pre>

### Type Changed: Security.SecRecord

Added property:

<pre style='color: green'>
	public SecAuthenticationUI AuthenticationUI { get; set; }
</pre>

### Type Changed: Security.SslCipherSuite

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

### Type Changed: Security.SslContext

Added method:

<pre style='color: green'>
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);
</pre>

### Type Changed: Security.SslSessionOption

Added values:

<pre style='color: green'>
	AllowServerIdentityChange = 5,
	BreakOnClientHello = 7,
</pre>

### Type Changed: Security.SslStatus

Added values:

<pre style='color: green'>
	SSLClientHelloReceived = -9851,
	SSLWeakPeerEphemeralDHKey = -9850,
</pre>

### New Type Security.SecAuthenticationUI

<pre style='color: green'>
[Serializable]
public enum SecAuthenticationUI {
	Allow = 0,
	Fail = 1,
	NotSet = -1,
	Skip = 2,
}
</pre>

### New Type Security.SslSessionStrengthPolicy

<pre style='color: green'>
[Serializable]
public enum SslSessionStrengthPolicy {
	ATSv1 = 1,
	Default = 0,
}
</pre>

## Namespace SpriteKit

### Type Changed: SpriteKit.SKAction

Added methods:

<pre style='color: green'>
	public static SKAction AnimateWithNormalTextures (SKTexture[] textures, double secondsPerFrame);
	public static SKAction AnimateWithNormalTextures (SKTexture[] textures, double secondsPerFrame, bool resize, bool restore);
	public static SKAction Create (string name);
	public static SKAction Create (string name, Foundation.NSUrl url);
	public static SKAction Create (string name, double duration);
	public static SKAction Create (string name, Foundation.NSUrl url, double duration);
	public static SKAction CreateApplyAngularImpulse (nfloat impulse, double duration);
	public static SKAction CreateApplyForce (CoreGraphics.CGVector force, double duration);
	public static SKAction CreateApplyForce (CoreGraphics.CGVector force, CoreGraphics.CGPoint point, double duration);
	public static SKAction CreateApplyImpulse (CoreGraphics.CGVector impulse, double duration);
	public static SKAction CreateApplyImpulse (CoreGraphics.CGVector impulse, CoreGraphics.CGPoint point, double duration);
	public static SKAction CreateApplyTorque (nfloat torque, double duration);
	public static SKAction CreateChangeChargeBy (float by, double duration);
	public static SKAction CreateChangeChargeTo (float newCharge, double duration);
	public static SKAction CreateChangeMassBy (float by, double duration);
	public static SKAction CreateChangeMassTo (float newMass, double duration);
	public static SKAction CreateChangeObstructionBy (float by, double duration);
	public static SKAction CreateChangeObstructionTo (float target, double duration);
	public static SKAction CreateChangeOcclusionBy (float by, double duration);
	public static SKAction CreateChangeOcclusionTo (float target, double duration);
	public static SKAction CreateChangePlaybackRate (float playbackRate, double duration);
	public static SKAction CreateChangePlaybackRateBy (float playbackRate, double duration);
	public static SKAction CreateChangeReverbBy (float by, double duration);
	public static SKAction CreateChangeReverbTo (float target, double duration);
	public static SKAction CreateChangeVolume (float newVolume, double duration);
	public static SKAction CreateChangeVolumeBy (float by, double duration);
	public static SKAction CreatePause ();
	public static SKAction CreatePlay ();
	public static SKAction CreateStereoPanBy (float by, double duration);
	public static SKAction CreateStereoPanTo (float target, double duration);
	public static SKAction CreateStop ();
	public static SKAction SetNormalTexture (SKTexture texture);
	public static SKAction SetNormalTexture (SKTexture texture, bool resize);
</pre>

### Type Changed: SpriteKit.SKEmitterNode

Added property:

<pre style='color: green'>
	public virtual SKParticleRenderOrder ParticleRenderOrder { get; set; }
</pre>

### Type Changed: SpriteKit.SKFieldNode

Obsoleted methods:

```
[Obsolete ()]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

### Type Changed: SpriteKit.SKNode

Added methods:

<pre style='color: green'>
	public virtual void MoveToParent (SKNode parent);
	public static GameplayKit.GKPolygonObstacle[] ObstaclesFromNodeBounds (SKNode[] nodes);
	public static GameplayKit.GKPolygonObstacle[] ObstaclesFromNodePhysicsBodies (SKNode[] nodes);
	public static GameplayKit.GKPolygonObstacle[] ObstaclesFromSpriteTextures (SKNode[] sprites, float accuracy);
</pre>

### Type Changed: SpriteKit.SKScene

Added properties:

<pre style='color: green'>
	public virtual AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual SKCameraNode Camera { get; set; }
	public virtual SKNode Listener { get; set; }
</pre>

### Type Changed: SpriteKit.SKTexture

Added property:

<pre style='color: green'>
	public virtual CoreGraphics.CGImage CGImage { get; }
</pre>

### Type Changed: SpriteKit.SKTextureAtlas

Added methods:

<pre style='color: green'>
	public static void PreloadTextureAtlases (string[] atlasNames, SKTextureAtlasLoadCallback completionHandler);
	public static System.Threading.Tasks.Task&lt;SKTextureAtlasLoadResult&gt; PreloadTextureAtlasesAsync (string[] atlasNames);
</pre>

### Type Changed: SpriteKit.SKTransition

Added interface:

<pre style='color: green'>
	Foundation.INSCopying
</pre>

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
</pre>

### Type Changed: SpriteKit.SKView

Added constructor:

<pre style='color: green'>
	public SKView (CoreGraphics.CGRect frame);
</pre>

### New Type SpriteKit.SKAudioNode

<pre style='color: green'>
public class SKAudioNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SKAudioNode (AVFoundation.AVAudioNode node);
	public SKAudioNode (Foundation.NSCoder coder);
	protected SKAudioNode (Foundation.NSObjectFlag t);
	public SKAudioNode (Foundation.NSUrl url);
	protected SKAudioNode (IntPtr handle);
	public SKAudioNode (string fileName);
	// properties
	public virtual bool AutoplayLooped { get; set; }
	public virtual AVFoundation.AVAudioNode AvAudioNode { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual bool Positional { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type SpriteKit.SKCameraNode

<pre style='color: green'>
public class SKCameraNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SKCameraNode ();
	public SKCameraNode (Foundation.NSCoder coder);
	protected SKCameraNode (Foundation.NSObjectFlag t);
	protected SKCameraNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSSet&lt;SKNode&gt; ContainedNodeSet { get; }
	// methods
	public virtual bool Contains (SKNode node);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type SpriteKit.SKParticleRenderOrder

<pre style='color: green'>
[Serializable]
public enum SKParticleRenderOrder {
	DontCare = 2,
	OldestFirst = 1,
	OldestLast = 0,
}
</pre>

### New Type SpriteKit.SKReferenceNode

<pre style='color: green'>
public class SKReferenceNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SKReferenceNode (Foundation.NSCoder coder);
	protected SKReferenceNode (Foundation.NSObjectFlag t);
	public SKReferenceNode (Foundation.NSUrl url);
	protected SKReferenceNode (IntPtr handle);
	public SKReferenceNode (string fileName);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void DidLoadReferenceNode (SKNode node);
	public static SKReferenceNode FromFile (string fileName);
	public static SKReferenceNode FromUrl (Foundation.NSUrl referenceUrl);
	public virtual void Resolve ();
}
</pre>

### New Type SpriteKit.SKTextureAtlasLoadCallback

<pre style='color: green'>
public sealed delegate SKTextureAtlasLoadCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKTextureAtlasLoadCallback (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSError error, SKTextureAtlas foundAtlases, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSError error, SKTextureAtlas foundAtlases);
}
</pre>

### New Type SpriteKit.SKTextureAtlasLoadResult

<pre style='color: green'>
public class SKTextureAtlasLoadResult {
	// constructors
	public SKTextureAtlasLoadResult (Foundation.NSError error, SKTextureAtlas foundAtlases);
	// properties
	public Foundation.NSError Error { get; set; }
	public SKTextureAtlas FoundAtlases { get; set; }
}
</pre>

## Namespace VideoToolbox

### Type Changed: VideoToolbox.VTDecompressionProperties

Added property:

<pre style='color: green'>
	public VTPixelTransferProperties PixelTransferSettings { get; set; }
</pre>

### New Type VideoToolbox.VTDownsamplingMode

<pre style='color: green'>
[Serializable]
public enum VTDownsamplingMode {
	Average = 2,
	Decimate = 1,
	Unset = 0,
}
</pre>

### New Type VideoToolbox.VTPixelTransferProperties

<pre style='color: green'>
public class VTPixelTransferProperties : Foundation.DictionaryContainer {
	// constructors
	public VTPixelTransferProperties ();
	public VTPixelTransferProperties (Foundation.NSDictionary dictionary);
	// properties
	public AVFoundation.AVVideoCleanApertureSettings DestinationCleanAperture { get; set; }
	public VTColorPrimaries DestinationColorPrimaries { get; set; }
	public Foundation.NSData DestinationICCProfile { get; set; }
	public AVFoundation.AVVideoPixelAspectRatioSettings DestinationPixelAspectRatio { get; set; }
	public VTTransferFunction DestinationTransferFunction { get; set; }
	public VTYCbCrMatrix DestinationYCbCrMatrix { get; set; }
	public VTDownsamplingMode DownsamplingMode { get; set; }
	public VTScalingMode ScalingMode { get; set; }
}
</pre>

### New Type VideoToolbox.VTPixelTransferPropertyKeys

<pre style='color: green'>
public static class VTPixelTransferPropertyKeys {
	// properties
	public static Foundation.NSString DestinationCleanAperture { get; }
	public static Foundation.NSString DestinationColorPrimaries { get; }
	public static Foundation.NSString DestinationICCProfile { get; }
	public static Foundation.NSString DestinationPixelAspectRatio { get; }
	public static Foundation.NSString DestinationTransferFunction { get; }
	public static Foundation.NSString DestinationYCbCrMatrix { get; }
	public static Foundation.NSString DownsamplingMode { get; }
	public static Foundation.NSString DownsamplingMode_Average { get; }
	public static Foundation.NSString DownsamplingMode_Decimate { get; }
	public static Foundation.NSString ScalingMode { get; }
	public static Foundation.NSString ScalingMode_CropSourceToCleanAperture { get; }
	public static Foundation.NSString ScalingMode_Letterbox { get; }
	public static Foundation.NSString ScalingMode_Normal { get; }
	public static Foundation.NSString ScalingMode_Trim { get; }
}
</pre>

### New Type VideoToolbox.VTScalingMode

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

### New Type VideoToolbox.VTUtilities

<pre style='color: green'>
public static class VTUtilities {
	// methods
	public static VTStatus ToCGImage (CoreVideo.CVPixelBuffer pixelBuffer, out CoreGraphics.CGImage image);
}
</pre>

## Namespace WebKit

### Type Changed: WebKit.DomEvent

Added constructor:

<pre style='color: green'>
	public DomEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void InitEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
```

### Type Changed: WebKit.DomKeyboardEvent

Added constructors:

<pre style='color: green'>
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	[Obsolete ()]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: WebKit.DomMouseEvent

Added constructor:

<pre style='color: green'>
	public DomMouseEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, IDomEventTarget relatedTarget);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, IDomEventTarget relatedTarget);
```

### Type Changed: WebKit.DomOverflowEvent

Added constructor:

<pre style='color: green'>
	public DomOverflowEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
</pre>

Obsoleted methods:

```
[Obsolete ()]
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
[Obsolete ()]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
```

### Type Changed: WebKit.DomWheelEvent

Added constructor:

<pre style='color: green'>
	public DomWheelEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete ()]
	public virtual void InitEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: WebKit.WKErrorCode

Added value:

<pre style='color: green'>
	JavaScriptResultTypeIsUnsupported = 5,
</pre>

### Type Changed: WebKit.WKFrameInfo

Added property:

<pre style='color: green'>
	public virtual WKSecurityOrigin SecurityOrigin { get; }
</pre>

### Type Changed: WebKit.WKNavigationDelegate

Added method:

<pre style='color: green'>
	public virtual void ContentProcessDidTerminate (WKWebView webView);
</pre>

### Type Changed: WebKit.WKNavigationDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void ContentProcessDidTerminate (IWKNavigationDelegate This, WKWebView webView);
</pre>

### Type Changed: WebKit.WKUIDelegate

Added method:

<pre style='color: green'>
	public virtual void DidClose (WKWebView webView);
</pre>

### Type Changed: WebKit.WKUIDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DidClose (IWKUIDelegate This, WKWebView webView);
</pre>

### Type Changed: WebKit.WKWebView

Added properties:

<pre style='color: green'>
	public virtual bool AllowsLinkPreview { get; set; }
	public virtual Security.SecCertificate[] CertificateChain { get; }
	public virtual string CustomUserAgent { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public void EvaluateJavaScript (string javascript, WKJavascriptEvaluationResult completionHandler);
	public System.Threading.Tasks.Task&lt;Foundation.NSObject&gt; EvaluateJavaScriptAsync (string javascript);
	public virtual WKNavigation LoadData (Foundation.NSData data, string mimeType, string characterEncodingName, Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadFileUrl (Foundation.NSUrl url, Foundation.NSUrl readAccessUrl);
	public WKNavigation LoadHtmlString (string htmlString, Foundation.NSUrl baseUrl);
</pre>

### Type Changed: WebKit.WKWebViewConfiguration

Added properties:

<pre style='color: green'>
	public virtual bool AllowsAirPlayForMediaPlayback { get; set; }
	public virtual string ApplicationNameForUserAgent { get; set; }
	public virtual WKWebsiteDataStore WebsiteDataStore { get; set; }
</pre>

### New Type WebKit.WKSecurityOrigin

<pre style='color: green'>
public class WKSecurityOrigin : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected WKSecurityOrigin (Foundation.NSObjectFlag t);
	protected WKSecurityOrigin (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Host { get; }
	public virtual nint Port { get; }
	public virtual string Protocol { get; }
}
</pre>

### New Type WebKit.WKWebsiteDataRecord

<pre style='color: green'>
public class WKWebsiteDataRecord : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public WKWebsiteDataRecord ();
	protected WKWebsiteDataRecord (Foundation.NSObjectFlag t);
	protected WKWebsiteDataRecord (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSSet&lt;Foundation.NSString&gt; DataTypes { get; }
	public virtual string DisplayName { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type WebKit.WKWebsiteDataStore

<pre style='color: green'>
public class WKWebsiteDataStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public WKWebsiteDataStore ();
	protected WKWebsiteDataStore (Foundation.NSObjectFlag t);
	protected WKWebsiteDataStore (IntPtr handle);
	// properties
	public static Foundation.NSSet&lt;Foundation.NSString&gt; AllWebsiteDataTypes { get; }
	public override IntPtr ClassHandle { get; }
	public static WKWebsiteDataStore DefaultDataStore { get; }
	public static WKWebsiteDataStore NonPersistentDataStore { get; }
	public virtual bool Persistent { get; }
	// methods
	public virtual void FetchDataRecordsOfTypes (Foundation.NSSet&lt;Foundation.NSString&gt; dataTypes, System.Action&lt;Foundation.NSArray&gt; completionHandler);
	public virtual void RemoveDataOfTypes (Foundation.NSSet&lt;Foundation.NSString&gt; websiteDataTypes, Foundation.NSDate date, System.Action completionHandler);
	public virtual void RemoveDataOfTypes (Foundation.NSSet&lt;Foundation.NSString&gt; dataTypes, WKWebsiteDataRecord[] dataRecords, System.Action completionHandler);
}
</pre>

### New Type WebKit.WKWebsiteDataType

<pre style='color: green'>
public static class WKWebsiteDataType {
	// properties
	public static Foundation.NSString Cookies { get; }
	public static Foundation.NSString DiskCache { get; }
	public static Foundation.NSString IndexedDBDatabases { get; }
	public static Foundation.NSString LocalStorage { get; }
	public static Foundation.NSString MemoryCache { get; }
	public static Foundation.NSString OfflineWebApplicationCache { get; }
	public static Foundation.NSString SessionStorage { get; }
	public static Foundation.NSString WebSQLDatabases { get; }
}
</pre>

## New Namespace Contacts

### New Type Contacts.CNAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum CNAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
</pre>

### New Type Contacts.CNContact

<pre style='color: green'>
public class CNContact : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContact ();
	public CNContact (Foundation.NSCoder coder);
	protected CNContact (Foundation.NSObjectFlag t);
	protected CNContact (IntPtr handle);
	// properties
	public virtual Foundation.NSDateComponents Birthday { get; }
	public override IntPtr ClassHandle { get; }
	public virtual Contacts.CNLabeledValue&lt;CNContactRelation&gt;[] ContactRelations { get; }
	public virtual CNContactType ContactType { get; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSDateComponents&gt;[] Dates { get; }
	public virtual string DepartmentName { get; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSString&gt;[] EmailAddresses { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual string FamilyName { get; }
	public virtual string GivenName { get; }
	public virtual string Identifier { get; }
	public virtual Foundation.NSData ImageData { get; }
	public virtual Contacts.CNLabeledValue&lt;CNInstantMessageAddress&gt;[] InstantMessageAddresses { get; }
	public virtual string JobTitle { get; }
	public virtual string MiddleName { get; }
	public virtual string NamePrefix { get; }
	public virtual string NameSuffix { get; }
	public virtual string Nickname { get; }
	public virtual Foundation.NSDateComponents NonGregorianBirthday { get; }
	public virtual string Note { get; }
	public virtual string OrganizationName { get; }
	public virtual Contacts.CNLabeledValue&lt;CNPhoneNumber&gt;[] PhoneNumbers { get; }
	public virtual string PhoneticFamilyName { get; }
	public virtual string PhoneticGivenName { get; }
	public virtual string PhoneticMiddleName { get; }
	public virtual Contacts.CNLabeledValue&lt;CNPostalAddress&gt;[] PostalAddresses { get; }
	public virtual string PreviousFamilyName { get; }
	public static Foundation.NSString PropertyNotFetchedExceptionName { get; }
	public virtual Contacts.CNLabeledValue&lt;CNSocialProfile&gt;[] SocialProfiles { get; }
	public virtual Foundation.NSData ThumbnailImageData { get; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSString&gt;[] UrlAddresses { get; }
	// methods
	public bool AreKeysAvailable (CNContactOptions options);
	protected virtual bool AreKeysAvailable (Foundation.NSArray keyDescriptors);
	public bool AreKeysAvailable&lt;T&gt; (T[] keyDescriptors);
	public static System.Func&lt;Foundation.NSObject,Foundation.NSObject,Foundation.NSComparisonResult&gt; ComparatorForName (CNContactSortOrder sortOrder);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static ICNKeyDescriptor GetDescriptorForAllComparatorKeys ();
	public static Foundation.NSPredicate GetPredicateForContacts (string matchingName);
	public static Foundation.NSPredicate GetPredicateForContacts (string[] identifiers);
	public static Foundation.NSPredicate GetPredicateForContactsInContainer (string containerIdentifier);
	public static Foundation.NSPredicate GetPredicateForContactsInGroup (string groupIdentifier);
	public virtual bool IsKeyAvailable (CNContactOptions options);
	public virtual bool IsKeyAvailable (Foundation.NSString contactKey);
	public virtual bool IsUnifiedWithContact (string contactIdentifier);
	public static string LocalizeProperty (CNContactOptions options);
	public static string LocalizeProperty (Foundation.NSString contactKey);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNContactDisplayNameOrder

<pre style='color: green'>
[Serializable]
public enum CNContactDisplayNameOrder {
	FamilyNameFirst = 2,
	GivenNameFirst = 1,
	UserDefault = 0,
}
</pre>

### New Type Contacts.CNContactFetchRequest

<pre style='color: green'>
public class CNContactFetchRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactFetchRequest (ICNKeyDescriptor[] keysToFetch);
	protected CNContactFetchRequest (Foundation.NSArray keysToFetch);
	protected CNContactFetchRequest (Foundation.NSObjectFlag t);
	public CNContactFetchRequest (Foundation.NSString[] keysToFetch);
	public CNContactFetchRequest (ObjCRuntime.INativeObject[] keysToFetch);
	protected CNContactFetchRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSArray KeysToFetch { get; set; }
	public virtual bool MutableObjects { get; set; }
	public virtual Foundation.NSPredicate Predicate { get; set; }
	public virtual CNContactSortOrder SortOrder { get; set; }
	public virtual bool UnifyResults { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Contacts.CNContactFormatter

<pre style='color: green'>
public class CNContactFormatter : Foundation.NSFormatter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactFormatter ();
	public CNContactFormatter (Foundation.NSCoder coder);
	protected CNContactFormatter (Foundation.NSObjectFlag t);
	protected CNContactFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString ContactPropertyAttribute { get; }
	public virtual CNContactFormatterStyle Style { get; set; }
	// methods
	public virtual Foundation.NSAttributedString GetAttributedString (CNContact contact, Foundation.NSDictionary attributes);
	public static Foundation.NSAttributedString GetAttributedStringFrom (CNContact contact, CNContactFormatterStyle style, Foundation.NSDictionary attributes);
	public static string GetDelimiterFor (CNContact contact);
	public static ICNKeyDescriptor GetDescriptorForRequiredKeys (CNContactFormatterStyle style);
	public static CNContactDisplayNameOrder GetNameOrderFor (CNContact contact);
	public virtual string GetString (CNContact contact);
	public static string GetStringFrom (CNContact contact, CNContactFormatterStyle style);
}
</pre>

### New Type Contacts.CNContactFormatterStyle

<pre style='color: green'>
[Serializable]
public enum CNContactFormatterStyle {
	FullName = 0,
	PhoneticFullName = 1,
}
</pre>

### New Type Contacts.CNContactKey

<pre style='color: green'>
public static class CNContactKey {
	// properties
	public static Foundation.NSString Birthday { get; }
	public static Foundation.NSString Dates { get; }
	public static Foundation.NSString DepartmentName { get; }
	public static Foundation.NSString EmailAddresses { get; }
	public static Foundation.NSString FamilyName { get; }
	public static Foundation.NSString GivenName { get; }
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString InstantMessageAddresses { get; }
	public static Foundation.NSString JobTitle { get; }
	public static Foundation.NSString MiddleName { get; }
	public static Foundation.NSString NamePrefix { get; }
	public static Foundation.NSString NameSuffix { get; }
	public static Foundation.NSString Nickname { get; }
	public static Foundation.NSString NonGregorianBirthday { get; }
	public static Foundation.NSString Note { get; }
	public static Foundation.NSString OrganizationName { get; }
	public static Foundation.NSString PhoneNumbers { get; }
	public static Foundation.NSString PhoneticFamilyName { get; }
	public static Foundation.NSString PhoneticGivenName { get; }
	public static Foundation.NSString PhoneticMiddleName { get; }
	public static Foundation.NSString PostalAddresses { get; }
	public static Foundation.NSString PreviousFamilyName { get; }
	public static Foundation.NSString Relations { get; }
	public static Foundation.NSString SocialProfiles { get; }
	public static Foundation.NSString ThumbnailImageData { get; }
	public static Foundation.NSString Type { get; }
	public static Foundation.NSString UrlAddresses { get; }
}
</pre>

### New Type Contacts.CNContactOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum CNContactOptions {
	Birthday = 128,
	Dates = 131072,
	DepartmentName = 32,
	EmailAddresses = 32768,
	InstantMessageAddresses = 2097152,
	JobTitle = 64,
	Nickname = 1,
	None = 0,
	NonGregorianBirthday = 256,
	Note = 512,
	OrganizationName = 16,
	PhoneNumbers = 16384,
	PhoneticFamilyName = 8,
	PhoneticGivenName = 2,
	PhoneticMiddleName = 4,
	PostalAddresses = 65536,
	Relations = 524288,
	SocialProfiles = 1048576,
	ThumbnailImageData = 2048,
	Type = 8192,
	UrlAddresses = 262144,
}
</pre>

### New Type Contacts.CNContactProperty

<pre style='color: green'>
public class CNContactProperty : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactProperty ();
	public CNContactProperty (Foundation.NSCoder coder);
	protected CNContactProperty (Foundation.NSObjectFlag t);
	protected CNContactProperty (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CNContact Contact { get; }
	public virtual string Identifier { get; }
	public virtual string Key { get; }
	public virtual string Label { get; }
	public virtual Foundation.NSObject Value { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type Contacts.CNContactRelation

<pre style='color: green'>
public class CNContactRelation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactRelation ();
	public CNContactRelation (Foundation.NSCoder coder);
	protected CNContactRelation (Foundation.NSObjectFlag t);
	protected CNContactRelation (IntPtr handle);
	public CNContactRelation (string name);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CNContactRelation FromName (string name);
}
</pre>

### New Type Contacts.CNContactSortOrder

<pre style='color: green'>
[Serializable]
public enum CNContactSortOrder {
	FamilyName = 3,
	GivenName = 2,
	None = 0,
	UserDefault = 1,
}
</pre>

### New Type Contacts.CNContactStore

<pre style='color: green'>
public class CNContactStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactStore ();
	protected CNContactStore (Foundation.NSObjectFlag t);
	protected CNContactStore (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string DefaultContainerIdentifier { get; }
	public static Foundation.NSString NotificationDidChange { get; }
	// methods
	public virtual bool EnumerateContacts (CNContactFetchRequest fetchRequest, out Foundation.NSError error, CNContactStoreEnumerateContactsHandler handler);
	public virtual bool ExecuteSaveRequest (CNSaveRequest saveRequest, out Foundation.NSError error);
	public static CNAuthorizationStatus GetAuthorizationStatus (CNEntityType entityType);
	public virtual CNContainer[] GetContainers (Foundation.NSPredicate predicate, out Foundation.NSError error);
	public virtual CNGroup[] GetGroups (Foundation.NSPredicate predicate, out Foundation.NSError error);
	protected virtual CNContact GetUnifiedContact (string identifier, Foundation.NSArray keys, out Foundation.NSError error);
	public CNContact GetUnifiedContact&lt;T&gt; (string identifier, T[] keys, out Foundation.NSError error);
	protected virtual CNContact[] GetUnifiedContacts (Foundation.NSPredicate predicate, Foundation.NSArray keys, out Foundation.NSError error);
	public CNContact[] GetUnifiedContacts&lt;T&gt; (Foundation.NSPredicate predicate, T[] keys, out Foundation.NSError error);
	protected virtual Foundation.NSObject GetUnifiedMeContact (Foundation.NSArray keys, out Foundation.NSError error);
	public Foundation.NSObject GetUnifiedMeContact&lt;T&gt; (T[] keys, out Foundation.NSError error);
	public virtual void RequestAccess (CNEntityType entityType, CNContactStoreRequestAccessHandler completionHandler);
	public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RequestAccessAsync (CNEntityType entityType);

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveNotificationDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type Contacts.CNContactStoreEnumerateContactsHandler

<pre style='color: green'>
public sealed delegate CNContactStoreEnumerateContactsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreEnumerateContactsHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CNContact contact, bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CNContact contact, bool stop);
}
</pre>

### New Type Contacts.CNContactStoreRequestAccessHandler

<pre style='color: green'>
public sealed delegate CNContactStoreRequestAccessHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CNContactStoreRequestAccessHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool granted, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool granted, Foundation.NSError error);
}
</pre>

### New Type Contacts.CNContactsUserDefaults

<pre style='color: green'>
public class CNContactsUserDefaults : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactsUserDefaults ();
	protected CNContactsUserDefaults (Foundation.NSObjectFlag t);
	protected CNContactsUserDefaults (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string CountryCode { get; }
	public virtual CNContactSortOrder SortOrder { get; }
	// methods
	public static CNContactsUserDefaults GetSharedDefaults ();
}
</pre>

### New Type Contacts.CNContactType

<pre style='color: green'>
[Serializable]
public enum CNContactType {
	Organization = 1,
	Person = 0,
}
</pre>

### New Type Contacts.CNContactVCardSerialization

<pre style='color: green'>
public class CNContactVCardSerialization : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContactVCardSerialization ();
	protected CNContactVCardSerialization (Foundation.NSObjectFlag t);
	protected CNContactVCardSerialization (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static CNContact[] GetContactsFromData (Foundation.NSData data, out Foundation.NSError error);
	public static Foundation.NSData GetDataFromContacts (CNContact[] contacts, out Foundation.NSError error);
	public static ICNKeyDescriptor GetDescriptorFromRequiredKeys ();
}
</pre>

### New Type Contacts.CNContainer

<pre style='color: green'>
public class CNContainer : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNContainer ();
	public CNContainer (Foundation.NSCoder coder);
	protected CNContainer (Foundation.NSObjectFlag t);
	protected CNContainer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CNContainerType ContainerType { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type Contacts.CNContainer_PredicatesExtension

<pre style='color: green'>
public static class CNContainer_PredicatesExtension {
	// methods
	public static Foundation.NSPredicate GetPredicateForContainerOfContact (CNContainer This, string contactIdentifier);
	public static Foundation.NSPredicate GetPredicateForContainerOfGroup (CNContainer This, string groupIdentifier);
	public static Foundation.NSPredicate GetPredicateForContainers (CNContainer This, string[] identifiers);
}
</pre>

### New Type Contacts.CNContainerKey

<pre style='color: green'>
public static class CNContainerKey {
	// properties
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString Name { get; }
	public static Foundation.NSString Type { get; }
}
</pre>

### New Type Contacts.CNContainerType

<pre style='color: green'>
[Serializable]
public enum CNContainerType {
	CardDav = 3,
	Exchange = 2,
	Local = 1,
	Unassigned = 0,
}
</pre>

### New Type Contacts.CNEntityType

<pre style='color: green'>
[Serializable]
public enum CNEntityType {
	Contacts = 0,
}
</pre>

### New Type Contacts.CNErrorCode

<pre style='color: green'>
[Serializable]
public enum CNErrorCode {
	AuthorizationDenied = 100,
	CommunicationError = 1,
	ContainmentCycle = 202,
	ContainmentScope = 203,
	DataAccessError = 2,
	InsertedRecordAlreadyExists = 201,
	ParentRecordDoesNotExist = 204,
	PolicyViolation = 500,
	PredicateInvalid = 400,
	RecordDoesNotExist = 200,
	ValidationConfigurationError = 302,
	ValidationMultipleErrors = 300,
	ValidationTypeMismatch = 301,
}
</pre>

### New Type Contacts.CNErrorUserInfoKey

<pre style='color: green'>
public static class CNErrorUserInfoKey {
	// properties
	public static Foundation.NSString AffectedRecordIdentifiers { get; }
	public static Foundation.NSString AffectedRecords { get; }
	public static Foundation.NSString KeyPaths { get; }
	public static Foundation.NSString ValidationErrors { get; }
}
</pre>

### New Type Contacts.CNGroup

<pre style='color: green'>
public class CNGroup : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNGroup ();
	public CNGroup (Foundation.NSCoder coder);
	protected CNGroup (Foundation.NSObjectFlag t);
	protected CNGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNGroup_PredicatesExtension

<pre style='color: green'>
public static class CNGroup_PredicatesExtension {
	// methods
	public static Foundation.NSPredicate GetPredicateForGroups (CNGroup This, string[] identifiers);
	public static Foundation.NSPredicate GetPredicateForGroupsInContainer (CNGroup This, string containerIdentifier);
	public static Foundation.NSPredicate GetPredicateForSubgroupsInGroup (CNGroup This, string parentGroupIdentifier);
}
</pre>

### New Type Contacts.CNGroupKey

<pre style='color: green'>
public static class CNGroupKey {
	// properties
	public static Foundation.NSString Identifier { get; }
	public static Foundation.NSString Name { get; }
}
</pre>

### New Type Contacts.CNInstantMessageAddress

<pre style='color: green'>
public class CNInstantMessageAddress : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNInstantMessageAddress ();
	public CNInstantMessageAddress (Foundation.NSCoder coder);
	protected CNInstantMessageAddress (Foundation.NSObjectFlag t);
	protected CNInstantMessageAddress (IntPtr handle);
	public CNInstantMessageAddress (string username, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string Username { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNInstantMessageAddressOption property);
	public static string LocalizeProperty (Foundation.NSString propertyKey);
	public static string LocalizeService (CNInstantMessageServiceOption serviceOption);
	public static string LocalizeService (Foundation.NSString service);
}
</pre>

### New Type Contacts.CNInstantMessageAddressKey

<pre style='color: green'>
public static class CNInstantMessageAddressKey {
	// properties
	public static Foundation.NSString Service { get; }
	public static Foundation.NSString Username { get; }
}
</pre>

### New Type Contacts.CNInstantMessageAddressOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageAddressOption {
	Service = 1,
	Username = 0,
}
</pre>

### New Type Contacts.CNInstantMessageServiceKey

<pre style='color: green'>
public static class CNInstantMessageServiceKey {
	// properties
	public static Foundation.NSString Aim { get; }
	public static Foundation.NSString Facebook { get; }
	public static Foundation.NSString GaduGadu { get; }
	public static Foundation.NSString GoogleTalk { get; }
	public static Foundation.NSString Icq { get; }
	public static Foundation.NSString Jabber { get; }
	public static Foundation.NSString Msn { get; }
	public static Foundation.NSString QQ { get; }
	public static Foundation.NSString Skype { get; }
	public static Foundation.NSString Yahoo { get; }
}
</pre>

### New Type Contacts.CNInstantMessageServiceOption

<pre style='color: green'>
[Serializable]
public enum CNInstantMessageServiceOption {
	Aim = 0,
	Facebook = 1,
	GaduGadu = 2,
	GoogleTalk = 3,
	Icq = 4,
	Jabber = 5,
	Msn = 6,
	QQ = 7,
	Skype = 8,
	Yahoo = 9,
}
</pre>

### New Type Contacts.CNLabelContactRelationKey

<pre style='color: green'>
public static class CNLabelContactRelationKey {
	// properties
	public static Foundation.NSString Assistant { get; }
	public static Foundation.NSString Brother { get; }
	public static Foundation.NSString Child { get; }
	public static Foundation.NSString Father { get; }
	public static Foundation.NSString Friend { get; }
	public static Foundation.NSString Manager { get; }
	public static Foundation.NSString Mother { get; }
	public static Foundation.NSString Parent { get; }
	public static Foundation.NSString Partner { get; }
	public static Foundation.NSString Sister { get; }
	public static Foundation.NSString Spouse { get; }
}
</pre>

### New Type Contacts.CNLabeledValue`1

<pre style='color: green'>
public class CNLabeledValue`1 : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNLabeledValue`1 ();
	public CNLabeledValue`1 (Foundation.NSCoder coder);
	protected CNLabeledValue`1 (Foundation.NSObjectFlag t);
	protected CNLabeledValue`1 (IntPtr handle);
	public CNLabeledValue`1 (string label, ValueType value);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual string Label { get; }
	public virtual ValueType Value { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static ValueType FromLabel (string label, ValueType value);
	public virtual ValueType GetLabeledValue (string label);
	public virtual ValueType GetLabeledValue (ValueType value);
	public virtual ValueType GetLabeledValue (string label, ValueType value);
	public static string LocalizeLabel (Foundation.NSString labelKey);
}
</pre>

### New Type Contacts.CNLabelKey

<pre style='color: green'>
public static class CNLabelKey {
	// properties
	public static Foundation.NSString DateAnniversary { get; }
	public static Foundation.NSString EmailiCloud { get; }
	public static Foundation.NSString Home { get; }
	public static Foundation.NSString Other { get; }
	public static Foundation.NSString UrlAddressHomePage { get; }
	public static Foundation.NSString Work { get; }
}
</pre>

### New Type Contacts.CNLabelPhoneNumberKey

<pre style='color: green'>
public static class CNLabelPhoneNumberKey {
	// properties
	public static Foundation.NSString HomeFax { get; }
	public static Foundation.NSString iPhone { get; }
	public static Foundation.NSString Main { get; }
	public static Foundation.NSString Mobile { get; }
	public static Foundation.NSString OtherFax { get; }
	public static Foundation.NSString Pager { get; }
	public static Foundation.NSString WorkFax { get; }
}
</pre>

### New Type Contacts.CNMutableContact

<pre style='color: green'>
public class CNMutableContact : Contacts.CNContact, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNMutableContact ();
	public CNMutableContact (Foundation.NSCoder coder);
	protected CNMutableContact (Foundation.NSObjectFlag t);
	protected CNMutableContact (IntPtr handle);
	// properties
	public virtual Foundation.NSDateComponents Birthday { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Contacts.CNLabeledValue&lt;CNContactRelation&gt;[] ContactRelations { get; set; }
	public virtual CNContactType ContactType { get; set; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSDateComponents&gt;[] Dates { get; set; }
	public virtual string DepartmentName { get; set; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSString&gt;[] EmailAddresses { get; set; }
	public virtual string FamilyName { get; set; }
	public virtual string GivenName { get; set; }
	public virtual Foundation.NSData ImageData { get; set; }
	public virtual Contacts.CNLabeledValue&lt;CNInstantMessageAddress&gt;[] InstantMessageAddresses { get; set; }
	public virtual string JobTitle { get; set; }
	public virtual string MiddleName { get; set; }
	public virtual string NamePrefix { get; set; }
	public virtual string NameSuffix { get; set; }
	public virtual string Nickname { get; set; }
	public virtual Foundation.NSDateComponents NonGregorianBirthday { get; set; }
	public virtual string Note { get; set; }
	public virtual string OrganizationName { get; set; }
	public virtual Contacts.CNLabeledValue&lt;CNPhoneNumber&gt;[] PhoneNumbers { get; set; }
	public virtual string PhoneticFamilyName { get; set; }
	public virtual string PhoneticGivenName { get; set; }
	public virtual string PhoneticMiddleName { get; set; }
	public virtual Contacts.CNLabeledValue&lt;CNPostalAddress&gt;[] PostalAddresses { get; set; }
	public virtual string PreviousFamilyName { get; set; }
	public virtual Contacts.CNLabeledValue&lt;CNSocialProfile&gt;[] SocialProfiles { get; set; }
	public virtual Contacts.CNLabeledValue&lt;Foundation.NSString&gt;[] UrlAddresses { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Contacts.CNMutableGroup

<pre style='color: green'>
public class CNMutableGroup : Contacts.CNGroup, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNMutableGroup ();
	public CNMutableGroup (Foundation.NSCoder coder);
	protected CNMutableGroup (Foundation.NSObjectFlag t);
	protected CNMutableGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
}
</pre>

### New Type Contacts.CNMutablePostalAddress

<pre style='color: green'>
public class CNMutablePostalAddress : Contacts.CNPostalAddress, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNMutablePostalAddress ();
	public CNMutablePostalAddress (Foundation.NSCoder coder);
	protected CNMutablePostalAddress (Foundation.NSObjectFlag t);
	protected CNMutablePostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; set; }
	public virtual string IsoCountryCode { get; set; }
	public virtual string PostalCode { get; set; }
	public virtual string State { get; set; }
	public virtual string Street { get; set; }
}
</pre>

### New Type Contacts.CNPhoneNumber

<pre style='color: green'>
public class CNPhoneNumber : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNPhoneNumber (Foundation.NSCoder coder);
	protected CNPhoneNumber (Foundation.NSObjectFlag t);
	protected CNPhoneNumber (IntPtr handle);
	public CNPhoneNumber (string stringValue);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string StringValue { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CNPhoneNumber PhoneNumberWithStringValue (string stringValue);
}
</pre>

### New Type Contacts.CNPostalAddress

<pre style='color: green'>
public class CNPostalAddress : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNPostalAddress ();
	public CNPostalAddress (Foundation.NSCoder coder);
	protected CNPostalAddress (Foundation.NSObjectFlag t);
	protected CNPostalAddress (IntPtr handle);
	// properties
	public virtual string City { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string Country { get; }
	public virtual string IsoCountryCode { get; }
	public virtual string PostalCode { get; }
	public virtual string State { get; }
	public virtual string Street { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNPostalAddressKeyOption option);
	public static string LocalizeProperty (Foundation.NSString property);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
</pre>

### New Type Contacts.CNPostalAddressFormatter

<pre style='color: green'>
public class CNPostalAddressFormatter : Foundation.NSFormatter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNPostalAddressFormatter ();
	public CNPostalAddressFormatter (Foundation.NSCoder coder);
	protected CNPostalAddressFormatter (Foundation.NSObjectFlag t);
	protected CNPostalAddressFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString LocalizedPropertyNameAttribute { get; }
	public static Foundation.NSString PropertyAttribute { get; }
	public virtual CNPostalAddressFormatterStyle Style { get; set; }
	// methods
	public static Foundation.NSAttributedString GetAttributedStringFrom (CNPostalAddress postalAddress, CNPostalAddressFormatterStyle style, Foundation.NSDictionary attributes);
	public virtual Foundation.NSAttributedString GetAttributedStringFromPostalAddress (CNPostalAddress postalAddress, Foundation.NSDictionary attributes);
	public static string GetStringFrom (CNPostalAddress postalAddress, CNPostalAddressFormatterStyle style);
	public virtual string GetStringFromPostalAddress (CNPostalAddress postalAddress);
}
</pre>

### New Type Contacts.CNPostalAddressFormatterStyle

<pre style='color: green'>
[Serializable]
public enum CNPostalAddressFormatterStyle {
	MailingAddress = 0,
}
</pre>

### New Type Contacts.CNPostalAddressKey

<pre style='color: green'>
public static class CNPostalAddressKey {
	// properties
	public static Foundation.NSString City { get; }
	public static Foundation.NSString Country { get; }
	public static Foundation.NSString IsoCountryCode { get; }
	public static Foundation.NSString PostalCode { get; }
	public static Foundation.NSString State { get; }
	public static Foundation.NSString Street { get; }
}
</pre>

### New Type Contacts.CNPostalAddressKeyOption

<pre style='color: green'>
[Serializable]
public enum CNPostalAddressKeyOption {
	City = 1,
	Country = 4,
	IsoCountryCode = 5,
	PostalCode = 3,
	State = 2,
	Street = 0,
}
</pre>

### New Type Contacts.CNSaveRequest

<pre style='color: green'>
public class CNSaveRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNSaveRequest ();
	protected CNSaveRequest (Foundation.NSObjectFlag t);
	protected CNSaveRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddContact (CNMutableContact contact, string identifier);
	public virtual void AddGroup (CNMutableGroup group, string identifier);
	public virtual void AddMember (CNContact contact, CNGroup group);
	public virtual void AddSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void DeleteContact (CNMutableContact contact);
	public virtual void DeleteGroup (CNMutableGroup group);
	public virtual void RemoveMember (CNContact contact, CNGroup group);
	public virtual void RemoveSubgroup (CNGroup subgroup, CNGroup group);
	public virtual void UpdateContact (CNMutableContact contact);
	public virtual void UpdateGroup (CNMutableGroup group);
}
</pre>

### New Type Contacts.CNSocialProfile

<pre style='color: green'>
public class CNSocialProfile : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CNSocialProfile ();
	public CNSocialProfile (Foundation.NSCoder coder);
	protected CNSocialProfile (Foundation.NSObjectFlag t);
	protected CNSocialProfile (IntPtr handle);
	public CNSocialProfile (string url, string username, string userIdentifier, string service);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Service { get; }
	public virtual string UrlString { get; }
	public virtual string UserIdentifier { get; }
	public virtual string Username { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static string LocalizeProperty (CNSocialProfileOption option);
	public static string LocalizeProperty (Foundation.NSString key);
	public static string LocalizeService (CNSocialProfileServiceOption serviceOption);
	public static string LocalizeService (Foundation.NSString service);
}
</pre>

### New Type Contacts.CNSocialProfileKey

<pre style='color: green'>
public static class CNSocialProfileKey {
	// properties
	public static Foundation.NSString Service { get; }
	public static Foundation.NSString UrlString { get; }
	public static Foundation.NSString UserIdentifier { get; }
	public static Foundation.NSString Username { get; }
}
</pre>

### New Type Contacts.CNSocialProfileOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileOption {
	Service = 3,
	UrlString = 0,
	UserIdentifier = 2,
	Username = 1,
}
</pre>

### New Type Contacts.CNSocialProfileServiceKey

<pre style='color: green'>
public static class CNSocialProfileServiceKey {
	// properties
	public static Foundation.NSString Facebook { get; }
	public static Foundation.NSString Flickr { get; }
	public static Foundation.NSString GameCenter { get; }
	public static Foundation.NSString LinkedIn { get; }
	public static Foundation.NSString MySpace { get; }
	public static Foundation.NSString SinaWeibo { get; }
	public static Foundation.NSString TencentWeibo { get; }
	public static Foundation.NSString Twitter { get; }
	public static Foundation.NSString Yelp { get; }
}
</pre>

### New Type Contacts.CNSocialProfileServiceOption

<pre style='color: green'>
[Serializable]
public enum CNSocialProfileServiceOption {
	Facebook = 0,
	Flickr = 1,
	GameCenter = 8,
	LinkedIn = 2,
	MySpace = 3,
	SinaWeibo = 4,
	TencentWeibo = 5,
	Twitter = 6,
	Yelp = 7,
}
</pre>

### New Type Contacts.ICNKeyDescriptor

<pre style='color: green'>
public interface ICNKeyDescriptor : Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## New Namespace CoreAudioKit

### New Type CoreAudioKit.AUViewController

<pre style='color: green'>
public class AUViewController : AppKit.NSViewController, AppKit.INSSeguePerforming, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AUViewController ();
	public AUViewController (Foundation.NSCoder coder);
	protected AUViewController (Foundation.NSObjectFlag t);
	protected AUViewController (IntPtr handle);
	public AUViewController (string nibName, Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void BeginRequestWithExtensionContext (Foundation.NSExtensionContext context);
}
</pre>

## New Namespace GameplayKit

### New Type GameplayKit.GKAgent

<pre style='color: green'>
public class GKAgent : GameplayKit.GKComponent, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKAgent ();
	protected GKAgent (Foundation.NSObjectFlag t);
	protected GKAgent (IntPtr handle);
	// properties
	public virtual GKBehavior Behavior { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual IGKAgentDelegate Delegate { get; set; }
	public virtual float Mass { get; set; }
	public virtual float MaxAcceleration { get; set; }
	public virtual float MaxSpeed { get; set; }
	public virtual float Radius { get; set; }
	public virtual float Speed { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type GameplayKit.GKAgent2D

<pre style='color: green'>
public class GKAgent2D : GameplayKit.GKAgent, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKAgent2D ();
	protected GKAgent2D (Foundation.NSObjectFlag t);
	protected GKAgent2D (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 Position { get; set; }
	public virtual float Rotation { get; set; }
	public virtual OpenTK.Vector2 Velocity { get; }
	// methods
	public virtual void Update (double seconds);
}
</pre>

### New Type GameplayKit.GKAgentDelegate

<pre style='color: green'>
public class GKAgentDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IGKAgentDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKAgentDelegate ();
	protected GKAgentDelegate (Foundation.NSObjectFlag t);
	protected GKAgentDelegate (IntPtr handle);
	// methods
	public virtual void AgentDidUpdate (GKAgent agent);
	public virtual void AgentWillUpdate (GKAgent agent);
}
</pre>

### New Type GameplayKit.GKAgentDelegate_Extensions

<pre style='color: green'>
public static class GKAgentDelegate_Extensions {
	// methods
	public static void AgentDidUpdate (IGKAgentDelegate This, GKAgent agent);
	public static void AgentWillUpdate (IGKAgentDelegate This, GKAgent agent);
}
</pre>

### New Type GameplayKit.GKARC4RandomSource

<pre style='color: green'>
public class GKARC4RandomSource : GameplayKit.GKRandomSource, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKARC4RandomSource ();
	public GKARC4RandomSource (Foundation.NSCoder coder);
	public GKARC4RandomSource (Foundation.NSData seed);
	protected GKARC4RandomSource (Foundation.NSObjectFlag t);
	protected GKARC4RandomSource (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSData Seed { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void DropValues (uint count);
}
</pre>

### New Type GameplayKit.GKBehavior

<pre style='color: green'>
public class GKBehavior : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKBehavior ();
	protected GKBehavior (Foundation.NSObjectFlag t);
	protected GKBehavior (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint GoalCount { get; }
	public GKGoal Item { get; }
	public Foundation.NSNumber Item { get; set; }
	// methods
	public static GKBehavior FromGoal (GKGoal goal, float weight);
	public static GKBehavior FromGoals (Foundation.NSDictionary&lt;GKGoal,Foundation.NSNumber&gt; weightedGoals);
	public static GKBehavior FromGoals (GKGoal[] goals);
	public static GKBehavior FromGoals (GKGoal[] goals, Foundation.NSNumber[] weights);
	public virtual float GetWeight (GKGoal goal);
	public virtual void RemoveAllGoals ();
	public virtual void RemoveGoal (GKGoal goal);
	public virtual void SetWeight (float weight, GKGoal goal);
}
</pre>

### New Type GameplayKit.GKCircleObstacle

<pre style='color: green'>
public class GKCircleObstacle : GameplayKit.GKObstacle, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKCircleObstacle (Foundation.NSObjectFlag t);
	protected GKCircleObstacle (IntPtr handle);
	public GKCircleObstacle (float radius);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 Position { get; set; }
	public virtual float Radius { get; set; }
	// methods
	public static GKCircleObstacle FromRadius (float radius);
}
</pre>

### New Type GameplayKit.GKComponent

<pre style='color: green'>
public abstract class GKComponent : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKComponent ();
	protected GKComponent (Foundation.NSObjectFlag t);
	protected GKComponent (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKEntity Entity { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Update (double seconds);
}
</pre>

### New Type GameplayKit.GKComponentSystem`1

<pre style='color: green'>
public class GKComponentSystem`1 : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKComponentSystem`1 ();
	protected GKComponentSystem`1 (Foundation.NSObjectFlag t);
	public GKComponentSystem`1 (ObjCRuntime.Class cls);
	protected GKComponentSystem`1 (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ObjCRuntime.Class ComponentClass { get; }
	public virtual TComponent[] Components { get; }
	public System.Type ComponentType { get; }
	public TComponent Item { get; }
	// methods
	public virtual void AddComponent (GKEntity entity);
	public virtual void AddComponent (TComponent component);
	public virtual void RemoveComponent (GKEntity entity);
	public virtual void RemoveComponent (TComponent component);
	public virtual void Update (double seconds);
}
</pre>

### New Type GameplayKit.GKEntity

<pre style='color: green'>
public class GKEntity : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKEntity ();
	protected GKEntity (Foundation.NSObjectFlag t);
	protected GKEntity (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKComponent[] Components { get; }
	// methods
	public virtual void AddComponent (GKComponent component);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	protected virtual GKComponent GetComponent (ObjCRuntime.Class componentClass);
	public GKComponent GetComponent (System.Type componentType);
	public static GKEntity GetEntity ();
	protected virtual void RemoveComponent (ObjCRuntime.Class componentClass);
	public void RemoveComponent (System.Type componentType);
	public virtual void Update (double seconds);
}
</pre>

### New Type GameplayKit.GKGameModel

<pre style='color: green'>
public class GKGameModel {
	// constructors
	public GKGameModel ();
	// fields
	public static const int MaxScore;
	public static const int MinScore;
}
</pre>

### New Type GameplayKit.GKGameModel_Extensions

<pre style='color: green'>
public static class GKGameModel_Extensions {
	// methods
	public static nint GetScore (IGKGameModel This, IGKGameModelPlayer player);
	public static bool IsLoss (IGKGameModel This, IGKGameModelPlayer player);
	public static bool IsWin (IGKGameModel This, IGKGameModelPlayer player);
}
</pre>

### New Type GameplayKit.GKGameModelPlayer_Extensions

<pre style='color: green'>
public static class GKGameModelPlayer_Extensions {
	// methods
	public static nint GetPlayerId (IGKGameModelPlayer This);
}
</pre>

### New Type GameplayKit.GKGaussianDistribution

<pre style='color: green'>
public class GKGaussianDistribution : GameplayKit.GKRandomDistribution, Foundation.INSObjectProtocol, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKGaussianDistribution (Foundation.NSObjectFlag t);
	protected GKGaussianDistribution (IntPtr handle);
	public GKGaussianDistribution (IGKRandom source, nint lowestInclusive, nint highestInclusive);
	public GKGaussianDistribution (IGKRandom source, float mean, float deviation);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual float Deviation { get; }
	public virtual float Mean { get; }
}
</pre>

### New Type GameplayKit.GKGoal

<pre style='color: green'>
public class GKGoal : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKGoal ();
	protected GKGoal (Foundation.NSObjectFlag t);
	protected GKGoal (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static GKGoal GetGoalToAlign (GKAgent[] agents, float maxDistance, float maxAngle);
	public static GKGoal GetGoalToAvoidAgents (GKAgent[] agents, double maxPredictionTime);
	public static GKGoal GetGoalToAvoidObstacles (GKObstacle[] obstacles, double maxPredictionTime);
	public static GKGoal GetGoalToCohere (GKAgent[] agents, float maxDistance, float maxAngle);
	public static GKGoal GetGoalToFleeAgent (GKAgent agent);
	public static GKGoal GetGoalToFollowPath (GKPath path, double maxPredictionTime, bool forward);
	public static GKGoal GetGoalToInterceptAgent (GKAgent target, double maxPredictionTime);
	public static GKGoal GetGoalToReachTargetSpeed (float targetSpeed);
	public static GKGoal GetGoalToSeekAgent (GKAgent agent);
	public static GKGoal GetGoalToSeparate (GKAgent[] agents, float maxDistance, float maxAngle);
	public static GKGoal GetGoalToStayOnPath (GKPath path, double maxPredictionTime);
	public static GKGoal GetGoalToWander (float speed);
}
</pre>

### New Type GameplayKit.GKGraph

<pre style='color: green'>
public class GKGraph : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKGraph ();
	protected GKGraph (Foundation.NSObjectFlag t);
	public GKGraph (GKGraphNode[] nodes);
	protected GKGraph (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKGraphNode[] Nodes { get; }
	// methods
	public virtual void AddNodes (GKGraphNode[] nodes);
	public virtual void ConnectNodeToLowestCostNode (GKGraphNode node, bool bidirectional);
	protected override void Dispose (bool disposing);
	public virtual GKGraphNode[] FindPath (GKGraphNode startNode, GKGraphNode endNode);
	public static GKGraph FromNodes (GKGraphNode[] nodes);
	public virtual void RemoveNodes (GKGraphNode[] nodes);
}
</pre>

### New Type GameplayKit.GKGraphNode

<pre style='color: green'>
public class GKGraphNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKGraphNode ();
	protected GKGraphNode (Foundation.NSObjectFlag t);
	protected GKGraphNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKGraphNode[] ConnectedNodes { get; }
	// methods
	public virtual void AddConnections (GKGraphNode[] nodes, bool bidirectional);
	protected override void Dispose (bool disposing);
	public virtual GKGraphNode[] FindPathFrom (GKGraphNode startNode);
	public virtual GKGraphNode[] FindPathTo (GKGraphNode goalNode);
	public virtual float GetCost (GKGraphNode node);
	public virtual float GetEstimatedCost (GKGraphNode node);
	public virtual void RemoveConnections (GKGraphNode[] nodes, bool bidirectional);
}
</pre>

### New Type GameplayKit.GKGraphNode2D

<pre style='color: green'>
public class GKGraphNode2D : GameplayKit.GKGraphNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKGraphNode2D (Foundation.NSObjectFlag t);
	public GKGraphNode2D (OpenTK.Vector2 point);
	protected GKGraphNode2D (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 Position { get; set; }
	// methods
	public static GKGraphNode2D FromPoint (OpenTK.Vector2 point);
}
</pre>

### New Type GameplayKit.GKGridGraph

<pre style='color: green'>
public class GKGridGraph : GameplayKit.GKGraph, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKGridGraph ();
	protected GKGridGraph (Foundation.NSObjectFlag t);
	protected GKGridGraph (IntPtr handle);
	public GKGridGraph (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool DiagonalsAllowed { get; }
	public virtual uint GridHeight { get; }
	public virtual OpenTK.Vector2i GridOrigin { get; }
	public virtual uint GridWidth { get; }
	// methods
	public virtual void ConnectNodeToAdjacentNodes (GKGridGraphNode node);
	public static GKGridGraph FromGridStartingAt (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed);
	public virtual GKGridGraphNode GetNodeAt (OpenTK.Vector2i position);
}
</pre>

### New Type GameplayKit.GKGridGraphNode

<pre style='color: green'>
public class GKGridGraphNode : GameplayKit.GKGraphNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKGridGraphNode (Foundation.NSObjectFlag t);
	public GKGridGraphNode (OpenTK.Vector2i gridPosition);
	protected GKGridGraphNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2i GridPosition { get; set; }
	// methods
	public static GKGridGraphNode FromGridPosition (OpenTK.Vector2i gridPosition);
}
</pre>

### New Type GameplayKit.GKLinearCongruentialRandomSource

<pre style='color: green'>
public class GKLinearCongruentialRandomSource : GameplayKit.GKRandomSource, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKLinearCongruentialRandomSource ();
	public GKLinearCongruentialRandomSource (Foundation.NSCoder coder);
	protected GKLinearCongruentialRandomSource (Foundation.NSObjectFlag t);
	protected GKLinearCongruentialRandomSource (IntPtr handle);
	public GKLinearCongruentialRandomSource (ulong seed);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ulong Seed { get; set; }
}
</pre>

### New Type GameplayKit.GKMersenneTwisterRandomSource

<pre style='color: green'>
public class GKMersenneTwisterRandomSource : GameplayKit.GKRandomSource, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKMersenneTwisterRandomSource ();
	public GKMersenneTwisterRandomSource (Foundation.NSCoder coder);
	protected GKMersenneTwisterRandomSource (Foundation.NSObjectFlag t);
	protected GKMersenneTwisterRandomSource (IntPtr handle);
	public GKMersenneTwisterRandomSource (ulong seed);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual ulong Seed { get; set; }
}
</pre>

### New Type GameplayKit.GKMinMaxStrategist

<pre style='color: green'>
public class GKMinMaxStrategist : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKMinMaxStrategist ();
	protected GKMinMaxStrategist (Foundation.NSObjectFlag t);
	protected GKMinMaxStrategist (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IGKGameModel GameModel { get; set; }
	public virtual nint MaxLookAheadDepth { get; set; }
	public virtual IGKRandom RandomSource { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual IGKGameModelUpdate GetBestMove (IGKGameModelPlayer player);
	public virtual IGKGameModelUpdate GetRandomMove (IGKGameModelPlayer player, nint numMovesToConsider);
}
</pre>

### New Type GameplayKit.GKNSPredicateRule

<pre style='color: green'>
public class GKNSPredicateRule : GameplayKit.GKRule, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKNSPredicateRule ();
	protected GKNSPredicateRule (Foundation.NSObjectFlag t);
	public GKNSPredicateRule (Foundation.NSPredicate predicate);
	protected GKNSPredicateRule (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSPredicate Predicate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool EvaluatePredicate (GKRuleSystem system);
}
</pre>

### New Type GameplayKit.GKObstacle

<pre style='color: green'>
public abstract class GKObstacle : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKObstacle ();
	protected GKObstacle (Foundation.NSObjectFlag t);
	protected GKObstacle (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type GameplayKit.GKObstacleGraph

<pre style='color: green'>
public class GKObstacleGraph : GameplayKit.GKGraph, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKObstacleGraph ();
	protected GKObstacleGraph (Foundation.NSObjectFlag t);
	protected GKObstacleGraph (IntPtr handle);
	public GKObstacleGraph (GKPolygonObstacle[] obstacles, float bufferRadius);
	// properties
	public virtual float BufferRadius { get; }
	public override IntPtr ClassHandle { get; }
	public virtual GKPolygonObstacle[] Obstacles { get; }
	// methods
	public virtual void AddObstacles (GKPolygonObstacle[] obstacles);
	public virtual void ConnectNodeUsingObstacles (GKGraphNode2D node);
	public virtual void ConnectNodeUsingObstacles (GKGraphNode2D node, GKPolygonObstacle[] obstaclesToIgnore);
	public virtual void ConnectNodeUsingObstaclesIgnoringBufferRadius (GKGraphNode2D node, GKPolygonObstacle[] obstaclesBufferRadiusToIgnore);
	protected override void Dispose (bool disposing);
	public static GKObstacleGraph FromObstacles (GKPolygonObstacle[] obstacles, float bufferRadius);
	public virtual GKGraphNode2D[] GetNodes (GKPolygonObstacle obstacle);
	public virtual bool IsConnectionLocked (GKGraphNode2D startNode, GKGraphNode2D endNode);
	public virtual void LockConnection (GKGraphNode2D startNode, GKGraphNode2D endNode);
	public virtual void RemoveAllObstacles ();
	public virtual void RemoveObstacles (GKPolygonObstacle[] obstacles);
	public virtual void UnlockConnection (GKGraphNode2D startNode, GKGraphNode2D endNode);
}
</pre>

### New Type GameplayKit.GKPath

<pre style='color: green'>
public class GKPath : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKPath (Foundation.NSObjectFlag t);
	protected GKPath (IntPtr handle);
	public GKPath (GKGraphNode2D[] graphNodes, float radius);
	public GKPath (OpenTK.Vector2[] points, float radius, bool cyclical);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Cyclical { get; set; }
	public virtual uint NumPoints { get; }
	public virtual float Radius { get; set; }
	// methods
	public static GKPath FromGraphNodes (GKGraphNode2D[] graphNodes, float radius);
	public static GKPath FromPoints (OpenTK.Vector2[] points, float radius, bool cyclical);
	public virtual OpenTK.Vector2 GetPoint (uint index);
}
</pre>

### New Type GameplayKit.GKPolygonObstacle

<pre style='color: green'>
public class GKPolygonObstacle : GameplayKit.GKObstacle, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKPolygonObstacle (Foundation.NSObjectFlag t);
	public GKPolygonObstacle (OpenTK.Vector2[] points);
	protected GKPolygonObstacle (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint VertexCount { get; }
	// methods
	public static GKPolygonObstacle FromPoints (OpenTK.Vector2[] points);
	public virtual OpenTK.Vector2 GetVertex (uint index);
}
</pre>

### New Type GameplayKit.GKRandomDistribution

<pre style='color: green'>
public class GKRandomDistribution : Foundation.NSObject, Foundation.INSObjectProtocol, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKRandomDistribution (Foundation.NSObjectFlag t);
	protected GKRandomDistribution (IntPtr handle);
	public GKRandomDistribution (IGKRandom source, nint lowestInclusive, nint highestInclusive);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint HighestValue { get; }
	public virtual nint LowestValue { get; }
	public virtual uint NumberOfPossibleOutcomes { get; }
	// methods
	public static GKRandomDistribution GetD20 ();
	public static GKRandomDistribution GetD6 ();
	public static GKRandomDistribution GetDie (nint sideCount);
	public static GKRandomDistribution GetDistributionBetween (nint lowestInclusive, nint highestInclusive);
	public virtual bool GetNextBool ();
	public virtual nint GetNextInt ();
	public virtual uint GetNextInt (uint upperBound);
	public virtual float GetNextUniform ();
}
</pre>

### New Type GameplayKit.GKRandomSource

<pre style='color: green'>
public class GKRandomSource : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKRandomSource ();
	public GKRandomSource (Foundation.NSCoder coder);
	protected GKRandomSource (Foundation.NSObjectFlag t);
	protected GKRandomSource (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static GKRandomSource SharedRandom { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool GetNextBool ();
	public virtual nint GetNextInt ();
	public virtual uint GetNextInt (uint upperBound);
	public virtual float GetNextUniform ();
	public virtual Foundation.NSObject[] ShuffleObjects (Foundation.NSObject[] array);
}
</pre>

### New Type GameplayKit.GKRule

<pre style='color: green'>
public class GKRule : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKRule ();
	protected GKRule (Foundation.NSObjectFlag t);
	protected GKRule (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint Salience { get; set; }
	// methods
	public virtual bool EvaluatePredicate (GKRuleSystem system);
	public static GKRule FromPredicate (System.Func&lt;GKRuleSystem,System.Boolean&gt; predicate, System.Action&lt;GKRuleSystem&gt; action);
	public static GKRule FromPredicateAssertingFact (Foundation.NSPredicate predicate, Foundation.NSObject fact, float grade);
	public static GKRule FromPredicateRetractingFact (Foundation.NSPredicate predicate, Foundation.NSObject fact, float grade);
	public virtual void PerformAction (GKRuleSystem system);
}
</pre>

### New Type GameplayKit.GKRuleSystem

<pre style='color: green'>
public class GKRuleSystem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public GKRuleSystem ();
	protected GKRuleSystem (Foundation.NSObjectFlag t);
	protected GKRuleSystem (IntPtr handle);
	// properties
	public virtual GKRule[] Agenda { get; }
	public override IntPtr ClassHandle { get; }
	public virtual GKRule[] Executed { get; }
	public virtual Foundation.NSObject[] Facts { get; }
	public virtual GKRule[] Rules { get; }
	public virtual Foundation.NSMutableDictionary State { get; }
	// methods
	public virtual void AddRule (GKRule rule);
	public virtual void AddRules (GKRule[] rules);
	public virtual void AssertFact (Foundation.NSObject fact);
	public virtual void AssertFact (Foundation.NSObject fact, float grade);
	protected override void Dispose (bool disposing);
	public virtual void Evaluate ();
	public virtual float GetGrade (Foundation.NSObject fact);
	public virtual float GetMaximumGrade (Foundation.NSObject[] facts);
	public virtual float GetMinimumGrade (Foundation.NSObject[] facts);
	public virtual void RemoveAllRules ();
	public virtual void Reset ();
	public virtual void RetractFact (Foundation.NSObject fact);
	public virtual void RetractFact (Foundation.NSObject fact, float grade);
}
</pre>

### New Type GameplayKit.GKShuffledDistribution

<pre style='color: green'>
public class GKShuffledDistribution : GameplayKit.GKRandomDistribution, Foundation.INSObjectProtocol, IGKRandom, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKShuffledDistribution (Foundation.NSObjectFlag t);
	protected GKShuffledDistribution (IntPtr handle);
	public GKShuffledDistribution (IGKRandom source, nint lowestInclusive, nint highestInclusive);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type GameplayKit.GKState

<pre style='color: green'>
public abstract class GKState : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKState ();
	protected GKState (Foundation.NSObjectFlag t);
	protected GKState (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKStateMachine StateMachine { get; }
	// methods
	public virtual void DidEnter (GKState previousState);
	protected override void Dispose (bool disposing);
	public static GKState GetState ();
	public bool IsValidNextState (GKState state);
	public virtual bool IsValidNextState (ObjCRuntime.Class stateClass);
	public bool IsValidNextState (System.Type stateType);
	public virtual void Update (double seconds);
	public virtual void WillExit (GKState nextState);
}
</pre>

### New Type GameplayKit.GKStateMachine

<pre style='color: green'>
public class GKStateMachine : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected GKStateMachine (Foundation.NSObjectFlag t);
	public GKStateMachine (GKState[] states);
	protected GKStateMachine (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual GKState CurrentState { get; }
	// methods
	public bool CanEnterState (GKState state);
	protected virtual bool CanEnterState (ObjCRuntime.Class stateClass);
	public bool CanEnterState (System.Type stateType);
	protected override void Dispose (bool disposing);
	public virtual bool EnterState (GKState state);
	protected virtual bool EnterState (ObjCRuntime.Class stateClass);
	public virtual bool EnterState (System.Type stateType);
	public static GKStateMachine FromStates (GKState[] states);
	public GKState GetState (GKState state);
	protected virtual GKState GetState (ObjCRuntime.Class stateClass);
	public GKState GetState (System.Type stateType);
	public virtual void Update (double seconds);
}
</pre>

### New Type GameplayKit.IGKAgentDelegate

<pre style='color: green'>
public interface IGKAgentDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type GameplayKit.IGKGameModel

<pre style='color: green'>
public interface IGKGameModel : Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ApplyGameModelUpdate (IGKGameModelUpdate gameModelUpdate);
	public virtual IGKGameModelPlayer GetActivePlayer ();
	public virtual IGKGameModelUpdate[] GetGameModelUpdates (IGKGameModelPlayer player);
	public virtual IGKGameModelPlayer[] GetPlayers ();
	public virtual void SetGameModel (IGKGameModel gameModel);
}
</pre>

### New Type GameplayKit.IGKGameModelPlayer

<pre style='color: green'>
public interface IGKGameModelPlayer : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type GameplayKit.IGKGameModelUpdate

<pre style='color: green'>
public interface IGKGameModelUpdate : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual nint Value { get; set; }
}
</pre>

### New Type GameplayKit.IGKRandom

<pre style='color: green'>
public interface IGKRandom : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual bool GetNextBool ();
	public virtual nint GetNextInt ();
	public virtual uint GetNextInt (uint upperBound);
	public virtual float GetNextUniform ();
}
</pre>

## New Namespace MediaToolbox

### New Type MediaToolbox.MTFormatNames

<pre style='color: green'>
public static class MTFormatNames {
	// methods
	public static string GetLocalizedName (CoreMedia.CMMediaType mediaType);
	public static string GetLocalizedName (CoreMedia.CMMediaType mediaType, uint mediaSubType);
}
</pre>

## New Namespace Metal

### New Type Metal.IMTLBlitCommandEncoder

<pre style='color: green'>
public interface IMTLBlitCommandEncoder : IMTLCommandEncoder, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, IMTLBuffer destinationBuffer, uint destinationOffset, uint size);
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceBytesPerRow, uint sourceBytesPerImage, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinatinBytesPerRow, uint destinationBytesPerImage);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void FillBuffer (IMTLBuffer buffer, Foundation.NSRange range, byte value);
	public virtual void GenerateMipmapsForTexture (IMTLTexture texture);
	public virtual void Synchronize (IMTLResource resource);
	public virtual void Synchronize (IMTLTexture texture, uint slice, uint level);
}
</pre>

### New Type Metal.IMTLBuffer

<pre style='color: green'>
public interface IMTLBuffer : IMTLResource, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IntPtr Contents { get; }
	public virtual uint Length { get; }
	// methods
	public virtual void DidModify (Foundation.NSRange range);
}
</pre>

### New Type Metal.IMTLCommandBuffer

<pre style='color: green'>
public interface IMTLCommandBuffer : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLBlitCommandEncoder BlitCommandEncoder { get; }
	public virtual IMTLCommandQueue CommandQueue { get; }
	public virtual IMTLComputeCommandEncoder ComputeCommandEncoder { get; }
	public virtual IMTLDevice Device { get; }
	public virtual Foundation.NSError Error { get; }
	public virtual string Label { get; set; }
	public virtual bool RetainedReferences { get; }
	public virtual MTLCommandBufferStatus Status { get; }
	// methods
	public virtual void AddCompletedHandler (System.Action&lt;IMTLCommandBuffer&gt; block);
	public virtual void AddScheduledHandler (System.Action&lt;IMTLCommandBuffer&gt; block);
	public virtual void Commit ();
	public virtual IMTLParallelRenderCommandEncoder CreateParallelRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual void Enqueue ();
	public virtual void PresentDrawable (IMTLDrawable drawable);
	public virtual void PresentDrawable (IMTLDrawable drawable, double presentationTime);
	public virtual void WaitUntilCompleted ();
	public virtual void WaitUntilScheduled ();
}
</pre>

### New Type Metal.IMTLCommandEncoder

<pre style='color: green'>
public interface IMTLCommandEncoder : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual void EndEncoding ();
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
}
</pre>

### New Type Metal.IMTLCommandQueue

<pre style='color: green'>
public interface IMTLCommandQueue : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLCommandBuffer CommandBuffer ();
	public virtual IMTLCommandBuffer CommandBufferWithUnretainedReferences ();
	public virtual void InsertDebugCaptureBoundary ();
}
</pre>

### New Type Metal.IMTLComputeCommandEncoder

<pre style='color: green'>
public interface IMTLComputeCommandEncoder : IMTLCommandEncoder, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
	public virtual void SetBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetBufferOffset (uint offset, uint index);
	public virtual void SetBuffers (IMTLBuffer[] buffers, IntPtr offsets, Foundation.NSRange range);
	public virtual void SetBytes (IntPtr bytes, uint length, uint index);
	public virtual void SetComputePipelineState (IMTLComputePipelineState state);
	public virtual void SetSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, Foundation.NSRange range);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, IntPtr floatArrayPtrLodMinClamps, IntPtr floatArrayPtrLodMaxClamps, Foundation.NSRange range);
	public virtual void SetTexture (IMTLTexture texture, uint index);
	public virtual void SetTextures (IMTLTexture[] textures, Foundation.NSRange range);
	public virtual void SetThreadgroupMemoryLength (uint length, uint index);
}
</pre>

### New Type Metal.IMTLComputePipelineState

<pre style='color: green'>
public interface IMTLComputePipelineState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual uint MaxTotalThreadsPerThreadgroup { get; }
	public virtual uint ThreadExecutionWidth { get; }
}
</pre>

### New Type Metal.IMTLDepthStencilState

<pre style='color: green'>
public interface IMTLDepthStencilState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
</pre>

### New Type Metal.IMTLDevice

<pre style='color: green'>
public interface IMTLDevice : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual string Name { get; }
	// methods
	public virtual IMTLBuffer CreateBuffer (uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBuffer (IntPtr pointer, uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBufferNoCopy (IntPtr pointer, uint length, MTLResourceOptions options, MTLDeallocator deallocator);
	public virtual IMTLCommandQueue CreateCommandQueue ();
	public virtual IMTLCommandQueue CreateCommandQueue (uint maxCommandBufferCount);
	public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, out Foundation.NSError error);
	public virtual void CreateComputePipelineState (IMTLFunction computeFunction, System.Action&lt;IMTLComputePipelineState,Foundation.NSError&gt; completionHandler);
	public virtual void CreateComputePipelineState (IMTLFunction computeFunction, MTLPipelineOption options, System.Action&lt;IMTLComputePipelineState,Metal.MTLComputePipelineReflection,Foundation.NSError&gt; completionHandler);
	public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out Foundation.NSError error);
	public virtual IMTLLibrary CreateDefaultLibrary ();
	public virtual IMTLDepthStencilState CreateDepthStencilState (MTLDepthStencilDescriptor descriptor);
	public virtual IMTLLibrary CreateLibrary (Foundation.NSObject data, out Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (string filepath, out Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (string source, MTLCompileOptions options, out Foundation.NSError error);
	public virtual void CreateLibrary (string source, MTLCompileOptions options, System.Action&lt;IMTLLibrary,Foundation.NSError&gt; completionHandler);
	public virtual IMTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, out Foundation.NSError error);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, System.Action&lt;IMTLRenderPipelineState,Foundation.NSError&gt; completionHandler);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action&lt;IMTLRenderPipelineState,Metal.MTLRenderPipelineReflection,Foundation.NSError&gt; completionHandler);
	public virtual IMTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out Foundation.NSError error);
	public virtual IMTLSamplerState CreateSamplerState (MTLSamplerDescriptor descriptor);
	public virtual IMTLTexture CreateTexture (MTLTextureDescriptor descriptor);
	public virtual bool SupportsFeatureSet (MTLFeatureSet featureSet);
}
</pre>

### New Type Metal.IMTLDrawable

<pre style='color: green'>
public interface IMTLDrawable : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Present ();
	public virtual void Present (double presentationTime);
}
</pre>

### New Type Metal.IMTLFunction

<pre style='color: green'>
public interface IMTLFunction : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual MTLFunctionType FunctionType { get; }
	public virtual string Name { get; }
	public virtual MTLVertexAttribute[] VertexAttributes { get; }
}
</pre>

### New Type Metal.IMTLLibrary

<pre style='color: green'>
public interface IMTLLibrary : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string[] FunctionNames { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLFunction CreateFunction (string functionName);
}
</pre>

### New Type Metal.IMTLParallelRenderCommandEncoder

<pre style='color: green'>
public interface IMTLParallelRenderCommandEncoder : IMTLCommandEncoder, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder ();
}
</pre>

### New Type Metal.IMTLRenderCommandEncoder

<pre style='color: green'>
public interface IMTLRenderCommandEncoder : IMTLCommandEncoder, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset);
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset, uint instanceCount);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount, uint instanceCount);
	public virtual void SetBlendColor (float red, float green, float blue, float alpha);
	public virtual void SetCullMode (MTLCullMode cullMode);
	public virtual void SetDepthBias (float depthBias, float slopeScale, float clamp);
	public virtual void SetDepthStencilState (IMTLDepthStencilState depthStencilState);
	public virtual void SetFragmentBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetFragmentBufferOffset (uint offset, uint index);
	public virtual void SetFragmentBuffers (IMTLBuffer buffers, IntPtr IntPtrOffsets, Foundation.NSRange range);
	public virtual void SetFragmentBytes (IntPtr bytes, uint length, uint index);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, Foundation.NSRange range);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, IntPtr floatArrayPtrLodMinClamps, IntPtr floatArrayPtrLodMaxClamps, Foundation.NSRange range);
	public virtual void SetFragmentTexture (IMTLTexture texture, uint index);
	public virtual void SetFragmentTextures (IMTLTexture[] textures, Foundation.NSRange range);
	public virtual void SetFrontFacingWinding (MTLWinding frontFacingWinding);
	public virtual void SetRenderPipelineState (IMTLRenderPipelineState pipelineState);
	public virtual void SetScissorRect (MTLScissorRect rect);
	public virtual void SetStencilReferenceValue (uint referenceValue);
	public virtual void SetTriangleFillMode (MTLTriangleFillMode fillMode);
	public virtual void SetVertexBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetVertexBufferOffset (uint offset, uint index);
	public virtual void SetVertexBuffers (IMTLBuffer[] buffers, IntPtr uintArrayPtrOffsets, Foundation.NSRange range);
	public virtual void SetVertexBytes (IntPtr bytes, uint length, uint index);
	public virtual void SetVertexSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetVertexSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, Foundation.NSRange range);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, IntPtr floatArrayPtrLodMinClamps, IntPtr floatArrayPtrLodMaxClamps, Foundation.NSRange range);
	public virtual void SetVertexTexture (IMTLTexture texture, uint index);
	public virtual void SetVertexTextures (IMTLTexture[] textures, Foundation.NSRange range);
	public virtual void SetViewport (MTLViewport viewport);
	public virtual void SetVisibilityResultMode (MTLVisibilityResultMode mode, uint offset);
}
</pre>

### New Type Metal.IMTLRenderPipelineState

<pre style='color: green'>
public interface IMTLRenderPipelineState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
</pre>

### New Type Metal.IMTLResource

<pre style='color: green'>
public interface IMTLResource : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MTLCpuCacheMode CpuCacheMode { get; }
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);
}
</pre>

### New Type Metal.IMTLSamplerState

<pre style='color: green'>
public interface IMTLSamplerState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
</pre>

### New Type Metal.IMTLTexture

<pre style='color: green'>
public interface IMTLTexture : IMTLResource, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual uint ArrayLength { get; }
	public virtual uint Depth { get; }
	public virtual bool FramebufferOnly { get; }
	public virtual uint Height { get; }
	public virtual uint MipmapLevelCount { get; }
	public virtual MTLPixelFormat PixelFormat { get; }
	public virtual IMTLResource RootResource { get; }
	public virtual uint SampleCount { get; }
	public virtual MTLTextureType TextureType { get; }
	public virtual uint Width { get; }
	// methods
	public virtual IMTLTexture CreateTextureView (MTLPixelFormat pixelFormat);
	public virtual void GetBytes (IntPtr pixelBytes, uint bytesPerRow, MTLRegion region, uint level);
	public virtual void GetBytes (IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLRegion region, uint level, uint slice);
	public virtual void ReplaceRegion (MTLRegion region, uint level, IntPtr pixelBytes, uint bytesPerRow);
	public virtual void ReplaceRegion (MTLRegion region, uint level, uint slice, IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
}
</pre>

### New Type Metal.MTLArgument

<pre style='color: green'>
public class MTLArgument : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLArgument ();
	protected MTLArgument (Foundation.NSObjectFlag t);
	protected MTLArgument (IntPtr handle);
	// properties
	public virtual MTLArgumentAccess Access { get; }
	public virtual bool Active { get; }
	public virtual uint BufferAlignment { get; }
	public virtual uint BufferDataSize { get; }
	public virtual MTLDataType BufferDataType { get; }
	public virtual MTLStructType BufferStructType { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Index { get; }
	public virtual string Name { get; }
	public virtual MTLDataType TextureDataType { get; }
	public virtual MTLTextureType TextureType { get; }
	public virtual uint ThreadgroupMemoryAlignment { get; }
	public virtual uint ThreadgroupMemoryDataSize { get; }
	public virtual MTLArgumentType Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLArgumentAccess

<pre style='color: green'>
[Serializable]
public enum MTLArgumentAccess {
	ReadOnly = 0,
	ReadWrite = 1,
	WriteOnly = 2,
}
</pre>

### New Type Metal.MTLArgumentType

<pre style='color: green'>
[Serializable]
public enum MTLArgumentType {
	Buffer = 0,
	Sampler = 3,
	Texture = 2,
	ThreadgroupMemory = 1,
}
</pre>

### New Type Metal.MTLArrayType

<pre style='color: green'>
public class MTLArrayType : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLArrayType ();
	protected MTLArrayType (Foundation.NSObjectFlag t);
	protected MTLArrayType (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLDataType ElementType { get; }
	public virtual uint Length { get; }
	public virtual uint Stride { get; }
	// methods
	public virtual MTLArrayType ElementArrayType ();
	public virtual MTLStructType ElementStructType ();
}
</pre>

### New Type Metal.MTLBlendFactor

<pre style='color: green'>
[Serializable]
public enum MTLBlendFactor {
	BlendAlpha = 13,
	BlendColor = 11,
	DestinationAlpha = 8,
	DestinationColor = 6,
	One = 1,
	OneMinusBlendAlpha = 14,
	OneMinusBlendColor = 12,
	OneMinusDestinationAlpha = 9,
	OneMinusDestinationColor = 7,
	OneMinusSourceAlpha = 5,
	OneMinusSourceColor = 3,
	SourceAlpha = 4,
	SourceAlphaSaturated = 10,
	SourceColor = 2,
	Zero = 0,
}
</pre>

### New Type Metal.MTLBlendOperation

<pre style='color: green'>
[Serializable]
public enum MTLBlendOperation {
	Add = 0,
	Max = 4,
	Min = 3,
	ReverseSubtract = 2,
	Subtract = 1,
}
</pre>

### New Type Metal.MTLBlitCommandEncoder_Extensions

<pre style='color: green'>
public static class MTLBlitCommandEncoder_Extensions {
	// methods
	public static void CopyFromBuffer (IMTLBlitCommandEncoder This, IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceBytesPerRow, uint sourceBytesPerImage, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin, MTLBlitOption options);
	public static void CopyFromTexture (IMTLBlitCommandEncoder This, IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinatinBytesPerRow, uint destinationBytesPerImage, MTLBlitOption options);
}
</pre>

### New Type Metal.MTLBlitOption

<pre style='color: green'>
[Serializable]
[Flags]
public enum MTLBlitOption {
	DepthFromDepthStencil = 1,
	None = 0,
	StencilFromDepthStencil = 2,
}
</pre>

### New Type Metal.MTLClearColor

<pre style='color: green'>
public struct MTLClearColor {
	// constructors
	public MTLClearColor (double red, double green, double blue, double alpha);
	// fields
	public double Alpha;
	public double Blue;
	public double Green;
	public double Red;
}
</pre>

### New Type Metal.MTLClearValue

<pre style='color: green'>
public struct MTLClearValue {
	// constructors
	public MTLClearValue (MTLClearColor color);
	public MTLClearValue (double depth);
	public MTLClearValue (ulong stencil);
	// fields
	public MTLClearColor Color;
	public double Depth;
	public ulong Stencil;
}
</pre>

### New Type Metal.MTLColorWriteMask

<pre style='color: green'>
[Serializable]
[Flags]
public enum MTLColorWriteMask {
	All = 15,
	Alpha = 1,
	Blue = 2,
	Green = 4,
	None = 0,
	Red = 8,
}
</pre>

### New Type Metal.MTLCommandBufferError

<pre style='color: green'>
[Serializable]
public enum MTLCommandBufferError {
	Blacklisted = 4,
	Internal = 1,
	InvalidResource = 9,
	None = 0,
	NotPermitted = 7,
	OutOfMemory = 8,
	PageFault = 3,
	Timeout = 2,
}
</pre>

### New Type Metal.MTLCommandBufferStatus

<pre style='color: green'>
[Serializable]
public enum MTLCommandBufferStatus {
	Committed = 2,
	Completed = 4,
	Enqueued = 1,
	Error = 5,
	NotEnqueued = 0,
	Scheduled = 3,
}
</pre>

### New Type Metal.MTLCompareFunction

<pre style='color: green'>
[Serializable]
public enum MTLCompareFunction {
	Always = 7,
	Equal = 2,
	Greater = 4,
	GreaterEqual = 6,
	Less = 1,
	LessEqual = 3,
	Never = 0,
	NotEqual = 5,
}
</pre>

### New Type Metal.MTLCompileOptions

<pre style='color: green'>
public class MTLCompileOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLCompileOptions ();
	protected MTLCompileOptions (Foundation.NSObjectFlag t);
	protected MTLCompileOptions (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool FastMathEnabled { get; set; }
	public virtual MTLLanguageVersion LanguageVersion { get; set; }
	public virtual Foundation.NSDictionary PreprocessorMacros { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLComputeCommandEncoder_Extensions

<pre style='color: green'>
public static class MTLComputeCommandEncoder_Extensions {
	// methods
	public static void DispatchThreadgroups (IMTLComputeCommandEncoder This, IMTLBuffer indirectBuffer, uint indirectBufferOffset, MTLSize threadsPerThreadgroup);
}
</pre>

### New Type Metal.MTLComputePipelineDescriptor

<pre style='color: green'>
public class MTLComputePipelineDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLComputePipelineDescriptor ();
	protected MTLComputePipelineDescriptor (Foundation.NSObjectFlag t);
	protected MTLComputePipelineDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IMTLFunction ComputeFunction { get; set; }
	public virtual string Label { get; set; }
	public virtual bool ThreadGroupSizeIsMultipleOfThreadExecutionWidth { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
</pre>

### New Type Metal.MTLComputePipelineReflection

<pre style='color: green'>
public class MTLComputePipelineReflection : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLComputePipelineReflection ();
	protected MTLComputePipelineReflection (Foundation.NSObjectFlag t);
	protected MTLComputePipelineReflection (IntPtr handle);
	// properties
	public virtual Foundation.NSObject[] Arguments { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLCpuCacheMode

<pre style='color: green'>
[Serializable]
public enum MTLCpuCacheMode {
	DefaultCache = 0,
	WriteCombined = 1,
}
</pre>

### New Type Metal.MTLCullMode

<pre style='color: green'>
[Serializable]
public enum MTLCullMode {
	Back = 2,
	Front = 1,
	None = 0,
}
</pre>

### New Type Metal.MTLDataType

<pre style='color: green'>
[Serializable]
public enum MTLDataType {
	Array = 2,
	Bool = 53,
	Bool2 = 54,
	Bool3 = 55,
	Bool4 = 56,
	Char = 45,
	Char2 = 46,
	Char3 = 47,
	Char4 = 48,
	Float = 3,
	Float2 = 4,
	Float2x2 = 7,
	Float2x3 = 8,
	Float2x4 = 9,
	Float3 = 5,
	Float3x2 = 10,
	Float3x3 = 11,
	Float3x4 = 12,
	Float4 = 6,
	Float4x2 = 13,
	Float4x3 = 14,
	Float4x4 = 15,
	Half = 16,
	Half2 = 17,
	Half2x2 = 20,
	Half2x3 = 21,
	Half2x4 = 22,
	Half3 = 18,
	Half3x2 = 23,
	Half3x3 = 24,
	Half3x4 = 25,
	Half4 = 19,
	Half4x2 = 26,
	Half4x3 = 27,
	Half4x4 = 28,
	Int = 29,
	Int2 = 30,
	Int3 = 31,
	Int4 = 32,
	None = 0,
	Short = 37,
	Short2 = 38,
	Short3 = 39,
	Short4 = 40,
	Struct = 1,
	UChar = 49,
	UChar2 = 50,
	UChar3 = 51,
	UChar4 = 52,
	UInt = 33,
	UInt2 = 34,
	UInt3 = 35,
	UInt4 = 36,
	UShort = 41,
	UShort2 = 42,
	UShort3 = 43,
	UShort4 = 44,
}
</pre>

### New Type Metal.MTLDeallocator

<pre style='color: green'>
public sealed delegate MTLDeallocator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public MTLDeallocator (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (IntPtr pointer, uint length, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (IntPtr pointer, uint length);
}
</pre>

### New Type Metal.MTLDepthClipMode

<pre style='color: green'>
[Serializable]
public enum MTLDepthClipMode {
	Clamp = 1,
	Clip = 0,
}
</pre>

### New Type Metal.MTLDepthStencilDescriptor

<pre style='color: green'>
public class MTLDepthStencilDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLDepthStencilDescriptor ();
	protected MTLDepthStencilDescriptor (Foundation.NSObjectFlag t);
	protected MTLDepthStencilDescriptor (IntPtr handle);
	// properties
	public virtual MTLStencilDescriptor BackFaceStencil { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLCompareFunction DepthCompareFunction { get; set; }
	public virtual bool DepthWriteEnabled { get; set; }
	public virtual MTLStencilDescriptor FrontFaceStencil { get; set; }
	public virtual string Label { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLDevice

<pre style='color: green'>
public static class MTLDevice {
	// properties
	public static IMTLDevice SystemDefault { get; }
}
</pre>

### New Type Metal.MTLDevice_Extensions

<pre style='color: green'>
public static class MTLDevice_Extensions {
	// methods
	public static IMTLBuffer CreateBuffer&lt;T&gt; (IMTLDevice This, T[] data, MTLResourceOptions options);
	public static IMTLBuffer CreateBufferNoCopy&lt;T&gt; (IMTLDevice This, T[] data, MTLResourceOptions options, MTLDeallocator deallocator);
	public static void CreateComputePipelineState (IMTLDevice This, MTLComputePipelineDescriptor descriptor, MTLPipelineOption options, MTLNewComputePipelineStateWithReflectionCompletionHandler completionHandler);
	public static IMTLComputePipelineState CreateComputePipelineState (IMTLDevice This, MTLComputePipelineDescriptor descriptor, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out Foundation.NSError error);
	public static bool GetDepth24Stencil8PixelFormatSupported (IMTLDevice This);
	public static bool GetHeadless (IMTLDevice This);
	public static bool GetLowPower (IMTLDevice This);
	public static MTLSize GetMaxThreadsPerThreadgroup (IMTLDevice This);
	public static bool SupportsTextureSampleCount (IMTLDevice This, uint sampleCount);
}
</pre>

### New Type Metal.MTLDispatchThreadgroupsIndirectArguments

<pre style='color: green'>
public struct MTLDispatchThreadgroupsIndirectArguments {
	// fields
	public uint ThreadGroupsPerGrid1;
	public uint ThreadGroupsPerGrid2;
	public uint ThreadGroupsPerGrid3;
}
</pre>

### New Type Metal.MTLDrawable

<pre style='color: green'>
public abstract class MTLDrawable : Foundation.NSObject, Foundation.INSObjectProtocol, IMTLDrawable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTLDrawable ();
	protected MTLDrawable (Foundation.NSObjectFlag t);
	protected MTLDrawable (IntPtr handle);
	// methods
	public virtual void Present ();
	public virtual void Present (double presentationTime);
}
</pre>

### New Type Metal.MTLDrawIndexedPrimitivesIndirectArguments

<pre style='color: green'>
public struct MTLDrawIndexedPrimitivesIndirectArguments {
	// fields
	public uint BaseInstance;
	public uint BaseVertex;
	public uint IndexCount;
	public uint IndexStart;
	public uint InstanceCount;
}
</pre>

### New Type Metal.MTLDrawPrimitivesIndirectArguments

<pre style='color: green'>
public struct MTLDrawPrimitivesIndirectArguments {
	// fields
	public uint BaseInstance;
	public uint InstanceCount;
	public uint VertexCount;
	public uint VertexStart;
}
</pre>

### New Type Metal.MTLFeatureSet

<pre style='color: green'>
[Serializable]
public enum MTLFeatureSet {
	iOS_GPUFamily1_v1 = 0,
	iOS_GPUFamily1_v2 = 2,
	iOS_GPUFamily2_v1 = 1,
	iOS_GPUFamily2_v2 = 3,
	iOS_GPUFamily3_v1 = 4,
}
</pre>

### New Type Metal.MTLFunctionType

<pre style='color: green'>
[Serializable]
public enum MTLFunctionType {
	Fragment = 2,
	Kernel = 3,
	Vertex = 1,
}
</pre>

### New Type Metal.MTLIndexType

<pre style='color: green'>
[Serializable]
public enum MTLIndexType {
	UInt16 = 0,
	UInt32 = 1,
}
</pre>

### New Type Metal.MTLLanguageVersion

<pre style='color: green'>
[Serializable]
public enum MTLLanguageVersion {
	v1_1 = 65537,
}
</pre>

### New Type Metal.MTLLibraryError

<pre style='color: green'>
[Serializable]
public enum MTLLibraryError {
	CompileFailure = 3,
	CompileWarning = 4,
	Internal = 2,
	Unsupported = 1,
}
</pre>

### New Type Metal.MTLLoadAction

<pre style='color: green'>
[Serializable]
public enum MTLLoadAction {
	Clear = 2,
	DontCare = 0,
	Load = 1,
}
</pre>

### New Type Metal.MTLMultisampleDepthResolveFilter

<pre style='color: green'>
[Serializable]
public enum MTLMultisampleDepthResolveFilter {
	Max = 2,
	Min = 1,
	Sample0 = 0,
}
</pre>

### New Type Metal.MTLNewComputePipelineStateWithReflectionCompletionHandler

<pre style='color: green'>
public sealed delegate MTLNewComputePipelineStateWithReflectionCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public MTLNewComputePipelineStateWithReflectionCompletionHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (IMTLComputePipelineState computePipelineState, MTLComputePipelineReflection reflection, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (IMTLComputePipelineState computePipelineState, MTLComputePipelineReflection reflection, Foundation.NSError error);
}
</pre>

### New Type Metal.MTLOrigin

<pre style='color: green'>
public struct MTLOrigin {
	// constructors
	public MTLOrigin (nint x, nint y, nint z);
	// fields
	public nint X;
	public nint Y;
	public nint Z;
	// methods
	public override string ToString ();
}
</pre>

### New Type Metal.MTLPipelineOption

<pre style='color: green'>
[Serializable]
[Flags]
public enum MTLPipelineOption {
	ArgumentInfo = 1,
	BufferTypeInfo = 2,
	None = 0,
}
</pre>

### New Type Metal.MTLPixelFormat

<pre style='color: green'>
[Serializable]
public enum MTLPixelFormat {
	A8Unorm = 1,
	BC1_RGBA_sRGB = 131,
	BC1RGBA = 130,
	BC2_RGBA_sRGB = 133,
	BC2RGBA = 132,
	BC3_RGBA_sRGB = 135,
	BC3RGBA = 134,
	BC4_RSnorm = 141,
	BC4_RUnorm = 140,
	BC5_RGSnorm = 143,
	BC5_RGUnorm = 142,
	BC6H_RGBFloat = 150,
	BC6H_RGBUFloat = 151,
	BC7_RGBAUnorm = 152,
	BC7_RGBAUnorm_sRGB = 153,
	BGRA8Unorm = 80,
	BGRA8Unorm_sRGB = 81,
	BGRG422 = 241,
	Depth24Unorm_Stencil8 = 255,
	Depth32Float = 252,
	Depth32Float_Stencil8 = 260,
	GBGR422 = 240,
	Invalid = 0,
	R16Float = 25,
	R16Sint = 24,
	R16Snorm = 22,
	R16Uint = 23,
	R16Unorm = 20,
	R32Float = 55,
	R32Sint = 54,
	R32Uint = 53,
	R8Sint = 14,
	R8Snorm = 12,
	R8Uint = 13,
	R8Unorm = 10,
	R8Unorm_sRGB = 11,
	RG11B10Float = 92,
	RG16Float = 65,
	RG16Sint = 64,
	RG16Snorm = 62,
	RG16Uint = 63,
	RG16Unorm = 60,
	RG32Float = 105,
	RG32Sint = 104,
	RG32Uint = 103,
	RG8Sint = 34,
	RG8Snorm = 32,
	RG8Uint = 33,
	RG8Unorm = 30,
	RGB10A2Uint = 91,
	RGB10A2Unorm = 90,
	RGB9E5Float = 93,
	RGBA16Float = 115,
	RGBA16Sint = 114,
	RGBA16Snorm = 112,
	RGBA16Uint = 113,
	RGBA16Unorm = 110,
	RGBA32Float = 125,
	RGBA32Sint = 124,
	RGBA32Uint = 123,
	RGBA8Sint = 74,
	RGBA8Snorm = 72,
	RGBA8Uint = 73,
	RGBA8Unorm = 70,
	RGBA8Unorm_sRGB = 71,
	Stencil8 = 253,
}
</pre>

### New Type Metal.MTLPrimitiveType

<pre style='color: green'>
[Serializable]
public enum MTLPrimitiveType {
	Line = 1,
	LineStrip = 2,
	Point = 0,
	Triangle = 3,
	TriangleStrip = 4,
}
</pre>

### New Type Metal.MTLPurgeableState

<pre style='color: green'>
[Serializable]
public enum MTLPurgeableState {
	Empty = 4,
	KeepCurrent = 1,
	NonVolatile = 2,
	Volatile = 3,
}
</pre>

### New Type Metal.MTLRegion

<pre style='color: green'>
public struct MTLRegion {
	// constructors
	public MTLRegion (MTLOrigin origin, MTLSize size);
	// fields
	public MTLOrigin Origin;
	public MTLSize Size;
	// methods
	public static MTLRegion Create1D (nint x, nint width);
	public static MTLRegion Create1D (uint x, uint width);
	public static MTLRegion Create2D (nint x, nint y, nint width, nint height);
	public static MTLRegion Create2D (uint x, uint y, uint width, uint height);
	public static MTLRegion Create3D (nint x, nint y, nint z, nint width, nint height, nint depth);
	public static MTLRegion Create3D (uint x, uint y, uint z, uint width, uint height, uint depth);
}
</pre>

### New Type Metal.MTLRenderCommandEncoder_Extensions

<pre style='color: green'>
public static class MTLRenderCommandEncoder_Extensions {
	// methods
	public static void DrawIndexedPrimitives (IMTLRenderCommandEncoder This, MTLPrimitiveType primitiveType, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset, IMTLBuffer indirectBuffer, uint indirectBufferOffset);
	public static void DrawIndexedPrimitives (IMTLRenderCommandEncoder This, MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset, uint instanceCount, nint baseVertex, uint baseInstance);
	public static void DrawPrimitives (IMTLRenderCommandEncoder This, MTLPrimitiveType primitiveType, IMTLBuffer indirectBuffer, uint indirectBufferOffset);
	public static void DrawPrimitives (IMTLRenderCommandEncoder This, MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount, uint instanceCount, uint baseInstance);
	public static void SetDepthClipMode (IMTLRenderCommandEncoder This, MTLDepthClipMode depthClipMode);
	public static void SetStencilFrontReferenceValue (IMTLRenderCommandEncoder This, uint frontReferenceValue, uint backReferenceValue);
}
</pre>

### New Type Metal.MTLRenderPassAttachmentDescriptor

<pre style='color: green'>
public class MTLRenderPassAttachmentDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassAttachmentDescriptor ();
	protected MTLRenderPassAttachmentDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPassAttachmentDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint DepthPlane { get; set; }
	public virtual uint Level { get; set; }
	public virtual MTLLoadAction LoadAction { get; set; }
	public virtual uint ResolveDepthPlane { get; set; }
	public virtual uint ResolveLevel { get; set; }
	public virtual uint ResolveSlice { get; set; }
	public virtual IMTLTexture ResolveTexture { get; set; }
	public virtual uint Slice { get; set; }
	public virtual MTLStoreAction StoreAction { get; set; }
	public virtual IMTLTexture Texture { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLRenderPassColorAttachmentDescriptor

<pre style='color: green'>
public class MTLRenderPassColorAttachmentDescriptor : Metal.MTLRenderPassAttachmentDescriptor, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassColorAttachmentDescriptor ();
	protected MTLRenderPassColorAttachmentDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPassColorAttachmentDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLClearColor ClearColor { get; set; }
}
</pre>

### New Type Metal.MTLRenderPassColorAttachmentDescriptorArray

<pre style='color: green'>
public class MTLRenderPassColorAttachmentDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassColorAttachmentDescriptorArray ();
	protected MTLRenderPassColorAttachmentDescriptorArray (Foundation.NSObjectFlag t);
	protected MTLRenderPassColorAttachmentDescriptorArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public MTLRenderPassColorAttachmentDescriptor Item { get; set; }
}
</pre>

### New Type Metal.MTLRenderPassDepthAttachmentDescriptor

<pre style='color: green'>
public class MTLRenderPassDepthAttachmentDescriptor : Metal.MTLRenderPassAttachmentDescriptor, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassDepthAttachmentDescriptor ();
	protected MTLRenderPassDepthAttachmentDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPassDepthAttachmentDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual double ClearDepth { get; set; }
}
</pre>

### New Type Metal.MTLRenderPassDescriptor

<pre style='color: green'>
public class MTLRenderPassDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassDescriptor ();
	protected MTLRenderPassDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPassDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLRenderPassColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLRenderPassDepthAttachmentDescriptor DepthAttachment { get; set; }
	public virtual MTLRenderPassStencilAttachmentDescriptor StencilAttachment { get; set; }
	public virtual IMTLBuffer VisibilityResultBuffer { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static MTLRenderPassDescriptor CreateRenderPassDescriptor ();
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLRenderPassStencilAttachmentDescriptor

<pre style='color: green'>
public class MTLRenderPassStencilAttachmentDescriptor : Metal.MTLRenderPassAttachmentDescriptor, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPassStencilAttachmentDescriptor ();
	protected MTLRenderPassStencilAttachmentDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPassStencilAttachmentDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint ClearStencil { get; set; }
}
</pre>

### New Type Metal.MTLRenderPipelineColorAttachmentDescriptor

<pre style='color: green'>
public class MTLRenderPipelineColorAttachmentDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPipelineColorAttachmentDescriptor ();
	protected MTLRenderPipelineColorAttachmentDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPipelineColorAttachmentDescriptor (IntPtr handle);
	// properties
	public virtual MTLBlendOperation AlphaBlendOperation { get; set; }
	public virtual bool BlendingEnabled { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLBlendFactor DestinationAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor DestinationRgbBlendFactor { get; set; }
	public virtual MTLPixelFormat PixelFormat { get; set; }
	public virtual MTLBlendOperation RgbBlendOperation { get; set; }
	public virtual MTLBlendFactor SourceAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor SourceRgbBlendFactor { get; set; }
	public virtual MTLColorWriteMask WriteMask { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type Metal.MTLRenderPipelineColorAttachmentDescriptorArray

<pre style='color: green'>
public class MTLRenderPipelineColorAttachmentDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPipelineColorAttachmentDescriptorArray ();
	protected MTLRenderPipelineColorAttachmentDescriptorArray (Foundation.NSObjectFlag t);
	protected MTLRenderPipelineColorAttachmentDescriptorArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public MTLRenderPipelineColorAttachmentDescriptor Item { get; set; }
}
</pre>

### New Type Metal.MTLRenderPipelineDescriptor

<pre style='color: green'>
public class MTLRenderPipelineDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPipelineDescriptor ();
	protected MTLRenderPipelineDescriptor (Foundation.NSObjectFlag t);
	protected MTLRenderPipelineDescriptor (IntPtr handle);
	// properties
	public virtual bool AlphaToCoverageEnabled { get; set; }
	public virtual bool AlphaToOneEnabled { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLRenderPipelineColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLPixelFormat DepthAttachmentPixelFormat { get; set; }
	public virtual IMTLFunction FragmentFunction { get; set; }
	public virtual string Label { get; set; }
	public virtual bool RasterizationEnabled { get; set; }
	public virtual uint SampleCount { get; set; }
	public virtual MTLPixelFormat StencilAttachmentPixelFormat { get; set; }
	public virtual MTLVertexDescriptor VertexDescriptor { get; set; }
	public virtual IMTLFunction VertexFunction { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
</pre>

### New Type Metal.MTLRenderPipelineError

<pre style='color: green'>
[Serializable]
public enum MTLRenderPipelineError {
	Internal = 1,
	InvalidInput = 3,
	Unsupported = 2,
}
</pre>

### New Type Metal.MTLRenderPipelineReflection

<pre style='color: green'>
public class MTLRenderPipelineReflection : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLRenderPipelineReflection ();
	protected MTLRenderPipelineReflection (Foundation.NSObjectFlag t);
	protected MTLRenderPipelineReflection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject[] FragmentArguments { get; }
	public virtual Foundation.NSObject[] VertexArguments { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type Metal.MTLResource_Extensions

<pre style='color: green'>
public static class MTLResource_Extensions {
	// methods
	public static MTLStorageMode GetStorageMode (IMTLResource This);
}
</pre>

### New Type Metal.MTLResourceOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum MTLResourceOptions {
	CpuCacheModeDefault = 0,
	CpuCacheModeWriteCombined = 1,
	StorageModeManaged = 16,
	StorageModePrivate = 32,
	StorageModeShared = 0,
}
</pre>

### New Type Metal.MTLSamplerAddressMode

<pre style='color: green'>
[Serializable]
public enum MTLSamplerAddressMode {
	ClampToEdge = 0,
	ClampToZero = 4,
	MirrorClampToEdge = 1,
	MirrorRepeat = 3,
	Repeat = 2,
}
</pre>

### New Type Metal.MTLSamplerDescriptor

<pre style='color: green'>
public class MTLSamplerDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLSamplerDescriptor ();
	protected MTLSamplerDescriptor (Foundation.NSObjectFlag t);
	protected MTLSamplerDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLCompareFunction CompareFunction { get; set; }
	public virtual string Label { get; set; }
	public virtual bool LodAverage { get; set; }
	public virtual float LodMaxClamp { get; set; }
	public virtual float LodMinClamp { get; set; }
	public virtual MTLSamplerMinMagFilter MagFilter { get; set; }
	public virtual uint MaxAnisotropy { get; set; }
	public virtual MTLSamplerMinMagFilter MinFilter { get; set; }
	public virtual MTLSamplerMipFilter MipFilter { get; set; }
	public virtual bool NormalizedCoordinates { get; set; }
	public virtual MTLSamplerAddressMode RAddressMode { get; set; }
	public virtual MTLSamplerAddressMode SAddressMode { get; set; }
	public virtual MTLSamplerAddressMode TAddressMode { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type Metal.MTLSamplerMinMagFilter

<pre style='color: green'>
[Serializable]
public enum MTLSamplerMinMagFilter {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type Metal.MTLSamplerMipFilter

<pre style='color: green'>
[Serializable]
public enum MTLSamplerMipFilter {
	Linear = 2,
	Nearest = 1,
	NotMipmapped = 0,
}
</pre>

### New Type Metal.MTLScissorRect

<pre style='color: green'>
public struct MTLScissorRect {
	// constructors
	public MTLScissorRect (uint x, uint y, uint width, uint height);
	// fields
	public uint Height;
	public uint Width;
	public uint X;
	public uint Y;
	// methods
	public override string ToString ();
}
</pre>

### New Type Metal.MTLSize

<pre style='color: green'>
public struct MTLSize {
	// constructors
	public MTLSize (nint width, nint height, nint depth);
	// fields
	public nint Depth;
	public nint Height;
	public nint Width;
}
</pre>

### New Type Metal.MTLStencilDescriptor

<pre style='color: green'>
public class MTLStencilDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLStencilDescriptor ();
	protected MTLStencilDescriptor (Foundation.NSObjectFlag t);
	protected MTLStencilDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLStencilOperation DepthFailureOperation { get; set; }
	public virtual MTLStencilOperation DepthStencilPassOperation { get; set; }
	public virtual uint ReadMask { get; set; }
	public virtual MTLCompareFunction StencilCompareFunction { get; set; }
	public virtual MTLStencilOperation StencilFailureOperation { get; set; }
	public virtual uint WriteMask { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type Metal.MTLStencilOperation

<pre style='color: green'>
[Serializable]
public enum MTLStencilOperation {
	DecrementClamp = 4,
	DecrementWrap = 7,
	IncrementClamp = 3,
	IncrementWrap = 6,
	Invert = 5,
	Keep = 0,
	Replace = 2,
	Zero = 1,
}
</pre>

### New Type Metal.MTLStorageMode

<pre style='color: green'>
[Serializable]
public enum MTLStorageMode {
	Managed = 1,
	Private = 2,
	Shared = 0,
}
</pre>

### New Type Metal.MTLStoreAction

<pre style='color: green'>
[Serializable]
public enum MTLStoreAction {
	DontCare = 0,
	MultisampleResolve = 2,
	Store = 1,
}
</pre>

### New Type Metal.MTLStructMember

<pre style='color: green'>
public class MTLStructMember : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLStructMember ();
	protected MTLStructMember (Foundation.NSObjectFlag t);
	protected MTLStructMember (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLDataType DataType { get; }
	public virtual string Name { get; }
	public virtual uint Offset { get; }
	// methods
	public virtual MTLArrayType ArrayType ();
	public virtual MTLStructType StructType ();
}
</pre>

### New Type Metal.MTLStructType

<pre style='color: green'>
public class MTLStructType : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLStructType ();
	protected MTLStructType (Foundation.NSObjectFlag t);
	protected MTLStructType (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLStructMember[] Members { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MTLStructMember Lookup (string name);
}
</pre>

### New Type Metal.MTLTexture_Extensions

<pre style='color: green'>
public static class MTLTexture_Extensions {
	// methods
	public static IMTLTexture CreateTextureView (IMTLTexture This, MTLPixelFormat pixelFormat, MTLTextureType textureType, Foundation.NSRange levelRange, Foundation.NSRange sliceRange);
	public static IMTLBuffer GetBuffer (IMTLTexture This);
	public static uint GetBufferBytesPerRow (IMTLTexture This);
	public static uint GetBufferOffset (IMTLTexture This);
	public static uint GetParentRelativeLevel (IMTLTexture This);
	public static uint GetParentRelativeSlice (IMTLTexture This);
	public static IMTLTexture GetParentTexture (IMTLTexture This);
}
</pre>

### New Type Metal.MTLTextureDescriptor

<pre style='color: green'>
public class MTLTextureDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLTextureDescriptor ();
	protected MTLTextureDescriptor (Foundation.NSObjectFlag t);
	protected MTLTextureDescriptor (IntPtr handle);
	// properties
	public virtual uint ArrayLength { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLCpuCacheMode CpuCacheMode { get; set; }
	public virtual uint Depth { get; set; }
	public virtual uint Height { get; set; }
	public virtual uint MipmapLevelCount { get; set; }
	public virtual MTLPixelFormat PixelFormat { get; set; }
	public virtual MTLResourceOptions ResourceOptions { get; set; }
	public virtual uint SampleCount { get; set; }
	public virtual MTLStorageMode StorageMode { get; set; }
	public virtual MTLTextureType TextureType { get; set; }
	public virtual MTLTextureUsage Usage { get; set; }
	public virtual uint Width { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static MTLTextureDescriptor CreateTexture2DDescriptor (MTLPixelFormat pixelFormat, uint width, uint height, bool mipmapped);
	public static MTLTextureDescriptor CreateTextureCubeDescriptor (MTLPixelFormat pixelFormat, uint size, bool mipmapped);
}
</pre>

### New Type Metal.MTLTextureType

<pre style='color: green'>
[Serializable]
public enum MTLTextureType {
	k1D = 0,
	k1DArray = 1,
	k2D = 2,
	k2DArray = 3,
	k2DMultisample = 4,
	k3D = 7,
	kCube = 5,
	kCubeArray = 6,
}
</pre>

### New Type Metal.MTLTextureUsage

<pre style='color: green'>
[Serializable]
[Flags]
public enum MTLTextureUsage {
	Blit = 8,
	PixelFormatView = 16,
	RenderTarget = 4,
	ShaderRead = 1,
	ShaderWrite = 2,
	Unknown = 0,
}
</pre>

### New Type Metal.MTLTriangleFillMode

<pre style='color: green'>
[Serializable]
public enum MTLTriangleFillMode {
	Fill = 0,
	Lines = 1,
}
</pre>

### New Type Metal.MTLVertexAttribute

<pre style='color: green'>
public class MTLVertexAttribute : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexAttribute ();
	protected MTLVertexAttribute (Foundation.NSObjectFlag t);
	protected MTLVertexAttribute (IntPtr handle);
	// properties
	public virtual bool Active { get; }
	public virtual uint AttributeIndex { get; }
	public virtual MTLDataType AttributeType { get; }
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; }
}
</pre>

### New Type Metal.MTLVertexAttributeDescriptor

<pre style='color: green'>
public class MTLVertexAttributeDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexAttributeDescriptor ();
	protected MTLVertexAttributeDescriptor (Foundation.NSObjectFlag t);
	protected MTLVertexAttributeDescriptor (IntPtr handle);
	// properties
	public virtual uint BufferIndex { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLVertexFormat Format { get; set; }
	public virtual uint Offset { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type Metal.MTLVertexAttributeDescriptorArray

<pre style='color: green'>
public class MTLVertexAttributeDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexAttributeDescriptorArray ();
	protected MTLVertexAttributeDescriptorArray (Foundation.NSObjectFlag t);
	protected MTLVertexAttributeDescriptorArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public MTLVertexAttributeDescriptor Item { get; set; }
}
</pre>

### New Type Metal.MTLVertexBufferLayoutDescriptor

<pre style='color: green'>
public class MTLVertexBufferLayoutDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexBufferLayoutDescriptor ();
	protected MTLVertexBufferLayoutDescriptor (Foundation.NSObjectFlag t);
	protected MTLVertexBufferLayoutDescriptor (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTLVertexStepFunction StepFunction { get; set; }
	public virtual uint StepRate { get; set; }
	public virtual uint Stride { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type Metal.MTLVertexBufferLayoutDescriptorArray

<pre style='color: green'>
public class MTLVertexBufferLayoutDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexBufferLayoutDescriptorArray ();
	protected MTLVertexBufferLayoutDescriptorArray (Foundation.NSObjectFlag t);
	protected MTLVertexBufferLayoutDescriptorArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public MTLVertexBufferLayoutDescriptor Item { get; set; }
}
</pre>

### New Type Metal.MTLVertexDescriptor

<pre style='color: green'>
public class MTLVertexDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTLVertexDescriptor ();
	protected MTLVertexDescriptor (Foundation.NSObjectFlag t);
	protected MTLVertexDescriptor (IntPtr handle);
	// properties
	public virtual MTLVertexAttributeDescriptorArray Attributes { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MTLVertexBufferLayoutDescriptorArray Layouts { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static MTLVertexDescriptor Create ();
	protected override void Dispose (bool disposing);
	public static MTLVertexDescriptor FromModelIO (ModelIO.MDLVertexDescriptor descriptor);
	public virtual void Reset ();
}
</pre>

### New Type Metal.MTLVertexFormat

<pre style='color: green'>
[Serializable]
public enum MTLVertexFormat {
	Char2 = 4,
	Char2Normalized = 10,
	Char3 = 5,
	Char3Normalized = 11,
	Char4 = 6,
	Char4Normalized = 12,
	Float = 28,
	Float2 = 29,
	Float3 = 30,
	Float4 = 31,
	Half2 = 25,
	Half3 = 26,
	Half4 = 27,
	Int = 32,
	Int1010102Normalized = 40,
	Int2 = 33,
	Int3 = 34,
	Int4 = 35,
	Invalid = 0,
	Short2 = 16,
	Short2Normalized = 22,
	Short3 = 17,
	Short3Normalized = 23,
	Short4 = 18,
	Short4Normalized = 24,
	UChar2 = 1,
	UChar2Normalized = 7,
	UChar3 = 2,
	UChar3Normalized = 8,
	UChar4 = 3,
	UChar4Normalized = 9,
	UInt = 36,
	UInt1010102Normalized = 41,
	UInt2 = 37,
	UInt3 = 38,
	UInt4 = 39,
	UShort2 = 13,
	UShort2Normalized = 19,
	UShort3 = 14,
	UShort3Normalized = 20,
	UShort4 = 15,
	UShort4Normalized = 21,
}
</pre>

### New Type Metal.MTLVertexFormatExtensions

<pre style='color: green'>
public static class MTLVertexFormatExtensions {
	// methods
	public static ModelIO.MDLVertexFormat ToModelVertexFormat (MTLVertexFormat vertexFormat);
}
</pre>

### New Type Metal.MTLVertexStepFunction

<pre style='color: green'>
[Serializable]
public enum MTLVertexStepFunction {
	Constant = 0,
	PerInstance = 2,
	PerVertex = 1,
}
</pre>

### New Type Metal.MTLViewport

<pre style='color: green'>
public struct MTLViewport {
	// constructors
	public MTLViewport (double originX, double originY, double width, double height, double znear, double zfar);
	// fields
	public double Height;
	public double OriginX;
	public double OriginY;
	public double Width;
	public double ZFar;
	public double ZNear;
	// methods
	public override string ToString ();
}
</pre>

### New Type Metal.MTLVisibilityResultMode

<pre style='color: green'>
[Serializable]
public enum MTLVisibilityResultMode {
	Boolean = 1,
	Counting = 2,
	Disabled = 0,
}
</pre>

### New Type Metal.MTLWinding

<pre style='color: green'>
[Serializable]
public enum MTLWinding {
	Clockwise = 0,
	CounterClockwise = 1,
}
</pre>

## New Namespace MetalKit

### New Type MetalKit.IMTKViewDelegate

<pre style='color: green'>
public interface IMTKViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Draw (MTKView view);
	public virtual void DrawableSizeWillChange (MTKView view, CoreGraphics.CGSize size);
}
</pre>

### New Type MetalKit.MTKMesh

<pre style='color: green'>
public class MTKMesh : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKMesh (Foundation.NSObjectFlag t);
	protected MTKMesh (IntPtr handle);
	public MTKMesh (ModelIO.MDLMesh mesh, Metal.IMTLDevice device, out Foundation.NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual MTKSubmesh[] Submeshes { get; }
	public virtual MTKMeshBuffer[] VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual ModelIO.MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static MTKMesh[] FromAsset (ModelIO.MDLAsset asset, Metal.IMTLDevice device, out ModelIO.MDLMesh[] sourceMeshes, out Foundation.NSError error);
}
</pre>

### New Type MetalKit.MTKMeshBuffer

<pre style='color: green'>
public class MTKMeshBuffer : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ModelIO.IMDLMeshBuffer, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKMeshBuffer (Foundation.NSObjectFlag t);
	protected MTKMeshBuffer (IntPtr handle);
	// properties
	public virtual ModelIO.IMDLMeshBufferAllocator Allocator { get; }
	public virtual Metal.IMTLBuffer Buffer { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Length { get; }
	public virtual ModelIO.MDLMeshBufferMap Map { get; }
	public virtual uint Offset { get; }
	public virtual ModelIO.MDLMeshBufferType Type { get; }
	public virtual ModelIO.IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void FillData (Foundation.NSData data, uint offset);
}
</pre>

### New Type MetalKit.MTKMeshBufferAllocator

<pre style='color: green'>
public class MTKMeshBufferAllocator : Foundation.NSObject, Foundation.INSObjectProtocol, ModelIO.IMDLMeshBufferAllocator, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKMeshBufferAllocator (Foundation.NSObjectFlag t);
	public MTKMeshBufferAllocator (Metal.IMTLDevice device);
	protected MTKMeshBufferAllocator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Metal.IMTLDevice Device { get; }
	// methods
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (ModelIO.IMDLMeshBufferZone zone, Foundation.NSData data, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBuffer CreateBuffer (ModelIO.IMDLMeshBufferZone zone, uint length, ModelIO.MDLMeshBufferType type);
	public virtual ModelIO.IMDLMeshBufferZone CreateZone (uint capacity);
	public virtual ModelIO.IMDLMeshBufferZone CreateZone (Foundation.NSNumber[] sizes, Foundation.NSNumber[] types);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MetalKit.MTKModel

<pre style='color: green'>
public static class MTKModel {
	// properties
	public static Foundation.NSString ErrorDomain { get; }
	public static Foundation.NSString ErrorKey { get; }
}
</pre>

### New Type MetalKit.MTKSubmesh

<pre style='color: green'>
public class MTKSubmesh : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKSubmesh (Foundation.NSObjectFlag t);
	protected MTKSubmesh (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MTKMeshBuffer IndexBuffer { get; }
	public virtual uint IndexCount { get; }
	public virtual Metal.MTLIndexType IndexType { get; }
	public virtual MTKMesh Mesh { get; }
	public virtual string Name { get; set; }
	public virtual Metal.MTLPrimitiveType PrimitiveType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MetalKit.MTKTextureLoader

<pre style='color: green'>
public class MTKTextureLoader : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKTextureLoader (Foundation.NSObjectFlag t);
	public MTKTextureLoader (Metal.IMTLDevice device);
	protected MTKTextureLoader (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Metal.IMTLDevice Device { get; }
	// methods
	protected override void Dispose (bool disposing);
	public void FromCGImage (CoreGraphics.CGImage cgImage, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);
	public Metal.IMTLTexture FromCGImage (CoreGraphics.CGImage cgImage, MTKTextureLoaderOptions options, out Foundation.NSError error);
	public void FromData (Foundation.NSData data, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);
	public Metal.IMTLTexture FromData (Foundation.NSData data, MTKTextureLoaderOptions options, out Foundation.NSError error);
	public void FromUrl (Foundation.NSUrl url, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);
	public Metal.IMTLTexture FromUrl (Foundation.NSUrl url, MTKTextureLoaderOptions options, out Foundation.NSError error);
}
</pre>

### New Type MetalKit.MTKTextureLoaderCallback

<pre style='color: green'>
public sealed delegate MTKTextureLoaderCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public MTKTextureLoaderCallback (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Metal.IMTLTexture texture, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Metal.IMTLTexture texture, Foundation.NSError error);
}
</pre>

### New Type MetalKit.MTKTextureLoaderError

<pre style='color: green'>
public static class MTKTextureLoaderError {
	// properties
	public static Foundation.NSString Domain { get; }
	public static Foundation.NSString Key { get; }
}
</pre>

### New Type MetalKit.MTKTextureLoaderOptions

<pre style='color: green'>
public class MTKTextureLoaderOptions : Foundation.DictionaryContainer {
	// constructors
	public MTKTextureLoaderOptions ();
	public MTKTextureLoaderOptions (Foundation.NSDictionary dictionary);
	// properties
	public bool? AllocateMipmaps { get; }
	public bool? Srgb { get; }
	public Metal.MTLCpuCacheMode? TextureCpuCacheMode { get; set; }
	public Metal.MTLTextureUsage? TextureUsage { get; set; }
}
</pre>

### New Type MetalKit.MTKView

<pre style='color: green'>
public class MTKView : AppKit.NSView, AppKit.INSAppearanceCustomization, AppKit.INSDraggingDestination, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MTKView (Foundation.NSCoder coder);
	protected MTKView (Foundation.NSObjectFlag t);
	protected MTKView (IntPtr handle);
	public MTKView (CoreGraphics.CGRect frameRect, Metal.IMTLDevice device);
	// properties
	public virtual bool AutoResizeDrawable { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Metal.MTLClearColor ClearColor { get; set; }
	public virtual double ClearDepth { get; set; }
	public virtual uint ClearStencil { get; set; }
	public virtual Metal.MTLPixelFormat ColorPixelFormat { get; set; }
	public virtual CoreAnimation.ICAMetalDrawable CurrentDrawable { get; }
	public virtual Metal.MTLRenderPassDescriptor CurrentRenderPassDescriptor { get; }
	public IMTKViewDelegate Delegate { get; set; }
	public virtual Metal.MTLPixelFormat DepthStencilPixelFormat { get; set; }
	public virtual Metal.IMTLTexture DepthStencilTexture { get; }
	public virtual Metal.IMTLDevice Device { get; set; }
	public virtual CoreGraphics.CGSize DrawableSize { get; set; }
	public virtual bool EnableSetNeedsDisplay { get; set; }
	public virtual bool FramebufferOnly { get; set; }
	public virtual Metal.IMTLTexture MultisampleColorTexture { get; }
	public virtual bool Paused { get; set; }
	public virtual nint PreferredFramesPerSecond { get; set; }
	public virtual bool PresentsWithTransaction { get; set; }
	public virtual uint SampleCount { get; set; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Draw ();
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void ReleaseDrawables ();
}
</pre>

### New Type MetalKit.MTKViewDelegate

<pre style='color: green'>
public abstract class MTKViewDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMTKViewDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MTKViewDelegate ();
	protected MTKViewDelegate (Foundation.NSObjectFlag t);
	protected MTKViewDelegate (IntPtr handle);
	// methods
	public virtual void Draw (MTKView view);
	public virtual void DrawableSizeWillChange (MTKView view, CoreGraphics.CGSize size);
}
</pre>

## New Namespace ModelIO

### New Type ModelIO.IMDLComponent

<pre style='color: green'>
public interface IMDLComponent : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ModelIO.IMDLMeshBuffer

<pre style='color: green'>
public interface IMDLMeshBuffer : Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MDLMeshBufferMap Map { get; }
	// methods
	public virtual void FillData (Foundation.NSData data, uint offset);
}
</pre>

### New Type ModelIO.IMDLMeshBufferAllocator

<pre style='color: green'>
public interface IMDLMeshBufferAllocator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IMDLMeshBuffer CreateBuffer (Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (IMDLMeshBufferZone zone, Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone CreateZone (uint capacity);
	public virtual IMDLMeshBufferZone CreateZone (Foundation.NSNumber[] sizes, Foundation.NSNumber[] types);
}
</pre>

### New Type ModelIO.IMDLMeshBufferZone

<pre style='color: green'>
public interface IMDLMeshBufferZone : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type ModelIO.IMDLNamed

<pre style='color: green'>
public interface IMDLNamed : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual string Name { get; set; }
}
</pre>

### New Type ModelIO.IMDLObjectContainerComponent

<pre style='color: green'>
public interface IMDLObjectContainerComponent : IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.IMDLTransformComponent

<pre style='color: green'>
public interface IMDLTransformComponent : IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
}
</pre>

### New Type ModelIO.MDLAreaLight

<pre style='color: green'>
public class MDLAreaLight : ModelIO.MDLPhysicallyPlausibleLight, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLAreaLight (Foundation.NSObjectFlag t);
	protected MDLAreaLight (IntPtr handle);
	// properties
	public virtual float AreaRadius { get; set; }
	public virtual float Aspect { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2 SuperEllipticPower { get; set; }
}
</pre>

### New Type ModelIO.MDLAsset

<pre style='color: green'>
public class MDLAsset : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLAsset ();
	protected MDLAsset (Foundation.NSObjectFlag t);
	public MDLAsset (Foundation.NSUrl url);
	protected MDLAsset (IntPtr handle);
	public MDLAsset (Foundation.NSUrl url, MDLVertexDescriptor vertexDescriptor, IMDLMeshBufferAllocator bufferAllocator);
	public MDLAsset (Foundation.NSUrl url, MDLVertexDescriptor vertexDescriptor, IMDLMeshBufferAllocator bufferAllocator, bool preserveTopology, out Foundation.NSError error);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public virtual IMDLMeshBufferAllocator BufferAllocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual double EndTime { get; set; }
	public virtual double FrameInterval { get; set; }
	public MDLObject Item { get; }
	public virtual double StartTime { get; set; }
	public virtual Foundation.NSUrl Url { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	public static bool CanExportFileExtension (string extension);
	public static bool CanImportFileExtension (string extension);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual bool ExportAssetToUrl (Foundation.NSUrl url, out Foundation.NSError error);
	public static MDLAsset FromScene (SceneKit.SCNScene scene);
	public virtual MDLAxisAlignedBoundingBox GetBoundingBox (double atTime);
	public virtual MDLObject GetObject (uint index);
	public virtual MDLObject GetObjectAtIndexedSubscript (uint index);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.MDLAxisAlignedBoundingBox

<pre style='color: green'>
public struct MDLAxisAlignedBoundingBox {
	// constructors
	public MDLAxisAlignedBoundingBox (OpenTK.Vector3 maxBounds, OpenTK.Vector3 minBounds);
	// fields
	public OpenTK.Vector3 MaxBounds;
	public OpenTK.Vector3 MinBounds;
}
</pre>

### New Type ModelIO.MDLCamera

<pre style='color: green'>
public class MDLCamera : ModelIO.MDLObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLCamera ();
	protected MDLCamera (Foundation.NSObjectFlag t);
	protected MDLCamera (IntPtr handle);
	// properties
	public virtual uint ApertureBladeCount { get; set; }
	public virtual float BarrelDistortion { get; set; }
	public virtual float ChromaticAberration { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector3 Exposure { get; set; }
	public virtual OpenTK.Vector2 ExposureCompression { get; set; }
	public virtual float FarVisibilityDistance { get; set; }
	public virtual float FieldOfView { get; set; }
	public virtual float FisheyeDistortion { get; set; }
	public virtual OpenTK.Vector3 Flash { get; set; }
	public virtual float FocalLength { get; set; }
	public virtual float FocusDistance { get; set; }
	public virtual float FStop { get; set; }
	public virtual float MaximumCircleOfConfusion { get; set; }
	public virtual float NearVisibilityDistance { get; set; }
	public virtual float OpticalVignetting { get; set; }
	public virtual OpenTK.Matrix4 ProjectionMatrix { get; }
	public virtual float SensorAspect { get; set; }
	public virtual OpenTK.Vector2 SensorEnlargement { get; set; }
	public virtual OpenTK.Vector2 SensorShift { get; set; }
	public virtual float SensorVerticalAperture { get; set; }
	public virtual double ShutterOpenInterval { get; set; }
	public virtual float WorldToMetersConversionScale { get; set; }
	// methods
	public virtual MDLTexture BokehKernelWithSize (OpenTK.Vector2i size);
	public virtual void FrameBoundingBox (MDLAxisAlignedBoundingBox boundingBox, bool setNearAndFar);
	public static MDLCamera FromSceneCamera (SceneKit.SCNCamera sceneCamera);
	public virtual void LookAt (OpenTK.Vector3 focusPosition);
	public virtual void LookAt (OpenTK.Vector3 focusPosition, OpenTK.Vector3 cameraPosition);
	public virtual OpenTK.Vector3 RayTo (OpenTK.Vector2i pixel, OpenTK.Vector2i size);
}
</pre>

### New Type ModelIO.MDLCheckerboardTexture

<pre style='color: green'>
public class MDLCheckerboardTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLCheckerboardTexture (Foundation.NSObjectFlag t);
	protected MDLCheckerboardTexture (IntPtr handle);
	public MDLCheckerboardTexture (float divisions, string name, OpenTK.Vector2i dimensions, int channelCount, MDLTextureChannelEncoding channelEncoding, CoreGraphics.CGColor color1, CoreGraphics.CGColor color2);
	public MDLCheckerboardTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGColor Color1 { get; set; }
	public virtual CoreGraphics.CGColor Color2 { get; set; }
	public virtual float Divisions { get; set; }
}
</pre>

### New Type ModelIO.MDLColorSwatchTexture

<pre style='color: green'>
public class MDLColorSwatchTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLColorSwatchTexture (Foundation.NSObjectFlag t);
	protected MDLColorSwatchTexture (IntPtr handle);
	public MDLColorSwatchTexture (CoreGraphics.CGColor color1, CoreGraphics.CGColor color2, string name, OpenTK.Vector2i textureDimensions);
	public MDLColorSwatchTexture (float colorTemperature1, float colorTemperature2, string name, OpenTK.Vector2i textureDimensions);
	public MDLColorSwatchTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type ModelIO.MDLGeometryType

<pre style='color: green'>
[Serializable]
public enum MDLGeometryType {
	Lines = 1,
	Points = 0,
	Quads = 4,
	Triangles = 2,
	TriangleStrips = 3,
	VariableTopology = 5,
}
</pre>

### New Type ModelIO.MDLIndexBitDepth

<pre style='color: green'>
[Serializable]
public enum MDLIndexBitDepth {
	Invalid = 0,
	UInt16 = 16,
	UInt32 = 32,
	UInt8 = 8,
}
</pre>

### New Type ModelIO.MDLLight

<pre style='color: green'>
public class MDLLight : ModelIO.MDLObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLLight ();
	protected MDLLight (Foundation.NSObjectFlag t);
	protected MDLLight (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLLightType LightType { get; set; }
	// methods
	public static MDLLight FromSceneLight (SceneKit.SCNLight sceneLight);
	public virtual CoreGraphics.CGColor GetIrradiance (OpenTK.Vector3 point);
	public virtual CoreGraphics.CGColor GetIrradiance (OpenTK.Vector3 point, CoreGraphics.CGColorSpace colorSpace);
}
</pre>

### New Type ModelIO.MDLLightProbe

<pre style='color: green'>
public class MDLLightProbe : ModelIO.MDLLight, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLLightProbe ();
	protected MDLLightProbe (Foundation.NSObjectFlag t);
	protected MDLLightProbe (IntPtr handle);
	public MDLLightProbe (MDLTexture reflectiveTexture, MDLTexture irradianceTexture);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTexture IrradianceTexture { get; }
	public virtual MDLTexture ReflectiveTexture { get; }
	public virtual Foundation.NSData SphericalHarmonicsCoefficients { get; }
	public virtual uint SphericalHarmonicsLevel { get; }
	// methods
	public static MDLLightProbe Create (nint textureSize, MDLTransform transform, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, MDLTexture reflectiveCubemap, MDLTexture irradianceCubemap);
	protected override void Dispose (bool disposing);
	public virtual void GenerateSphericalHarmonicsFromIrradiance (uint sphericalHarmonicsLevel);
}
</pre>

### New Type ModelIO.MDLLightType

<pre style='color: green'>
[Serializable]
public enum MDLLightType {
	Ambient = 1,
	Directional = 2,
	DiscArea = 6,
	Environment = 11,
	Linear = 5,
	Photometric = 9,
	Point = 4,
	Probe = 10,
	RectangularArea = 7,
	Spot = 3,
	SuperElliptical = 8,
	Unknown = 0,
}
</pre>

### New Type ModelIO.MDLMaterial

<pre style='color: green'>
public class MDLMaterial : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMaterial ();
	protected MDLMaterial (Foundation.NSObjectFlag t);
	protected MDLMaterial (IntPtr handle);
	public MDLMaterial (string name, MDLScatteringFunction scatteringFunction);
	// properties
	public virtual MDLMaterial BaseMaterial { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual string Name { get; set; }
	public virtual MDLScatteringFunction ScatteringFunction { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static MDLMaterial FromSceneMaterial (SceneKit.SCNMaterial material);
	public virtual MDLMaterialProperty GetProperty (MDLMaterialSemantic semantic);
	public virtual MDLMaterialProperty GetProperty (string name);
	public virtual void RemoveAllProperties ();
	public virtual void RemoveProperty (MDLMaterialProperty property);
	public virtual void SetProperty (MDLMaterialProperty property);
}
</pre>

### New Type ModelIO.MDLMaterialMipMapFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialMipMapFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type ModelIO.MDLMaterialProperty

<pre style='color: green'>
public class MDLMaterialProperty : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLMaterialProperty (Foundation.NSObjectFlag t);
	protected MDLMaterialProperty (IntPtr handle);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, CoreGraphics.CGColor color);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, Foundation.NSUrl url);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, MDLTextureSampler textureSampler);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Matrix4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector2 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector3 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Vector4 value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, float value);
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, string stringValue);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGColor Color { get; set; }
	public virtual OpenTK.Vector2 Float2Value { get; set; }
	public virtual OpenTK.Vector3 Float3Value { get; set; }
	public virtual OpenTK.Vector4 Float4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual OpenTK.Matrix4 Matrix4x4 { get; set; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialSemantic Semantic { get; set; }
	public virtual string StringValue { get; set; }
	public virtual MDLTextureSampler TextureSamplerValue { get; set; }
	public virtual MDLMaterialPropertyType Type { get; }
	public virtual Foundation.NSUrl UrlValue { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetProperties (MDLMaterialProperty property);
}
</pre>

### New Type ModelIO.MDLMaterialPropertyType

<pre style='color: green'>
[Serializable]
public enum MDLMaterialPropertyType {
	Color = 4,
	Float = 5,
	Float2 = 6,
	Float3 = 7,
	Float4 = 8,
	Matrix44 = 9,
	None = 0,
	String = 1,
	Texture = 3,
	Url = 2,
}
</pre>

### New Type ModelIO.MDLMaterialSemantic

<pre style='color: green'>
[Serializable]
public enum MDLMaterialSemantic {
	AmbientOcclusion = 22,
	AmbientOcclusionScale = 23,
	Anisotropic = 7,
	AnisotropicRotation = 8,
	BaseColor = 0,
	Bump = 14,
	Clearcoat = 11,
	ClearcoatGloss = 12,
	Displacement = 20,
	DisplacementScale = 21,
	Emission = 13,
	InterfaceIndexOfRefraction = 16,
	MaterialIndexOfRefraction = 17,
	Metallic = 2,
	None = 32768,
	ObjectSpaceNormal = 18,
	Opacity = 15,
	Roughness = 6,
	Sheen = 9,
	SheenTint = 10,
	Specular = 3,
	SpecularExponent = 4,
	SpecularTint = 5,
	Subsurface = 1,
	TangentSpaceNormal = 19,
	UserDefined = 32769,
}
</pre>

### New Type ModelIO.MDLMaterialTextureFilterMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureFilterMode {
	Linear = 1,
	Nearest = 0,
}
</pre>

### New Type ModelIO.MDLMaterialTextureWrapMode

<pre style='color: green'>
[Serializable]
public enum MDLMaterialTextureWrapMode {
	Clamp = 0,
	Mirror = 2,
	Repeat = 1,
}
</pre>

### New Type ModelIO.MDLMesh

<pre style='color: green'>
public class MDLMesh : ModelIO.MDLObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMesh ();
	protected MDLMesh (Foundation.NSObjectFlag t);
	protected MDLMesh (IntPtr handle);
	public MDLMesh (IMDLMeshBuffer vertexBuffer, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	public MDLMesh (IMDLMeshBuffer[] vertexBuffers, uint vertexCount, MDLVertexDescriptor descriptor, MDLSubmesh[] submeshes);
	// properties
	public MDLVertexAttributeData AnisotropyVertexData { get; }
	public MDLVertexAttributeData BinormalVertexData { get; }
	public MDLVertexAttributeData BitangentVertexData { get; }
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public override IntPtr ClassHandle { get; }
	public MDLVertexAttributeData ColorVertexData { get; }
	public MDLVertexAttributeData EdgeCreaseVertexData { get; }
	public MDLVertexAttributeData JointIndicesVertexData { get; }
	public MDLVertexAttributeData JointWeightsVertexData { get; }
	public MDLVertexAttributeData NormalVertexData { get; }
	public MDLVertexAttributeData OcclusionValueVertexData { get; }
	public MDLVertexAttributeData PositionVertexData { get; }
	public MDLVertexAttributeData ShadingBasisUVertexData { get; }
	public MDLVertexAttributeData ShadingBasisVVertexData { get; }
	public MDLVertexAttributeData SubdivisionStencilVertexData { get; }
	public virtual Foundation.NSMutableArray&lt;MDLSubmesh&gt; Submeshes { get; }
	public MDLVertexAttributeData TangentVertexData { get; }
	public MDLVertexAttributeData TextureCoordinateVertexData { get; }
	public virtual IMDLMeshBuffer[] VertexBuffers { get; }
	public virtual uint VertexCount { get; }
	public virtual MDLVertexDescriptor VertexDescriptor { get; set; }
	// methods
	public virtual void AddAttribute (string name, MDLVertexFormat format);
	public virtual void AddNormals (string name, float creaseThreshold);
	public virtual void AddTangentBasis (string textureCoordinateAttributeName, string tangentAttributeName, string bitangentAttributeName);
	public virtual void AddTangentBasisWithNormals (string textureCoordinateAttributeName, string normalAttributeName, string tangentAttributeName);
	public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateCylindroid (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipsoid (OpenTK.Vector3 radii, uint radialSegments, uint verticalSegments, MDLGeometryType geometryType, bool inwardNormals, bool hemisphere, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateEllipticalCone (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateIcosahedron (float radius, bool inwardNormals, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreatePlane (OpenTK.Vector2 dimensions, OpenTK.Vector2i segments, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);
	public static MDLMesh CreateSubdividedMesh (MDLMesh mesh, uint submeshIndex, uint subdivisionLevels);
	protected override void Dispose (bool disposing);
	public static MDLMesh FromGeometry (SceneKit.SCNGeometry geometry);
	public virtual bool GenerateAmbientOcclusionTexture (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionTexture (OpenTK.Vector2i textureSize, nint raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateAmbientOcclusionVertexColors (nint raysPerSample, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateAmbientOcclusionVertexColors (float bakeQuality, float attenuationFactor, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual bool GenerateLightMapTexture (OpenTK.Vector2i textureSize, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapTexture (float bakeQuality, MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName, string materialPropertyName);
	public virtual bool GenerateLightMapVertexColors (MDLLight[] lightsToConsider, MDLObject[] objectsToConsider, string vertexAttributeName);
	public virtual void MakeVerticesUnique ();
}
</pre>

### New Type ModelIO.MDLMeshBuffer_Extensions

<pre style='color: green'>
public static class MDLMeshBuffer_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBuffer This);
	public static uint GetLength (IMDLMeshBuffer This);
	public static MDLMeshBufferType GetType (IMDLMeshBuffer This);
	public static IMDLMeshBufferZone GetZone (IMDLMeshBuffer This);
}
</pre>

### New Type ModelIO.MDLMeshBufferData

<pre style='color: green'>
public class MDLMeshBufferData : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, IMDLMeshBuffer, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMeshBufferData ();
	protected MDLMeshBufferData (Foundation.NSObjectFlag t);
	protected MDLMeshBufferData (IntPtr handle);
	public MDLMeshBufferData (MDLMeshBufferType type, Foundation.NSData data);
	public MDLMeshBufferData (MDLMeshBufferType type, uint length);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSData Data { get; }
	public virtual uint Length { get; }
	public virtual MDLMeshBufferMap Map { get; }
	public virtual MDLMeshBufferType Type { get; }
	public virtual IMDLMeshBufferZone Zone { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void FillData (Foundation.NSData data, uint offset);
}
</pre>

### New Type ModelIO.MDLMeshBufferDataAllocator

<pre style='color: green'>
public class MDLMeshBufferDataAllocator : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLMeshBufferAllocator, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMeshBufferDataAllocator ();
	protected MDLMeshBufferDataAllocator (Foundation.NSObjectFlag t);
	protected MDLMeshBufferDataAllocator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual IMDLMeshBuffer CreateBuffer (Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (IMDLMeshBufferZone zone, Foundation.NSData data, MDLMeshBufferType type);
	public virtual IMDLMeshBuffer CreateBuffer (IMDLMeshBufferZone zone, uint length, MDLMeshBufferType type);
	public virtual IMDLMeshBufferZone CreateZone (uint capacity);
	public virtual IMDLMeshBufferZone CreateZone (Foundation.NSNumber[] sizes, Foundation.NSNumber[] types);
}
</pre>

### New Type ModelIO.MDLMeshBufferMap

<pre style='color: green'>
public class MDLMeshBufferMap : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMeshBufferMap ();
	protected MDLMeshBufferMap (Foundation.NSObjectFlag t);
	protected MDLMeshBufferMap (IntPtr handle);
	public MDLMeshBufferMap (IntPtr bytes, System.Action deallocator);
	// properties
	public virtual IntPtr Bytes { get; }
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type ModelIO.MDLMeshBufferType

<pre style='color: green'>
[Serializable]
public enum MDLMeshBufferType {
	Index = 2,
	Vertex = 1,
}
</pre>

### New Type ModelIO.MDLMeshBufferZone_Extensions

<pre style='color: green'>
public static class MDLMeshBufferZone_Extensions {
	// methods
	public static IMDLMeshBufferAllocator GetAllocator (IMDLMeshBufferZone This);
	public static uint GetCapacity (IMDLMeshBufferZone This);
}
</pre>

### New Type ModelIO.MDLMeshBufferZoneDefault

<pre style='color: green'>
public class MDLMeshBufferZoneDefault : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLMeshBufferZone, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLMeshBufferZoneDefault ();
	protected MDLMeshBufferZoneDefault (Foundation.NSObjectFlag t);
	protected MDLMeshBufferZoneDefault (IntPtr handle);
	// properties
	public virtual IMDLMeshBufferAllocator Allocator { get; }
	public virtual uint Capacity { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLNoiseTexture

<pre style='color: green'>
public class MDLNoiseTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLNoiseTexture (Foundation.NSObjectFlag t);
	protected MDLNoiseTexture (IntPtr handle);
	public MDLNoiseTexture (float smoothness, string name, OpenTK.Vector2i textureDimensions, MDLTextureChannelEncoding channelEncoding);
	public MDLNoiseTexture (float smoothness, string name, OpenTK.Vector2i textureDimensions, int channelCount, MDLTextureChannelEncoding channelEncoding, bool grayscale);
	public MDLNoiseTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type ModelIO.MDLNormalMapTexture

<pre style='color: green'>
public class MDLNormalMapTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLNormalMapTexture (Foundation.NSObjectFlag t);
	protected MDLNormalMapTexture (IntPtr handle);
	public MDLNormalMapTexture (MDLTexture sourceTexture, string name, float smoothness, float contrast);
	public MDLNormalMapTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type ModelIO.MDLObject

<pre style='color: green'>
public class MDLObject : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLObject ();
	protected MDLObject (Foundation.NSObjectFlag t);
	protected MDLObject (IntPtr handle);
	// properties
	public virtual IMDLObjectContainerComponent Children { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual MDLObject Parent { get; set; }
	public virtual IMDLTransformComponent Transform { get; set; }
	// methods
	public virtual void AddChild (MDLObject child);
	protected override void Dispose (bool disposing);
	public static MDLObject FromNode (SceneKit.SCNNode node);
	public virtual MDLAxisAlignedBoundingBox GetBoundingBox (double atTime);
	public virtual IMDLComponent IsComponentConforming (ObjCRuntime.Protocol protocol);
	public virtual void SetComponent (IMDLComponent component, ObjCRuntime.Protocol protocol);
}
</pre>

### New Type ModelIO.MDLObjectContainer

<pre style='color: green'>
public class MDLObjectContainer : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLComponent, IMDLObjectContainerComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLObjectContainer ();
	protected MDLObjectContainer (Foundation.NSObjectFlag t);
	protected MDLObjectContainer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLObject[] Objects { get; }
	// methods
	public virtual void AddObject (MDLObject object);
	protected override void Dispose (bool disposing);
	public virtual void RemoveObject (MDLObject object);
}
</pre>

### New Type ModelIO.MDLPhotometricLight

<pre style='color: green'>
public class MDLPhotometricLight : ModelIO.MDLPhysicallyPlausibleLight, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLPhotometricLight ();
	protected MDLPhotometricLight (Foundation.NSObjectFlag t);
	public MDLPhotometricLight (Foundation.NSUrl url);
	protected MDLPhotometricLight (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTexture LightCubeMap { get; }
	public virtual Foundation.NSData SphericalHarmonicsCoefficients { get; }
	public virtual uint SphericalHarmonicsLevel { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void GenerateCubemap (uint textureSize);
	public virtual void GenerateSphericalHarmonics (uint sphericalHarmonicsLevel);
}
</pre>

### New Type ModelIO.MDLPhysicallyPlausibleLight

<pre style='color: green'>
public class MDLPhysicallyPlausibleLight : ModelIO.MDLLight, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLPhysicallyPlausibleLight ();
	protected MDLPhysicallyPlausibleLight (Foundation.NSObjectFlag t);
	protected MDLPhysicallyPlausibleLight (IntPtr handle);
	// properties
	public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGColor Color { get; set; }
	public virtual float InnerConeAngle { get; set; }
	public virtual float Lumens { get; set; }
	public virtual float OuterConeAngle { get; set; }
	// methods
	public virtual void SetColor (float temperature);
}
</pre>

### New Type ModelIO.MDLPhysicallyPlausibleScatteringFunction

<pre style='color: green'>
public class MDLPhysicallyPlausibleScatteringFunction : ModelIO.MDLScatteringFunction, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLPhysicallyPlausibleScatteringFunction ();
	protected MDLPhysicallyPlausibleScatteringFunction (Foundation.NSObjectFlag t);
	protected MDLPhysicallyPlausibleScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty Anisotropic { get; }
	public virtual MDLMaterialProperty AnisotropicRotation { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Clearcoat { get; }
	public virtual MDLMaterialProperty ClearcoatGloss { get; }
	public virtual MDLMaterialProperty Metallic { get; }
	public virtual MDLMaterialProperty Roughness { get; }
	public virtual MDLMaterialProperty Sheen { get; }
	public virtual MDLMaterialProperty SheenTint { get; }
	public virtual MDLMaterialProperty SpecularAmount { get; }
	public virtual MDLMaterialProperty SpecularTint { get; }
	public virtual MDLMaterialProperty Subsurface { get; }
	public virtual nint Version { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLScatteringFunction

<pre style='color: green'>
public class MDLScatteringFunction : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLScatteringFunction ();
	protected MDLScatteringFunction (Foundation.NSObjectFlag t);
	protected MDLScatteringFunction (IntPtr handle);
	// properties
	public virtual MDLMaterialProperty AmbientOcclusion { get; }
	public virtual MDLMaterialProperty AmbientOcclusionScale { get; }
	public virtual MDLMaterialProperty BaseColor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialProperty Emission { get; }
	public virtual MDLMaterialProperty InterfaceIndexOfRefraction { get; }
	public virtual MDLMaterialProperty MaterialIndexOfRefraction { get; }
	public virtual string Name { get; set; }
	public virtual MDLMaterialProperty Normal { get; }
	public virtual MDLMaterialProperty Specular { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLSkyCubeTexture

<pre style='color: green'>
public class MDLSkyCubeTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLSkyCubeTexture (Foundation.NSObjectFlag t);
	protected MDLSkyCubeTexture (IntPtr handle);
	public MDLSkyCubeTexture (string name, MDLTextureChannelEncoding channelEncoding, OpenTK.Vector2i textureDimensions, float turbidity, float sunElevation, float upperAtmosphereScattering, float groundAlbedo);
	public MDLSkyCubeTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public virtual float Brightness { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual float Contrast { get; set; }
	public virtual float Exposure { get; set; }
	public virtual float Gamma { get; set; }
	public virtual float GroundAlbedo { get; set; }
	public virtual CoreGraphics.CGColor GroundColor { get; set; }
	public virtual OpenTK.Vector2 HighDynamicRangeCompression { get; set; }
	public virtual float HorizonElevation { get; set; }
	public virtual float Saturation { get; set; }
	public virtual float SunElevation { get; set; }
	public virtual float Turbidity { get; set; }
	public virtual float UpperAtmosphereScattering { get; set; }
	// methods
	public virtual void UpdateTexture ();
}
</pre>

### New Type ModelIO.MDLStereoscopicCamera

<pre style='color: green'>
public class MDLStereoscopicCamera : ModelIO.MDLCamera, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLStereoscopicCamera ();
	protected MDLStereoscopicCamera (Foundation.NSObjectFlag t);
	protected MDLStereoscopicCamera (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual float InterPupillaryDistance { get; set; }
	public virtual OpenTK.Matrix4 LeftProjectionMatrix { get; }
	public virtual float LeftVergence { get; set; }
	public virtual OpenTK.Matrix4 LeftViewMatrix { get; }
	public virtual float Overlap { get; set; }
	public virtual OpenTK.Matrix4 RightProjectionMatrix { get; }
	public virtual float RightVergence { get; set; }
	public virtual OpenTK.Matrix4 RightViewMatrix { get; }
}
</pre>

### New Type ModelIO.MDLSubmesh

<pre style='color: green'>
public class MDLSubmesh : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLSubmesh ();
	protected MDLSubmesh (Foundation.NSObjectFlag t);
	protected MDLSubmesh (IntPtr handle);
	public MDLSubmesh (MDLSubmesh indexBuffer, MDLIndexBitDepth indexType, MDLGeometryType geometryType);
	public MDLSubmesh (IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryType geometryType, MDLMaterial material);
	public MDLSubmesh (string name, IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryType geometryType, MDLMaterial material);
	public MDLSubmesh (string name, IMDLMeshBuffer indexBuffer, uint indexCount, MDLIndexBitDepth indexType, MDLGeometryType geometryType, MDLMaterial material, MDLSubmeshTopology topology);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLGeometryType GeometryType { get; }
	public virtual IMDLMeshBuffer IndexBuffer { get; }
	public virtual uint IndexCount { get; }
	public virtual MDLIndexBitDepth IndexType { get; }
	public virtual MDLMaterial Material { get; set; }
	public virtual string Name { get; set; }
	public virtual MDLSubmeshTopology Topology { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static MDLSubmesh FromGeometryElement (SceneKit.SCNGeometryElement element);
}
</pre>

### New Type ModelIO.MDLSubmeshTopology

<pre style='color: green'>
public class MDLSubmeshTopology : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLSubmeshTopology ();
	protected MDLSubmeshTopology (Foundation.NSObjectFlag t);
	protected MDLSubmeshTopology (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint EdgeCreaseCount { get; set; }
	public virtual IMDLMeshBuffer EdgeCreaseIndices { get; set; }
	public virtual IMDLMeshBuffer EdgeCreases { get; set; }
	public virtual uint FaceCount { get; set; }
	public virtual IMDLMeshBuffer FaceTopology { get; set; }
	public virtual uint HoleCount { get; set; }
	public virtual IMDLMeshBuffer Holes { get; set; }
	public virtual uint VertexCreaseCount { get; set; }
	public virtual IMDLMeshBuffer VertexCreaseIndices { get; set; }
	public virtual IMDLMeshBuffer VertexCreases { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLTexture

<pre style='color: green'>
public class MDLTexture : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLTexture ();
	protected MDLTexture (Foundation.NSObjectFlag t);
	protected MDLTexture (IntPtr handle);
	public MDLTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public virtual uint ChannelCount { get; }
	public virtual MDLTextureChannelEncoding ChannelEncoding { get; }
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector2i Dimensions { get; }
	public virtual bool IsCube { get; set; }
	public virtual uint MipLevelCount { get; }
	public virtual string Name { get; set; }
	public virtual nint RowStride { get; }
	// methods
	public static MDLTexture CreateIrradianceTextureCube (MDLTexture texture, string name, OpenTK.Vector2i dimensions);
	public static MDLTexture CreateIrradianceTextureCube (MDLTexture reflectiveTexture, string name, OpenTK.Vector2i dimensions, float roughness);
	public static MDLTexture CreateTextureCube (string[] imageNames);
	public static MDLTexture CreateTextureCube (string[] imageNames, Foundation.NSBundle bundleOrNil);
	public static MDLTexture FromBundle (string name);
	public static MDLTexture FromBundle (string name, Foundation.NSBundle bundleOrNil);
	public virtual CoreGraphics.CGImage GetImageFromTexture ();
	public virtual Foundation.NSData GetTexelDataWithBottomLeftOrigin ();
	public virtual Foundation.NSData GetTexelDataWithBottomLeftOrigin (nint mipLevel, bool create);
	public virtual Foundation.NSData GetTexelDataWithTopLeftOrigin ();
	public virtual Foundation.NSData GetTexelDataWithTopLeftOrigin (nint mipLevel, bool create);
	public virtual bool WriteToUrl (Foundation.NSUrl url);
	public virtual bool WriteToUrl (Foundation.NSUrl url, string type);
}
</pre>

### New Type ModelIO.MDLTextureChannelEncoding

<pre style='color: green'>
[Serializable]
public enum MDLTextureChannelEncoding {
	Float16 = 258,
	Float32 = 260,
	UInt16 = 2,
	UInt24 = 3,
	UInt32 = 4,
	UInt8 = 1,
}
</pre>

### New Type ModelIO.MDLTextureFilter

<pre style='color: green'>
public class MDLTextureFilter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLTextureFilter ();
	protected MDLTextureFilter (Foundation.NSObjectFlag t);
	protected MDLTextureFilter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLMaterialTextureFilterMode MagFilter { get; set; }
	public virtual MDLMaterialTextureFilterMode MinFilter { get; set; }
	public virtual MDLMaterialMipMapFilterMode MipFilter { get; set; }
	public virtual MDLMaterialTextureWrapMode RWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode SWrapMode { get; set; }
	public virtual MDLMaterialTextureWrapMode TWrapMode { get; set; }
}
</pre>

### New Type ModelIO.MDLTextureSampler

<pre style='color: green'>
public class MDLTextureSampler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLTextureSampler ();
	protected MDLTextureSampler (Foundation.NSObjectFlag t);
	protected MDLTextureSampler (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MDLTextureFilter HardwareFilter { get; set; }
	public virtual MDLTexture Texture { get; set; }
	public virtual MDLTransform Transform { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLTransform

<pre style='color: green'>
public class MDLTransform : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLComponent, IMDLTransformComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLTransform ();
	protected MDLTransform (Foundation.NSObjectFlag t);
	public MDLTransform (IMDLTransformComponent component);
	public MDLTransform (OpenTK.Matrix4 matrix);
	protected MDLTransform (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix4 Matrix { get; set; }
	public virtual double MaximumTime { get; }
	public virtual double MinimumTime { get; }
	public virtual OpenTK.Vector3 Rotation { get; set; }
	public virtual OpenTK.Vector3 Scale { get; set; }
	public virtual OpenTK.Vector3 Shear { get; set; }
	public virtual OpenTK.Vector3 Translation { get; set; }
	// methods
	public static OpenTK.Matrix4 CreateGlobalTransform (MDLObject obj, double atTime);
	public virtual OpenTK.Matrix4 GetLocalTransform (double atTime);
	public virtual OpenTK.Vector3 GetRotation (double atTime);
	public virtual OpenTK.Matrix4 GetRotationMatrix (double atTime);
	public virtual OpenTK.Vector3 GetScale (double atTime);
	public virtual OpenTK.Vector3 GetShear (double atTime);
	public virtual OpenTK.Vector3 GetTranslation (double atTime);
	public virtual void SetIdentity ();
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform);
	public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);
	public virtual void SetRotation (OpenTK.Vector3 rotation, double time);
	public virtual void SetScale (OpenTK.Vector3 scale, double time);
	public virtual void SetShear (OpenTK.Vector3 scale, double time);
	public virtual void SetTranslation (OpenTK.Vector3 translation, double time);
}
</pre>

### New Type ModelIO.MDLTransformComponent_Extensions

<pre style='color: green'>
public static class MDLTransformComponent_Extensions {
	// methods
	public static OpenTK.Matrix4 GetLocalTransform (IMDLTransformComponent This, double atTime);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform);
	public static void SetLocalTransform (IMDLTransformComponent This, OpenTK.Matrix4 transform, double time);
}
</pre>

### New Type ModelIO.MDLUrlTexture

<pre style='color: green'>
public class MDLUrlTexture : ModelIO.MDLTexture, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLUrlTexture (Foundation.NSObjectFlag t);
	protected MDLUrlTexture (IntPtr handle);
	public MDLUrlTexture (Foundation.NSUrl url, string name);
	public MDLUrlTexture (Foundation.NSData pixelData, bool topLeftOrigin, string name, OpenTK.Vector2i dimensions, nint rowStride, uint channelCount, MDLTextureChannelEncoding channelEncoding, bool isCube);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSUrl Url { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLVertexAttribute

<pre style='color: green'>
public class MDLVertexAttribute : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLVertexAttribute ();
	protected MDLVertexAttribute (Foundation.NSObjectFlag t);
	protected MDLVertexAttribute (IntPtr handle);
	public MDLVertexAttribute (string name, MDLVertexFormat format, uint offset, uint bufferIndex);
	// properties
	public virtual uint BufferIndex { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual OpenTK.Vector4 InitializationValue { get; set; }
	public virtual string Name { get; set; }
	public virtual uint Offset { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type ModelIO.MDLVertexAttributeData

<pre style='color: green'>
public class MDLVertexAttributeData : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLVertexAttributeData (Foundation.NSObjectFlag t);
	protected MDLVertexAttributeData (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IntPtr DataStart { get; set; }
	public virtual MDLVertexFormat Format { get; set; }
	public virtual MDLMeshBufferMap Map { get; set; }
	public virtual uint Stride { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type ModelIO.MDLVertexAttributes

<pre style='color: green'>
public static class MDLVertexAttributes {
	// properties
	public static Foundation.NSString Anisotropy { get; }
	public static Foundation.NSString Binormal { get; }
	public static Foundation.NSString Bitangent { get; }
	public static Foundation.NSString Color { get; }
	public static Foundation.NSString EdgeCrease { get; }
	public static Foundation.NSString JointIndices { get; }
	public static Foundation.NSString JointWeights { get; }
	public static Foundation.NSString Normal { get; }
	public static Foundation.NSString OcclusionValue { get; }
	public static Foundation.NSString Position { get; }
	public static Foundation.NSString ShadingBasisU { get; }
	public static Foundation.NSString ShadingBasisV { get; }
	public static Foundation.NSString SubdivisionStencil { get; }
	public static Foundation.NSString Tangent { get; }
	public static Foundation.NSString TextureCoordinate { get; }
}
</pre>

### New Type ModelIO.MDLVertexBufferLayout

<pre style='color: green'>
public class MDLVertexBufferLayout : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLVertexBufferLayout ();
	protected MDLVertexBufferLayout (Foundation.NSObjectFlag t);
	protected MDLVertexBufferLayout (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint Stride { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
</pre>

### New Type ModelIO.MDLVertexDescriptor

<pre style='color: green'>
public class MDLVertexDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MDLVertexDescriptor ();
	protected MDLVertexDescriptor (Foundation.NSObjectFlag t);
	public MDLVertexDescriptor (MDLVertexDescriptor vertexDescriptor);
	protected MDLVertexDescriptor (IntPtr handle);
	// properties
	public virtual Foundation.NSMutableArray&lt;MDLVertexAttribute&gt; Attributes { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSMutableArray&lt;MDLVertexBufferLayout&gt; Layouts { get; set; }
	// methods
	public virtual void AddOrReplaceAttribute (MDLVertexAttribute attribute);
	public virtual MDLVertexAttribute AttributeNamed (string name);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static MDLVertexDescriptor FromMetal (Metal.MTLVertexDescriptor descriptor);
	public virtual void Reset ();
	public virtual void SetPackedOffsets ();
	public virtual void SetPackedStrides ();
}
</pre>

### New Type ModelIO.MDLVertexFormat

<pre style='color: green'>
[Serializable]
public enum MDLVertexFormat {
	Char = 131073,
	Char2 = 131074,
	Char2Normalized = 262146,
	Char3 = 131075,
	Char3Normalized = 262147,
	Char4 = 131076,
	Char4Normalized = 262148,
	CharBits = 131072,
	CharNormalized = 262145,
	CharNormalizedBits = 262144,
	Float = 786433,
	Float2 = 786434,
	Float3 = 786435,
	Float4 = 786436,
	FloatBits = 786432,
	Half = 720897,
	Half2 = 720898,
	Half3 = 720899,
	Half4 = 720900,
	HalfBits = 720896,
	Int = 655361,
	Int1010102Normalized = 659460,
	Int2 = 655362,
	Int3 = 655363,
	Int4 = 655364,
	IntBits = 655360,
	Invalid = 0,
	PackedBits = 4096,
	Short = 393217,
	Short2 = 393218,
	Short2Normalized = 524290,
	Short3 = 393219,
	Short3Normalized = 524291,
	Short4 = 393220,
	Short4Normalized = 524292,
	ShortBits = 393216,
	ShortNormalized = 524289,
	ShortNormalizedBits = 524288,
	UChar = 65537,
	UChar2 = 65538,
	UChar2Normalized = 196610,
	UChar3 = 65539,
	UChar3Normalized = 196611,
	UChar4 = 65540,
	UChar4Normalized = 196612,
	UCharBits = 65536,
	UCharNormalized = 196609,
	UCharNormalizedBits = 196608,
	UInt = 589825,
	UInt1010102Normalized = 593924,
	UInt2 = 589826,
	UInt3 = 589827,
	UInt4 = 589828,
	UIntBits = 589824,
	UShort = 327681,
	UShort2 = 327682,
	UShort2Normalized = 458754,
	UShort3 = 327683,
	UShort3Normalized = 458755,
	UShort4 = 327684,
	UShort4Normalized = 458756,
	UShortBits = 327680,
	UShortNormalized = 458753,
	UShortNormalizedBits = 458752,
}
</pre>

### New Type ModelIO.MDLVertexFormatExtensions

<pre style='color: green'>
public static class MDLVertexFormatExtensions {
	// methods
	public static Metal.MTLVertexFormat ToMetalVertexFormat (MDLVertexFormat vertexFormat);
}
</pre>

### New Type ModelIO.MDLVoxelArray

<pre style='color: green'>
public class MDLVoxelArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MDLVoxelArray (Foundation.NSObjectFlag t);
	protected MDLVoxelArray (IntPtr handle);
	public MDLVoxelArray (Foundation.NSData voxelData, MDLAxisAlignedBoundingBox boundingBox, float voxelExtent);
	public MDLVoxelArray (MDLAsset asset, int divisions, int interiorShells, int exteriorShells, float patchRadius);
	public MDLVoxelArray (MDLAsset asset, int divisions, float interiorNBWidth, float exteriorNBWidth, float patchRadius);
	// properties
	public virtual MDLAxisAlignedBoundingBox BoundingBox { get; }
	public override IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual MDLVoxelIndexExtent VoxelIndexExtent { get; }
	// methods
	public virtual MDLMesh CreateMesh (IMDLMeshBufferAllocator allocator);
	public virtual void DifferenceWith (MDLVoxelArray voxels);
	public virtual OpenTK.Vector4i GetIndex (OpenTK.Vector3 spatiallocation);
	public virtual OpenTK.Vector3 GetSpatialLocation (OpenTK.Vector4i index);
	public virtual MDLAxisAlignedBoundingBox GetVoxelBoundingBox (OpenTK.Vector4i index);
	public virtual Foundation.NSData GetVoxelIndices ();
	public virtual Foundation.NSData GetVoxels (MDLVoxelIndexExtent withinExtent);
	public virtual void IntersectWith (MDLVoxelArray voxels);
	public virtual void SetVoxel (OpenTK.Vector4i index);
	public virtual void SetVoxels (MDLMesh mesh, int divisions, int interiorShells, int exteriorShells, float patchRadius);
	public virtual void SetVoxels (MDLMesh mesh, int divisions, float interiorNBWidth, float exteriorNBWidth, float patchRadius);
	public virtual void UnionWith (MDLVoxelArray voxels);
	public virtual bool VoxelExists (OpenTK.Vector4i atIndex, bool allowAnyX, bool allowAnyY, bool allowAnyZ, bool allowAnyShell);
}
</pre>

### New Type ModelIO.MDLVoxelIndexExtent

<pre style='color: green'>
public struct MDLVoxelIndexExtent {
	// constructors
	public MDLVoxelIndexExtent (OpenTK.Vector4 minimumExtent, OpenTK.Vector4 maximumExtent);
	// fields
	public OpenTK.Vector4 MaximumExtent;
	public OpenTK.Vector4 MinimumExtent;
}
</pre>

## New Namespace SearchKit

### New Type SearchKit.SKDocument

<pre style='color: green'>
public class SKDocument : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKDocument (Foundation.NSUrl url);
	public SKDocument (string name, SKDocument parent, string scheme);
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
public class SKIndex : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public SKTextAnalysis AnalysisProperties { get; }
	public nint DocumentCount { get; }
	public virtual IntPtr Handle { get; }
	public nint MaximumBytesBeforeFlush { get; set; }
	public nint MaximumDocumentID { get; }
	public nint MaximumTermID { get; }
	// methods
	protected override void ~SKIndex ();
	public bool AddDocument (SKDocument document, string mimeHint, bool canReplace);
	public bool AddDocumentWithText (SKDocument document, string text, bool canReplace);
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
	public SKDocument GetDocument (nint documentId);
	public static void LoadDefaultExtractorPlugIns ();
	public bool MoveDocument (SKDocument document, SKDocument newParent);
	public bool RemoveDocument (SKDocument document);
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
public class SKSearch : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~SKSearch ();
	public void Cancel ();
	protected virtual void Dispose (bool disposing);
	public bool FindMatches (nint maxCount, ref nint[] ids, double waitTime, out nint foundCount);
	public bool FindMatches (nint maxCount, ref nint[] ids, ref float[] scores, double waitTime, out nint foundCount);
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
public class SKSummary : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IntPtr Handle { get; }
	public nint ParagraphCount { get; }
	public nint SentenceCount { get; }
	// methods
	protected override void ~SKSummary ();
	public static SKSummary Create (Foundation.NSString nsString);
	public static SKSummary Create (string text);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public string GetParagraph (nint idx);
	public string GetParagraphSummary (nint maxParagraphs);
	public nint GetParagraphSummaryInfo (nint maxNumParagraphsInSummary, nint[] rankOrderOfParagraphs, nint[] paragraphIndexOfParagraphs);
	public string GetSentence (nint idx);
	public string GetSentenceSummary (nint maxSentences);
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
