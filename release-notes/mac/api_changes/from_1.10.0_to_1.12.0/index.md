---
id: 3A405188-42AD-4EF5-9BCA-CFBD08BD393E
title: "From 1.10.0 to 1.12.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Added fields:

```
public static const string AccountsLibrary = "/System/Library/Frameworks/Accounts.framework/Accounts";
	public static const string AVKitLibrary = "/System/Library/Frameworks/AVKit.framework/AVKit";
	public static const string CloudKitLibrary = "/System/Library/Frameworks/CloudKit.framework/CloudKit";
	public static const string CryptoTokenKitLibrary = "/System/Library/Frameworks/CryptoTokenKit.framework/CryptoTokenKit";
	public static const string EventKitLibrary = "/System/Library/Frameworks/EventKit.framework/EventKit";
	public static const string FinderSyncLibrary = "/System/Library/Frameworks/FinderSync.framework/FinderSync";
	public static const string GameControllerLibrary = "/System/Library/Frameworks/GameController.framework/GameController";
	public static const string GLKitLibrary = "/System/Library/Frameworks/GLKit.framework/GLKit";
	public static const string HypervisorLibrary = "/System/Library/Frameworks/Hypervisor.framework/Hypervisor";
	public static const string IOBluetoothLibrary = "/System/Library/Frameworks/IOBluetooth.framework/IOBluetooth";
	public static const string IOBluetoothUILibrary = "/System/Library/Frameworks/IOBluetoothUI.framework/IOBluetoothUI";
	public static const string JavaScriptCoreLibrary = "/System/Library/Frameworks/JavaScriptCore.framework/JavaScriptCore";
	public static const string LocalAuthenticationLibrary = "/System/Library/Frameworks/LocalAuthentication.framework/LocalAuthentication";
	public static const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
	public static const string MediaAccessibilityLibrary = "/System/Library/Frameworks/MediaAccessibility.framework/MediaAccessibility";
	public static const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";
	public static const string NotificationCenterLibrary = "/System/Library/Frameworks/NotificationCenter.framework/NotificationCenter";
	public static const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";
	public static const string SpriteKitLibrary = "/System/Library/Frameworks/SpriteKit.framework/SpriteKit";
	public static const string Version = "1.12.0";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
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

### Type Changed: MonoMac.AppKit.NSActionCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSAlert

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSAlertDelegate

Added interfaces:

```
INSAlertDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual MonoMac.Foundation.NSString[] RunLoopModesForAnimating { get; }
```

### Type Changed: MonoMac.AppKit.NSAnimationContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSAnimationDelegate

Added interfaces:

```
INSAnimationDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSApplication

Added interfaces:

```
INSWindowRestoration
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSApplicationOcclusionState OcclusionState { get; }
```

Added event:

```
public event System.EventHandler<NSApplicationFailedEventArgs> FailedToContinueUserActivity;
```

Removed method:

```
[Obsolete ("Use MainMenu property")]
	public virtual void SetMainMenu (NSMenu aMenu);
```

Added method:

```
[Obsolete ("Use MainMenu property")]
	public void SetMainMenu (NSMenu aMenu);
```

### Type Changed: MonoMac.AppKit.NSApplicationDelegate

Added interfaces:

```
INSApplicationDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual void FailedToContinueUserActivity (NSApplication application, string userActivityType, MonoMac.Foundation.NSError error);
```

Obsoleted method:

```
[Obsolete ("Use DidFinishLaunching (NSNotification) instead")]
	public virtual void FinishedLaunching (MonoMac.Foundation.NSObject notification);
```

### Type Changed: MonoMac.AppKit.NSArrayController

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSATSTypesetter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSBezierPath

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSBitmapFormat

Added values:

```
BigEndian16Bit = 1024,
	BigEndian32Bit = 2048,
	LittleEndian16Bit = 256,
	LittleEndian32Bit = 512,
```

### Type Changed: MonoMac.AppKit.NSBitmapImageRep

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSBox

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSBrowser

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual void SetColumnResizingType (NSBrowserColumnResizingType columnResizingType);
```

Added method:

```
[Obsolete ("Use the ColumnResizingType property instead")]
	public void SetColumnResizingType (NSBrowserColumnResizingType columnResizingType);
```

### Type Changed: MonoMac.AppKit.NSBrowserCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSBrowserDelegate

Added interfaces:

```
INSBrowserDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSButton

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSButtonCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual void SetShowsStateBy (int aType);
```

Added method:

```
[Obsolete ("Use the ShowsStateBy property instead")]
	public void SetShowsStateBy (int aType);
```

### Type Changed: MonoMac.AppKit.NSCachedImageRep

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSCIImageRep

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSClipView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool AutomaticallyAdjustsContentInsets { get; set; }
	public virtual NSEdgeInsets ContentInsets { get; set; }
```

Added method:

```
public virtual System.Drawing.RectangleF ConstrainBoundsRect (System.Drawing.RectangleF proposedBounds);
```

### Type Changed: MonoMac.AppKit.NSCollectionView

Added interfaces:

```
INSDraggingDestination
	INSDraggingSource
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSCollectionViewDelegate

Added interfaces:

```
INSCollectionViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSCollectionViewItem

Added interfaces:

```
INSSeguePerforming
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSColor

Added interfaces:

```
INSPasteboardReading
	INSPasteboardWriting
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public static NSColor LabelColor { get; }
	public static NSColor QuaternaryLabelColor { get; }
	public static NSColor SecondaryLabelColor { get; }
	public static NSColor TertiaryLabelColor { get; }
```

Added methods:

```
public static NSColor FromHsba (float hue, float saturation, float brightness, float alpha);
	public static NSColor FromRgba (float red, float green, float blue, float alpha);
	public static NSColor FromWhite (float white, float alpha);
	public virtual MonoMac.Foundation.NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual MonoMac.Foundation.NSObject InitWithPasteboardPropertyList (MonoMac.Foundation.NSObject propertyList, string type);
```

### Type Changed: MonoMac.AppKit.NSColorList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSColorPanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual NSColorPanelFlags Mode { get; set; }
```

Added property:

```
public virtual NSColorPanelMode Mode { get; set; }
```

### Type Changed: MonoMac.AppKit.NSColorPicker

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSColorSpace

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSColorWell

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSComboBox

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

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

### Type Changed: MonoMac.AppKit.NSComboBoxCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual string CompletedString (string substring);
```

### Type Changed: MonoMac.AppKit.NSComboBoxCellDataSource

Added interfaces:

```
INSComboBoxCellDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSComboBoxDataSource

Added interfaces:

```
INSComboBoxDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSComposite

Added values:

```
Color = 27,
	ColorBurn = 20,
	ColorDodge = 19,
	Darken = 17,
	Difference = 23,
	Exclusion = 24,
	HardLight = 22,
	Hue = 25,
	Lighten = 18,
	Luminosity = 28,
	Multiply = 14,
	Overlay = 16,
	Saturation = 26,
	Screen = 15,
	SoftLight = 21,
```

### Type Changed: MonoMac.AppKit.NSControl

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual NSControlSize ControlSize { get; set; }
	public virtual bool Highlighted { get; set; }
	public virtual NSLineBreakMode LineBreakMode { get; set; }
	public virtual bool UsesSingleLineMode { get; set; }
```

Added methods:

```
public virtual void DrawWithExpansionFrame (System.Drawing.RectangleF cellFrame, NSView view);
	public virtual void EditWithFrame (System.Drawing.RectangleF aRect, NSText textObj, MonoMac.Foundation.NSObject anObject, NSEvent theEvent);
	public virtual void EndEditing (NSText textObj);
	public virtual void SelectWithFrame (System.Drawing.RectangleF aRect, NSText textObj, MonoMac.Foundation.NSObject anObject, int selStart, int selLength);
	public virtual System.Drawing.SizeF SizeThatFits (System.Drawing.SizeF size);
```

### Type Changed: MonoMac.AppKit.NSController

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSControlTextFilter

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (System.IAsyncResult result);
	public virtual string[] Invoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (ref int index, System.IAsyncResult result);
	public virtual string[] Invoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
```

### Type Changed: MonoMac.AppKit.NSCursor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSCustomImageRep

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDatePicker

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDatePickerCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDatePickerCellDelegate

Added interfaces:

```
INSDatePickerCellDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDockTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDockTilePlugIn

Added interfaces:

```
INSDockTilePlugIn
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDocument

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSPrintOperation PDFPrintOperation { get; }
```

Removed method:

```
public virtual void SetDisplayName (string displayNameOrNull);
```

Added methods:

```
public virtual void SaveDocumentAsPdf (MonoMac.Foundation.NSObject sender);

	[Obsolete ("Use the DisplayName property instead")]
	public void SetDisplayName (string displayNameOrNull);
```

### Type Changed: MonoMac.AppKit.NSDocumentController

Added interfaces:

```
INSWindowRestoration
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public static MonoMac.Foundation.NSObject SharedDocumentController { get; }
```

Added property:

```
public static NSDocumentController SharedDocumentController { get; }
```

Removed method:

```
public virtual void OpenDocumentWithContentsOfUrl (MonoMac.Foundation.NSUrl url, bool displayDocument, OpenDocumentCompletionHandler completionHandler);
```

Added method:

```
[Obsolete ("Use OpenDocument instead")]
	public void OpenDocumentWithContentsOfUrl (MonoMac.Foundation.NSUrl url, bool displayDocument, OpenDocumentCompletionHandler completionHandler);
```

### Type Changed: MonoMac.AppKit.NSDraggingDestination

Added interfaces:

```
INSDraggingDestination
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDraggingImageComponent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDraggingInfo

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, NSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
```

Added methods:

```
public void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, NSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
	public void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, MonoMac.Foundation.NSArray classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
```

### Type Changed: MonoMac.AppKit.NSDraggingItem

Added constructor:

```
public NSDraggingItem (INSPasteboardWriting pasteboardWriter);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDraggingSession

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, NSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
```

Added methods:

```
public void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, NSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
	public void EnumerateDraggingItems (NSDraggingItemEnumerationOptions enumOpts, NSView view, MonoMac.Foundation.NSArray classArray, MonoMac.Foundation.NSDictionary searchOptions, NSDraggingEnumerator enumerator);
```

### Type Changed: MonoMac.AppKit.NSDraggingSource

Added interfaces:

```
INSDraggingSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSDrawer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual void Close ();
	public virtual void Open ();
```

### Type Changed: MonoMac.AppKit.NSDrawerDelegate

Added interfaces:

```
INSDrawerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSEPSImageRep

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual System.IntPtr EventRef { get; }
```

### Type Changed: MonoMac.AppKit.NSFont

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual System.Drawing.SizeF AdvancementForGlyph (uint ag);
```

Added method:

```
public virtual System.Drawing.SizeF AdvancementForGlyph (uint aGlyph);
```

### Type Changed: MonoMac.AppKit.NSFontCollection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSFontDescriptor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSFontManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSFontPanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSForm

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSFormCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual System.IntPtr ConstrainScrollPoint (string aString);
```

Added method:

```
public virtual float TitleWidthConstraintedToSize (System.Drawing.SizeF aSize);
```

### Type Changed: MonoMac.AppKit.NSGlyphGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSGlyphInfo

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSGradient

Added constructors:

```
public NSGradient (NSColor[] colors, double[] locations);
	public NSGradient (NSColor[] colors, double[] locations, NSColorSpace colorSpace);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSGraphics

Added method:

```
public static void SetFocusRingStyle (NSFocusRingPlacement placement);
```

### Type Changed: MonoMac.AppKit.NSGraphicsContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual MonoMac.CoreGraphics.CGContext CGContext { get; }
```

Added method:

```
public static NSGraphicsContext FromCGContext (MonoMac.CoreGraphics.CGContext graphicsPort, bool initialFlippedState);
```

### Type Changed: MonoMac.AppKit.NSHelpManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSImage

Added constructor:

```
public NSImage (MonoMac.Foundation.NSData data, bool ignoresOrientation);
```

Added interfaces:

```
INSPasteboardReading
	INSPasteboardWriting
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual NSEdgeInsets CapInsets { get; set; }
	public virtual bool MatchesOnlyOnBestFittingAxis { get; set; }
	public virtual NSImageResizingMode ResizingMode { get; set; }
```

Removed method:

```
public virtual void DrawInRect (System.Drawing.RectangleF dstRect, System.Drawing.RectangleF srcRect, NSCompositingOperation operation, float delta);
```

Added methods:

```
public virtual void Draw (System.Drawing.RectangleF rect);
	public void DrawInRect (System.Drawing.RectangleF dstRect, System.Drawing.RectangleF srcRect, NSCompositingOperation operation, float delta);
	public virtual MonoMac.Foundation.NSObject GetLayerContentsForContentsScale (float layerContentsScale);
	public virtual MonoMac.Foundation.NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual float GetRecommendedLayerContentsScale (float preferredContentsScale);
	public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual MonoMac.Foundation.NSObject InitWithPasteboardPropertyList (MonoMac.Foundation.NSObject propertyList, string type);
```

### Type Changed: MonoMac.AppKit.NSImageCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSImageDelegate

Added interfaces:

```
INSImageDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSImageRep

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSImageView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSLayoutConstraint

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual bool Active { get; set; }
```

Added methods:

```
public static void ActivateConstraints (NSLayoutConstraint[] constraints);
	public static void DeactivateConstraints (NSLayoutConstraint[] constraints);
	public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, object[] viewsAndMetrics);
```

### Type Changed: MonoMac.AppKit.NSLayoutManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual MonoMac.Foundation.NSRange CharacterRangeForGlyphRange (MonoMac.Foundation.NSRange glyphRange, out MonoMac.Foundation.NSRange actualGlyphRange);
	public virtual void DrawBackgroundForGlyphRange (MonoMac.Foundation.NSRange glyphsToShow, System.Drawing.PointF origin);
	public virtual void DrawGlyphsForGlyphRange (MonoMac.Foundation.NSRange glyphsToShow, System.Drawing.PointF origin);
	public uint GlyphAtIndex (int glyphIndex, ref bool isValidIndex);
	public uint GlyphAtIndex (int glyphIndex);
	public virtual MonoMac.Foundation.NSRange GlyphRangeForCharacterRange (MonoMac.Foundation.NSRange charRange, out MonoMac.Foundation.NSRange actualCharRange);
```

Obsoleted methods:

```
[Obsolete ("Use GlyphAtIndex instead")]
	public virtual uint GlyphAtIndexisValidIndex (uint glyphIndex, ref bool isValidIndex);

	[Obsolete ("Use GlyphAtIndex instead")]
	public virtual uint GlyphCount (int glyphIndex);
```

### Type Changed: MonoMac.AppKit.NSLayoutManagerDelegate

Added interfaces:

```
INSLayoutManagerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSLevelIndicator

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSLevelIndicatorStyle LevelIndicatorStyle { get; set; }
```

### Type Changed: MonoMac.AppKit.NSLevelIndicatorCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMatrix

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMatrixDelegate

Added interfaces:

```
INSMatrixDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMenu

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMenuDelegate

Added interfaces:

```
INSMenuDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMenuItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMenuItemCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMenuView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSMutableFontCollection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public static NSMutableFontCollection FromDescriptors (NSFontDescriptor[] queryDescriptors);
	public static NSMutableFontCollection FromLocale (MonoMac.Foundation.NSLocale locale);
	public static NSMutableFontCollection FromName (string name, NSFontCollectionVisibility visibility);
	public static NSMutableFontCollection FromName (string name);
	public static NSMutableFontCollection GetAllAvailableFonts ();
```

### Type Changed: MonoMac.AppKit.NSMutableParagraphStyle

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSNib

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSObjectController

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual void SetEditable (bool editable);
```

Added method:

```
[Obsolete ("Use the Editable property instead")]
	public void SetEditable (bool editable);
```

### Type Changed: MonoMac.AppKit.NSOpenGLContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSOpenGLPixelFormat PixelFormat { get; }
```

### Type Changed: MonoMac.AppKit.NSOpenGLPixelBuffer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOpenGLPixelFormat

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOpenGLProfile

Added value:

```
Version4_1Core = 16640,
```

### Type Changed: MonoMac.AppKit.NSOpenGLView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOpenPanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOpenSavePanelDelegate

Added interfaces:

```
INSOpenSavePanelDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOutlineView

Added interfaces:

```
INSDraggingSource
	INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSUserInterfaceLayoutDirection UserInterfaceLayoutDirection { get; set; }
```

Added methods:

```
public virtual MonoMac.Foundation.NSObject GetChild (int index, MonoMac.Foundation.NSObject parentItem);
	public virtual int NumberOfChildren (MonoMac.Foundation.NSObject item);
```

### Type Changed: MonoMac.AppKit.NSOutlineViewDataSource

Added interfaces:

```
INSOutlineViewDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSOutlineViewDelegate

Added interfaces:

```
INSOutlineViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPageController

Added interfaces:

```
INSSeguePerforming
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public NSPageControllerGetFrame GetFrame { get; set; }
	public NSPageControllerGetIdentifier GetIdentifier { get; set; }
	public NSPageControllerGetViewController GetViewController { get; set; }
```

Added event:

```
public event System.EventHandler<NSPageControllerPrepareViewControllerEventArgs> PrepareViewController;
```

### Type Changed: MonoMac.AppKit.NSPageControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual System.Drawing.RectangleF GetFrame (NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public virtual string GetIdentifier (NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public virtual NSViewController GetViewController (NSPageController pageController, string identifier);
	public virtual void PrepareViewController (NSPageController pageController, NSViewController viewController, MonoMac.Foundation.NSObject targetObject);
```

### Type Changed: MonoMac.AppKit.NSPageControllerDelegate_Extensions

Added methods:

```
public static System.Drawing.RectangleF GetFrame (INSPageControllerDelegate This, NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public static string GetIdentifier (INSPageControllerDelegate This, NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public static NSViewController GetViewController (INSPageControllerDelegate This, NSPageController pageController, string identifier);
	public static void PrepareViewController (INSPageControllerDelegate This, NSPageController pageController, NSViewController viewController, MonoMac.Foundation.NSObject targetObject);
```

### Type Changed: MonoMac.AppKit.NSPageLayout

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSParagraphStyle

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPasteboard

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed methods:

```
public virtual MonoMac.Foundation.NSObject[] ReadObjectsForClasses (NSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary options);
	public virtual bool WriteObjects (NSPasteboardReading[] objects);
```

Added methods:

```
public virtual MonoMac.Foundation.NSObject[] ReadObjectsForClasses (INSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary options);
	public bool WriteObjects (NSPasteboardReading[] objects);
	public bool WriteObjects (INSPasteboardWriting[] objects);
	public bool WriteObjects (NSPasteboardWriting[] objects);
```

### Type Changed: MonoMac.AppKit.NSPasteboardItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPasteboardItemDataProvider

Added interfaces:

```
INSPasteboardItemDataProvider
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPasteboardReading

Added interfaces:

```
INSPasteboardReading
	MonoMac.Foundation.INSObjectProtocol
```

Removed methods:

```
public virtual string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
```

Added methods:

```
public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
```

### Type Changed: MonoMac.AppKit.NSPasteboardWriting

Added interfaces:

```
INSPasteboardWriting
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPathCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPathCellDelegate

Added interfaces:

```
INSPathCellDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPathComponentCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPathControl

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSString[] AllowedTypes { get; set; }
	public virtual NSPathControlItem ClickedPathItem { get; }
	public virtual bool Editable { get; set; }
	public virtual NSPathControlItem[] PathItems { get; set; }
	public virtual MonoMac.Foundation.NSAttributedString PlaceholderAttributedString { get; set; }
	public virtual string PlaceholderString { get; set; }
```

### Type Changed: MonoMac.AppKit.NSPathControlDelegate

Added interfaces:

```
INSPathControlDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual bool ShouldDragItem (NSPathControl pathControl, NSPathControlItem pathItem, NSPasteboard pasteboard);
```

### Type Changed: MonoMac.AppKit.NSPopover

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPopoverDelegate

Added interfaces:

```
INSPopoverDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPopUpButton

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual int SelectedTag { get; }
```

### Type Changed: MonoMac.AppKit.NSPopUpButtonCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPredicateEditor

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPredicateEditorRowTemplate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrinter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrintInfo

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrintOperation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrintPanel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrintPanelAccessorizing

Added interfaces:

```
INSPrintPanelAccessorizing
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSPrintPreviewGraphicsContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSProgressIndicator

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRemoteOpenPanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRemoteSavePanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSResponder

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public MonoMac.Foundation.NSObject ValidRequestorForSendType (string sendType, string returnType);
```

Obsoleted method:

```
[Obsolete ("Use ValidRequestorForSendType instead")]
	public virtual MonoMac.Foundation.NSObject ValidRequestorForSendTypereturnType (string sendType, string returnType);
```

### Type Changed: MonoMac.AppKit.NSRuleEditor

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRuleEditorDelegate

Added interfaces:

```
INSRuleEditorDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRulerMarker

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRulerView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSRunningApplication

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual bool OwnsMenuBar { get; }
```

### Type Changed: MonoMac.AppKit.NSSavePanel

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool ShowsTagField { get; set; }
	public virtual string[] TagNames { get; set; }
```

Removed event:

```
[Obsolete ("On 10.6 and newer Use DidChangeToDirectoryUrl instead")]
	[Obsolete ("On 10.6 and newer Use DidChangeToDirectoryUrl instead")]
	public event System.EventHandler<NSOpenSaveFilenameEventArgs> DirectoryDidChange;
```

Added event:

```
public event System.EventHandler<NSOpenSaveFilenameEventArgs> DirectoryDidChange;
```

### Type Changed: MonoMac.AppKit.NSScreen

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public static bool ScreensHaveSeparateSpaces ();
```

### Type Changed: MonoMac.AppKit.NSScroller

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSScrollView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSearchField

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual int MaximumRecents { get; set; }
	public virtual NSMenu SearchMenuTemplate { get; set; }
	public virtual bool SendsSearchStringImmediately { get; set; }
	public virtual bool SendsWholeSearchString { get; set; }
```

### Type Changed: MonoMac.AppKit.NSSearchFieldCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSecureTextField

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSecureTextFieldCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSegmentedCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSegmentedControl

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSegmentStyle

Added value:

```
Separated = 8,
```

### Type Changed: MonoMac.AppKit.NSShadow

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSharingService

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual string AccountName { get; }
	public virtual MonoMac.Foundation.NSUrl[] AttachmentFileUrls { get; }
	public virtual string MenuItemTitle { get; set; }
	public virtual string MessageBody { get; }
	public virtual MonoMac.Foundation.NSUrl PermanentLink { get; }
	public virtual MonoMac.Foundation.NSObject[] Recipients { get; set; }
	public virtual string Subject { get; set; }
```

### Type Changed: MonoMac.AppKit.NSSharingServiceDelegate

Added interfaces:

```
INSSharingServiceDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Removed methods:

```
public virtual System.Drawing.RectangleF SourceFrameOnScreenForShareItem (NSSharingService sharingService, NSPasteboardWriting item);
	public virtual NSImage TransitionImageForShareItem (NSSharingService sharingService, NSPasteboardWriting item, System.Drawing.RectangleF contentRect);
```

Added methods:

```
public virtual System.Drawing.RectangleF SourceFrameOnScreenForShareItem (NSSharingService sharingService, INSPasteboardWriting item);
	public virtual NSImage TransitionImageForShareItem (NSSharingService sharingService, INSPasteboardWriting item, System.Drawing.RectangleF contentRect);
```

### Type Changed: MonoMac.AppKit.NSSharingServicePicker

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSharingServicePickerDelegate

Added interfaces:

```
INSSharingServicePickerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSharingServiceSourceFrameOnScreenForShareItem

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (NSSharingService sharingService, NSPasteboardWriting item, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF Invoke (NSSharingService sharingService, NSPasteboardWriting item);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (NSSharingService sharingService, INSPasteboardWriting item, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF Invoke (NSSharingService sharingService, INSPasteboardWriting item);
```

### Type Changed: MonoMac.AppKit.NSSharingServiceTransitionImageForShareItem

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (NSSharingService sharingService, NSPasteboardWriting item, System.Drawing.RectangleF contentRect, System.AsyncCallback callback, object object);
	public virtual NSImage Invoke (NSSharingService sharingService, NSPasteboardWriting item, System.Drawing.RectangleF contentRect);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (NSSharingService sharingService, INSPasteboardWriting item, System.Drawing.RectangleF contentRect, System.AsyncCallback callback, object object);
	public virtual NSImage Invoke (NSSharingService sharingService, INSPasteboardWriting item, System.Drawing.RectangleF contentRect);
```

### Type Changed: MonoMac.AppKit.NSSlider

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSSliderType SliderType { get; set; }
```

### Type Changed: MonoMac.AppKit.NSSliderCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual System.Drawing.RectangleF BarRectFlipped (bool flipped);
```

### Type Changed: MonoMac.AppKit.NSSound

Added interfaces:

```
INSPasteboardReading
	INSPasteboardWriting
	MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual MonoMac.Foundation.NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual MonoMac.Foundation.NSObject InitWithPasteboardPropertyList (MonoMac.Foundation.NSObject propertyList, string type);
```

### Type Changed: MonoMac.AppKit.NSSoundDelegate

Added interfaces:

```
INSSoundDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSpeechRecognizer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSpeechRecognizerDelegate

Added interfaces:

```
INSSpeechRecognizerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSpeechSynthesizer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSpeechSynthesizerDelegate

Added interfaces:

```
INSSpeechSynthesizerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSpellChecker

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public MonoMac.Foundation.NSTextCheckingResult[] CheckString (string stringToCheck, MonoMac.Foundation.NSRange range, MonoMac.Foundation.NSTextCheckingTypes checkingTypes, NSTextCheckingOptions options, int tag, out MonoMac.Foundation.NSOrthography orthography, out int wordCount);
	public static bool IsAutomaticDashSubstitutionEnabled ();
	public static bool IsAutomaticQuoteSubstitutionEnabled ();
	public NSMenu MenuForResults (MonoMac.Foundation.NSTextCheckingResult result, string checkedString, NSTextCheckingOptions options, System.Drawing.PointF location, NSView view);
	public int RequestChecking (string stringToCheck, MonoMac.Foundation.NSRange range, MonoMac.Foundation.NSTextCheckingTypes checkingTypes, NSTextCheckingOptions options, int tag, System.Action<System.Int32,MonoMac.Foundation.NSTextCheckingResult[],MonoMac.Foundation.NSOrthography,System.Int32> completionHandler);
	public virtual int RequestChecking (string stringToCheck, MonoMac.Foundation.NSRange range, MonoMac.Foundation.NSTextCheckingTypes checkingTypes, MonoMac.Foundation.NSDictionary options, int tag, System.Action<System.Int32,MonoMac.Foundation.NSTextCheckingResult[],MonoMac.Foundation.NSOrthography,System.Int32> completionHandler);
```

### Type Changed: MonoMac.AppKit.NSSplitView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSSplitViewDelegate

Added interfaces:

```
INSSplitViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSStatusBar

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSStatusItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual NSStatusBarButton Button { get; }
```

### Type Changed: MonoMac.AppKit.NSStepper

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableCellView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableColumn

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual string Title { get; set; }
```

### Type Changed: MonoMac.AppKit.NSTableHeaderCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableHeaderView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableRowView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool NextRowSelected { get; set; }
	public virtual bool PreviousRowSelected { get; set; }
```

### Type Changed: MonoMac.AppKit.NSTableView

Added interfaces:

```
INSDraggingSource
	INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSDictionary RegisteredNibsByIdentifier { get; }
	public virtual bool UsesStaticContents { get; set; }
```

Added methods:

```
public virtual NSImage DragImageForRowsWithIndexestableColumnseventoffset (MonoMac.Foundation.NSIndexSet dragRows, NSTableColumn[] tableColumns, NSEvent dragEvent, ref System.Drawing.PointF dragImageOffset);
	public virtual void RegisterNib (NSNib nib, string identifier);
	public virtual void RowViewAdded (NSTableRowView rowView, int row);
	public virtual void RowViewRemoved (NSTableRowView rowView, int row);
```

### Type Changed: MonoMac.AppKit.NSTableViewDataSource

Added interfaces:

```
INSTableViewDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableViewDelegate

Added interfaces:

```
INSTableViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTableViewSource

Added interfaces:

```
INSTableViewSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTabView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTabViewDelegate

Added interfaces:

```
INSTabViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTabViewItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual NSImage Image { get; set; }
	public virtual string ToolTip { get; set; }
	public virtual NSViewController ViewController { get; set; }
```

Added method:

```
public static NSTabViewItem GetTabViewItem (NSViewController viewController);
```

### Type Changed: MonoMac.AppKit.NSText

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextAlternatives

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextAttachment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextAttachmentCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextBlock

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextContainer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextDelegate

Added interfaces:

```
INSTextDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextField

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSAttributedString PlaceholderAttributedString { get; set; }
	public virtual string PlaceholderString { get; set; }
```

### Type Changed: MonoMac.AppKit.NSTextFieldCell

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextFieldDelegate

Added interfaces:

```
INSTextFieldDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
```

Added method:

```
public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
```

### Type Changed: MonoMac.AppKit.NSTextFinder

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextFinderBarContainer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextFinderClient

Added interfaces:

```
INSTextFinderClient
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextInputContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextStorage

Added constructor:

```
public NSTextStorage (string str);
```

Added interfaces:

```
INSPasteboardReading
	INSPasteboardWriting
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextStorageDelegate

Added interfaces:

```
INSTextStorageDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextTab

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextTable

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextTableBlock

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTextView

Added interfaces:

```
INSDraggingSource
	INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual NSTextViewDelegate Delegate { get; set; }
```

Added properties:

```
public NSTextViewDelegate Delegate { get; set; }
	public virtual bool UsesRolloverButtonForSelection { get; set; }
```

### Type Changed: MonoMac.AppKit.NSTextViewDelegate

Added interfaces:

```
INSTextViewDelegate
	INSTextDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTokenField

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTokenFieldDelegate

Added interfaces:

```
INSTokenFieldDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSToolbar

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual bool AllowsExtensionItems { get; set; }
```

### Type Changed: MonoMac.AppKit.NSToolbarDelegate

Added interfaces:

```
INSToolbarDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSToolbarItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTouch

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTrackingArea

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTreeController

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTreeNode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSTypesetter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSView

Added interfaces:

```
INSDraggingDestination
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool AllowsVibrancy { get; }
	public virtual bool CanDrawSubviewsIntoLayer { get; set; }
	public virtual NSGestureRecognizer[] GestureRecognizers { get; set; }
	public static bool IsCompatibleWithResponsiveScrolling { get; }
	public virtual bool LayerUsesCoreImageFilters { get; set; }
	public virtual System.Drawing.RectangleF PreparedContentRect { get; set; }
	public virtual NSUserInterfaceLayoutDirection UserInterfaceLayoutDirection { get; set; }
```

Added methods:

```
public virtual void AddGestureRecognizer (NSGestureRecognizer gestureRecognizer);
	public virtual void DidChangeBackingProperties ();
	public virtual void PrepareContentInRect (System.Drawing.RectangleF rect);
	public virtual void PrepareForReuse ();
	public virtual void RemoveGestureRecognizer (NSGestureRecognizer gestureRecognizer);
```

### Type Changed: MonoMac.AppKit.NSViewAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSViewController

Added interfaces:

```
INSSeguePerforming
	INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual NSViewController[] ChildViewControllers { get; set; }
	public virtual string Identifier { get; set; }
	public virtual NSViewController ParentViewController { get; }
	public virtual System.Drawing.SizeF PreferredContentSize { get; set; }
	public virtual NSViewController[] PresentedViewControllers { get; }
	public virtual NSViewController PresentingViewController { get; }
	public virtual NSStoryboard Storyboard { get; }
	public virtual bool ViewLoaded { get; }
```

Added methods:

```
public virtual void AddChildViewController (NSViewController childViewController);
	public virtual void DismissController (MonoMac.Foundation.NSObject sender);
	public virtual void DismissViewController (NSViewController viewController);
	public virtual void InsertChildViewController (NSViewController childViewController, int index);
	public virtual void PerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
	public virtual void PreferredContentSizeDidChange (NSViewController viewController);
	public virtual void PrepareForSegue (NSStoryboardSegue segue, MonoMac.Foundation.NSObject sender);
	public virtual void PresentViewController (NSViewController viewController, System.Drawing.RectangleF positioningRect, NSView positioningView, uint preferredEdge, NSPopoverBehavior behavior);
	public virtual void PresentViewController (NSViewController viewController, NSViewControllerPresentationAnimator animator);
	public virtual void PresentViewControllerAsModalWindow (NSViewController viewController);
	public virtual void PresentViewControllerAsSheet (NSViewController viewController);
	public virtual void RemoveChildViewController (int index);
	public virtual void RemoveFromParentViewController ();
	public virtual bool ShouldPerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
	public virtual void TransitionFromViewController (NSViewController fromViewController, NSViewController toViewController, NSViewControllerTransitionOptions options, System.Action completion);
	public virtual void UpdateViewConstraints ();
	public virtual void ViewDidAppear ();
	public virtual void ViewDidDisappear ();
	public virtual void ViewDidLayout ();
	public virtual void ViewDidLoad ();
	public virtual void ViewWillAppear ();
	public virtual void ViewWillDisappear ();
	public virtual void ViewWillLayout ();
	public virtual void ViewWillTransition (System.Drawing.SizeF newSize);
```

### Type Changed: MonoMac.AppKit.NSWindow

Added interfaces:

```
INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSObject ContentLayoutGuide { get; }
	public virtual System.Drawing.RectangleF ContentLayoutRect { get; }
	public virtual NSViewController ContentViewController { get; set; }
	public virtual NSWindowOcclusionState OcclusionState { get; }
	public virtual NSWindow SheetParent { get; }
	public virtual NSWindow[] Sheets { get; }
	public virtual NSTitlebarAccessoryViewController[] TitlebarAccessoryViewControllers { get; }
	public virtual bool TitlebarAppearsTransparent { get; set; }
	public virtual NSWindowTitleVisibility TitleVisibility { get; set; }
```

Added event:

```
public event System.EventHandler DidChangeBackingProperties;
```

Added methods:

```
public virtual void AddTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController);
	public virtual void BeginCriticalSheet (NSWindow sheetWindow, System.Action<int> completionHandler);
	public virtual void BeginSheet (NSWindow sheetWindow, System.Action<int> completionHandler);
	public virtual void EndSheet (NSWindow sheetWindow, int returnCode);
	public virtual void EndSheet (NSWindow sheetWindow);
	public static NSWindow GetWindowWithContentViewController (NSViewController contentViewController);
	public virtual void InsertTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController, int index);
	public virtual void RemoveTitlebarAccessoryViewControllerAtIndex (int index);
	public virtual void TrackEventsMatching (NSEventMask mask, double timeout, string mode, NSWindowTrackEventsMatchingCompletionHandler trackingHandler);
```

### Type Changed: MonoMac.AppKit.NSWindowController

Added interfaces:

```
INSSeguePerforming
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual NSViewController ContentViewController { get; set; }
	public virtual NSStoryboard Storyboard { get; }
```

Added methods:

```
public virtual void DismissController (MonoMac.Foundation.NSObject sender);
	public virtual void PerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
	public virtual void PrepareForSegue (NSStoryboardSegue segue, MonoMac.Foundation.NSObject sender);
	public virtual bool ShouldPerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
```

### Type Changed: MonoMac.AppKit.NSWindowDelegate

Added interfaces:

```
INSWindowDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual void DidChangeBackingProperties (MonoMac.Foundation.NSNotification notification);
```

### Type Changed: MonoMac.AppKit.NSWindowRestoration

Added interfaces:

```
INSWindowRestoration
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AppKit.NSWindowStyle

Added value:

```
FullSizeContentView = 32768,
```

### Type Changed: MonoMac.AppKit.NSWorkspace

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual NSRunningApplication OpenURL (MonoMac.Foundation.NSUrl url, NSWorkspaceLaunchOptions options, MonoMac.Foundation.NSDictionary configuration, out MonoMac.Foundation.NSError error);
	public virtual NSRunningApplication OpenURLs (MonoMac.Foundation.NSUrl[] urls, MonoMac.Foundation.NSUrl applicationURL, NSWorkspaceLaunchOptions options, MonoMac.Foundation.NSDictionary configuration, out MonoMac.Foundation.NSError error);
```

### New Type MonoMac.AppKit.INSAlertDelegate

```
public interface INSAlertDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSAnimationDelegate

```
public interface INSAnimationDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSAppearanceCustomization

```
public interface INSAppearanceCustomization : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSApplicationDelegate

```
public interface INSApplicationDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSBrowserDelegate

```
public interface INSBrowserDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSCollectionViewDelegate

```
public interface INSCollectionViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSComboBoxCellDataSource

```
public interface INSComboBoxCellDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSComboBoxDataSource

```
public interface INSComboBoxDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSComboBoxDelegate

```
public interface INSComboBoxDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSTextFieldDelegate {
}
```

### New Type MonoMac.AppKit.INSControlTextEditingDelegate

```
public interface INSControlTextEditingDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSDatePickerCellDelegate

```
public interface INSDatePickerCellDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSDockTilePlugIn

```
public interface INSDockTilePlugIn : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual NSMenu DockMenu ();
	public virtual void SetDockTile (NSDockTile dockTile);
}
```

### New Type MonoMac.AppKit.INSDraggingDestination

```
public interface INSDraggingDestination : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSDraggingSource

```
public interface INSDraggingSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSDrawerDelegate

```
public interface INSDrawerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSGestureRecognizerDelegate

```
public interface INSGestureRecognizerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSImageDelegate

```
public interface INSImageDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSLayoutManagerDelegate

```
public interface INSLayoutManagerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSMatrixDelegate

```
public interface INSMatrixDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSMenuDelegate

```
public interface INSMenuDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void MenuWillHighlightItem (NSMenu menu, NSMenuItem item);
}
```

### New Type MonoMac.AppKit.INSOpenSavePanelDelegate

```
public interface INSOpenSavePanelDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSOutlineViewDataSource

```
public interface INSOutlineViewDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSOutlineViewDelegate

```
public interface INSOutlineViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSPasteboardItemDataProvider

```
public interface INSPasteboardItemDataProvider : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void FinishedWithDataProvider (NSPasteboard pasteboard);
	public virtual void ProvideDataForType (NSPasteboard pasteboard, NSPasteboardItem item, string type);
}
```

### New Type MonoMac.AppKit.INSPasteboardReading

```
public interface INSPasteboardReading : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual MonoMac.Foundation.NSObject InitWithPasteboardPropertyList (MonoMac.Foundation.NSObject propertyList, string type);
}
```

### New Type MonoMac.AppKit.INSPasteboardWriting

```
public interface INSPasteboardWriting : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSPathCellDelegate

```
public interface INSPathCellDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSPathControlDelegate

```
public interface INSPathControlDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual bool AcceptDrop (NSPathControl pathControl, NSDraggingInfo info);
	public virtual bool ShouldDragPathComponentCell (NSPathControl pathControl, NSPathComponentCell pathComponentCell, NSPasteboard pasteboard);
	public virtual NSDragOperation ValidateDrop (NSPathControl pathControl, NSDraggingInfo info);
	public virtual void WillDisplayOpenPanel (NSPathControl pathControl, NSOpenPanel openPanel);
	public virtual void WillPopUpMenu (NSPathControl pathControl, NSMenu menu);
}
```

### New Type MonoMac.AppKit.INSPopoverDelegate

```
public interface INSPopoverDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSPrintPanelAccessorizing

```
public interface INSPrintPanelAccessorizing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual MonoMac.Foundation.NSSet KeyPathsForValuesAffectingPreview ();
	public virtual MonoMac.Foundation.NSDictionary[] LocalizedSummaryItems ();
}
```

### New Type MonoMac.AppKit.INSRuleEditorDelegate

```
public interface INSRuleEditorDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual MonoMac.Foundation.NSObject ChildForCriterion (NSRuleEditor editor, int index, MonoMac.Foundation.NSObject criterion, NSRuleEditorRowType rowType);
	public virtual MonoMac.Foundation.NSObject DisplayValue (NSRuleEditor editor, MonoMac.Foundation.NSObject criterion, int row);
	public virtual int NumberOfChildren (NSRuleEditor editor, MonoMac.Foundation.NSObject criterion, NSRuleEditorRowType rowType);
	public virtual MonoMac.Foundation.NSDictionary PredicateParts (NSRuleEditor editor, MonoMac.Foundation.NSObject criterion, MonoMac.Foundation.NSObject value, int row);
	public virtual void RowsDidChange (MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.INSSeguePerforming

```
public interface INSSeguePerforming : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSharingServiceDelegate

```
public interface INSSharingServiceDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSharingServicePickerDelegate

```
public interface INSSharingServicePickerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSoundDelegate

```
public interface INSSoundDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSpeechRecognizerDelegate

```
public interface INSSpeechRecognizerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSpeechSynthesizerDelegate

```
public interface INSSpeechSynthesizerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSSplitViewDelegate

```
public interface INSSplitViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSStackViewDelegate

```
public interface INSStackViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTableViewDataSource

```
public interface INSTableViewDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTableViewDelegate

```
public interface INSTableViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTableViewSource

```
public interface INSTableViewSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTabViewDelegate

```
public interface INSTabViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTextDelegate

```
public interface INSTextDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTextFieldDelegate

```
public interface INSTextFieldDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTextFinderClient

```
public interface INSTextFinderClient : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool AllowsMultipleSelection { get; }
	public virtual bool Editable { get; }
	public virtual MonoMac.Foundation.NSRange FirstSelectedRange { get; }
	public virtual bool Selectable { get; }
	public virtual MonoMac.Foundation.NSArray SelectedRanges { get; set; }
	public virtual string String { get; }
	public virtual MonoMac.Foundation.NSArray VisibleCharacterRanges { get; }
	// methods
	public virtual NSView ContentViewAtIndexeffectiveCharacterRange (uint index, ref MonoMac.Foundation.NSRange outRange);
	public virtual void DidReplaceCharacters ();
	public virtual void DrawCharactersInRangeforContentView (MonoMac.Foundation.NSRange range, NSView view);
	public virtual MonoMac.Foundation.NSArray RectsForCharacterRange (MonoMac.Foundation.NSRange range);
	public virtual void ReplaceCharactersInRangewithString (MonoMac.Foundation.NSRange range, string str);
	public virtual void ScrollRangeToVisible (MonoMac.Foundation.NSRange range);
	public virtual bool ShouldReplaceCharactersInRangeswithStrings (MonoMac.Foundation.NSArray ranges, MonoMac.Foundation.NSArray strings);
	public virtual string StringAtIndexeffectiveRangeendsWithSearchBoundary (uint characterIndex, ref MonoMac.Foundation.NSRange outRange, bool outFlag);
	public virtual uint StringLength ();
}
```

### New Type MonoMac.AppKit.INSTextStorageDelegate

```
public interface INSTextStorageDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSTextViewDelegate

```
public interface INSTextViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSTextDelegate {
}
```

### New Type MonoMac.AppKit.INSTokenFieldDelegate

```
public interface INSTokenFieldDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSToolbarDelegate

```
public interface INSToolbarDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSUserInterfaceItemIdentification

```
public interface INSUserInterfaceItemIdentification : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSViewControllerPresentationAnimator

```
public interface INSViewControllerPresentationAnimator : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void AnimateDismissal (NSViewController viewController, NSViewController fromViewController);
	public virtual void AnimatePresentation (NSViewController viewController, NSViewController fromViewController);
}
```

### New Type MonoMac.AppKit.INSWindowDelegate

```
public interface INSWindowDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.INSWindowRestoration

```
public interface INSWindowRestoration : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.NSAlertDelegate_Extensions

```
public static class NSAlertDelegate_Extensions {
	// methods
	public static bool ShowHelp (INSAlertDelegate This, NSAlert alert);
}
```

### New Type MonoMac.AppKit.NSAnimationDelegate_Extensions

```
public static class NSAnimationDelegate_Extensions {
	// methods
	public static void AnimationDidEnd (INSAnimationDelegate This, NSAnimation animation);
	public static void AnimationDidReachProgressMark (INSAnimationDelegate This, NSAnimation animation, float progress);
	public static void AnimationDidStop (INSAnimationDelegate This, NSAnimation animation);
	public static bool AnimationShouldStart (INSAnimationDelegate This, NSAnimation animation);
	public static float ComputeAnimationCurve (INSAnimationDelegate This, NSAnimation animation, float progress);
}
```

### New Type MonoMac.AppKit.NSAppearance

```
public class NSAppearance : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSAppearance ();
	public NSAppearance (MonoMac.Foundation.NSCoder coder);
	public NSAppearance (MonoMac.Foundation.NSObjectFlag t);
	public NSAppearance (System.IntPtr handle);
	public NSAppearance (string name, MonoMac.Foundation.NSBundle bundle);
	// properties
	public virtual bool AllowsVibrancy { get; }
	public override System.IntPtr ClassHandle { get; }
	public static NSAppearance CurrentAppearance { get; set; }
	public virtual string Name { get; }
	public static MonoMac.Foundation.NSString NameAqua { get; }
	public static MonoMac.Foundation.NSString NameLightContent { get; }
	public static MonoMac.Foundation.NSString NameVibrantDark { get; }
	public static MonoMac.Foundation.NSString NameVibrantLight { get; }
	// methods
	public static NSAppearance GetAppearance (MonoMac.Foundation.NSString name);
}
```

### New Type MonoMac.AppKit.NSAppearanceCustomization

```
public class NSAppearanceCustomization : MonoMac.Foundation.NSObject, INSAppearanceCustomization, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSAppearanceCustomization ();
	public NSAppearanceCustomization (MonoMac.Foundation.NSCoder coder);
	public NSAppearanceCustomization (MonoMac.Foundation.NSObjectFlag t);
	public NSAppearanceCustomization (System.IntPtr handle);
	// properties
	public virtual NSAppearance Appearance { get; set; }
	public virtual NSAppearance EffectiveAppearance { get; }
}
```

### New Type MonoMac.AppKit.NSAppearanceCustomization_Extensions

```
public static class NSAppearanceCustomization_Extensions {
	// methods
	public static NSAppearance GetAppearance (INSAppearanceCustomization This);
	public static NSAppearance GetEffectiveAppearance (INSAppearanceCustomization This);
	public static void SetAppearance (INSAppearanceCustomization This, NSAppearance value);
}
```

### New Type MonoMac.AppKit.NSApplicationDelegate_Extensions

```
public static class NSApplicationDelegate_Extensions {
	// methods
	public static NSMenu ApplicationDockMenu (INSApplicationDelegate This, NSApplication sender);
	public static bool ApplicationOpenUntitledFile (INSApplicationDelegate This, NSApplication sender);
	public static bool ApplicationShouldHandleReopen (INSApplicationDelegate This, NSApplication sender, bool hasVisibleWindows);
	public static bool ApplicationShouldOpenUntitledFile (INSApplicationDelegate This, NSApplication sender);
	public static NSApplicationTerminateReply ApplicationShouldTerminate (INSApplicationDelegate This, NSApplication sender);
	public static bool ApplicationShouldTerminateAfterLastWindowClosed (INSApplicationDelegate This, NSApplication sender);
	public static void DecodedRestorableState (INSApplicationDelegate This, NSApplication app, MonoMac.Foundation.NSCoder state);
	public static void DidBecomeActive (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidFinishLaunching (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidHide (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidResignActive (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidUnhide (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidUpdate (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void FailedToContinueUserActivity (INSApplicationDelegate This, NSApplication application, string userActivityType, MonoMac.Foundation.NSError error);
	public static void FailedToRegisterForRemoteNotifications (INSApplicationDelegate This, NSApplication application, MonoMac.Foundation.NSError error);
	public static bool OpenFile (INSApplicationDelegate This, NSApplication sender, string filename);
	public static void OpenFiles (INSApplicationDelegate This, NSApplication sender, string[] filenames);
	public static bool OpenFileWithoutUI (INSApplicationDelegate This, MonoMac.Foundation.NSObject sender, string filename);
	public static bool OpenTempFile (INSApplicationDelegate This, NSApplication sender, string filename);
	public static void OrderFrontStandardAboutPanel (INSApplicationDelegate This, MonoMac.Foundation.NSObject sender);
	public static void OrderFrontStandardAboutPanelWithOptions (INSApplicationDelegate This, MonoMac.Foundation.NSDictionary optionsDictionary);
	public static bool PrintFile (INSApplicationDelegate This, NSApplication sender, string filename);
	public static NSApplicationPrintReply PrintFiles (INSApplicationDelegate This, NSApplication application, string[] fileNames, MonoMac.Foundation.NSDictionary printSettings, bool showPrintPanels);
	public static bool ReadSelectionFromPasteboard (INSApplicationDelegate This, NSPasteboard pboard);
	public static void ReceivedRemoteNotification (INSApplicationDelegate This, NSApplication application, MonoMac.Foundation.NSDictionary userInfo);
	public static void RegisteredForRemoteNotifications (INSApplicationDelegate This, NSApplication application, MonoMac.Foundation.NSData deviceToken);
	public static void RegisterServicesMenu (INSApplicationDelegate This, string[] sendTypes, string[] returnTypes);
	public static void ScreenParametersChanged (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillBecomeActive (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillEncodeRestorableState (INSApplicationDelegate This, NSApplication app, MonoMac.Foundation.NSCoder encoder);
	public static void WillFinishLaunching (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillHide (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static MonoMac.Foundation.NSError WillPresentError (INSApplicationDelegate This, NSApplication application, MonoMac.Foundation.NSError error);
	public static void WillResignActive (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillTerminate (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillUnhide (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillUpdate (INSApplicationDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool WriteSelectionToPasteboard (INSApplicationDelegate This, NSPasteboard board, string[] types);
}
```

### New Type MonoMac.AppKit.NSApplicationFailedEventArgs

```
public class NSApplicationFailedEventArgs : System.EventArgs {
	// constructors
	public NSApplicationFailedEventArgs (string userActivityType, MonoMac.Foundation.NSError error);
	// properties
	public MonoMac.Foundation.NSError Error { get; set; }
	public string UserActivityType { get; set; }
}
```

### New Type MonoMac.AppKit.NSApplicationOcclusionState

```
[Serializable]
[Flags]
public enum NSApplicationOcclusionState {
	Visible = 2,
}
```

### New Type MonoMac.AppKit.NSBrowserDelegate_Extensions

```
public static class NSBrowserDelegate_Extensions {
	// methods
	public static bool AcceptDrop (INSBrowserDelegate This, NSBrowser browser, NSDraggingInfo info, int row, int column, NSBrowserDropOperation dropOperation);
	public static bool CanDragRowsWithIndexes (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSIndexSet rowIndexes, int column, NSEvent theEvent);
	public static void ColumnConfigurationDidChange (INSBrowserDelegate This, MonoMac.Foundation.NSNotification notification);
	public static string ColumnTitle (INSBrowserDelegate This, NSBrowser sender, int column);
	public static int CountChildren (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static void CreateRowsForColumn (INSBrowserDelegate This, NSBrowser sender, int column, NSMatrix matrix);
	public static void DidChangeLastColumn (INSBrowserDelegate This, NSBrowser browser, int oldLastColumn, int toColumn);
	public static void DidScroll (INSBrowserDelegate This, NSBrowser sender);
	public static MonoMac.Foundation.NSObject GetChild (INSBrowserDelegate This, NSBrowser browser, int index, MonoMac.Foundation.NSObject item);
	public static NSViewController HeaderViewControllerForItem (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static bool IsColumnValid (INSBrowserDelegate This, NSBrowser sender, int column);
	public static bool IsLeafItem (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static int NextTypeSelectMatch (INSBrowserDelegate This, NSBrowser browser, int startRow, int endRow, int column, string searchString);
	public static MonoMac.Foundation.NSObject ObjectValueForItem (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static NSViewController PreviewViewControllerForLeafItem (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static string[] PromisedFilesDroppedAtDestination (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSUrl dropDestination, MonoMac.Foundation.NSIndexSet rowIndexes, int column);
	public static MonoMac.Foundation.NSObject RootItemForBrowser (INSBrowserDelegate This, NSBrowser browser);
	public static float RowHeight (INSBrowserDelegate This, NSBrowser browser, int row, int columnIndex);
	public static int RowsInColumn (INSBrowserDelegate This, NSBrowser sender, int column);
	public static bool SelectCellWithString (INSBrowserDelegate This, NSBrowser sender, string title, int column);
	public static MonoMac.Foundation.NSIndexSet SelectionIndexesForProposedSelection (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSIndexSet proposedSelectionIndexes, int inColumn);
	public static bool SelectRowInColumn (INSBrowserDelegate This, NSBrowser sender, int row, int column);
	public static void SetObjectValue (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject obj, MonoMac.Foundation.NSObject item);
	public static bool ShouldEditItem (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSObject item);
	public static bool ShouldShowCellExpansion (INSBrowserDelegate This, NSBrowser browser, int row, int column);
	public static float ShouldSizeColumn (INSBrowserDelegate This, NSBrowser browser, int columnIndex, bool userResize, float suggestedWidth);
	public static bool ShouldTypeSelectForEvent (INSBrowserDelegate This, NSBrowser browser, NSEvent theEvent, string currentSearchString);
	public static float SizeToFitWidth (INSBrowserDelegate This, NSBrowser browser, int columnIndex);
	public static string TypeSelectString (INSBrowserDelegate This, NSBrowser browser, int row, int column);
	public static NSDragOperation ValidateDrop (INSBrowserDelegate This, NSBrowser browser, NSDraggingInfo info, ref int row, ref int column, NSBrowserDropOperation dropOperation);
	public static void WillDisplayCell (INSBrowserDelegate This, NSBrowser sender, MonoMac.Foundation.NSObject cell, int row, int column);
	public static void WillScroll (INSBrowserDelegate This, NSBrowser sender);
	public static bool WriteRowsWithIndexesToPasteboard (INSBrowserDelegate This, NSBrowser browser, MonoMac.Foundation.NSIndexSet rowIndexes, int column, NSPasteboard pasteboard);
}
```

### New Type MonoMac.AppKit.NSClickGestureRecognizer

```
public class NSClickGestureRecognizer : MonoMac.AppKit.NSGestureRecognizer, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSClickGestureRecognizer ();
	public NSClickGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSClickGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSClickGestureRecognizer (System.IntPtr handle);
	public NSClickGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSClickGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSClickGestureRecognizer (System.Action<NSClickGestureRecognizer> action);
	// properties
	public virtual uint ButtonMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int NumberOfClicksRequired { get; set; }
}
```

### New Type MonoMac.AppKit.NSCollectionViewDelegate_Extensions

```
public static class NSCollectionViewDelegate_Extensions {
	// methods
	public static bool AcceptDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, int index, NSCollectionViewDropOperation dropOperation);
	public static bool CanDragItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSIndexSet indexes, NSEvent evt);
	public static void DraggingSessionEnded (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, NSDragOperation dragOperation);
	public static void DraggingSessionWillBegin (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSIndexSet indexes);
	public static string[] NamesOfPromisedFilesDroppedAtDestination (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSUrl dropUrl, MonoMac.Foundation.NSIndexSet indexes);
	public static NSPasteboardWriting PasteboardWriterForItemAtIndex (INSCollectionViewDelegate This, NSCollectionView collectionView, uint index);
	public static void UpdateDraggingItemsForDrag (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo);
	public static NSDragOperation ValidateDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref int dropIndex, NSCollectionViewDropOperation dropOperation);
	public static bool WriteItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSIndexSet indexes, NSPasteboard toPasteboard);
}
```

### New Type MonoMac.AppKit.NSComboBoxCellDataSource_Extensions

```
public static class NSComboBoxCellDataSource_Extensions {
	// methods
	public static string CompletedString (INSComboBoxCellDataSource This, NSComboBoxCell comboBox, string uncompletedString);
	public static uint IndexOfItem (INSComboBoxCellDataSource This, NSComboBoxCell comboBox, string value);
	public static int ItemCount (INSComboBoxCellDataSource This, NSComboBoxCell comboBox);
	public static MonoMac.Foundation.NSObject ObjectValueForItem (INSComboBoxCellDataSource This, NSComboBoxCell comboBox, int index);
}
```

### New Type MonoMac.AppKit.NSComboBoxDataSource_Extensions

```
public static class NSComboBoxDataSource_Extensions {
	// methods
	public static string CompletedString (INSComboBoxDataSource This, NSComboBox comboBox, string uncompletedString);
	public static int IndexOfItem (INSComboBoxDataSource This, NSComboBox comboBox, string value);
	public static int ItemCount (INSComboBoxDataSource This, NSComboBox comboBox);
	public static MonoMac.Foundation.NSObject ObjectValueForItem (INSComboBoxDataSource This, NSComboBox comboBox, int index);
}
```

### New Type MonoMac.AppKit.NSComboBoxDelegate

```
public class NSComboBoxDelegate : MonoMac.AppKit.NSTextFieldDelegate, INSComboBoxDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSTextFieldDelegate, MonoMac.Foundation.INSObjectProtocol {
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

### New Type MonoMac.AppKit.NSControlTextEditingDelegate

```
public class NSControlTextEditingDelegate : MonoMac.Foundation.NSObject, INSControlTextEditingDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSControlTextEditingDelegate ();
	public NSControlTextEditingDelegate (MonoMac.Foundation.NSCoder coder);
	public NSControlTextEditingDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSControlTextEditingDelegate (System.IntPtr handle);
	// methods
	public virtual bool DidFailToFormatString (NSControl control, string str, string error);
	public virtual void DidFailToValidatePartialString (NSControl control, string str, string error);
	public virtual bool DoCommandBySelector (NSControl control, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
	public virtual bool IsValidObject (NSControl control, MonoMac.Foundation.NSObject objectToValidate);
	public virtual bool TextShouldBeginEditing (NSControl control, NSText fieldEditor);
	public virtual bool TextShouldEndEditing (NSControl control, NSText fieldEditor);
}
```

### New Type MonoMac.AppKit.NSControlTextEditingDelegate_Extensions

```
public static class NSControlTextEditingDelegate_Extensions {
	// methods
	public static bool DidFailToFormatString (INSControlTextEditingDelegate This, NSControl control, string str, string error);
	public static void DidFailToValidatePartialString (INSControlTextEditingDelegate This, NSControl control, string str, string error);
	public static bool DoCommandBySelector (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public static string[] GetCompletions (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
	public static bool IsValidObject (INSControlTextEditingDelegate This, NSControl control, MonoMac.Foundation.NSObject objectToValidate);
	public static bool TextShouldBeginEditing (INSControlTextEditingDelegate This, NSControl control, NSText fieldEditor);
	public static bool TextShouldEndEditing (INSControlTextEditingDelegate This, NSControl control, NSText fieldEditor);
}
```

### New Type MonoMac.AppKit.NSDatePickerCellDelegate_Extensions

```
public static class NSDatePickerCellDelegate_Extensions {
	// methods
	public static void ValidateProposedDateValue (INSDatePickerCellDelegate This, NSDatePickerCell aDatePickerCell, ref MonoMac.Foundation.NSDate proposedDateValue, double proposedTimeInterval);
}
```

### New Type MonoMac.AppKit.NSDockTilePlugIn_Extensions

```
public static class NSDockTilePlugIn_Extensions {
}
```

### New Type MonoMac.AppKit.NSDraggingDestination_Extensions

```
public static class NSDraggingDestination_Extensions {
	// methods
	public static void ConcludeDragOperation (INSDraggingDestination This, NSDraggingInfo sender);
	public static void DraggingEnded (INSDraggingDestination This, NSDraggingInfo sender);
	public static NSDragOperation DraggingEntered (INSDraggingDestination This, NSDraggingInfo sender);
	public static void DraggingExited (INSDraggingDestination This, NSDraggingInfo sender);
	public static NSDragOperation DraggingUpdated (INSDraggingDestination This, NSDraggingInfo sender);
	public static bool GetWantsPeriodicDraggingUpdates (INSDraggingDestination This);
	public static bool PerformDragOperation (INSDraggingDestination This, NSDraggingInfo sender);
	public static bool PrepareForDragOperation (INSDraggingDestination This, NSDraggingInfo sender);
}
```

### New Type MonoMac.AppKit.NSDraggingSource_Extensions

```
public static class NSDraggingSource_Extensions {
	// methods
	public static void DraggedImageBeganAt (INSDraggingSource This, NSImage image, System.Drawing.PointF screenPoint);
	public static void DraggedImageEndedAtDeposited (INSDraggingSource This, NSImage image, System.Drawing.PointF screenPoint, bool deposited);
	public static void DraggedImageEndedAtOperation (INSDraggingSource This, NSImage image, System.Drawing.PointF screenPoint, NSDragOperation operation);
	public static void DraggedImageMovedTo (INSDraggingSource This, NSImage image, System.Drawing.PointF screenPoint);
	public static NSDragOperation DraggingSourceOperationMaskForLocal (INSDraggingSource This, bool flag);
	public static bool GetIgnoreModifierKeysWhileDragging (INSDraggingSource This);
	public static string[] NamesOfPromisedFilesDroppedAtDestination (INSDraggingSource This, MonoMac.Foundation.NSUrl dropDestination);
}
```

### New Type MonoMac.AppKit.NSDrawerDelegate_Extensions

```
public static class NSDrawerDelegate_Extensions {
	// methods
	public static void DrawerDidClose (INSDrawerDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DrawerDidOpen (INSDrawerDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool DrawerShouldClose (INSDrawerDelegate This, NSDrawer sender);
	public static bool DrawerShouldOpen (INSDrawerDelegate This, NSDrawer sender);
	public static void DrawerWillClose (INSDrawerDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DrawerWillOpen (INSDrawerDelegate This, MonoMac.Foundation.NSNotification notification);
	public static System.Drawing.SizeF DrawerWillResizeContents (INSDrawerDelegate This, NSDrawer sender, System.Drawing.SizeF toSize);
}
```

### New Type MonoMac.AppKit.NSGestureEvent

```
public sealed delegate NSGestureEvent : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSGestureEvent (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent);
}
```

### New Type MonoMac.AppKit.NSGestureProbe

```
public sealed delegate NSGestureProbe : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSGestureProbe (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (NSGestureRecognizer gestureRecognizer);
}
```

### New Type MonoMac.AppKit.NSGestureRecognizer

```
public class NSGestureRecognizer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSGestureRecognizer ();
	public NSGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSGestureRecognizer (System.IntPtr handle);
	public NSGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSGestureRecognizer (MonoMac.ObjCRuntime.Selector sel, NSGestureRecognizer.Token token);
	// fields
	public static MonoMac.ObjCRuntime.Selector ParametrizedSelector;
	// properties
	public virtual MonoMac.ObjCRuntime.Selector Action { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool DelaysKeyEvents { get; set; }
	public virtual bool DelaysMagnificationEvents { get; set; }
	public virtual bool DelaysOtherMouseButtonEvents { get; set; }
	public virtual bool DelaysPrimaryMouseButtonEvents { get; set; }
	public virtual bool DelaysRotationEvents { get; set; }
	public virtual bool DelaysSecondaryMouseButtonEvents { get; set; }
	public NSGestureRecognizerDelegate Delegate { get; set; }
	public virtual bool Enabled { get; set; }
	public NSGestureProbe ShouldBegin { get; set; }
	public NSGesturesProbe ShouldBeRequiredToFail { get; set; }
	public NSGestureEvent ShouldReceiveEvent { get; set; }
	public NSGesturesProbe ShouldRecognizeSimultaneously { get; set; }
	public NSGesturesProbe ShouldRequireFailure { get; set; }
	public virtual NSGestureRecognizerState State { get; }
	public virtual MonoMac.Foundation.NSObject Target { get; set; }
	public virtual NSView View { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual bool CanBePrevented (NSGestureRecognizer preventingGestureRecognizer);
	public virtual bool CanPrevent (NSGestureRecognizer preventedGestureRecognizer);
	protected override void Dispose (bool disposing);
	public virtual void FlagsChanged (NSEvent flagEvent);
	public virtual void KeyDown (NSEvent keyEvent);
	public virtual void KeyUp (NSEvent keyEvent);
	public virtual System.Drawing.PointF LocationInView (NSView view);
	public virtual void Magnify (NSEvent magnifyEvent);
	public virtual void MouseDown (NSEvent mouseEvent);
	public virtual void MouseDragged (NSEvent mouseEvent);
	public virtual void MouseUp (NSEvent mouseEvent);
	public virtual void OtherMouseDown (NSEvent mouseEvent);
	public virtual void OtherMouseDragged (NSEvent mouseEvent);
	public virtual void OtherMouseUp (NSEvent mouseEvent);
	public virtual void Reset ();
	public virtual void RightMouseDown (NSEvent mouseEvent);
	public virtual void RightMouseDragged (NSEvent mouseEvent);
	public virtual void RightMouseUp (NSEvent mouseEvent);
	public virtual void Rotate (NSEvent rotateEvent);
	public virtual bool ShouldBeRequiredToFailByGestureRecognizer (NSGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldRequireFailureOfGestureRecognizer (NSGestureRecognizer otherGestureRecognizer);
	public virtual void TabletPoint (NSEvent tabletEvent);

	// inner types
	public class Token : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public NSGestureRecognizer ();
	}
	public class ParameterlessDispatch : MonoMac.AppKit.NSGestureRecognizer+Token, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// methods
		public void Activated ();
	}
	public class ParametrizedDispatch : MonoMac.AppKit.NSGestureRecognizer+Token, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// methods
		public void Activated (NSGestureRecognizer sender);
	}
}
```

### New Type MonoMac.AppKit.NSGestureRecognizerDelegate

```
public class NSGestureRecognizerDelegate : MonoMac.Foundation.NSObject, INSGestureRecognizerDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSGestureRecognizerDelegate ();
	public NSGestureRecognizerDelegate (MonoMac.Foundation.NSCoder coder);
	public NSGestureRecognizerDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSGestureRecognizerDelegate (System.IntPtr handle);
	// methods
	public virtual bool ShouldBegin (NSGestureRecognizer gestureRecognizer);
	public virtual bool ShouldBeRequiredToFail (NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldReceiveEvent (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent);
	public virtual bool ShouldRecognizeSimultaneously (NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldRequireFailure (NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
}
```

### New Type MonoMac.AppKit.NSGestureRecognizerDelegate_Extensions

```
public static class NSGestureRecognizerDelegate_Extensions {
	// methods
	public static bool ShouldBegin (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer);
	public static bool ShouldBeRequiredToFail (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
	public static bool ShouldReceiveEvent (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent);
	public static bool ShouldRecognizeSimultaneously (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
	public static bool ShouldRequireFailure (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
}
```

### New Type MonoMac.AppKit.NSGestureRecognizerState

```
[Serializable]
public enum NSGestureRecognizerState {
	Began = 1,
	Cancelled = 4,
	Changed = 2,
	Ended = 3,
	Failed = 5,
	Possible = 0,
	Recognized = 3,
}
```

### New Type MonoMac.AppKit.NSGesturesProbe

```
public sealed delegate NSGesturesProbe : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSGesturesProbe (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (NSGestureRecognizer gestureRecognizer, NSGestureRecognizer otherGestureRecognizer);
}
```

### New Type MonoMac.AppKit.NSImageDelegate_Extensions

```
public static class NSImageDelegate_Extensions {
	// methods
	public static void DidLoadPartOfRepresentation (INSImageDelegate This, NSImage image, NSImageRep rep, int rows);
	public static void DidLoadRepresentation (INSImageDelegate This, NSImage image, NSImageRep rep, NSImageLoadStatus status);
	public static void DidLoadRepresentationHeader (INSImageDelegate This, NSImage image, NSImageRep rep);
	public static NSImage ImageDidNotDraw (INSImageDelegate This, MonoMac.Foundation.NSObject sender, System.Drawing.RectangleF aRect);
	public static void WillLoadRepresentation (INSImageDelegate This, NSImage image, NSImageRep rep);
}
```

### New Type MonoMac.AppKit.NSImageResizingMode

```
[Serializable]
public enum NSImageResizingMode {
	Stretch = 0,
	Tile = 1,
}
```

### New Type MonoMac.AppKit.NSLayoutManagerDelegate_Extensions

```
public static class NSLayoutManagerDelegate_Extensions {
	// methods
	public static void LayoutCompleted (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, bool layoutFinishedFlag);
	public static void LayoutInvalidated (INSLayoutManagerDelegate This, NSLayoutManager sender);
	public static MonoMac.Foundation.NSDictionary ShouldUseTemporaryAttributes (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, MonoMac.Foundation.NSDictionary temporaryAttributes, bool drawingToScreen, int charIndex, System.IntPtr effectiveCharRange);
}
```

### New Type MonoMac.AppKit.NSMagnificationGestureRecognizer

```
public class NSMagnificationGestureRecognizer : MonoMac.AppKit.NSGestureRecognizer, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSMagnificationGestureRecognizer ();
	public NSMagnificationGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSMagnificationGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSMagnificationGestureRecognizer (System.IntPtr handle);
	public NSMagnificationGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSMagnificationGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSMagnificationGestureRecognizer (System.Action<NSMagnificationGestureRecognizer> action);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Magnification { get; set; }
}
```

### New Type MonoMac.AppKit.NSMatrixDelegate_Extensions

```
public static class NSMatrixDelegate_Extensions {
	// methods
	public static bool DidFailToFormatString (INSMatrixDelegate This, NSControl control, string str, string error);
	public static void DidFailToValidatePartialString (INSMatrixDelegate This, NSControl control, string str, string error);
	public static bool DoCommandBySelector (INSMatrixDelegate This, NSControl control, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public static string[] GetCompletions (INSMatrixDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
	public static bool IsValidObject (INSMatrixDelegate This, NSControl control, MonoMac.Foundation.NSObject objectToValidate);
	public static bool TextShouldBeginEditing (INSMatrixDelegate This, NSControl control, NSText fieldEditor);
	public static bool TextShouldEndEditing (INSMatrixDelegate This, NSControl control, NSText fieldEditor);
}
```

### New Type MonoMac.AppKit.NSMenuDelegate_Extensions

```
public static class NSMenuDelegate_Extensions {
	// methods
	public static System.Drawing.RectangleF ConfinementRectForMenu (INSMenuDelegate This, NSMenu menu, NSScreen screen);
	public static bool HasKeyEquivalentForEvent (INSMenuDelegate This, NSMenu menu, NSEvent theEvent, MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public static void MenuDidClose (INSMenuDelegate This, NSMenu menu);
	public static int MenuItemCount (INSMenuDelegate This, NSMenu menu);
	public static void MenuWillOpen (INSMenuDelegate This, NSMenu menu);
	public static void NeedsUpdate (INSMenuDelegate This, NSMenu menu);
	public static bool UpdateItem (INSMenuDelegate This, NSMenu menu, NSMenuItem item, int atIndex, bool shouldCancel);
}
```

### New Type MonoMac.AppKit.NSModalResponse

```
[Serializable]
public enum NSModalResponse {
	Abort = -1001,
	Continue = -1002,
	Stop = -1000,
}
```

### New Type MonoMac.AppKit.NSOpenSavePanelDelegate_Extensions

```
public static class NSOpenSavePanelDelegate_Extensions {
	// methods
	public static MonoMac.Foundation.NSComparisonResult CompareFilenames (INSOpenSavePanelDelegate This, NSSavePanel panel, string name1, string name2, bool caseSensitive);
	public static void DidChangeToDirectory (INSOpenSavePanelDelegate This, NSSavePanel panel, MonoMac.Foundation.NSUrl newDirectoryUrl);
	public static void DirectoryDidChange (INSOpenSavePanelDelegate This, NSSavePanel panel, string path);
	public static bool IsValidFilename (INSOpenSavePanelDelegate This, NSSavePanel panel, string fileName);
	public static void SelectionDidChange (INSOpenSavePanelDelegate This, NSSavePanel panel);
	public static bool ShouldEnableUrl (INSOpenSavePanelDelegate This, NSSavePanel panel, MonoMac.Foundation.NSUrl url);
	public static bool ShouldShowFilename (INSOpenSavePanelDelegate This, NSSavePanel panel, string filename);
	public static string UserEnteredFilename (INSOpenSavePanelDelegate This, NSSavePanel panel, string filename, bool confirmed);
	public static bool ValidateUrl (INSOpenSavePanelDelegate This, NSSavePanel panel, MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSError outError);
	public static void WillExpand (INSOpenSavePanelDelegate This, NSSavePanel panel, bool expanding);
}
```

### New Type MonoMac.AppKit.NSOutlineViewDataSource_Extensions

```
public static class NSOutlineViewDataSource_Extensions {
	// methods
	public static bool AcceptDrop (INSOutlineViewDataSource This, NSOutlineView outlineView, NSDraggingInfo info, MonoMac.Foundation.NSObject item, int index);
	public static void DraggingSessionEnded (INSOutlineViewDataSource This, NSOutlineView outlineView, NSDraggingSession session, System.Drawing.PointF screenPoint, NSDragOperation operation);
	public static void DraggingSessionWillBegin (INSOutlineViewDataSource This, NSOutlineView outlineView, NSDraggingSession session, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSArray draggedItems);
	public static string[] FilesDropped (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSUrl dropDestination, MonoMac.Foundation.NSArray items);
	public static MonoMac.Foundation.NSObject GetChild (INSOutlineViewDataSource This, NSOutlineView outlineView, int childIndex, MonoMac.Foundation.NSObject item);
	public static int GetChildrenCount (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static MonoMac.Foundation.NSObject GetObjectValue (INSOutlineViewDataSource This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static bool ItemExpandable (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static MonoMac.Foundation.NSObject ItemForPersistentObject (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject theObject);
	public static bool OutlineViewwriteItemstoPasteboard (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSArray items, NSPasteboard pboard);
	public static NSPasteboardWriting PasteboardWriterForItem (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static MonoMac.Foundation.NSObject PersistentObjectForItem (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static void SetObjectValue (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSObject theObject, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static void SortDescriptorsChanged (INSOutlineViewDataSource This, NSOutlineView outlineView, MonoMac.Foundation.NSSortDescriptor[] oldDescriptors);
	public static void UpdateDraggingItemsForDrag (INSOutlineViewDataSource This, NSOutlineView outlineView, NSDraggingInfo draggingInfo);
	public static NSDragOperation ValidateDrop (INSOutlineViewDataSource This, NSOutlineView outlineView, NSDraggingInfo info, MonoMac.Foundation.NSObject item, int index);
}
```

### New Type MonoMac.AppKit.NSOutlineViewDelegate_Extensions

```
public static class NSOutlineViewDelegate_Extensions {
	// methods
	public static void ColumnDidMove (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void ColumnDidResize (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidAddRowView (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableRowView rowView, int row);
	public static void DidClickTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn);
	public static void DidDragTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn);
	public static void DidRemoveRowView (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableRowView rowView, int row);
	public static NSCell GetCell (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static MonoMac.Foundation.NSObject GetNextTypeSelectMatch (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject startItem, MonoMac.Foundation.NSObject endItem, string searchString);
	public static float GetRowHeight (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static MonoMac.Foundation.NSIndexSet GetSelectionIndexes (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSIndexSet proposedSelectionIndexes);
	public static string GetSelectString (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static float GetSizeToFitColumnWidth (INSOutlineViewDelegate This, NSOutlineView outlineView, int column);
	public static NSView GetView (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static bool IsGroupItem (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static void ItemDidCollapse (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void ItemDidExpand (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void ItemWillCollapse (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void ItemWillExpand (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void MouseDown (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn);
	public static NSTableRowView RowViewForItem (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static void SelectionDidChange (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void SelectionIsChanging (INSOutlineViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool SelectionShouldChange (INSOutlineViewDelegate This, NSOutlineView outlineView);
	public static bool ShouldCollapseItem (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static bool ShouldEditTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static bool ShouldExpandItem (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static bool ShouldReorder (INSOutlineViewDelegate This, NSOutlineView outlineView, int columnIndex, int newColumnIndex);
	public static bool ShouldSelectItem (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static bool ShouldSelectTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn);
	public static bool ShouldShowCellExpansion (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static bool ShouldShowOutlineCell (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
	public static bool ShouldTrackCell (INSOutlineViewDelegate This, NSOutlineView outlineView, NSCell cell, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static bool ShouldTypeSelect (INSOutlineViewDelegate This, NSOutlineView outlineView, NSEvent theEvent, string searchString);
	public static string ToolTipForCell (INSOutlineViewDelegate This, NSOutlineView outlineView, NSCell cell, ref System.Drawing.RectangleF rect, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item, System.Drawing.PointF mouseLocation);
	public static NSView ViewForTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static void WillDisplayCell (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject cell, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
	public static void WillDisplayOutlineCell (INSOutlineViewDelegate This, NSOutlineView outlineView, MonoMac.Foundation.NSObject cell, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
}
```

### New Type MonoMac.AppKit.NSPageControllerGetFrame

```
public sealed delegate NSPageControllerGetFrame : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSPageControllerGetFrame (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSPageController pageController, MonoMac.Foundation.NSObject targetObject, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF EndInvoke (System.IAsyncResult result);
	public virtual System.Drawing.RectangleF Invoke (NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
}
```

### New Type MonoMac.AppKit.NSPageControllerGetIdentifier

```
public sealed delegate NSPageControllerGetIdentifier : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSPageControllerGetIdentifier (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSPageController pageController, MonoMac.Foundation.NSObject targetObject, System.AsyncCallback callback, object object);
	public virtual string EndInvoke (System.IAsyncResult result);
	public virtual string Invoke (NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
}
```

### New Type MonoMac.AppKit.NSPageControllerGetViewController

```
public sealed delegate NSPageControllerGetViewController : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSPageControllerGetViewController (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSPageController pageController, string identifier, System.AsyncCallback callback, object object);
	public virtual NSViewController EndInvoke (System.IAsyncResult result);
	public virtual NSViewController Invoke (NSPageController pageController, string identifier);
}
```

### New Type MonoMac.AppKit.NSPageControllerPrepareViewControllerEventArgs

```
public class NSPageControllerPrepareViewControllerEventArgs : System.EventArgs {
	// constructors
	public NSPageControllerPrepareViewControllerEventArgs (NSViewController viewController, MonoMac.Foundation.NSObject targetObject);
	// properties
	public MonoMac.Foundation.NSObject TargetObject { get; set; }
	public NSViewController ViewController { get; set; }
}
```

### New Type MonoMac.AppKit.NSPanGestureRecognizer

```
public class NSPanGestureRecognizer : MonoMac.AppKit.NSGestureRecognizer, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSPanGestureRecognizer ();
	public NSPanGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSPanGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSPanGestureRecognizer (System.IntPtr handle);
	public NSPanGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSPanGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSPanGestureRecognizer (System.Action<NSPanGestureRecognizer> action);
	// properties
	public virtual uint ButtonMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void SetTranslation (System.Drawing.PointF translation, NSView view);
	public virtual System.Drawing.PointF TranslationInView (NSView view);
	public virtual System.Drawing.PointF VelocityInView (NSView view);
}
```

### New Type MonoMac.AppKit.NSPasteboardItemDataProvider_Extensions

```
public static class NSPasteboardItemDataProvider_Extensions {
}
```

### New Type MonoMac.AppKit.NSPasteboardReading_Extensions

```
public static class NSPasteboardReading_Extensions {
}
```

### New Type MonoMac.AppKit.NSPasteboardWriting_Extensions

```
public static class NSPasteboardWriting_Extensions {
	// methods
	public static MonoMac.Foundation.NSObject GetPasteboardPropertyListForType (INSPasteboardWriting This, string type);
	public static string[] GetWritableTypesForPasteboard (INSPasteboardWriting This, NSPasteboard pasteboard);
	public static NSPasteboardWritingOptions GetWritingOptionsForType (INSPasteboardWriting This, string type, NSPasteboard pasteboard);
}
```

### New Type MonoMac.AppKit.NSPathCellDelegate_Extensions

```
public static class NSPathCellDelegate_Extensions {
	// methods
	public static void WillDisplayOpenPanel (INSPathCellDelegate This, NSPathCell pathCell, NSOpenPanel openPanel);
	public static void WillPopupMenu (INSPathCellDelegate This, NSPathCell pathCell, NSMenu menu);
}
```

### New Type MonoMac.AppKit.NSPathControlDelegate_Extensions

```
public static class NSPathControlDelegate_Extensions {
	// methods
	public static bool ShouldDragItem (INSPathControlDelegate This, NSPathControl pathControl, NSPathControlItem pathItem, NSPasteboard pasteboard);
}
```

### New Type MonoMac.AppKit.NSPathControlItem

```
public class NSPathControlItem : MonoMac.AppKit.NSObjectController, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSPathControlItem ();
	public NSPathControlItem (MonoMac.Foundation.NSCoder coder);
	public NSPathControlItem (MonoMac.Foundation.NSObjectFlag t);
	public NSPathControlItem (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSAttributedString AttributedTitle { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSImage Image { get; set; }
	public virtual string Title { get; set; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AppKit.NSPdfImageRep

```
public class NSPdfImageRep : MonoMac.AppKit.NSImageRep, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSPdfImageRep (MonoMac.Foundation.NSCoder coder);
	public NSPdfImageRep (MonoMac.Foundation.NSObjectFlag t);
	public NSPdfImageRep (System.IntPtr handle);
	public NSPdfImageRep (MonoMac.Foundation.NSData pdfData);
	// properties
	public virtual System.Drawing.RectangleF Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int CurrentPage { get; set; }
	public virtual int PageCount { get; }
	public virtual MonoMac.Foundation.NSData PdfRepresentation { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AppKit.NSPopoverDelegate_Extensions

```
public static class NSPopoverDelegate_Extensions {
	// methods
	public static void DidClose (INSPopoverDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidShow (INSPopoverDelegate This, MonoMac.Foundation.NSNotification notification);
	public static NSWindow GetDetachableWindowForPopover (INSPopoverDelegate This, NSPopover popover);
	public static bool ShouldClose (INSPopoverDelegate This, NSPopover popover);
	public static void WillClose (INSPopoverDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillShow (INSPopoverDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.NSPressGestureRecognizer

```
public class NSPressGestureRecognizer : MonoMac.AppKit.NSGestureRecognizer, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSPressGestureRecognizer ();
	public NSPressGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSPressGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSPressGestureRecognizer (System.IntPtr handle);
	public NSPressGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSPressGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSPressGestureRecognizer (System.Action<NSPressGestureRecognizer> action);
	// properties
	public virtual float AllowableMovement { get; set; }
	public virtual uint ButtonMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual double MinimumPressDuration { get; set; }
}
```

### New Type MonoMac.AppKit.NSPrintPanelAccessorizing_Extensions

```
public static class NSPrintPanelAccessorizing_Extensions {
}
```

### New Type MonoMac.AppKit.NSRotationGestureRecognizer

```
public class NSRotationGestureRecognizer : MonoMac.AppKit.NSGestureRecognizer, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSRotationGestureRecognizer ();
	public NSRotationGestureRecognizer (MonoMac.Foundation.NSCoder coder);
	public NSRotationGestureRecognizer (MonoMac.Foundation.NSObjectFlag t);
	public NSRotationGestureRecognizer (System.IntPtr handle);
	public NSRotationGestureRecognizer (MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public NSRotationGestureRecognizer (MonoMac.Foundation.NSAction action);
	public NSRotationGestureRecognizer (System.Action<NSRotationGestureRecognizer> action);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rotation { get; set; }
	public virtual float RotationInDegrees { get; set; }
}
```

### New Type MonoMac.AppKit.NSRuleEditorDelegate_Extensions

```
public static class NSRuleEditorDelegate_Extensions {
	// methods
	public static void Changed (INSRuleEditorDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void EditingBegan (INSRuleEditorDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void EditingEnded (INSRuleEditorDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.NSSeguePerforming

```
public class NSSeguePerforming : MonoMac.Foundation.NSObject, INSSeguePerforming, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSSeguePerforming ();
	public NSSeguePerforming (MonoMac.Foundation.NSCoder coder);
	public NSSeguePerforming (MonoMac.Foundation.NSObjectFlag t);
	public NSSeguePerforming (System.IntPtr handle);
	// methods
	public virtual void PerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
	public virtual void PrepareForSegue (NSStoryboardSegue segue, MonoMac.Foundation.NSObject sender);
	public virtual bool ShouldPerformSegue (string identifier, MonoMac.Foundation.NSObject sender);
}
```

### New Type MonoMac.AppKit.NSSeguePerforming_Extensions

```
public static class NSSeguePerforming_Extensions {
	// methods
	public static void PerformSegue (INSSeguePerforming This, string identifier, MonoMac.Foundation.NSObject sender);
	public static void PrepareForSegue (INSSeguePerforming This, NSStoryboardSegue segue, MonoMac.Foundation.NSObject sender);
	public static bool ShouldPerformSegue (INSSeguePerforming This, string identifier, MonoMac.Foundation.NSObject sender);
}
```

### New Type MonoMac.AppKit.NSSharingServiceDelegate_Extensions

```
public static class NSSharingServiceDelegate_Extensions {
	// methods
	public static void DidFailToShareItems (INSSharingServiceDelegate This, NSSharingService sharingService, MonoMac.Foundation.NSObject[] items, MonoMac.Foundation.NSError error);
	public static void DidShareItems (INSSharingServiceDelegate This, NSSharingService sharingService, MonoMac.Foundation.NSObject[] items);
	public static System.Drawing.RectangleF SourceFrameOnScreenForShareItem (INSSharingServiceDelegate This, NSSharingService sharingService, INSPasteboardWriting item);
	public static NSWindow SourceWindowForShareItems (INSSharingServiceDelegate This, NSSharingService sharingService, MonoMac.Foundation.NSObject[] items, NSSharingContentScope sharingContentScope);
	public static NSImage TransitionImageForShareItem (INSSharingServiceDelegate This, NSSharingService sharingService, INSPasteboardWriting item, System.Drawing.RectangleF contentRect);
	public static void WillShareItems (INSSharingServiceDelegate This, NSSharingService sharingService, MonoMac.Foundation.NSObject[] items);
}
```

### New Type MonoMac.AppKit.NSSharingServicePickerDelegate_Extensions

```
public static class NSSharingServicePickerDelegate_Extensions {
	// methods
	public static NSSharingServiceDelegate DelegateForSharingService (INSSharingServicePickerDelegate This, NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
	public static void DidChooseSharingService (INSSharingServicePickerDelegate This, NSSharingServicePicker sharingServicePicker, NSSharingService service);
	public static NSSharingService[] SharingServicesForItems (INSSharingServicePickerDelegate This, NSSharingServicePicker sharingServicePicker, MonoMac.Foundation.NSObject[] items, NSSharingService[] proposedServices);
}
```

### New Type MonoMac.AppKit.NSSoundDelegate_Extensions

```
public static class NSSoundDelegate_Extensions {
	// methods
	public static void DidFinishPlaying (INSSoundDelegate This, NSSound sound, bool finished);
}
```

### New Type MonoMac.AppKit.NSSpeechRecognizerDelegate_Extensions

```
public static class NSSpeechRecognizerDelegate_Extensions {
	// methods
	public static void DidRecognizeCommand (INSSpeechRecognizerDelegate This, NSSpeechRecognizer sender, string command);
}
```

### New Type MonoMac.AppKit.NSSpeechSynthesizerDelegate_Extensions

```
public static class NSSpeechSynthesizerDelegate_Extensions {
	// methods
	public static void DidEncounterError (INSSpeechSynthesizerDelegate This, NSSpeechSynthesizer sender, uint characterIndex, string theString, string message);
	public static void DidEncounterSyncMessage (INSSpeechSynthesizerDelegate This, NSSpeechSynthesizer sender, string message);
	public static void DidFinishSpeaking (INSSpeechSynthesizerDelegate This, NSSpeechSynthesizer sender, bool finishedSpeaking);
	public static void WillSpeakPhoneme (INSSpeechSynthesizerDelegate This, NSSpeechSynthesizer sender, short phonemeOpcode);
	public static void WillSpeakWord (INSSpeechSynthesizerDelegate This, NSSpeechSynthesizer sender, MonoMac.Foundation.NSRange wordCharacterRange, string ofString);
}
```

### New Type MonoMac.AppKit.NSSplitViewController

```
public class NSSplitViewController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, INSSeguePerforming, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSSplitViewController ();
	public NSSplitViewController (MonoMac.Foundation.NSCoder coder);
	public NSSplitViewController (MonoMac.Foundation.NSObjectFlag t);
	public NSSplitViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSSplitView SplitView { get; set; }
	public virtual NSSplitViewItem[] SplitViewItems { get; set; }
	// methods
	public virtual void AddSplitViewItem (NSSplitViewItem splitViewItem);
	protected override void Dispose (bool disposing);
	public virtual NSSplitViewItem GetSplitViewItem (NSViewController viewController);
	public virtual void InsertSplitViewItem (NSSplitViewItem splitViewItem, int index);
	public virtual void RemoveSplitViewItem (NSSplitViewItem splitViewItem);
}
```

### New Type MonoMac.AppKit.NSSplitViewDelegate_Extensions

```
public static class NSSplitViewDelegate_Extensions {
	// methods
	public static bool CanCollapse (INSSplitViewDelegate This, NSSplitView splitView, NSView subview);
	public static float ConstrainSplitPosition (INSSplitViewDelegate This, NSSplitView splitView, float proposedPosition, int subviewDividerIndex);
	public static void DidResizeSubviews (INSSplitViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static System.Drawing.RectangleF GetAdditionalEffectiveRect (INSSplitViewDelegate This, NSSplitView splitView, int dividerIndex);
	public static System.Drawing.RectangleF GetEffectiveRect (INSSplitViewDelegate This, NSSplitView splitView, System.Drawing.RectangleF proposedEffectiveRect, System.Drawing.RectangleF drawnRect, int dividerIndex);
	public static void Resize (INSSplitViewDelegate This, NSSplitView splitView, System.Drawing.SizeF oldSize);
	public static float SetMaxCoordinateOfSubview (INSSplitViewDelegate This, NSSplitView splitView, float proposedMaximumPosition, int subviewDividerIndex);
	public static float SetMinCoordinateOfSubview (INSSplitViewDelegate This, NSSplitView splitView, float proposedMinimumPosition, int subviewDividerIndex);
	public static bool ShouldAdjustSize (INSSplitViewDelegate This, NSSplitView splitView, NSView view);
	public static bool ShouldCollapseForDoubleClick (INSSplitViewDelegate This, NSSplitView splitView, NSView subview, int doubleClickAtDividerIndex);
	public static bool ShouldHideDivider (INSSplitViewDelegate This, NSSplitView splitView, int dividerIndex);
	public static void SplitViewWillResizeSubviews (INSSplitViewDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.NSSplitViewItem

```
public class NSSplitViewItem : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSSplitViewItem ();
	public NSSplitViewItem (MonoMac.Foundation.NSCoder coder);
	public NSSplitViewItem (MonoMac.Foundation.NSObjectFlag t);
	public NSSplitViewItem (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSDictionary Animations { get; set; }
	public virtual MonoMac.Foundation.NSObject Animator { get; }
	public virtual bool CanCollapse { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Collapsed { get; set; }
	public virtual float HoldingPriority { get; set; }
	public virtual NSViewController ViewController { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject AnimationFor (MonoMac.Foundation.NSString key);
	public static MonoMac.Foundation.NSObject DefaultAnimationFor (MonoMac.Foundation.NSString key);
	protected override void Dispose (bool disposing);
	public static NSSplitViewItem FromViewController (NSViewController viewController);
}
```

### New Type MonoMac.AppKit.NSStackView

```
public class NSStackView : MonoMac.AppKit.NSView, INSDraggingDestination, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSStackView ();
	public NSStackView (MonoMac.Foundation.NSCoder coder);
	public NSStackView (MonoMac.Foundation.NSObjectFlag t);
	public NSStackView (System.IntPtr handle);
	// properties
	public virtual NSLayoutAttribute Alignment { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public NSStackViewDelegate Delegate { get; set; }
	public virtual NSView[] DetachedViews { get; }
	public virtual NSEdgeInsets EdgeInsets { get; set; }
	public virtual bool HasEqualSpacing { get; set; }
	public virtual NSUserInterfaceLayoutOrientation Orientation { get; set; }
	public virtual float Spacing { get; set; }
	public virtual NSView[] Views { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual void AddView (NSView aView, NSStackViewGravity gravity);
	public virtual float ClippingResistancePriorityForOrientation (NSLayoutConstraintOrientation orientation);
	public virtual float CustomSpacingAfterView (NSView aView);
	protected override void Dispose (bool disposing);
	public static NSStackView FromViews (NSView[] views);
	public virtual float HuggingPriority (NSLayoutConstraintOrientation orientation);
	public virtual void InsertView (NSView aView, uint index, NSStackViewGravity gravity);
	public virtual void RemoveView (NSView aView);
	public virtual void SetClippingResistancePriority (float clippingResistancePriority, NSLayoutConstraintOrientation orientation);
	public virtual void SetCustomSpacing (float spacing, NSView aView);
	public virtual void SetHuggingPriority (float huggingPriority, NSLayoutConstraintOrientation orientation);
	public virtual void SetViews (NSView[] views, NSStackViewGravity gravity);
	public virtual void SetVisibilityPriority (float priority, NSView aView);
	public virtual NSView[] ViewsInGravity (NSStackViewGravity gravity);
	public virtual float VisibilityPriority (NSView aView);
}
```

### New Type MonoMac.AppKit.NSStackViewDelegate

```
public class NSStackViewDelegate : MonoMac.Foundation.NSObject, INSStackViewDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSStackViewDelegate ();
	public NSStackViewDelegate (MonoMac.Foundation.NSCoder coder);
	public NSStackViewDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSStackViewDelegate (System.IntPtr handle);
	// methods
	public virtual void DidReattachViews (NSStackView stackView, NSView[] views);
	public virtual void WillDetachViews (NSStackView stackView, NSView[] views);
}
```

### New Type MonoMac.AppKit.NSStackViewDelegate_Extensions

```
public static class NSStackViewDelegate_Extensions {
	// methods
	public static void DidReattachViews (INSStackViewDelegate This, NSStackView stackView, NSView[] views);
	public static void WillDetachViews (INSStackViewDelegate This, NSStackView stackView, NSView[] views);
}
```

### New Type MonoMac.AppKit.NSStackViewGravity

```
[Serializable]
public enum NSStackViewGravity {
	Bottom = 3,
	Center = 2,
	Leading = 1,
	Top = 1,
	Trailing = 3,
}
```

### New Type MonoMac.AppKit.NSStackViewVisibilityPriority

```
[Serializable]
public enum NSStackViewVisibilityPriority {
	DetachOnlyIfNecessary = 900,
	Musthold = 1000,
	NotVisible = 0,
}
```

### New Type MonoMac.AppKit.NSStatusBarButton

```
public class NSStatusBarButton : MonoMac.AppKit.NSButton, INSDraggingDestination, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSStatusBarButton ();
	public NSStatusBarButton (MonoMac.Foundation.NSCoder coder);
	public NSStatusBarButton (MonoMac.Foundation.NSObjectFlag t);
	public NSStatusBarButton (System.IntPtr handle);
	public NSStatusBarButton (System.Drawing.RectangleF frameRect);
	// properties
	public virtual bool AppearsDisabled { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AppKit.NSStoryboard

```
public class NSStoryboard : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSStoryboard ();
	public NSStoryboard (MonoMac.Foundation.NSCoder coder);
	public NSStoryboard (MonoMac.Foundation.NSObjectFlag t);
	public NSStoryboard (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static NSStoryboard FromName (string name, MonoMac.Foundation.NSBundle storyboardBundleOrNil);
	public virtual MonoMac.Foundation.NSObject InstantiateControllerWithIdentifier (string identifier);
	public virtual MonoMac.Foundation.NSObject InstantiateInitialController ();
}
```

### New Type MonoMac.AppKit.NSStoryboardSegue

```
public class NSStoryboardSegue : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSStoryboardSegue ();
	public NSStoryboardSegue (MonoMac.Foundation.NSCoder coder);
	public NSStoryboardSegue (MonoMac.Foundation.NSObjectFlag t);
	public NSStoryboardSegue (System.IntPtr handle);
	public NSStoryboardSegue (string identifier, MonoMac.Foundation.NSObject sourceController, MonoMac.Foundation.NSObject destinationController);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSObject DestinationController { get; }
	public virtual string Identifier { get; }
	public virtual MonoMac.Foundation.NSObject SourceController { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static NSStoryboardSegue FromIdentifier (string identifier, MonoMac.Foundation.NSObject sourceController, MonoMac.Foundation.NSObject destinationController, System.Action performHandler);
	public virtual void Perform ();
}
```

### New Type MonoMac.AppKit.NSStringDrawing

```
public static class NSStringDrawing {
	// methods
	public static void DrawAtPoint (string This, System.Drawing.PointF point, MonoMac.Foundation.NSDictionary attributes);
	public static void DrawInRect (string This, System.Drawing.RectangleF rect, MonoMac.Foundation.NSDictionary attributes);
	public static System.Drawing.SizeF StringSize (string This, MonoMac.Foundation.NSDictionary attributes);
}
```

### New Type MonoMac.AppKit.NSStringDrawing_NSAttributedString

```
public static class NSStringDrawing_NSAttributedString {
	// methods
	public static void DrawAtPoint (MonoMac.Foundation.NSAttributedString This, System.Drawing.PointF point);
	public static void DrawInRect (MonoMac.Foundation.NSAttributedString This, System.Drawing.RectangleF rect);
	public static System.Drawing.SizeF GetSize (MonoMac.Foundation.NSAttributedString This);
}
```

### New Type MonoMac.AppKit.NSStringDrawing_NSString

```
public static class NSStringDrawing_NSString {
	// methods
	public static void DrawAtPoint (MonoMac.Foundation.NSString This, System.Drawing.PointF point, MonoMac.Foundation.NSDictionary attributes);
	public static void DrawInRect (MonoMac.Foundation.NSString This, System.Drawing.RectangleF rect, MonoMac.Foundation.NSDictionary attributes);
	public static System.Drawing.SizeF StringSize (MonoMac.Foundation.NSString This, MonoMac.Foundation.NSDictionary attributes);
}
```

### New Type MonoMac.AppKit.NSTableViewDataSource_Extensions

```
public static class NSTableViewDataSource_Extensions {
	// methods
	public static bool AcceptDrop (INSTableViewDataSource This, NSTableView tableView, NSDraggingInfo info, int row, NSTableViewDropOperation dropOperation);
	public static void DraggingSessionEnded (INSTableViewDataSource This, NSTableView tableView, NSDraggingSession draggingSession, System.Drawing.PointF endedAtScreenPoint, NSDragOperation operation);
	public static void DraggingSessionWillBegin (INSTableViewDataSource This, NSTableView tableView, NSDraggingSession draggingSession, System.Drawing.PointF willBeginAtScreenPoint, MonoMac.Foundation.NSIndexSet rowIndexes);
	public static string[] FilesDropped (INSTableViewDataSource This, NSTableView tableView, MonoMac.Foundation.NSUrl dropDestination, MonoMac.Foundation.NSIndexSet indexSet);
	public static MonoMac.Foundation.NSObject GetObjectValue (INSTableViewDataSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static NSPasteboardWriting GetPasteboardWriterForRow (INSTableViewDataSource This, NSTableView tableView, int row);
	public static int GetRowCount (INSTableViewDataSource This, NSTableView tableView);
	public static void SetObjectValue (INSTableViewDataSource This, NSTableView tableView, MonoMac.Foundation.NSObject theObject, NSTableColumn tableColumn, int row);
	public static void SortDescriptorsChanged (INSTableViewDataSource This, NSTableView tableView, MonoMac.Foundation.NSSortDescriptor[] oldDescriptors);
	public static void UpdateDraggingItems (INSTableViewDataSource This, NSTableView tableView, NSDraggingInfo draggingInfo);
	public static NSDragOperation ValidateDrop (INSTableViewDataSource This, NSTableView tableView, NSDraggingInfo info, int row, NSTableViewDropOperation dropOperation);
	public static bool WriteRows (INSTableViewDataSource This, NSTableView tableView, MonoMac.Foundation.NSIndexSet rowIndexes, NSPasteboard pboard);
}
```

### New Type MonoMac.AppKit.NSTableViewDelegate_Extensions

```
public static class NSTableViewDelegate_Extensions {
	// methods
	public static void ColumnDidMove (INSTableViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void ColumnDidResize (INSTableViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static NSTableRowView CoreGetRowView (INSTableViewDelegate This, NSTableView tableView, int row);
	public static void DidAddRowView (INSTableViewDelegate This, NSTableView tableView, NSTableRowView rowView, int row);
	public static void DidClickTableColumn (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn);
	public static void DidDragTableColumn (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn);
	public static void DidRemoveRowView (INSTableViewDelegate This, NSTableView tableView, NSTableRowView rowView, int row);
	public static NSCell GetDataCell (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static int GetNextTypeSelectMatch (INSTableViewDelegate This, NSTableView tableView, int startRow, int endRow, string searchString);
	public static float GetRowHeight (INSTableViewDelegate This, NSTableView tableView, int row);
	public static MonoMac.Foundation.NSIndexSet GetSelectionIndexes (INSTableViewDelegate This, NSTableView tableView, MonoMac.Foundation.NSIndexSet proposedSelectionIndexes);
	public static string GetSelectString (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static float GetSizeToFitColumnWidth (INSTableViewDelegate This, NSTableView tableView, int column);
	public static MonoMac.Foundation.NSString GetToolTip (INSTableViewDelegate This, NSTableView tableView, NSCell cell, ref System.Drawing.RectangleF rect, NSTableColumn tableColumn, int row, System.Drawing.PointF mouseLocation);
	public static NSView GetViewForItem (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool IsGroupRow (INSTableViewDelegate This, NSTableView tableView, int row);
	public static void MouseDownInHeaderOfTableColumn (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn);
	public static void SelectionDidChange (INSTableViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void SelectionIsChanging (INSTableViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool SelectionShouldChange (INSTableViewDelegate This, NSTableView tableView);
	public static bool ShouldEditTableColumn (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool ShouldReorder (INSTableViewDelegate This, NSTableView tableView, int columnIndex, int newColumnIndex);
	public static bool ShouldSelectRow (INSTableViewDelegate This, NSTableView tableView, int row);
	public static bool ShouldSelectTableColumn (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn);
	public static bool ShouldShowCellExpansion (INSTableViewDelegate This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool ShouldTrackCell (INSTableViewDelegate This, NSTableView tableView, NSCell cell, NSTableColumn tableColumn, int row);
	public static bool ShouldTypeSelect (INSTableViewDelegate This, NSTableView tableView, NSEvent theEvent, string searchString);
	public static void WillDisplayCell (INSTableViewDelegate This, NSTableView tableView, MonoMac.Foundation.NSObject cell, NSTableColumn tableColumn, int row);
}
```

### New Type MonoMac.AppKit.NSTableViewSource_Extensions

```
public static class NSTableViewSource_Extensions {
	// methods
	public static bool AcceptDrop (INSTableViewSource This, NSTableView tableView, NSDraggingInfo info, int row, NSTableViewDropOperation dropOperation);
	public static void ColumnDidMove (INSTableViewSource This, MonoMac.Foundation.NSNotification notification);
	public static void ColumnDidResize (INSTableViewSource This, MonoMac.Foundation.NSNotification notification);
	public static void DidAddRowView (INSTableViewSource This, NSTableView tableView, NSTableRowView rowView, int row);
	public static void DidClickTableColumn (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn);
	public static void DidDragTableColumn (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn);
	public static void DidRemoveRowView (INSTableViewSource This, NSTableView tableView, NSTableRowView rowView, int row);
	public static void DraggingSessionEnded (INSTableViewSource This, NSTableView tableView, NSDraggingSession draggingSession, System.Drawing.PointF endedAtScreenPoint, NSDragOperation operation);
	public static void DraggingSessionWillBegin (INSTableViewSource This, NSTableView tableView, NSDraggingSession draggingSession, System.Drawing.PointF willBeginAtScreenPoint, MonoMac.Foundation.NSIndexSet rowIndexes);
	public static string[] FilesDropped (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSUrl dropDestination, MonoMac.Foundation.NSIndexSet indexSet);
	public static NSCell GetCell (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static int GetNextTypeSelectMatch (INSTableViewSource This, NSTableView tableView, int startRow, int endRow, string searchString);
	public static MonoMac.Foundation.NSObject GetObjectValue (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static NSPasteboardWriting GetPasteboardWriterForRow (INSTableViewSource This, NSTableView tableView, int row);
	public static int GetRowCount (INSTableViewSource This, NSTableView tableView);
	public static float GetRowHeight (INSTableViewSource This, NSTableView tableView, int row);
	public static NSTableRowView GetRowView (INSTableViewSource This, NSTableView tableView, int row);
	public static MonoMac.Foundation.NSIndexSet GetSelectionIndexes (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSIndexSet proposedSelectionIndexes);
	public static string GetSelectString (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static float GetSizeToFitColumnWidth (INSTableViewSource This, NSTableView tableView, int column);
	public static NSView GetViewForItem (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool IsGroupRow (INSTableViewSource This, NSTableView tableView, int row);
	public static void MouseDown (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn);
	public static void SelectionDidChange (INSTableViewSource This, MonoMac.Foundation.NSNotification notification);
	public static void SelectionIsChanging (INSTableViewSource This, MonoMac.Foundation.NSNotification notification);
	public static bool SelectionShouldChange (INSTableViewSource This, NSTableView tableView);
	public static void SetObjectValue (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSObject theObject, NSTableColumn tableColumn, int row);
	public static bool ShouldEditTableColumn (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool ShouldReorder (INSTableViewSource This, NSTableView tableView, int columnIndex, int newColumnIndex);
	public static bool ShouldSelectRow (INSTableViewSource This, NSTableView tableView, int row);
	public static bool ShouldSelectTableColumn (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn);
	public static bool ShouldShowCellExpansion (INSTableViewSource This, NSTableView tableView, NSTableColumn tableColumn, int row);
	public static bool ShouldTrackCell (INSTableViewSource This, NSTableView tableView, NSCell cell, NSTableColumn tableColumn, int row);
	public static bool ShouldTypeSelect (INSTableViewSource This, NSTableView tableView, NSEvent theEvent, string searchString);
	public static void SortDescriptorsChanged (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSSortDescriptor[] oldDescriptors);
	public static void UpdateDraggingItems (INSTableViewSource This, NSTableView tableView, NSDraggingInfo draggingInfo);
	public static NSDragOperation ValidateDrop (INSTableViewSource This, NSTableView tableView, NSDraggingInfo info, int row, NSTableViewDropOperation dropOperation);
	public static void WillDisplayCell (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSObject cell, NSTableColumn tableColumn, int row);
	public static bool WriteRows (INSTableViewSource This, NSTableView tableView, MonoMac.Foundation.NSIndexSet rowIndexes, NSPasteboard pboard);
}
```

### New Type MonoMac.AppKit.NSTabViewController

```
public class NSTabViewController : MonoMac.AppKit.NSViewController, INSTabViewDelegate, INSToolbarDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCoding, INSSeguePerforming, INSUserInterfaceItemIdentification, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSTabViewController ();
	public NSTabViewController (MonoMac.Foundation.NSCoder coder);
	public NSTabViewController (MonoMac.Foundation.NSObjectFlag t);
	public NSTabViewController (System.IntPtr handle);
	// properties
	public virtual bool CanPropagateSelectedChildViewControllerTitle { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSSegmentedControl SegmentedControl { get; set; }
	public virtual int SelectedTabViewItemIndex { get; set; }
	public virtual NSTabViewControllerTabStyle TabStyle { get; set; }
	public virtual NSTabView TabView { get; set; }
	public virtual NSTabViewItem[] TabViewItems { get; set; }
	public virtual NSViewControllerTransitionOptions TransitionOptions { get; set; }
	// methods
	public virtual void AddTabViewItem (NSTabViewItem tabViewItem);
	public virtual string[] AllowedItemIdentifiers (NSToolbar toolbar);
	public virtual string[] DefaultItemIdentifiers (NSToolbar toolbar);
	public virtual void DidRemoveItem (MonoMac.Foundation.NSNotification notification);
	public virtual void DidSelect (NSTabView tabView, NSTabViewItem item);
	protected override void Dispose (bool disposing);
	public virtual NSTabViewItem GetTabViewItem (NSViewController viewController);
	public virtual void InsertTabViewItem (NSTabViewItem tabViewItem, int index);
	public virtual void NumberOfItemsChanged (NSTabView tabView);
	public virtual void RemoveTabViewItem (NSTabViewItem tabViewItem);
	public virtual string[] SelectableItemIdentifiers (NSToolbar toolbar);
	public virtual bool ShouldSelectTabViewItem (NSTabView tabView, NSTabViewItem item);
	public virtual void WillAddItem (MonoMac.Foundation.NSNotification notification);
	public virtual NSToolbarItem WillInsertItem (NSToolbar toolbar, string itemIdentifier, bool willBeInserted);
	public virtual void WillSelect (NSTabView tabView, NSTabViewItem item);
}
```

### New Type MonoMac.AppKit.NSTabViewControllerTabStyle

```
[Serializable]
public enum NSTabViewControllerTabStyle {
	SegmentedControlOnBottom = 1,
	SegmentedControlOnTop = 0,
	Toolbar = 2,
	Unspecified = -1,
}
```

### New Type MonoMac.AppKit.NSTabViewDelegate_Extensions

```
public static class NSTabViewDelegate_Extensions {
	// methods
	public static void DidSelect (INSTabViewDelegate This, NSTabView tabView, NSTabViewItem item);
	public static void NumberOfItemsChanged (INSTabViewDelegate This, NSTabView tabView);
	public static bool ShouldSelectTabViewItem (INSTabViewDelegate This, NSTabView tabView, NSTabViewItem item);
	public static void WillSelect (INSTabViewDelegate This, NSTabView tabView, NSTabViewItem item);
}
```

### New Type MonoMac.AppKit.NSTextCheckingOptions

```
public class NSTextCheckingOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingOptions ();
	public NSTextCheckingOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public string DocumentAuthor { get; set; }
	public string DocumentTitle { get; set; }
	public MonoMac.Foundation.NSUrl DocumentUrl { get; set; }
	public MonoMac.Foundation.NSOrthography Orthography { get; set; }
	public string[] Quotes { get; set; }
	public MonoMac.Foundation.NSDate ReferenceDate { get; set; }
	public MonoMac.Foundation.NSTimeZone ReferenceTimeZone { get; set; }
	public MonoMac.Foundation.NSDictionary Replacements { get; set; }
}
```

### New Type MonoMac.AppKit.NSTextDelegate_Extensions

```
public static class NSTextDelegate_Extensions {
	// methods
	public static void TextDidBeginEditing (INSTextDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void TextDidChange (INSTextDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void TextDidEndEditing (INSTextDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool TextShouldBeginEditing (INSTextDelegate This, NSText textObject);
	public static bool TextShouldEndEditing (INSTextDelegate This, NSText textObject);
}
```

### New Type MonoMac.AppKit.NSTextFieldDelegate_Extensions

```
public static class NSTextFieldDelegate_Extensions {
	// methods
	public static void Changed (INSTextFieldDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool DidFailToFormatString (INSTextFieldDelegate This, NSControl control, string str, string error);
	public static void DidFailToValidatePartialString (INSTextFieldDelegate This, NSControl control, string str, string error);
	public static bool DoCommandBySelector (INSTextFieldDelegate This, NSControl control, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public static void EditingBegan (INSTextFieldDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void EditingEnded (INSTextFieldDelegate This, MonoMac.Foundation.NSNotification notification);
	public static string[] GetCompletions (INSTextFieldDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
	public static bool IsValidObject (INSTextFieldDelegate This, NSControl control, MonoMac.Foundation.NSObject objectToValidate);
	public static bool TextShouldBeginEditing (INSTextFieldDelegate This, NSControl control, NSText fieldEditor);
	public static bool TextShouldEndEditing (INSTextFieldDelegate This, NSControl control, NSText fieldEditor);
}
```

### New Type MonoMac.AppKit.NSTextFinderClient_Extensions

```
public static class NSTextFinderClient_Extensions {
}
```

### New Type MonoMac.AppKit.NSTextStorageDelegate_Extensions

```
public static class NSTextStorageDelegate_Extensions {
	// methods
	public static void TextStorageDidProcessEditing (INSTextStorageDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void TextStorageWillProcessEditing (INSTextStorageDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.NSTextViewDelegate_Extensions

```
public static class NSTextViewDelegate_Extensions {
	// methods
	public static void CellClicked (INSTextViewDelegate This, NSTextView textView, NSTextAttachmentCell cell, System.Drawing.RectangleF cellFrame, uint charIndex);
	public static void CellDoubleClicked (INSTextViewDelegate This, NSTextView textView, NSTextAttachmentCell cell, System.Drawing.RectangleF cellFrame, uint charIndex);
	public static void DidChangeSelection (INSTextViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidChangeTypingAttributes (INSTextViewDelegate This, MonoMac.Foundation.NSNotification notification);
	public static MonoMac.Foundation.NSTextCheckingResult[] DidCheckText (INSTextViewDelegate This, NSTextView view, MonoMac.Foundation.NSRange range, MonoMac.Foundation.NSTextCheckingTypes checkingTypes, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSTextCheckingResult[] results, MonoMac.Foundation.NSOrthography orthography, int wordCount);
	public static bool DoCommandBySelector (INSTextViewDelegate This, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public static void DraggedCell (INSTextViewDelegate This, NSTextView view, NSTextAttachmentCell cell, System.Drawing.RectangleF rect, NSEvent theevent);
	public static string[] GetCompletions (INSTextViewDelegate This, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
	public static MonoMac.Foundation.NSUndoManager GetUndoManager (INSTextViewDelegate This, NSTextView view);
	public static string[] GetWritablePasteboardTypes (INSTextViewDelegate This, NSTextView view, NSTextAttachmentCell forCell, uint charIndex);
	public static bool LinkClicked (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSObject link, uint charIndex);
	public static NSMenu MenuForEvent (INSTextViewDelegate This, NSTextView view, NSMenu menu, NSEvent theEvent, uint charIndex);
	public static bool ShouldChangeTextInRange (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSRange affectedCharRange, string replacementString);
	public static bool ShouldChangeTextInRanges (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSValue[] affectedRanges, string[] replacementStrings);
	public static MonoMac.Foundation.NSDictionary ShouldChangeTypingAttributes (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSDictionary oldTypingAttributes, MonoMac.Foundation.NSDictionary newTypingAttributes);
	public static int ShouldSetSpellingState (INSTextViewDelegate This, NSTextView textView, int value, MonoMac.Foundation.NSRange affectedCharRange);
	public static MonoMac.Foundation.NSRange WillChangeSelection (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSRange oldSelectedCharRange, MonoMac.Foundation.NSRange newSelectedCharRange);
	public static MonoMac.Foundation.NSValue[] WillChangeSelectionFromRanges (INSTextViewDelegate This, NSTextView textView, MonoMac.Foundation.NSValue[] oldSelectedCharRanges, MonoMac.Foundation.NSValue[] newSelectedCharRanges);
	public static MonoMac.Foundation.NSDictionary WillCheckText (INSTextViewDelegate This, NSTextView view, MonoMac.Foundation.NSRange range, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSTextCheckingTypes checkingTypes);
	public static string WillDisplayToolTip (INSTextViewDelegate This, NSTextView textView, string tooltip, uint characterIndex);
	public static bool WriteCell (INSTextViewDelegate This, NSTextView view, NSTextAttachmentCell cell, uint charIndex, NSPasteboard pboard, string type);
}
```

### New Type MonoMac.AppKit.NSTitlebarAccessoryViewController

```
public class NSTitlebarAccessoryViewController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, INSSeguePerforming, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSTitlebarAccessoryViewController ();
	public NSTitlebarAccessoryViewController (MonoMac.Foundation.NSCoder coder);
	public NSTitlebarAccessoryViewController (MonoMac.Foundation.NSObjectFlag t);
	public NSTitlebarAccessoryViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float FullScreenMinHeight { get; set; }
	public virtual NSLayoutAttribute LayoutAttribute { get; set; }
	// methods
	public virtual void ViewDidAppear ();
	public virtual void ViewDidDisappear ();
	public virtual void ViewWillAppear ();
}
```

### New Type MonoMac.AppKit.NSTokenFieldDelegate_Extensions

```
public static class NSTokenFieldDelegate_Extensions {
	// methods
	public static string[] GetCompletionStrings (INSTokenFieldDelegate This, NSTokenField tokenField, string substring, int tokenIndex, int selectedIndex);
	public static string GetDisplayString (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
	public static string GetEditingString (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
	public static NSMenu GetMenu (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
	public static MonoMac.Foundation.NSObject GetRepresentedObject (INSTokenFieldDelegate This, NSTokenField tokenField, string editingString);
	public static NSTokenStyle GetStyle (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
	public static bool HasMenu (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
	public static MonoMac.Foundation.NSObject[] Read (INSTokenFieldDelegate This, NSTokenField tokenField, NSPasteboard pboard);
	public static NSTokenField[] ShouldAddObjects (INSTokenFieldDelegate This, NSTokenField tokenField, NSTokenField[] tokens, uint index);
	public static bool WriteRepresented (INSTokenFieldDelegate This, NSTokenField tokenField, MonoMac.Foundation.NSArray objects, NSPasteboard pboard);
}
```

### New Type MonoMac.AppKit.NSToolbarDelegate_Extensions

```
public static class NSToolbarDelegate_Extensions {
	// methods
	public static string[] AllowedItemIdentifiers (INSToolbarDelegate This, NSToolbar toolbar);
	public static string[] DefaultItemIdentifiers (INSToolbarDelegate This, NSToolbar toolbar);
	public static void DidRemoveItem (INSToolbarDelegate This, MonoMac.Foundation.NSNotification notification);
	public static string[] SelectableItemIdentifiers (INSToolbarDelegate This, NSToolbar toolbar);
	public static void WillAddItem (INSToolbarDelegate This, MonoMac.Foundation.NSNotification notification);
	public static NSToolbarItem WillInsertItem (INSToolbarDelegate This, NSToolbar toolbar, string itemIdentifier, bool willBeInserted);
}
```

### New Type MonoMac.AppKit.NSUserDefaultsController

```
public class NSUserDefaultsController : MonoMac.AppKit.NSController, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSUserDefaultsController ();
	public NSUserDefaultsController (MonoMac.Foundation.NSCoder coder);
	public NSUserDefaultsController (MonoMac.Foundation.NSObjectFlag t);
	public NSUserDefaultsController (System.IntPtr handle);
	public NSUserDefaultsController (MonoMac.Foundation.NSUserDefaults defaults, MonoMac.Foundation.NSDictionary initialValues);
	// properties
	public virtual bool AppliesImmediately { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSUserDefaults Defaults { get; }
	public virtual bool HasUnappliedChanges { get; }
	public virtual MonoMac.Foundation.NSDictionary InitialValues { get; set; }
	public static NSUserDefaultsController SharedUserDefaultsController { get; }
	public virtual MonoMac.Foundation.NSObject Values { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Revert (MonoMac.Foundation.NSObject sender);
	public virtual void RevertToInitialValues (MonoMac.Foundation.NSObject sender);
	public virtual void Save (MonoMac.Foundation.NSObject sender);
}
```

### New Type MonoMac.AppKit.NSUserInterfaceItemIdentification_Extensions

```
public static class NSUserInterfaceItemIdentification_Extensions {
	// methods
	public static string GetIdentifier (INSUserInterfaceItemIdentification This);
	public static void SetIdentifier (INSUserInterfaceItemIdentification This, string value);
}
```

### New Type MonoMac.AppKit.NSUserInterfaceLayoutOrientation

```
[Serializable]
public enum NSUserInterfaceLayoutOrientation {
	Horizontal = 0,
	Vertical = 1,
}
```

### New Type MonoMac.AppKit.NSViewControllerPresentationAnimator

```
public abstract class NSViewControllerPresentationAnimator : MonoMac.Foundation.NSObject, INSViewControllerPresentationAnimator, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSViewControllerPresentationAnimator ();
	public NSViewControllerPresentationAnimator (MonoMac.Foundation.NSCoder coder);
	public NSViewControllerPresentationAnimator (MonoMac.Foundation.NSObjectFlag t);
	public NSViewControllerPresentationAnimator (System.IntPtr handle);
	// methods
	public virtual void AnimateDismissal (NSViewController viewController, NSViewController fromViewController);
	public virtual void AnimatePresentation (NSViewController viewController, NSViewController fromViewController);
}
```

### New Type MonoMac.AppKit.NSViewControllerPresentationAnimator_Extensions

```
public static class NSViewControllerPresentationAnimator_Extensions {
}
```

### New Type MonoMac.AppKit.NSViewControllerTransitionOptions

```
[Serializable]
[Flags]
public enum NSViewControllerTransitionOptions {
	AllowUserInteraction = 4096,
	Crossfade = 1,
	None = 0,
	SlideBackward = 384,
	SlideDown = 32,
	SlideForward = 320,
	SlideLeft = 64,
	SlideRight = 128,
	SlideUp = 16,
}
```

### New Type MonoMac.AppKit.NSVisualEffectBlendingMode

```
[Serializable]
public enum NSVisualEffectBlendingMode {
	BehindWindow = 0,
	WithinWindow = 1,
}
```

### New Type MonoMac.AppKit.NSVisualEffectMaterial

```
[Serializable]
public enum NSVisualEffectMaterial {
	AppearanceBased = 0,
	Dark = 2,
	Light = 1,
	Titlebar = 3,
}
```

### New Type MonoMac.AppKit.NSVisualEffectState

```
[Serializable]
public enum NSVisualEffectState {
	Active = 1,
	FollowsWindowActiveState = 0,
	Inactive = 2,
}
```

### New Type MonoMac.AppKit.NSVisualEffectView

```
public class NSVisualEffectView : MonoMac.AppKit.NSView, INSDraggingDestination, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSVisualEffectView ();
	public NSVisualEffectView (MonoMac.Foundation.NSCoder coder);
	public NSVisualEffectView (MonoMac.Foundation.NSObjectFlag t);
	public NSVisualEffectView (System.IntPtr handle);
	// properties
	public virtual NSVisualEffectBlendingMode BlendingMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSBackgroundStyle InteriorBackgroundStyle { get; }
	public virtual NSImage MaskImage { get; set; }
	public virtual NSVisualEffectMaterial Material { get; set; }
	public virtual NSVisualEffectState State { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void ViewDidMove ();
	public virtual void ViewWillMove (NSWindow newWindow);
}
```

### New Type MonoMac.AppKit.NSWindowDelegate_Extensions

```
public static class NSWindowDelegate_Extensions {
	// methods
	public static NSWindow[] CustomWindowsToEnterFullScreen (INSWindowDelegate This, NSWindow window);
	public static NSWindow[] CustomWindowsToExitFullScreen (INSWindowDelegate This, NSWindow window);
	public static void DidBecomeKey (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidBecomeMain (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidChangeBackingProperties (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidChangeScreen (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidChangeScreenProfile (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidDecodeRestorableState (INSWindowDelegate This, NSWindow window, MonoMac.Foundation.NSCoder coder);
	public static void DidDeminiaturize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidEndLiveResize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidEndSheet (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidEnterFullScreen (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidEnterVersionBrowser (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidExitFullScreen (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidExitVersionBrowser (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidExpose (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidFailToEnterFullScreen (INSWindowDelegate This, NSWindow window);
	public static void DidFailToExitFullScreen (INSWindowDelegate This, NSWindow window);
	public static void DidMiniaturize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidMoved (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidResignKey (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidResignMain (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidResize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void DidUpdate (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static bool ShouldDragDocumentWithEvent (INSWindowDelegate This, NSWindow window, NSEvent theEvent, System.Drawing.PointF dragImageLocation, NSPasteboard withPasteboard);
	public static bool ShouldPopUpDocumentPathMenu (INSWindowDelegate This, NSWindow window, NSMenu menu);
	public static bool ShouldZoom (INSWindowDelegate This, NSWindow window, System.Drawing.RectangleF newFrame);
	public static void StartCustomAnimationToEnterFullScreen (INSWindowDelegate This, NSWindow window, double duration);
	public static void StartCustomAnimationToExitFullScreen (INSWindowDelegate This, NSWindow window, double duration);
	public static void WillBeginSheet (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillClose (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillEncodeRestorableState (INSWindowDelegate This, NSWindow window, MonoMac.Foundation.NSCoder coder);
	public static void WillEnterFullScreen (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillEnterVersionBrowser (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillExitFullScreen (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillExitVersionBrowser (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillMiniaturize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillMove (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static System.Drawing.RectangleF WillPositionSheet (INSWindowDelegate This, NSWindow window, NSWindow sheet, System.Drawing.RectangleF usingRect);
	public static System.Drawing.SizeF WillResize (INSWindowDelegate This, NSWindow sender, System.Drawing.SizeF toFrameSize);
	public static System.Drawing.SizeF WillResizeForVersionBrowser (INSWindowDelegate This, NSWindow window, System.Drawing.SizeF maxPreferredSize, System.Drawing.SizeF maxAllowedSize);
	public static MonoMac.Foundation.NSObject WillReturnFieldEditor (INSWindowDelegate This, NSWindow sender, MonoMac.Foundation.NSObject client);
	public static MonoMac.Foundation.NSUndoManager WillReturnUndoManager (INSWindowDelegate This, NSWindow window);
	public static void WillStartLiveResize (INSWindowDelegate This, MonoMac.Foundation.NSNotification notification);
	public static System.Drawing.SizeF WillUseFullScreenContentSize (INSWindowDelegate This, NSWindow window, System.Drawing.SizeF proposedSize);
	public static NSApplicationPresentationOptions WillUseFullScreenPresentationOptions (INSWindowDelegate This, NSWindow window, NSApplicationPresentationOptions proposedOptions);
	public static System.Drawing.RectangleF WillUseStandardFrame (INSWindowDelegate This, NSWindow window, System.Drawing.RectangleF newFrame);
	public static bool WindowShouldClose (INSWindowDelegate This, MonoMac.Foundation.NSObject sender);
}
```

### New Type MonoMac.AppKit.NSWindowOcclusionState

```
[Serializable]
[Flags]
public enum NSWindowOcclusionState {
	Visible = 2,
}
```

### New Type MonoMac.AppKit.NSWindowRestoration_Extensions

```
public static class NSWindowRestoration_Extensions {
}
```

### New Type MonoMac.AppKit.NSWindowTitleVisibility

```
[Serializable]
public enum NSWindowTitleVisibility {
	Hidden = 1,
	HiddenWhenActive = 2,
	Visible = 0,
}
```

### New Type MonoMac.AppKit.NSWindowTrackEventsMatchingCompletionHandler

```
public sealed delegate NSWindowTrackEventsMatchingCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSWindowTrackEventsMatchingCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSEvent evt, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSEvent evt, ref bool stop);
}
```

## Namespace MonoMac.AudioToolbox

### Type Changed: MonoMac.AudioToolbox.AudioFile

Added interface:

```
MonoMac.ObjCRuntime.INativeObject
```

Removed property:

```
public System.IntPtr Handle { get; }
```

Added property:

```
public virtual System.IntPtr Handle { get; }
```

Obsoleted method:

```
[Obsolete ("Use ReadPacketData instead")]
	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, System.IntPtr buffer);
```

### Type Changed: MonoMac.AudioToolbox.AudioFormatType

Added value:

```
AMRWideBand = 1935767394,
```

### Type Changed: MonoMac.AudioToolbox.AudioQueue

Added method:

```
protected override void ~AudioQueue ();
```

### Type Changed: MonoMac.AudioToolbox.AudioQueueStatus

Added value:

```
BufferEnqueuedTwice = -66666,
```

### Type Changed: MonoMac.AudioToolbox.AudioSource

Added interface:

```
MonoMac.ObjCRuntime.INativeObject
```

### Type Changed: MonoMac.AudioToolbox.AudioStreamBasicDescription

Added fields:

```
public static AudioFormatFlags AudioFormatFlagsAudioUnitNativeFloat;
	public static AudioFormatFlags AudioFormatFlagsNativeFloat;
```

## Namespace MonoMac.AudioUnit

### Type Changed: MonoMac.AudioUnit.AudioComponent

Added methods:

```
public static AudioComponent FindComponent (ref AudioComponentDescription cd);
	public static AudioComponent FindNextComponent (AudioComponent cmp, ref AudioComponentDescription cd);
```

Obsoleted methods:

```
[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter")]
	public static AudioComponent FindComponent (AudioComponentDescription cd);

	[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter")]
	public static AudioComponent FindNextComponent (AudioComponent cmp, AudioComponentDescription cd);
```

### Type Changed: MonoMac.AudioUnit.AudioTypeMixer

Added value:

```
Spacial = 862217581,
```

### Type Changed: MonoMac.AudioUnit.AudioTypeMusicDevice

Added value:

```
MidiSynth = 1836284270,
```

### Type Changed: MonoMac.AudioUnit.AudioUnit

Added methods:

```
public uint GetCurrentDevice (AudioUnitScopeType scope, uint audioUnitElement);
	public static uint GetCurrentInputDevice ();
	public uint GetElementCount (AudioUnitScopeType scope);
	public AudioUnitStatus SetCurrentDevice (uint inputDevice, AudioUnitScopeType scope, uint audioUnitElement);
```

### Type Changed: MonoMac.AudioUnit.AudioUnitParameterFlag

Added value:

```
OmitFromPresets = 8192,
```

### Type Changed: MonoMac.AudioUnit.AudioUnitParameterType

Added values:

```
Distance = 2,
	Elevation = 1,
	Enable = 5,
	Gain = 3,
	GlobalReverbGain = 9,
	MaxGain = 7,
	MinGain = 6,
	ObstructionAttenuation = 11,
	OcclussionAttenuation = 10,
	PlaybackRate = 4,
	ReverbBlend = 8,
	ReverbFilterEnable = 18,
	ReverbFilterType = 17,
	RoundTripAacEncodingStrategy = 1,
	RoundTripAacFormat = 0,
	RoundTripAacRateOrQuality = 2,
	SpacialMixerAzimuth = 0,
	SpatialAzimuth = 0,
	SpatialDistance = 2,
	SpatialElevation = 1,
	SpatialEnable = 5,
	SpatialGain = 3,
	SpatialGlobalReverbGain = 9,
	SpatialMaxGain = 7,
	SpatialMinGain = 6,
	SpatialObstructionAttenuation = 11,
	SpatialOcclusionAttenuation = 10,
	SpatialPlaybackRate = 4,
	SpatialReverbBlend = 8,
```

### Type Changed: MonoMac.AudioUnit.AudioUnitPropertyIDType

Added values:

```
AttenuationCurve = 3013,
	BankName = 1007,
	DistanceParams = 3010,
	InstrumentCount = 1000,
	InstrumentName = 1001,
	InstrumentNumber = 1004,
	MidiSynthEnablePreload = 4119,
	RenderingFlags = 3003,
	ReverbRoomType = 10,
	SoundBankURL = 1100,
	SpatializationAlgorithm = 3000,
	UsesInternalReverb = 1005,
```

### Type Changed: MonoMac.AudioUnit.AUGraph

Obsoleted property:

```
[Obsolete ("Use Handle property instead")]
	public System.IntPtr Handler { get; }
```

Added methods:

```
public AudioUnitStatus AddRenderNotify (RenderDelegate callback);
	public AudioUnitStatus RemoveRenderNotify (RenderDelegate callback);
	public AUGraphError SetNodeInputCallback (int destNode, uint destInputNumber, RenderDelegate renderDelegate);
```

### New Type MonoMac.AudioUnit.AudioComponentDescriptionNative

```
public struct AudioComponentDescriptionNative {
	// constructors
	public AudioComponentDescriptionNative (AudioComponentDescription other);
	// fields
	public AudioComponentFlag ComponentFlags;
	public int ComponentFlagsMask;
	public AudioComponentManufacturerType ComponentManufacturer;
	public int ComponentSubType;
	public AudioComponentType ComponentType;
	// methods
	public void CopyTo (AudioComponentDescription cd);
}
```

### New Type MonoMac.AudioUnit.ScheduledAudioSliceFlag

```
[Serializable]
[Flags]
public enum ScheduledAudioSliceFlag {
	BeganToRender = 2,
	BeganToRenderLate = 4,
	Complete = 1,
	Interrupt = 16,
	InterruptAtLoop = 32,
	Loop = 8,
}
```

### New Type MonoMac.AudioUnit.SpatialMixerAttenuation

```
[Serializable]
public enum SpatialMixerAttenuation {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
```

### New Type MonoMac.AudioUnit.SpatialMixerRenderingFlags

```
[Serializable]
[Flags]
public enum SpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
```

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVAsset

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual AVMetadataItem[] Metadata { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetExportSession

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool CanPerformMultiplePassesOverSourceMediaData { get; set; }
	public virtual MonoMac.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetImageGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Obsoleted method:

```
[Obsolete ("Use the overload that takes NSValue[] instead")]
	public virtual void GenerateCGImagesAsynchronously (MonoMac.Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
```

### Type Changed: MonoMac.AVFoundation.AVAssetReader

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetReaderAudioMixOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetReaderOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual bool SupportsRandomAccess { get; set; }
```

Added methods:

```
public virtual void MarkConfigurationAsFinal ();
	public virtual void ResetForReadingTimeRanges (MonoMac.Foundation.NSValue[] timeRanges);
```

### Type Changed: MonoMac.AVFoundation.AVAssetReaderTrackOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetReaderVideoCompositionOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoader

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual void DidCancelAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public virtual void DidCancelLoadingRequest (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
	public virtual bool ShouldWaitForRenewalOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public virtual bool ShouldWaitForResponseToAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added methods:

```
public static void DidCancelAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public static void DidCancelLoadingRequest (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
	public static bool ShouldWaitForRenewalOfRequestedResource (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public static bool ShouldWaitForResponseToAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoadingRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

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

### Type Changed: MonoMac.AVFoundation.AVAssetTrack

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual AVMetadataItem[] Metadata { get; }
	public virtual bool RequiresFrameReordering { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetTrackGroup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetTrackSegment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetTrackTrackAssociation

Added property:

```
public static MonoMac.Foundation.NSString MetadataReferent { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSString[] AvailableMediaTypes { get; }
	public virtual MonoMac.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriterInput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual bool CanPerformMultiplePasses { get; }
	public virtual AVAssetWriterInputPassDescription CurrentPassDescription { get; }
	public virtual bool PerformsMultiPassEncodingIfSupported { get; set; }
	public virtual int PreferredMediaChunkAlignment { get; set; }
	public virtual MonoMac.CoreMedia.CMTime PreferredMediaChunkDuration { get; set; }
	public virtual MonoMac.Foundation.NSUrl SampleReferenceBaseUrl { get; set; }
```

Added methods:

```
public virtual void MarkCurrentPassAsFinished ();
	public virtual void SetPassHandler (MonoMac.CoreFoundation.DispatchQueue queue, System.Action passHandler);
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriterInputGroup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriterInputPixelBufferAdaptor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAsynchronousKeyValueLoading

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAsynchronousVideoCompositionRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioMix

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioMixInputParameters

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioPlayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioPlayerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioRecorder

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioRecorderDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVAudioSessionErrorCode

Added values:

```
CannotStartRecording = 561145187,
	InsufficientPriority = 561017449,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureAudioChannel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureAudioDataOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureConnection

Added constructors:

```
public AVCaptureConnection (AVCaptureInputPort[] inputPorts, AVCaptureOutput output);
	public AVCaptureConnection (AVCaptureInputPort inputPort, AVCaptureVideoPreviewLayer layer);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureDevice

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureDeviceInput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureDevicePosition

Added value:

```
Unspecified = 0,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureExposureMode

Added value:

```
Custom = 3,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureFileOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public void StartRecordingToOutputFile (MonoMac.Foundation.NSUrl outputFileUrl, System.Action<MonoMac.Foundation.NSObject[]> startRecordingFromConnections, System.Action<MonoMac.Foundation.NSObject[],MonoMac.Foundation.NSError> finishedRecording);
```

### Type Changed: MonoMac.AVFoundation.AVCaptureFileOutputRecordingDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureFocusMode

Added values:

```
AutoFocus = 1,
	ContinuousAutoFocus = 2,
	Locked = 0,
```

Obsoleted fields:

```
[Obsolete ("use AutoFocus instead")]
	ModeAutoFocus = 1,

	[Obsolete ("use ContinuousAutoFocus instead")]
	ModeContinuousAutoFocus = 2,

	[Obsolete ("use Locked instead")]
	ModeLocked = 0,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureInput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureInputPort

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureMovieFileOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureSession

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual MonoMac.CoreMedia.CMClock MasterClock { get; }
```

Added methods:

```
public virtual void AddConnection (AVCaptureConnection connection);
	public virtual void AddInputWithNoConnections (AVCaptureInput input);
	public virtual void AddOutputWithNoConnections (AVCaptureOutput output);
	public virtual bool CanAddConnection (AVCaptureConnection connection);
	public virtual void RemoveConnection (AVCaptureConnection connection);
```

### Type Changed: MonoMac.AVFoundation.AVCaptureStillImageOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoDataOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoPreviewLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public AVLayerVideoGravity LayerVideoGravity { get; set; }
	public string VideoGravity { get; set; }
	protected virtual MonoMac.Foundation.NSString WeakVideoGravity { get; set; }
```

Added method:

```
public static AVCaptureVideoPreviewLayer CreateWithNoConnection (AVCaptureSession session);
```

### Type Changed: MonoMac.AVFoundation.AVComposition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCompositionTrack

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVCompositionTrackSegment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVError

Added values:

```
ApplicationIsNotAuthorizedToUseDevice = 11852,
	FailedToParse2 = -11853,
	FileTypeDoesNotSupportSampleReferences = -11854,
	UndecodableMediaData = -11855,
```

### Type Changed: MonoMac.AVFoundation.AVFrameRateRange

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMediaSelectionGroup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual AVMediaSelectionOption DefaultOption { get; }
```

### Type Changed: MonoMac.AVFoundation.AVMediaSelectionOption

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMediaType

Added property:

```
public static MonoMac.Foundation.NSString Metadata { get; }
```

### Type Changed: MonoMac.AVFoundation.AVMetadata

Added properties:

```
public static MonoMac.Foundation.NSString FormatHlsMetadata { get; }
	public static MonoMac.Foundation.NSString IcyMetadataKeyStreamTitle { get; }
	public static MonoMac.Foundation.NSString IcyMetadataKeyStreamUrl { get; }
	public static MonoMac.Foundation.NSString IsoUserDataKeyTaggedCharacteristic { get; }
	public static MonoMac.Foundation.NSString KeySpaceIcy { get; }
```

### Type Changed: MonoMac.AVFoundation.AVMetadataItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed properties:

```
public virtual MonoMac.CoreMedia.CMTime Duration { get; }
	public virtual MonoMac.Foundation.NSDictionary ExtraAttributes { get; }
	public virtual string KeySpace { get; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; }
	public virtual MonoMac.CoreMedia.CMTime Time { get; }
	public virtual MonoMac.Foundation.NSObject Value { get; }
```

Added properties:

```
public virtual MonoMac.Foundation.NSString DataType { get; set; }
	public virtual MonoMac.CoreMedia.CMTime Duration { get; set; }
	public virtual string ExtendedLanguageTag { get; set; }
	public virtual MonoMac.Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; set; }
	public virtual MonoMac.Foundation.NSString MetadataIdentifier { get; set; }
	public virtual MonoMac.CoreMedia.CMTime Time { get; set; }
	public virtual MonoMac.Foundation.NSObject Value { get; set; }
```

Added methods:

```
public static AVMetadataItem[] FilterWithIdentifier (AVMetadataItem[] metadataItems, MonoMac.Foundation.NSString metadataIdentifer);
	public static MonoMac.Foundation.NSObject GetKeyForIdentifier (MonoMac.Foundation.NSString identifier);
	public static MonoMac.Foundation.NSString GetKeySpaceForIdentifier (MonoMac.Foundation.NSString identifier);
	public static MonoMac.Foundation.NSString GetMetadataIdentifier (MonoMac.Foundation.NSObject key, MonoMac.Foundation.NSString keySpace);
```

### Type Changed: MonoMac.AVFoundation.AVMetadataItemFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableAudioMix

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableAudioMixInputParameters

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableComposition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableCompositionTrack

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableMetadataItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public override MonoMac.Foundation.NSString DataType { get; set; }
	public override string ExtendedLanguageTag { get; set; }
	public override MonoMac.Foundation.NSString MetadataIdentifier { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVMutableTimedMetadataGroup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableVideoComposition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableVideoCompositionInstruction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVMutableVideoCompositionLayerInstruction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public AVLayerVideoGravity? ExternalPlaybackVideoGravity { get; set; }
	protected virtual MonoMac.Foundation.NSString WeakExternalPlaybackVideoGravity { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVPlayerActionAtItemEnd

Added value:

```
Advance = 0,
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual double PreferredPeakBitRate { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemAccessLog

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemAccessLogEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemErrorLog

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemErrorLogEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemLegibleOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemLegibleOutputPushDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemOutputPullDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemOutputPushDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemTrack

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItemVideoOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVPlayerLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public AVLayerVideoGravity LayerVideoGravity { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVPlayerMediaSelectionCriteria

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVQueuePlayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVSynchronizedLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVTextStyleRule

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVTimedMetadataGroup

Added constructor:

```
public AVTimedMetadataGroup (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual MonoMac.CoreMedia.CMFormatDescription CopyFormatDescription ();
```

### Type Changed: MonoMac.AVFoundation.AVUrlAsset

Removed constructor:

```
public AVUrlAsset (MonoMac.Foundation.NSUrl URL, MonoMac.Foundation.NSDictionary options);
```

Added constructor:

```
public AVUrlAsset (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public static AVUrlAsset FromUrl (MonoMac.Foundation.NSUrl URL, MonoMac.Foundation.NSDictionary options);
```

Added method:

```
public static AVUrlAsset FromUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
```

### Type Changed: MonoMac.AVFoundation.AVVideoCodecSettings

Removed properties:

```
public AVVideoPixelAspectRatioSettings PixelAspectRatio { set; }
	public AVVideoCleanApertureSettings VideoCleanAperture { set; }
```

Added properties:

```
public AVVideoPixelAspectRatioSettings PixelAspectRatio { get; set; }
	public AVVideoCleanApertureSettings VideoCleanAperture { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoComposition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositionCoreAnimationTool

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositionInstruction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed properties:

```
public virtual bool EnablePostProcessing { get; }
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions { get; }
	public virtual MonoMac.CoreMedia.CMTimeRange TimeRange { get; }
```

Added properties:

```
public virtual bool EnablePostProcessing { get; set; }
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions { get; set; }
	public virtual MonoMac.CoreMedia.CMTimeRange TimeRange { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositionLayerInstruction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositionRenderContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoCompositionValidationHandling

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.AVFoundation.AVVideoSettingsCompressed

Removed properties:

```
public AVVideoCodec? Codec { set; }
	public AVVideoCodecSettings CodecSettings { set; }
	public AVVideoScalingMode? ScalingMode { set; }
```

Added properties:

```
public AVVideoCodec? Codec { get; set; }
	public AVVideoCodecSettings CodecSettings { get; set; }
	public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVVideoSettingsUncompressed

Removed property:

```
public AVVideoScalingMode? ScalingMode { set; }
```

Added property:

```
public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: MonoMac.AVFoundation.IAVPlayerItemLegibleOutputPushDelegate

Added interface:

```
IAVPlayerItemOutputPushDelegate
```

### New Type MonoMac.AVFoundation.AVAssetReaderOutputMetadataAdaptor

```
public class AVAssetReaderOutputMetadataAdaptor : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderOutputMetadataAdaptor (MonoMac.Foundation.NSCoder coder);
	public AVAssetReaderOutputMetadataAdaptor (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetReaderOutputMetadataAdaptor (System.IntPtr handle);
	public AVAssetReaderOutputMetadataAdaptor (AVAssetReaderTrackOutput trackOutput);
	// properties
	public virtual AVAssetReaderTrackOutput AssetReaderTrackOutput { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static AVAssetReaderOutputMetadataAdaptor Create (AVAssetReaderTrackOutput trackOutput);
	protected override void Dispose (bool disposing);
	public virtual AVTimedMetadataGroup NextTimedMetadataGroup ();
}
```

### New Type MonoMac.AVFoundation.AVAssetReaderSampleReferenceOutput

```
public class AVAssetReaderSampleReferenceOutput : MonoMac.AVFoundation.AVAssetReaderOutput, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderSampleReferenceOutput (MonoMac.Foundation.NSCoder coder);
	public AVAssetReaderSampleReferenceOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetReaderSampleReferenceOutput (System.IntPtr handle);
	public AVAssetReaderSampleReferenceOutput (AVAssetTrack track);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAssetTrack Track { get; }
	// methods
	public static AVAssetReaderSampleReferenceOutput Create (AVAssetTrack track);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAssetResourceLoadingContentInformationRequest

```
public class AVAssetResourceLoadingContentInformationRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual MonoMac.Foundation.NSDate RenewalDate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAssetResourceLoadingDataRequest

```
public class AVAssetResourceLoadingDataRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingDataRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoadingDataRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingDataRequest (System.IntPtr handle);

	[Obsolete ("Type is not meant to be created by user code")]
	public AVAssetResourceLoadingDataRequest ();
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

### New Type MonoMac.AVFoundation.AVAssetResourceRenewalRequest

```
public class AVAssetResourceRenewalRequest : MonoMac.AVFoundation.AVAssetResourceLoadingRequest, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceRenewalRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceRenewalRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceRenewalRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAssetWriterInputMetadataAdaptor

```
public class AVAssetWriterInputMetadataAdaptor : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputMetadataAdaptor (MonoMac.Foundation.NSCoder coder);
	public AVAssetWriterInputMetadataAdaptor (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetWriterInputMetadataAdaptor (System.IntPtr handle);
	public AVAssetWriterInputMetadataAdaptor (AVAssetWriterInput assetWriterInput);
	// properties
	public virtual AVAssetWriterInput AssetWriterInput { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual bool AppendTimedMetadataGroup (AVTimedMetadataGroup timedMetadataGroup);
	public static AVAssetWriterInputMetadataAdaptor Create (AVAssetWriterInput input);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAssetWriterInputPassDescription

```
public class AVAssetWriterInputPassDescription : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputPassDescription ();
	public AVAssetWriterInputPassDescription (MonoMac.Foundation.NSCoder coder);
	public AVAssetWriterInputPassDescription (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetWriterInputPassDescription (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSValue[] SourceTimeRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAudio3DAngularOrientation

```
public struct AVAudio3DAngularOrientation {
	// fields
	public float Pitch;
	public float Roll;
	public float Yaw;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DAngularOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DAngularOrientation left, AVAudio3DAngularOrientation right);
	public static bool op_Inequality (AVAudio3DAngularOrientation left, AVAudio3DAngularOrientation right);
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVAudio3DMixing

```
public abstract class AVAudio3DMixing : MonoMac.Foundation.NSObject, IAVAudio3DMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudio3DMixing ();
	public AVAudio3DMixing (MonoMac.Foundation.NSCoder coder);
	public AVAudio3DMixing (MonoMac.Foundation.NSObjectFlag t);
	public AVAudio3DMixing (System.IntPtr handle);
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudio3DMixing_Extensions

```
public static class AVAudio3DMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudio3DMixingRenderingAlgorithm

```
[Serializable]
public enum AVAudio3DMixingRenderingAlgorithm {
	EqualPowerPanning = 0,
	HRTF = 2,
	SoundField = 3,
	SphericalHead = 1,
	StereoPassThrough = 5,
}
```

### New Type MonoMac.AVFoundation.AVAudio3DVectorOrientation

```
public struct AVAudio3DVectorOrientation {
	// constructors
	public AVAudio3DVectorOrientation (MonoMac.OpenGL.Vector3 forward, MonoMac.OpenGL.Vector3 up);
	// fields
	public MonoMac.OpenGL.Vector3 Forward;
	public MonoMac.OpenGL.Vector3 Up;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DVectorOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public static bool op_Inequality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVAudioBuffer

```
public class AVAudioBuffer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioBuffer (MonoMac.Foundation.NSCoder coder);
	public AVAudioBuffer (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioBuffer (System.IntPtr handle);
	// properties
	public MonoMac.AudioToolbox.AudioBuffers AudioBufferList { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat Format { get; }
	public MonoMac.AudioToolbox.AudioBuffers MutableAudioBufferList { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.AVFoundation.AVAudioChannelLayout

```
public class AVAudioChannelLayout : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioChannelLayout ();
	public AVAudioChannelLayout (MonoMac.Foundation.NSCoder coder);
	public AVAudioChannelLayout (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioChannelLayout (System.IntPtr handle);
	public AVAudioChannelLayout (uint layoutTag);
	public AVAudioChannelLayout (MonoMac.AudioToolbox.AudioChannelLayout layout);
	// properties
	public virtual uint ChannelCount { get; }
	public override System.IntPtr ClassHandle { get; }
	public MonoMac.AudioToolbox.AudioChannelLayout Layout { get; }
	public virtual uint LayoutTag { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioChannelLayout a, AVAudioChannelLayout b);
	public static bool op_Inequality (AVAudioChannelLayout a, AVAudioChannelLayout b);
}
```

### New Type MonoMac.AVFoundation.AVAudioCommonFormat

```
[Serializable]
public enum AVAudioCommonFormat {
	Other = 0,
	PCMFloat32 = 1,
	PCMFloat64 = 2,
	PCMInt16 = 3,
	PCMInt32 = 4,
}
```

### New Type MonoMac.AVFoundation.AVAudioEngine

```
public class AVAudioEngine : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEngine ();
	public AVAudioEngine (MonoMac.Foundation.NSCoder coder);
	public AVAudioEngine (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEngine (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual AVAudioInputNode InputNode { get; }
	public virtual AVAudioMixerNode MainMixerNode { get; }
	public virtual AVAudioOutputNode OutputNode { get; }
	public virtual bool Running { get; }
	// methods
	public virtual void AttachNode (AVAudioNode node);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, uint sourceBus, uint targetBus, AVAudioFormat format);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, AVAudioFormat format);
	public virtual void DetachNode (AVAudioNode node);
	public virtual void DisconnectNodeInput (AVAudioNode node, uint bus);
	public virtual void DisconnectNodeInput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node, uint bus);
	protected override void Dispose (bool disposing);
	public virtual void Pause ();
	public virtual void Prepare ();
	public virtual void Reset ();
	public virtual bool StartAndReturnError (out MonoMac.Foundation.NSError outError);
	public virtual void Stop ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoMac.Foundation.NSObject ObserveConfigurationChange (System.EventHandler<MonoMac.Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentDistanceAttenuationModel

```
[Serializable]
public enum AVAudioEnvironmentDistanceAttenuationModel {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentDistanceAttenuationParameters

```
public class AVAudioEnvironmentDistanceAttenuationParameters : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentDistanceAttenuationParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationModel DistanceAttenuationModel { get; set; }
	public virtual float MaximumDistance { get; set; }
	public virtual float ReferenceDistance { get; set; }
	public virtual float RolloffFactor { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentNode

```
public class AVAudioEnvironmentNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioEnvironmentNode ();
	public AVAudioEnvironmentNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationParameters DistanceAttenuationParameters { get; }
	public virtual AVAudio3DAngularOrientation ListenerAngularOrientation { get; set; }
	public virtual MonoMac.OpenGL.Vector3 ListenerPosition { get; set; }
	public virtual AVAudio3DVectorOrientation ListenerVectorOrientation { get; set; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual AVAudioEnvironmentReverbParameters ReverbParameters { get; }
	public virtual float Volume { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject[] ApplicableRenderingAlgorithms ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentReverbParameters

```
public class AVAudioEnvironmentReverbParameters : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentReverbParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentReverbParameters (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentReverbParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enable { get; set; }
	public virtual AVAudioUnitEQFilterParameters FilterParameters { get; }
	public virtual float Level { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void LoadFactoryReverbPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type MonoMac.AVFoundation.AVAudioFile

```
public class AVAudioFile : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFile ();
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AudioSettings settings, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AVAudioCommonFormat format, bool interleaved, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (System.IntPtr handle);
	public AVAudioFile (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioFile (MonoMac.Foundation.NSCoder coder);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AudioSettings settings, AVAudioCommonFormat format, bool interleaved, out MonoMac.Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat FileFormat { get; }
	public virtual long FramePosition { get; set; }
	public virtual long Length { get; }
	public virtual AVAudioFormat ProcessingFormat { get; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, out MonoMac.Foundation.NSError outError);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, uint frames, out MonoMac.Foundation.NSError outError);
	public virtual bool WriteFromBuffer (AVAudioPcmBuffer buffer, out MonoMac.Foundation.NSError outError);
}
```

### New Type MonoMac.AVFoundation.AVAudioFormat

```
public class AVAudioFormat : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFormat ();
	public AVAudioFormat (MonoMac.Foundation.NSDictionary settings);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, bool interleaved, AVAudioChannelLayout layout);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, uint channels, bool interleaved);
	public AVAudioFormat (double sampleRate, AVAudioChannelLayout layout);
	public AVAudioFormat (double sampleRate, uint channels);
	public AVAudioFormat (ref MonoMac.AudioToolbox.AudioStreamBasicDescription description, AVAudioChannelLayout layout);
	public AVAudioFormat (ref MonoMac.AudioToolbox.AudioStreamBasicDescription description);
	public AVAudioFormat (System.IntPtr handle);
	public AVAudioFormat (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioFormat (MonoMac.Foundation.NSCoder coder);
	public AVAudioFormat (AudioSettings settings);
	// properties
	public virtual uint ChannelCount { get; }
	public virtual AVAudioChannelLayout ChannelLayout { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioCommonFormat CommonFormat { get; }
	public virtual bool Interleaved { get; }
	public virtual double SampleRate { get; }
	public AudioSettings Settings { get; }
	public virtual bool Standard { get; }
	public virtual MonoMac.AudioToolbox.AudioStreamBasicDescription StreamDescription { get; }
	public virtual MonoMac.Foundation.NSDictionary WeakSettings { get; }
	// methods
	protected override void Dispose (bool disposing);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioFormat a, AVAudioFormat b);
	public static bool op_Inequality (AVAudioFormat a, AVAudioFormat b);
}
```

### New Type MonoMac.AVFoundation.AVAudioInputNode

```
public class AVAudioInputNode : MonoMac.AVFoundation.AVAudioIONode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioInputNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioInputNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioInputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioIONode

```
public class AVAudioIONode : MonoMac.AVFoundation.AVAudioNode, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioIONode (MonoMac.Foundation.NSCoder coder);
	public AVAudioIONode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioIONode (System.IntPtr handle);
	// properties
	public virtual MonoMac.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual double PresentationLatency { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioMixerNode

```
public class AVAudioMixerNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioMixerNode ();
	public AVAudioMixerNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioMixerNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioMixerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioMixing_Extensions

```
public static class AVAudioMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudioNode

```
public class AVAudioNode : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEngine Engine { get; }
	public virtual AVAudioTime LastRenderTime { get; }
	public virtual uint NumberOfInputs { get; }
	public virtual uint NumberOfOutputs { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual AVAudioFormat GetBusInputFormat (uint bus);
	public virtual AVAudioFormat GetBusOutputFormat (uint bus);
	public virtual string GetNameForInputBus (uint bus);
	public virtual string GetNameForOutputBus (uint bus);
	public virtual void InstallTapOnBus (uint bus, uint bufferSize, AVAudioFormat format, AVAudioNodeTapBlock tapBlock);
	public virtual void RemoveTapOnBus (uint bus);
	public virtual void Reset ();
}
```

### New Type MonoMac.AVFoundation.AVAudioNodeTapBlock

```
public sealed delegate AVAudioNodeTapBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public AVAudioNodeTapBlock (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AVAudioPcmBuffer buffer, AVAudioTime when, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (AVAudioPcmBuffer buffer, AVAudioTime when);
}
```

### New Type MonoMac.AVFoundation.AVAudioOutputNode

```
public class AVAudioOutputNode : MonoMac.AVFoundation.AVAudioIONode, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioOutputNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioOutputNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioOutputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioPcmBuffer

```
public class AVAudioPcmBuffer : MonoMac.AVFoundation.AVAudioBuffer, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioPcmBuffer (MonoMac.Foundation.NSCoder coder);
	public AVAudioPcmBuffer (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioPcmBuffer (System.IntPtr handle);
	public AVAudioPcmBuffer (AVAudioFormat format, uint frameCapacity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.IntPtr FloatChannelData { get; }
	public virtual uint FrameCapacity { get; }
	public virtual uint FrameLength { get; set; }
	public virtual System.IntPtr Int16ChannelData { get; }
	public virtual System.IntPtr Int32ChannelData { get; }
	public virtual uint Stride { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioPlayerNode

```
public class AVAudioPlayerNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioPlayerNode ();
	public AVAudioPlayerNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioPlayerNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioPlayerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual bool Playing { get; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
	// methods
	public virtual AVAudioTime GetNodeTimeFromPlayerTime (AVAudioTime playerTime);
	public virtual AVAudioTime GetPlayerTimeFromNodeTime (AVAudioTime nodeTime);
	public virtual void Pause ();
	public virtual void Play ();
	public virtual void PlayAtTime (AVAudioTime when);
	public virtual void PrepareWithFrameCount (uint frameCount);
	public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, System.Action completionHandler);
	public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, System.Action completionHandler);
	public virtual void ScheduleFile (AVAudioFile file, AVAudioTime when, System.Action completionHandler);
	public virtual void ScheduleSegment (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, System.Action completionHandler);
	public virtual void Stop ();
}
```

### New Type MonoMac.AVFoundation.AVAudioPlayerNodeBufferOptions

```
[Serializable]
[Flags]
public enum AVAudioPlayerNodeBufferOptions {
	Interrupts = 2,
	InterruptsAtLoop = 4,
	Loops = 1,
}
```

### New Type MonoMac.AVFoundation.AVAudioSessionRecordPermission

```
[Serializable]
public enum AVAudioSessionRecordPermission {
	Denied = 1684369017,
	Granted = 1735552628,
	Undetermined = 1970168948,
}
```

### New Type MonoMac.AVFoundation.AVAudioSessionSilenceSecondaryAudioHintType

```
[Serializable]
public enum AVAudioSessionSilenceSecondaryAudioHintType {
	Begin = 1,
	End = 0,
}
```

### New Type MonoMac.AVFoundation.AVAudioStereoMixing

```
public abstract class AVAudioStereoMixing : MonoMac.Foundation.NSObject, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioStereoMixing ();
	public AVAudioStereoMixing (MonoMac.Foundation.NSCoder coder);
	public AVAudioStereoMixing (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioStereoMixing (System.IntPtr handle);
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioStereoMixing_Extensions

```
public static class AVAudioStereoMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudioTime

```
public class AVAudioTime : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioTime ();
	public AVAudioTime (long sampleTime, double sampleRate);
	public AVAudioTime (ulong hostTime);
	public AVAudioTime (ref MonoMac.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public AVAudioTime (System.IntPtr handle);
	public AVAudioTime (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioTime (MonoMac.Foundation.NSCoder coder);
	public AVAudioTime (ulong hostTime, long sampleTime, double sampleRate);
	// properties
	public virtual MonoMac.AudioToolbox.AudioTimeStamp AudioTimeStamp { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual ulong HostTime { get; }
	public virtual bool HostTimeValid { get; }
	public virtual double SampleRate { get; }
	public virtual long SampleTime { get; }
	public virtual bool SampleTimeValid { get; }
	// methods
	public virtual AVAudioTime ExtrapolateTimeFromAnchor (AVAudioTime anchorTime);
	public static AVAudioTime FromAudioTimeStamp (ref MonoMac.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public static AVAudioTime FromHostTime (ulong hostTime);
	public static AVAudioTime FromHostTime (ulong hostTime, long sampleTime, double sampleRate);
	public static AVAudioTime FromSampleTime (long sampleTime, double sampleRate);
	public static ulong HostTimeForSeconds (double seconds);
	public static double SecondsForHostTime (ulong hostTime);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnit

```
public class AVAudioUnit : MonoMac.AVFoundation.AVAudioNode, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnit (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnit (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnit (System.IntPtr handle);
	// properties
	public virtual MonoMac.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual uint Version { get; }
	// methods
	public virtual bool LoadAudioUnitPreset (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDelay

```
public class AVAudioUnitDelay : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDelay ();
	public AVAudioUnitDelay (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitDelay (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitDelay (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DelayTime { get; set; }
	public virtual float Feedback { get; set; }
	public virtual float LowPassCutoff { get; set; }
	public virtual float WetDryMix { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDistortion

```
public class AVAudioUnitDistortion : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDistortion ();
	public AVAudioUnitDistortion (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitDistortion (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitDistortion (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PreGain { get; set; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitDistortionPreset preset);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDistortionPreset

```
[Serializable]
public enum AVAudioUnitDistortionPreset {
	DrumsBitBrush = 0,
	DrumsBufferBeats = 1,
	DrumsLoFi = 2,
	MultiBrokenSpeaker = 3,
	MultiCellphoneConcert = 4,
	MultiDecimated1 = 5,
	MultiDecimated2 = 6,
	MultiDecimated3 = 7,
	MultiDecimated4 = 8,
	MultiDistortedCubed = 10,
	MultiDistortedFunk = 9,
	MultiDistortedSquared = 11,
	MultiEcho1 = 12,
	MultiEcho2 = 13,
	MultiEchoTight1 = 14,
	MultiEchoTight2 = 15,
	MultiEverythingIsBroken = 16,
	SpeechAlienChatter = 17,
	SpeechCosmicInterference = 18,
	SpeechGoldenPi = 19,
	SpeechRadioTower = 20,
	SpeechWaves = 21,
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitEffect

```
public class AVAudioUnitEffect : MonoMac.AVFoundation.AVAudioUnit, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEffect (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEffect (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitEffect (System.IntPtr handle);
	public AVAudioUnitEffect (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitEQ

```
public class AVAudioUnitEQ : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQ ();
	public AVAudioUnitEQ (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEQ (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitEQ (System.IntPtr handle);
	public AVAudioUnitEQ (uint numberOfBands);
	// properties
	public virtual AVAudioUnitEQFilterParameters[] Bands { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalGain { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitEQFilterParameters

```
public class AVAudioUnitEQFilterParameters : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQFilterParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEQFilterParameters (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitEQFilterParameters (System.IntPtr handle);
	// properties
	public virtual float Bandwidth { get; set; }
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioUnitEQFilterType FilterType { get; set; }
	public virtual float Frequency { get; set; }
	public virtual float Gain { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitEQFilterType

```
[Serializable]
public enum AVAudioUnitEQFilterType {
	BandPass = 5,
	BandStop = 6,
	HighPass = 2,
	HighShelf = 8,
	LowPass = 1,
	LowShelf = 7,
	Parametric = 0,
	ResonantHighPass = 4,
	ResonantHighShelf = 10,
	ResonantLowPass = 3,
	ResonantLowShelf = 9,
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitGenerator

```
public class AVAudioUnitGenerator : MonoMac.AVFoundation.AVAudioUnit, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVAudioUnitGenerator (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitGenerator (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitGenerator (System.IntPtr handle);
	public AVAudioUnitGenerator (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitMidiInstrument

```
public class AVAudioUnitMidiInstrument : MonoMac.AVFoundation.AVAudioUnit, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitMidiInstrument (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitMidiInstrument (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitMidiInstrument (System.IntPtr handle);
	public AVAudioUnitMidiInstrument (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void SendController (byte controller, byte value, byte channel);
	public virtual void SendMidiEvent (byte midiStatus, byte data1, byte data2);
	public virtual void SendMidiEvent (byte midiStatus, byte data1);
	public virtual void SendMidiSysExEvent (MonoMac.Foundation.NSData midiData);
	public virtual void SendPitchBend (ushort pitchbend, byte channel);
	public virtual void SendPressure (byte pressure, byte channel);
	public virtual void SendPressureForKey (byte key, byte value, byte channel);
	public virtual void SendProgramChange (byte program, byte channel);
	public virtual void SendProgramChange (byte program, byte bankMSB, byte bankLSB, byte channel);
	public virtual void StartNote (byte note, byte velocity, byte channel);
	public virtual void StopNote (byte note, byte channel);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitReverb

```
public class AVAudioUnitReverb : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitReverb ();
	public AVAudioUnitReverb (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitReverb (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitReverb (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitReverbPreset

```
[Serializable]
public enum AVAudioUnitReverbPreset {
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
```

### New Type MonoMac.AVFoundation.AVAudioUnitSampler

```
public class AVAudioUnitSampler : MonoMac.AVFoundation.AVAudioUnitMidiInstrument, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitSampler ();
	public AVAudioUnitSampler (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitSampler (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitSampler (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalTuning { get; set; }
	public virtual float MasterGain { get; set; }
	public virtual float StereoPan { get; set; }
	// methods
	public virtual bool LoadAudioFiles (MonoMac.Foundation.NSUrl[] audioFiles, out MonoMac.Foundation.NSError outError);
	public virtual bool LoadInstrument (MonoMac.Foundation.NSUrl instrumentUrl, out MonoMac.Foundation.NSError outError);
	public virtual bool LoadSoundBank (MonoMac.Foundation.NSUrl bankUrl, byte program, byte bankMSB, byte bankLSB, out MonoMac.Foundation.NSError outError);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitTimeEffect

```
public class AVAudioUnitTimeEffect : MonoMac.AVFoundation.AVAudioUnit, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimeEffect (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitTimeEffect (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitTimeEffect (System.IntPtr handle);
	public AVAudioUnitTimeEffect (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitTimePitch

```
public class AVAudioUnitTimePitch : MonoMac.AVFoundation.AVAudioUnitTimeEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimePitch ();
	public AVAudioUnitTimePitch (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitTimePitch (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitTimePitch (System.IntPtr handle);
	public AVAudioUnitTimePitch (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Overlap { get; set; }
	public virtual float Pitch { get; set; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitVarispeed

```
public class AVAudioUnitVarispeed : MonoMac.AVFoundation.AVAudioUnitTimeEffect, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitVarispeed ();
	public AVAudioUnitVarispeed (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitVarispeed (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitVarispeed (System.IntPtr handle);
	public AVAudioUnitVarispeed (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVCaptureAudioFileOutput

```
public class AVCaptureAudioFileOutput : MonoMac.AVFoundation.AVCaptureFileOutput, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureAudioFileOutput ();
	public AVCaptureAudioFileOutput (MonoMac.Foundation.NSCoder coder);
	public AVCaptureAudioFileOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureAudioFileOutput (System.IntPtr handle);
	// properties
	public AudioSettings AudioSettings { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVMetadataItem[] Metadata { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakAudioSettings { get; set; }
	// methods
	public static MonoMac.Foundation.NSString[] AvailableOutputFileTypes ();
	protected override void Dispose (bool disposing);
	public virtual void StartRecording (MonoMac.Foundation.NSUrl outputFileUrl, string fileType, AVCaptureFileOutputRecordingDelegate recordingDelegate);
}
```

### New Type MonoMac.AVFoundation.AVCaptureAudioPreviewOutput

```
public class AVCaptureAudioPreviewOutput : MonoMac.AVFoundation.AVCaptureOutput, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureAudioPreviewOutput ();
	public AVCaptureAudioPreviewOutput (MonoMac.Foundation.NSCoder coder);
	public AVCaptureAudioPreviewOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureAudioPreviewOutput (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSString OutputDeviceUniqueID { get; set; }
	public virtual float Volume { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVCaptureAutoFocusSystem

```
[Serializable]
public enum AVCaptureAutoFocusSystem {
	ContrastDetection = 1,
	None = 0,
	PhaseDetection = 2,
}
```

### New Type MonoMac.AVFoundation.AVCaptureDeviceFormat

```
public class AVCaptureDeviceFormat : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureDeviceFormat (MonoMac.Foundation.NSCoder coder);
	public AVCaptureDeviceFormat (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureDeviceFormat (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMFormatDescription FormatDescription { get; }
	public virtual MonoMac.Foundation.NSString MediaType { get; }
	public virtual AVFrameRateRange[] VideoSupportedFrameRateRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVCaptureDeviceInputSource

```
public class AVCaptureDeviceInputSource : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureDeviceInputSource ();
	public AVCaptureDeviceInputSource (MonoMac.Foundation.NSCoder coder);
	public AVCaptureDeviceInputSource (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureDeviceInputSource (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string InputSourceID { get; }
	public virtual string LocalizedName { get; }
}
```

### New Type MonoMac.AVFoundation.AVCaptureScreenInput

```
public class AVCaptureScreenInput : MonoMac.AVFoundation.AVCaptureInput, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureScreenInput ();
	public AVCaptureScreenInput (MonoMac.Foundation.NSCoder coder);
	public AVCaptureScreenInput (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureScreenInput (System.IntPtr handle);
	public AVCaptureScreenInput (uint displayID);
	// properties
	public virtual bool CapturesCursor { get; set; }
	public virtual bool CapturesMouseClicks { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF CropRect { get; set; }
	public virtual MonoMac.CoreMedia.CMTime MinFrameDuration { get; set; }
	public virtual bool RemovesDuplicateFrames { get; set; }
	public virtual float ScaleFactor { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVCaptureVideoStabilizationMode

```
[Serializable]
public enum AVCaptureVideoStabilizationMode {
	Auto = 3,
	Cinematic = 2,
	Off = 0,
	Standard = 1,
}
```

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceChromaticityValues

```
public struct AVCaptureWhiteBalanceChromaticityValues {
	// constructors
	public AVCaptureWhiteBalanceChromaticityValues (float x, float y);
	// fields
	public float X;
	public float Y;
	// methods
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceGains

```
public struct AVCaptureWhiteBalanceGains {
	// constructors
	public AVCaptureWhiteBalanceGains (float redGain, float greenGain, float blueGain);
	// fields
	public float BlueGain;
	public float GreenGain;
	public float RedGain;
	// methods
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues

```
public struct AVCaptureWhiteBalanceTemperatureAndTintValues {
	// constructors
	public AVCaptureWhiteBalanceTemperatureAndTintValues (float temperature, float tint);
	// fields
	public float Temperature;
	public float Tint;
	// methods
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVLayerVideoGravity

```
[Serializable]
public enum AVLayerVideoGravity {
	Resize = 2,
	ResizeAspect = 0,
	ResizeAspectFill = 1,
}
```

### New Type MonoMac.AVFoundation.AVMetadataIdentifiers

```
public static class AVMetadataIdentifiers {

	// inner types
	public static class CommonIdentifier {
		// properties
		public static MonoMac.Foundation.NSString AlbumName { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString Artwork { get; }
		public static MonoMac.Foundation.NSString AssetIdentifier { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString Contributor { get; }
		public static MonoMac.Foundation.NSString Copyrights { get; }
		public static MonoMac.Foundation.NSString CreationDate { get; }
		public static MonoMac.Foundation.NSString Creator { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString Format { get; }
		public static MonoMac.Foundation.NSString Language { get; }
		public static MonoMac.Foundation.NSString LastModifiedDate { get; }
		public static MonoMac.Foundation.NSString Location { get; }
		public static MonoMac.Foundation.NSString Make { get; }
		public static MonoMac.Foundation.NSString Model { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString Relation { get; }
		public static MonoMac.Foundation.NSString Software { get; }
		public static MonoMac.Foundation.NSString Source { get; }
		public static MonoMac.Foundation.NSString Subject { get; }
		public static MonoMac.Foundation.NSString Title { get; }
		public static MonoMac.Foundation.NSString Type { get; }
	}
	public static class QuickTime {
		// properties
		public static MonoMac.Foundation.NSString UserDataAlbum { get; }
		public static MonoMac.Foundation.NSString UserDataArranger { get; }
		public static MonoMac.Foundation.NSString UserDataArtist { get; }
		public static MonoMac.Foundation.NSString UserDataAuthor { get; }
		public static MonoMac.Foundation.NSString UserDataChapter { get; }
		public static MonoMac.Foundation.NSString UserDataComment { get; }
		public static MonoMac.Foundation.NSString UserDataComposer { get; }
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataCreationDate { get; }
		public static MonoMac.Foundation.NSString UserDataCredits { get; }
		public static MonoMac.Foundation.NSString UserDataDescription { get; }
		public static MonoMac.Foundation.NSString UserDataDirector { get; }
		public static MonoMac.Foundation.NSString UserDataDisclaimer { get; }
		public static MonoMac.Foundation.NSString UserDataEncodedBy { get; }
		public static MonoMac.Foundation.NSString UserDataFullName { get; }
		public static MonoMac.Foundation.NSString UserDataGenre { get; }
		public static MonoMac.Foundation.NSString UserDataHostComputer { get; }
		public static MonoMac.Foundation.NSString UserDataInformation { get; }
		public static MonoMac.Foundation.NSString UserDataKeywords { get; }
		public static MonoMac.Foundation.NSString UserDataLocationISO6709 { get; }
		public static MonoMac.Foundation.NSString UserDataMake { get; }
		public static MonoMac.Foundation.NSString UserDataModel { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalArtist { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalFormat { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalSource { get; }
		public static MonoMac.Foundation.NSString UserDataPerformers { get; }
		public static MonoMac.Foundation.NSString UserDataPhonogramRights { get; }
		public static MonoMac.Foundation.NSString UserDataProducer { get; }
		public static MonoMac.Foundation.NSString UserDataProduct { get; }
		public static MonoMac.Foundation.NSString UserDataPublisher { get; }
		public static MonoMac.Foundation.NSString UserDataSoftware { get; }
		public static MonoMac.Foundation.NSString UserDataSpecialPlaybackRequirements { get; }
		public static MonoMac.Foundation.NSString UserDataTaggedCharacteristic { get; }
		public static MonoMac.Foundation.NSString UserDataTrack { get; }
		public static MonoMac.Foundation.NSString UserDataTrackName { get; }
		public static MonoMac.Foundation.NSString UserDataUrlLink { get; }
		public static MonoMac.Foundation.NSString UserDataWarning { get; }
		public static MonoMac.Foundation.NSString UserDataWriter { get; }
	}
	public static class Iso {
		// properties
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataTaggedCharacteristic { get; }
	}
	public static class ThreeGP {
		// properties
		public static MonoMac.Foundation.NSString UserDataAlbumAndTrack { get; }
		public static MonoMac.Foundation.NSString UserDataAuthor { get; }
		public static MonoMac.Foundation.NSString UserDataCollection { get; }
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataDescription { get; }
		public static MonoMac.Foundation.NSString UserDataGenre { get; }
		public static MonoMac.Foundation.NSString UserDataKeywordList { get; }
		public static MonoMac.Foundation.NSString UserDataLocation { get; }
		public static MonoMac.Foundation.NSString UserDataMediaClassification { get; }
		public static MonoMac.Foundation.NSString UserDataMediaRating { get; }
		public static MonoMac.Foundation.NSString UserDataPerformer { get; }
		public static MonoMac.Foundation.NSString UserDataRecordingYear { get; }
		public static MonoMac.Foundation.NSString UserDataThumbnail { get; }
		public static MonoMac.Foundation.NSString UserDataTitle { get; }
		public static MonoMac.Foundation.NSString UserDataUserRating { get; }
	}
	public static class QuickTimeMetadata {
		// properties
		public static MonoMac.Foundation.NSString Album { get; }
		public static MonoMac.Foundation.NSString Arranger { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString Artwork { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString CameraFrameReadoutTime { get; }
		public static MonoMac.Foundation.NSString CameraIdentifier { get; }
		public static MonoMac.Foundation.NSString CollectionUser { get; }
		public static MonoMac.Foundation.NSString Comment { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CreationDate { get; }
		public static MonoMac.Foundation.NSString Credits { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString DirectionFacing { get; }
		public static MonoMac.Foundation.NSString DirectionMotion { get; }
		public static MonoMac.Foundation.NSString Director { get; }
		public static MonoMac.Foundation.NSString DisplayName { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString Genre { get; }
		public static MonoMac.Foundation.NSString Information { get; }
		public static MonoMac.Foundation.NSString iXML { get; }
		public static MonoMac.Foundation.NSString Keywords { get; }
		public static MonoMac.Foundation.NSString LocationBody { get; }
		public static MonoMac.Foundation.NSString LocationDate { get; }
		public static MonoMac.Foundation.NSString LocationISO6709 { get; }
		public static MonoMac.Foundation.NSString LocationName { get; }
		public static MonoMac.Foundation.NSString LocationNote { get; }
		public static MonoMac.Foundation.NSString LocationRole { get; }
		public static MonoMac.Foundation.NSString Make { get; }
		public static MonoMac.Foundation.NSString Model { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString Performer { get; }
		public static MonoMac.Foundation.NSString PhonogramRights { get; }
		public static MonoMac.Foundation.NSString PreferredAffineTransform { get; }
		public static MonoMac.Foundation.NSString Producer { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RatingUser { get; }
		public static MonoMac.Foundation.NSString Software { get; }
		public static MonoMac.Foundation.NSString Title { get; }
		public static MonoMac.Foundation.NSString Year { get; }
	}
	public static class iTunesMetadata {
		// properties
		public static MonoMac.Foundation.NSString AccountKind { get; }
		public static MonoMac.Foundation.NSString Acknowledgement { get; }
		public static MonoMac.Foundation.NSString Album { get; }
		public static MonoMac.Foundation.NSString AlbumArtist { get; }
		public static MonoMac.Foundation.NSString AppleID { get; }
		public static MonoMac.Foundation.NSString Arranger { get; }
		public static MonoMac.Foundation.NSString ArtDirector { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString ArtistID { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString BeatsPerMin { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Conductor { get; }
		public static MonoMac.Foundation.NSString ContentRating { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CoverArt { get; }
		public static MonoMac.Foundation.NSString Credits { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString Director { get; }
		public static MonoMac.Foundation.NSString DiscCompilation { get; }
		public static MonoMac.Foundation.NSString DiscNumber { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString EncodingTool { get; }
		public static MonoMac.Foundation.NSString EQ { get; }
		public static MonoMac.Foundation.NSString ExecProducer { get; }
		public static MonoMac.Foundation.NSString GenreID { get; }
		public static MonoMac.Foundation.NSString Grouping { get; }
		public static MonoMac.Foundation.NSString LinerNotes { get; }
		public static MonoMac.Foundation.NSString Lyrics { get; }
		public static MonoMac.Foundation.NSString OnlineExtras { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString Performer { get; }
		public static MonoMac.Foundation.NSString PhonogramRights { get; }
		public static MonoMac.Foundation.NSString PlaylistID { get; }
		public static MonoMac.Foundation.NSString PredefinedGenre { get; }
		public static MonoMac.Foundation.NSString Producer { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RecordCompany { get; }
		public static MonoMac.Foundation.NSString ReleaseDate { get; }
		public static MonoMac.Foundation.NSString Soloist { get; }
		public static MonoMac.Foundation.NSString SongID { get; }
		public static MonoMac.Foundation.NSString SongName { get; }
		public static MonoMac.Foundation.NSString SoundEngineer { get; }
		public static MonoMac.Foundation.NSString Thanks { get; }
		public static MonoMac.Foundation.NSString TrackNumber { get; }
		public static MonoMac.Foundation.NSString TrackSubTitle { get; }
		public static MonoMac.Foundation.NSString UserComment { get; }
		public static MonoMac.Foundation.NSString UserGenre { get; }
	}
	public static class ID3Metadata {
		// properties
		public static MonoMac.Foundation.NSString AlbumSortOrder { get; }
		public static MonoMac.Foundation.NSString AlbumTitle { get; }
		public static MonoMac.Foundation.NSString AttachedPicture { get; }
		public static MonoMac.Foundation.NSString AudioEncryption { get; }
		public static MonoMac.Foundation.NSString AudioSeekPointIndex { get; }
		public static MonoMac.Foundation.NSString Band { get; }
		public static MonoMac.Foundation.NSString BeatsPerMinute { get; }
		public static MonoMac.Foundation.NSString Comments { get; }
		public static MonoMac.Foundation.NSString CommercialInformation { get; }
		public static MonoMac.Foundation.NSString Commerical { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Conductor { get; }
		public static MonoMac.Foundation.NSString ContentGroupDescription { get; }
		public static MonoMac.Foundation.NSString ContentType { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CopyrightInformation { get; }
		public static MonoMac.Foundation.NSString Date { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString EncodedWith { get; }
		public static MonoMac.Foundation.NSString EncodingTime { get; }
		public static MonoMac.Foundation.NSString Encryption { get; }
		public static MonoMac.Foundation.NSString Equalization { get; }
		public static MonoMac.Foundation.NSString Equalization2 { get; }
		public static MonoMac.Foundation.NSString EventTimingCodes { get; }
		public static MonoMac.Foundation.NSString FileOwner { get; }
		public static MonoMac.Foundation.NSString FileType { get; }
		public static MonoMac.Foundation.NSString GeneralEncapsulatedObject { get; }
		public static MonoMac.Foundation.NSString GroupIdentifier { get; }
		public static MonoMac.Foundation.NSString InitialKey { get; }
		public static MonoMac.Foundation.NSString InternationalStandardRecordingCode { get; }
		public static MonoMac.Foundation.NSString InternetRadioStationName { get; }
		public static MonoMac.Foundation.NSString InternetRadioStationOwner { get; }
		public static MonoMac.Foundation.NSString InvolvedPeopleList_v23 { get; }
		public static MonoMac.Foundation.NSString InvolvedPeopleList_v24 { get; }
		public static MonoMac.Foundation.NSString Language { get; }
		public static MonoMac.Foundation.NSString LeadPerformer { get; }
		public static MonoMac.Foundation.NSString Length { get; }
		public static MonoMac.Foundation.NSString Link { get; }
		public static MonoMac.Foundation.NSString Lyricist { get; }
		public static MonoMac.Foundation.NSString MediaType { get; }
		public static MonoMac.Foundation.NSString ModifiedBy { get; }
		public static MonoMac.Foundation.NSString Mood { get; }
		public static MonoMac.Foundation.NSString MpegLocationLookupTable { get; }
		public static MonoMac.Foundation.NSString MusicCDIdentifier { get; }
		public static MonoMac.Foundation.NSString MusicianCreditsList { get; }
		public static MonoMac.Foundation.NSString OfficialArtistWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialAudioFileWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialAudioSourceWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialInternetRadioStationHomepage { get; }
		public static MonoMac.Foundation.NSString OfficialPublisherWebpage { get; }
		public static MonoMac.Foundation.NSString OriginalAlbumTitle { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString OriginalFilename { get; }
		public static MonoMac.Foundation.NSString OriginalLyricist { get; }
		public static MonoMac.Foundation.NSString OriginalReleaseTime { get; }
		public static MonoMac.Foundation.NSString OriginalReleaseYear { get; }
		public static MonoMac.Foundation.NSString Ownership { get; }
		public static MonoMac.Foundation.NSString PartOfASet { get; }
		public static MonoMac.Foundation.NSString Payment { get; }
		public static MonoMac.Foundation.NSString PerformerSortOrder { get; }
		public static MonoMac.Foundation.NSString PlayCounter { get; }
		public static MonoMac.Foundation.NSString PlaylistDelay { get; }
		public static MonoMac.Foundation.NSString Popularimeter { get; }
		public static MonoMac.Foundation.NSString PositionSynchronization { get; }
		public static MonoMac.Foundation.NSString Private { get; }
		public static MonoMac.Foundation.NSString ProducedNotice { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RecommendedBufferSize { get; }
		public static MonoMac.Foundation.NSString RecordingDates { get; }
		public static MonoMac.Foundation.NSString RecordingTime { get; }
		public static MonoMac.Foundation.NSString RelativeVolumeAdjustment { get; }
		public static MonoMac.Foundation.NSString RelativeVolumeAdjustment2 { get; }
		public static MonoMac.Foundation.NSString ReleaseTime { get; }
		public static MonoMac.Foundation.NSString Reverb { get; }
		public static MonoMac.Foundation.NSString Seek { get; }
		public static MonoMac.Foundation.NSString SetSubtitle { get; }
		public static MonoMac.Foundation.NSString Signature { get; }
		public static MonoMac.Foundation.NSString Size { get; }
		public static MonoMac.Foundation.NSString SubTitle { get; }
		public static MonoMac.Foundation.NSString SynchronizedLyric { get; }
		public static MonoMac.Foundation.NSString SynchronizedTempoCodes { get; }
		public static MonoMac.Foundation.NSString TaggingTime { get; }
		public static MonoMac.Foundation.NSString TermsOfUse { get; }
		public static MonoMac.Foundation.NSString Time { get; }
		public static MonoMac.Foundation.NSString TitleDescription { get; }
		public static MonoMac.Foundation.NSString TitleSortOrder { get; }
		public static MonoMac.Foundation.NSString TrackNumber { get; }
		public static MonoMac.Foundation.NSString UniqueFileIdentifier { get; }
		public static MonoMac.Foundation.NSString UnsynchronizedLyric { get; }
		public static MonoMac.Foundation.NSString UserText { get; }
		public static MonoMac.Foundation.NSString UserUrl { get; }
		public static MonoMac.Foundation.NSString Year { get; }
	}
	public static class IcyMetadata {
		// properties
		public static MonoMac.Foundation.NSString StreamTitle { get; }
		public static MonoMac.Foundation.NSString StreamUrl { get; }
	}
}
```

### New Type MonoMac.AVFoundation.AVMetadataObjectType

```
[Serializable]
[Flags]
public enum AVMetadataObjectType {
	AztecCode = 2,
	Code128Code = 4,
	Code39Code = 8,
	Code39Mod43Code = 16,
	Code93Code = 32,
	DataMatrixCode = 8192,
	EAN13Code = 64,
	EAN8Code = 128,
	Face = 1,
	Interleaved2of5Code = 2048,
	ITF14Code = 4096,
	None = 0,
	PDF417Code = 256,
	QRCode = 512,
	UPCECode = 1024,
}
```

### New Type MonoMac.AVFoundation.AVMidiPlayer

```
public class AVMidiPlayer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMidiPlayer ();
	public AVMidiPlayer (MonoMac.Foundation.NSCoder coder);
	public AVMidiPlayer (MonoMac.Foundation.NSObjectFlag t);
	public AVMidiPlayer (System.IntPtr handle);
	public AVMidiPlayer (MonoMac.Foundation.NSUrl contentsUrl, MonoMac.Foundation.NSUrl soundBankUrl, out MonoMac.Foundation.NSError outError);
	public AVMidiPlayer (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSUrl sounddBankUrl, out MonoMac.Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double CurrentPosition { get; set; }
	public virtual double Duration { get; }
	public virtual bool Playing { get; }
	public virtual float Rate { get; set; }
	// methods
	public virtual void Play (System.Action completionHandler);
	public virtual System.Threading.Tasks.Task PlayAsync ();
	public virtual void PrepareToPlay ();
	public virtual void Stop ();
}
```

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutput

```
public class AVPlayerItemMetadataOutput : MonoMac.AVFoundation.AVPlayerItemOutput, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutput ();
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutput (System.IntPtr handle);
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSString[] metadataIdentifiers);
	// properties
	public virtual double AdvanceIntervalForDelegateInvocation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public AVPlayerItemMetadataOutputPushDelegate Delegate { get; }
	public virtual MonoMac.CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemMetadataOutputPushDelegate pushDelegate, MonoMac.CoreFoundation.DispatchQueue delegateQueue);
}
```

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutputPushDelegate

```
public class AVPlayerItemMetadataOutputPushDelegate : MonoMac.Foundation.NSObject, IAVPlayerItemMetadataOutputPushDelegate, IAVPlayerItemOutputPushDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVPlayerItemMetadataOutputPushDelegate ();
	public AVPlayerItemMetadataOutputPushDelegate (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutputPushDelegate (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void DidOutputTimedMetadataGroups (AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
```

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutputPushDelegate_Extensions

```
public static class AVPlayerItemMetadataOutputPushDelegate_Extensions {
	// methods
	public static void DidOutputTimedMetadataGroups (IAVPlayerItemMetadataOutputPushDelegate This, AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
}
```

### New Type MonoMac.AVFoundation.AVQueuedSampleBufferRenderingStatus

```
[Serializable]
public enum AVQueuedSampleBufferRenderingStatus {
	Failed = 2,
	Rendering = 1,
	Unknown = 0,
}
```

### New Type MonoMac.AVFoundation.AVSampleBufferDisplayLayer

```
public class AVSampleBufferDisplayLayer : MonoMac.CoreAnimation.CALayer, MonoMac.CoreAnimation.ICAMediaTiming, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public AVSampleBufferDisplayLayer ();
	public AVSampleBufferDisplayLayer (MonoMac.Foundation.NSCoder coder);
	public AVSampleBufferDisplayLayer (MonoMac.Foundation.NSObjectFlag t);
	public AVSampleBufferDisplayLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMTimebase ControlTimebase { get; set; }
	public virtual MonoMac.Foundation.NSError Error { get; }
	public virtual bool ReadyForMoreMediaData { get; }
	public virtual AVQueuedSampleBufferRenderingStatus Status { get; }
	public virtual string VideoGravity { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnqueueSampleBuffer (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer);
	public virtual void Flush ();
	public virtual void FlushAndRemoveImage ();
	public virtual void RequestMediaDataWhenReadyOnQueue (MonoMac.CoreFoundation.DispatchQueue queue, System.Action enqueuer);
	public virtual void StopRequestingMediaData ();
}
```

### New Type MonoMac.AVFoundation.AVUtilities

```
public static class AVUtilities {
	// methods
	public static System.Drawing.RectangleF WithAspectRatio (System.Drawing.RectangleF self, System.Drawing.SizeF aspectRatio);
}
```

### New Type MonoMac.AVFoundation.IAVAudio3DMixing

```
public interface IAVAudio3DMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVAudioMixing

```
public interface IAVAudioMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IAVAudio3DMixing, IAVAudioStereoMixing {
	// properties
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVAudioStereoMixing

```
public interface IAVAudioStereoMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVPlayerItemMetadataOutputPushDelegate

```
public interface IAVPlayerItemMetadataOutputPushDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IAVPlayerItemOutputPushDelegate {
}
```

## Namespace MonoMac.CoreAnimation

### Type Changed: MonoMac.CoreAnimation.CAAction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public static MonoMac.Foundation.NSString AnimationCubic { get; }
	public static MonoMac.Foundation.NSString AnimationCubicPaced { get; }
	public virtual MonoMac.SceneKit.SCNAnimationEvent[] AnimationEvents { get; set; }
	public virtual float FadeInDuration { get; set; }
	public virtual float FadeOutDuration { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CAAnimationDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAAnimationGroup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CABasicAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAConstraint

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAConstraintLayoutManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAEmitterBehavior

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAEmitterCell

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAEmitterLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
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

### Type Changed: MonoMac.CoreAnimation.CAGradientLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.Foundation.NSNumber[] BiasValues { get; set; }
	public virtual MonoMac.Foundation.NSNumber[] ContinuityValues { get; set; }
	public virtual MonoMac.Foundation.NSNumber[] TensionValues { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CALayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.CoreImage.CIFilter[] BackgroundFilters { get; set; }
	public virtual MonoMac.Foundation.NSObject CompositingFilter { get; set; }
	public virtual float ContentsScale { get; set; }
	public virtual float MinificationFilterBias { get; set; }
	public virtual MonoMac.Foundation.NSDictionary Style { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CALayerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.CoreAnimation.CAMediaTiming

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAMediaTiming_Extensions

Added methods:

```
public static bool GetAutoReverses (ICAMediaTiming This);
	public static double GetBeginTime (ICAMediaTiming This);
	public static double GetDuration (ICAMediaTiming This);
	public static string GetFillMode (ICAMediaTiming This);
	public static float GetRepeatCount (ICAMediaTiming This);
	public static double GetRepeatDuration (ICAMediaTiming This);
	public static float GetSpeed (ICAMediaTiming This);
	public static double GetTimeOffset (ICAMediaTiming This);
	public static void SetAutoReverses (ICAMediaTiming This, bool value);
	public static void SetBeginTime (ICAMediaTiming This, double value);
	public static void SetDuration (ICAMediaTiming This, double value);
	public static void SetFillMode (ICAMediaTiming This, string value);
	public static void SetRepeatCount (ICAMediaTiming This, float value);
	public static void SetRepeatDuration (ICAMediaTiming This, double value);
	public static void SetSpeed (ICAMediaTiming This, float value);
	public static void SetTimeOffset (ICAMediaTiming This, double value);
```

### Type Changed: MonoMac.CoreAnimation.CAMediaTimingFunction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAOpenGLLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAPropertyAnimation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAReplicatorLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAScrollLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CAShapeLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CATextLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CATiledLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CATransaction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CATransformLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreAnimation.CATransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual MonoMac.Foundation.NSObject filter { get; set; }
```

Added properties:

```
[Obsolete ("The name has been fixed, use Filter instead")]
	public MonoMac.Foundation.NSObject filter { get; set; }
	public virtual MonoMac.Foundation.NSObject Filter { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CAValueFunction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

## Namespace MonoMac.CoreBluetooth

### Type Changed: MonoMac.CoreBluetooth.CBATTRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBCentral

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBCentralManager

Added constructor:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoMac.CoreFoundation.DispatchQueue queue, CBCentralInitOptions options);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBCentralManagerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBCharacteristic

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed properties:

```
public virtual CBDescriptor[] Descriptors { get; }
	public virtual CBCharacteristicProperties Properties { get; }
	public virtual MonoMac.Foundation.NSData Value { get; }
```

Added properties:

```
public virtual CBDescriptor[] Descriptors { get; set; }
	public virtual CBCharacteristicProperties Properties { get; set; }
	public virtual MonoMac.Foundation.NSData Value { get; set; }
```

### Type Changed: MonoMac.CoreBluetooth.CBDescriptor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBError

Added value:

```
ConnectionFailed = 10,
```

### Type Changed: MonoMac.CoreBluetooth.CBMutableCharacteristic

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBMutableDescriptor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBMutableService

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheral

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed events:

```
public event System.EventHandler<NSErrorEventArgs> DiscoveredService;

	[Obsolete ("Deprecated in iOS7")]
	[Obsolete ("Deprecated in iOS7")]
	public event System.EventHandler InvalidatedService;
	public event System.EventHandler<NSErrorEventArgs> RssiUpdated;
```

Added events:

```
public event System.EventHandler<MonoMac.Foundation.NSErrorEventArgs> DiscoveredService;
	public event System.EventHandler InvalidatedService;
	public event System.EventHandler<CBRssiEventArgs> RssiRead;
	public event System.EventHandler<MonoMac.Foundation.NSErrorEventArgs> RssiUpdated;
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheralDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual void RssiRead (CBPeripheral peripheral, MonoMac.Foundation.NSNumber rssi, MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheralDelegate_Extensions

Added method:

```
public static void RssiRead (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoMac.Foundation.NSNumber rssi, MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheralManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed event:

```
public event System.EventHandler<NSErrorEventArgs> AdvertisingStarted;
```

Added event:

```
public event System.EventHandler<MonoMac.Foundation.NSErrorEventArgs> AdvertisingStarted;
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheralManagerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.CBService

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed properties:

```
public virtual CBCharacteristic[] Characteristics { get; }
	public virtual CBService[] IncludedServices { get; }
	public virtual bool Primary { get; }
```

Added properties:

```
public virtual CBCharacteristic[] Characteristics { get; set; }
	public virtual CBService[] IncludedServices { get; set; }
	public virtual bool Primary { get; set; }
```

### Type Changed: MonoMac.CoreBluetooth.CBUUID

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreBluetooth.PeripheralScanningOptions

Removed property:

```
public bool AllowDuplicatesKey { set; }
```

Added property:

```
public bool AllowDuplicatesKey { get; set; }
```

### Type Changed: MonoMac.CoreBluetooth.StartAdvertisingOptions

Removed property:

```
public CBUUID[] ServicesUUID { set; }
```

Added property:

```
public CBUUID[] ServicesUUID { get; set; }
```

### Removed Type MonoMac.CoreBluetooth.NSErrorEventArgs ### New Type MonoMac.CoreBluetooth.CBCentralInitOptions

```
public class CBCentralInitOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public CBCentralInitOptions ();
	public CBCentralInitOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? ShowPowerAlert { get; set; }
}
```

### New Type MonoMac.CoreBluetooth.CBRssiEventArgs

```
public class CBRssiEventArgs : System.EventArgs {
	// constructors
	public CBRssiEventArgs (MonoMac.Foundation.NSNumber rssi, MonoMac.Foundation.NSError error);
	// properties
	public MonoMac.Foundation.NSError Error { get; set; }
	public MonoMac.Foundation.NSNumber Rssi { get; set; }
}
```



## Namespace MonoMac.CoreData

### Type Changed: MonoMac.CoreData.NSAtomicStore

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSAtomicStoreCacheNode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSAttributeDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSAttributeType

Added value:

```
ObjectID = 2000,
```

### Type Changed: MonoMac.CoreData.NSEntityDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSEntityMapping

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSEntityMigrationPolicy

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSFetchedPropertyDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSFetchRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSIncrementalStore

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSIncrementalStoreNode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSManagedObject

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSManagedObjectContext

Added interfaces:

```
MonoMac.Foundation.INSLocking
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual string Name { get; set; }
```

Added method:

```
public virtual NSPersistentStoreResult ExecuteRequest (NSPersistentStoreRequest request, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreData.NSManagedObjectID

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSManagedObjectModel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSMappingModel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSMergeConflict

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSMergePolicy

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSMigrationManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSPersistentStore

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator

Obsoleted constructor:

```
[Obsolete ("Use .ctor(NSManagedObjectModel)")]
	public NSPersistentStoreCoordinator ();
```

Added interfaces:

```
MonoMac.Foundation.INSLocking
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual string Name { get; set; }
```

Added methods:

```
public virtual void Perform (System.Action code);
	public virtual void PerformAndWait (System.Action code);
```

### Type Changed: MonoMac.CoreData.NSPersistentStoreRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSPersistentStoreRequestType

Added value:

```
BatchUpdate = 6,
```

### Type Changed: MonoMac.CoreData.NSPropertyDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSPropertyMapping

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSRelationshipDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreData.NSSaveChangesRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.CoreData.NSAsynchronousFetchRequest

```
public class NSAsynchronousFetchRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSAsynchronousFetchRequest ();
	public NSAsynchronousFetchRequest (MonoMac.Foundation.NSCoder coder);
	public NSAsynchronousFetchRequest (MonoMac.Foundation.NSObjectFlag t);
	public NSAsynchronousFetchRequest (System.IntPtr handle);
	public NSAsynchronousFetchRequest (NSFetchRequest request, System.Action<NSAsynchronousFetchResult> completion);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int EstimatedResultCount { get; set; }
	public virtual NSFetchRequest FetchRequest { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSAsynchronousFetchResult

```
public class NSAsynchronousFetchResult : MonoMac.CoreData.NSPersistentStoreAsynchronousResult, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchResult ();
	public NSAsynchronousFetchResult (MonoMac.Foundation.NSCoder coder);
	public NSAsynchronousFetchResult (MonoMac.Foundation.NSObjectFlag t);
	public NSAsynchronousFetchResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSAsynchronousFetchRequest FetchRequest { get; }
	public virtual MonoMac.Foundation.NSObject[] FinalResult { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSBatchUpdateRequest

```
public class NSBatchUpdateRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSBatchUpdateRequest ();
	public NSBatchUpdateRequest (MonoMac.Foundation.NSCoder coder);
	public NSBatchUpdateRequest (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchUpdateRequest (System.IntPtr handle);
	public NSBatchUpdateRequest (string entityName);
	public NSBatchUpdateRequest (NSEntityDescription entity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSEntityDescription Entity { get; }
	public virtual string EntityName { get; }
	public virtual bool IncludesSubentities { get; set; }
	public virtual MonoMac.Foundation.NSPredicate Predicate { get; set; }
	public virtual MonoMac.Foundation.NSDictionary PropertiesToUpdate { get; set; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; set; }
	// methods
	public static NSBatchUpdateRequest BatchUpdateRequestWithEntityName (string entityName);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSBatchUpdateRequestResultType

```
[Serializable]
public enum NSBatchUpdateRequestResultType {
	StatusOnly = 0,
	UpdatedObjectIDs = 1,
	UpdatedObjectsCount = 2,
}
```

### New Type MonoMac.CoreData.NSBatchUpdateResult

```
public class NSBatchUpdateResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateResult ();
	public NSBatchUpdateResult (MonoMac.Foundation.NSCoder coder);
	public NSBatchUpdateResult (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchUpdateResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSObject Result { get; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSPersistentStoreAsynchronousResult

```
public class NSPersistentStoreAsynchronousResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreAsynchronousResult ();
	public NSPersistentStoreAsynchronousResult (MonoMac.Foundation.NSCoder coder);
	public NSPersistentStoreAsynchronousResult (MonoMac.Foundation.NSObjectFlag t);
	public NSPersistentStoreAsynchronousResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSManagedObjectContext ManagedObjectContext { get; }
	public virtual MonoMac.Foundation.NSError OperationError { get; }
	public virtual MonoMac.Foundation.NSProgress Progress { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSPersistentStoreResult

```
public class NSPersistentStoreResult : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreResult ();
	public NSPersistentStoreResult (MonoMac.Foundation.NSCoder coder);
	public NSPersistentStoreResult (MonoMac.Foundation.NSObjectFlag t);
	public NSPersistentStoreResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
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

### Type Changed: MonoMac.CoreFoundation.CFSocket

Added events:

```
public event System.EventHandler<CFSocket.CFSocketDataEventArgs> DataEvent;
	public event System.EventHandler<CFSocket.CFSocketReadEventArgs> ReadEvent;
	public event System.EventHandler<CFSocket.CFSocketWriteEventArgs> WriteEvent;
```

### New Type MonoMac.CoreFoundation.CFSocketDataEventArgs

```
public class CFSocketDataEventArgs : System.EventArgs {
	// constructors
	public CFSocket (System.Net.IPEndPoint remote, byte[] data);
	// properties
	public byte[] Data { get; }
	public System.Net.IPEndPoint RemoteEndPoint { get; }
}
```

### New Type MonoMac.CoreFoundation.CFSocketReadEventArgs

```
public class CFSocketReadEventArgs : System.EventArgs {
	// constructors
	public CFSocket ();
}
```

### New Type MonoMac.CoreFoundation.CFSocketWriteEventArgs

```
public class CFSocketWriteEventArgs : System.EventArgs {
	// constructors
	public CFSocket ();
}
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

### Type Changed: MonoMac.CoreFoundation.CFStream.CFStreamCallback

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr s, CFStreamEventType type, System.IntPtr info, System.AsyncCallback callback, object object);
	public virtual void Invoke (System.IntPtr s, CFStreamEventType type, System.IntPtr info);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr s, int type, System.IntPtr info, System.AsyncCallback callback, object object);
	public virtual void Invoke (System.IntPtr s, int type, System.IntPtr info);
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

### Type Changed: MonoMac.CoreFoundation.DispatchTime

Added property:

```
public DispatchTime WallTime { get; }
```

## Namespace MonoMac.CoreGraphics

### Type Changed: MonoMac.CoreGraphics.CGAffineTransform

Added methods:

```
public static CGAffineTransform Rotate (CGAffineTransform transform, float angle);
	public static CGAffineTransform Scale (CGAffineTransform transform, float sx, float sy);
	public System.Drawing.SizeF TransformSize (System.Drawing.SizeF size);
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

### Type Changed: MonoMac.CoreGraphics.CGVector

Removed method:

```
public override string ToString ();
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

### Type Changed: MonoMac.CoreImage.CIAdditionCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIAffineClamp

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIAffineFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIAffineTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIAffineTransform

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIAutoAdjustmentFilterOptions

Added fields:

```
public bool? AutoAdjustCrop;
	public bool? AutoAdjustLevel;
```

### Type Changed: MonoMac.CoreImage.CIBarsSwipeTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIBlendFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIBlendWithAlphaMask

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIBlendWithMask

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIBloom

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIBumpDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIBumpDistortionLinear

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CICheckerboardGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CICircleSplashDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CICircularScreen

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public float[] Components { get; }
```

### Type Changed: MonoMac.CoreImage.CIColorBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColorBurnBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColorClamp

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorControls

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorCrossPolynomial

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorCube

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorCubeWithColorSpace

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColorDodgeBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColorInvert

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMap

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMatrix

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMonochrome

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorPolynomial

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIColorPosterize

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CICompositingFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIConstantColorGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIContext

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIContextOptions

Added properties:

```
public int? CIImageFormat { get; set; }
	public bool? PriorityRequestLow { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIConvolution3X3

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIConvolution5X5

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIConvolution9Horizontal

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIConvolution9Vertical

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIConvolutionCore

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CICopyMachineTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CICrop

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDarkenBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIDepthOfField

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDetector

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public static MonoMac.Foundation.NSString AspectRatio { get; }
	public static MonoMac.Foundation.NSString FocalLength { get; }
	public static MonoMac.Foundation.NSString TypeQRCode { get; }
	public static MonoMac.Foundation.NSString TypeRectangle { get; }
```

Added methods:

```
public static CIDetector CreateQRDetector (CIContext context, CIDetectorOptions detectorOptions);
	public static CIDetector CreateRectangleDetector (CIContext context, CIDetectorOptions detectorOptions);
```

### Type Changed: MonoMac.CoreImage.CIDetectorOptions

Added properties:

```
public float? AspectRatio { get; set; }
	public float? FocalLength { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDifferenceBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIDisintegrateWithMaskTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIDissolveTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIDistortionFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDotScreen

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIEightfoldReflectedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIExclusionBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIExposureAdjust

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIFaceBalance

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFaceFeature

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFalseColor

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIFeature

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFilter

Added constructor:

```
protected CIFilter ();
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual string Name { get; }
```

Added properties:

```
public CIImage Image { get; set; }
	public virtual string Name { get; set; }
	public CIImage OutputImage { get; }
```

Added methods:

```
public static CIFilter GetFilter (string name, MonoMac.Foundation.NSDictionary inputParameters);
	public virtual MonoMac.ImageKit.IKFilterUIView GetFilterUIView (MonoMac.Foundation.NSDictionary configurationOptions, MonoMac.Foundation.NSArray excludedKeys);
```

### Type Changed: MonoMac.CoreImage.CIFilterGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFilterShape

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFlashTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFourfoldReflectedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFourfoldRotatedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIFourfoldTranslatedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIGammaAdjust

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIGaussianBlur

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIGaussianGradient

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIGlideReflectedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIGloom

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIHardLightBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIHatchedScreen

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIHighlightShadowAdjust

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIHoleDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIHueAdjust

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIHueBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIImage

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual CIImage CreateByClampingToExtent ();
	public virtual CIImage CreateByCompositingOverImage (CIImage dest);
	public virtual CIImage CreateByFiltering (string filterName, MonoMac.Foundation.NSDictionary inputParameters);
	public virtual CIImage CreateWithOrientation (CIImageOrientation orientation);
	public static CIImage FromData (MonoMac.Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, CIFormat pixelFormat, MonoMac.CoreGraphics.CGColorSpace colorSpace);
	public virtual MonoMac.CoreGraphics.CGAffineTransform GetImageTransform (CIImageOrientation orientation);
```

Obsoleted method:

```
[Obsolete ("Use the overload acceping a CIFormat enum (instead of an int) for pixelFormat")]
	public static CIImage FromData (MonoMac.Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, int pixelFormat, MonoMac.CoreGraphics.CGColorSpace colorSpace);
```

### Type Changed: MonoMac.CoreImage.CIImageAccumulator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIImageInitializationOptions

Removed property:

```
public MonoMac.CoreGraphics.CGColorSpace ColorSpace { set; }
```

Added property:

```
public MonoMac.CoreGraphics.CGColorSpace ColorSpace { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIImageInitializationOptionsWithMetadata

Removed property:

```
public MonoMac.CoreGraphics.CGImageProperties Properties { set; }
```

Added property:

```
public MonoMac.CoreGraphics.CGImageProperties Properties { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIKernel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public static CIKernel[] FromProgram (string coreImageShaderProgram);
```

Added methods:

```
[Obsolete ("Use FromProgramSingle")]
	public static CIKernel FromProgram (string coreImageShaderProgram);
	public static CIKernel[] FromProgramMultiple (string coreImageShaderProgram);

	[Obsolete ("Use FromProgramMultiple")]
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
	public static CIKernel FromProgramSingle (string coreImageShaderProgram);
```

### Type Changed: MonoMac.CoreImage.CILanczosScaleTransform

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CILightenBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CILinearGradient

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CILineScreen

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CILuminosityBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIMaskToAlpha

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMaximumComponent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMaximumCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIMinimumComponent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMinimumCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIModTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIMultiplyBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIMultiplyCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIOverlayBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPageCurlTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPerspectiveTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPerspectiveTransform

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffect

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectChrome

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectFade

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectInstant

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectMono

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectNoir

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectProcess

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectTonal

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffectTransfer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPinchDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIPixellate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPlugIn

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIQRCodeGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIRadialGradient

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIRandomGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIRippleTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISampler

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISaturationBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIScreenBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIScreenFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CISepiaTone

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CISharpenLuminance

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CISixfoldReflectedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISixfoldRotatedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISoftLightBlendMode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISourceAtopCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISourceInCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISourceOutCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISourceOverCompositing

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIStarShineGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIStraightenFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIStripesGenerator

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CISwipeTransition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CITemperatureAndTint

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITileFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIToneCurve

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITransitionFilter

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITwelvefoldReflectedTile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CITwirlDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIUnsharpMask

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIVector

Added constructors:

```
public CIVector (MonoMac.CoreGraphics.CGAffineTransform r);
	public CIVector (System.Drawing.RectangleF r);
	public CIVector (System.Drawing.PointF p);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIVibrance

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIVignetteEffect

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIVortexDistortion

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreImage.CIWhitePointAdjust

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public CIImage Image { get; set; }
```

### New Type MonoMac.CoreImage.CIAccordionFoldTransition

```
public class CIAccordionFoldTransition : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAccordionFoldTransition ();
	public CIAccordionFoldTransition (System.IntPtr handle);
	// properties
	public float BottomHeight { get; set; }
	public float FoldShadowAmount { get; set; }
	public int NumberOfFolds { get; set; }
	public CIImage TargetImage { get; set; }
	public float Time { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaAverage

```
public class CIAreaAverage : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaAverage ();
	public CIAreaAverage (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaHistogram

```
public class CIAreaHistogram : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaHistogram ();
	public CIAreaHistogram (System.IntPtr handle);
	// properties
	public float Count { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaMaximum

```
public class CIAreaMaximum : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximum ();
	public CIAreaMaximum (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaMaximumAlpha

```
public class CIAreaMaximumAlpha : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMaximumAlpha ();
	public CIAreaMaximumAlpha (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaMinimum

```
public class CIAreaMinimum : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimum ();
	public CIAreaMinimum (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAreaMinimumAlpha

```
public class CIAreaMinimumAlpha : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAreaMinimumAlpha ();
	public CIAreaMinimumAlpha (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAztecCodeGenerator

```
public class CIAztecCodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIAztecCodeGenerator ();
	public CIAztecCodeGenerator (System.IntPtr handle);
	// properties
	public bool CompactStyle { get; set; }
	public float CorrectionLevel { get; set; }
	public int Layers { get; set; }
	public MonoMac.Foundation.NSData Message { get; set; }
}
```

### New Type MonoMac.CoreImage.CIBoxBlur

```
public class CIBoxBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIBoxBlur ();
	public CIBoxBlur (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CICircularWrap

```
public class CICircularWrap : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CICircularWrap ();
	public CICircularWrap (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CICMYKHalftone

```
public class CICMYKHalftone : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CICMYKHalftone ();
	public CICMYKHalftone (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float GrayComponentReplacement { get; set; }
	public float InputSharpness { get; set; }
	public float UnderColorRemoval { get; set; }
	public float Width { get; set; }
}
```

### New Type MonoMac.CoreImage.CICode128BarcodeGenerator

```
public class CICode128BarcodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CICode128BarcodeGenerator ();
	public CICode128BarcodeGenerator (System.IntPtr handle);
	// properties
	public MonoMac.Foundation.NSData Message { get; set; }
	public float QuietSpace { get; set; }
}
```

### New Type MonoMac.CoreImage.CIColumnAverage

```
public class CIColumnAverage : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIColumnAverage ();
	public CIColumnAverage (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIComicEffect

```
public class CIComicEffect : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIComicEffect ();
	public CIComicEffect (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIConvolution7X7

```
public class CIConvolution7X7 : MonoMac.CoreImage.CIConvolutionCore, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIConvolution7X7 ();
	public CIConvolution7X7 (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CICrystallize

```
public class CICrystallize : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CICrystallize ();
	public CICrystallize (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CIDiscBlur

```
public class CIDiscBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIDiscBlur ();
	public CIDiscBlur (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIDisplacementDistortion

```
public class CIDisplacementDistortion : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIDisplacementDistortion ();
	public CIDisplacementDistortion (System.IntPtr handle);
	// properties
	public float Scale { get; set; }
}
```

### New Type MonoMac.CoreImage.CIDivideBlendMode

```
public class CIDivideBlendMode : MonoMac.CoreImage.CIBlendFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIDivideBlendMode ();
	public CIDivideBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIDroste

```
public class CIDroste : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIDroste ();
	public CIDroste (System.IntPtr handle);
	// properties
	public CIVector InsetPoint0 { get; set; }
	public CIVector InsetPoint1 { get; set; }
	public float Periodicity { get; set; }
	public float Rotation { get; set; }
	public float Strands { get; set; }
	public float Zoom { get; set; }
}
```

### New Type MonoMac.CoreImage.CIEdges

```
public class CIEdges : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIEdges ();
	public CIEdges (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIEdgeWork

```
public class CIEdgeWork : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIEdgeWork ();
	public CIEdgeWork (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIGlassDistortion

```
public class CIGlassDistortion : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIGlassDistortion ();
	public CIGlassDistortion (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Scale { get; set; }
	public CIImage Texture { get; set; }
}
```

### New Type MonoMac.CoreImage.CIGlassLozenge

```
public class CIGlassLozenge : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIGlassLozenge ();
	public CIGlassLozenge (System.IntPtr handle);
	// properties
	public CIVector Point0 { get; set; }
	public CIVector Point1 { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
}
```

### New Type MonoMac.CoreImage.CIHeightFieldFromMask

```
public class CIHeightFieldFromMask : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIHeightFieldFromMask ();
	public CIHeightFieldFromMask (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIHexagonalPixellate

```
public class CIHexagonalPixellate : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIHexagonalPixellate ();
	public CIHexagonalPixellate (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Scale { get; set; }
}
```

### New Type MonoMac.CoreImage.CIHistogramDisplayFilter

```
public class CIHistogramDisplayFilter : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIHistogramDisplayFilter ();
	public CIHistogramDisplayFilter (System.IntPtr handle);
	// properties
	public float Height { get; set; }
	public float HighLimit { get; set; }
	public float LowLimit { get; set; }
}
```

### New Type MonoMac.CoreImage.CIKaleidoscope

```
public class CIKaleidoscope : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIKaleidoscope ();
	public CIKaleidoscope (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Count { get; set; }
}
```

### New Type MonoMac.CoreImage.CILenticularHaloGenerator

```
public class CILenticularHaloGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CILenticularHaloGenerator ();
	public CILenticularHaloGenerator (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float HaloOverlap { get; set; }
	public float HaloRadius { get; set; }
	public float HaloWidth { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float Time { get; set; }
}
```

### New Type MonoMac.CoreImage.CILinearBurnBlendMode

```
public class CILinearBurnBlendMode : MonoMac.CoreImage.CIBlendFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CILinearBurnBlendMode ();
	public CILinearBurnBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CILinearDodgeBlendMode

```
public class CILinearDodgeBlendMode : MonoMac.CoreImage.CIBlendFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CILinearDodgeBlendMode ();
	public CILinearDodgeBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CILinearToSRGBToneCurve

```
public class CILinearToSRGBToneCurve : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CILinearToSRGBToneCurve ();
	public CILinearToSRGBToneCurve (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CILineOverlay

```
public class CILineOverlay : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CILineOverlay ();
	public CILineOverlay (System.IntPtr handle);
	// properties
	public float Contrast { get; set; }
	public float EdgeIntensity { get; set; }
	public float NRNoiseLevel { get; set; }
	public float NRSharpness { get; set; }
	public float Threshold { get; set; }
}
```

### New Type MonoMac.CoreImage.CIMaskedVariableBlur

```
public class CIMaskedVariableBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIMaskedVariableBlur ();
	public CIMaskedVariableBlur (System.IntPtr handle);
	// properties
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CIMedianFilter

```
public class CIMedianFilter : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIMedianFilter ();
	public CIMedianFilter (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIMotionBlur

```
public class CIMotionBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIMotionBlur ();
	public CIMotionBlur (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CINoiseReduction

```
public class CINoiseReduction : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CINoiseReduction ();
	public CINoiseReduction (System.IntPtr handle);
	// properties
	public float NoiseLevel { get; set; }
	public float Sharpness { get; set; }
}
```

### New Type MonoMac.CoreImage.CIOpTile

```
public class CIOpTile : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIOpTile ();
	public CIOpTile (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Scale { get; set; }
	public float Width { get; set; }
}
```

### New Type MonoMac.CoreImage.CIPageCurlWithShadowTransition

```
public class CIPageCurlWithShadowTransition : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIPageCurlWithShadowTransition ();
	public CIPageCurlWithShadowTransition (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIImage BacksideImage { get; set; }
	public CIVector Extent { get; set; }
	public float InputTime { get; set; }
	public float Radius { get; set; }
	public float ShadowAmount { get; set; }
	public CIVector ShadowExtent { get; set; }
	public float ShadowSize { get; set; }
	public CIImage TargetImage { get; set; }
}
```

### New Type MonoMac.CoreImage.CIParallelogramTile

```
public class CIParallelogramTile : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIParallelogramTile ();
	public CIParallelogramTile (System.IntPtr handle);
	// properties
	public float AcuteAngle { get; set; }
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
```

### New Type MonoMac.CoreImage.CIPerspectiveCorrection

```
public class CIPerspectiveCorrection : MonoMac.CoreImage.CIPerspectiveTransform, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIPerspectiveCorrection ();
	public CIPerspectiveCorrection (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIPinLightBlendMode

```
public class CIPinLightBlendMode : MonoMac.CoreImage.CIBlendFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIPinLightBlendMode ();
	public CIPinLightBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIPointillize

```
public class CIPointillize : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIPointillize ();
	public CIPointillize (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CIRectangleFeature

```
public class CIRectangleFeature : MonoMac.CoreImage.CIFeature, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIRectangleFeature ();
	public CIRectangleFeature (MonoMac.Foundation.NSCoder coder);
	public CIRectangleFeature (MonoMac.Foundation.NSObjectFlag t);
	public CIRectangleFeature (System.IntPtr handle);
	// properties
	public virtual System.Drawing.PointF BottomLeft { get; }
	public virtual System.Drawing.PointF BottomRight { get; }
	public virtual System.Drawing.RectangleF Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Drawing.PointF TopLeft { get; }
	public virtual System.Drawing.PointF TopRight { get; }
}
```

### New Type MonoMac.CoreImage.CIRowAverage

```
public class CIRowAverage : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIRowAverage ();
	public CIRowAverage (System.IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
```

### New Type MonoMac.CoreImage.CIShadedMaterial

```
public class CIShadedMaterial : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIShadedMaterial ();
	public CIShadedMaterial (System.IntPtr handle);
	// properties
	public float Scale { get; set; }
	public CIImage ShadingImage { get; set; }
}
```

### New Type MonoMac.CoreImage.CISpotColor

```
public class CISpotColor : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CISpotColor ();
	public CISpotColor (System.IntPtr handle);
	// properties
	public CIColor CenterColor1 { get; set; }
	public CIColor CenterColor2 { get; set; }
	public CIColor CenterColor3 { get; set; }
	public float Closeness1 { get; set; }
	public float Closeness2 { get; set; }
	public float Closeness3 { get; set; }
	public float Contrast1 { get; set; }
	public float Contrast2 { get; set; }
	public float Contrast3 { get; set; }
	public CIColor ReplacementColor1 { get; set; }
	public CIColor ReplacementColor2 { get; set; }
	public CIColor ReplacementColor3 { get; set; }
}
```

### New Type MonoMac.CoreImage.CISpotLight

```
public class CISpotLight : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CISpotLight ();
	public CISpotLight (System.IntPtr handle);
	// properties
	public float Brightness { get; set; }
	public CIColor Color { get; set; }
	public float Concentration { get; set; }
	public CIVector LightPointsAt { get; set; }
	public CIVector LightPosition { get; set; }
}
```

### New Type MonoMac.CoreImage.CISRGBToneCurveToLinear

```
public class CISRGBToneCurveToLinear : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CISRGBToneCurveToLinear ();
	public CISRGBToneCurveToLinear (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIStretchCrop

```
public class CIStretchCrop : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIStretchCrop ();
	public CIStretchCrop (System.IntPtr handle);
	// properties
	public float CenterStretchAmount { get; set; }
	public float CropAmount { get; set; }
	public CIVector Size { get; set; }
}
```

### New Type MonoMac.CoreImage.CISubtractBlendMode

```
public class CISubtractBlendMode : MonoMac.CoreImage.CIBlendFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CISubtractBlendMode ();
	public CISubtractBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CISunbeamsGenerator

```
public class CISunbeamsGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CISunbeamsGenerator ();
	public CISunbeamsGenerator (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIColor Color { get; set; }
	public float CropAmount { get; set; }
	public float MaxStriationRadius { get; set; }
	public float StriationContrast { get; set; }
	public float StriationStrength { get; set; }
	public float SunRadius { get; set; }
	public float Time { get; set; }
}
```

### New Type MonoMac.CoreImage.CITorusLensDistortion

```
public class CITorusLensDistortion : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CITorusLensDistortion ();
	public CITorusLensDistortion (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
	public float Refraction { get; set; }
	public float Width { get; set; }
}
```

### New Type MonoMac.CoreImage.CITriangleTile

```
public class CITriangleTile : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CITriangleTile ();
	public CITriangleTile (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float Width { get; set; }
}
```

### New Type MonoMac.CoreImage.CIVignette

```
public class CIVignette : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIVignette ();
	public CIVignette (System.IntPtr handle);
	// properties
	public float Intensity { get; set; }
	public float Radius { get; set; }
}
```

### New Type MonoMac.CoreImage.CIZoomBlur

```
public class CIZoomBlur : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CIZoomBlur ();
	public CIZoomBlur (System.IntPtr handle);
	// properties
	public float Amount { get; set; }
	public CIVector Center { get; set; }
}
```

## Namespace MonoMac.CoreLocation

### Type Changed: MonoMac.CoreLocation.CLAuthorizationStatus

Added values:

```
AuthorizedAlways = 3,
	AuthorizedWhenInUse = 4,
```

### Type Changed: MonoMac.CoreLocation.CLLocation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreLocation.CLLocationManager

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed event:

```
[Obsolete ("Deprecated in iOS 6.0")]
	[Obsolete ("Deprecated in iOS 6.0")]
	public event System.EventHandler<CLLocationUpdatedEventArgs> UpdatedLocation;
```

Added event:

```
public event System.EventHandler<CLLocationUpdatedEventArgs> UpdatedLocation;
```

### Type Changed: MonoMac.CoreLocation.CLLocationManagerDelegate

Added interfaces:

```
ICLLocationManagerDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.CoreLocation.CLBeaconRegion

```
public class CLBeaconRegion {
	// constructors

	[Obsolete ("Does not return a valid instance on iOS8")]
	public CLBeaconRegion ();
}
```

### New Type MonoMac.CoreLocation.CLHeading

```
public class CLHeading : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CLHeading (MonoMac.Foundation.NSCoder coder);
	public CLHeading (MonoMac.Foundation.NSObjectFlag t);
	public CLHeading (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double HeadingAccuracy { get; }
	public virtual double MagneticHeading { get; }
	public virtual MonoMac.Foundation.NSDate Timestamp { get; }
	public virtual double TrueHeading { get; }
	public virtual double X { get; }
	public virtual double Y { get; }
	public virtual double Z { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual string Description ();
	protected override void Dispose (bool disposing);
}
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
	public static void UpdatedLocation (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
}
```

### New Type MonoMac.CoreLocation.CLPlacemark

```
public class CLPlacemark : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CLPlacemark (MonoMac.Foundation.NSCoder coder);
	public CLPlacemark (MonoMac.Foundation.NSObjectFlag t);
	public CLPlacemark (System.IntPtr handle);
	public CLPlacemark (CLPlacemark placemark);
	// properties
	public virtual MonoMac.Foundation.NSDictionary AddressDictionary { get; }
	public virtual string AdministrativeArea { get; }
	public virtual string[] AreasOfInterest { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Country { get; }
	public virtual string InlandWater { get; }
	public virtual string IsoCountryCode { get; }
	public virtual string Locality { get; }
	public virtual CLLocation Location { get; }
	public virtual string Name { get; }
	public virtual string Ocean { get; }
	public virtual string PostalCode { get; }
	public virtual CLRegion Region { get; }
	public virtual string SubAdministrativeArea { get; }
	public virtual string SubLocality { get; }
	public virtual string SubThoroughfare { get; }
	public virtual string Thoroughfare { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreLocation.CLRegion

```
public class CLRegion : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public CLRegion (MonoMac.Foundation.NSCoder coder);
	public CLRegion (MonoMac.Foundation.NSObjectFlag t);
	public CLRegion (System.IntPtr handle);
	public CLRegion (CLLocationCoordinate2D center, double radius, string identifier);
	// properties
	public virtual CLLocationCoordinate2D Center { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual bool NotifyOnEntry { get; set; }
	public virtual bool NotifyOnExit { get; set; }
	public virtual double Radius { get; }
	// methods
	public virtual bool Contains (CLLocationCoordinate2D coordinate);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
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

### Type Changed: MonoMac.CoreMedia.CMFormatDescription

Added methods:

```
public static CMFormatDescription Create (System.IntPtr handle);
	public MonoMac.Foundation.NSObject GetExtension (string extensionKey);
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

### Type Changed: MonoMac.CoreMedia.CMSampleBuffer

Added methods:

```
public CMSampleBufferError CallForEachSample (System.Func<CMSampleBuffer,System.Int32,MonoMac.CoreMedia.CMSampleBufferError> callback);
	public static CMSampleBuffer CreateReady (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMSampleTimingInfo[] sampleTimingArray, uint[] sampleSizeArray, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithImageBuffer (MonoMac.CoreVideo.CVImageBuffer imageBuffer, CMFormatDescription formatDescription, CMSampleTimingInfo[] sampleTiming, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, MonoMac.AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
	public CMSampleBufferError SetInvalidateCallback (System.Action<CMSampleBuffer> invalidateHandler);
```

### Type Changed: MonoMac.CoreMedia.CMTime

Added properties:

```
public bool HasBeenRounded { get; }
	public bool IsNumeric { get; }
```

Obsoleted property:

```
[Obsolete ("Use ToDictionary instead")]
	public System.IntPtr AsDictionary { get; }
```

Added methods:

```
public static CMTime FromDictionary (MonoMac.Foundation.NSDictionary dict);
	public static CMTime Multiply (CMTime time, int multiplier, int divisor);
	public static bool op_GreaterThan (CMTime time1, CMTime time2);
	public static bool op_GreaterThanOrEqual (CMTime time1, CMTime time2);
	public static bool op_LessThan (CMTime time1, CMTime time2);
	public static bool op_LessThanOrEqual (CMTime time1, CMTime time2);
	public MonoMac.Foundation.NSDictionary ToDictionary ();
```

Obsoleted method:

```
[Obsolete ("Use FromDictionary (NSDictionary) instead")]
	public static CMTime FromDictionary (System.IntPtr dict);
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

Added methods:

```
protected override void ~MidiPacket ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
```

### Type Changed: MonoMac.CoreMidi.MidiPacketsEventArgs

Added interface:

```
System.IDisposable
```

Added methods:

```
protected override void ~MidiPacketsEventArgs ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
```

## Namespace MonoMac.CoreServices

### Type Changed: MonoMac.CoreServices.CFHTTPStream

Added method:

```
public void SetProxy (MonoMac.CoreFoundation.CFProxySettings proxySettings);
```

## Namespace MonoMac.CoreText

### Type Changed: MonoMac.CoreText.CTFontFeatureKey

Removed fields:

```
public static MonoMac.Foundation.NSString Exclusive;
	public static MonoMac.Foundation.NSString Identifier;
	public static MonoMac.Foundation.NSString Name;
	public static MonoMac.Foundation.NSString Selectors;
```

Added properties:

```
public static MonoMac.Foundation.NSString Exclusive { get; }
	public static MonoMac.Foundation.NSString Identifier { get; }
	public static MonoMac.Foundation.NSString Name { get; }
	public static MonoMac.Foundation.NSString Selectors { get; }
```

### Type Changed: MonoMac.CoreText.CTFontFeatureSelectorKey

Removed fields:

```
public static MonoMac.Foundation.NSString Default;
	public static MonoMac.Foundation.NSString Identifier;
	public static MonoMac.Foundation.NSString Name;
	public static MonoMac.Foundation.NSString Setting;
```

Added properties:

```
public static MonoMac.Foundation.NSString Default { get; }
	public static MonoMac.Foundation.NSString Identifier { get; }
	public static MonoMac.Foundation.NSString Name { get; }
	public static MonoMac.Foundation.NSString Setting { get; }
```

### Type Changed: MonoMac.CoreText.CTFontVariationAxisKey

Removed fields:

```
public static MonoMac.Foundation.NSString DefaultValue;
	public static MonoMac.Foundation.NSString Identifier;
	public static MonoMac.Foundation.NSString MaximumValue;
	public static MonoMac.Foundation.NSString MinimumValue;
	public static MonoMac.Foundation.NSString Name;
```

Added properties:

```
public static MonoMac.Foundation.NSString DefaultValue { get; }
	public static MonoMac.Foundation.NSString Identifier { get; }
	public static MonoMac.Foundation.NSString MaximumValue { get; }
	public static MonoMac.Foundation.NSString MinimumValue { get; }
	public static MonoMac.Foundation.NSString Name { get; }
```

### Type Changed: MonoMac.CoreText.CTLineBoundsOptions

Added value:

```
IncludeLanguageExtents = 32,
```

### Type Changed: MonoMac.CoreText.CTParagraphStyleSettings

Added property:

```
public CTLineBoundsOptions? LineBoundsOptions { get; set; }
```

## Namespace MonoMac.CoreVideo

### Type Changed: MonoMac.CoreVideo.CVImageBuffer

Added field:

```
public static MonoMac.Foundation.NSString AlphaChannelIsOpaque;
```

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

Added field:

```
public static MonoMac.Foundation.NSString MetalCompatibilityKey;
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

Removed property:

```
public MonoMac.CoreFoundation.CFAllocator MemoryAllocator { set; }
```

Added properties:

```
public bool? AllocateWithIOSurface { get; set; }
	public MonoMac.CoreFoundation.CFAllocator MemoryAllocator { get; set; }
	public bool? MetalCompatibility { get; set; }
```

### Type Changed: MonoMac.CoreVideo.CVPixelFormatDescription

Added fields:

```
public static MonoMac.Foundation.NSString ContainsRgb;
	public static MonoMac.Foundation.NSString ContainsYCbCr;
```

### Type Changed: MonoMac.CoreVideo.CVReturn

Added value:

```
PixelBufferNotMetalCompatible = -6684,
```

## Namespace MonoMac.CoreWlan

### Type Changed: MonoMac.CoreWlan.CW8021XProfile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreWlan.CWChannel

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual uint ChannelNumber { get; }
```

Added property:

```
public virtual int ChannelNumber { get; }
```

### Type Changed: MonoMac.CoreWlan.CWConfiguration

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreWlan.CWInterface

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual uint TransmitPower { get; }
```

Added property:

```
public virtual int TransmitPower { get; }
```

Removed method:

```
public virtual bool SetWEPKey (MonoMac.Foundation.NSData key, CWCipherKeyFlags flags, uint index, out MonoMac.Foundation.NSError error);
```

Added method:

```
public virtual bool SetWEPKey (MonoMac.Foundation.NSData key, CWCipherKeyFlags flags, int index, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreWlan.CWMutableConfiguration

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreWlan.CWMutableNetworkProfile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreWlan.CWNetwork

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual uint BeaconInterval { get; }
```

Added property:

```
public virtual int BeaconInterval { get; }
```

### Type Changed: MonoMac.CoreWlan.CWNetworkProfile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.CoreWlan.CWWirelessProfile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

## Namespace MonoMac.Foundation

### Type Changed: MonoMac.Foundation.DictionaryContainer

Added methods:

```
protected T GetNativeValue<T> (NSString key);
	protected int? GetNIntValue (NSString key);
	protected uint? GetNUIntValue (NSString key);
	protected T GetStrongDictionary<T> (NSString key);
	protected uint? GetUInt32Value (NSString key);
	protected void SetArrayValue<T> (NSString key, T[] values);
```

### Type Changed: MonoMac.Foundation.ExportAttribute

Obsoleted constructor:

```
[Obsolete ("Every exported selector must include a name")]
	public ExportAttribute ();
```

### Type Changed: MonoMac.Foundation.INSMachPortDelegate

Added interface:

```
INSPortDelegate
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

### Type Changed: MonoMac.Foundation.INSUrlConnectionDownloadDelegate

Added interface:

```
INSUrlConnectionDelegate
```

### Type Changed: MonoMac.Foundation.NSAffineTransform

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSAppleEventDescriptor

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSAppleEventManager

Added interface:

```
INSObjectProtocol
```

Added method:

```
public void RemoveEventHandler (AEEventClass eventClass, AEEventID eventID);
```

Obsoleted method:

```
[Obsolete ("Use RemoveEventHandler instead")]
	public virtual void RemoveEventHandlerForEventClassandEventID (AEEventClass eventClass, AEEventID eventID);
```

### Type Changed: MonoMac.Foundation.NSArray

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSAttributedString

Added interfaces:

```
MonoMac.AppKit.INSPasteboardReading
	MonoMac.AppKit.INSPasteboardWriting
	INSSecureCoding
	INSObjectProtocol
```

Added methods:

```
public virtual System.Drawing.RectangleF BoundingRectWithSize (System.Drawing.SizeF size, NSStringDrawingOptions options);
	public virtual NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public static MonoMac.AppKit.NSPasteboardReadingOptions GetReadingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual MonoMac.AppKit.NSPasteboardWritingOptions GetWritingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual NSObject InitWithPasteboardPropertyList (NSObject propertyList, string type);
```

### Type Changed: MonoMac.Foundation.NSAutoreleasePool

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSBlockOperation

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSBundle

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, string localizationName);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension);
	public static NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, NSUrl bundleURL);
	public static NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, NSUrl bundleURL);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, string localizationName);
```

### Type Changed: MonoMac.Foundation.NSByteCountFormatter

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual NSFormattingContext FormattingContext { get; set; }
```

### Type Changed: MonoMac.Foundation.NSCache

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCacheDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCachedUrlResponse

Added interfaces:

```
INSSecureCoding
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCalendar

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual string AMSymbol { get; }
	public static NSString DayChangedNotification { get; }
	public virtual string[] EraSymbols { get; }
	public virtual string[] LongEraSymbols { get; }
	public virtual string[] MonthSymbols { get; }
	public virtual string PMSymbol { get; }
	public virtual string[] QuarterSymbols { get; }
	public virtual string[] ShortMonthSymbols { get; }
	public virtual string[] ShortQuarterSymbols { get; }
	public virtual string[] ShortStandaloneMonthSymbols { get; }
	public virtual string[] ShortStandaloneQuarterSymbols { get; }
	public virtual string[] ShortStandaloneWeekdaySymbols { get; }
	public virtual string[] ShortWeekdaySymbols { get; }
	public virtual string[] StandaloneMonthSymbols { get; }
	public virtual string[] StandaloneQuarterSymbols { get; }
	public virtual string[] StandaloneWeekdaySymbols { get; }
	public virtual string[] VeryShortMonthSymbols { get; }
	public virtual string[] VeryShortStandaloneMonthSymbols { get; }
	public virtual string[] VeryShortStandaloneWeekdaySymbols { get; }
	public virtual string[] VeryShortWeekdaySymbols { get; }
	public virtual string[] WeekdaySymbols { get; }
```

Added methods:

```
public virtual NSComparisonResult CompareDate (NSDate date1, NSDate date2, NSCalendarUnit granularity);
	public virtual NSDateComponents ComponentsFromDateToDate (NSCalendarUnit unitFlags, NSDateComponents startingDate, NSDateComponents resultDate, NSCalendarOptions options);
	public virtual NSDateComponents ComponentsInTimeZone (NSTimeZone timezone, NSDate date);
	public virtual NSDate Date (int era, int year, int month, int date, int hour, int minute, int second, int nanosecond);
	public virtual NSDate DateByAddingUnit (NSCalendarUnit unit, int value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingsHour (int hour, int minute, int second, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingUnit (NSCalendarUnit unit, int value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateForWeekOfYear (int era, int year, int week, int weekday, int hour, int minute, int second, int nanosecond);
	public virtual void EnumerateDatesStartingAfterDate (NSDate start, NSDateComponents matchingComponents, NSCalendarOptions options, EnumerateDatesCallback callback);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSDateComponents components, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSCalendarUnit unit, int value, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, int hour, int minute, int second, NSCalendarOptions options);
	public virtual bool FindNextWeekend (out NSDate date, out double interval, NSCalendarOptions options, NSDate afterDate);
	public virtual int GetComponentFromDate (NSCalendarUnit unit, NSDate date);
	public virtual void GetComponentsFromDate (out int era, out int year, out int month, out int day, NSDate date);
	public virtual void GetComponentsFromDateForWeekOfYear (out int era, out int year, out int weekOfYear, out int weekday, NSDate date);
	public virtual void GetHourComponentsFromDate (out int hour, out int minute, out int second, out int nanosecond, NSDate date);
	public virtual bool IsDateInToday (NSDate date);
	public virtual bool IsDateInTomorrow (NSDate date);
	public virtual bool IsDateInWeekend (NSDate date);
	public virtual bool IsDateInYesterday (NSDate date);
	public virtual bool IsEqualToUnitGranularity (NSDate date1, NSDate date2, NSCalendarUnit unit);
	public virtual bool IsInSameDay (NSDate date1, NSDate date2);
	public virtual bool Matches (NSDate date, NSDateComponents components);
	public virtual bool RangeOfWeekendContainingDate (out NSDate weekendStartDate, out double interval, NSDate date);
	public virtual NSDate StartOfDayForDate (NSDate date);
```

### Type Changed: MonoMac.Foundation.NSCalendarType

Added values:

```
Coptic = 11,
	EthiopicAmeteAlem = 12,
	EthiopicAmeteMihret = 13,
	IslamicTabular = 14,
	IslamicUmmAlQura = 15,
```

### Type Changed: MonoMac.Foundation.NSCalendarUnit

Added value:

```
Nanosecond = 32768,
```

### Type Changed: MonoMac.Foundation.NSCharacterSet

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCoder

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCoding

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSComparisonPredicate

Added interface:

```
INSObjectProtocol
```

Removed methods:

```
public static NSPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoMac.ObjCRuntime.Selector selector);
```

Added methods:

```
public static NSComparisonPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSComparisonPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoMac.ObjCRuntime.Selector selector);
```

### Type Changed: MonoMac.Foundation.NSCompoundPredicate

Added interface:

```
INSObjectProtocol
```

Removed methods:

```
public static NSPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

Added methods:

```
public static NSCompoundPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSCompoundPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSCompoundPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

### Type Changed: MonoMac.Foundation.NSConnection

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSConnectionDelegate

Added interfaces:

```
INSConnectionDelegate
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSCopying

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSData

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual bool Save (string path, bool atomically);
	public bool Save (NSUrl url, NSDataWritingOptions options, out NSError error);
	public virtual bool Save (NSUrl url, bool atomically);
	public byte[] ToArray ();
```

### Type Changed: MonoMac.Foundation.NSDate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSDateComponents

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual bool IsValidDate { get; }
	public virtual int Nanosecond { get; set; }
```

Added methods:

```
public virtual int GetValueForComponent (NSCalendarUnit unit);
	public virtual bool IsValidDateInCalendar (NSCalendar calendar);
	public virtual void SetValueForComponent (int value, NSCalendarUnit unit);
```

### Type Changed: MonoMac.Foundation.NSDateFormatter

Added interface:

```
INSObjectProtocol
```

Added method:

```
public virtual void SetLocalizedDateFormatFromTemplate (string dateFormatTemplate);
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

Added interfaces:

```
System.IEquatable<NSNumber>
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSDictionary

Added interface:

```
INSObjectProtocol
```

Added method:

```
public NSFileAttributes ToFileAttributes ();
```

### Type Changed: MonoMac.Foundation.NSDirectoryEnumerator

Added interfaces:

```
System.Collections.Generic.IEnumerator<NSString>
	System.Collections.Generic.IEnumerator<string>
	System.Collections.IEnumerator
	INSObjectProtocol
```

Removed methods:

```
public virtual NSDate FileCreationDate (NSDictionary fileAttributes);
	public virtual bool FileExtensionHidden (NSDictionary fileAttributes);
	public virtual NSNumber FileGroupOwnerAccountID (NSDictionary fileAttributes);
	public virtual string FileGroupOwnerAccountName (NSDictionary fileAttributes);
	public virtual uint FileHfsCreatorCode (NSDictionary fileAttributes);
	public virtual uint FileHfsTypeCode (NSDictionary fileAttributes);
	public virtual bool FileIsAppendOnly (NSDictionary fileAttributes);
	public virtual bool FileIsImmutable (NSDictionary fileAttributes);
	public virtual NSDate FileModificationDate (NSDictionary fileAttributes);
	public virtual NSNumber FileOwnerAccountID (NSDictionary fileAttributes);
	public virtual string FileOwnerAccountName (NSDictionary fileAttributes);
	public virtual uint FilePosixPermissions (NSDictionary fileAttributes);
	public virtual uint FileSystemFileNumber (NSDictionary fileAttributes);
	public virtual int FileSystemNumber (NSDictionary fileAttributes);
	public virtual string FileType (NSDictionary fileAttributes);
```

Added methods:

```
[Obsolete ("Use ToFileAttributes ().CreationDate instead")]
	public NSDate FileCreationDate (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().ExtensionHidden instead")]
	public bool FileExtensionHidden (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().GroupOwnerAccountID instead")]
	public NSNumber FileGroupOwnerAccountID (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().GroupOwnerAccountName instead")]
	public string FileGroupOwnerAccountName (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().HfsCreatorCode instead")]
	public uint FileHfsCreatorCode (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().HfsTypeCode instead")]
	public uint FileHfsTypeCode (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().IsAppendOnly instead")]
	public bool FileIsAppendOnly (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().IsImmutable instead")]
	public bool FileIsImmutable (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().ModificationDate instead")]
	public NSDate FileModificationDate (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().OwnerAccountID instead")]
	public NSNumber FileOwnerAccountID (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().OwnerAccountName instead")]
	public string FileOwnerAccountName (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().PosixPermissions instead")]
	public uint FilePosixPermissions (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().SystemFileNumber instead")]
	public uint FileSystemFileNumber (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().SystemNumber instead")]
	public int FileSystemNumber (NSDictionary fileAttributes);

	[Obsolete ("Use ToFileAttributes ().Type instead")]
	public string FileType (NSDictionary fileAttributes);
```

### Type Changed: MonoMac.Foundation.NSDistantObjectRequest

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSDistributedNotificationCenter

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSEnumerator

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSError

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public static NSString CoreLocationErrorDomain { get; }
	public virtual string HelpAnchor { get; }
	public virtual string LocalizedFailureReason { get; }
	public virtual string[] LocalizedRecoveryOptions { get; }
	public virtual string LocalizedRecoverySuggestion { get; }
	public static NSString NSNetServicesErrorDomain { get; }
	public static NSString NSStreamSocketSSLErrorDomain { get; }
	public static NSString NSStreamSOCKSErrorDomain { get; }
```

### Type Changed: MonoMac.Foundation.NSException

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSExpression

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSFileAttributes

Added properties:

```
public bool? ExtensionHidden { get; set; }
	public uint? GroupOwnerAccountID { get; set; }
	public string GroupOwnerAccountName { get; set; }
	public uint? HfsCreatorCode { get; set; }
	public uint? OwnerAccountID { get; set; }
	public uint? ReferenceCount { get; set; }
	public ulong? Size { get; set; }
	public uint? SystemFileNumber { get; set; }
	public int? SystemNumber { get; set; }
	public NSFileType? Type { get; set; }
```

Obsoleted properties:

```
[Obsolete ("Use ExtensionHidden instead")]
	public bool? FileExtensionHidden { get; set; }

	[Obsolete ("Use GroupOwnerAccountID instead")]
	public uint? FileGroupOwnerAccountID { get; set; }

	[Obsolete ("Use GroupOwnerAccountID instead")]
	public uint? FileOwnerAccountID { get; set; }

	[Obsolete ("Use ReferenceCount instead")]
	public uint? FileReferenceCount { get; set; }

	[Obsolete ("Use Size instead")]
	public ulong? FileSize { get; set; }

	[Obsolete ("Use SystemFileNumber instead")]
	public uint? FileSystemFileNumber { get; set; }

	[Obsolete ("Use Type instead")]
	public NSFileType? FileType { get; set; }
```

Added method:

```
public static NSFileAttributes FromDictionary (NSDictionary dict);
```

Obsoleted method:

```
[Obsolete ("Use FromDictionary instead")]
	public static NSFileAttributes FromDict (NSDictionary dict);
```

### Type Changed: MonoMac.Foundation.NSFileCoordinator

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual string PurposeIdentifier { get; set; }
```

Added method:

```
public virtual void CoordinateAccess (NSFileAccessIntent[] intents, NSOperationQueue executionQueue, System.Action<NSError> accessor);
```

### Type Changed: MonoMac.Foundation.NSFileCoordinatorReadingOptions

Added values:

```
ForUploading = 8,
	ImmediatelyAvailableMetadataOnly = 4,
	ResolvesSymbolicLink = 2,
```

### Type Changed: MonoMac.Foundation.NSFileHandle

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSFileManager

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
```

### Type Changed: MonoMac.Foundation.NSFileManagerDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSFilePresenter

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual void AccommodatePresentedItemDeletion (System.Action<NSError> completionHandler);
	public virtual void AccommodatePresentedSubitemDeletion (NSUrl url, System.Action<NSError> completionHandler);
	public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
	public virtual void SavePresentedItemChanges (System.Action<NSError> completionHandler);
```

### Type Changed: MonoMac.Foundation.NSFilePresenter_Extensions

Added methods:

```
public static void AccommodatePresentedItemDeletion (INSFilePresenter This, System.Action<NSError> completionHandler);
	public static void AccommodatePresentedSubitemDeletion (INSFilePresenter This, NSUrl url, System.Action<NSError> completionHandler);
	public static NSOperationQueue GetPesentedItemOperationQueue (INSFilePresenter This);
	public static NSUrl GetPrimaryPresentedItemUrl (INSFilePresenter This);
	public static void RelinquishPresentedItemToReader (INSFilePresenter This, NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, NSFilePresenterReacquirer writerAction);
	public static void SavePresentedItemChanges (INSFilePresenter This, System.Action<NSError> completionHandler);
```

### Type Changed: MonoMac.Foundation.NSFileVersion

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSFileWrapper

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSFormatter

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSHost

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSHttpCookie

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSHttpCookieStorage

Added interface:

```
INSObjectProtocol
```

Added method:

```
public virtual void RemoveCookiesSinceDate (NSDate date);
```

### Type Changed: MonoMac.Foundation.NSHttpUrlResponse

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSIndexPath

Added interfaces:

```
INSSecureCoding
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSIndexSet

Added interfaces:

```
INSSecureCoding
	INSObjectProtocol
```

Added methods:

```
public virtual void EnumerateIndexes (NSRange range, NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (EnumerateIndexSetCallback enumeratorCallback);
```

### Type Changed: MonoMac.Foundation.NSInputStream

Added interface:

```
INSObjectProtocol
```

Added method:

```
public int Read (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoMac.Foundation.NSInvocation

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSJsonSerialization

Added interface:

```
INSObjectProtocol
```

Added method:

```
public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, out NSError error);
```

Obsoleted method:

```
[Obsolete ("Use the Deserialize(NSData,NSJsonReadingOptions,out NSError) overload instead")]
	public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, NSError error);
```

### Type Changed: MonoMac.Foundation.NSKeyedArchiver

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSKeyedArchiverDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSKeyedUnarchiver

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSKeyedUnarchiverDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSLinguisticTagger

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSLocale

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMachPort

Added constructors:

```
public NSMachPort (uint machPort);
	public NSMachPort (uint machPort, NSMachPortRights options);
```

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMachPortDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMetadataItem

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public NSString DisplayName { get; }
	public NSItemDownloadingStatus DownloadingStatus { get; }
	public NSDate FileSystemContentChangeDate { get; }
	public NSDate FileSystemCreationDate { get; }
	public NSString FileSystemName { get; }
	public NSNumber FileSystemSize { get; }
	public bool IsUbiquitous { get; }
	public NSString Path { get; }
	public NSError UbiquitousItemDownloadingError { get; }
	public bool UbiquitousItemHasUnresolvedConflicts { get; }
	public bool UbiquitousItemIsDownloading { get; }
	public bool UbiquitousItemIsUploaded { get; }
	public bool UbiquitousItemIsUploading { get; }
	public double UbiquitousItemPercentDownloaded { get; }
	public double UbiquitousItemPercentUploaded { get; }
	public NSError UbiquitousItemUploadingError { get; }
	public NSUrl Url { get; }
```

### Type Changed: MonoMac.Foundation.NSMetadataQuery

Added interface:

```
INSObjectProtocol
```

Removed property:

```
public virtual NSMetadataQueryDelegate WeakDelegate { get; set; }
```

Added properties:

```
public static NSString AccessibleUbiquitousExternalDocumentsScope { get; }
	public static NSString ContentTypeKey { get; }
	public static NSString ContentTypeTreeKey { get; }
	public static NSString LocalDocumentsScope { get; }
	public static NSString NetworkScope { get; }
	public static NSString UbiquitousDataScope { get; }
	public static NSString UbiquitousDocumentsScope { get; }
	public static NSString UbiquitousItemContainerDisplayNameKey { get; }
	public static NSString UbiquitousItemDownloadingErrorKey { get; }
	public static NSString UbiquitousItemDownloadingStatusKey { get; }
	public static NSString UbiquitousItemDownloadRequestedKey { get; }
	public static NSString UbiquitousItemIsExternalDocumentKey { get; }
	public static NSString UbiquitousItemUploadingErrorKey { get; }
	public static NSString UbiquitousItemURLInLocalContainerKey { get; }
	public virtual NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoMac.Foundation.NSMetadataQueryAttributeValueTuple

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMetadataQueryDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMetadataQueryResultGroup

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMethodSignature

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual System.IntPtr MethodReturnType { get; }
```

Added methods:

```
public static NSMethodSignature FromObjcTypes (System.IntPtr utf8objctypes);
	public virtual System.IntPtr GetArgumentType (uint index);
```

### Type Changed: MonoMac.Foundation.NSMutableArray

Added constructor:

```
public NSMutableArray (uint capacity);
```

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public static NSMutableArray FromFile (string path);
	public static NSMutableArray FromUrl (NSUrl url);
```

### Type Changed: MonoMac.Foundation.NSMutableAttributedString

Added interfaces:

```
MonoMac.AppKit.INSPasteboardReading
	MonoMac.AppKit.INSPasteboardWriting
	INSSecureCoding
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableCharacterSet

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableCopying

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableData

Added interface:

```
INSObjectProtocol
```

Obsoleted method:

```
[Obsolete ("Use the Length property setter")]
	public virtual void SetLength (uint len);
```

### Type Changed: MonoMac.Foundation.NSMutableDictionary

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableIndexSet

Added interfaces:

```
INSSecureCoding
	INSObjectProtocol
```

Added methods:

```
public virtual void AddIndexesInRange (NSRange range);
	public virtual void RemoveIndexesInRange (NSRange range);
```

### Type Changed: MonoMac.Foundation.NSMutableOrderedSet

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableSet

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableString

Added interfaces:

```
MonoMac.AppKit.INSPasteboardReading
	MonoMac.AppKit.INSPasteboardWriting
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSMutableUrlRequest

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNetService

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual bool IncludesPeerToPeer { get; set; }
```

### Type Changed: MonoMac.Foundation.NSNetServiceBrowser

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual bool IncludesPeerToPeer { get; set; }
```

### Type Changed: MonoMac.Foundation.NSNetServiceBrowserDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNetServiceDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNotification

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNotificationCenter

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNotificationQueue

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNull

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSNumber

Added interfaces:

```
System.IEquatable<NSNumber>
	INSObjectProtocol
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

### Type Changed: MonoMac.Foundation.NSNumberFormatter

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSObject

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.ObjCRuntime.Class Class { get; }
	public virtual bool IsProxy { get; }
	public virtual NSObject Self { get; }
	public virtual MonoMac.ObjCRuntime.Class Superclass { get; }
	public virtual NSZone Zone { get; }
```

Removed methods:

```
public NSObject DangerousAutorelease ();
	public void DangerousRelease ();
	public NSObject DangerousRetain ();
	public virtual void PerformSelector (MonoMac.ObjCRuntime.Selector sel, NSObject obj, double delay);
```

Added methods:

```
public System.IDisposable AddObserver (string key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public System.IDisposable AddObserver (NSString key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public void AddObserver (NSObject observer, string keyPath, NSKeyValueObservingOptions options, System.IntPtr context);
	public virtual NSObject DangerousAutorelease ();
	public virtual void DangerousRelease ();
	public virtual NSObject DangerousRetain ();
	public virtual uint GetNativeHash ();
	public virtual bool IsEqual (NSObject anObject);
	public virtual bool IsKindOfClass (MonoMac.ObjCRuntime.Class aClass);
	public virtual bool IsMemberOfClass (MonoMac.ObjCRuntime.Class aClass);
	public static bool IsNewRefcountEnabled ();
	protected void MarkDirty ();
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector, NSObject anObject);
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector);
	public virtual void PerformSelector (MonoMac.ObjCRuntime.Selector selector, NSObject withObject, double delay);
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector, NSObject object1, NSObject object2);
	public void RemoveObserver (NSObject observer, string keyPath);
	public void RemoveObserver (NSObject observer, string keyPath, System.IntPtr context);
	public virtual void RemoveObserver (NSObject observer, NSString keyPath, System.IntPtr context);
```

### Type Changed: MonoMac.Foundation.NSOperation

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual bool Asynchronous { get; }
	public virtual string Name { get; set; }
	public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoMac.Foundation.NSOperationQueue

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual NSQualityOfService QualityOfService { get; set; }
	public virtual MonoMac.CoreFoundation.DispatchQueue UnderlyingQueue { get; set; }
```

### Type Changed: MonoMac.Foundation.NSOrderedSet

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSOrthography

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSOutputStream

Added interface:

```
INSObjectProtocol
```

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

### Type Changed: MonoMac.Foundation.NSPipe

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPort

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual bool SendBeforeDate (NSDate limitDate, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
	public virtual bool SendBeforeDate (NSDate limitDate, uint msgID, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
```

### Type Changed: MonoMac.Foundation.NSPortDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPortMessage

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPortNameServer

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPredicate

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public static NSPredicate FromFormat (string predicateFormat, NSObject argument);
	public static NSPredicate FromFormat (string predicateFormat);
```

### Type Changed: MonoMac.Foundation.NSProcessInfo

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual NSOperatingSystemVersion OperatingSystemVersion { get; }
```

Added method:

```
public virtual bool IsOperatingSystemAtLeastVersion (NSOperatingSystemVersion version);
```

### Type Changed: MonoMac.Foundation.NSProgress

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPropertyListSerialization

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSPurgeableData

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSRunLoop

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSSet

Added interface:

```
INSObjectProtocol
```

Added method:

```
public virtual NSObject LookupMember (NSObject probe);
```

### Type Changed: MonoMac.Foundation.NSSortDescriptor

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSStream

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public NSData DataWrittenToMemoryStream { get; }
	public NSNumber FileCurrentOffset { get; }
	public NSStreamServiceType ServiceType { get; set; }
	public NSStreamSocketSecurityLevel SocketSecurityLevel { get; set; }
	public NSStreamSocksOptions SocksOptions { get; set; }
```

Added methods:

```
public static void GetBoundStreams (uint bufferSize, out NSInputStream inputStream, out NSOutputStream outputStream);
	public static void GetStreamsToHost (string hostname, int port, out NSInputStream inputStream, out NSOutputStream outputStream);
```

### Type Changed: MonoMac.Foundation.NSStreamDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSString

Added interfaces:

```
MonoMac.AppKit.INSPasteboardReading
	MonoMac.AppKit.INSPasteboardWriting
	INSObjectProtocol
```

Added field:

```
public static NSString Empty;
```

Added methods:

```
public virtual bool Contains (NSString str);
	public static uint DetectStringEncoding (NSData rawData, EncodingDetectionOptions options, out string convertedString, out bool usedLossyConversion);
	public static uint DetectStringEncoding (NSData rawData, NSDictionary options, out string convertedString, out bool usedLossyConversion);
	public virtual void GetLineStart (out uint startPtr, out uint lineEndPtr, out uint contentsEndPtr, NSRange range);
	public virtual NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public static MonoMac.AppKit.NSPasteboardReadingOptions GetReadingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual MonoMac.AppKit.NSPasteboardWritingOptions GetWritingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual NSObject InitWithPasteboardPropertyList (NSObject propertyList, string type);
	public virtual NSRange LineRangeForRange (NSRange range);
	public virtual bool LocalizedCaseInsensitiveContains (NSString str);
```

### Type Changed: MonoMac.Foundation.NSTask

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSTextCheckingResult

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSThread

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoMac.Foundation.NSTimer

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSTimeZone

Added interface:

```
INSObjectProtocol
```

Added property:

```
public static NSDictionary Abbreviations { get; }
```

Added methods:

```
public virtual string Abbreviation ();
	public virtual string GetLocalizedName (NSTimeZoneNameStyle style, NSLocale locale);
```

### Type Changed: MonoMac.Foundation.NSUbiquitousKeyValueStore

Added interface:

```
INSObjectProtocol
```

Added method:

```
public NSDictionary ToDictionary ();
```

Obsoleted method:

```
[Obsolete ("Use ToDictionary instead")]
	public virtual NSDictionary DictionaryRepresentation ();
```

### Type Changed: MonoMac.Foundation.NSUndoManager

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrl

Removed constructors:

```
public NSUrl (string path, NSUrl relativeToUrl);
	public NSUrl (string path);
```

Added constructors:

```
public NSUrl (string urlString, NSUrl relativeToUrl);
	public NSUrl (string urlString);
```

Added interfaces:

```
MonoMac.AppKit.INSPasteboardReading
	MonoMac.AppKit.INSPasteboardWriting
	System.IEquatable<NSUrl>
	INSObjectProtocol
```

Added properties:

```
public static NSString AddedToDirectoryDateKey { get; }
	public static NSString DocumentIdentifierKey { get; }
	public static NSString GenerationIdentifierKey { get; }
	public virtual string LastPathComponent { get; }
	public virtual string[] PathComponents { get; }
	public static NSString ThumbnailDictionaryKey { get; }
	public static NSString UbiquitousItemContainerDisplayNameKey { get; }
	public static NSString UbiquitousItemDownloadRequestedKey { get; }
```

Added methods:

```
public virtual NSUrl AppendPathExtension (string extension);
	public static NSUrl CreateFileUrl (string[] pathComponents);
	public virtual bool Equals (NSUrl url);
	public virtual NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public static MonoMac.AppKit.NSPasteboardReadingOptions GetReadingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual MonoMac.AppKit.NSPasteboardWritingOptions GetWritingOptionsForType (string type, MonoMac.AppKit.NSPasteboard pasteboard);
	public virtual NSObject InitWithPasteboardPropertyList (NSObject propertyList, string type);
	public virtual NSUrl RemoveLastPathComponent ();
	public virtual NSUrl RemovePathExtension ();
	public static NSUrl ResolveAlias (NSUrl aliasFileUrl, NSUrlBookmarkResolutionOptions options, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value, out NSError error);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with a NSString constant")]
	public bool SetResource (string key, NSObject value, out NSError error);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool SetResource (string key, NSObject value);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool TryGetResource (string key, out NSObject value, out NSError error);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool TryGetResource (string key, out NSObject value);
```

### Type Changed: MonoMac.Foundation.NSUrlAuthenticationChallenge

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlCache

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual void GetCachedResponse (NSUrlSessionDataTask dataTask, System.Action<NSCachedUrlResponse> completionHandler);
	public virtual System.Threading.Tasks.Task<NSCachedUrlResponse> GetCachedResponseAsync (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponse (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponsesSinceDate (NSDate date);
	public virtual void StoreCachedResponse (NSCachedUrlResponse cachedResponse, NSUrlSessionDataTask dataTask);
```

### Type Changed: MonoMac.Foundation.NSUrlComponents

Added interface:

```
INSObjectProtocol
```

Added property:

```
public virtual NSUrlQueryItem[] QueryItems { get; set; }
```

Added method:

```
public virtual string AsString ();
```

### Type Changed: MonoMac.Foundation.NSUrlConnection

Added interfaces:

```
INSURLAuthenticationChallengeSender
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlConnectionDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlConnectionDownloadDelegate

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlCredential

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlCredentialStorage

Added interface:

```
INSObjectProtocol
```

Added methods:

```
public virtual void GetCredentials (NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task, System.Action<NSDictionary> completionHandler);
	public virtual void GetDefaultCredential (NSUrlProtectionSpace space, NSUrlSessionTask task, System.Action<NSUrlCredential> completionHandler);
	public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSDictionary options, NSUrlSessionTask task);
	public virtual void SetCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
	public virtual void SetDefaultCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
```

### Type Changed: MonoMac.Foundation.NSUrlDownload

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlDownloadDelegate

Added interfaces:

```
INSUrlDownloadDelegate
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlError

Added values:

```
BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionRequiresSharedContainer = -995,
	BackgroundSessionWasDisconnected = -997,
```

### Type Changed: MonoMac.Foundation.NSUrlErrorCancelledReason

Added value:

```
InsufficientSystemResources = 2,
```

### Type Changed: MonoMac.Foundation.NSUrlProtectionSpace

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlProtocol

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlProtocolClient

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlRequest

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUrlResponse

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUserDefaults

Added interface:

```
INSObjectProtocol
```

Added method:

```
public NSDictionary ToDictionary ();
```

Obsoleted method:

```
[Obsolete ("Use ToDictionary instead")]
	public virtual NSDictionary AsDictionary ();
```

### Type Changed: MonoMac.Foundation.NSUserNotification

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUserNotificationCenter

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUserNotificationCenterDelegate

Added interfaces:

```
INSUserNotificationCenterDelegate
	INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSUuid

Added interface:

```
INSObjectProtocol
```

### Type Changed: MonoMac.Foundation.NSValue

Added interface:

```
INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.CoreAnimation.CATransform3D CATransform3DValue { get; }
	public virtual MonoMac.SceneKit.SCNMatrix4 SCNMatrix4Value { get; }
```

Added methods:

```
public static NSValue FromCATransform3D (MonoMac.CoreAnimation.CATransform3D transform);
	public static NSValue FromSCNMatrix4 (MonoMac.SceneKit.SCNMatrix4 matrix);
```

### Type Changed: MonoMac.Foundation.NSValueTransformer

Added interface:

```
INSObjectProtocol
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

### Type Changed: MonoMac.Foundation.NSZone

Added constructor:

```
public NSZone (System.IntPtr handle, bool owns);
```

### New Type MonoMac.Foundation.EncodingDetectionOptions

```
public class EncodingDetectionOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public EncodingDetectionOptions ();
	public EncodingDetectionOptions (NSDictionary dictionary);
	// properties
	public bool? EncodingDetectionAllowLossy { get; set; }
	public NSStringEncoding[] EncodingDetectionDisallowedEncodings { get; set; }
	public bool? EncodingDetectionFromWindows { get; set; }
	public NSString EncodingDetectionLikelyLanguage { get; set; }
	public NSString EncodingDetectionLossySubstitution { get; set; }
	public NSStringEncoding[] EncodingDetectionSuggestedEncodings { get; set; }
	public bool? EncodingDetectionUseOnlySuggestedEncodings { get; set; }
}
```

### New Type MonoMac.Foundation.EnumerateDatesCallback

```
public sealed delegate EnumerateDatesCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public EnumerateDatesCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSDate date, bool exactMatch, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSDate date, bool exactMatch, ref bool stop);
}
```

### New Type MonoMac.Foundation.EnumerateIndexSetCallback

```
public sealed delegate EnumerateIndexSetCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public EnumerateIndexSetCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint idx, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (uint idx, ref bool stop);
}
```

### New Type MonoMac.Foundation.INSConnectionDelegate

```
public interface INSConnectionDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.INSLocking

```
public interface INSLocking : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Lock ();
	public virtual void Unlock ();
}
```

### New Type MonoMac.Foundation.INSObjectProtocol

```
public interface INSObjectProtocol : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MonoMac.ObjCRuntime.Class Class { get; }
	public virtual string Description { get; }
	public virtual bool IsProxy { get; }
	public virtual int RetainCount { get; }
	public virtual NSObject Self { get; }
	public virtual MonoMac.ObjCRuntime.Class Superclass { get; }
	public virtual NSZone Zone { get; }
	// methods
	public virtual bool ConformsToProtocol (System.IntPtr aProtocol);
	public virtual NSObject DangerousAutorelease ();
	public virtual void DangerousRelease ();
	public virtual NSObject DangerousRetain ();
	public virtual uint GetNativeHash ();
	public virtual bool IsEqual (NSObject anObject);
	public virtual bool IsKindOfClass (MonoMac.ObjCRuntime.Class aClass);
	public virtual bool IsMemberOfClass (MonoMac.ObjCRuntime.Class aClass);
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector);
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector, NSObject object1, NSObject object2);
	public virtual NSObject PerformSelector (MonoMac.ObjCRuntime.Selector aSelector, NSObject anObject);
	public virtual bool RespondsToSelector (MonoMac.ObjCRuntime.Selector sel);
}
```

### New Type MonoMac.Foundation.INSURLAuthenticationChallengeSender

```
public interface INSURLAuthenticationChallengeSender : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void CancelAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
}
```

### New Type MonoMac.Foundation.INSUrlDownloadDelegate

```
public interface INSUrlDownloadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.INSUrlSessionDataDelegate

```
public interface INSUrlSessionDataDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUrlSessionDelegate

```
public interface INSUrlSessionDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.INSUrlSessionDownloadDelegate

```
public interface INSUrlSessionDownloadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUrlSessionTaskDelegate

```
public interface INSUrlSessionTaskDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUserNotificationCenterDelegate

```
public interface INSUserNotificationCenterDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.NSAppleScript

```
public class NSAppleScript : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSAppleScript (NSCoder coder);
	public NSAppleScript (NSObjectFlag t);
	public NSAppleScript (System.IntPtr handle);
	public NSAppleScript (string source);
	public NSAppleScript (NSUrl url, out NSDictionary errorInfo);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compiled { get; }
	public virtual string Source { get; }
	// methods
	public virtual bool CompileAndReturnError (out NSDictionary errorInfo);
	public virtual NSObject Copy (NSZone zone);
	public virtual NSAppleEventDescriptor ExecuteAndReturnError (out NSDictionary errorInfo);
	public virtual NSAppleEventDescriptor ExecuteAppleEvent (NSAppleEventDescriptor eventDescriptor, out NSDictionary errorInfo);
}
```

### New Type MonoMac.Foundation.NSCalendarDate

```
public class NSCalendarDate : MonoMac.Foundation.NSDate, INSCoding, INSCopying, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSCalendarDate ();
	public NSCalendarDate (string description);
	public NSCalendarDate (string description, string calendarFormat);
	public NSCalendarDate (string description, string calendarFormat, NSObject locale);
	public NSCalendarDate (System.IntPtr handle);
	public NSCalendarDate (NSObjectFlag t);
	public NSCalendarDate (NSCoder coder);
	public NSCalendarDate (int year, uint month, uint day, uint hour, uint minute, uint second, NSTimeZone aTimeZone);
	// properties
	public virtual string CalendarFormat { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int DayOfCommonEra { get; }
	public virtual int DayOfMonth { get; }
	public virtual int DayOfWeek { get; }
	public virtual int DayOfYear { get; }
	public virtual int HourOfDay { get; }
	public virtual int MinuteOfHour { get; }
	public virtual int MonthOfYear { get; }
	public virtual int SecondOfMinute { get; }
	public virtual NSTimeZone TimeZone { get; set; }
	public virtual int YearOfCommonEra { get; }
	// methods
	public virtual NSCalendarDate DateByAddingYears (int year, int month, int day, int hour, int minute, int second);
	protected override void Dispose (bool disposing);
	public virtual string GetDescription (string calendarFormat, NSObject locale);
	public virtual string GetDescription (string calendarFormat);
	public virtual string GetDescription (NSLocale locale);
}
```

### New Type MonoMac.Foundation.NSCocoaError

```
[Serializable]
public enum NSCocoaError {
	ExecutableArchitectureMismatch = 3585,
	ExecutableErrorMaximum = 3839,
	ExecutableErrorMinimum = 3584,
	ExecutableLink = 3588,
	ExecutableLoad = 3587,
	ExecutableNotLoadable = 3584,
	ExecutableRuntimeMismatch = 3586,
	FeatureUnsupported = 3328,
	FileErrorMaximum = 1023,
	FileErrorMinimum = 0,
	FileLocking = 255,
	FileNoSuchFile = 4,
	FileReadCorruptFile = 259,
	FileReadInapplicableStringEncoding = 261,
	FileReadInvalidFileName = 258,
	FileReadNoPermission = 257,
	FileReadNoSuchFile = 260,
	FileReadTooLarge = 263,
	FileReadUnknown = 256,
	FileReadUnknownStringEncoding = 264,
	FileReadUnsupportedScheme = 262,
	FileWriteFileExists = 516,
	FileWriteInapplicableStringEncoding = 517,
	FileWriteInvalidFileName = 514,
	FileWriteNoPermission = 513,
	FileWriteOutOfSpace = 640,
	FileWriteUnknown = 512,
	FileWriteUnsupportedScheme = 518,
	FileWriteVolumeReadOnly = 642,
	Formatting = 2048,
	FormattingErrorMaximum = 2559,
	FormattingErrorMinimum = 2048,
	KeyValueValidation = 1024,
	None = 0,
	PropertyListErrorMaximum = 4095,
	PropertyListErrorMinimum = 3840,
	PropertyListReadCorrupt = 3840,
	PropertyListReadStream = 3842,
	PropertyListReadUnknownVersion = 3841,
	PropertyListWriteInvalid = 3852,
	PropertyListWriteStream = 3851,
	UbiquitousFileErrorMaximum = 4607,
	UbiquitousFileErrorMinimum = 4352,
	UbiquitousFileNotUploadedDueToQuota = 4354,
	UbiquitousFileUbiquityServerNotAvailable = 4355,
	UbiquitousFileUnavailable = 4353,
	UserActivityConnectionUnavailableError = 4609,
	UserActivityErrorMaximum = 4863,
	UserActivityErrorMinimum = 4608,
	UserActivityHandoffFailedError = 4608,
	UserActivityHandoffUserInfoTooLargeError = 4611,
	UserActivityRemoteApplicationTimedOutError = 4610,
	UserCancelled = 3072,
	ValidationErrorMaximum = 2047,
	ValidationErrorMinimum = 1024,
	XpcConnectionErrorMaximum = 4224,
	XpcConnectionErrorMinimum = 4096,
	XpcConnectionInterrupted = 4097,
	XpcConnectionInvalid = 4099,
	XpcConnectionReplyInvalid = 4101,
}
```

### New Type MonoMac.Foundation.NSConnectionDelegate_Extensions

```
public static class NSConnectionDelegate_Extensions {
	// methods
	public static bool AllowNewConnection (INSConnectionDelegate This, NSConnection newConnection, NSConnection parentConnection);
	public static bool AuthenticateComponents (INSConnectionDelegate This, NSArray components, NSData authenticationData);
	public static NSObject CreateConversation (INSConnectionDelegate This, NSConnection connection);
	public static NSData GetAuthenticationData (INSConnectionDelegate This, NSArray components);
	public static bool HandleRequest (INSConnectionDelegate This, NSConnection connection, NSDistantObjectRequest request);
	public static bool ShouldMakeNewConnection (INSConnectionDelegate This, NSConnection parentConnection, NSConnection newConnection);
}
```

### New Type MonoMac.Foundation.NSDateComponentsFormatter

```
public class NSDateComponentsFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSDateComponentsFormatter ();
	public NSDateComponentsFormatter (NSCoder coder);
	public NSDateComponentsFormatter (NSObjectFlag t);
	public NSDateComponentsFormatter (System.IntPtr handle);
	// properties
	public virtual NSCalendarUnit AllowedUnits { get; set; }
	public virtual bool AllowsFractionalUnits { get; set; }
	public virtual NSCalendar Calendar { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool CollapsesLargestUnit { get; set; }
	public virtual NSFormattingContext FormattingContext { get; set; }
	public virtual bool IncludesApproximationPhrase { get; set; }
	public virtual bool IncludesTimeRemainingPhrase { get; set; }
	public virtual int MaximumUnitCount { get; set; }
	public virtual NSDateComponentsFormatterUnitsStyle UnitsStyle { get; set; }
	public virtual NSDateComponentsFormatterZeroFormattingBehavior ZeroFormattingBehavior { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public static string LocalizedStringFromDateComponents (NSDateComponents components, NSDateComponentsFormatterUnitsStyle unitsStyle);
	public virtual string StringForObjectValue (NSObject obj);
	public virtual string StringFromDate (NSDate startDate, NSDate endDate);
	public virtual string StringFromDateComponents (NSDateComponents components);
	public virtual string StringFromTimeInterval (double ti);
}
```

### New Type MonoMac.Foundation.NSDateComponentsFormatterUnitsStyle

```
[Serializable]
public enum NSDateComponentsFormatterUnitsStyle {
	Abbreviated = 1,
	Full = 3,
	Positional = 0,
	Short = 2,
	SpellOut = 4,
}
```

### New Type MonoMac.Foundation.NSDateComponentsFormatterZeroFormattingBehavior

```
[Serializable]
public enum NSDateComponentsFormatterZeroFormattingBehavior {
	Default = 1,
	DropAll = 14,
	DropLeading = 2,
	DropMiddle = 4,
	DropTrailing = 8,
	None = 0,
	Pad = 65536,
}
```

### New Type MonoMac.Foundation.NSDateIntervalFormatter

```
public class NSDateIntervalFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSDateIntervalFormatter ();
	public NSDateIntervalFormatter (NSCoder coder);
	public NSDateIntervalFormatter (NSObjectFlag t);
	public NSDateIntervalFormatter (System.IntPtr handle);
	// properties
	public virtual NSCalendar Calendar { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSDateIntervalFormatterStyle DateStyle { get; set; }
	public virtual string DateTemplate { get; set; }
	public virtual NSLocale Locale { get; set; }
	public virtual NSDateIntervalFormatterStyle TimeStyle { get; set; }
	public virtual NSTimeZone TimeZone { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual string StringFromDate (NSDate fromDate, NSDate toDate);
}
```

### New Type MonoMac.Foundation.NSDateIntervalFormatterStyle

```
[Serializable]
public enum NSDateIntervalFormatterStyle {
	Full = 4,
	Long = 3,
	Medium = 2,
	None = 0,
	Short = 1,
}
```

### New Type MonoMac.Foundation.NSEnergyFormatter

```
public class NSEnergyFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSEnergyFormatter ();
	public NSEnergyFormatter (NSCoder coder);
	public NSEnergyFormatter (NSObjectFlag t);
	public NSEnergyFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForFoodEnergyUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromJoules (double numberInJoules);
	public virtual string StringFromValue (double value, NSEnergyFormatterUnit unit);
	public virtual string UnitStringFromJoules (double numberInJoules, out NSEnergyFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSEnergyFormatterUnit unit);
}
```

### New Type MonoMac.Foundation.NSEnergyFormatterUnit

```
[Serializable]
public enum NSEnergyFormatterUnit {
	Calorie = 1793,
	Joule = 11,
	Kilocalorie = 1794,
	Kilojoule = 14,
}
```

### New Type MonoMac.Foundation.NSExtension

```
public class NSExtension {
	// methods

	[Obsolete ("It is not necessary to call this method anymore. It will be removed in a future release.")]
	public static void Initialize ();
}
```

### New Type MonoMac.Foundation.NSFileAccessIntent

```
public class NSFileAccessIntent : MonoMac.Foundation.NSObject, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSFileAccessIntent (NSCoder coder);
	public NSFileAccessIntent (NSObjectFlag t);
	public NSFileAccessIntent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrl Url { get; }
	// methods
	public static NSFileAccessIntent CreateReadingIntent (NSUrl url, NSFileCoordinatorReadingOptions options);
	public static NSFileAccessIntent CreateWritingIntent (NSUrl url, NSFileCoordinatorWritingOptions options);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.Foundation.NSFilePresenterReacquirer

```
public sealed delegate NSFilePresenterReacquirer : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSFilePresenterReacquirer (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.Action reacquirer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.Action reacquirer);
}
```

### New Type MonoMac.Foundation.NSFormattingContext

```
[Serializable]
public enum NSFormattingContext {
	BeginningOfSentence = 4,
	Dynamic = 1,
	ListItem = 3,
	MiddleOfSentence = 5,
	Standalone = 2,
	Unknown = 0,
}
```

### New Type MonoMac.Foundation.NSFormattingUnitStyle

```
[Serializable]
public enum NSFormattingUnitStyle {
	Long = 3,
	Medium = 2,
	Short = 1,
}
```

### New Type MonoMac.Foundation.NSItemDownloadingStatus

```
[Serializable]
public enum NSItemDownloadingStatus {
	Current = 0,
	Downloaded = 1,
	NotDownloaded = 2,
	Unknown = -1,
}
```

### New Type MonoMac.Foundation.NSItemProviderErrorCode

```
[Serializable]
public enum NSItemProviderErrorCode {
	ItemUnavailable = -1000,
	None = 0,
	UnexpectedValueClass = -1100,
	Unknown = -1,
}
```

### New Type MonoMac.Foundation.NSLengthFormatter

```
public class NSLengthFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSLengthFormatter ();
	public NSLengthFormatter (NSCoder coder);
	public NSLengthFormatter (NSObjectFlag t);
	public NSLengthFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForPersonHeightUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromMeters (double numberInMeters);
	public virtual string StringFromValue (double value, NSLengthFormatterUnit unit);
	public virtual string UnitStringFromMeters (double numberInMeters, ref NSLengthFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSLengthFormatterUnit unit);
}
```

### New Type MonoMac.Foundation.NSLengthFormatterUnit

```
[Serializable]
public enum NSLengthFormatterUnit {
	Centimeter = 9,
	Foot = 1282,
	Inch = 1281,
	Kilometer = 14,
	Meter = 11,
	Mile = 1284,
	Millimeter = 8,
	Yard = 1283,
}
```

### New Type MonoMac.Foundation.NSLocking_Extensions

```
public static class NSLocking_Extensions {
}
```

### New Type MonoMac.Foundation.NSMassFormatter

```
public class NSMassFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSMassFormatter ();
	public NSMassFormatter (NSCoder coder);
	public NSMassFormatter (NSObjectFlag t);
	public NSMassFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForPersonMassUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromKilograms (double numberInKilograms);
	public virtual string StringFromValue (double value, NSMassFormatterUnit unit);
	public virtual string UnitStringFromKilograms (double numberInKilograms, ref NSMassFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSMassFormatterUnit unit);
}
```

### New Type MonoMac.Foundation.NSMassFormatterUnit

```
[Serializable]
public enum NSMassFormatterUnit {
	Gram = 11,
	Kilogram = 14,
	Ounce = 1537,
	Pound = 1538,
	Stone = 1539,
}
```

### New Type MonoMac.Foundation.NSObjectProtocol_Extensions

```
public static class NSObjectProtocol_Extensions {
	// methods
	public static string GetDebugDescription (INSObjectProtocol This);
}
```

### New Type MonoMac.Foundation.NSObservedChange

```
public class NSObservedChange {
	// constructors
	public NSObservedChange (NSDictionary source);
	// properties
	public NSKeyValueChange Change { get; }
	public NSIndexSet Indexes { get; }
	public bool IsPrior { get; }
	public NSObject NewValue { get; }
	public NSObject OldValue { get; }
}
```

### New Type MonoMac.Foundation.NSOperatingSystemVersion

```
public struct NSOperatingSystemVersion {
	// constructors
	public NSOperatingSystemVersion (int major, int minor, int patchVersion);
	// fields
	public int Major;
	public int Minor;
	public int PatchVersion;
	// methods
	public override string ToString ();
}
```

### New Type MonoMac.Foundation.NSQualityOfService

```
[Serializable]
public enum NSQualityOfService {
	Background = 9,
	Default = -1,
	UserInitiated = 25,
	UserInteractive = 33,
	Utility = 17,
}
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

### New Type MonoMac.Foundation.NSUrl_PromisedItems

```
public static class NSUrl_PromisedItems {
	// methods
	public static bool CheckPromisedItemIsReachable (NSUrl This, out NSError error);
	public static bool GetPromisedItemResourceValue (NSUrl This, NSObject value, NSString key, out NSError error);
	public static NSDictionary GetPromisedItemResourceValues (NSUrl This, NSString[] keys, out NSError error);
}
```

### New Type MonoMac.Foundation.NSURLAuthenticationChallengeSender

```
public abstract class NSURLAuthenticationChallengeSender : MonoMac.Foundation.NSObject, INSURLAuthenticationChallengeSender, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSURLAuthenticationChallengeSender ();
	public NSURLAuthenticationChallengeSender (NSCoder coder);
	public NSURLAuthenticationChallengeSender (NSObjectFlag t);
	public NSURLAuthenticationChallengeSender (System.IntPtr handle);
	// methods
	public virtual void CancelAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
}
```

### New Type MonoMac.Foundation.NSURLAuthenticationChallengeSender_Extensions

```
public static class NSURLAuthenticationChallengeSender_Extensions {
}
```

### New Type MonoMac.Foundation.NSUrlDownloadDelegate_Extensions

```
public static class NSUrlDownloadDelegate_Extensions {
	// methods
	public static void CanceledAuthenticationChallenge (INSUrlDownloadDelegate This, NSUrlDownload download, NSUrlAuthenticationChallenge challenge);
	public static void CreatedDestination (INSUrlDownloadDelegate This, NSUrlDownload download, string path);
	public static void DecideDestination (INSUrlDownloadDelegate This, NSUrlDownload download, string suggestedFilename);
	public static bool DecodeSourceData (INSUrlDownloadDelegate This, NSUrlDownload download, string encodingType);
	public static void DownloadBegan (INSUrlDownloadDelegate This, NSUrlDownload download);
	public static void FailedWithError (INSUrlDownloadDelegate This, NSUrlDownload download, NSError error);
	public static void Finished (INSUrlDownloadDelegate This, NSUrlDownload download);
	public static void ReceivedAuthenticationChallenge (INSUrlDownloadDelegate This, NSUrlDownload download, NSUrlAuthenticationChallenge challenge);
	public static void ReceivedData (INSUrlDownloadDelegate This, NSUrlDownload download, uint length);
	public static void ReceivedResponse (INSUrlDownloadDelegate This, NSUrlDownload download, NSUrlResponse response);
	public static void Resume (INSUrlDownloadDelegate This, NSUrlDownload download, NSUrlResponse response, long startingByte);
	public static NSUrlRequest WillSendRequest (INSUrlDownloadDelegate This, NSUrlDownload download, NSUrlRequest request, NSUrlResponse redirectResponse);
}
```

### New Type MonoMac.Foundation.NSUrlDownloadSessionResponse

```
public sealed delegate NSUrlDownloadSessionResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlDownloadSessionResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrl location, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrl location, NSUrlResponse response, NSError error);
}
```

### New Type MonoMac.Foundation.NSUrlQueryItem

```
public class NSUrlQueryItem : MonoMac.Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlQueryItem ();
	public NSUrlQueryItem (NSCoder coder);
	public NSUrlQueryItem (NSObjectFlag t);
	public NSUrlQueryItem (System.IntPtr handle);
	public NSUrlQueryItem (string name, string value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public virtual string Value { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
}
```

### New Type MonoMac.Foundation.NSURLRelationship

```
[Serializable]
public enum NSURLRelationship {
	Contains = 0,
	Other = 2,
	Same = 1,
}
```

### New Type MonoMac.Foundation.NSUrlSession

```
public class NSUrlSession : MonoMac.Foundation.NSObject, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSession ();
	public NSUrlSession (NSCoder coder);
	public NSUrlSession (NSObjectFlag t);
	public NSUrlSession (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrlSessionConfiguration Configuration { get; }
	public NSUrlSessionDelegate Delegate { get; }
	public virtual NSOperationQueue DelegateQueue { get; }
	public virtual string SessionDescription { get; set; }
	public static NSUrlSession SharedSession { get; }
	public virtual NSObject WeakDelegate { get; }
	// methods
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrl url, out NSUrlSessionDataTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrlRequest request, out NSUrlSessionDataTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrlRequest request);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlDownloadSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlDownloadSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSData resumeData);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrl url, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrlRequest request, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrlRequest request);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlDownloadSessionResponse completionHandler);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskFromResumeDataAsync (NSData resumeData, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskFromResumeDataAsync (NSData resumeData);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL, NSUrlSessionResponse completionHandler);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData, out NSUrlSessionUploadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL, out NSUrlSessionUploadTask result);
	protected override void Dispose (bool disposing);
	public virtual void FinishTasksAndInvalidate ();
	public virtual void Flush (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task FlushAsync ();
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration);
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);
	public static NSUrlSession FromWeakConfiguration (NSUrlSessionConfiguration configuration, NSObject weakDelegate, NSOperationQueue delegateQueue);
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
	public virtual System.Threading.Tasks.Task<NSUrlSessionActiveTasks> GetTasksAsync ();
	public virtual void InvalidateAndCancel ();
	public virtual void Reset (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task ResetAsync ();
}
```

### New Type MonoMac.Foundation.NSUrlSessionActiveTasks

```
public class NSUrlSessionActiveTasks {
	// constructors
	public NSUrlSessionActiveTasks (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
	// properties
	public NSUrlSessionDataTask[] DataTasks { get; set; }
	public NSUrlSessionDownloadTask[] DownloadTasks { get; set; }
	public NSUrlSessionUploadTask[] UploadTasks { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionConfiguration

```
public class NSUrlSessionConfiguration : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionConfiguration ();
	public NSUrlSessionConfiguration (NSCoder coder);
	public NSUrlSessionConfiguration (NSObjectFlag t);
	public NSUrlSessionConfiguration (System.IntPtr handle);
	// properties
	public virtual bool AllowsCellularAccess { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSDictionary ConnectionProxyDictionary { get; set; }
	public static NSUrlSessionConfiguration DefaultSessionConfiguration { get; }
	public virtual bool Discretionary { get; set; }
	public static NSUrlSessionConfiguration EphemeralSessionConfiguration { get; }
	public virtual NSDictionary HttpAdditionalHeaders { get; set; }
	public virtual NSHttpCookieAcceptPolicy HttpCookieAcceptPolicy { get; set; }
	public virtual NSHttpCookieStorage HttpCookieStorage { get; set; }
	public virtual int HttpMaximumConnectionsPerHost { get; set; }
	public virtual bool HttpShouldSetCookies { get; set; }
	public virtual bool HttpShouldUsePipelining { get; set; }
	public virtual string Identifier { get; }
	public virtual NSUrlRequestNetworkServiceType NetworkServiceType { get; set; }
	public virtual NSUrlRequestCachePolicy RequestCachePolicy { get; set; }
	public virtual bool SessionSendsLaunchEvents { get; set; }
	public virtual string SharedContainerIdentifier { get; set; }
	public virtual double TimeoutIntervalForRequest { get; set; }
	public virtual double TimeoutIntervalForResource { get; set; }
	public virtual MonoMac.Security.SslProtocol TLSMaximumSupportedProtocol { get; set; }
	public virtual MonoMac.Security.SslProtocol TLSMinimumSupportedProtocol { get; set; }
	public virtual NSUrlCache URLCache { get; set; }
	public virtual NSUrlCredentialStorage URLCredentialStorage { get; set; }
	public virtual NSArray WeakProtocolClasses { get; set; }
	// methods
	public static NSUrlSessionConfiguration BackgroundSessionConfiguration (string identifier);
	public virtual NSObject Copy (NSZone zone);
	public static NSUrlSessionConfiguration CreateBackgroundSessionConfiguration (string identifier);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataDelegate

```
public class NSUrlSessionDataDelegate : MonoMac.Foundation.NSUrlSessionTaskDelegate, INSUrlSessionDataDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate, INSObjectProtocol {
	// constructors
	public NSUrlSessionDataDelegate ();
	public NSUrlSessionDataDelegate (NSCoder coder);
	public NSUrlSessionDataDelegate (NSObjectFlag t);
	public NSUrlSessionDataDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBecomeDownloadTask (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public virtual void DidReceiveData (NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public virtual void DidReceiveResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, System.Action<NSUrlSessionResponseDisposition> completionHandler);
	public virtual void WillCacheResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, System.Action<NSCachedUrlResponse> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataDelegate_Extensions

```
public static class NSUrlSessionDataDelegate_Extensions {
	// methods
	public static void DidBecomeDownloadTask (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public static void DidReceiveData (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public static void DidReceiveResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, System.Action<NSUrlSessionResponseDisposition> completionHandler);
	public static void WillCacheResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, System.Action<NSCachedUrlResponse> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataTask

```
public class NSUrlSessionDataTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionDataTask ();
	public NSUrlSessionDataTask (NSCoder coder);
	public NSUrlSessionDataTask (NSObjectFlag t);
	public NSUrlSessionDataTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataTaskRequest

```
public class NSUrlSessionDataTaskRequest {
	// constructors
	public NSUrlSessionDataTaskRequest (NSData data, NSUrlResponse response);
	// properties
	public NSData Data { get; set; }
	public NSUrlResponse Response { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionDelegate

```
public class NSUrlSessionDelegate : MonoMac.Foundation.NSObject, INSUrlSessionDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionDelegate ();
	public NSUrlSessionDelegate (NSCoder coder);
	public NSUrlSessionDelegate (NSObjectFlag t);
	public NSUrlSessionDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBecomeInvalid (NSUrlSession session, NSError error);
	public virtual void DidFinishEventsForBackgroundSession (NSUrlSession session);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDelegate_Extensions

```
public static class NSUrlSessionDelegate_Extensions {
	// methods
	public static void DidBecomeInvalid (INSUrlSessionDelegate This, NSUrlSession session, NSError error);
	public static void DidFinishEventsForBackgroundSession (INSUrlSessionDelegate This, NSUrlSession session);
	public static void DidReceiveChallenge (INSUrlSessionDelegate This, NSUrlSession session, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadDelegate

```
public class NSUrlSessionDownloadDelegate : MonoMac.Foundation.NSUrlSessionTaskDelegate, INSUrlSessionDownloadDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate, INSObjectProtocol {
	// constructors
	public NSUrlSessionDownloadDelegate ();
	public NSUrlSessionDownloadDelegate (NSCoder coder);
	public NSUrlSessionDownloadDelegate (NSObjectFlag t);
	public NSUrlSessionDownloadDelegate (System.IntPtr handle);
	// properties
	public static NSString TaskResumeDataKey { get; }
	// methods
	public virtual void DidFinishDownloading (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public virtual void DidResume (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public virtual void DidWriteData (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadDelegate_Extensions

```
public static class NSUrlSessionDownloadDelegate_Extensions {
	// methods
	public static void DidFinishDownloading (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public static void DidResume (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public static void DidWriteData (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadTask

```
public class NSUrlSessionDownloadTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionDownloadTask ();
	public NSUrlSessionDownloadTask (NSCoder coder);
	public NSUrlSessionDownloadTask (NSObjectFlag t);
	public NSUrlSessionDownloadTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void Cancel (System.Action<NSData> resumeCallback);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadTaskRequest

```
public class NSUrlSessionDownloadTaskRequest {
	// constructors
	public NSUrlSessionDownloadTaskRequest (NSUrl location, NSUrlResponse response);
	// properties

	[Obsolete ("Use the Location property")]
	public NSData Data { get; set; }
	public NSUrl Location { get; set; }
	public NSUrlResponse Response { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionPendingTasks

```
public sealed delegate NSUrlSessionPendingTasks : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionPendingTasks (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
}
```

### New Type MonoMac.Foundation.NSUrlSessionResponse

```
public sealed delegate NSUrlSessionResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSData data, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSData data, NSUrlResponse response, NSError error);
}
```

### New Type MonoMac.Foundation.NSUrlSessionTask

```
public class NSUrlSessionTask : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionTask ();
	public NSUrlSessionTask (NSCoder coder);
	public NSUrlSessionTask (NSObjectFlag t);
	public NSUrlSessionTask (System.IntPtr handle);
	// properties
	public virtual long BytesExpectedToReceive { get; }
	public virtual long BytesExpectedToSend { get; }
	public virtual long BytesReceived { get; }
	public virtual long BytesSent { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrlRequest CurrentRequest { get; }
	public virtual NSError Error { get; }
	public virtual NSUrlRequest OriginalRequest { get; }
	public virtual float Priority { get; set; }
	public virtual NSUrlResponse Response { get; }
	public virtual NSUrlSessionTaskState State { get; }
	public virtual string TaskDescription { get; set; }
	public virtual uint TaskIdentifier { get; }
	public static long TransferSizeUnknown { get; }
	// methods
	public virtual void Cancel ();
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Resume ();
	public virtual void Suspend ();
}
```

### New Type MonoMac.Foundation.NSUrlSessionTaskDelegate

```
public class NSUrlSessionTaskDelegate : MonoMac.Foundation.NSUrlSessionDelegate, INSUrlSessionTaskDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionDelegate, INSObjectProtocol {
	// constructors
	public NSUrlSessionTaskDelegate ();
	public NSUrlSessionTaskDelegate (NSCoder coder);
	public NSUrlSessionTaskDelegate (NSObjectFlag t);
	public NSUrlSessionTaskDelegate (System.IntPtr handle);
	// methods
	public virtual void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public virtual void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public virtual void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public virtual void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionTaskDelegate_Extensions

```
public static class NSUrlSessionTaskDelegate_Extensions {
	// methods
	public static void DidCompleteWithError (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSError error);
	public static void DidReceiveChallenge (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public static void DidSendBodyData (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public static void NeedNewBodyStream (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public static void WillPerformHttpRedirection (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
}
```

### New Type MonoMac.Foundation.NSURLSessionTaskPriority

```
public static class NSURLSessionTaskPriority {
	// properties
	public static float Default { get; }
	public static float High { get; }
	public static float Low { get; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionUploadTask

```
public class NSUrlSessionUploadTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSUrlSessionUploadTask ();
	public NSUrlSessionUploadTask (NSCoder coder);
	public NSUrlSessionUploadTask (NSObjectFlag t);
	public NSUrlSessionUploadTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.Foundation.NSUserNotificationCenterDelegate_Extensions

```
public static class NSUserNotificationCenterDelegate_Extensions {
	// methods
	public static void DidActivateNotification (INSUserNotificationCenterDelegate This, NSUserNotificationCenter center, NSUserNotification notification);
	public static void DidDeliverNotification (INSUserNotificationCenterDelegate This, NSUserNotificationCenter center, NSUserNotification notification);
	public static bool ShouldPresentNotification (INSUserNotificationCenterDelegate This, NSUserNotificationCenter center, NSUserNotification notification);
}
```

## Namespace MonoMac.GameKit

### Type Changed: MonoMac.GameKit.GKAchievement

Added constructor:

```
public GKAchievement (string identifier, GKPlayer player);
```

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual GKPlayer Player { get; }
```

Added methods:

```
public virtual MonoMac.AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
	public virtual void IssueChallengeToPlayers (string[] playerIDs, string message);
	public static void ReportAchievements (GKAchievement[] achievements, GKChallenge[] challenges, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements, GKChallenge[] challenges);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements);
	public virtual void SelectChallengeablePlayerIDs (string[] playerIDs, System.Action<System.String[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<System.String[]> SelectChallengeablePlayerIDsAsync (string[] playerIDs);
	public virtual void SelectChallengeablePlayers (GKPlayer[] players, System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> SelectChallengeablePlayersAsync (GKPlayer[] players);
```

### Type Changed: MonoMac.GameKit.GKAchievementChallenge

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKAchievementDescription

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKAchievementViewController

Added interfaces:

```
MonoMac.AppKit.INSSeguePerforming
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKAchievementViewControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKChallenge

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual GKPlayer IssuingPlayer { get; }
	public virtual GKPlayer ReceivingPlayer { get; }
```

### Type Changed: MonoMac.GameKit.GKDialogController

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKFriendRequestComposeViewController

Added interfaces:

```
MonoMac.AppKit.INSSeguePerforming
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public virtual void AddRecipientPlayers (GKPlayer[] players);
```

### Type Changed: MonoMac.GameKit.GKFriendRequestComposeViewControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKInvite

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual uint PlayerAttributes { get; }
	public virtual int PlayerGroup { get; }
	public virtual GKPlayer Sender { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.GameKit.GKLeaderboard

Added constructor:

```
public GKLeaderboard (GKPlayer[] players);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKLeaderboardViewController

Added interfaces:

```
MonoMac.AppKit.INSSeguePerforming
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKLeaderboardViewControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKLocalPlayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual System.Action<MonoMac.AppKit.NSViewController,MonoMac.Foundation.NSError> AuthenticateHandler { get; set; }
```

Added methods:

```
public virtual void DeleteSavedGames (string name, System.Action<MonoMac.Foundation.NSError> handler);
	public virtual void FetchSavedGames (System.Action<GKSavedGame[],MonoMac.Foundation.NSError> handler);
	public virtual void GenerateIdentityVerificationSignature (GKIdentityVerificationSignatureHandler completionHandler);
	public virtual void LoadDefaultLeaderboardCategoryID (System.Action<System.String,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardCategoryIDAsync ();
	public virtual void LoadDefaultLeaderboardIdentifier (System.Action<System.String,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardIdentifierAsync ();
	public virtual void LoadFriendPlayers (System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> LoadFriendPlayersAsync ();
	public virtual void RegisterListener (GKLocalPlayerListener listener);
	public virtual void ResolveConflictingSavedGames (GKSavedGame[] conflictingSavedGames, MonoMac.Foundation.NSData data, System.Action<GKSavedGame[],MonoMac.Foundation.NSError> handler);
	public virtual void SaveGameData (MonoMac.Foundation.NSData data, string name, System.Action<GKSavedGame,MonoMac.Foundation.NSError> handler);
	public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
	public virtual void SetDefaultLeaderboardIdentifier (string leaderboardIdentifier, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardIdentifierAsync (string leaderboardIdentifier);
	public virtual void UnregisterAllListeners ();
	public virtual void UnregisterListener (GKLocalPlayerListener listener);
```

### Type Changed: MonoMac.GameKit.GKMatch

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public GKMatchReinvitationForDisconnectedPlayer ShouldReinviteDisconnectedPlayer { get; set; }
```

Added events:

```
public event System.EventHandler<GKMatchReceivedDataFromRemotePlayerEventArgs> DataReceivedFromPlayer;
	public event System.EventHandler<GKMatchConnectionChangedEventArgs> StateChangedForPlayer;
```

Removed method:

```
public virtual bool SendDataToAllPlayers (MonoMac.Foundation.NSData data, GKMatchSendDataMode mode, System.IntPtr ptrToNSErrorHandle);
```

Added methods:

```
public virtual void ChooseBestHostingPlayer (System.Action<GKPlayer> completionHandler);
	public virtual bool SendData (MonoMac.Foundation.NSData data, string[] players, GKMatchSendDataMode mode, out MonoMac.Foundation.NSError error);
	public virtual bool SendData (MonoMac.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, out MonoMac.Foundation.NSError error);

	[Obsolete ("Use SendDataToAllPlayers")]
	public virtual bool SendDataToAllPlayer (MonoMac.Foundation.NSData data, GKMatchSendDataMode mode, out MonoMac.Foundation.NSError error);
	public virtual bool SendDataToAllPlayers (MonoMac.Foundation.NSData data, GKMatchSendDataMode mode, out MonoMac.Foundation.NSError error);

	[Obsolete ("Use SendDataToAllPlayers that takes out NSError")]
	public bool SendDataToAllPlayers (MonoMac.Foundation.NSData data, GKMatchSendDataMode mode, System.IntPtr ptrToNSErrorHandle);
```

### Type Changed: MonoMac.GameKit.GKMatchDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual void DataReceivedFromPlayer (GKMatch match, MonoMac.Foundation.NSData data, GKPlayer player);
	public virtual bool ShouldReinviteDisconnectedPlayer (GKMatch match, GKPlayer player);
	public virtual void StateChangedForPlayer (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
```

### Type Changed: MonoMac.GameKit.GKMatchDelegate_Extensions

Added methods:

```
public static void DataReceived (IGKMatchDelegate This, GKMatch match, MonoMac.Foundation.NSData data, string playerId);
	public static void DataReceivedFromPlayer (IGKMatchDelegate This, GKMatch match, MonoMac.Foundation.NSData data, GKPlayer player);
	public static bool ShouldReinviteDisconnectedPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player);
	public static void StateChangedForPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player, GKPlayerConnectionState state);
```

### Type Changed: MonoMac.GameKit.GKMatchmaker

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual void CancelPendingInvite (GKPlayer player);
	public virtual void FindPlayersForHostedRequest (GKMatchRequest request, System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> FindPlayersForHostedRequestAsync (GKMatchRequest request);
	public virtual void StartBrowsingForNearbyPlayers (System.Action<GKPlayer,System.Boolean> handler);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewController

Added interfaces:

```
MonoMac.AppKit.INSSeguePerforming
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added events:

```
public event System.EventHandler<GKMatchmakingPlayersEventArgs> DidFindHostedPlayers;
	public event System.EventHandler<GKMatchmakingPlayerEventArgs> HostedPlayerDidAccept;
```

Added method:

```
public virtual void SetHostedPlayerConnected (GKPlayer playerID, bool connected);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
	public virtual void HostedPlayerDidAccept (GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewControllerDelegate_Extensions

Added method:

```
public static void HostedPlayerDidAccept (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoMac.GameKit.GKMatchRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual GKPlayer[] Recipients { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetRecipientResponseHandler (System.Action<GKPlayer,MonoMac.GameKit.GKInviteRecipientResponse> handler);
```

### Type Changed: MonoMac.GameKit.GKNotificationBanner

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKPlayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKScore

Added constructor:

```
public GKScore (string identifier, GKPlayer player);
```

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public string Category { get; set; }
	public virtual GKPlayer GamePlayer { get; }
```

Added method:

```
public virtual MonoMac.AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
```

### Type Changed: MonoMac.GameKit.GKScoreChallenge

Added interfaces:

```
MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKTurnBasedEventHandler

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKTurnBasedEventHandlerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

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

### Type Changed: MonoMac.GameKit.GKTurnBasedExchange

Added constructors:

```
public GKTurnBasedExchange (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedExchange (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedExchange (System.IntPtr handle);
```

Added interfaces:

```
MonoMac.Foundation.INSObjectProtocol
	MonoMac.ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDate CompletionDate { get; }
	public virtual MonoMac.Foundation.NSData Data { get; }
	public virtual string ExchangeID { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant[] Recipients { get; }
	public virtual GKTurnBasedExchangeReply[] Replies { get; }
	public virtual MonoMac.Foundation.NSDate SendDate { get; }
	public virtual GKTurnBasedParticipant Sender { get; }
	public virtual GKTurnBasedExchangeStatus Status { get; }
	public virtual MonoMac.Foundation.NSDate TimeoutDate { get; }
	public static double TimeoutDefault { get; }
	public static double TimeoutNone { get; }
```

Added methods:

```
public virtual void Cancel (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task CancelAsync (string localizableMessage, MonoMac.Foundation.NSObject[] arguments);
	protected override void Dispose (bool disposing);
	public virtual void Reply (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, MonoMac.Foundation.NSData data, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task ReplyAsync (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, MonoMac.Foundation.NSData data);
```

### Type Changed: MonoMac.GameKit.GKTurnBasedExchangeReply

Added constructors:

```
public GKTurnBasedExchangeReply (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedExchangeReply (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedExchangeReply (System.IntPtr handle);
```

Added interfaces:

```
MonoMac.Foundation.INSObjectProtocol
	MonoMac.ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSData Data { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant Recipient { get; }
	public virtual MonoMac.Foundation.NSDate ReplyDate { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.GameKit.GKTurnBasedMatch

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKTurnBasedMatchmakerViewController

Added interfaces:

```
MonoMac.AppKit.INSSeguePerforming
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKTurnBasedMatchmakerViewControllerDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.GameKit.GKTurnBasedParticipant

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual GKPlayer Player { get; }
```

### Type Changed: MonoMac.GameKit.GKVoiceChat

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual GKPlayer[] Players { get; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetMuteStatus (GKPlayer player, bool isMuted);
	public virtual void SetPlayerVoiceChatStateChangeHandler (System.Action<GKPlayer,MonoMac.GameKit.GKVoiceChatPlayerState> handler);
```

### Type Changed: MonoMac.GameKit.IGKMatchDelegate

Removed method:

```
public virtual void DataReceived (GKMatch match, MonoMac.Foundation.NSData data, string playerId);
```

### Type Changed: MonoMac.GameKit.IGKMatchmakerViewControllerDelegate

Added method:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
```

### New Type MonoMac.GameKit.GKChallengeComposeHandler

```
public sealed delegate GKChallengeComposeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKChallengeComposeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs);
}
```

### New Type MonoMac.GameKit.GKChallengeListener

```
public class GKChallengeListener : MonoMac.Foundation.NSObject, IGKChallengeListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKChallengeListener ();
	public GKChallengeListener (MonoMac.Foundation.NSCoder coder);
	public GKChallengeListener (MonoMac.Foundation.NSObjectFlag t);
	public GKChallengeListener (System.IntPtr handle);
	// methods
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKChallengeListener_Extensions

```
public static class GKChallengeListener_Extensions {
	// methods
	public static void DidCompleteChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void DidReceiveChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
	public static void IssuedChallengeWasCompleted (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void WantsToPlayChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKGameCenterControllerDelegate

```
public class GKGameCenterControllerDelegate : MonoMac.Foundation.NSObject, IGKGameCenterControllerDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKGameCenterControllerDelegate ();
	public GKGameCenterControllerDelegate (MonoMac.Foundation.NSCoder coder);
	public GKGameCenterControllerDelegate (MonoMac.Foundation.NSObjectFlag t);
	public GKGameCenterControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void Finished (GKGameCenterViewController controller);
}
```

### New Type MonoMac.GameKit.GKGameCenterControllerDelegate_Extensions

```
public static class GKGameCenterControllerDelegate_Extensions {
	// methods
	public static void Finished (IGKGameCenterControllerDelegate This, GKGameCenterViewController controller);
}
```

### New Type MonoMac.GameKit.GKGameCenterViewController

```
public class GKGameCenterViewController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, MonoMac.AppKit.INSSeguePerforming, MonoMac.AppKit.INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKGameCenterViewController ();
	public GKGameCenterViewController (MonoMac.Foundation.NSCoder coder);
	public GKGameCenterViewController (MonoMac.Foundation.NSObjectFlag t);
	public GKGameCenterViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public GKGameCenterControllerDelegate Delegate { get; set; }
	public virtual string LeaderboardCategory { get; set; }
	public virtual string LeaderboardIdentifier { get; set; }
	public virtual GKLeaderboardTimeScope LeaderboardTimeScope { get; set; }
	public virtual GKGameCenterViewControllerState ViewState { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler Finished;
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.GameKit.GKIdentityVerificationSignatureHandler

```
public sealed delegate GKIdentityVerificationSignatureHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKIdentityVerificationSignatureHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSUrl publicKeyUrl, MonoMac.Foundation.NSData signature, MonoMac.Foundation.NSData salt, ulong timestamp, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSUrl publicKeyUrl, MonoMac.Foundation.NSData signature, MonoMac.Foundation.NSData salt, ulong timestamp, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.GameKit.GKInviteEventListener

```
public class GKInviteEventListener : MonoMac.Foundation.NSObject, IGKInviteEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKInviteEventListener ();
	public GKInviteEventListener (MonoMac.Foundation.NSCoder coder);
	public GKInviteEventListener (MonoMac.Foundation.NSObjectFlag t);
	public GKInviteEventListener (System.IntPtr handle);
	// methods
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type MonoMac.GameKit.GKInviteEventListener_Extensions

```
public static class GKInviteEventListener_Extensions {
	// methods
	public static void DidAcceptInvite (IGKInviteEventListener This, GKPlayer player, GKInvite invite);
	public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type MonoMac.GameKit.GKInviteRecipientResponse

```
[Serializable]
public enum GKInviteRecipientResponse {
	Accepted = 0,
	Declined = 1,
	Failed = 2,
	Incompatible = 3,
	NoAnswer = 5,
	UnableToConnect = 4,
}
```

### New Type MonoMac.GameKit.GKLocalPlayerListener

```
public class GKLocalPlayerListener : MonoMac.Foundation.NSObject, IGKLocalPlayerListener, IGKChallengeListener, IGKInviteEventListener, IGKSavedGameListener, IGKTurnBasedEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKLocalPlayerListener ();
	public GKLocalPlayerListener (MonoMac.Foundation.NSCoder coder);
	public GKLocalPlayerListener (MonoMac.Foundation.NSObjectFlag t);
	public GKLocalPlayerListener (System.IntPtr handle);
	// methods
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);
	public virtual void HasConflictingSavedGames (GKPlayer player, GKSavedGame[] savedGames);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKLocalPlayerListener_Extensions

```
public static class GKLocalPlayerListener_Extensions {
}
```

### New Type MonoMac.GameKit.GKMatchConnectionChangedEventArgs

```
public class GKMatchConnectionChangedEventArgs : System.EventArgs {
	// constructors
	public GKMatchConnectionChangedEventArgs (GKPlayer player, GKPlayerConnectionState state);
	// properties
	public GKPlayer Player { get; set; }
	public GKPlayerConnectionState State { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchmakingPlayerEventArgs

```
public class GKMatchmakingPlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayerEventArgs (GKPlayer playerID);
	// properties
	public GKPlayer PlayerID { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchmakingPlayersEventArgs

```
public class GKMatchmakingPlayersEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayersEventArgs (GKPlayer[] playerIDs);
	// properties
	public GKPlayer[] PlayerIDs { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchReceivedDataFromRemotePlayerEventArgs

```
public class GKMatchReceivedDataFromRemotePlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchReceivedDataFromRemotePlayerEventArgs (MonoMac.Foundation.NSData data, GKPlayer player);
	// properties
	public MonoMac.Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchReinvitationForDisconnectedPlayer

```
public sealed delegate GKMatchReinvitationForDisconnectedPlayer : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKMatchReinvitationForDisconnectedPlayer (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (GKMatch match, GKPlayer player, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (GKMatch match, GKPlayer player);
}
```

### New Type MonoMac.GameKit.GKSavedGame

```
public class GKSavedGame : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKSavedGame ();
	public GKSavedGame (MonoMac.Foundation.NSCoder coder);
	public GKSavedGame (MonoMac.Foundation.NSObjectFlag t);
	public GKSavedGame (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DeviceName { get; }
	public virtual MonoMac.Foundation.NSDate ModificationDate { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void LoadData (System.Action<MonoMac.Foundation.NSData,MonoMac.Foundation.NSError> handler);
	public virtual System.Threading.Tasks.Task<MonoMac.Foundation.NSData> LoadDataAsync ();
}
```

### New Type MonoMac.GameKit.GKSavedGameListener

```
public class GKSavedGameListener : MonoMac.Foundation.NSObject, IGKSavedGameListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKSavedGameListener ();
	public GKSavedGameListener (MonoMac.Foundation.NSCoder coder);
	public GKSavedGameListener (MonoMac.Foundation.NSObjectFlag t);
	public GKSavedGameListener (System.IntPtr handle);
	// methods
	public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void HasConflictingSavedGames (GKPlayer player, GKSavedGame[] savedGames);
}
```

### New Type MonoMac.GameKit.GKSavedGameListener_Extensions

```
public static class GKSavedGameListener_Extensions {
	// methods
	public static void DidModifySavedGame (IGKSavedGameListener This, GKPlayer player, GKSavedGame savedGame);
	public static void HasConflictingSavedGames (IGKSavedGameListener This, GKPlayer player, GKSavedGame[] savedGames);
}
```

### New Type MonoMac.GameKit.GKTurnBasedEventListener

```
public class GKTurnBasedEventListener : MonoMac.Foundation.NSObject, IGKTurnBasedEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GKTurnBasedEventListener ();
	public GKTurnBasedEventListener (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedEventListener (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedEventListener (System.IntPtr handle);
	// methods
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
```

### New Type MonoMac.GameKit.GKTurnBasedEventListener_Extensions

```
public static class GKTurnBasedEventListener_Extensions {
	// methods
	public static void DidRequestMatchWithOtherPlayers (IGKTurnBasedEventListener This, GKPlayer player, GKPlayer[] playersToInvite);
	public static void DidRequestMatchWithPlayers (IGKTurnBasedEventListener This, GKPlayer player, string[] playerIDsToInvite);
	public static void MatchEnded (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
	public static void ReceivedExchangeCancellation (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeReplies (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeRequest (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedTurnEvent (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
```

### New Type MonoMac.GameKit.IGKChallengeListener

```
public interface IGKChallengeListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKGameCenterControllerDelegate

```
public interface IGKGameCenterControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKInviteEventListener

```
public interface IGKInviteEventListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKLocalPlayerListener

```
public interface IGKLocalPlayerListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IGKChallengeListener, IGKInviteEventListener, IGKSavedGameListener, IGKTurnBasedEventListener {
}
```

### New Type MonoMac.GameKit.IGKSavedGameListener

```
public interface IGKSavedGameListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKTurnBasedEventListener

```
public interface IGKTurnBasedEventListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoMac.ImageIO

### Type Changed: MonoMac.ImageIO.CGImageDestination

Added methods:

```
public void AddImage (MonoMac.CoreGraphics.CGImage image, CGImageDestinationOptions options);
	public void AddImage (CGImageSource source, int index, CGImageDestinationOptions options);
	public static CGImageDestination Create (MonoMac.CoreGraphics.CGDataConsumer consumer, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
```

### Type Changed: MonoMac.ImageIO.CGImageDestinationOptions

Added properties:

```
public bool EmbedThumbnail { get; set; }
	public int? ImageMaxPixelSize { get; set; }
	public bool ShouldExcludeGPS { get; set; }
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

### Type Changed: MonoMac.ImageIO.CGImageProperties

Added properties:

```
public static MonoMac.Foundation.NSString GPSHPositioningError { get; }
	public static MonoMac.Foundation.NSString PNGDelayTime { get; }
	public static MonoMac.Foundation.NSString PNGLoopCount { get; }
	public static MonoMac.Foundation.NSString PNGUnclampedDelayTime { get; }
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

### New Type MonoMac.ImageIO.CGImagePropertyOrientation

```
[Serializable]
public enum CGImagePropertyOrientation {
	Down = 3,
	DownMirrored = 4,
	Left = 8,
	LeftMirrored = 5,
	Right = 6,
	RightMirrored = 7,
	Up = 1,
	UpMirrored = 2,
}
```

## Namespace MonoMac.ImageKit

### Type Changed: MonoMac.ImageKit.IKCameraDeviceView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKCameraDeviceViewDelegate

Added interfaces:

```
IIKCameraDeviceViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKDeviceBrowserView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKDeviceBrowserViewDelegate

Added interfaces:

```
IIKDeviceBrowserViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKFilterBrowserPanel

Added interfaces:

```
MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKFilterBrowserView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKFilterCustomUIProvider

Added interfaces:

```
IIKFilterCustomUIProvider
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKFilterUIView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public virtual IKFilterUIView GetFilterUIView (MonoMac.CoreImage.CIFilter filter, MonoMac.Foundation.NSDictionary configurationOptions, MonoMac.Foundation.NSArray excludedKeys);
```

### Type Changed: MonoMac.ImageKit.IKImageBrowserCell

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageBrowserDataSource

Added interfaces:

```
IIKImageBrowserDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageBrowserDelegate

Added interfaces:

```
IIKImageBrowserDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageBrowserItem

Added interfaces:

```
IIKImageBrowserItem
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageBrowserView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageEditPanel

Added interfaces:

```
MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageEditPanelDataSource

Added interfaces:

```
IIKImageEditPanelDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKImageView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKPictureTaker

Added interfaces:

```
MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKSaveOptions

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKSaveOptionsDelegate

Added interfaces:

```
IIKSaveOptionsDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKScannerDeviceView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKScannerDeviceViewDelegate

Added interfaces:

```
IIKScannerDeviceViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKSlideshow

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ImageKit.IKSlideshowDataSource

Added interfaces:

```
IIKSlideshowDataSource
	MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.ImageKit.IIKCameraDeviceViewDelegate

```
public interface IIKCameraDeviceViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.ImageKit.IIKDeviceBrowserViewDelegate

```
public interface IIKDeviceBrowserViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.ImageKit.IIKFilterCustomUIProvider

```
public interface IIKFilterCustomUIProvider : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IKFilterUIView GetFilterUIView (MonoMac.Foundation.NSDictionary configurationOptions, MonoMac.Foundation.NSArray excludedKeys);
}
```

### New Type MonoMac.ImageKit.IIKImageBrowserDataSource

```
public interface IIKImageBrowserDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual IKImageBrowserItem GetItem (IKImageBrowserView aBrowser, int index);
	public virtual int ItemCount (IKImageBrowserView aBrowser);
}
```

### New Type MonoMac.ImageKit.IIKImageBrowserDelegate

```
public interface IIKImageBrowserDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.ImageKit.IIKImageBrowserItem

```
public interface IIKImageBrowserItem : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MonoMac.Foundation.NSObject ImageRepresentation { get; }
	public virtual MonoMac.Foundation.NSString ImageRepresentationType { get; }
	public virtual string ImageUID { get; }
}
```

### New Type MonoMac.ImageKit.IIKImageEditPanelDataSource

```
public interface IIKImageEditPanelDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MonoMac.CoreGraphics.CGImage Image { get; }
	// methods
	public virtual void SetImageAndProperties (MonoMac.CoreGraphics.CGImage image, MonoMac.Foundation.NSDictionary metaData);
}
```

### New Type MonoMac.ImageKit.IIKSaveOptionsDelegate

```
public interface IIKSaveOptionsDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.ImageKit.IIKScannerDeviceViewDelegate

```
public interface IIKScannerDeviceViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.ImageKit.IIKSlideshowDataSource

```
public interface IIKSlideshowDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual int ItemCount { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject GetItemAt (int index);
}
```

### New Type MonoMac.ImageKit.IKCameraDeviceViewDelegate_Extensions

```
public static class IKCameraDeviceViewDelegate_Extensions {
	// methods
	public static void DidEncounterError (IIKCameraDeviceViewDelegate This, IKCameraDeviceView cameraDeviceView, MonoMac.Foundation.NSError error);
	public static void SelectionDidChange (IIKCameraDeviceViewDelegate This, IKCameraDeviceView cameraDeviceView);
}
```

### New Type MonoMac.ImageKit.IKDeviceBrowserViewDelegate_Extensions

```
public static class IKDeviceBrowserViewDelegate_Extensions {
	// methods
	public static void DidEncounterError (IIKDeviceBrowserViewDelegate This, IKDeviceBrowserView deviceBrowserView, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.ImageKit.IKFilterCustomUIProvider_Extensions

```
public static class IKFilterCustomUIProvider_Extensions {
}
```

### New Type MonoMac.ImageKit.IKImageBrowserDataSource_Extensions

```
public static class IKImageBrowserDataSource_Extensions {
	// methods
	public static MonoMac.Foundation.NSDictionary GetGroup (IIKImageBrowserDataSource This, IKImageBrowserView aBrowser, int index);
	public static int GroupCount (IIKImageBrowserDataSource This, IKImageBrowserView aBrowser);
	public static bool MoveItems (IIKImageBrowserDataSource This, IKImageBrowserView aBrowser, MonoMac.Foundation.NSIndexSet indexes, int destinationIndex);
	public static void RemoveItems (IIKImageBrowserDataSource This, IKImageBrowserView aBrowser, MonoMac.Foundation.NSIndexSet indexes);
	public static int WriteItemsToPasteboard (IIKImageBrowserDataSource This, IKImageBrowserView aBrowser, MonoMac.Foundation.NSIndexSet itemIndexes, MonoMac.AppKit.NSPasteboard pasteboard);
}
```

### New Type MonoMac.ImageKit.IKImageBrowserDelegate_Extensions

```
public static class IKImageBrowserDelegate_Extensions {
	// methods
	public static void BackgroundWasRightClicked (IIKImageBrowserDelegate This, IKImageBrowserView browser, MonoMac.AppKit.NSEvent nsevent);
	public static void CellWasDoubleClicked (IIKImageBrowserDelegate This, IKImageBrowserView browser, int index);
	public static void CellWasRightClicked (IIKImageBrowserDelegate This, IKImageBrowserView browser, int index, MonoMac.AppKit.NSEvent nsevent);
	public static void SelectionDidChange (IIKImageBrowserDelegate This, IKImageBrowserView browser);
}
```

### New Type MonoMac.ImageKit.IKImageBrowserItem_Extensions

```
public static class IKImageBrowserItem_Extensions {
	// methods
	public static string GetImageSubtitle (IIKImageBrowserItem This);
	public static string GetImageTitle (IIKImageBrowserItem This);
	public static int GetImageVersion (IIKImageBrowserItem This);
	public static bool GetIsSelectable (IIKImageBrowserItem This);
}
```

### New Type MonoMac.ImageKit.IKImageEditPanelDataSource_Extensions

```
public static class IKImageEditPanelDataSource_Extensions {
	// methods
	public static bool GetHasAdjustMode (IIKImageEditPanelDataSource This);
	public static bool GetHasDetailsMode (IIKImageEditPanelDataSource This);
	public static bool GetHasEffectsMode (IIKImageEditPanelDataSource This);
	public static MonoMac.Foundation.NSDictionary GetImageProperties (IIKImageEditPanelDataSource This);
	public static MonoMac.CoreGraphics.CGImage GetThumbnail (IIKImageEditPanelDataSource This, System.Drawing.SizeF maximumSize);
}
```

### New Type MonoMac.ImageKit.IKSaveOptionsDelegate_Extensions

```
public static class IKSaveOptionsDelegate_Extensions {
	// methods
	public static bool ShouldShowType (IIKSaveOptionsDelegate This, IKSaveOptions saveOptions, string imageUTType);
}
```

### New Type MonoMac.ImageKit.IKScannerDeviceViewDelegate_Extensions

```
public static class IKScannerDeviceViewDelegate_Extensions {
	// methods
	public static void DidEncounterError (IIKScannerDeviceViewDelegate This, IKScannerDeviceView scannerDeviceView, MonoMac.Foundation.NSError error);
	public static void DidScan (IIKScannerDeviceViewDelegate This, IKScannerDeviceView scannerDeviceView, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.ImageKit.IKSlideshowDataSource_Extensions

```
public static class IKSlideshowDataSource_Extensions {
	// methods
	public static bool CanExportItemToApplication (IIKSlideshowDataSource This, int index, string applicationBundleIdentifier);
	public static void DidChange (IIKSlideshowDataSource This, int newIndex);
	public static void DidStop (IIKSlideshowDataSource This);
	public static string GetNameOfItemAt (IIKSlideshowDataSource This, int index);
	public static void WillStart (IIKSlideshowDataSource This);
}
```

## Namespace MonoMac.MobileCoreServices

### Type Changed: MonoMac.MobileCoreServices.UTType

Removed fields:

```
public static MonoMac.Foundation.NSString AliasFile;
	public static MonoMac.Foundation.NSString AliasRecord;
	public static MonoMac.Foundation.NSString AppleICNS;
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Audio;
	public static MonoMac.Foundation.NSString Application;
	public static MonoMac.Foundation.NSString ApplicationBundle;
	public static MonoMac.Foundation.NSString ApplicationFile;
	public static MonoMac.Foundation.NSString Archive;
	public static MonoMac.Foundation.NSString Audio;
	public static MonoMac.Foundation.NSString AudiovisualContent;
	public static MonoMac.Foundation.NSString BMP;
	public static MonoMac.Foundation.NSString Bundle;
	public static MonoMac.Foundation.NSString CHeader;
	public static MonoMac.Foundation.NSString CompositeContent;
	public static MonoMac.Foundation.NSString ConformsToKey;
	public static MonoMac.Foundation.NSString Contact;
	public static MonoMac.Foundation.NSString Content;
	public static MonoMac.Foundation.NSString CPlusPlusHeader;
	public static MonoMac.Foundation.NSString CPlusPlusSource;
	public static MonoMac.Foundation.NSString CSource;
	public static MonoMac.Foundation.NSString Data;
	public static MonoMac.Foundation.NSString DescriptionKey;
	public static MonoMac.Foundation.NSString Directory;
	public static MonoMac.Foundation.NSString DiskImage;
	public static MonoMac.Foundation.NSString ExportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString FileURL;
	public static MonoMac.Foundation.NSString FlatRTFD;
	public static MonoMac.Foundation.NSString Folder;
	public static MonoMac.Foundation.NSString Framework;
	public static MonoMac.Foundation.NSString GIF;
	public static MonoMac.Foundation.NSString HTML;
	public static MonoMac.Foundation.NSString ICO;
	public static MonoMac.Foundation.NSString IconFileKey;
	public static MonoMac.Foundation.NSString IdentifierKey;
	public static MonoMac.Foundation.NSString Image;
	public static MonoMac.Foundation.NSString ImportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString InkText;
	public static MonoMac.Foundation.NSString Item;
	public static MonoMac.Foundation.NSString JavaSource;
	public static MonoMac.Foundation.NSString JPEG;
	public static MonoMac.Foundation.NSString JPEG2000;
	public static MonoMac.Foundation.NSString Message;
	public static MonoMac.Foundation.NSString MountPoint;
	public static MonoMac.Foundation.NSString Movie;
	public static MonoMac.Foundation.NSString MP3;
	public static MonoMac.Foundation.NSString MPEG;
	public static MonoMac.Foundation.NSString MPEG4;
	public static MonoMac.Foundation.NSString MPEG4Audio;
	public static MonoMac.Foundation.NSString ObjectiveCPlusPlusSource;
	public static MonoMac.Foundation.NSString ObjectiveCSource;
	public static MonoMac.Foundation.NSString Package;
	public static MonoMac.Foundation.NSString PDF;
	public static MonoMac.Foundation.NSString PICT;
	public static MonoMac.Foundation.NSString PlainText;
	public static MonoMac.Foundation.NSString PNG;
	public static MonoMac.Foundation.NSString QuickTimeImage;
	public static MonoMac.Foundation.NSString QuickTimeMovie;
	public static MonoMac.Foundation.NSString ReferenceURLKey;
	public static MonoMac.Foundation.NSString Resolvable;
	public static MonoMac.Foundation.NSString RTF;
	public static MonoMac.Foundation.NSString RTFD;
	public static MonoMac.Foundation.NSString SourceCode;
	public static MonoMac.Foundation.NSString SymLink;
	public static MonoMac.Foundation.NSString TagClassFilenameExtension;
	public static MonoMac.Foundation.NSString TagClassMIMEType;
	public static MonoMac.Foundation.NSString TagClassNSPboardType;
	public static MonoMac.Foundation.NSString TagClassOSType;
	public static MonoMac.Foundation.NSString TagSpecificationKey;
	public static MonoMac.Foundation.NSString Text;
	public static MonoMac.Foundation.NSString TIFF;
	public static MonoMac.Foundation.NSString TXNTextAndMultimediaData;
	public static MonoMac.Foundation.NSString URL;
	public static MonoMac.Foundation.NSString UTF16ExternalPlainText;
	public static MonoMac.Foundation.NSString UTF16PlainText;
	public static MonoMac.Foundation.NSString UTF8PlainText;
	public static MonoMac.Foundation.NSString VCard;
	public static MonoMac.Foundation.NSString VersionKey;
	public static MonoMac.Foundation.NSString Video;
	public static MonoMac.Foundation.NSString Volume;
	public static MonoMac.Foundation.NSString WebArchive;
	public static MonoMac.Foundation.NSString XML;
```

Added properties:

```
public static MonoMac.Foundation.NSString AliasFile { get; }
	public static MonoMac.Foundation.NSString AliasRecord { get; }
	public static MonoMac.Foundation.NSString AppleICNS { get; }
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Audio { get; }
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Video { get; }
	public static MonoMac.Foundation.NSString AppleScript { get; }
	public static MonoMac.Foundation.NSString Application { get; }
	public static MonoMac.Foundation.NSString ApplicationBundle { get; }
	public static MonoMac.Foundation.NSString ApplicationFile { get; }
	public static MonoMac.Foundation.NSString Archive { get; }
	public static MonoMac.Foundation.NSString AssemblyLanguageSource { get; }
	public static MonoMac.Foundation.NSString Audio { get; }
	public static MonoMac.Foundation.NSString AudioInterchangeFileFormat { get; }
	public static MonoMac.Foundation.NSString AudiovisualContent { get; }
	public static MonoMac.Foundation.NSString AVIMovie { get; }
	public static MonoMac.Foundation.NSString BinaryPropertyList { get; }
	public static MonoMac.Foundation.NSString BMP { get; }
	public static MonoMac.Foundation.NSString Bookmark { get; }
	public static MonoMac.Foundation.NSString Bundle { get; }
	public static MonoMac.Foundation.NSString Bzip2Archive { get; }
	public static MonoMac.Foundation.NSString CalendarEvent { get; }
	public static MonoMac.Foundation.NSString CHeader { get; }
	public static MonoMac.Foundation.NSString CommaSeparatedText { get; }
	public static MonoMac.Foundation.NSString CompositeContent { get; }
	public static MonoMac.Foundation.NSString ConformsToKey { get; }
	public static MonoMac.Foundation.NSString Contact { get; }
	public static MonoMac.Foundation.NSString Content { get; }
	public static MonoMac.Foundation.NSString CPlusPlusHeader { get; }
	public static MonoMac.Foundation.NSString CPlusPlusSource { get; }
	public static MonoMac.Foundation.NSString CSource { get; }
	public static MonoMac.Foundation.NSString Data { get; }
	public static MonoMac.Foundation.NSString Database { get; }
	public static MonoMac.Foundation.NSString DelimitedText { get; }
	public static MonoMac.Foundation.NSString DescriptionKey { get; }
	public static MonoMac.Foundation.NSString Directory { get; }
	public static MonoMac.Foundation.NSString DiskImage { get; }
	public static MonoMac.Foundation.NSString ElectronicPublication { get; }
	public static MonoMac.Foundation.NSString EmailMessage { get; }
	public static MonoMac.Foundation.NSString Executable { get; }
	public static MonoMac.Foundation.NSString ExportedTypeDeclarationsKey { get; }
	public static MonoMac.Foundation.NSString FileURL { get; }
	public static MonoMac.Foundation.NSString FlatRTFD { get; }
	public static MonoMac.Foundation.NSString Folder { get; }
	public static MonoMac.Foundation.NSString Font { get; }
	public static MonoMac.Foundation.NSString Framework { get; }
	public static MonoMac.Foundation.NSString GIF { get; }
	public static MonoMac.Foundation.NSString GNUZipArchive { get; }
	public static MonoMac.Foundation.NSString HTML { get; }
	public static MonoMac.Foundation.NSString ICO { get; }
	public static MonoMac.Foundation.NSString IconFileKey { get; }
	public static MonoMac.Foundation.NSString IdentifierKey { get; }
	public static MonoMac.Foundation.NSString Image { get; }
	public static MonoMac.Foundation.NSString ImportedTypeDeclarationsKey { get; }
	public static MonoMac.Foundation.NSString InkText { get; }
	public static MonoMac.Foundation.NSString InternetLocation { get; }
	public static MonoMac.Foundation.NSString Item { get; }
	public static MonoMac.Foundation.NSString JavaArchive { get; }
	public static MonoMac.Foundation.NSString JavaClass { get; }
	public static MonoMac.Foundation.NSString JavaScript { get; }
	public static MonoMac.Foundation.NSString JavaSource { get; }
	public static MonoMac.Foundation.NSString JPEG { get; }
	public static MonoMac.Foundation.NSString JPEG2000 { get; }
	public static MonoMac.Foundation.NSString JSON { get; }
	public static MonoMac.Foundation.NSString Log { get; }
	public static MonoMac.Foundation.NSString M3UPlaylist { get; }
	public static MonoMac.Foundation.NSString Message { get; }
	public static MonoMac.Foundation.NSString MIDIAudio { get; }
	public static MonoMac.Foundation.NSString MountPoint { get; }
	public static MonoMac.Foundation.NSString Movie { get; }
	public static MonoMac.Foundation.NSString MP3 { get; }
	public static MonoMac.Foundation.NSString MPEG { get; }
	public static MonoMac.Foundation.NSString MPEG2TransportStream { get; }
	public static MonoMac.Foundation.NSString MPEG2Video { get; }
	public static MonoMac.Foundation.NSString MPEG4 { get; }
	public static MonoMac.Foundation.NSString MPEG4Audio { get; }
	public static MonoMac.Foundation.NSString ObjectiveCPlusPlusSource { get; }
	public static MonoMac.Foundation.NSString ObjectiveCSource { get; }
	public static MonoMac.Foundation.NSString OSAScript { get; }
	public static MonoMac.Foundation.NSString OSAScriptBundle { get; }
	public static MonoMac.Foundation.NSString Package { get; }
	public static MonoMac.Foundation.NSString PDF { get; }
	public static MonoMac.Foundation.NSString PerlScript { get; }
	public static MonoMac.Foundation.NSString PHPScript { get; }
	public static MonoMac.Foundation.NSString PICT { get; }
	public static MonoMac.Foundation.NSString PKCS12 { get; }
	public static MonoMac.Foundation.NSString PlainText { get; }
	public static MonoMac.Foundation.NSString Playlist { get; }
	public static MonoMac.Foundation.NSString PluginBundle { get; }
	public static MonoMac.Foundation.NSString PNG { get; }
	public static MonoMac.Foundation.NSString Presentation { get; }
	public static MonoMac.Foundation.NSString PropertyList { get; }
	public static MonoMac.Foundation.NSString PythonScript { get; }
	public static MonoMac.Foundation.NSString QuickLookGenerator { get; }
	public static MonoMac.Foundation.NSString QuickTimeImage { get; }
	public static MonoMac.Foundation.NSString QuickTimeMovie { get; }
	public static MonoMac.Foundation.NSString RawImage { get; }
	public static MonoMac.Foundation.NSString ReferenceURLKey { get; }
	public static MonoMac.Foundation.NSString Resolvable { get; }
	public static MonoMac.Foundation.NSString RTF { get; }
	public static MonoMac.Foundation.NSString RTFD { get; }
	public static MonoMac.Foundation.NSString RubyScript { get; }
	public static MonoMac.Foundation.NSString ScalableVectorGraphics { get; }
	public static MonoMac.Foundation.NSString Script { get; }
	public static MonoMac.Foundation.NSString ShellScript { get; }
	public static MonoMac.Foundation.NSString SourceCode { get; }
	public static MonoMac.Foundation.NSString SpotlightImporter { get; }
	public static MonoMac.Foundation.NSString Spreadsheet { get; }
	public static MonoMac.Foundation.NSString SymLink { get; }
	public static MonoMac.Foundation.NSString SystemPreferencesPane { get; }
	public static MonoMac.Foundation.NSString TabSeparatedText { get; }
	public static MonoMac.Foundation.NSString TagClassFilenameExtension { get; }
	public static MonoMac.Foundation.NSString TagClassMIMEType { get; }
	public static MonoMac.Foundation.NSString TagClassNSPboardType { get; }
	public static MonoMac.Foundation.NSString TagClassOSType { get; }
	public static MonoMac.Foundation.NSString TagSpecificationKey { get; }
	public static MonoMac.Foundation.NSString Text { get; }
	public static MonoMac.Foundation.NSString ThreeDContent { get; }
	public static MonoMac.Foundation.NSString TIFF { get; }
	public static MonoMac.Foundation.NSString ToDoItem { get; }
	public static MonoMac.Foundation.NSString TXNTextAndMultimediaData { get; }
	public static MonoMac.Foundation.NSString UnixExecutable { get; }
	public static MonoMac.Foundation.NSString URL { get; }
	public static MonoMac.Foundation.NSString URLBookmarkData { get; }
	public static MonoMac.Foundation.NSString UTF16ExternalPlainText { get; }
	public static MonoMac.Foundation.NSString UTF16PlainText { get; }
	public static MonoMac.Foundation.NSString UTF8PlainText { get; }
	public static MonoMac.Foundation.NSString UTF8TabSeparatedText { get; }
	public static MonoMac.Foundation.NSString VCard { get; }
	public static MonoMac.Foundation.NSString VersionKey { get; }
	public static MonoMac.Foundation.NSString Video { get; }
	public static MonoMac.Foundation.NSString Volume { get; }
	public static MonoMac.Foundation.NSString WaveformAudio { get; }
	public static MonoMac.Foundation.NSString WebArchive { get; }
	public static MonoMac.Foundation.NSString WindowsExecutable { get; }
	public static MonoMac.Foundation.NSString X509Certificate { get; }
	public static MonoMac.Foundation.NSString XML { get; }
	public static MonoMac.Foundation.NSString XMLPropertyList { get; }
	public static MonoMac.Foundation.NSString XPCService { get; }
	public static MonoMac.Foundation.NSString ZipArchive { get; }
```

Added methods:

```
public bool ConformsTo (string uti, string conformsToUti);
	public string[] CopyAllTags (string uti, string tagClass);
	public string[] CreateAllIdentifiers (string tagClass, string tag, string conformingToUti);
	public static string CreatePreferredIdentifier (string tagClass, string tag, string conformingToUti);
	public string GetDescription (string uti);
	public static bool IsDeclared (string utType);
	public static bool IsDynamic (string utType);
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
public static void AudioComponentDescriptionNative_objc_msgSend_stret (out MonoMac.AudioUnit.AudioComponentDescriptionNative retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioComponentDescriptionNative_objc_msgSendSuper_stret (out MonoMac.AudioUnit.AudioComponentDescriptionNative retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioStreamBasicDescription_objc_msgSend_stret (out MonoMac.AudioToolbox.AudioStreamBasicDescription retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioStreamBasicDescription_objc_msgSendSuper_stret (out MonoMac.AudioToolbox.AudioStreamBasicDescription retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioTimeStamp_objc_msgSend_stret (out MonoMac.AudioToolbox.AudioTimeStamp retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioTimeStamp_objc_msgSendSuper_stret (out MonoMac.AudioToolbox.AudioTimeStamp retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DAngularOrientation_objc_msgSend_stret (out MonoMac.AVFoundation.AVAudio3DAngularOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DAngularOrientation_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVAudio3DAngularOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.AVFoundation.AVAudio3DVectorOrientation AVAudio3DVectorOrientation_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DVectorOrientation_objc_msgSend_stret (out MonoMac.AVFoundation.AVAudio3DVectorOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.AVFoundation.AVAudio3DVectorOrientation AVAudio3DVectorOrientation_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DVectorOrientation_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVAudio3DVectorOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static bool bool_objc_msgSend_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_CLLocationCoordinate2D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreLocation.CLLocationCoordinate2D arg1);
	public static bool bool_objc_msgSend_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_byte_byte_byte_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, byte arg2, byte arg3, byte arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, uint arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_out_Boolean_out_Boolean_out_Boolean_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_UInt32_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4, uint arg5);
	public static bool bool_objc_msgSend_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_NSOperatingSystemVersion (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSOperatingSystemVersion arg1);
	public static bool bool_objc_msgSend_out_NSURLRelationship_int_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, int arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_out_NSURLRelationship_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSend_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_ref_IntPtr_out_Double_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, int arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_ref_IntPtr_out_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, System.IntPtr arg3);
	public static bool bool_objc_msgSend_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_CLLocationCoordinate2D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreLocation.CLLocationCoordinate2D arg1);
	public static bool bool_objc_msgSendSuper_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_byte_byte_byte_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, byte arg2, byte arg3, byte arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, uint arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_out_Boolean_out_Boolean_out_Boolean_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_UInt32_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4, uint arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_NSOperatingSystemVersion (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSOperatingSystemVersion arg1);
	public static bool bool_objc_msgSendSuper_out_NSURLRelationship_int_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, int arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_out_NSURLRelationship_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_Double_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, int arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2);
	public static void CGAffineTransform_objc_msgSend_stret_int (out MonoMac.CoreGraphics.CGAffineTransform retval, System.IntPtr receiver, System.IntPtr selector, int arg1);
	public static void CGAffineTransform_objc_msgSendSuper_stret_int (out MonoMac.CoreGraphics.CGAffineTransform retval, System.IntPtr receiver, System.IntPtr selector, int arg1);
	public static double Double_objc_msgSend_UInt64 (System.IntPtr receiver, System.IntPtr selector, ulong arg1);
	public static double Double_objc_msgSendSuper_UInt64 (System.IntPtr receiver, System.IntPtr selector, ulong arg1);
	public static float float_objc_msgSend_SizeF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1);
	public static float float_objc_msgSendSuper_SizeF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSend_IntPtr_NSRange_UInt64_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, System.IntPtr arg6);
	public static int int_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSendSuper_IntPtr_NSRange_UInt64_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, System.IntPtr arg6);
	public static int int_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_AudioComponentDescriptionNative (System.IntPtr receiver, System.IntPtr selector, MonoMac.AudioUnit.AudioComponentDescriptionNative arg1);
	public static System.IntPtr IntPtr_objc_msgSend_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_CATransform3D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreAnimation.CATransform3D arg1);
	public static System.IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreLocation.CLLocationCoordinate2D arg1, double arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_out_NSEnergyFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, out MonoMac.Foundation.NSEnergyFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_ref_NSLengthFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSLengthFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_ref_NSMassFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSMassFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_UInt32 (System.IntPtr receiver, System.IntPtr selector, double arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSend_float_float_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4, bool arg5);
	public static System.IntPtr IntPtr_objc_msgSend_float_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, MonoMac.SceneKit.SCNVector3 arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6, int arg7, int arg8);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, System.IntPtr arg4, int arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_UInt32_UInt32_UInt32_UInt32_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, uint arg2, uint arg3, uint arg4, uint arg5, uint arg6, System.IntPtr arg7);
	public static System.IntPtr IntPtr_objc_msgSend_Int64_Double (System.IntPtr receiver, System.IntPtr selector, long arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_NSRange_ref_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref int arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.Drawing.PointF arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_NSRange_UInt64_IntPtr_int_ref_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, ref System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNMatrix4_SCNMatrix4_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2, MonoMac.SceneKit.SCNMatrix4 arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3, MonoMac.SceneKit.SCNVector3 arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_SCNVector3_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3, System.IntPtr arg4, MonoMac.SceneKit.SCNVector3 arg5, MonoMac.SceneKit.SCNVector3 arg6);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, bool arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_IntPtr_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_QTTime_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioStreamBasicDescription (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioStreamBasicDescription_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioTimeStamp_Double (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioTimeStamp arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static System.IntPtr IntPtr_objc_msgSend_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector3_SCNVector3_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector4_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_Double_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, bool arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_Double_UInt32_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, uint arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSend_UInt64_Int64_Double (System.IntPtr receiver, System.IntPtr selector, ulong arg1, long arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_AudioComponentDescriptionNative (System.IntPtr receiver, System.IntPtr selector, MonoMac.AudioUnit.AudioComponentDescriptionNative arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CATransform3D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreAnimation.CATransform3D arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreLocation.CLLocationCoordinate2D arg1, double arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_out_NSEnergyFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, out MonoMac.Foundation.NSEnergyFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_ref_NSLengthFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSLengthFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_ref_NSMassFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSMassFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_UInt32 (System.IntPtr receiver, System.IntPtr selector, double arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_float_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4, bool arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, MonoMac.SceneKit.SCNVector3 arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6, int arg7, int arg8);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, System.IntPtr arg4, int arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_UInt32_UInt32_UInt32_UInt32_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, uint arg2, uint arg3, uint arg4, uint arg5, uint arg6, System.IntPtr arg7);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Int64_Double (System.IntPtr receiver, System.IntPtr selector, long arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_NSRange_ref_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref int arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.Drawing.PointF arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_NSRange_UInt64_IntPtr_int_ref_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, ref System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNMatrix4_SCNMatrix4_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2, MonoMac.SceneKit.SCNMatrix4 arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3, MonoMac.SceneKit.SCNVector3 arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_SCNVector3_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3, System.IntPtr arg4, MonoMac.SceneKit.SCNVector3 arg5, MonoMac.SceneKit.SCNVector3 arg6);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, bool arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_IntPtr_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTime_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioStreamBasicDescription (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioStreamBasicDescription_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioTimeStamp_Double (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioTimeStamp arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector3_SCNVector3_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector4_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_Double_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, bool arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_Double_UInt32_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, uint arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt64_Int64_Double (System.IntPtr receiver, System.IntPtr selector, ulong arg1, long arg2, double arg3);
	public static void NSOperatingSystemVersion_objc_msgSend_stret (out MonoMac.Foundation.NSOperatingSystemVersion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void NSOperatingSystemVersion_objc_msgSendSuper_stret (out MonoMac.Foundation.NSOperatingSystemVersion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void RectangleF_objc_msgSend_stret_SizeF_UInt32 (out System.Drawing.RectangleF retval, System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, uint arg2);
	public static void RectangleF_objc_msgSendSuper_stret_SizeF_UInt32 (out System.Drawing.RectangleF retval, System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, uint arg2);
	public static void SCNMatrix4_objc_msgSend_stret (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNMatrix4_objc_msgSend_stret_SCNMatrix4_IntPtr (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1, System.IntPtr arg2);
	public static void SCNMatrix4_objc_msgSendSuper_stret (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNMatrix4_objc_msgSendSuper_stret_SCNMatrix4_IntPtr (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1, System.IntPtr arg2);
	public static void SCNQuaternion_objc_msgSend_stret (out MonoMac.SceneKit.SCNQuaternion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNQuaternion_objc_msgSendSuper_stret (out MonoMac.SceneKit.SCNQuaternion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNVector3_objc_msgSend_stret_SCNVector3 (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1);
	public static void SCNVector3_objc_msgSend_stret_SCNVector3_IntPtr (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, System.IntPtr arg2);
	public static void SCNVector3_objc_msgSendSuper_stret_SCNVector3 (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1);
	public static void SCNVector3_objc_msgSendSuper_stret_SCNVector3_IntPtr (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, System.IntPtr arg2);
	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_out_Boolean (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, out bool arg4);
	public static uint UInt32_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_out_Boolean (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, out bool arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static ulong UInt64_objc_msgSend_Double (System.IntPtr receiver, System.IntPtr selector, double arg1);
	public static ulong UInt64_objc_msgSendSuper_Double (System.IntPtr receiver, System.IntPtr selector, double arg1);
	public static void Vector3_objc_msgSend_stret (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Vector3_objc_msgSendSuper_stret (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void void_objc_msgSend_AVAudio3DAngularOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DAngularOrientation arg1);
	public static void void_objc_msgSend_AVAudio3DVectorOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DVectorOrientation arg1);
	public static void void_objc_msgSend_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2);
	public static void void_objc_msgSend_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3);
	public static void void_objc_msgSend_byte_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3, byte arg4);
	public static void void_objc_msgSend_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSend_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_Int64_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4);
	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4, long arg5);
	public static void void_objc_msgSend_IntPtr_IntPtr_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_RectangleF_IntPtr_UInt32_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.RectangleF arg2, System.IntPtr arg3, uint arg4, int arg5);
	public static void void_objc_msgSend_IntPtr_ref_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, double arg3);
	public static void void_objc_msgSend_IntPtr_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2);
	public static void void_objc_msgSend_IntPtr_UInt32_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, int arg3);
	public static void void_objc_msgSend_NSEdgeInsets (System.IntPtr receiver, System.IntPtr selector, MonoMac.AppKit.NSEdgeInsets arg1);
	public static void void_objc_msgSend_NSRange_PointF (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.Drawing.PointF arg2);
	public static void void_objc_msgSend_out_Int32_out_Int32_out_Int32_out_Int32_IntPtr (System.IntPtr receiver, System.IntPtr selector, out int arg1, out int arg2, out int arg3, out int arg4, System.IntPtr arg5);
	public static void void_objc_msgSend_out_UInt32_out_UInt32_out_UInt32_NSRange (System.IntPtr receiver, System.IntPtr selector, out uint arg1, out uint arg2, out uint arg3, MonoMac.Foundation.NSRange arg4);
	public static void void_objc_msgSend_RectangleF_IntPtr_IntPtr_int_int (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, int arg5);
	public static void void_objc_msgSend_RectangleF_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_ref_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out float arg2, int arg3);
	public static void void_objc_msgSend_ref_SCNVector3_ref_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.SceneKit.SCNVector3 arg1, ref MonoMac.SceneKit.SCNVector3 arg2);
	public static void void_objc_msgSend_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static void void_objc_msgSend_SCNQuaternion (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNQuaternion arg1);
	public static void void_objc_msgSend_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, bool arg2);
	public static void void_objc_msgSend_SCNVector3_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, bool arg3);
	public static void void_objc_msgSend_SCNVector4_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, bool arg2);
	public static void void_objc_msgSend_UInt16_byte (System.IntPtr receiver, System.IntPtr selector, ushort arg1, byte arg2);
	public static void void_objc_msgSend_UInt32_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static void void_objc_msgSend_UInt32_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_UInt64_Double_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, ulong arg1, double arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_Vector3 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static void void_objc_msgSendSuper_AVAudio3DAngularOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DAngularOrientation arg1);
	public static void void_objc_msgSendSuper_AVAudio3DVectorOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DVectorOrientation arg1);
	public static void void_objc_msgSendSuper_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2);
	public static void void_objc_msgSendSuper_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3);
	public static void void_objc_msgSendSuper_byte_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3, byte arg4);
	public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSendSuper_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_Int64_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4, long arg5);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_RectangleF_IntPtr_UInt32_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.RectangleF arg2, System.IntPtr arg3, uint arg4, int arg5);
	public static void void_objc_msgSendSuper_IntPtr_ref_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, double arg3);
	public static void void_objc_msgSendSuper_IntPtr_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2);
	public static void void_objc_msgSendSuper_IntPtr_UInt32_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, int arg3);
	public static void void_objc_msgSendSuper_NSEdgeInsets (System.IntPtr receiver, System.IntPtr selector, MonoMac.AppKit.NSEdgeInsets arg1);
	public static void void_objc_msgSendSuper_NSRange_PointF (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.Drawing.PointF arg2);
	public static void void_objc_msgSendSuper_out_Int32_out_Int32_out_Int32_out_Int32_IntPtr (System.IntPtr receiver, System.IntPtr selector, out int arg1, out int arg2, out int arg3, out int arg4, System.IntPtr arg5);
	public static void void_objc_msgSendSuper_out_UInt32_out_UInt32_out_UInt32_NSRange (System.IntPtr receiver, System.IntPtr selector, out uint arg1, out uint arg2, out uint arg3, MonoMac.Foundation.NSRange arg4);
	public static void void_objc_msgSendSuper_RectangleF_IntPtr_IntPtr_int_int (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, int arg5);
	public static void void_objc_msgSendSuper_RectangleF_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_ref_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out float arg2, int arg3);
	public static void void_objc_msgSendSuper_ref_SCNVector3_ref_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.SceneKit.SCNVector3 arg1, ref MonoMac.SceneKit.SCNVector3 arg2);
	public static void void_objc_msgSendSuper_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static void void_objc_msgSendSuper_SCNQuaternion (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNQuaternion arg1);
	public static void void_objc_msgSendSuper_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, bool arg2);
	public static void void_objc_msgSendSuper_SCNVector3_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, bool arg3);
	public static void void_objc_msgSendSuper_SCNVector4_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, bool arg2);
	public static void void_objc_msgSendSuper_UInt16_byte (System.IntPtr receiver, System.IntPtr selector, ushort arg1, byte arg2);
	public static void void_objc_msgSendSuper_UInt32_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static void void_objc_msgSendSuper_UInt32_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_UInt64_Double_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, ulong arg1, double arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_Vector3 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static float xamarin_float_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static float xamarin_float_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr_int_int_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, int arg4);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, int arg4, int arg5);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr_int_int_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, int arg4);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, int arg4, int arg5);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3);
```

### Type Changed: MonoMac.ObjCRuntime.Platform

Added values:

```
iOS_2_2 = 131584,
	iOS_3_1 = 196864,
	iOS_8_1 = 524544,
	iOS_8_2 = 524800,
```

### Type Changed: MonoMac.ObjCRuntime.PlatformHelper

Added method:

```
public static bool Is64BitOnlyOnCurrentPlatform (Platform platform);
```

### Type Changed: MonoMac.ObjCRuntime.Runtime

Added methods:

```
public static System.Delegate CreateBlockProxy (System.Reflection.MethodInfo method, System.IntPtr block);
	public static System.Reflection.MethodInfo GetBlockWrapperCreator (System.Reflection.MethodInfo method, int parameter);
	public static T GetINativeObject<T> (System.IntPtr ptr, bool owns);
```

### Type Changed: MonoMac.ObjCRuntime.Selector

Obsoleted constructor:

```
[Obsolete ("Use the (string) constructor.")]
	public Selector (string name, bool alloc);
```

Added interface:

```
INativeObject
```

Removed property:

```
public System.IntPtr Handle { get; }
```

Added property:

```
public virtual System.IntPtr Handle { get; }
```

Removed method:

```
public static int GetFrameLength (System.IntPtr this, System.IntPtr sel);
```

### Removed Type MonoMac.ObjCRuntime.NSObjectMarshaler`1 ### New Type MonoMac.ObjCRuntime.BaseWrapper

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

### Type Changed: MonoMac.OpenGL.GL

Removed property:

```
protected object SyncRoot { get; }
```

### Type Changed: MonoMac.OpenGL.MathHelper

Added fields:

```
public static double DTOR;
	public static float DTORF;
```

### Type Changed: MonoMac.OpenGL.MonoMacGameView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.OpenGL.Quaternion

Added constructor:

```
public Quaternion (ref Matrix3 matrix);
```

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

### New Type MonoMac.OpenGL.Matrix3

```
[Serializable]
public struct Matrix3, System.IEquatable<Matrix3> {
	// constructors
	public Matrix3 (ref Matrix3 matrix);
	public Matrix3 (float r0c0, float r0c1, float r0c2, float r1c0, float r1c1, float r1c2, float r2c0, float r2c1, float r2c2);
	public Matrix3 (float[] floatArray);
	public Matrix3 (Quaterniond quaternion);
	// fields
	public static Matrix3 Identity;
	public float R0C0;
	public float R0C1;
	public float R0C2;
	public float R1C0;
	public float R1C1;
	public float R1C2;
	public float R2C0;
	public float R2C1;
	public float R2C2;
	public static Matrix3 Zero;
	// properties
	public float Determinant { get; }
	public float Item { get; set; }
	public float Item { get; set; }
	// methods
	public static void Add (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public void Add (ref Matrix3 matrix, out Matrix3 result);
	public void Add (ref Matrix3 matrix);
	public static bool Equals (ref Matrix3 left, ref Matrix3 right);
	public virtual bool Equals (Matrix3 matrix);
	public bool Equals (ref Matrix3 matrix);
	public bool EqualsApprox (ref Matrix3 matrix, float tolerance);
	public static bool EqualsApprox (ref Matrix3 left, ref Matrix3 right, float tolerance);
	public override int GetHashCode ();
	public void Multiply (float scalar);
	public void Multiply (ref Matrix3 matrix);
	public void Multiply (float scalar, out Matrix3 result);
	public static void Multiply (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public static void Multiply (ref Matrix3 matrix, float scalar, out Matrix3 result);
	public void Multiply (ref Matrix3 matrix, out Matrix3 result);
	public static System.IntPtr op_Explicit (Matrix3 matrix);
	public static float* op_Explicit (Matrix3 matrix);
	public static float[] op_Explicit (Matrix3 matrix);
	public void Rotate (float angle);
	public void Rotate (float angle, out Matrix3 result);
	public static void Rotate (ref Matrix3 matrix, float angle, out Matrix3 result);
	public static void RotateMatrix (float angle, out Matrix3 result);
	public void Subtract (ref Matrix3 matrix);
	public static void Subtract (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public void Subtract (ref Matrix3 matrix, out Matrix3 result);
	public Quaternion ToQuaternion ();
	public override string ToString ();
	public static void Transform (ref Matrix3 matrix, ref Vector3 vector, out Vector3 result);
	public void Transform (ref Vector3 vector);
	public void Transform (ref Vector3 vector, out Vector3 result);
	public static void Transform (ref Matrix3 matrix, ref Vector3 vector);
	public static void Transpose (ref Matrix3 matrix, out Matrix3 result);
	public void Transpose (out Matrix3 result);
	public void Transpose ();
}
```

### New Type MonoMac.OpenGL.Matrix3d

```
[Serializable]
public struct Matrix3d, System.IEquatable<Matrix3d> {
	// constructors
	public Matrix3d (ref Matrix3d matrix);
	public Matrix3d (double r0c0, double r0c1, double r0c2, double r1c0, double r1c1, double r1c2, double r2c0, double r2c1, double r2c2);
	public Matrix3d (double[] doubleArray);
	public Matrix3d (Quaterniond quaternion);
	// fields
	public static Matrix3d Identity;
	public double R0C0;
	public double R0C1;
	public double R0C2;
	public double R1C0;
	public double R1C1;
	public double R1C2;
	public double R2C0;
	public double R2C1;
	public double R2C2;
	public static Matrix3d Zero;
	// properties
	public double Determinant { get; }
	public double Item { get; set; }
	public double Item { get; set; }
	// methods
	public static void Add (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public void Add (ref Matrix3d matrix, out Matrix3d result);
	public void Add (ref Matrix3d matrix);
	public static bool Equals (ref Matrix3d left, ref Matrix3d right);
	public virtual bool Equals (Matrix3d matrix);
	public bool Equals (ref Matrix3d matrix);
	public bool EqualsApprox (ref Matrix3d matrix, double tolerance);
	public static bool EqualsApprox (ref Matrix3d left, ref Matrix3d right, double tolerance);
	public override int GetHashCode ();
	public void Multiply (double scalar);
	public void Multiply (ref Matrix3d matrix);
	public void Multiply (double scalar, out Matrix3d result);
	public static void Multiply (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public static void Multiply (ref Matrix3d matrix, double scalar, out Matrix3d result);
	public void Multiply (ref Matrix3d matrix, out Matrix3d result);
	public static System.IntPtr op_Explicit (Matrix3d matrix);
	public static double* op_Explicit (Matrix3d matrix);
	public static double[] op_Explicit (Matrix3d matrix);
	public void Rotate (double angle);
	public void Rotate (double angle, out Matrix3d result);
	public static void Rotate (ref Matrix3d matrix, double angle, out Matrix3d result);
	public static void RotateMatrix (double angle, out Matrix3d result);
	public void Subtract (ref Matrix3d matrix);
	public static void Subtract (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public void Subtract (ref Matrix3d matrix, out Matrix3d result);
	public override string ToString ();
	public void Transform (ref Vector3d vector, out Vector3d result);
	public static void Transform (ref Matrix3d matrix, ref Vector3d vector);
	public static void Transform (ref Matrix3d matrix, ref Vector3d vector, out Vector3d result);
	public void Transform (ref Vector3d vector);
	public static void Transpose (ref Matrix3d matrix, out Matrix3d result);
	public void Transpose (out Matrix3d result);
	public void Transpose ();
}
```

## Namespace MonoMac.PdfKit

### Type Changed: MonoMac.PdfKit.PdfAction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfActionGoTo

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfActionNamed

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfActionRemoteGoTo

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfActionResetForm

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfActionUrl

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationButtonWidget

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationChoiceWidget

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationCircle

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationFreeText

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationInk

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationLine

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationLink

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationMarkup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationPopup

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationSquare

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationStamp

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationText

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfAnnotationTextWidget

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfBorder

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfDestination

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfDocument

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfDocumentDelegate

Added interfaces:

```
IPdfDocumentDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfOutline

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfPage

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfSelection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfThumbnailView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.PdfKit.PdfViewDelegate

Added interfaces:

```
IPdfViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.PdfKit.IPdfDocumentDelegate

```
public interface IPdfDocumentDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.PdfKit.IPdfViewDelegate

```
public interface IPdfViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.PdfKit.PdfDocumentDelegate_Extensions

```
public static class PdfDocumentDelegate_Extensions {
	// methods
	public static MonoMac.ObjCRuntime.Class ClassForAnnotationClass (IPdfDocumentDelegate This, MonoMac.ObjCRuntime.Class sender);
	public static void DidMatchString (IPdfDocumentDelegate This, PdfSelection sender);
	public static void FindFinished (IPdfDocumentDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void MatchFound (IPdfDocumentDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void PageFindFinished (IPdfDocumentDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void PageFindStarted (IPdfDocumentDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.PdfKit.PdfViewDelegate_Extensions

```
public static class PdfViewDelegate_Extensions {
	// methods
	public static void OpenPdf (IPdfViewDelegate This, PdfView sender, PdfActionRemoteGoTo action);
	public static void PerformFind (IPdfViewDelegate This, PdfView sender);
	public static void PerformGoToPage (IPdfViewDelegate This, PdfView sender);
	public static void PerformPrint (IPdfViewDelegate This, PdfView sender);
	public static string TitleOfPrintJob (IPdfViewDelegate This, PdfView sender);
	public static float WillChangeScaleFactor (IPdfViewDelegate This, PdfView sender, float scale);
	public static void WillClickOnLink (IPdfViewDelegate This, PdfView sender, MonoMac.Foundation.NSUrl url);
}
```

## Namespace MonoMac.QTKit

### Type Changed: MonoMac.QTKit.QTCaptureAudioPreviewOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureConnection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureDecompressedVideoOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureDecompressedVideoOutputDelegate

Added interfaces:

```
IQTCaptureDecompressedVideoOutputDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureDevice

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureDeviceInput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureFileOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureFileOutputDelegate

Added interfaces:

```
IQTCaptureFileOutputDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureInput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureMovieFileOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureOutput

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureSession

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCaptureViewDelegate

Added interfaces:

```
IQTCaptureViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTCompressionOptions

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTDataReference

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTFormatDescription

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTMedia

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTMovie

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTMovieLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTMovieView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTMovieViewDelegate

Added interfaces:

```
IQTMovieViewDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTSampleBuffer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QTKit.QTTrack

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.QTKit.IQTCaptureDecompressedVideoOutputDelegate

```
public interface IQTCaptureDecompressedVideoOutputDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.QTKit.IQTCaptureFileOutputDelegate

```
public interface IQTCaptureFileOutputDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.QTKit.IQTCaptureViewDelegate

```
public interface IQTCaptureViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.QTKit.IQTMovieViewDelegate

```
public interface IQTMovieViewDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.QTKit.QTCaptureDecompressedVideoOutputDelegate_Extensions

```
public static class QTCaptureDecompressedVideoOutputDelegate_Extensions {
	// methods
	public static void DidDropVideoFrame (IQTCaptureDecompressedVideoOutputDelegate This, QTCaptureOutput captureOutput, QTSampleBuffer sampleBuffer, QTCaptureConnection connection);
	public static void DidOutputVideoFrame (IQTCaptureDecompressedVideoOutputDelegate This, QTCaptureOutput captureOutput, MonoMac.CoreVideo.CVImageBuffer videoFrame, QTSampleBuffer sampleBuffer, QTCaptureConnection connection);
}
```

### New Type MonoMac.QTKit.QTCaptureFileOutputDelegate_Extensions

```
public static class QTCaptureFileOutputDelegate_Extensions {
	// methods
	public static void DidFinishRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileURL, QTCaptureConnection[] connections, MonoMac.Foundation.NSError reason);
	public static void DidOutputSampleBuffer (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, QTSampleBuffer sampleBuffer, QTCaptureConnection connection);
	public static void DidPauseRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl fileUrl, QTCaptureConnection[] connections);
	public static void DidResumeRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl fileUrl, QTCaptureConnection[] connections);
	public static void DidStartRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl fileUrl, QTCaptureConnection[] connections);
	public static void MustChangeOutputFile (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileURL, QTCaptureConnection[] connections, MonoMac.Foundation.NSError reason);
	public static bool ShouldChangeOutputFile (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileURL, QTCaptureConnection[] connections, MonoMac.Foundation.NSError reason);
	public static void WillFinishRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileURL, QTCaptureConnection[] connections, MonoMac.Foundation.NSError reason);
	public static void WillStartRecording (IQTCaptureFileOutputDelegate This, QTCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl fileUrl, QTCaptureConnection[] connections);
}
```

### New Type MonoMac.QTKit.QTCaptureViewDelegate_Extensions

```
public static class QTCaptureViewDelegate_Extensions {
	// methods
	public static MonoMac.CoreImage.CIImage WillDisplayImage (IQTCaptureViewDelegate This, QTCaptureView view, MonoMac.CoreImage.CIImage image);
}
```

### New Type MonoMac.QTKit.QTMovieViewDelegate_Extensions

```
public static class QTMovieViewDelegate_Extensions {
	// methods
	public static MonoMac.CoreImage.CIImage ViewWillDisplayImage (IQTMovieViewDelegate This, QTMovieView view, MonoMac.CoreImage.CIImage image);
}
```

## Namespace MonoMac.QuartzComposer

### Type Changed: MonoMac.QuartzComposer.QCComposition

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QuartzComposer.QCCompositionLayer

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.QuartzComposer.QCCompositionRepository

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

## Namespace MonoMac.SceneKit

### Type Changed: MonoMac.SceneKit.SCNAnimationEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNBox

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNCamera

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ProjectionTransform { get; set; }
```

Added properties:

```
public virtual float Aperture { get; set; }
	public virtual bool AutomaticallyAdjustsZRange { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float FocalBlurRadius { get; set; }
	public virtual float FocalDistance { get; set; }
	public virtual float FocalSize { get; set; }
	public virtual double OrthographicScale { get; set; }
	public virtual SCNMatrix4 ProjectionTransform { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNCapsule

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNCone

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNConstraint

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual float InfluenceFactor { get; set; }
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNCylinder

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNFloor

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

Added property:

```
public virtual float ReflectionResolutionScaleFactor { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNGeometry

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual SCNGeometryElement EdgeCreasesElement { get; set; }
	public virtual SCNGeometrySource EdgeCreasesSource { get; set; }
	public virtual SCNLevelOfDetail[] LevelsOfDetail { get; set; }
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual uint SubdivisionLevel { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public static SCNGeometry Create ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
	public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoMac.SceneKit.SCNGeometryElement

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNGeometrySource

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public static SCNGeometrySource FromData (MonoMac.Foundation.NSData data, SCNGeometrySourceSemantics geometrySourceSemantic, int vectorCount, bool floatComponents, int componentsPerVector, int bytesPerComponent, int offset, int stride);
```

### Type Changed: MonoMac.SceneKit.SCNGeometrySourceSemantic

Added properties:

```
public static MonoMac.Foundation.NSString BoneIndices { get; }
	public static MonoMac.Foundation.NSString BoneWeights { get; }
	public static MonoMac.Foundation.NSString EdgeCrease { get; }
	public static MonoMac.Foundation.NSString VertexCrease { get; }
```

### Type Changed: MonoMac.SceneKit.SCNHitTest

Added property:

```
public static MonoMac.Foundation.NSString IgnoreHiddenNodesKey { get; }
```

### Type Changed: MonoMac.SceneKit.SCNHitTestResult

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ModelTransform { get; }
```

Added property:

```
public virtual SCNMatrix4 ModelTransform { get; }
```

### Type Changed: MonoMac.SceneKit.SCNLayer

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNLevelOfDetail

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNLight

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual string LightType { get; set; }
```

Added properties:

```
public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationFalloffExponent { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual SCNMaterialProperty Gobo { get; }
	public virtual MonoMac.Foundation.NSString LightType { get; set; }
	public virtual float OrthographicScale { get; set; }
	public virtual float ShadowBias { get; set; }
	public virtual System.Drawing.SizeF ShadowMapSize { get; set; }
	public virtual SCNShadowMode ShadowMode { get; set; }
	public virtual uint ShadowSampleCount { get; set; }
	public virtual float SpotInnerAngle { get; set; }
	public virtual float SpotOuterAngle { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual float ZFar { get; set; }
	public virtual float ZNear { get; set; }
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNLookAtConstraint

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNMaterial

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual float FresnelExponent { get; set; }
	public virtual bool ReadsFromDepthBuffer { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNMaterialProperty

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ContentsTransform { get; set; }
```

Added properties:

```
public MonoMac.AppKit.NSColor ContentColor { get; set; }
	public MonoMac.AppKit.NSImage ContentImage { get; set; }
	public MonoMac.AppKit.NSImage[] ContentImageCube { get; set; }
	public MonoMac.CoreAnimation.CALayer ContentLayer { get; set; }
	public MonoMac.Foundation.NSString ContentPath { get; set; }
	public virtual SCNMatrix4 ContentsTransform { get; set; }
	public MonoMac.Foundation.NSUrl ContentUrl { get; set; }
	public virtual float Intensity { get; set; }
	public virtual float MaxAnisotropy { get; set; }
```

Added methods:

```
public static SCNMaterialProperty Create (MonoMac.Foundation.NSObject contents);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNMorpher

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNNode

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNActionable
	ISCNAnimatable
	ISCNBoundingVolume
	MonoMac.Foundation.INSObjectProtocol
```

Removed properties:

```
public virtual MonoMac.CoreAnimation.CATransform3D Pivot { get; set; }
	public virtual MonoMac.CoreAnimation.CATransform3D Transform { get; set; }
	public virtual MonoMac.CoreAnimation.CATransform3D WorldTransform { get; }
```

Added properties:

```
public virtual bool CastsShadow { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual SCNConstraint[] Constraints { get; set; }
	public virtual SCNVector3 EulerAngles { get; set; }
	public virtual MonoMac.CoreImage.CIFilter[] Filters { get; set; }
	public virtual SCNMorpher Morpher { get; set; }
	public virtual SCNQuaternion Orientation { get; set; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsBody PhysicsBody { get; set; }
	public virtual SCNPhysicsField PhysicsField { get; set; }
	public virtual SCNMatrix4 Pivot { get; set; }
	public virtual SCNSkinner Skinner { get; set; }
	public virtual SCNMatrix4 Transform { get; set; }
	public virtual SCNMatrix4 WorldTransform { get; }
```

Removed method:

```
public virtual SCNNode FindNodes (SCNNodePredicate predicate);
```

Added methods:

```
public void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, string key);
	public void AddNodes (SCNNode[] nodes);
	public virtual void AddParticleSystem (SCNParticleSystem system);
	public virtual SCNVector3 ConvertPositionFromNode (SCNVector3 position, SCNNode node);
	public virtual SCNVector3 ConvertPositionToNode (SCNVector3 position, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformFromNode (SCNMatrix4 transform, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformToNode (SCNMatrix4 transform, SCNNode node);
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);
	public virtual SCNNode[] FindNodes (SCNNodePredicate predicate);
	public virtual SCNNode FlattenedClone ();
	public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, SCNHitTestOptions options);
	public virtual SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, MonoMac.Foundation.NSDictionary options);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoMac.SceneKit.SCNNodeRendererDelegate

Added interfaces:

```
ISCNNodeRendererDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNPlane

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual float CornerRadius { get; set; }
	public virtual int CornerSegmentCount { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNProgram

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public static MonoMac.Foundation.NSString MappingChannelKey { get; }
	public virtual bool Opaque { get; set; }
```

Added method:

```
public void SetSemantic (MonoMac.Foundation.NSString geometrySourceSemantic, string symbol, SCNProgramSemanticOptions options);
```

### Type Changed: MonoMac.SceneKit.SCNProgramDelegate

Added interfaces:

```
ISCNProgramDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNPyramid

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNRenderer

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual double NextFrameTimeInSeconds { get; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual void Render (double timeInSeconds);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNScene

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual SCNMaterialProperty Background { get; }
	public static MonoMac.Foundation.NSString EndTimeAttributeKey { get; }
	public virtual MonoMac.Foundation.NSObject FogColor { get; set; }
	public virtual float FogDensityExponent { get; set; }
	public virtual float FogEndDistance { get; set; }
	public virtual float FogStartDistance { get; set; }
	public static MonoMac.Foundation.NSString FrameRateAttributeKey { get; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsWorld PhysicsWorld { get; }
	public static MonoMac.Foundation.NSString StartTimeAttributeKey { get; }
	public static MonoMac.Foundation.NSString UpAxisAttributeKey { get; }
```

Added methods:

```
public virtual void AddParticleSystem (SCNParticleSystem system, SCNMatrix4 transform);
	public static SCNScene FromFile (string name, string directory, SCNSceneLoadingOptions options);
	public static SCNScene FromFile (string name, string directory, MonoMac.Foundation.NSDictionary options);
	public static SCNScene FromFile (string name);
	public static SCNScene FromUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options, out MonoMac.Foundation.NSError error);
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual bool WriteToUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
	public bool WriteToUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
```

### Type Changed: MonoMac.SceneKit.SCNSceneRendererDelegate

Added interfaces:

```
ISCNSceneRendererDelegate
	MonoMac.Foundation.INSObjectProtocol
```

Removed methods:

```
public virtual void DidRenderScene (MonoMac.Foundation.NSObject renderer, SCNScene scene, double time);
	public virtual void WillRenderScene (MonoMac.Foundation.NSObject renderer, SCNScene scene, double time);
```

Added methods:

```
public virtual void DidApplyAnimations (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

### Type Changed: MonoMac.SceneKit.SCNSceneSource

Added constructors:

```
public SCNSceneSource (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNSceneSource (MonoMac.Foundation.NSData data, SCNSceneLoadingOptions options);
```

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed method:

```
public static MonoMac.Foundation.NSObject FromData (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options);
```

Added methods:

```
public virtual MonoMac.Foundation.NSObject[] EntriesPassingTest (SCNSceneSourceFilter predicate);
	public static SCNSceneSource FromData (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options);
	public static SCNSceneSource FromData (MonoMac.Foundation.NSData data, SCNSceneLoadingOptions options);
	public SCNSceneSource FromUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public MonoMac.Foundation.NSObject GetEntryWithIdentifier<T> (string uid);
	public string[] GetIdentifiersOfEntries<T> ();
	public SCNScene SceneFromOptions (SCNSceneLoadingOptions options, SCNSceneSourceStatusHandler statusHandler);
	public SCNScene SceneWithOption (SCNSceneLoadingOptions options, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.SceneKit.SCNSceneSourceLoading

Added properties:

```
public static MonoMac.Foundation.NSString AnimationImportPolicyDoNotPlay { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyKey { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlay { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlayRepeatedly { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlayUsingSceneTimeBase { get; }
	public static MonoMac.Foundation.NSString AssetDirectoryUrlsKey { get; }
	public static MonoMac.Foundation.NSString ConvertToYUpKey { get; }
	public static MonoMac.Foundation.NSString ConvertUnitsToMetersKey { get; }
	public static MonoMac.Foundation.NSString OverrideAssetUrlsKey { get; }
```

### Type Changed: MonoMac.SceneKit.SCNShaderModifiers

Added constructors:

```
public SCNShaderModifiers ();
	public SCNShaderModifiers (MonoMac.Foundation.NSDictionary dictionary);
```

Removed properties:

```
public static MonoMac.Foundation.NSString EntryPointFragment { get; }
	public static MonoMac.Foundation.NSString EntryPointGeometry { get; }
	public static MonoMac.Foundation.NSString EntryPointLightingModel { get; }
	public static MonoMac.Foundation.NSString EntryPointSurface { get; }
```

Added properties:

```
public string EntryPointFragment { get; set; }
	public string EntryPointGeometry { get; set; }
	public string EntryPointLightingModel { get; set; }
	public string EntryPointSurface { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNShape

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNSkinner

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual SCNGeometry BaseGeometry { get; set; }
	public virtual SCNMatrix4 BaseGeometryBindTransform { get; set; }
	public virtual SCNGeometrySource BoneIndices { get; }
	public SCNMatrix4[] BoneInverseBindTransforms { get; }
	public virtual SCNNode[] Bones { get; }
	public virtual SCNGeometrySource BoneWeights { get; }
```

Added method:

```
public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, SCNMatrix4[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
```

### Type Changed: MonoMac.SceneKit.SCNSphere

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNText

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual MonoMac.AppKit.NSBezierPath ChamferProfile { get; set; }
	public virtual float Flatness { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNTorus

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNTransaction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNTransformConstraint

Removed constructor:

```
public SCNTransformConstraint ();
```

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNTransformConstraintHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform, System.AsyncCallback callback, object object);
	public virtual MonoMac.CoreAnimation.CATransform3D EndInvoke (System.IAsyncResult result);
	public virtual MonoMac.CoreAnimation.CATransform3D Invoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, SCNMatrix4 transform, System.AsyncCallback callback, object object);
	public virtual SCNMatrix4 EndInvoke (System.IAsyncResult result);
	public virtual SCNMatrix4 Invoke (SCNNode node, SCNMatrix4 transform);
```

### Type Changed: MonoMac.SceneKit.SCNTube

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.SceneKit.SCNVector3

Removed constructor:

```
public SCNVector3 (MonoMac.OpenGL.Vector3 vector);
```

Added constructors:

```
public SCNVector3 (MonoMac.OpenGL.Vector3 v);
	public SCNVector3 (SCNVector3 v);
	public SCNVector3 (SCNVector4 v);
```

Added interface:

```
System.IEquatable<SCNVector3>
```

Added fields:

```
public static SCNVector3 One;
	public static int SizeInBytes;
	public static SCNVector3 UnitX;
	public static SCNVector3 UnitY;
	public static SCNVector3 UnitZ;
	public static SCNVector3 Zero;
```

Added properties:

```
public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public MonoMac.OpenGL.Vector2 Xy { get; set; }
```

Added methods:

```
[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector3 right);
	public static void Add (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Add (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector3 right);
	public static SCNVector3 BaryCentric (SCNVector3 a, SCNVector3 b, SCNVector3 c, float u, float v);
	public static void BaryCentric (ref SCNVector3 a, ref SCNVector3 b, ref SCNVector3 c, float u, float v, out SCNVector3 result);
	public static float CalculateAngle (SCNVector3 first, SCNVector3 second);
	public static void CalculateAngle (ref SCNVector3 first, ref SCNVector3 second, out float result);
	public static void Clamp (ref SCNVector3 vec, ref SCNVector3 min, ref SCNVector3 max, out SCNVector3 result);
	public static SCNVector3 Clamp (SCNVector3 vec, SCNVector3 min, SCNVector3 max);
	public static SCNVector3 ComponentMax (SCNVector3 a, SCNVector3 b);
	public static void ComponentMax (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 ComponentMin (SCNVector3 a, SCNVector3 b);
	public static void ComponentMin (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Cross (SCNVector3 left, SCNVector3 right);
	public static void Cross (ref SCNVector3 left, ref SCNVector3 right, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static void Div (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static SCNVector3 Div (SCNVector3 a, float f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);
	public static SCNVector3 Divide (SCNVector3 vector, float scale);
	public static void Divide (ref SCNVector3 vector, float scale, out SCNVector3 result);
	public static SCNVector3 Divide (SCNVector3 vector, SCNVector3 scale);
	public static void Divide (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static float Dot (SCNVector3 left, SCNVector3 right);
	public static void Dot (ref SCNVector3 left, ref SCNVector3 right, out float result);
	public virtual bool Equals (SCNVector3 other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static SCNVector3 Lerp (SCNVector3 a, SCNVector3 b, float blend);
	public static void Lerp (ref SCNVector3 a, ref SCNVector3 b, float blend, out SCNVector3 result);
	public static SCNVector3 Max (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 Min (SCNVector3 left, SCNVector3 right);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public static void Mult (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public static SCNVector3 Mult (SCNVector3 a, float f);
	public static SCNVector3 Multiply (SCNVector3 vector, SCNVector3 scale);
	public static SCNVector3 Multiply (SCNVector3 vector, float scale);
	public static void Multiply (ref SCNVector3 vector, float scale, out SCNVector3 result);
	public static void Multiply (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static SCNVector3 Normalize (SCNVector3 vec);
	public static void Normalize (ref SCNVector3 vec, out SCNVector3 result);
	public void Normalize ();
	public void NormalizeFast ();
	public static SCNVector3 NormalizeFast (SCNVector3 vec);
	public static void NormalizeFast (ref SCNVector3 vec, out SCNVector3 result);
	public static SCNVector3 op_Addition (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Division (SCNVector3 vec, float scale);
	public static bool op_Equality (SCNVector3 left, SCNVector3 right);
	public static bool op_Inequality (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Multiply (SCNVector3 vec, float scale);
	public static SCNVector3 op_Multiply (float scale, SCNVector3 vec);
	public static SCNVector3 op_Subtraction (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_UnaryNegation (SCNVector3 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector3 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector3 scale);

	[Obsolete ("Use static Subtract() method instead.")]
	public static void Sub (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);

	[Obsolete ("Use static Subtract() method instead.")]
	public static SCNVector3 Sub (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector3 right);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector3 right);
	public static void Subtract (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Subtract (SCNVector3 a, SCNVector3 b);
	public override string ToString ();
	public static void Transform (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector4 result);
	public static SCNVector4 Transform (SCNVector3 vec, SCNMatrix4 mat);
	public static SCNVector3 TransformNormal (SCNVector3 norm, SCNMatrix4 mat);
	public static void TransformNormal (ref SCNVector3 norm, ref SCNMatrix4 mat, out SCNVector3 result);
	public static void TransformNormalInverse (ref SCNVector3 norm, ref SCNMatrix4 invMat, out SCNVector3 result);
	public static SCNVector3 TransformNormalInverse (SCNVector3 norm, SCNMatrix4 invMat);
	public static void TransformPerspective (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector3 result);
	public static SCNVector3 TransformPerspective (SCNVector3 vec, SCNMatrix4 mat);
	public static SCNVector3 TransformPosition (SCNVector3 pos, SCNMatrix4 mat);
	public static void TransformPosition (ref SCNVector3 pos, ref SCNMatrix4 mat, out SCNVector3 result);
	public static void TransformVector (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector3 result);
	public static SCNVector3 TransformVector (SCNVector3 vec, SCNMatrix4 mat);
```

### Type Changed: MonoMac.SceneKit.SCNVector4

Removed constructor:

```
public SCNVector4 (MonoMac.OpenGL.Vector4 vector);
```

Added constructors:

```
public SCNVector4 (MonoMac.OpenGL.Vector2 v);
	public SCNVector4 (SCNVector3 v);
	public SCNVector4 (MonoMac.OpenGL.Vector3 v);
	public SCNVector4 (MonoMac.OpenGL.Vector4 v);
	public SCNVector4 (SCNVector3 v, float w);
	public SCNVector4 (SCNVector4 v);
```

Added interface:

```
System.IEquatable<SCNVector4>
```

Added fields:

```
public static SCNVector4 One;
	public static int SizeInBytes;
	public static SCNVector4 UnitW;
	public static SCNVector4 UnitX;
	public static SCNVector4 UnitY;
	public static SCNVector4 UnitZ;
	public static SCNVector4 Zero;
```

Added properties:

```
public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public MonoMac.OpenGL.Vector2 Xy { get; set; }
	public SCNVector3 Xyz { get; set; }
```

Added methods:

```
[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector4 right);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector4 right);
	public static void Add (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Add (SCNVector4 a, SCNVector4 b);
	public static SCNVector4 BaryCentric (SCNVector4 a, SCNVector4 b, SCNVector4 c, float u, float v);
	public static void BaryCentric (ref SCNVector4 a, ref SCNVector4 b, ref SCNVector4 c, float u, float v, out SCNVector4 result);
	public static void Clamp (ref SCNVector4 vec, ref SCNVector4 min, ref SCNVector4 max, out SCNVector4 result);
	public static SCNVector4 Clamp (SCNVector4 vec, SCNVector4 min, SCNVector4 max);
	public static void Div (ref SCNVector4 a, float f, out SCNVector4 result);
	public static SCNVector4 Div (SCNVector4 a, float f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);
	public static SCNVector4 Divide (SCNVector4 vector, SCNVector4 scale);
	public static void Divide (ref SCNVector4 vector, float scale, out SCNVector4 result);
	public static void Divide (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Divide (SCNVector4 vector, float scale);
	public static float Dot (SCNVector4 left, SCNVector4 right);
	public static void Dot (ref SCNVector4 left, ref SCNVector4 right, out float result);
	public override bool Equals (object obj);
	public virtual bool Equals (SCNVector4 other);
	public override int GetHashCode ();
	public static void Lerp (ref SCNVector4 a, ref SCNVector4 b, float blend, out SCNVector4 result);
	public static SCNVector4 Lerp (SCNVector4 a, SCNVector4 b, float blend);
	public static SCNVector4 Max (SCNVector4 a, SCNVector4 b);
	public static void Max (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static void Min (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Min (SCNVector4 a, SCNVector4 b);
	public static SCNVector4 Mult (SCNVector4 a, float f);
	public static void Mult (ref SCNVector4 a, float f, out SCNVector4 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);
	public static void Multiply (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, SCNVector4 scale);
	public static void Multiply (ref SCNVector4 vector, float scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, float scale);
	public void Normalize ();
	public static SCNVector4 Normalize (SCNVector4 vec);
	public static void Normalize (ref SCNVector4 vec, out SCNVector4 result);
	public void NormalizeFast ();
	public static void NormalizeFast (ref SCNVector4 vec, out SCNVector4 result);
	public static SCNVector4 NormalizeFast (SCNVector4 vec);
	public static SCNVector4 op_Addition (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Division (SCNVector4 vec, float scale);
	public static bool op_Equality (SCNVector4 left, SCNVector4 right);
	public static float* op_Explicit (SCNVector4 v);
	public static System.IntPtr op_Explicit (SCNVector4 v);
	public static bool op_Inequality (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Multiply (float scale, SCNVector4 vec);
	public static SCNVector4 op_Multiply (SCNVector4 vec, float scale);
	public static SCNVector4 op_Subtraction (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_UnaryNegation (SCNVector4 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz, float sw);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector4 right);
	public static SCNVector4 Sub (SCNVector4 a, SCNVector4 b);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector4 right);
	public static void Sub (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static void Subtract (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Subtract (SCNVector4 a, SCNVector4 b);
	public override string ToString ();
	public static void Transform (ref SCNVector4 vec, ref SCNMatrix4 mat, out SCNVector4 result);
	public static SCNVector4 Transform (SCNVector4 vec, SCNMatrix4 mat);
```

### Type Changed: MonoMac.SceneKit.SCNView

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
	MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

Added properties:

```
public virtual SCNAntialiasingMode AntialiasingMode { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual MonoMac.AppKit.NSImage Snapshot ();
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNWrapMode

Removed values:

```
Clamp = 0,
	ClampToBorder = 2,
	Mirror = 3,
	Repeat = 1,
```

Added values:

```
Clamp = 1,
	ClampToBorder = 3,
	Mirror = 4,
	Repeat = 2,
```

### New Type MonoMac.SceneKit._SCNShaderModifiers

```
public static class _SCNShaderModifiers {
}
```

### New Type MonoMac.SceneKit.ISCNActionable

```
public interface ISCNActionable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNAnimatable

```
public interface ISCNAnimatable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNBoundingVolume

```
public interface ISCNBoundingVolume : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
}
```

### New Type MonoMac.SceneKit.ISCNNodeRendererDelegate

```
public interface ISCNNodeRendererDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNPhysicsContactDelegate

```
public interface ISCNPhysicsContactDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNProgramDelegate

```
public interface ISCNProgramDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNSceneExportDelegate

```
public interface ISCNSceneExportDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNSceneRenderer

```
public interface ISCNSceneRenderer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
}
```

### New Type MonoMac.SceneKit.ISCNSceneRendererDelegate

```
public interface ISCNSceneRendererDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNShadable

```
public interface ISCNShadable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNTechniqueSupport

```
public interface ISCNTechniqueSupport : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNAction

```
public class SCNAction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNAction ();
	public SCNAction (MonoMac.Foundation.NSCoder coder);
	public SCNAction (MonoMac.Foundation.NSObjectFlag t);
	public SCNAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DurationInSeconds { get; set; }
	public virtual float Speed { get; set; }
	public virtual SCNActionTimingMode TimingMode { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNAction CustomAction (double seconds, SCNActionNodeWithElapsedTimeHandler handler);
	public static SCNAction FadeIn (double durationInSeconds);
	public static SCNAction FadeOpacityBy (float factor, double durationInSeconds);
	public static SCNAction FadeOpacityTo (float opacity, double durationInSeconds);
	public static SCNAction FadeOut (double durationInSeconds);
	public static SCNAction FromJavascript (string script, double seconds);
	public static SCNAction Group (SCNAction[] actions);
	public static SCNAction MoveBy (SCNVector3 delta, double durationInSeconds);
	public static SCNAction MoveBy (float deltaX, float deltaY, float deltaZ, double durationInSeconds);
	public static SCNAction MoveTo (SCNVector3 location, double durationInSeconds);
	public static SCNAction RemoveFromParentNode ();
	public static SCNAction RepeatAction (SCNAction action, uint count);
	public static SCNAction RepeatActionForever (SCNAction action);
	public virtual SCNAction ReversedAction ();
	public static SCNAction RotateBy (float angle, SCNVector3 axis, double durationInSeconds);
	public static SCNAction RotateBy (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds, bool shortestUnitArc);
	public static SCNAction RotateTo (SCNVector4 axisAngle, double durationInSeconds);
	public static SCNAction Run (System.Action<SCNNode> handler, MonoMac.CoreFoundation.DispatchQueue queue);
	public static SCNAction Run (System.Action<SCNNode> handler);
	public static SCNAction ScaleBy (float scale, double durationInSeconds);
	public static SCNAction ScaleTo (float scale, double durationInSeconds);
	public static SCNAction Sequence (SCNAction[] actions);
	public virtual void SetTimingFunction (System.Action<float> timingFunction);
	public static SCNAction Wait (double durationInSeconds);
	public static SCNAction Wait (double durationInSeconds, double durationRange);
}
```

### New Type MonoMac.SceneKit.SCNActionable

```
public class SCNActionable : MonoMac.Foundation.NSObject, ISCNActionable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNActionable ();
	public SCNActionable (MonoMac.Foundation.NSCoder coder);
	public SCNActionable (MonoMac.Foundation.NSObjectFlag t);
	public SCNActionable (System.IntPtr handle);
	// methods
	public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
}
```

### New Type MonoMac.SceneKit.SCNActionable_Extensions

```
public static class SCNActionable_Extensions {
	// methods
	public static SCNAction GetAction (ISCNActionable This, string key);
	public static bool HasActions (ISCNActionable This);
	public static void RemoveAction (ISCNActionable This, string key);
	public static void RemoveAllActions (ISCNActionable This);
	public static void RunAction (ISCNActionable This, SCNAction action);
	public static void RunAction (ISCNActionable This, SCNAction action, string key);
	public static void RunAction (ISCNActionable This, SCNAction action, System.Action block);
	public static void RunAction (ISCNActionable This, SCNAction action, string key, System.Action block);
}
```

### New Type MonoMac.SceneKit.SCNActionNodeWithElapsedTimeHandler

```
public sealed delegate SCNActionNodeWithElapsedTimeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNActionNodeWithElapsedTimeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, float elapsedTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (SCNNode node, float elapsedTime);
}
```

### New Type MonoMac.SceneKit.SCNActionTimingMode

```
[Serializable]
public enum SCNActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type MonoMac.SceneKit.SCNAnimatable

```
public class SCNAnimatable : MonoMac.Foundation.NSObject, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNAnimatable ();
	public SCNAnimatable (MonoMac.Foundation.NSCoder coder);
	public SCNAnimatable (MonoMac.Foundation.NSObjectFlag t);
	public SCNAnimatable (System.IntPtr handle);
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, string key);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNAnimatable_Extensions

```
public static class SCNAnimatable_Extensions {
	// methods
	public static void AddAnimation (ISCNAnimatable This, MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public static MonoMac.CoreAnimation.CAAnimation GetAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static MonoMac.Foundation.NSString[] GetAnimationKeys (ISCNAnimatable This);
	public static bool IsAnimationPaused (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void PauseAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void RemoveAllAnimations (ISCNAnimatable This);
	public static void RemoveAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void RemoveAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key, float duration);
	public static void ResumeAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNAnimationImportPolicy

```
[Serializable]
public enum SCNAnimationImportPolicy {
	DoNotPlay = 3,
	Play = 1,
	PlayRepeatedly = 2,
	PlayUsingSceneTimeBase = 4,
	Unknown = 0,
}
```

### New Type MonoMac.SceneKit.SCNAntialiasingMode

```
[Serializable]
public enum SCNAntialiasingMode {
	Multisampling16X = 4,
	Multisampling2X = 1,
	Multisampling4X = 2,
	Multisampling8X = 3,
	None = 0,
}
```

### New Type MonoMac.SceneKit.SCNBindingHandler

```
public sealed delegate SCNBindingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNBindingHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint programId, uint location, SCNNode renderedNode, SCNRenderer renderer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (uint programId, uint location, SCNNode renderedNode, SCNRenderer renderer);
}
```

### New Type MonoMac.SceneKit.SCNBoundingVolume

```
public abstract class SCNBoundingVolume : MonoMac.Foundation.NSObject, ISCNBoundingVolume, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNBoundingVolume ();
	public SCNBoundingVolume (MonoMac.Foundation.NSCoder coder);
	public SCNBoundingVolume (MonoMac.Foundation.NSObjectFlag t);
	public SCNBoundingVolume (System.IntPtr handle);
	// methods
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
	public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
}
```

### New Type MonoMac.SceneKit.SCNBoundingVolume_Extensions

```
public static class SCNBoundingVolume_Extensions {
	// methods
	public static bool GetBoundingBox (ISCNBoundingVolume This, ref SCNVector3 min, ref SCNVector3 max);
	public static bool GetBoundingSphere (ISCNBoundingVolume This, ref SCNVector3 center, ref float radius);
}
```

### New Type MonoMac.SceneKit.SCNFieldForceEvaluator

```
public sealed delegate SCNFieldForceEvaluator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNFieldForceEvaluator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNVector3 position, SCNVector3 velocity, float mass, float charge, double timeInSeconds, System.AsyncCallback callback, object object);
	public virtual SCNVector3 EndInvoke (System.IAsyncResult result);
	public virtual SCNVector3 Invoke (SCNVector3 position, SCNVector3 velocity, float mass, float charge, double timeInSeconds);
}
```

### New Type MonoMac.SceneKit.SCNGeometrySourceSemantics

```
[Serializable]
public enum SCNGeometrySourceSemantics {
	BoneIndices = 7,
	BoneWeights = 6,
	Color = 2,
	EdgeCrease = 5,
	Normal = 1,
	Texcoord = 3,
	Vertex = 0,
	VertexCrease = 4,
}
```

### New Type MonoMac.SceneKit.SCNHitTestOptions

```
public class SCNHitTestOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNHitTestOptions ();
	public SCNHitTestOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? BackFaceCulling { get; set; }
	public bool? BoundingBoxOnly { get; set; }
	public bool? FirstFoundOnly { get; set; }
	public bool? IgnoreChildNodes { get; set; }
	public bool? IgnoreHiddenNodes { get; set; }
	public SCNNode RootNode { get; set; }
	public bool? SortResults { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNIKConstraint

```
public class SCNIKConstraint : MonoMac.SceneKit.SCNConstraint, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNIKConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNIKConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SCNIKConstraint (System.IntPtr handle);
	// properties
	public virtual SCNNode ChainRootNode { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 TargetPosition { get; set; }
	// methods
	public static SCNIKConstraint Create (SCNNode chainRootNode);
	protected override void Dispose (bool disposing);
	public virtual float GetMaxAllowedRotationAngle (SCNNode node);
	public virtual void SetMaxAllowedRotationAnglet (float angle, SCNNode node);
}
```

### New Type MonoMac.SceneKit.SCNMatrix4

```
[Serializable]
public struct SCNMatrix4, System.IEquatable<SCNMatrix4> {
	// constructors
	public SCNMatrix4 (SCNVector4 row0, SCNVector4 row1, SCNVector4 row2, SCNVector4 row3);
	public SCNMatrix4 (float m00, float m01, float m02, float m03, float m10, float m11, float m12, float m13, float m20, float m21, float m22, float m23, float m30, float m31, float m32, float m33);
	public SCNMatrix4 (MonoMac.CoreAnimation.CATransform3D transform);
	// fields
	public static SCNMatrix4 Identity;
	public SCNVector4 Row0;
	public SCNVector4 Row1;
	public SCNVector4 Row2;
	public SCNVector4 Row3;
	// properties
	public SCNVector4 Column0 { get; }
	public SCNVector4 Column1 { get; }
	public SCNVector4 Column2 { get; }
	public SCNVector4 Column3 { get; }
	public float Determinant { get; }
	public float M11 { get; set; }
	public float M12 { get; set; }
	public float M13 { get; set; }
	public float M14 { get; set; }
	public float M21 { get; set; }
	public float M22 { get; set; }
	public float M23 { get; set; }
	public float M24 { get; set; }
	public float M31 { get; set; }
	public float M32 { get; set; }
	public float M33 { get; set; }
	public float M34 { get; set; }
	public float M41 { get; set; }
	public float M42 { get; set; }
	public float M43 { get; set; }
	public float M44 { get; set; }
	// methods
	public static void CreateFromAxisAngle (MonoMac.OpenGL.Vector3d axis, double angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateFromAxisAngle (SCNVector3 axis, float angle);
	public static void CreateFromAxisAngle (SCNVector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateFromAxisAngle (MonoMac.OpenGL.Vector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateOrthographic (float width, float height, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographic (float width, float height, float zNear, float zFar);
	public static void CreateOrthographicOffCenter (float left, float right, float bottom, float top, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographicOffCenter (float left, float right, float bottom, float top, float zNear, float zFar);
	public static void CreatePerspectiveFieldOfView (float fovy, float aspect, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveFieldOfView (float fovy, float aspect, float zNear, float zFar);
	public static void CreatePerspectiveOffCenter (float left, float right, float bottom, float top, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveOffCenter (float left, float right, float bottom, float top, float zNear, float zFar);
	public static void CreateRotationX (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationX (float angle);
	public static SCNMatrix4 CreateRotationY (float angle);
	public static void CreateRotationY (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationZ (float angle);
	public static void CreateRotationZ (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateTranslation (SCNVector3 vector);
	public static SCNMatrix4 CreateTranslation (float x, float y, float z);
	public static void CreateTranslation (float x, float y, float z, out SCNMatrix4 result);
	public static void CreateTranslation (ref SCNVector3 vector, out SCNMatrix4 result);
	public virtual bool Equals (SCNMatrix4 other);
	public override bool Equals (object obj);

	[Obsolete ("Use CreatePerspectiveOffCenter instead.")]
	public static SCNMatrix4 Frustum (float left, float right, float bottom, float top, float near, float far);
	public override int GetHashCode ();
	public static SCNMatrix4 Invert (SCNMatrix4 mat);
	public void Invert ();
	public static SCNMatrix4 LookAt (SCNVector3 eye, SCNVector3 target, SCNVector3 up);
	public static SCNMatrix4 LookAt (float eyeX, float eyeY, float eyeZ, float targetX, float targetY, float targetZ, float upX, float upY, float upZ);
	public static SCNMatrix4 Mult (SCNMatrix4 left, SCNMatrix4 right);
	public static void Mult (ref SCNMatrix4 left, ref SCNMatrix4 right, out SCNMatrix4 result);
	public static bool op_Equality (SCNMatrix4 left, SCNMatrix4 right);
	public static bool op_Inequality (SCNMatrix4 left, SCNMatrix4 right);
	public static SCNMatrix4 op_Multiply (SCNMatrix4 left, SCNMatrix4 right);

	[Obsolete ("Use CreatePerspectiveFieldOfView instead.")]
	public static SCNMatrix4 Perspective (float fovy, float aspect, float near, float far);

	[Obsolete ("Use CreateFromAxisAngle instead.")]
	public static SCNMatrix4 Rotate (SCNVector3 axis, float angle);
	public static SCNMatrix4 Rotate (MonoMac.OpenGL.Quaternion q);
	public static SCNMatrix4 Rotate (MonoMac.OpenGL.Quaterniond q);

	[Obsolete ("Use CreateRotationX instead.")]
	public static SCNMatrix4 RotateX (float angle);

	[Obsolete ("Use CreateRotationY instead.")]
	public static SCNMatrix4 RotateY (float angle);

	[Obsolete ("Use CreateRotationZ instead.")]
	public static SCNMatrix4 RotateZ (float angle);
	public static SCNMatrix4 Scale (float x, float y, float z);
	public static SCNMatrix4 Scale (SCNVector3 scale);
	public static SCNMatrix4 Scale (float scale);
	public override string ToString ();

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (SCNVector3 trans);

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (float x, float y, float z);
	public static void Transpose (ref SCNMatrix4 mat, out SCNMatrix4 result);
	public void Transpose ();
	public static SCNMatrix4 Transpose (SCNMatrix4 mat);
}
```

### New Type MonoMac.SceneKit.SCNNodeRendererDelegate_Extensions

```
public static class SCNNodeRendererDelegate_Extensions {
	// methods
	public static void Render (ISCNNodeRendererDelegate This, SCNNode node, SCNRenderer renderer, MonoMac.Foundation.NSDictionary arguments);
}
```

### New Type MonoMac.SceneKit.SCNParticleBirthDirection

```
[Serializable]
public enum SCNParticleBirthDirection {
	Constant = 0,
	Random = 2,
	SurfaceNormal = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleBirthLocation

```
[Serializable]
public enum SCNParticleBirthLocation {
	Surface = 0,
	Vertex = 2,
	Volume = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleBlendMode

```
[Serializable]
public enum SCNParticleBlendMode {
	Additive = 0,
	Alpha = 4,
	Multiply = 2,
	Replace = 5,
	Screen = 3,
	Subtract = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleEvent

```
[Serializable]
public enum SCNParticleEvent {
	Birth = 0,
	Collision = 2,
	Death = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleEventHandler

```
public sealed delegate SCNParticleEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, int count, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, int count);
}
```

### New Type MonoMac.SceneKit.SCNParticleImageSequenceAnimationMode

```
[Serializable]
public enum SCNParticleImageSequenceAnimationMode {
	AutoReverse = 2,
	Clamp = 1,
	Repeat = 0,
}
```

### New Type MonoMac.SceneKit.SCNParticleInputMode

```
[Serializable]
public enum SCNParticleInputMode {
	OverDistance = 1,
	OverLife = 0,
	OverOtherProperty = 2,
}
```

### New Type MonoMac.SceneKit.SCNParticleModifierHandler

```
public sealed delegate SCNParticleModifierHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleModifierHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, int start, int end, float deltaTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, int start, int end, float deltaTime);
}
```

### New Type MonoMac.SceneKit.SCNParticleModifierStage

```
[Serializable]
public enum SCNParticleModifierStage {
	PostCollision = 3,
	PostDynamics = 1,
	PreCollision = 2,
	PreDynamics = 0,
}
```

### New Type MonoMac.SceneKit.SCNParticleOrientationMode

```
[Serializable]
public enum SCNParticleOrientationMode {
	BillboardScreenAligned = 0,
	BillboardViewAligned = 1,
	BillboardYAligned = 3,
	Free = 2,
}
```

### New Type MonoMac.SceneKit.SCNParticlePropertyController

```
public class SCNParticlePropertyController : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNParticlePropertyController (MonoMac.Foundation.NSCoder coder);
	public SCNParticlePropertyController (MonoMac.Foundation.NSObjectFlag t);
	public SCNParticlePropertyController (System.IntPtr handle);
	// properties
	public virtual MonoMac.CoreAnimation.CAAnimation Animation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float InputBias { get; set; }
	public virtual SCNParticleInputMode InputMode { get; set; }
	public virtual SCNNode InputOrigin { get; set; }
	public virtual MonoMac.Foundation.NSString InputProperty { get; set; }
	public virtual float InputScale { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNParticlePropertyController Create (MonoMac.CoreAnimation.CAAnimation animation);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNParticleSortingMode

```
[Serializable]
public enum SCNParticleSortingMode {
	Distance = 2,
	None = 0,
	OldestFirst = 3,
	ProjectedDepth = 1,
	YoungestFirst = 4,
}
```

### New Type MonoMac.SceneKit.SCNParticleSystem

```
public class SCNParticleSystem : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNParticleSystem (MonoMac.Foundation.NSCoder coder);
	public SCNParticleSystem (MonoMac.Foundation.NSObjectFlag t);
	public SCNParticleSystem (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Acceleration { get; set; }
	public virtual bool AffectedByGravity { get; set; }
	public virtual bool AffectedByPhysicsFields { get; set; }
	public virtual SCNParticleBirthDirection BirthDirection { get; set; }
	public virtual SCNParticleBirthLocation BirthLocation { get; set; }
	public virtual float BirthRate { get; set; }
	public virtual float BirthRateVariation { get; set; }
	public virtual bool BlackPassEnabled { get; set; }
	public virtual SCNParticleBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNNode[] ColliderNodes { get; set; }
	public virtual float DampingFactor { get; set; }
	public virtual float EmissionDuration { get; set; }
	public virtual float EmissionDurationVariation { get; set; }
	public virtual SCNGeometry EmitterShape { get; set; }
	public virtual SCNVector3 EmittingDirection { get; set; }
	public virtual float FresnelExponent { get; set; }
	public virtual float IdleDuration { get; set; }
	public virtual float IdleDurationVariation { get; set; }
	public virtual SCNParticleImageSequenceAnimationMode ImageSequenceAnimationMode { get; set; }
	public virtual uint ImageSequenceColumnCount { get; set; }
	public virtual float ImageSequenceFrameRate { get; set; }
	public virtual float ImageSequenceFrameRateVariation { get; set; }
	public virtual float ImageSequenceInitialFrame { get; set; }
	public virtual float ImageSequenceInitialFrameVariation { get; set; }
	public virtual uint ImageSequenceRowCount { get; set; }
	public virtual bool LightingEnabled { get; set; }
	public virtual bool Local { get; set; }
	public virtual bool Loops { get; set; }
	public virtual SCNParticleOrientationMode OrientationMode { get; set; }
	public virtual float ParticleAngle { get; set; }
	public virtual float ParticleAngleVariation { get; set; }
	public virtual float ParticleAngularVelocity { get; set; }
	public virtual float ParticleAngularVelocityVariation { get; set; }
	public virtual float ParticleBounce { get; set; }
	public virtual float ParticleBounceVariation { get; set; }
	public virtual float ParticleCharge { get; set; }
	public virtual float ParticleChargeVariation { get; set; }
	public virtual MonoMac.AppKit.NSColor ParticleColor { get; set; }
	public virtual SCNVector4 ParticleColorVariation { get; set; }
	public virtual bool ParticleDiesOnCollision { get; set; }
	public virtual float ParticleFriction { get; set; }
	public virtual float ParticleFrictionVariation { get; set; }
	public virtual MonoMac.Foundation.NSObject ParticleImage { get; set; }
	public virtual float ParticleLifeSpan { get; set; }
	public virtual float ParticleLifeSpanVariation { get; set; }
	public virtual float ParticleMass { get; set; }
	public virtual float ParticleMassVariation { get; set; }
	public virtual float ParticleSize { get; set; }
	public virtual float ParticleSizeVariation { get; set; }
	public virtual float ParticleVelocity { get; set; }
	public virtual float ParticleVelocityVariation { get; set; }
	public virtual SCNParticleSortingMode SortingMode { get; set; }
	public virtual float SpeedFactor { get; set; }
	public virtual float SpreadingAngle { get; set; }
	public virtual float StretchFactor { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnCollision { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnDying { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnLiving { get; set; }
	public virtual float WarmupDuration { get; set; }
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual void AddModifier (MonoMac.Foundation.NSString[] properties, SCNParticleModifierStage stage, SCNParticleModifierHandler handler);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNParticleSystem Create ();
	public static SCNParticleSystem Create (string name, string directory);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleEvent (SCNParticleEvent evnt, MonoMac.Foundation.NSString[] properties, SCNParticleEventHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAllModifiers ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void RemoveModifiers (SCNParticleModifierStage stage);
	public virtual void Reset ();
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBallSocketJoint

```
public class SCNPhysicsBallSocketJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsBallSocketJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBallSocketJoint (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsBallSocketJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNPhysicsBallSocketJoint Create (SCNPhysicsBody bodyA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 anchorB);
	public static SCNPhysicsBallSocketJoint Create (SCNPhysicsBody body, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBehavior

```
public abstract class SCNPhysicsBehavior : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsBehavior (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBehavior (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsBehavior (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBody

```
public class SCNPhysicsBody : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsBody (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBody (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsBody (System.IntPtr handle);
	// properties
	public virtual bool AllowsResting { get; set; }
	public virtual float AngularDamping { get; set; }
	public virtual SCNVector4 AngularVelocity { get; set; }
	public virtual SCNVector3 AngularVelocityFactor { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float Charge { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint CollisionBitMask { get; set; }
	public virtual float Damping { get; set; }
	public virtual float Friction { get; set; }
	public virtual bool IsResting { get; }
	public virtual float Mass { get; set; }
	public virtual SCNPhysicsShape PhysicsShape { get; set; }
	public virtual float Restitution { get; set; }
	public virtual float RollingFriction { get; set; }
	public virtual SCNPhysicsBodyType Type { get; set; }
	public virtual SCNVector3 Velocity { get; set; }
	public virtual SCNVector3 VelocityFactor { get; set; }
	// methods
	public virtual void ApplyForce (SCNVector3 direction, bool impulse);
	public virtual void ApplyForce (SCNVector3 direction, SCNVector3 position, bool impulse);
	public virtual void ApplyTorque (SCNVector4 torque, bool impulse);
	public virtual void ClearAllForces ();
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsBody CreateBody (SCNPhysicsBodyType type, SCNPhysicsShape shape);
	public static SCNPhysicsBody CreateDynamicBody ();
	public static SCNPhysicsBody CreateKinematicBody ();
	public static SCNPhysicsBody CreateStaticBody ();
	protected override void Dispose (bool disposing);
	public virtual void ResetTransform ();
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBodyType

```
[Serializable]
public enum SCNPhysicsBodyType {
	Dynamic = 1,
	Kinematic = 2,
	Static = 0,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContact

```
public class SCNPhysicsContact : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContact (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsContact (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsContact (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float CollisionImpulse { get; }
	public virtual SCNVector3 ContactNormal { get; }
	public virtual SCNVector3 ContactPoint { get; }
	public virtual SCNNode NodeA { get; }
	public virtual SCNNode NodeB { get; }
	public virtual float PenetrationDistance { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContactDelegate

```
public class SCNPhysicsContactDelegate : MonoMac.Foundation.NSObject, ISCNPhysicsContactDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsContactDelegate ();
	public SCNPhysicsContactDelegate (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsContactDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidEndContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidUpdateContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContactDelegate_Extensions

```
public static class SCNPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidEndContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidUpdateContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContactEventArgs

```
public class SCNPhysicsContactEventArgs : System.EventArgs {
	// constructors
	public SCNPhysicsContactEventArgs (SCNPhysicsContact contact);
	// properties
	public SCNPhysicsContact Contact { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsField

```
public class SCNPhysicsField : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsField (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsField (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsField (System.IntPtr handle);
	// properties
	public virtual bool Active { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 Direction { get; set; }
	public virtual bool Exclusive { get; set; }
	public virtual float FalloffExponent { get; set; }
	public virtual SCNVector3 HalfExtent { get; set; }
	public virtual float MinimumDistance { get; set; }
	public virtual SCNVector3 Offset { get; set; }
	public virtual SCNPhysicsFieldScope Scope { get; set; }
	public virtual float Strength { get; set; }
	public virtual bool UsesEllipsoidalExtent { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsField CreateDragField ();
	public static SCNPhysicsField CreateElectricField ();
	public static SCNPhysicsField CreateLinearGravityField ();
	public static SCNPhysicsField CreateMagneticField ();
	public static SCNPhysicsField CreateNoiseField (float smoothness, float speed);
	public static SCNPhysicsField CreateRadialGravityField ();
	public static SCNPhysicsField CreateSpringField ();
	public static SCNPhysicsField CreateTurbulenceField (float smoothness, float speed);
	public static SCNPhysicsField CreateVortexField ();
	public static SCNPhysicsField CustomField (SCNFieldForceEvaluator evaluator);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsFieldScope

```
[Serializable]
public enum SCNPhysicsFieldScope {
	InsideExtent = 0,
	OutsideExtent = 1,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsHingeJoint

```
public class SCNPhysicsHingeJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsHingeJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsHingeJoint (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsHingeJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNVector3 AxisA { get; set; }
	public virtual SCNVector3 AxisB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNPhysicsHingeJoint Create (SCNPhysicsBody bodyA, SCNVector3 axisA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 axisB, SCNVector3 anchorB);
	public static SCNPhysicsHingeJoint Create (SCNPhysicsBody body, SCNVector3 axis, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsSearchMode

```
[Serializable]
public enum SCNPhysicsSearchMode {
	All = 2,
	Any = 0,
	Closest = 1,
	Unknown = -1,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShape

```
public class SCNPhysicsShape : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsShape (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsShape (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsShape (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeOptions options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNPhysicsShape[] shapes, SCNVector3[] transforms);
	public static SCNPhysicsShape Create (SCNNode node, MonoMac.Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, MonoMac.Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeOptions options);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptions

```
public class SCNPhysicsShapeOptions {
	// constructors
	public SCNPhysicsShapeOptions ();
	// properties
	public bool? KeepAsCompound { get; set; }
	public SCNVector3? Scale { get; set; }
	public SCNPhysicsShapeType? ShapeType { get; set; }
	// methods
	public MonoMac.Foundation.NSDictionary ToDictionary ();
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptionsKeys

```
public static class SCNPhysicsShapeOptionsKeys {
	// properties
	public static MonoMac.Foundation.NSString KeepAsCompound { get; }
	public static MonoMac.Foundation.NSString Scale { get; }
	public static MonoMac.Foundation.NSString Type { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptionsTypes

```
public static class SCNPhysicsShapeOptionsTypes {
	// properties
	public static MonoMac.Foundation.NSString BoundingBox { get; }
	public static MonoMac.Foundation.NSString ConcavePolyhedron { get; }
	public static MonoMac.Foundation.NSString ConvexHull { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeType

```
[Serializable]
public enum SCNPhysicsShapeType {
	BoundingBox = 1,
	ConcavePolyhedron = 2,
	ConvexHull = 0,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsSliderJoint

```
public class SCNPhysicsSliderJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsSliderJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsSliderJoint (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsSliderJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNVector3 AxisA { get; set; }
	public virtual SCNVector3 AxisB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float MaximumAngularLimit { get; set; }
	public virtual float MaximumLinearLimit { get; set; }
	public virtual float MinimumAngularLimit { get; set; }
	public virtual float MinimumLinearLimit { get; set; }
	public virtual float MotorMaximumForce { get; set; }
	public virtual float MotorMaximumTorque { get; set; }
	public virtual float MotorTargetAngularVelocity { get; set; }
	public virtual float MotorTargetLinearVelocity { get; set; }
	// methods
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody bodyA, SCNVector3 axisA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 axisB, SCNVector3 anchorB);
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody body, SCNVector3 axis, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsTest

```
public class SCNPhysicsTest : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNPhysicsTest ();
	public SCNPhysicsTest (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? BackfaceCulling { get; set; }
	public uint? CollisionBitMask { get; set; }
	public SCNPhysicsSearchMode SearchMode { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsTestKeys

```
public static class SCNPhysicsTestKeys {
	// properties
	public static MonoMac.Foundation.NSString BackfaceCullingKey { get; }
	public static MonoMac.Foundation.NSString CollisionBitMaskKey { get; }
	public static MonoMac.Foundation.NSString SearchModeKey { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsTestSearchModeKeys

```
public static class SCNPhysicsTestSearchModeKeys {
	// properties
	public static MonoMac.Foundation.NSString All { get; }
	public static MonoMac.Foundation.NSString Any { get; }
	public static MonoMac.Foundation.NSString Closest { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsVehicle

```
public class SCNPhysicsVehicle : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsVehicle (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsVehicle (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsVehicle (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBody ChassisBody { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float SpeedInKilometersPerHour { get; }
	public virtual SCNPhysicsVehicleWheel[] Wheels { get; }
	// methods
	public virtual void ApplyBrakingForce (float value, int index);
	public virtual void ApplyEngineForce (float value, int index);
	public static SCNPhysicsVehicle Create (SCNPhysicsBody chassisBody, SCNPhysicsVehicleWheel[] wheels);
	protected override void Dispose (bool disposing);
	public virtual void SetSteeringAngle (float value, int index);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsVehicleWheel

```
public class SCNPhysicsVehicleWheel : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsVehicleWheel (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsVehicleWheel (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsVehicleWheel (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Axle { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 ConnectionPosition { get; set; }
	public virtual float FrictionSlip { get; set; }
	public virtual float MaximumSuspensionForce { get; set; }
	public virtual float MaximumSuspensionTravel { get; set; }
	public virtual SCNNode Node { get; }
	public virtual float Radius { get; set; }
	public virtual SCNVector3 SteeringAxis { get; set; }
	public virtual float SuspensionCompression { get; set; }
	public virtual float SuspensionDamping { get; set; }
	public virtual float SuspensionRestLength { get; set; }
	public virtual float SuspensionStiffness { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsVehicleWheel Create (SCNNode node);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsWorld

```
public class SCNPhysicsWorld : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNPhysicsWorld (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsWorld (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsWorld (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBehavior[] AllBehaviors { get; }
	public override System.IntPtr ClassHandle { get; }
	public SCNPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual SCNVector3 Gravity { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeStep { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidBeginContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidEndContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidUpdateContact;
	// methods
	public virtual void AddBehavior (SCNPhysicsBehavior behavior);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, MonoMac.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, MonoMac.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, SCNPhysicsTest options);
	public SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, MonoMac.Foundation.NSDictionary options);
	protected override void Dispose (bool disposing);
	public virtual SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, MonoMac.Foundation.NSDictionary options);
	public SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, SCNPhysicsTest options);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (SCNPhysicsBehavior behavior);
	public virtual void UpdateCollisionPairs ();
}
```

### New Type MonoMac.SceneKit.SCNProgramDelegate_Extensions

```
public static class SCNProgramDelegate_Extensions {
	// methods
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public static void HandleError (ISCNProgramDelegate This, SCNProgram program, MonoMac.Foundation.NSError error);
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
}
```

### New Type MonoMac.SceneKit.SCNProgramSemanticOptions

```
public class SCNProgramSemanticOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNProgramSemanticOptions ();
	public SCNProgramSemanticOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public uint? MappingChannel { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNQuaternion

```
[Serializable]
public struct SCNQuaternion, System.IEquatable<SCNQuaternion> {
	// constructors
	public SCNQuaternion (SCNVector3 v, float w);
	public SCNQuaternion (float x, float y, float z, float w);
	public SCNQuaternion (ref MonoMac.OpenGL.Matrix3 matrix);
	public SCNQuaternion (MonoMac.OpenGL.Quaternion openTkQuaternion);
	// fields
	public static SCNQuaternion Identity;
	// properties
	public float Length { get; }
	public float LengthSquared { get; }
	public float W { get; set; }
	public float X { get; set; }
	public SCNVector3 Xyz { get; set; }

	[Obsolete ("Use Xyz property instead.")]
	public SCNVector3 XYZ { get; set; }
	public float Y { get; set; }
	public float Z { get; set; }
	// methods
	public static void Add (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Add (SCNQuaternion left, SCNQuaternion right);
	public static void Conjugate (ref SCNQuaternion q, out SCNQuaternion result);
	public static SCNQuaternion Conjugate (SCNQuaternion q);
	public void Conjugate ();
	public virtual bool Equals (SCNQuaternion other);
	public override bool Equals (object other);
	public static SCNQuaternion FromAxisAngle (SCNVector3 axis, float angle);
	public override int GetHashCode ();
	public static SCNQuaternion Invert (SCNQuaternion q);
	public static void Invert (ref SCNQuaternion q, out SCNQuaternion result);

	[Obsolete ("Use Multiply instead.")]
	public static SCNQuaternion Mult (SCNQuaternion left, SCNQuaternion right);

	[Obsolete ("Use Multiply instead.")]
	public static void Mult (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static void Multiply (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Multiply (SCNQuaternion quaternion, float scale);

	[Obsolete ("Use the overload without the ref float scale")]
	public static void Multiply (ref SCNQuaternion quaternion, ref float scale, out SCNQuaternion result);
	public static SCNQuaternion Multiply (SCNQuaternion left, SCNQuaternion right);
	public static void Multiply (ref SCNQuaternion quaternion, float scale, out SCNQuaternion result);
	public static SCNQuaternion Normalize (SCNQuaternion q);
	public static void Normalize (ref SCNQuaternion q, out SCNQuaternion result);
	public void Normalize ();
	public static SCNQuaternion op_Addition (SCNQuaternion left, SCNQuaternion right);
	public static bool op_Equality (SCNQuaternion left, SCNQuaternion right);
	public static bool op_Inequality (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion op_Multiply (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion op_Multiply (SCNQuaternion quaternion, float scale);
	public static SCNQuaternion op_Multiply (float scale, SCNQuaternion quaternion);
	public static SCNQuaternion op_Subtraction (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion Slerp (SCNQuaternion q1, SCNQuaternion q2, float blend);
	public static void Sub (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Sub (SCNQuaternion left, SCNQuaternion right);
	public SCNVector4 ToAxisAngle ();
	public void ToAxisAngle (out SCNVector3 axis, out float angle);
	public override string ToString ();
}
```

### New Type MonoMac.SceneKit.SCNSceneExportDelegate

```
public class SCNSceneExportDelegate : MonoMac.Foundation.NSObject, ISCNSceneExportDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNSceneExportDelegate ();
	public SCNSceneExportDelegate (MonoMac.Foundation.NSCoder coder);
	public SCNSceneExportDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SCNSceneExportDelegate (System.IntPtr handle);
	// methods
	public virtual MonoMac.Foundation.NSUrl WriteImage (MonoMac.AppKit.NSImage image, MonoMac.Foundation.NSUrl documentURL, MonoMac.Foundation.NSUrl originalImageURL);
}
```

### New Type MonoMac.SceneKit.SCNSceneExportDelegate_Extensions

```
public static class SCNSceneExportDelegate_Extensions {
	// methods
	public static MonoMac.Foundation.NSUrl WriteImage (ISCNSceneExportDelegate This, MonoMac.AppKit.NSImage image, MonoMac.Foundation.NSUrl documentURL, MonoMac.Foundation.NSUrl originalImageURL);
}
```

### New Type MonoMac.SceneKit.SCNSceneExportProgressHandler

```
public sealed delegate SCNSceneExportProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneExportProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (float totalProgress, MonoMac.Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (float totalProgress, MonoMac.Foundation.NSError error, out bool stop);
}
```

### New Type MonoMac.SceneKit.SCNSceneLoadingOptions

```
public class SCNSceneLoadingOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNSceneLoadingOptions ();
	public SCNSceneLoadingOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public SCNAnimationImportPolicy AnimationImportPolicy { get; set; }
	public MonoMac.Foundation.NSUrl[] AssetDirectoryUrls { get; set; }
	public bool? CheckConsistency { get; set; }
	public bool? ConvertToYUp { get; set; }
	public float? ConvertUnitsToMeters { get; set; }
	public bool? CreateNormalsIfAbsent { get; set; }
	public bool? FlattenScene { get; set; }
	public bool? OverrideAssetUrls { get; set; }
	public bool? StrictConformance { get; set; }
	public bool? UseSafeMode { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNSceneRenderer

```
public abstract class SCNSceneRenderer : MonoMac.Foundation.NSObject, ISCNSceneRenderer, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNSceneRenderer ();
	public SCNSceneRenderer (MonoMac.Foundation.NSCoder coder);
	public SCNSceneRenderer (MonoMac.Foundation.NSObjectFlag t);
	public SCNSceneRenderer (System.IntPtr handle);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public virtual System.IntPtr Context { get; }
	public virtual double CurrentTime { get; set; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public virtual SCNScene Scene { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
}
```

### New Type MonoMac.SceneKit.SCNSceneRenderer_Extensions

```
public static class SCNSceneRenderer_Extensions {
	// methods
	public static bool GetAutoenablesDefaultLighting (ISCNSceneRenderer This);
	public static System.IntPtr GetContext (ISCNSceneRenderer This);
	public static double GetCurrentTime (ISCNSceneRenderer This);
	public static bool GetJitteringEnabled (ISCNSceneRenderer This);
	public static bool GetLoops (ISCNSceneRenderer This);
	public static bool GetPlaying (ISCNSceneRenderer This);
	public static SCNNode GetPointOfView (ISCNSceneRenderer This);
	public static SCNScene GetScene (ISCNSceneRenderer This);
	public static double GetSceneTimeInSeconds (ISCNSceneRenderer This);
	public static bool GetShowsStatistics (ISCNSceneRenderer This);
	public static MonoMac.Foundation.NSObject GetWeakSceneRendererDelegate (ISCNSceneRenderer This);
	public static SCNHitTestResult[] HitTest (ISCNSceneRenderer This, System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public static bool IsNodeInsideFrustum (ISCNSceneRenderer This, SCNNode node, SCNNode pointOfView);
	public static void Prepare (ISCNSceneRenderer This, MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public static bool Prepare (ISCNSceneRenderer This, MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public static SCNVector3 ProjectPoint (ISCNSceneRenderer This, SCNVector3 point);
	public static void SetAutoenablesDefaultLighting (ISCNSceneRenderer This, bool value);
	public static void SetCurrentTime (ISCNSceneRenderer This, double value);
	public static void SetJitteringEnabled (ISCNSceneRenderer This, bool value);
	public static void SetLoops (ISCNSceneRenderer This, bool value);
	public static void SetPlaying (ISCNSceneRenderer This, bool value);
	public static void SetPointOfView (ISCNSceneRenderer This, SCNNode value);
	public static void SetScene (ISCNSceneRenderer This, SCNScene value);
	public static void SetSceneTimeInSeconds (ISCNSceneRenderer This, double value);
	public static void SetShowsStatistics (ISCNSceneRenderer This, bool value);
	public static void SetWeakSceneRendererDelegate (ISCNSceneRenderer This, MonoMac.Foundation.NSObject value);
	public static SCNVector3 UnprojectPoint (ISCNSceneRenderer This, SCNVector3 point);
}
```

### New Type MonoMac.SceneKit.SCNSceneRendererDelegate_Extensions

```
public static class SCNSceneRendererDelegate_Extensions {
	// methods
	public static void DidApplyAnimations (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void DidRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public static void DidSimulatePhysics (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void Update (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void WillRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
}
```

### New Type MonoMac.SceneKit.SCNSceneSourceFilter

```
public sealed delegate SCNSceneSourceFilter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneSourceFilter (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSObject entry, MonoMac.Foundation.NSString identifier, ref bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual bool Invoke (MonoMac.Foundation.NSObject entry, MonoMac.Foundation.NSString identifier, ref bool stop);
}
```

### New Type MonoMac.SceneKit.SCNShadable

```
public class SCNShadable : MonoMac.Foundation.NSObject, ISCNShadable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNShadable ();
	public SCNShadable (MonoMac.Foundation.NSCoder coder);
	public SCNShadable (MonoMac.Foundation.NSObjectFlag t);
	public SCNShadable (System.IntPtr handle);
	// properties
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
	// methods
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
}
```

### New Type MonoMac.SceneKit.SCNShadable_Extensions

```
public static class SCNShadable_Extensions {
	// methods
	public static SCNProgram GetProgram (ISCNShadable This);
	public static MonoMac.Foundation.NSDictionary GetWeakShaderModifiers (ISCNShadable This);
	public static void HandleBinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
	public static void HandleUnbinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
	public static void SetProgram (ISCNShadable This, SCNProgram value);
	public static void SetWeakShaderModifiers (ISCNShadable This, MonoMac.Foundation.NSDictionary value);
}
```

### New Type MonoMac.SceneKit.SCNShadowMode

```
[Serializable]
public enum SCNShadowMode {
	Deferred = 1,
	Forward = 0,
	Modulated = 2,
}
```

### New Type MonoMac.SceneKit.SCNTechnique

```
public class SCNTechnique : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNTechnique (MonoMac.Foundation.NSCoder coder);
	public SCNTechnique (MonoMac.Foundation.NSObjectFlag t);
	public SCNTechnique (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }

	[Obsolete ("Use ToDictionary () instead")]
	public virtual MonoMac.Foundation.NSDictionary DictionaryRepresentation { get; }
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNTechnique Create (MonoMac.Foundation.NSDictionary dictionary);
	public static SCNTechnique Create (SCNTechnique[] techniques);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
	public MonoMac.Foundation.NSDictionary ToDictionary ();
}
```

### New Type MonoMac.SceneKit.SCNTechniqueSupport

```
public abstract class SCNTechniqueSupport : MonoMac.Foundation.NSObject, ISCNTechniqueSupport, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SCNTechniqueSupport ();
	public SCNTechniqueSupport (MonoMac.Foundation.NSCoder coder);
	public SCNTechniqueSupport (MonoMac.Foundation.NSObjectFlag t);
	public SCNTechniqueSupport (System.IntPtr handle);
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNTechniqueSupport_Extensions

```
public static class SCNTechniqueSupport_Extensions {
}
```

## Namespace MonoMac.ScriptingBridge

### Type Changed: MonoMac.ScriptingBridge.SBApplication

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ScriptingBridge.SBApplicationDelegate

Added interfaces:

```
ISBApplicationDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.ScriptingBridge.SBObject

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.ScriptingBridge.ISBApplicationDelegate

```
public interface ISBApplicationDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual MonoMac.Foundation.NSObject EventDidFailwithError (System.IntPtr appleEvent, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.ScriptingBridge.SBApplicationDelegate_Extensions

```
public static class SBApplicationDelegate_Extensions {
}
```

## Namespace MonoMac.Security

### Type Changed: MonoMac.Security.SecAccessible

Added value:

```
WhenPasscodeSetThisDeviceOnly = 6,
```

### Type Changed: MonoMac.Security.SecRecord

Removed property:

```
public MonoMac.Foundation.NSData[] MatchIssuers { set; }
```

Added properties:

```
public SecAccessControl AccessControl { get; set; }
	public MonoMac.Foundation.NSData[] MatchIssuers { get; set; }
	public bool UseNoAuthenticationUI { get; set; }
	public string UseOperationPrompt { get; set; }
```

Obsoleted property:

```
[Obsolete ("Use GetValueRef and SetValueRef instead")]
	public MonoMac.Foundation.NSObject ValueRef { get; set; }
```

Added methods:

```
public T GetValueRef<T> ();
	public void SetValueRef (MonoMac.ObjCRuntime.INativeObject value);
```

### Type Changed: MonoMac.Security.SslSessionOption

Added value:

```
Fallback = 6,
```

### New Type MonoMac.Security.SecAccessControl

```
public class SecAccessControl {
	// constructors
	public SecAccessControl (SecAccessible accessible, SecAccessControlCreateFlags flags);
	// properties
	public SecAccessible Accessible { get; }
	public SecAccessControlCreateFlags Flags { get; }
}
```

### New Type MonoMac.Security.SecAccessControlCreateFlags

```
[Serializable]
[Flags]
public enum SecAccessControlCreateFlags {
	UserPresence = 1,
}
```

## Namespace MonoMac.StoreKit

### Type Changed: MonoMac.StoreKit.ISKProductsRequestDelegate

Added interface:

```
ISKRequestDelegate
```

### Type Changed: MonoMac.StoreKit.SKDownload

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKMutablePayment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKPayment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Removed property:

```
public virtual MonoMac.Foundation.NSData RequestData { get; }
```

Added property:

```
public virtual MonoMac.Foundation.NSData RequestData { get; set; }
```

Removed method:

```
[Obsolete ("Deprecated in iOS 5.0. Use PaymentWithProduct(SKProduct) after fetching the list of available products from SKProductRequest")]
	public static SKPayment PaymentWithProduct (string identifier);
```

### Type Changed: MonoMac.StoreKit.SKPaymentQueue

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKPaymentTransaction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKPaymentTransactionObserver

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKPaymentTransactionState

Added value:

```
Deferred = 4,
```

### Type Changed: MonoMac.StoreKit.SKProduct

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKProductsRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKProductsRequestDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKProductsResponse

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKRequest

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.StoreKit.SKRequestDelegate

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.StoreKit.SKReceiptProperties

```
public class SKReceiptProperties : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SKReceiptProperties ();
	public SKReceiptProperties (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool IsExpired { get; set; }
	public bool IsRevoked { get; set; }
	public bool IsVolumePurchase { get; set; }
}
```

### New Type MonoMac.StoreKit.SKReceiptRefreshRequest

```
public class SKReceiptRefreshRequest : MonoMac.StoreKit.SKRequest, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKReceiptRefreshRequest ();
	public SKReceiptRefreshRequest (MonoMac.Foundation.NSCoder coder);
	public SKReceiptRefreshRequest (MonoMac.Foundation.NSObjectFlag t);
	public SKReceiptRefreshRequest (System.IntPtr handle);
	public SKReceiptRefreshRequest (MonoMac.Foundation.NSDictionary properties);
	public SKReceiptRefreshRequest (SKReceiptProperties receiptProperties);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public SKReceiptProperties ReceiptProperties { get; }
	public virtual MonoMac.Foundation.NSDictionary WeakReceiptProperties { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static void TerminateForInvalidReceipt ();
}
```

## Namespace MonoMac.SystemConfiguration

### Type Changed: MonoMac.SystemConfiguration.CaptiveNetwork

Obsoleted method:

```
[Obsolete ("Replaced by TryGetSupportedInterfaces")]
	public static string[] GetSupportedInterfaces ();
```

## Namespace MonoMac.WebKit

### Type Changed: MonoMac.WebKit.DomAbstractView

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomAttr

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomBlob

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCDataSection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCharacterData

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomComment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCssRule

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCssRuleList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCssStyleDeclaration

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCssStyleSheet

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomCssValue

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomDocument

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added methods:

```
public virtual DomEvent CreateEvent (string eventType);
	public virtual DomNodeIterator CreateNodeIterator (DomNode root, uint whatToShow, IDomNodeFilter filter, bool expandEntityReferences);
```

### Type Changed: MonoMac.WebKit.DomDocumentFragment

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomDocumentType

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomElement

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomEntityReference

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomEventListener

Added interfaces:

```
IDomEventListener
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomEventTarget

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomFile

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomFileList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlCollection

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlDocument

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlElement

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlFormElement

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlInputElement

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomHtmlTextAreaElement

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomImplementation

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomKeyboardEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomMediaList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomMouseEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomNamedNodeMap

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomNode

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomNodeList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomObject

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomOverflowEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomProcessingInstruction

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomProgressEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomRange

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomStyleSheet

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomStyleSheetList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomText

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomUIEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.DomWheelEvent

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.IDomEventTarget

Added interface:

```
MonoMac.Foundation.INSCopying
```

### Type Changed: MonoMac.WebKit.WebArchive

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebBackForwardList

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebDataSource

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebDocumentRepresentation

Added interfaces:

```
IWebDocumentRepresentation
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebDownload

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebDownloadDelegate

Added interfaces:

```
IWebDownloadDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebFrame

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebFrameLoadDelegate

Added interfaces:

```
IWebFrameLoadDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebFrameView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebHistoryItem

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebOpenPanelResultListener

Added interfaces:

```
IWebOpenPanelResultListener
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebPolicyDecisionListener

Added interfaces:

```
IWebPolicyDecisionListener
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebPolicyDelegate

Added interfaces:

```
IWebPolicyDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebPreferences

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebResource

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebResourceLoadDelegate

Added interfaces:

```
IWebResourceLoadDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebScriptObject

Added interface:

```
MonoMac.Foundation.INSObjectProtocol
```

Added method:

```
public void SetWebScriptValueAtIndex (int index, MonoMac.Foundation.NSObject value);
```

Obsoleted method:

```
[Obsolete ("Use SetWebScriptValueAtIndex instead")]
	public virtual void SetWebScriptValueAtIndexvalue (int index, MonoMac.Foundation.NSObject value);
```

### Type Changed: MonoMac.WebKit.WebUIDelegate

Added interfaces:

```
IWebUIDelegate
	MonoMac.Foundation.INSObjectProtocol
```

### Type Changed: MonoMac.WebKit.WebView

Added interfaces:

```
MonoMac.AppKit.INSDraggingDestination
	MonoMac.AppKit.INSUserInterfaceItemIdentification
	MonoMac.Foundation.INSObjectProtocol
```

### New Type MonoMac.WebKit.DomEventListener_Extensions

```
public static class DomEventListener_Extensions {
}
```

### New Type MonoMac.WebKit.DomHtmlAnchorElement

```
public class DomHtmlAnchorElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlAnchorElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlAnchorElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlAnchorElement (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSUrl AbsoluteImageUrl { get; }
	public virtual string AccessKey { get; set; }
	public virtual string Charset { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Coords { get; set; }
	public virtual string HashName { get; }
	public virtual string Host { get; }
	public virtual string Hostname { get; }
	public virtual string HRef { get; set; }
	public virtual string HRefLang { get; set; }
	public virtual string Name { get; set; }
	public virtual string Pathname { get; }
	public virtual string Port { get; }
	public virtual string Protocol { get; }
	public virtual string Rel { get; set; }
	public virtual string Rev { get; set; }
	public virtual string Search { get; }
	public virtual string Shape { get; set; }
	public virtual string Target { get; set; }
	public virtual string Text { get; }
	public virtual string Type { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlAppletElement

```
public class DomHtmlAppletElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlAppletElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlAppletElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlAppletElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public virtual string Alt { get; set; }
	public virtual string Archive { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Code { get; set; }
	public virtual string CodeBase { get; set; }
	public virtual string Height { get; set; }
	public virtual int HSpace { get; set; }
	public virtual string Name { get; set; }
	public virtual string Object { get; set; }
	public virtual int VSpace { get; set; }
	public virtual string Width { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlAreaElement

```
public class DomHtmlAreaElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlAreaElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlAreaElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlAreaElement (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSUrl AbsoluteImageUrl { get; }
	public virtual string AccessKey { get; set; }
	public virtual string Alt { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Coords { get; set; }
	public virtual string HashName { get; }
	public virtual string Host { get; }
	public virtual string Hostname { get; }
	public virtual string HRef { get; set; }
	public virtual bool NoHRef { get; set; }
	public virtual string Pathname { get; }
	public virtual string Port { get; }
	public virtual string Protocol { get; }
	public virtual string Search { get; }
	public virtual string Shape { get; set; }
	public virtual string Target { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlBaseElement

```
public class DomHtmlBaseElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlBaseElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlBaseElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlBaseElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string HRef { get; set; }
	public virtual string Target { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlBaseFontElement

```
public class DomHtmlBaseFontElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlBaseFontElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlBaseFontElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlBaseFontElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Color { get; set; }
	public virtual string Face { get; set; }
	public virtual string Size { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlBodyElement

```
public class DomHtmlBodyElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlBodyElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlBodyElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlBodyElement (System.IntPtr handle);
	// properties
	public virtual string ALink { get; set; }
	public virtual string Background { get; set; }
	public virtual string BgColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Link { get; set; }
	public virtual string Text { get; set; }
	public virtual string VLink { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlBRElement

```
public class DomHtmlBRElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlBRElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlBRElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlBRElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Clear { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlButtonElement

```
public class DomHtmlButtonElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlButtonElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlButtonElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlButtonElement (System.IntPtr handle);
	// properties
	public virtual string AccessKey { get; set; }
	public virtual bool Autofocus { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Disabled { get; set; }
	public virtual DomHtmlFormElement Form { get; }
	public virtual string Name { get; set; }
	public virtual string Type { get; set; }
	public virtual string Value { get; set; }
	public virtual bool WillValidate { get; }
	// methods
	public virtual void Click ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlDirectoryElement

```
public class DomHtmlDirectoryElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlDirectoryElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlDirectoryElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlDirectoryElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compact { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlDivElement

```
public class DomHtmlDivElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlDivElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlDivElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlDivElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.DomHtmlDListElement

```
public class DomHtmlDListElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlDListElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlDListElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlDListElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compact { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlEmbedElement

```
public class DomHtmlEmbedElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlEmbedElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlEmbedElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlEmbedElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int Height { get; set; }
	public virtual string Name { get; set; }
	public virtual string Src { get; set; }
	public virtual string Type { get; set; }
	public virtual int Width { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlFieldSetElement

```
public class DomHtmlFieldSetElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlFieldSetElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlFieldSetElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlFieldSetElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual DomHtmlFormElement Form { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlFontElement

```
public class DomHtmlFontElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlFontElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlFontElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlFontElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Color { get; set; }
	public virtual string Face { get; set; }
	public virtual string Size { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlFrameElement

```
public class DomHtmlFrameElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlFrameElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlFrameElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlFrameElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual DomDocument ContentDocument { get; }
	public virtual DomAbstractView ContentWindow { get; }
	public virtual string FrameBorder { get; set; }
	public virtual int Height { get; }
	public virtual string Location { get; set; }
	public virtual string LongDesc { get; set; }
	public virtual string MarginHeight { get; set; }
	public virtual string MarginWidth { get; set; }
	public virtual string Name { get; set; }
	public virtual bool NoResize { get; set; }
	public virtual string Scrolling { get; set; }
	public virtual string Src { get; set; }
	public virtual int Width { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlFrameSetElement

```
public class DomHtmlFrameSetElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlFrameSetElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlFrameSetElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlFrameSetElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Cols { get; set; }
	public virtual string Rows { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlHeadElement

```
public class DomHtmlHeadElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlHeadElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlHeadElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlHeadElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Profile { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlHeadingElement

```
public class DomHtmlHeadingElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlHeadingElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlHeadingElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlHeadingElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.DomHtmlHRElement

```
public class DomHtmlHRElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlHRElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlHRElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlHRElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool NoShade { get; set; }
	public virtual string Size { get; set; }
	public virtual string Width { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlHtmlElement

```
public class DomHtmlHtmlElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlHtmlElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlHtmlElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlHtmlElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Version { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlIFrameElement

```
public class DomHtmlIFrameElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlIFrameElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlIFrameElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlIFrameElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual DomDocument ContentDocument { get; }
	public virtual DomAbstractView ContentWindow { get; }
	public virtual string FrameBorder { get; set; }
	public virtual string Height { get; set; }
	public virtual string LongDesc { get; set; }
	public virtual string MarginHeight { get; set; }
	public virtual string MarginWidth { get; set; }
	public virtual string Name { get; set; }
	public virtual string Scrolling { get; set; }
	public virtual string Src { get; set; }
	public virtual string Width { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlImageElement

```
public class DomHtmlImageElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlImageElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlImageElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlImageElement (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSUrl AbsoluteImageUrl { get; }
	public virtual string Align { get; set; }
	public virtual string Alt { get; set; }
	public virtual string AltDisplayString { get; }
	public virtual string Border { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Complete { get; }
	public virtual int Height { get; set; }
	public virtual int HSpace { get; set; }
	public virtual bool IsMap { get; set; }
	public virtual string LongDesc { get; set; }
	public virtual string Lowsrc { get; set; }
	public virtual string Name { get; set; }
	public virtual int NaturalHeight { get; }
	public virtual int NaturalWidth { get; }
	public virtual string Src { get; set; }
	public virtual string UseMap { get; set; }
	public virtual int VSpace { get; set; }
	public virtual int Width { get; set; }
	public virtual int X { get; }
	public virtual int Y { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlLabelElement

```
public class DomHtmlLabelElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlLabelElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlLabelElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlLabelElement (System.IntPtr handle);
	// properties
	public virtual string AccessKey { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual DomHtmlFormElement Form { get; }
	public virtual string HtmlFor { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlLegendElement

```
public class DomHtmlLegendElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlLegendElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlLegendElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlLegendElement (System.IntPtr handle);
	// properties
	public virtual string AccessKey { get; set; }
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual DomHtmlFormElement Form { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlLIElement

```
public class DomHtmlLIElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlLIElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlLIElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlLIElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Type { get; set; }
	public virtual int Value { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlLinkElement

```
public class DomHtmlLinkElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlLinkElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlLinkElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlLinkElement (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSUrl AbsoluteImageUrl { get; }
	public virtual string Charset { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Disabled { get; set; }
	public virtual string HRef { get; set; }
	public virtual string HRefLang { get; set; }
	public virtual string Media { get; set; }
	public virtual string Rel { get; set; }
	public virtual string Rev { get; set; }
	public virtual DomStyleSheet Sheet { get; }
	public virtual string Target { get; set; }
	public virtual string Type { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlMapElement

```
public class DomHtmlMapElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlMapElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlMapElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlMapElement (System.IntPtr handle);
	// properties
	public virtual DomHtmlCollection Areas { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlMarqueeElement

```
public class DomHtmlMarqueeElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlMarqueeElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlMarqueeElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlMarqueeElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void Start ();
	public virtual void Stop ();
}
```

### New Type MonoMac.WebKit.DomHtmlMenuElement

```
public class DomHtmlMenuElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlMenuElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlMenuElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlMenuElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compact { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlMetaElement

```
public class DomHtmlMetaElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlMetaElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlMetaElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlMetaElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Content { get; set; }
	public virtual string HttpEquiv { get; set; }
	public virtual string Name { get; set; }
	public virtual string Scheme { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlModElement

```
public class DomHtmlModElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlModElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlModElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlModElement (System.IntPtr handle);
	// properties
	public virtual string Cite { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string DateTime { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlObjectElement

```
public class DomHtmlObjectElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlObjectElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlObjectElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlObjectElement (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSUrl AbsoluteImageUrl { get; }
	public virtual string Align { get; set; }
	public virtual string Archive { get; set; }
	public virtual string Border { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Code { get; set; }
	public virtual string CodeBase { get; set; }
	public virtual string CodeType { get; set; }
	public virtual DomDocument ContentDocument { get; }
	public virtual string Data { get; set; }
	public virtual bool Declare { get; set; }
	public virtual DomHtmlFormElement Form { get; }
	public virtual string Height { get; set; }
	public virtual int HSpace { get; set; }
	public virtual string Name { get; set; }
	public virtual string Standby { get; set; }
	public virtual string Type { get; set; }
	public virtual string UseMap { get; set; }
	public virtual int VSpace { get; set; }
	public virtual string Width { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlOListElement

```
public class DomHtmlOListElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlOListElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlOListElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlOListElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compact { get; set; }
	public virtual int Start { get; set; }
	public virtual string Type { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlOptGroupElement

```
public class DomHtmlOptGroupElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlOptGroupElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlOptGroupElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlOptGroupElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Disabled { get; set; }
	public virtual string Label { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlOptionElement

```
public class DomHtmlOptionElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlOptionElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlOptionElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlOptionElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool DefaultSelected { get; set; }
	public virtual bool Disabled { get; set; }
	public virtual DomHtmlFormElement Form { get; }
	public virtual int Index { get; }
	public virtual string Label { get; set; }
	public virtual bool Selected { get; set; }
	public virtual string Text { get; }
	public virtual string Value { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlOptionsCollection

```
public class DomHtmlOptionsCollection : MonoMac.WebKit.DomObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlOptionsCollection (MonoMac.Foundation.NSCoder coder);
	public DomHtmlOptionsCollection (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlOptionsCollection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public DomNode Item { get; }
	public DomNode Item { get; }
	public virtual uint Length { get; set; }
	public virtual int SelectedIndex { get; set; }
	// methods
	public virtual void Add (DomHtmlOptionElement option, uint index);
	public virtual DomNode GetItem (uint index);
	public virtual DomNode NamedItem (string name);
	public virtual void Remove (uint index);
}
```

### New Type MonoMac.WebKit.DomHtmlParagraphElement

```
public class DomHtmlParagraphElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlParagraphElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlParagraphElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlParagraphElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.DomHtmlParamElement

```
public class DomHtmlParamElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlParamElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlParamElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlParamElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual string Type { get; set; }
	public virtual string Value { get; set; }
	public virtual string ValueType { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlPreElement

```
public class DomHtmlPreElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlPreElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlPreElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlPreElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int Width { get; set; }
	public virtual bool Wrap { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlQuoteElement

```
public class DomHtmlQuoteElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlQuoteElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlQuoteElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlQuoteElement (System.IntPtr handle);
	// properties
	public virtual string Cite { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.DomHtmlScriptElement

```
public class DomHtmlScriptElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlScriptElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlScriptElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlScriptElement (System.IntPtr handle);
	// properties
	public virtual string Charset { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Defer { get; set; }
	public virtual string Event { get; set; }
	public virtual string HtmlFor { get; set; }
	public virtual string Src { get; set; }
	public virtual string Text { get; set; }
	public virtual string Type { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlSelectElement

```
public class DomHtmlSelectElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlSelectElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlSelectElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlSelectElement (System.IntPtr handle);
	// properties
	public virtual bool Autofocus { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Disabled { get; set; }
	public virtual DomHtmlFormElement Form { get; }
	public DomNode Item { get; }
	public DomNode Item { get; }
	public virtual int Length { get; }
	public virtual bool Multiple { get; set; }
	public virtual string Name { get; set; }
	public virtual DomHtmlOptionsCollection Options { get; }
	public virtual int SelectedIndex { get; set; }
	public virtual int Size { get; set; }
	public virtual string Type { get; }
	public virtual string Value { get; set; }
	public virtual bool WillValidate { get; }
	// methods
	public virtual void Add (DomHtmlElement element, DomHtmlElement before);
	protected override void Dispose (bool disposing);
	public virtual DomNode GetItem (uint index);
	public virtual DomNode NamedItem (string name);
	public virtual void Remove (int index);
}
```

### New Type MonoMac.WebKit.DomHtmlStyleElement

```
public class DomHtmlStyleElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlStyleElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlStyleElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlStyleElement (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Disabled { get; set; }
	public virtual string Media { get; set; }
	public virtual DomStyleSheet Sheet { get; }
	public virtual string Type { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.DomHtmlTableCaptionElement

```
public class DomHtmlTableCaptionElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableCaptionElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableCaptionElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableCaptionElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.DomHtmlTableCellElement

```
public class DomHtmlTableCellElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableCellElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableCellElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableCellElement (System.IntPtr handle);
	// properties
	public virtual string Abbr { get; set; }
	public virtual string Align { get; set; }
	public virtual string Axis { get; set; }
	public virtual string BgColor { get; set; }
	public virtual int CellIndex { get; }
	public virtual string Ch { get; set; }
	public virtual string ChOff { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int ColSpan { get; set; }
	public virtual string Headers { get; set; }
	public virtual string Height { get; set; }
	public virtual bool NoWrap { get; set; }
	public virtual int RowSpan { get; set; }
	public virtual string Scope { get; set; }
	public virtual string VAlign { get; set; }
	public virtual string Width { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlTableColElement

```
public class DomHtmlTableColElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableColElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableColElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableColElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public virtual string Ch { get; set; }
	public virtual string ChOff { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int Span { get; set; }
	public virtual string VAlign { get; set; }
	public virtual string Width { get; set; }
}
```

### New Type MonoMac.WebKit.DomHtmlTableElement

```
public class DomHtmlTableElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public virtual string BgColor { get; set; }
	public virtual string Border { get; set; }
	public virtual DomHtmlTableCaptionElement Caption { get; set; }
	public virtual string CellPadding { get; set; }
	public virtual string CellSpacing { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string FrameBorders { get; set; }
	public virtual DomHtmlCollection Rows { get; }
	public virtual string Rules { get; set; }
	public virtual string Summary { get; set; }
	public virtual DomHtmlCollection TBodies { get; }
	public virtual DomHtmlTableSectionElement TFoot { get; set; }
	public virtual DomHtmlTableSectionElement THead { get; set; }
	public virtual string Width { get; set; }
	// methods
	public virtual DomHtmlElement CreateCaption ();
	public virtual DomHtmlElement CreateTFoot ();
	public virtual DomHtmlElement CreateTHead ();
	public virtual void DeleteCaption ();
	public virtual void DeleteRow (int index);
	public virtual void DeleteTFoot ();
	public virtual void DeleteTHead ();
	protected override void Dispose (bool disposing);
	public virtual DomHtmlElement InsertRow (int index);
}
```

### New Type MonoMac.WebKit.DomHtmlTableRowElement

```
public class DomHtmlTableRowElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableRowElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableRowElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableRowElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public virtual string BgColor { get; set; }
	public virtual DomHtmlCollection Cells { get; }
	public virtual string Ch { get; set; }
	public virtual string ChOff { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int RowIndex { get; }
	public virtual int SectionRowIndex { get; }
	public virtual string VAlign { get; set; }
	// methods
	public virtual void DeleteCell (int index);
	protected override void Dispose (bool disposing);
	public virtual DomHtmlElement InsertCell (int index);
}
```

### New Type MonoMac.WebKit.DomHtmlTableSectionElement

```
public class DomHtmlTableSectionElement : MonoMac.WebKit.DomHtmlElement, IDomEventTarget, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomHtmlTableSectionElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTableSectionElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTableSectionElement (System.IntPtr handle);
	// properties
	public virtual string Align { get; set; }
	public virtual string Ch { get; set; }
	public virtual string ChOff { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual DomHtmlCollection Rows { get; }
	public virtual string VAlign { get; set; }
	// methods
	public virtual void DeleteRow (int index);
	protected override void Dispose (bool disposing);
	public virtual DomHtmlElement InsertRow (int index);
}
```

### New Type MonoMac.WebKit.DomNodeFilter

```
public abstract class DomNodeFilter : MonoMac.Foundation.NSObject, IDomNodeFilter, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomNodeFilter ();
	public DomNodeFilter (MonoMac.Foundation.NSCoder coder);
	public DomNodeFilter (MonoMac.Foundation.NSObjectFlag t);
	public DomNodeFilter (System.IntPtr handle);
	// methods
	public virtual short AcceptNode (DomNode n);
}
```

### New Type MonoMac.WebKit.DomNodeFilter_Extensions

```
public static class DomNodeFilter_Extensions {
}
```

### New Type MonoMac.WebKit.DomNodeIterator

```
public class DomNodeIterator : MonoMac.WebKit.DomObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public DomNodeIterator (MonoMac.Foundation.NSCoder coder);
	public DomNodeIterator (MonoMac.Foundation.NSObjectFlag t);
	public DomNodeIterator (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ExpandEntityReferences { get; }
	public virtual IDomNodeFilter Filter { get; }
	public virtual DomNode NextNode { get; }
	public virtual bool PointerBeforeReferenceNode { get; }
	public virtual DomNode PreviousNode { get; }
	public virtual DomNode ReferenceNode { get; }
	public virtual DomNode Root { get; }
	public virtual uint WhatToShow { get; }
	// methods
	public virtual void Detach ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.IDomEventListener

```
public interface IDomEventListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void HandleEvent (DomEvent evt);
}
```

### New Type MonoMac.WebKit.IDomNodeFilter

```
public interface IDomNodeFilter : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual short AcceptNode (DomNode n);
}
```

### New Type MonoMac.WebKit.IWebDocumentRepresentation

```
public interface IWebDocumentRepresentation : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool CanProvideDocumentSource { get; }
	public virtual string DocumentSource { get; }
	public virtual string Title { get; }
	// methods
	public virtual void FinishedLoading (WebDataSource dataSource);
	public virtual void ReceivedData (MonoMac.Foundation.NSData data, WebDataSource dataSource);
	public virtual void ReceivedError (MonoMac.Foundation.NSError error, WebDataSource dataSource);
	public virtual void SetDataSource (WebDataSource dataSource);
}
```

### New Type MonoMac.WebKit.IWebDownloadDelegate

```
public interface IWebDownloadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebFrameLoadDelegate

```
public interface IWebFrameLoadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebOpenPanelResultListener

```
public interface IWebOpenPanelResultListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebPolicyDecisionListener

```
public interface IWebPolicyDecisionListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebPolicyDelegate

```
public interface IWebPolicyDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebResourceLoadDelegate

```
public interface IWebResourceLoadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWebUIDelegate

```
public interface IWebUIDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.WebDocumentRepresentation_Extensions

```
public static class WebDocumentRepresentation_Extensions {
}
```

### New Type MonoMac.WebKit.WebDownloadDelegate_Extensions

```
public static class WebDownloadDelegate_Extensions {
	// methods
	public static MonoMac.AppKit.NSWindow OnDownloadWindowForSheet (IWebDownloadDelegate This, WebDownload download);
}
```

### New Type MonoMac.WebKit.WebFrameLoadDelegate_Extensions

```
public static class WebFrameLoadDelegate_Extensions {
	// methods
	public static void CanceledClientRedirect (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void ChangedLocationWithinPage (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void ClearedWindowObject (IWebFrameLoadDelegate This, WebView webView, WebScriptObject windowObject, WebFrame forFrame);
	public static void CommitedLoad (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void FailedLoadWithError (IWebFrameLoadDelegate This, WebView sender, MonoMac.Foundation.NSError error, WebFrame forFrame);
	public static void FailedProvisionalLoad (IWebFrameLoadDelegate This, WebView sender, MonoMac.Foundation.NSError error, WebFrame forFrame);
	public static void FinishedLoad (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void ReceivedIcon (IWebFrameLoadDelegate This, WebView sender, MonoMac.AppKit.NSImage image, WebFrame forFrame);
	public static void ReceivedServerRedirectForProvisionalLoad (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void ReceivedTitle (IWebFrameLoadDelegate This, WebView sender, string title, WebFrame forFrame);
	public static void StartedProvisionalLoad (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void WillCloseFrame (IWebFrameLoadDelegate This, WebView sender, WebFrame forFrame);
	public static void WillPerformClientRedirect (IWebFrameLoadDelegate This, WebView sender, MonoMac.Foundation.NSUrl toUrl, double secondsDelay, MonoMac.Foundation.NSDate fireDate, WebFrame forFrame);
	public static void WindowScriptObjectAvailable (IWebFrameLoadDelegate This, WebView webView, WebScriptObject windowScriptObject);
}
```

### New Type MonoMac.WebKit.WebHistory

```
public class WebHistory : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WebHistory ();
	public WebHistory (MonoMac.Foundation.NSCoder coder);
	public WebHistory (MonoMac.Foundation.NSObjectFlag t);
	public WebHistory (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int HistoryAgeInDaysLimit { get; set; }
	public virtual int HistoryItemLimit { get; set; }
	public static WebHistory OptionalSharedHistory { get; }
	public virtual MonoMac.Foundation.NSCalendarDate[] OrderedLastVisitedDays { get; }
	// methods
	public virtual void AddItems (WebHistoryItem[] newItems);
	protected override void Dispose (bool disposing);
	public virtual WebHistoryItem GetHistoryItemForUrl (MonoMac.Foundation.NSUrl url);
	public virtual WebHistoryItem[] GetOrderedItemsLastVisitedOnDay (MonoMac.Foundation.NSCalendarDate calendarDate);
	public virtual bool Load (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSError error);
	public virtual void RemoveAllItems ();
	public virtual void RemoveItems (WebHistoryItem[] items);
	public virtual bool Save (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSError error);
	public static void SetOptionalSharedHistory (WebHistory history);
}
```

### New Type MonoMac.WebKit.WebOpenPanelResultListener_Extensions

```
public static class WebOpenPanelResultListener_Extensions {
	// methods
	public static void Cancel (IWebOpenPanelResultListener This);
	public static void ChooseFilename (IWebOpenPanelResultListener This, string filename);
	public static void ChooseFilenames (IWebOpenPanelResultListener This, string[] filenames);
}
```

### New Type MonoMac.WebKit.WebPolicyDecisionListener_Extensions

```
public static class WebPolicyDecisionListener_Extensions {
	// methods
	public static void Download (IWebPolicyDecisionListener This);
	public static void Ignore (IWebPolicyDecisionListener This);
	public static void Use (IWebPolicyDecisionListener This);
}
```

### New Type MonoMac.WebKit.WebPolicyDelegate_Extensions

```
public static class WebPolicyDelegate_Extensions {
	// methods
	public static void DecidePolicyForMimeType (IWebPolicyDelegate This, WebView webView, string mimeType, MonoMac.Foundation.NSUrlRequest request, WebFrame frame, MonoMac.Foundation.NSObject decisionToken);
	public static void DecidePolicyForNavigation (IWebPolicyDelegate This, WebView webView, MonoMac.Foundation.NSDictionary actionInformation, MonoMac.Foundation.NSUrlRequest request, WebFrame frame, MonoMac.Foundation.NSObject decisionToken);
	public static void DecidePolicyForNewWindow (IWebPolicyDelegate This, WebView webView, MonoMac.Foundation.NSDictionary actionInformation, MonoMac.Foundation.NSUrlRequest request, string newFrameName, MonoMac.Foundation.NSObject decisionToken);
	public static void UnableToImplementPolicy (IWebPolicyDelegate This, WebView webView, MonoMac.Foundation.NSError error, WebFrame frame);
}
```

### New Type MonoMac.WebKit.WebResourceLoadDelegate_Extensions

```
public static class WebResourceLoadDelegate_Extensions {
	// methods
	public static void OnCancelledAuthenticationChallenge (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, MonoMac.Foundation.NSUrlAuthenticationChallenge challenge, WebDataSource dataSource);
	public static void OnFailedLoading (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, MonoMac.Foundation.NSError withError, WebDataSource dataSource);
	public static void OnFinishedLoading (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, WebDataSource dataSource);
	public static MonoMac.Foundation.NSObject OnIdentifierForInitialRequest (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSUrlRequest request, WebDataSource dataSource);
	public static void OnPlugInFailed (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSError error, WebDataSource dataSource);
	public static void OnReceivedAuthenticationChallenge (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, MonoMac.Foundation.NSUrlAuthenticationChallenge challenge, WebDataSource dataSource);
	public static void OnReceivedContentLength (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, int length, WebDataSource dataSource);
	public static void OnReceivedResponse (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, MonoMac.Foundation.NSUrlResponse responseReceived, WebDataSource dataSource);
	public static MonoMac.Foundation.NSUrlRequest OnSendRequest (IWebResourceLoadDelegate This, WebView sender, MonoMac.Foundation.NSObject identifier, MonoMac.Foundation.NSUrlRequest request, MonoMac.Foundation.NSUrlResponse redirectResponse, WebDataSource dataSource);
}
```

### New Type MonoMac.WebKit.WebUIDelegate_Extensions

```
public static class WebUIDelegate_Extensions {
	// methods
	public static bool UIAreToolbarsVisible (IWebUIDelegate This, WebView sender);
	public static void UIClose (IWebUIDelegate This, WebView sender);
	public static WebView UICreateModalDialog (IWebUIDelegate This, WebView sender, MonoMac.Foundation.NSUrlRequest request);
	public static WebView UICreateWebView (IWebUIDelegate This, WebView sender, MonoMac.Foundation.NSUrlRequest request);
	public static MonoMac.AppKit.NSEventModifierMask UIDragSourceActionMask (IWebUIDelegate This, WebView webView, System.Drawing.PointF point);
	public static void UIDrawFooterInRect (IWebUIDelegate This, WebView sender, System.Drawing.RectangleF rect);
	public static void UIDrawHeaderInRect (IWebUIDelegate This, WebView sender, System.Drawing.RectangleF rect);
	public static void UIFocus (IWebUIDelegate This, WebView sender);
	public static System.Drawing.RectangleF UIGetContentRect (IWebUIDelegate This, WebView sender);
	public static MonoMac.AppKit.NSMenuItem[] UIGetContextMenuItems (IWebUIDelegate This, WebView sender, MonoMac.Foundation.NSDictionary forElement, MonoMac.AppKit.NSMenuItem[] defaultMenuItems);
	public static MonoMac.AppKit.NSEventModifierMask UIGetDragDestinationActionMask (IWebUIDelegate This, WebView webView, MonoMac.AppKit.NSDraggingInfo draggingInfo);
	public static MonoMac.AppKit.NSResponder UIGetFirstResponder (IWebUIDelegate This, WebView sender);
	public static float UIGetFooterHeight (IWebUIDelegate This, WebView sender);
	public static System.Drawing.RectangleF UIGetFrame (IWebUIDelegate This, WebView sender);
	public static float UIGetHeaderHeight (IWebUIDelegate This, WebView sender);
	public static string UIGetStatusText (IWebUIDelegate This, WebView sender);
	public static bool UIIsResizable (IWebUIDelegate This, WebView sender);
	public static bool UIIsStatusBarVisible (IWebUIDelegate This, WebView sender);
	public static void UIMakeFirstResponder (IWebUIDelegate This, WebView sender, MonoMac.AppKit.NSResponder newResponder);
	public static void UIMouseDidMoveOverElement (IWebUIDelegate This, WebView sender, MonoMac.Foundation.NSDictionary elementInformation, MonoMac.AppKit.NSEventModifierMask modifierFlags);
	public static void UIPrintFrameView (IWebUIDelegate This, WebView sender, WebFrameView frameView);
	public static bool UIRunBeforeUnload (IWebUIDelegate This, WebView sender, string message, WebFrame initiatedByFrame);
	public static void UIRunJavaScriptAlertPanel (IWebUIDelegate This, WebView sender, string message);
	public static void UIRunJavaScriptAlertPanelMessage (IWebUIDelegate This, WebView sender, string withMessage, WebFrame initiatedByFrame);
	public static bool UIRunJavaScriptConfirmationPanel (IWebUIDelegate This, WebView sender, string withMessage, WebFrame initiatedByFrame);
	public static bool UIRunJavaScriptConfirmPanel (IWebUIDelegate This, WebView sender, string message);
	public static string UIRunJavaScriptTextInputPanel (IWebUIDelegate This, WebView sender, string prompt, string defaultText);
	public static string UIRunJavaScriptTextInputPanelWithFrame (IWebUIDelegate This, WebView sender, string prompt, string defaultText, WebFrame initiatedByFrame);
	public static void UIRunModal (IWebUIDelegate This, WebView sender);
	public static void UIRunOpenPanelForFileButton (IWebUIDelegate This, WebView sender, WebOpenPanelResultListener resultListener);
	public static void UISetContentRect (IWebUIDelegate This, WebView sender, System.Drawing.RectangleF frame);
	public static void UISetFrame (IWebUIDelegate This, WebView sender, System.Drawing.RectangleF newFrame);
	public static void UISetResizable (IWebUIDelegate This, WebView sender, bool resizable);
	public static void UISetStatusBarVisible (IWebUIDelegate This, WebView sender, bool visible);
	public static void UISetStatusText (IWebUIDelegate This, WebView sender, string text);
	public static void UISetToolbarsVisible (IWebUIDelegate This, WebView sender, bool visible);
	public static bool UIShouldPerformActionfromSender (IWebUIDelegate This, WebView webView, MonoMac.ObjCRuntime.Selector action, MonoMac.Foundation.NSObject sender);
	public static void UIShow (IWebUIDelegate This, WebView sender);
	public static void UIUnfocus (IWebUIDelegate This, WebView sender);
	public static bool UIValidateUserInterfaceItem (IWebUIDelegate This, WebView webView, MonoMac.Foundation.NSObject validatedUserInterfaceItem, bool defaultValidation);
	public static void UIWillPerformDragDestination (IWebUIDelegate This, WebView webView, WebDragDestinationAction action, MonoMac.AppKit.NSDraggingInfo draggingInfo);
	public static void UIWillPerformDragSource (IWebUIDelegate This, WebView webView, WebDragSourceAction action, System.Drawing.PointF sourcePoint, MonoMac.AppKit.NSPasteboard pasteboard);
}
```

### New Type MonoMac.WebKit.WKErrorCode

```
[Serializable]
public enum WKErrorCode {
	JavaScriptExceptionOccurred = 4,
	None = 0,
	Unknown = 1,
	WebContentProcessTerminated = 2,
	WebViewInvalidated = 3,
}
```

### New Type MonoMac.WebKit.WKNavigationActionPolicy

```
[Serializable]
public enum WKNavigationActionPolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoMac.WebKit.WKNavigationResponsePolicy

```
[Serializable]
public enum WKNavigationResponsePolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoMac.WebKit.WKNavigationType

```
[Serializable]
public enum WKNavigationType {
	BackForward = 2,
	FormResubmitted = 4,
	FormSubmitted = 1,
	LinkActivated = 0,
	Other = -1,
	Reload = 3,
}
```

### New Type MonoMac.WebKit.WKSelectionGranularity

```
[Serializable]
public enum WKSelectionGranularity {
	Character = 1,
	Dynamic = 0,
}
```

### New Type MonoMac.WebKit.WKUserScriptInjectionTime

```
[Serializable]
public enum WKUserScriptInjectionTime {
	AtDocumentEnd = 1,
	AtDocumentStart = 0,
}
```

## Removed Namespace MonoMac.AddressBook

### Removed Type MonoMac.AddressBook.ABAddressBook ### Removed Type MonoMac.AddressBook.ABAddressBookError ### Removed Type MonoMac.AddressBook.ABAuthorizationStatus ### Removed Type MonoMac.AddressBook.ABGroup ### Removed Type MonoMac.AddressBook.ABLabel ### Removed Type MonoMac.AddressBook.ABMultiValue`1 ### Removed Type MonoMac.AddressBook.ABMultiValueEntry`1 ### Removed Type MonoMac.AddressBook.ABMutableDateMultiValue ### Removed Type MonoMac.AddressBook.ABMutableDictionaryMultiValue ### Removed Type MonoMac.AddressBook.ABMutableMultiValue`1 ### Removed Type MonoMac.AddressBook.ABMutableStringMultiValue ### Removed Type MonoMac.AddressBook.ABPerson ### Removed Type MonoMac.AddressBook.ABPersonAddressKey ### Removed Type MonoMac.AddressBook.ABPersonCompositeNameFormat ### Removed Type MonoMac.AddressBook.ABPersonDateLabel ### Removed Type MonoMac.AddressBook.ABPersonImageFormat ### Removed Type MonoMac.AddressBook.ABPersonInstantMessageKey ### Removed Type MonoMac.AddressBook.ABPersonInstantMessageService ### Removed Type MonoMac.AddressBook.ABPersonKind ### Removed Type MonoMac.AddressBook.ABPersonPhoneLabel ### Removed Type MonoMac.AddressBook.ABPersonProperty ### Removed Type MonoMac.AddressBook.ABPersonRelatedNamesLabel ### Removed Type MonoMac.AddressBook.ABPersonSocialProfileService ### Removed Type MonoMac.AddressBook.ABPersonSortBy ### Removed Type MonoMac.AddressBook.ABPersonUrlLabel ### Removed Type MonoMac.AddressBook.ABPropertyType ### Removed Type MonoMac.AddressBook.ABRecord ### Removed Type MonoMac.AddressBook.ABRecordType ### Removed Type MonoMac.AddressBook.ABSource ### Removed Type MonoMac.AddressBook.ABSourceProperty ### Removed Type MonoMac.AddressBook.ABSourceType ### Removed Type MonoMac.AddressBook.ExternalChangeEventArgs ### Removed Type MonoMac.AddressBook.InstantMessageService ### Removed Type MonoMac.AddressBook.PersonAddress ### Removed Type MonoMac.AddressBook.SocialProfile 



## New Namespace MonoMac.Accounts



### New Type MonoMac.Accounts.ACAccountCredentialRenewResult

```
[Serializable]
public enum ACAccountCredentialRenewResult {
	Failed = 2,
	Rejected = 1,
	Renewed = 0,
}
```

### New Type MonoMac.Accounts.ACErrorCode

```
[Serializable]
public enum ACErrorCode {
	AccessDeniedByProtectionPolicy = 10,
	AccessInfoInvalid = 8,
	AccountAlreadyExits = 5,
	AccountAuthenticationFailed = 3,
	AccountMissingRequiredProperty = 2,
	AccountNotFound = 6,
	AccountTypeInvalid = 4,
	ClientPermissionDenied = 9,
	CoreDataSaveFailed = 18,
	CredentialNotFound = 11,
	DeniedByPlugin = 17,
	FailedSerializingAccountInfo = 19,
	FetchCredentialFailed = 12,
	InvalidClientBundleID = 16,
	InvalidCommand = 20,
	MissingMessageID = 21,
	PermissionDenied = 7,
	RemoveCredentialFailed = 14,
	StoreCredentialFailed = 13,
	Unknown = 1,
	UpdatingNonexistentAccount = 15,
}
```

## New Namespace MonoMac.AVKit



### New Type MonoMac.AVKit.AVPlayerViewControlsStyle

```
[Serializable]
public enum AVPlayerViewControlsStyle {
	Default = 1,
	Floating = 2,
	Inline = 1,
	Minimal = 3,
	None = 0,
}
```

## New Namespace MonoMac.CloudKit



### New Type MonoMac.CloudKit.CKAccountStatus

```
[Serializable]
public enum CKAccountStatus {
	Available = 1,
	CouldNotDetermine = 0,
	NoAccount = 3,
	Restricted = 2,
}
```

### New Type MonoMac.CloudKit.CKApplicationPermissions

```
[Serializable]
[Flags]
public enum CKApplicationPermissions {
	UserDiscoverability = 1,
}
```

### New Type MonoMac.CloudKit.CKApplicationPermissionStatus

```
[Serializable]
public enum CKApplicationPermissionStatus {
	CouldNotComplete = 1,
	Denied = 2,
	Granted = 3,
	InitialState = 0,
}
```

### New Type MonoMac.CloudKit.CKErrorCode

```
[Serializable]
public enum CKErrorCode {
	AssetFileModified = 17,
	AssetFileNotFound = 16,
	BadContainer = 5,
	BadDatabase = 24,
	BatchRequestFailed = 22,
	ChangeTokenExpired = 21,
	ConstraintViolation = 19,
	IncompatibleVersion = 18,
	InternalError = 1,
	InvalidArguments = 12,
	LimitExceeded = 27,
	MissingEntitlement = 8,
	NetworkFailure = 4,
	NetworkUnavailable = 3,
	None = 0,
	NotAuthenticated = 9,
	OperationCancelled = 20,
	PartialFailure = 2,
	PermissionFailure = 10,
	QuotaExceeded = 25,
	RequestRateLimited = 7,
	ResultsTruncated = 13,
	ServerRecordChanged = 14,
	ServerRejectedRequest = 15,
	ServiceUnavailable = 6,
	UnknownItem = 11,
	UserDeletedZone = 28,
	ZoneBusy = 23,
	ZoneNotFound = 26,
}
```

### New Type MonoMac.CloudKit.CKNotificationType

```
[Serializable]
public enum CKNotificationType {
	Query = 1,
	ReadNotification = 3,
	RecordZone = 2,
}
```

### New Type MonoMac.CloudKit.CKQueryNotificationReason

```
[Serializable]
public enum CKQueryNotificationReason {
	RecordCreated = 1,
	RecordDeleted = 3,
	RecordUpdated = 2,
}
```

### New Type MonoMac.CloudKit.CKRecord

```
public class CKRecord {
	// constructors
	public CKRecord ();
}
```

### New Type MonoMac.CloudKit.CKRecordSavePolicy

```
[Serializable]
public enum CKRecordSavePolicy {
	SaveAllKeys = 2,
	SaveChangedKeys = 1,
	SaveIfServerRecordUnchanged = 0,
}
```

### New Type MonoMac.CloudKit.CKRecordZoneCapabilities

```
[Serializable]
[Flags]
public enum CKRecordZoneCapabilities {
	Atomic = 2,
	FetchChanges = 1,
}
```

### New Type MonoMac.CloudKit.CKReferenceAction

```
[Serializable]
public enum CKReferenceAction {
	DeleteSelf = 1,
	None = 0,
}
```

### New Type MonoMac.CloudKit.CKSubscriptionOptions

```
[Serializable]
[Flags]
public enum CKSubscriptionOptions {
	FiresOnce = 8,
	FiresOnRecordCreation = 1,
	FiresOnRecordDeletion = 4,
	FiresOnRecordUpdate = 2,
}
```

### New Type MonoMac.CloudKit.CKSubscriptionType

```
[Serializable]
public enum CKSubscriptionType {
	Query = 1,
	RecordZone = 2,
}
```

## New Namespace MonoMac.EventKit



### New Type MonoMac.EventKit.EKAlarmProximity

```
[Serializable]
public enum EKAlarmProximity {
	Enter = 1,
	Leave = 2,
	None = 0,
}
```

### New Type MonoMac.EventKit.EKAlarmType

```
[Serializable]
public enum EKAlarmType {
	Audio = 1,
	Display = 0,
	Email = 3,
	Procedure = 2,
}
```

### New Type MonoMac.EventKit.EKAuthorizationStatus

```
[Serializable]
public enum EKAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
```

### New Type MonoMac.EventKit.EKCalendarEventAvailability

```
[Serializable]
[Flags]
public enum EKCalendarEventAvailability {
	Busy = 1,
	Free = 2,
	None = 0,
	Tentative = 4,
	Unavailable = 8,
}
```

### New Type MonoMac.EventKit.EKCalendarType

```
[Serializable]
public enum EKCalendarType {
	Birthday = 4,
	CalDav = 1,
	Exchange = 2,
	Local = 0,
	Subscription = 3,
}
```

### New Type MonoMac.EventKit.EKDay

```
[Serializable]
public enum EKDay {
	Friday = 6,
	Monday = 2,
	NotSet = 0,
	Saturday = 7,
	Sunday = 1,
	Thursday = 5,
	Tuesday = 3,
	Wednesday = 4,
}
```

### New Type MonoMac.EventKit.EKEntityMask

```
[Serializable]
[Flags]
public enum EKEntityMask {
	Event = 1,
	Reminder = 2,
}
```

### New Type MonoMac.EventKit.EKEntityType

```
[Serializable]
public enum EKEntityType {
	Event = 0,
	Reminder = 1,
}
```

### New Type MonoMac.EventKit.EKErrorCode

```
[Serializable]
public enum EKErrorCode {
	AlarmGreaterThanRecurrence = 8,
	AlarmProximityNotSupported = 21,
	CalendarDoesNotAllowEvents = 22,
	CalendarDoesNotAllowReminders = 23,
	CalendarHasNoSource = 14,
	CalendarIsImmutable = 16,
	CalendarReadOnly = 6,
	CalendarSourceCannotBeModified = 15,
	DatesInverted = 4,
	DurationGreaterThanRecurrence = 7,
	EventNotMutable = 0,
	InternalFailure = 5,
	InvalidSpan = 13,
	InvitesCannotBeMoved = 12,
	NoCalendar = 1,
	NoEndDate = 3,
	NoStartDate = 2,
	ObjectBelongsToDifferentStore = 11,
	RecurringReminderRequiresDueDate = 18,
	ReminderLocationsNotSupported = 20,
	SourceDoesNotAllowCalendarAddDelete = 17,
	SourceDoesNotAllowEvents = 25,
	SourceDoesNotAllowReminders = 24,
	StartDateCollidesWithOtherOccurrence = 10,
	StartDateTooFarInFuture = 9,
	StructuredLocationsNotSupported = 19,
}
```

### New Type MonoMac.EventKit.EKEventAvailability

```
[Serializable]
public enum EKEventAvailability {
	Busy = 0,
	Free = 1,
	NotSupported = -1,
	Tentative = 2,
	Unavailable = 3,
}
```

### New Type MonoMac.EventKit.EKEventEditViewAction

```
[Serializable]
public enum EKEventEditViewAction {
	Canceled = 0,
	Deleted = 2,
	Saved = 1,
}
```

### New Type MonoMac.EventKit.EKEventStatus

```
[Serializable]
public enum EKEventStatus {
	Cancelled = 3,
	Confirmed = 1,
	None = 0,
	Tentative = 2,
}
```

### New Type MonoMac.EventKit.EKEventViewAction

```
[Serializable]
public enum EKEventViewAction {
	Deleted = 2,
	Done = 0,
	Responded = 1,
}
```

### New Type MonoMac.EventKit.EKParticipantRole

```
[Serializable]
public enum EKParticipantRole {
	Chair = 3,
	NonParticipant = 4,
	Optional = 2,
	Required = 1,
	Unknown = 0,
}
```

### New Type MonoMac.EventKit.EKParticipantStatus

```
[Serializable]
public enum EKParticipantStatus {
	Accepted = 2,
	Completed = 6,
	Declined = 3,
	Delegated = 5,
	InProcess = 7,
	Pending = 1,
	Tentative = 4,
	Unknown = 0,
}
```

### New Type MonoMac.EventKit.EKParticipantType

```
[Serializable]
public enum EKParticipantType {
	Group = 4,
	Person = 1,
	Resource = 3,
	Room = 2,
	Unknown = 0,
}
```

### New Type MonoMac.EventKit.EKRecurrenceFrequency

```
[Serializable]
public enum EKRecurrenceFrequency {
	Daily = 0,
	Monthly = 2,
	Weekly = 1,
	Yearly = 3,
}
```

### New Type MonoMac.EventKit.EKSourceType

```
[Serializable]
public enum EKSourceType {
	Birthdays = 5,
	CalDav = 2,
	Exchange = 1,
	Local = 0,
	MobileMe = 3,
	Subscribed = 4,
}
```

### New Type MonoMac.EventKit.EKSpan

```
[Serializable]
public enum EKSpan {
	FutureEvents = 1,
	ThisEvent = 0,
}
```

## New Namespace MonoMac.GameController



### New Type MonoMac.GameController.GCController

```
public class GCController {
	// constructors
	public GCController ();
	// fields
	public static const int PlayerIndexUnset;
}
```

### New Type MonoMac.GameController.GCExtendedGamepadSnapshot

```
public class GCExtendedGamepadSnapshot {
	// constructors
	public GCExtendedGamepadSnapshot ();
	// methods
	public static bool TryGetSnapShotData (MonoMac.Foundation.NSData data, out GCExtendedGamepadSnapShotDataV100 snapshotData);
}
```

### New Type MonoMac.GameController.GCExtendedGamepadSnapShotDataV100

```
public struct GCExtendedGamepadSnapShotDataV100 {
	// fields
	public float ButtonA;
	public float ButtonB;
	public float ButtonX;
	public float ButtonY;
	public float DPadX;
	public float DPadY;
	public float LeftShoulder;
	public float LeftThumbstickX;
	public float LeftThumbstickY;
	public float LeftTrigger;
	public float RightShoulder;
	public float RightThumbstickX;
	public float RightThumbstickY;
	public float RightTrigger;
	public ushort Size;
	public ushort Version;
	// methods
	public MonoMac.Foundation.NSData ToNSData ();
}
```

### New Type MonoMac.GameController.GCGamepadSnapshot

```
public class GCGamepadSnapshot {
	// constructors
	public GCGamepadSnapshot ();
	// methods
	public static bool TryGetSnapshotData (MonoMac.Foundation.NSData data, out GCGamepadSnapShotDataV100 snapshotData);
}
```

### New Type MonoMac.GameController.GCGamepadSnapShotDataV100

```
public struct GCGamepadSnapShotDataV100 {
	// fields
	public float ButtonA;
	public float ButtonB;
	public float ButtonX;
	public float ButtonY;
	public float DPadX;
	public float DPadY;
	public float LeftShoulder;
	public float RightShoulder;
	public ushort Size;
	public ushort Version;
	// methods
	public MonoMac.Foundation.NSData ToNSData ();
}
```

## New Namespace MonoMac.GLKit



### New Type MonoMac.GLKit.GLKFogMode

```
[Serializable]
public enum GLKFogMode {
	Exp = 0,
	Exp2 = 1,
	Linear = 2,
}
```

### New Type MonoMac.GLKit.GLKLightingType

```
[Serializable]
public enum GLKLightingType {
	PerPixel = 1,
	PerVertex = 0,
}
```

### New Type MonoMac.GLKit.GLKNamedEffect

```
public abstract class GLKNamedEffect : MonoMac.Foundation.NSObject, IGLKNamedEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public GLKNamedEffect ();
	public GLKNamedEffect (MonoMac.Foundation.NSCoder coder);
	public GLKNamedEffect (MonoMac.Foundation.NSObjectFlag t);
	public GLKNamedEffect (System.IntPtr handle);
	// methods
	public virtual void PrepareToDraw ();
}
```

### New Type MonoMac.GLKit.GLKNamedEffect_Extensions

```
public static class GLKNamedEffect_Extensions {
}
```

### New Type MonoMac.GLKit.GLKTextureEnvMode

```
[Serializable]
public enum GLKTextureEnvMode {
	Decal = 2,
	Modulate = 1,
	Replace = 0,
}
```

### New Type MonoMac.GLKit.GLKTextureInfoAlphaState

```
[Serializable]
public enum GLKTextureInfoAlphaState {
	None = 0,
	NonPremultiplied = 1,
	Premultiplied = 2,
}
```

### New Type MonoMac.GLKit.GLKTextureInfoOrigin

```
[Serializable]
public enum GLKTextureInfoOrigin {
	BottomLeft = 2,
	TopLeft = 1,
	Unknown = 0,
}
```

### New Type MonoMac.GLKit.GLKTextureLoaderError

```
[Serializable]
public enum GLKTextureLoaderError {
	AlphaPremultiplicationFailure = 16,
	CompressedTextureUpload = 7,
	CubeMapInvalidNumFiles = 6,
	DataPreprocessingFailure = 12,
	FileOrURLNotFound = 0,
	IncompatibleFormatSRGB = 18,
	InvalidCGImage = 2,
	InvalidEAGLContext = 17,
	InvalidNSData = 1,
	MipmapUnsupported = 13,
	PVRAtlasUnsupported = 5,
	ReorientationFailure = 15,
	UncompressedTextureUpload = 8,
	UnknownFileType = 4,
	UnknownPathType = 3,
	UnsupportedBitDepth = 10,
	UnsupportedCubeMapDimensions = 9,
	UnsupportedOrientation = 14,
	UnsupportedPVRFormat = 11,
}
```

### New Type MonoMac.GLKit.GLKTextureTarget

```
[Serializable]
public enum GLKTextureTarget {
	CubeMap = 34067,
	TargetCt = 2,
	Texture2D = 3553,
}
```

### New Type MonoMac.GLKit.GLKVertexAttrib

```
[Serializable]
public enum GLKVertexAttrib {
	Color = 2,
	Normal = 1,
	Position = 0,
	TexCoord0 = 3,
	TexCoord1 = 4,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableColorFormat

```
[Serializable]
public enum GLKViewDrawableColorFormat {
	RGB565 = 1,
	RGBA8888 = 0,
	SRGBA8888 = 2,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableDepthFormat

```
[Serializable]
public enum GLKViewDrawableDepthFormat {
	Format16 = 1,
	Format24 = 2,
	None = 0,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableMultisample

```
[Serializable]
public enum GLKViewDrawableMultisample {
	None = 0,
	Sample4x = 1,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableStencilFormat

```
[Serializable]
public enum GLKViewDrawableStencilFormat {
	Format8 = 1,
	FormatNone = 0,
}
```

### New Type MonoMac.GLKit.IGLKNamedEffect

```
public interface IGLKNamedEffect : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void PrepareToDraw ();
}
```

## New Namespace MonoMac.LocalAuthentication



### New Type MonoMac.LocalAuthentication.LAPolicy

```
[Serializable]
public enum LAPolicy {
	DeviceOwnerAuthenticationWithBiometrics = 1,
}
```

### New Type MonoMac.LocalAuthentication.LAStatus

```
[Serializable]
public enum LAStatus {
	AuthenticationFailed = -1,
	PasscodeNotSet = -5,
	Success = 0,
	SystemCancel = -4,
	TouchIDNotAvailable = -6,
	TouchIDNotEnrolled = -7,
	UserCancel = -2,
	UserFallback = -3,
}
```

## New Namespace MonoMac.MediaAccessibility



### New Type MonoMac.MediaAccessibility.MACaptionAppearance

```
public static class MACaptionAppearance {
	// fields
	public static MonoMac.Foundation.NSString MediaCharacteristicDescribesMusicAndSoundForAccessibility;
	public static MonoMac.Foundation.NSString MediaCharacteristicTranscribesSpokenDialogForAccessibility;
	public static MonoMac.Foundation.NSString SettingsChangedNotification;
	// methods
	public static bool AddSelectedLanguage (MACaptionAppearanceDomain domain, string language);
	public static MonoMac.CoreGraphics.CGColor GetBackgroundColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetBackgroundOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MACaptionAppearanceDisplayType GetDisplayType (MACaptionAppearanceDomain domain);
	public static MonoMac.CoreText.CTFontDescriptor GetFontDescriptor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior, MACaptionAppearanceFontStyle fontStyle);
	public static MonoMac.CoreGraphics.CGColor GetForegroundColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetForegroundOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MonoMac.Foundation.NSString[] GetPreferredCaptioningMediaCharacteristics (MACaptionAppearanceDomain domain);
	public static float GetRelativeCharacterSize (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static string[] GetSelectedLanguages (MACaptionAppearanceDomain domain);
	public static MACaptionAppearanceTextEdgeStyle GetTextEdgeStyle (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MonoMac.CoreGraphics.CGColor GetWindowColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetWindowOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetWindowRoundedCornerRadius (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static void SetDisplayType (MACaptionAppearanceDomain domain, MACaptionAppearanceDisplayType displayType);
}
```

### New Type MonoMac.MediaAccessibility.MACaptionAppearanceBehavior

```
[Serializable]
public enum MACaptionAppearanceBehavior {
	UseContentIfAvailable = 1,
	UseValue = 0,
}
```

### New Type MonoMac.MediaAccessibility.MACaptionAppearanceDisplayType

```
[Serializable]
public enum MACaptionAppearanceDisplayType {
	AlwaysOn = 2,
	Automatic = 1,
	ForcedOnly = 0,
}
```

### New Type MonoMac.MediaAccessibility.MACaptionAppearanceDomain

```
[Serializable]
public enum MACaptionAppearanceDomain {
	Default = 0,
	User = 1,
}
```

### New Type MonoMac.MediaAccessibility.MACaptionAppearanceFontStyle

```
[Serializable]
public enum MACaptionAppearanceFontStyle {
	Casual = 5,
	Cursive = 6,
	Default = 0,
	MonospacedWithoutSerif = 3,
	MonospacedWithSerif = 1,
	ProportionalWithoutSerif = 4,
	ProportionalWithSerif = 2,
	SmallCapital = 7,
}
```

### New Type MonoMac.MediaAccessibility.MACaptionAppearanceTextEdgeStyle

```
[Serializable]
public enum MACaptionAppearanceTextEdgeStyle {
	Depressed = 3,
	DropShadow = 5,
	None = 1,
	Raised = 2,
	Undefined = 0,
	Uniform = 4,
}
```

## New Namespace MonoMac.NetworkExtension



### New Type MonoMac.NetworkExtension.NEEvaluateConnectionRuleAction

```
[Serializable]
public enum NEEvaluateConnectionRuleAction {
	ConnectIfNeeded = 1,
	NeverConnect = 2,
}
```

### New Type MonoMac.NetworkExtension.NEOnDemandRuleAction

```
[Serializable]
public enum NEOnDemandRuleAction {
	Connect = 1,
	Disconnect = 2,
	EvaluateConnection = 3,
	Ignore = 4,
}
```

### New Type MonoMac.NetworkExtension.NEOnDemandRuleInterfaceType

```
[Serializable]
public enum NEOnDemandRuleInterfaceType {
	Cellular = 3,
	Ethernet = 1,
	WiFi = 2,
}
```

### New Type MonoMac.NetworkExtension.NEVpnError

```
[Serializable]
public enum NEVpnError {
	ConfigurationDisabled = 2,
	ConfigurationInvalid = 1,
	ConfigurationStale = 4,
	ConnectionFailed = 3,
}
```

### New Type MonoMac.NetworkExtension.NEVpnIke2DeadPeerDetectionRate

```
[Serializable]
public enum NEVpnIke2DeadPeerDetectionRate {
	High = 3,
	Low = 1,
	Medium = 2,
	None = 0,
}
```

### New Type MonoMac.NetworkExtension.NEVpnIke2DiffieHellman

```
[Serializable]
public enum NEVpnIke2DiffieHellman {
	Group0 = 0,
	Group1 = 1,
	Group14 = 14,
	Group15 = 15,
	Group16 = 16,
	Group17 = 17,
	Group18 = 18,
	Group2 = 2,
	Group5 = 5,
}
```

### New Type MonoMac.NetworkExtension.NEVpnIke2EncryptionAlgorithm

```
[Serializable]
public enum NEVpnIke2EncryptionAlgorithm {
	AES128 = 3,
	AES256 = 4,
	DES = 1,
	TripleDES = 2,
}
```

### New Type MonoMac.NetworkExtension.NEVpnIke2IntegrityAlgorithm

```
[Serializable]
public enum NEVpnIke2IntegrityAlgorithm {
	SHA160 = 2,
	SHA256 = 3,
	SHA384 = 4,
	SHA512 = 5,
	SHA96 = 1,
}
```

### New Type MonoMac.NetworkExtension.NEVpnIkeAuthenticationMethod

```
[Serializable]
public enum NEVpnIkeAuthenticationMethod {
	Certificate = 1,
	None = 0,
	SharedSecret = 2,
}
```

### New Type MonoMac.NetworkExtension.NEVpnStatus

```
[Serializable]
public enum NEVpnStatus {
	Connected = 3,
	Connecting = 2,
	Disconnected = 1,
	Disconnecting = 5,
	Invalid = 0,
	Reasserting = 4,
}
```

## New Namespace MonoMac.SpriteKit



### New Type MonoMac.SpriteKit.SKActionTimingMode

```
[Serializable]
public enum SKActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type MonoMac.SpriteKit.SKBlendMode

```
[Serializable]
public enum SKBlendMode {
	Add = 1,
	Alpha = 0,
	Multiply = 3,
	MultiplyX2 = 4,
	Replace = 6,
	Screen = 5,
	Subtract = 2,
}
```

### New Type MonoMac.SpriteKit.SKInterpolationMode

```
[Serializable]
public enum SKInterpolationMode {
	Linear = 1,
	Spline = 2,
	Step = 3,
}
```

### New Type MonoMac.SpriteKit.SKLabelHorizontalAlignmentMode

```
[Serializable]
public enum SKLabelHorizontalAlignmentMode {
	Center = 0,
	Left = 1,
	Right = 2,
}
```

### New Type MonoMac.SpriteKit.SKLabelVerticalAlignmentMode

```
[Serializable]
public enum SKLabelVerticalAlignmentMode {
	Baseline = 0,
	Bottom = 3,
	Center = 1,
	Top = 2,
}
```

### New Type MonoMac.SpriteKit.SKRepeatMode

```
[Serializable]
public enum SKRepeatMode {
	Clamp = 1,
	Loop = 2,
}
```

### New Type MonoMac.SpriteKit.SKSceneScaleMode

```
[Serializable]
public enum SKSceneScaleMode {
	AspectFill = 1,
	AspectFit = 2,
	Fill = 0,
	ResizeFill = 3,
}
```

### New Type MonoMac.SpriteKit.SKTextureFilteringMode

```
[Serializable]
public enum SKTextureFilteringMode {
	Linear = 1,
	Nearest = 0,
}
```

### New Type MonoMac.SpriteKit.SKTransitionDirection

```
[Serializable]
public enum SKTransitionDirection {
	Down = 1,
	Left = 3,
	Right = 2,
	Up = 0,
}
```

### New Type MonoMac.SpriteKit.SKUniformType

```
[Serializable]
public enum SKUniformType {
	Float = 1,
	FloatMatrix2 = 5,
	FloatMatrix3 = 6,
	FloatMatrix4 = 7,
	FloatVector2 = 2,
	FloatVector3 = 3,
	FloatVector4 = 4,
	None = 0,
	Texture = 8,
}
```

## New Namespace MonoTouch.GameController



### New Type MonoTouch.GameController.GCControllerAxisInput

```
public class GCControllerAxisInput {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCControllerAxisInput ();
}
```

### New Type MonoTouch.GameController.GCControllerButtonInput

```
public class GCControllerButtonInput {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCControllerButtonInput ();
}
```

### New Type MonoTouch.GameController.GCControllerDirectionPad

```
public class GCControllerDirectionPad {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCControllerDirectionPad ();
}
```

### New Type MonoTouch.GameController.GCControllerElement

```
public class GCControllerElement {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCControllerElement ();
}
```

### New Type MonoTouch.GameController.GCExtendedGamepad

```
public class GCExtendedGamepad {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCExtendedGamepad ();
}
```

### New Type MonoTouch.GameController.GCGamepad

```
public class GCGamepad {
	// constructors

	[Obsolete ("Cannot create a default instance")]
	public GCGamepad ();
}
```
