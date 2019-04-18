---
id: 3F3AE9A4-EC39-4F9E-81BA-9A9F15B14062
title: "From 1.2 to 1.4"
---

<html><head><title>Comparison between XamMac.1.2.dll and XamMac.dll</title></head>
<body>
<p>This document describes API additions from Xamarin.Mac 1.2 to Xamarin.Mac
1.4. Most of the changes are new APIs supporting strongly-typed notifications in
AppKit, the introduction of CFPreferences, CaptiveNetwork, and
NetworkReachability APIs, and enhancements to WebKit.</p>

<h2>Namespace: MonoMac</h2>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Added:</p><pre>
 	public const string SystemConfigurationLibrary = "/System/Library/Frameworks/SystemConfiguration.framework/SystemConfiguration";
</pre>
<h2>Namespace: MonoMac.AVFoundation</h2>
<h3>Type Changed: MonoMac.AVFoundation.AVAsset</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task LoadValuesTaskAsync (string [] keys);
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetExportSession</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task ExportTaskAsync ();
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureStillImageOutput</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoMac.CoreMedia.CMSampleBuffer&gt; CaptureStillImageTaskAsync (AVCaptureConnection connection);
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVMetadataItem</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task LoadValuesTaskAsync (string [] keys);
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayer</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; PrerollAsync (float rate);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.CoreMedia.CMTime time);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.CoreMedia.CMTime time, MonoMac.CoreMedia.CMTime toleranceBefore, MonoMac.CoreMedia.CMTime toleranceAfter);
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItem</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.CoreMedia.CMTime time);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.CoreMedia.CMTime time, MonoMac.CoreMedia.CMTime toleranceBefore, MonoMac.CoreMedia.CMTime toleranceAfter);
</pre>
<h2>Namespace: MonoMac.AppKit</h2>
<h3>Type Changed: MonoMac.AppKit.NSAnimation</h3>
<p>Added:</p><pre>
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveProgressMark (EventHandler&lt;NSAnimationProgressMarkEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSAnimationProgressMarkEventArgs</h3>
<pre>
public class NSAnimationProgressMarkEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSAnimationProgressMarkEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public float Progress {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSApplication</h3>
<p>Added:</p><pre>
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidBecomeActive (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeScreenParameters (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidFinishLaunching (EventHandler&lt;NSApplicationDidFinishLaunchingEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidFinishRestoringWindows (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidHide (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidResignActive (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidUnhide (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidUpdate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillBecomeActive (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillFinishLaunching (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillHide (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillResignActive (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillTerminate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillUnhide (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillUpdate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSApplicationDidFinishLaunchingEventArgs</h3>
<pre>
public class NSApplicationDidFinishLaunchingEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSApplicationDidFinishLaunchingEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public bool IsLaunchDefault {
		get;
	}
	public bool IsLaunchFromUserNotification {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSBitmapImageRep</h3>
<p>Added:</p><pre>
 	[Obsolete("Use GetCompressionFactor instead")]
	public void GetCompressionfactor (out NSTiffCompression compression, out float factor);
 	[Obsolete("Use SetCompressionFactor instead")]
	public void SetCompressionfactor (NSTiffCompression compression, float factor);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSBrowser</h3>
<p>Removed:</p><pre>
 		set;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use GetItem instead")]
	public MonoMac.Foundation.NSObject ItemAtRowinColumn (int row, int column);
 	public virtual void SetCellClass (MonoMac.ObjCRuntime.Class factoryId);
 	}
 	public static MonoMac.Foundation.NSString ColumnConfigurationChangedNotification {
 		get;
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveColumnConfigurationChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSBrowserDelegate</h3>
<p>Added:</p><pre>
 	[Obsolete("Use DidChangeLastColumn instead")]
	public void DidChangeLastColumntoColumn (NSBrowser browser, int oldLastColumn, int toColumn);
 	[Obsolete("Use SelectRowInColumn instead")]
	public bool SelectRowinColumn (NSBrowser sender, int row, int column);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSCell</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ControlTintChangedNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveControlTintChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSColor</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString SystemColorsChanged {
 		get;
 	}
 	public static NSColor UnderPageBackground {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveSystemColorsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSColorPanel</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ColorChangedNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveColorChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSComboBox</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString SelectionDidChangeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString SelectionIsChangingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillDismissNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillPopUpNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillDismiss (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillPopUp (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSControl</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString TextDidBeginEditingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextDidChangeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextDidEndEditingNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveTextDidBeginEditing (EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveTextDidChange (EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveTextDidEndEditing (EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSControlTextEditingEventArgs</h3>
<pre>
public class NSControlTextEditingEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSControlTextEditingEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSTextView FieldEditor {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSDocumentController</h3>
<p>Added:</p><pre>
 	[Obsolete("Use RunModalOpenPanelforTypes instead")]
	public int RunModalOpenPanelforTypes (NSOpenPanel openPanel, string [] types);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSDrawer</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString DidCloseNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidOpenNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillCloseNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillOpenNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidClose (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidOpen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillClose (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillOpen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSEvent</h3>
<p>Added:</p><pre>
 	[Obsolete("Use TouchesMatchingPhase instead")]
	public MonoMac.Foundation.NSSet TouchesMatchingPhaseinView (NSTouchPhase phase, NSView view);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSFont</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString AntialiasThresholdChangedNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString FontSetChangedNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveAntialiasThresholdChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveFontSetChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSFontCollection</h3>
<p>Removed:</p><pre>
 	public static MonoMac.Foundation.NSString DidChangeNotification {
</pre>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ChangedNotification {
 		get;
 	}
 	[Obsolete("Use ChangedNotification instead")]
	public static MonoMac.Foundation.NSString DidChangeNotification {
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveChanged (EventHandler&lt;NSFontCollectionChangedEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSFontCollectionAction</h3>
<pre>
[Serializable]
public enum NSFontCollectionAction {
	Unknown,
	Shown,
	Hidden,
	Renamed
}
</pre>
<h3>New Type: MonoMac.AppKit.NSFontCollectionChangedEventArgs</h3>
<pre>
public class NSFontCollectionChangedEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSFontCollectionChangedEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSFontCollectionAction Action {
		get;
	}
	public string Name {
		get;
	}
	public string OldName {
		get;
	}
	public NSFontCollectionVisibility Visibility {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSHelpManager</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ContextHelpModeDidActivateNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ContextHelpModeDidDeactivateNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveContextHelpModeDidActivate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveContextHelpModeDidDeactivate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSImage</h3>
<p>Added:</p><pre>
 	public static NSImage ImageNamed (NSImageName name);
 	public MonoMac.CoreGraphics.CGImage CGImage {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSImageName</h3>
<pre>
[Serializable]
public enum NSImageName {
	QuickLookTemplate,
	BluetoothTemplate,
	IChatTheaterTemplate,
	SlideshowTemplate,
	ActionTemplate,
	SmartBadgeTemplate,
	PathTemplate,
	InvalidDataFreestandingTemplate,
	LockLockedTemplate,
	LockUnlockedTemplate,
	GoRightTemplate,
	GoLeftTemplate,
	RightFacingTriangleTemplate,
	LeftFacingTriangleTemplate,
	AddTemplate,
	RemoveTemplate,
	RevealFreestandingTemplate,
	FollowLinkFreestandingTemplate,
	EnterFullScreenTemplate,
	ExitFullScreenTemplate,
	StopProgressTemplate,
	StopProgressFreestandingTemplate,
	RefreshTemplate,
	RefreshFreestandingTemplate,
	Folder,
	TrashEmpty,
	TrashFull,
	HomeTemplate,
	BookmarksTemplate,
	Caution,
	StatusAvailable,
	StatusPartiallyAvailable,
	StatusUnavailable,
	StatusNone,
	ApplicationIcon,
	MenuOnStateTemplate,
	MenuMixedStateTemplate,
	UserGuest,
	MobileMe
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSImageRep</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString RegistryDidChangeNotification {
 		get;
 	}
 	public MonoMac.CoreGraphics.CGImage CGImage {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveRegistryDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSMatrix</h3>
<p>Added:</p><pre>
 	[Obsolete("Use GetRowColumnForPoint instead")]
	public bool GetRowCoumnForPoint (out int row, out int column, System.Drawing.PointF aPoint);
 	[Obsolete("Use HighlightCell instead")]
	public void HighlightCellatRowColumn (bool highlight, int row, int column);
 	[Obsolete("Use InsertColumn instead")]
	public void InsertColumnwithCells (int column, NSCell[] newCells);
 	[Obsolete("Use MakeCell instead")]
	public NSCell MakeCellAtRowcolumn (int row, int col);
 	[Obsolete("Use PutCell instead")]
	public void PutCellatRowColumn (NSCell newCell, int row, int column);
 	[Obsolete("Use ScrollCellToVisible instead")]
	public void ScrollCellToVisibleAtRowcolumn (int row, int column);
 	[Obsolete("Use SelectCell instead")]
	public void SelectCellAtRowcolumn (int row, int column);
 	[Obsolete("Use SetToolTipForCell instead")]
	public void SetToolTipforCell (string toolTipString, NSCell cell);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSMenu</h3>
<p>Added:</p><pre>
 	[Obsolete("Use InsertItem instead")]
	public void InsertItematIndex (NSMenuItem newItem, int index);
 	public static MonoMac.Foundation.NSString DidAddItemNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidBeginTrackingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidChangeItemNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidEndTrackingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidRemoveItemNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidSendActionNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillSendActionNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidAddItem (EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidBeginTracking (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeItem (EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEndTracking (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidRemoveItem (EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidSendAction (EventHandler&lt;NSMenuItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillSendAction (EventHandler&lt;NSMenuItemEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSMenuItemEventArgs</h3>
<pre>
public class NSMenuItemEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSMenuItemEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSMenu MenuItem {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.AppKit.NSMenuItemIndexEventArgs</h3>
<pre>
public class NSMenuItemIndexEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSMenuItemIndexEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public int MenuItemIndex {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSMenuView</h3>
<p>Removed:</p><pre>
 	public NSMenuView (int tokenInitAsTearOff);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSOutlineView</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ColumnDidMoveNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ColumnDidResizeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ItemDidCollapseNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ItemDidExpandNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ItemWillCollapseNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ItemWillExpandNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString SelectionDidChangeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString SelectionIsChangingNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveColumnDidMove (EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveColumnDidResize (EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveItemDidCollapse (EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveItemDidExpand (EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveItemWillCollapse (EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveItemWillExpand (EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSOutlineViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual string ToolTipForCell (NSOutlineView outlineView, NSCell cell, ref System.Drawing.RectangleF rect, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item, System.Drawing.PointF mouseLocation);
</pre>
<h3>New Type: MonoMac.AppKit.NSOutlineViewItemEventArgs</h3>
<pre>
public class NSOutlineViewItemEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSOutlineViewItemEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public MonoMac.Foundation.NSObject Item {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButton</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString WillPopUpNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveWillPopUp (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButtonCell</h3>
<p>Removed:</p><pre>
 	public NSMenuItem this [int idx] {
 	public NSMenuItem this [string title] {
</pre>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString WillPopUpNotification {
 		get;
 	}
 	public NSMenuItem this [string title] {
 	public NSMenuItem this [int idx] {
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveWillPopUp (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPopover</h3>
<p>Added:</p><pre>
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidClose (EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidShow (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillClose (EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillShow (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSPopoverCloseEventArgs</h3>
<pre>
public class NSPopoverCloseEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSPopoverCloseEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSPopoverCloseReason Reason {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.AppKit.NSPopoverCloseReason</h3>
<pre>
[Serializable]
public enum NSPopoverCloseReason {
	Unknown,
	Standard,
	DetachToWindow
}
</pre>
<h3>New Type: MonoMac.AppKit.NSPrintPreviewGraphicsContext</h3>
<pre>
public class NSPrintPreviewGraphicsContext : NSGraphicsContext {
	
	public NSPrintPreviewGraphicsContext (MonoMac.Foundation.NSCoder coder);
	public NSPrintPreviewGraphicsContext (MonoMac.Foundation.NSObjectFlag t);
	public NSPrintPreviewGraphicsContext (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSRuleEditor</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString RowsDidChangeNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveRowsDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSScreen</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ColorSpaceDidChangeNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveColorSpaceDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSScroller</h3>
<p>Removed:</p><pre>
 	public static MonoMac.Foundation.NSString NSPreferredScrollerStyleDidChangeNotification {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use DrawArrow instead")]
	public void DrawArrowhighlight (NSScrollerArrow whichArrow, bool highlight);
 	[Obsolete("Use PreferredStyleChangedNotification")]
	public static MonoMac.Foundation.NSString NSPreferredScrollerStyleDidChangeNotification {
 	public static MonoMac.Foundation.NSString PreferredStyleChangedNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObservePreferredStyleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSSplitView</h3>
<p>Added:</p><pre>
 	[Obsolete("Use SetPositionOfDivider instead")]
	public void SetPositionofDivider (float position, int dividerIndex);
 	public static MonoMac.Foundation.NSString NSSplitViewDidResizeSubviewsNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString NSSplitViewWillResizeSubviewsNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveNSSplitViewDidResizeSubviews (EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveNSSplitViewWillResizeSubviews (EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSSplitViewDividerIndexEventArgs</h3>
<pre>
public class NSSplitViewDividerIndexEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSSplitViewDividerIndexEventArgs (MonoMac.Foundation.NSNotification notification);
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSStatusItem</h3>
<p>Added:</p><pre>
 	[Obsolete("Use DrawStatusBarBackground instead")]
	public void DrawStatusBarBackgroundInRectwithHighlight (System.Drawing.RectangleF rect, bool highlight);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTableColumn</h3>
<p>Added:</p><pre>
 	public NSTableColumn (MonoMac.Foundation.NSString identifier);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTableRowView</h3>
<p>Added:</p><pre>
 	[Obsolete("Use DrawBackground instead")]
	public void DrawBackgrounn (System.Drawing.RectangleF dirtyRect);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTableView</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString ColumnDidMoveNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString ColumnDidResizeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString SelectionDidChangeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString SelectionIsChangingNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveColumnDidMove (EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveColumnDidResize (EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSText</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString DidBeginEditingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidChangeNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidEndEditingNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidBeginEditing (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEndEditing (EventHandler&lt;NSTextDidEndEditingEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextAlternatives</h3>
<p>Removed:</p><pre>
 		public static MonoMac.Foundation.NSObject ObserveSelectedAlternativeString (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 		public static MonoMac.Foundation.NSObject ObserveSelectedAlternativeString (EventHandler&lt;NSTextAlternativesSelectedAlternativeStringEventArgs&gt; handler);
</pre>
<h3>New Type: MonoMac.AppKit.NSTextAlternativesSelectedAlternativeStringEventArgs</h3>
<pre>
public class NSTextAlternativesSelectedAlternativeStringEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSTextAlternativesSelectedAlternativeStringEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public string AlternativeString {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextAttachmentCell</h3>
<p>Added:</p><pre>
 	[Obsolete("Use TrackMouse instead")]
	public bool TrackMouseinRectofViewuntilMouseUp (NSEvent theEvent, System.Drawing.RectangleF cellFrame, NSView controlView, bool untilMouseUp);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextBlock</h3>
<p>Added:</p><pre>
 	[Obsolete("Use WidthValueTypeForLayer instead")]
	public NSTextBlockValueType WidthValueTypeForLayeredge (NSTextBlockLayer layer, NSRectEdge edge);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextContainer</h3>
<p>Removed:</p><pre>
 	public virtual NSTextLayoutOrientation LayoutOrientation {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextDidEndEditingEventArgs</h3>
<pre>
public class NSTextDidEndEditingEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSTextDidEndEditingEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public int Movement {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextInputContext</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString KeyboardSelectionDidChangeNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveKeyboardSelectionDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextStorage</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString DidProcessEditingNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillProcessEditingNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidProcessEditing (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillProcessEditing (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextView</h3>
<p>Added:</p><pre>
 	[Obsolete("Use DragOperationForDraggingInfo instead")]
	public NSDragOperation DragOperationForDraggingInfotype (NSDraggingInfo dragInfo, string type);
 	[Obsolete("Use DrawInsertionPoint instead")]
	public void DrawInsertionPointInRectcolorturnedOn (System.Drawing.RectangleF rect, NSColor color, bool turnedOn);
 	[Obsolete("Use InsertCompletion instead")]
	public void InsertCompletionforPartialWord (string word, MonoMac.Foundation.NSRange charRange, int movement, bool isFinal);
 	[Obsolete("Use GetPreferredPasteboardType instead")]
	public string PreferredPasteboardTypeFromArrayrestrictedToTypesFromArray (string [] availableTypes, string [] allowedTypes);
 	[Obsolete("Use ReadSelectionFromPasteboard instead")]
	public bool ReadSelectionFromPasteboardtype (NSPasteboard pboard, string type);
 	[Obsolete("Use RulerViewWillAddMarker instead")]
	public float RulerViewWillAddMarkeratLocation (NSRulerView ruler, NSRulerMarker marker, float location);
 	[Obsolete("Use RulerViewWillMoveMarker instead")]
	public float RulerViewWillMoveMarkertoLocation (NSRulerView ruler, NSRulerMarker marker, float location);
 	[Obsolete("Use SetAlignmentRange instead")]
	public void SetAlignmentrange (NSTextAlignment alignment, MonoMac.Foundation.NSRange range);
 	[Obsolete("Use SetBaseWritingDirection instead")]
	public void SetBaseWritingDirectionrange (NSWritingDirection writingDirection, MonoMac.Foundation.NSRange range);
 	[Obsolete("Use SetSelectedRange instead")]
	public void SetSelectedRangeaffinitystillSelecting (MonoMac.Foundation.NSRange charRange, NSSelectionAffinity affinity, bool stillSelectingFlag);
 	[Obsolete("Use SetSelectedRanges instead")]
	public void SetSelectedRangesaffinitystillSelecting (MonoMac.Foundation.NSArray ranges, NSSelectionAffinity affinity, bool stillSelectingFlag);
 	[Obsolete("Use SetSpellingState instead")]
	public void SetSpellingStaterange (int value, MonoMac.Foundation.NSRange charRange);
 	[Obsolete("Use ShouldChangeTextInRangereplacementString instead")]
	public bool ShouldChangeTextInRangereplacementString (MonoMac.Foundation.NSRange affectedCharRange, string replacementString);
 	[Obsolete("Use ShouldChangeText instead")]
	public bool ShouldChangeTextInRangesreplacementStrings (MonoMac.Foundation.NSArray affectedRanges, string [] replacementStrings);
 	[Obsolete("Use ValidRequestorForSendType instead")]
	public MonoMac.Foundation.NSObject ValidRequestorForSendTypereturnType (string sendType, string returnType);
 	[Obsolete("Use WriteSelectionToPasteboard instead")]
	public bool WriteSelectionToPasteboardtype (NSPasteboard pboard, string type);
 	[Obsolete("Use __WriteSelectionToPasteboard instead")]
	public bool WriteSelectionToPasteboardtypes (NSPasteboard pboard, string [] types);
 	public static MonoMac.Foundation.NSString DidChangeSelectionNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidChangeTypingAttributesNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillChangeNotifyingTextViewNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidChangeSelection (EventHandler&lt;NSTextViewDidChangeSelectionEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeTypingAttributes (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillChangeNotifyingTextView (EventHandler&lt;NSTextViewWillChangeNotifyingTextViewEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextViewDidChangeSelectionEventArgs</h3>
<pre>
public class NSTextViewDidChangeSelectionEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSTextViewDidChangeSelectionEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public MonoMac.Foundation.NSValue OldSelectedCharacterRange {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextViewWillChangeNotifyingTextViewEventArgs</h3>
<pre>
public class NSTextViewWillChangeNotifyingTextViewEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSTextViewWillChangeNotifyingTextViewEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSTextView NewView {
		get;
	}
	public NSTextView OldView {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTokenFieldDelegate</h3>
<p>Removed:</p><pre>
 public abstract class NSTokenFieldDelegate : MonoMac.Foundation.NSObject {
 	public abstract string [] GetCompletionStrings (NSTokenField tokenField, string substring, int tokenIndex, int selectedIndex);
 	public abstract string GetDisplayString (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public abstract string GetEditingString (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public abstract NSMenu GetMenu (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public abstract MonoMac.Foundation.NSObject GetRepresentedObject (NSTokenField tokenField, string editingString);
 	public abstract NSTokenStyle GetStyle (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public abstract bool HasMenu (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public abstract MonoMac.Foundation.NSObject[] Read (NSTokenField tokenField, NSPasteboard pboard);
 	public abstract NSTokenField[] ShouldAddObjects (NSTokenField tokenField, NSTokenField[] tokens, uint index);
 	public abstract bool WriteRepresented (NSTokenField tokenField, MonoMac.Foundation.NSArray objects, NSPasteboard pboard);
</pre>
<p>Added:</p><pre>
 public class NSTokenFieldDelegate : MonoMac.Foundation.NSObject {
 	public virtual string [] GetCompletionStrings (NSTokenField tokenField, string substring, int tokenIndex, int selectedIndex);
 	public virtual string GetDisplayString (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public virtual string GetEditingString (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public virtual NSMenu GetMenu (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public virtual MonoMac.Foundation.NSObject GetRepresentedObject (NSTokenField tokenField, string editingString);
 	public virtual NSTokenStyle GetStyle (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public virtual bool HasMenu (NSTokenField tokenField, MonoMac.Foundation.NSObject representedObject);
 	public virtual MonoMac.Foundation.NSObject[] Read (NSTokenField tokenField, NSPasteboard pboard);
 	public virtual NSTokenField[] ShouldAddObjects (NSTokenField tokenField, NSTokenField[] tokens, uint index);
 	public virtual bool WriteRepresented (NSTokenField tokenField, MonoMac.Foundation.NSArray objects, NSPasteboard pboard);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSToolbar</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString NSToolbarDidRemoveItemNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString NSToolbarWillAddItemNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveNSToolbarDidRemoveItem (EventHandler&lt;NSToolbarItemEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveNSToolbarWillAddItem (EventHandler&lt;NSToolbarItemEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSToolbarItemEventArgs</h3>
<pre>
public class NSToolbarItemEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSToolbarItemEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSToolbarItem Item {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSView</h3>
<p>Removed:</p><pre>
 	public static MonoMac.Foundation.NSString NSViewBoundsDidChangeNotification {
 	public static MonoMac.Foundation.NSString NSViewDidUpdateTrackingAreasNotification {
 	public static MonoMac.Foundation.NSString NSViewFocusDidChangeNotification {
 	public static MonoMac.Foundation.NSString NSViewFrameDidChangeNotification {
 	public static MonoMac.Foundation.NSString NSViewGlobalFrameDidChangeNotification {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use CacheDisplay instead")]
	public void CacheDisplayInRecttoBitmapImageRep (System.Drawing.RectangleF rect, NSBitmapImageRep bitmapImageRep);
 	[Obsolete("Use DisplayRectIgnoringOpacity instead")]
	public void DisplayRectIgnoringOpacityinContext (System.Drawing.RectangleF aRect, NSGraphicsContext context);
 	[Obsolete("Use IsMouseInRect instead")]
	public bool MouseinRect (System.Drawing.PointF aPoint, System.Drawing.RectangleF aRect);
 	[Obsolete("Use ScrollRect instead")]
	public void ScrollRectby (System.Drawing.RectangleF aRect, System.Drawing.SizeF delta);
 	[Obsolete("Use SetContentHuggingPriorityForOrientation instead")]
	public void SetContentHuggingPriorityforOrientation (float priority, NSLayoutConstraintOrientation orientation);
 	[Obsolete("Use TranslateRectsNeedingDisplay instead")]
	public void TranslateRectsNeedingDisplayInRectby (System.Drawing.RectangleF clipRect, System.Drawing.SizeF delta);
 	public static MonoMac.Foundation.NSString BoundsChangedNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString FocusChangedNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString FrameChangedNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString GlobalFrameChangedNotification {
 		get;
 	}
 	[Obsolete("Use BoundsChangedNotification instead")]
	public static MonoMac.Foundation.NSString NSViewBoundsDidChangeNotification {
 		get;
 	}
 	[Obsolete("Use UpdatedTrackingAreasNotification instead")]
	public static MonoMac.Foundation.NSString NSViewDidUpdateTrackingAreasNotification {
 	[Obsolete("Use FocusChangedNotification instead")]
	public static MonoMac.Foundation.NSString NSViewFocusDidChangeNotification {
 	[Obsolete("Use FrameChangedNotification instead")]
	public static MonoMac.Foundation.NSString NSViewFrameDidChangeNotification {
 	[Obsolete("Use GlobalFrameChangedNotification instead")]
	public static MonoMac.Foundation.NSString NSViewGlobalFrameDidChangeNotification {
 	public static MonoMac.Foundation.NSString UpdatedTrackingAreasNotification {
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveBoundsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveFocusChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveFrameChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveGlobalFrameChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveUpdatedTrackingAreas (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSViewColumnMoveEventArgs</h3>
<pre>
public class NSViewColumnMoveEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSViewColumnMoveEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public int NewColumn {
		get;
	}
	public int OldColumn {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.AppKit.NSViewColumnResizeEventArgs</h3>
<pre>
public class NSViewColumnResizeEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSViewColumnResizeEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSTableColumn Column {
		get;
	}
	public int OldWidth {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSWindow</h3>
<p>Added:</p><pre>
 	[Obsolete("Use SetFrameFrom instead")]
	public void SetFrameFroom (string str);
</pre>
<h2>Namespace: MonoMac.AudioToolbox</h2>
<h3>Type Changed: MonoMac.AudioToolbox.AudioChannelDescription</h3>
<p>Removed:</p><pre>
 	public float [] Coords;
</pre>
<p>Added:</p><pre>
 	public float [] Coords {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoMac.AudioToolbox.AudioFileStream</h3>
<p>Added:</p><pre>
 	public AudioFileStreamStatus LastError {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AudioToolbox.AudioQueue</h3>
<p>Removed:</p><pre>
 	public T GetProperty&lt;T&gt; (AudioQueueProperty property);
</pre>
<p>Added:</p><pre>
 	public T GetProperty&lt;T&gt; (AudioQueueProperty property) where T : ValueType, struct, new ();
</pre>
<h2>Namespace: MonoMac.CoreAnimation</h2>
<h3>Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation</h3>
<p>Removed:</p><pre>
 	public static CAPropertyAnimation FromKeyPath (string path);
</pre>
<p>Added:</p><pre>
 	[Obsolete("This method in the future will return a CAKeyFrameAnimation, update your source, or use GetFromKeyPath to avoid this warning for now")]
	public static CAPropertyAnimation FromKeyPath (string path);
 	public static CAKeyFrameAnimation GetFromKeyPath (string path);
</pre>
<h2>Namespace: MonoMac.CoreFoundation</h2>
<h3>New Type: MonoMac.CoreFoundation.CFPreferences</h3>
<pre>
public static class CFPreferences {
	
	public static void AddSuitePreferencesToApp (MonoMac.Foundation.NSString applicationId, string suiteId);
	public static void AddSuitePreferencesToApp (string suiteId);
	public static void AddSuitePreferencesToApp (string applicationId, string suiteId);
	public static bool AppSynchronize ();
	public static bool AppSynchronize (MonoMac.Foundation.NSString applicationId);
	public static bool AppSynchronize (string applicationId);
	public static bool AppValueIsForced (string key);
	public static bool AppValueIsForced (string key, MonoMac.Foundation.NSString applicationId);
	public static bool AppValueIsForced (string key, string applicationId);
	public static bool GetAppBooleanValue (string key);
	public static bool GetAppBooleanValue (string key, MonoMac.Foundation.NSString applicationId);
	public static bool GetAppBooleanValue (string key, string applicationId);
	public static int GetAppIntegerValue (string key);
	public static int GetAppIntegerValue (string key, MonoMac.Foundation.NSString applicationId);
	public static int GetAppIntegerValue (string key, string applicationId);
	public static object GetAppValue (string key);
	public static object GetAppValue (string key, MonoMac.Foundation.NSString applicationId);
	public static object GetAppValue (string key, string applicationId);
	public static void RemoveAppValue (string key);
	public static void RemoveAppValue (string key, MonoMac.Foundation.NSString applicationId);
	public static void RemoveAppValue (string key, string applicationId);
	public static void RemoveSuitePreferencesFromApp (MonoMac.Foundation.NSString applicationId, string suiteId);
	public static void RemoveSuitePreferencesFromApp (string suiteId);
	public static void RemoveSuitePreferencesFromApp (string applicationId, string suiteId);
	public static void SetAppValue (string key, object value);
	public static void SetAppValue (string key, object value, MonoMac.Foundation.NSString applicationId);
	public static void SetAppValue (string key, object value, string applicationId);
	
	public static readonly MonoMac.Foundation.NSString CurrentApplication;
}
</pre>
<h2>Namespace: MonoMac.CoreGraphics</h2>
<h3>Type Changed: MonoMac.CoreGraphics.CGPDFDocument</h3>
<p>Added:</p><pre>
 	public CGPDFDictionary GetInfo ();
</pre>
<h2>Namespace: MonoMac.CoreServices</h2>
<h3>Type Changed: MonoMac.CoreServices.CFHTTPMessage</h3>
<p>Added:</p><pre>
 	public static CFHTTPMessage CreateEmpty (bool request);
 	public bool AppendBytes (byte [] bytes);
 	public bool AppendBytes (byte [] bytes, int count);
</pre>
<h2>Namespace: MonoMac.Foundation</h2>
<h3>Type Changed: MonoMac.Foundation.ExportAttribute</h3>
<p>Added:</p><pre>
 	public bool IsVariadic {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.Foundation.FieldAttribute</h3>
<pre>
public class FieldAttribute : Attribute {
	
	public FieldAttribute (string symbolName);
	public FieldAttribute (string symbolName, string libraryName);
	
	public string LibraryName {
		get;
		set;
	}
	public string SymbolName {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSAttributedString</h3>
<p>Added:</p><pre>
 	public NSAttributedString (string str, MonoMac.CoreText.CTStringAttributes attributes);
 	public MonoMac.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange effectiveRange);
 	public MonoMac.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
 	public NSAttributedString Substring (int start, int len);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSComparisonPredicateOptions</h3>
<p>Removed:</p><pre>
 	DiacriticInsensitive
</pre>
<p>Added:</p><pre>
 	DiacriticInsensitive,
 	Normalized
</pre>
<h3>New Type: MonoMac.Foundation.NSErrorException</h3>
<pre>
public class NSErrorException : Exception {
	
	public NSErrorException (NSError error);
	
	public int Code {
		get;
	}
	public string Domain {
		get;
	}
	public NSError Error {
		get;
	}
	public NSDictionary UserInfo {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSInputStream</h3>
<p>Removed:</p><pre>
 	public virtual void ScheduleInCFRunLoop (MonoMac.CoreFoundation.CFRunLoop runloop, NSString mode);
 	public virtual void UnscheduleInCFRunLoop (MonoMac.CoreFoundation.CFRunLoop runloop, NSString mode);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSLocale</h3>
<p>Added:</p><pre>
 	public string GetCountryCodeDisplayName (string value);
 	public string GetCurrencyCodeDisplayName (string value);
 	public string GetIdentifierDisplayName (string value);
 	public string GetLanguageCodeDisplayName (string value);
 	public string AlternateQuotationBeginDelimiterKey {
 		get;
 	}
 	public string AlternateQuotationEndDelimiterKey {
 		get;
 	}
 	public NSCalendar Calendar {
 		get;
 	}
 	public string CollationIdentifier {
 		get;
 	}
 	public string CollatorIdentifier {
 		get;
 	}
 	public string CountryCode {
 		get;
 	}
 	public string CurrencyCode {
 		get;
 	}
 	public string CurrencySymbol {
 		get;
 	}
 	public string DecimalSeparator {
 		get;
 	}
 	public NSCharacterSet ExemplarCharacterSet {
 		get;
 	}
 	public string GroupingSeparator {
 		get;
 	}
 	public string Identifier {
 		get;
 	}
 	public string LanguageCode {
 		get;
 	}
 	public string MeasurementSystem {
 		get;
 	}
 	public string QuotationBeginDelimiterKey {
 		get;
 	}
 	public string QuotationEndDelimiterKey {
 		get;
 	}
 	public string ScriptCode {
 		get;
 	}
 	public bool UsesMetricSystem {
 		get;
 	}
 	public string VariantCode {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.Foundation.NSMutableOrderedSet</h3>
<pre>
public class NSMutableOrderedSet : NSOrderedSet {
	
	public NSMutableOrderedSet (params NSObject[] objs);
	public NSMutableOrderedSet (params object [] objs);
	public NSMutableOrderedSet (params string [] strings);
	public NSMutableOrderedSet ();
	public NSMutableOrderedSet (NSCoder coder);
	public NSMutableOrderedSet (NSObjectFlag t);
	public NSMutableOrderedSet (IntPtr handle);
	public NSMutableOrderedSet (NSObject start);
	public NSMutableOrderedSet (NSSet source);
	public NSMutableOrderedSet (NSOrderedSet source);
	public NSMutableOrderedSet (int capacity);
	
	public virtual void Add (NSObject obj);
	public virtual void AddObjects (NSObject[] source);
	public virtual void ExchangeObject (int first, int second);
	public virtual void Insert (NSObject obj, int atIndex);
	public virtual void InsertObjects (NSObject[] objects, NSIndexSet atIndexes);
	public virtual void Intersect (NSOrderedSet intersectWith);
	public virtual void MoveObjects (NSIndexSet indexSet, int destination);
	public virtual void Remove (int index);
	public virtual void RemoveAllObjects ();
	public virtual void RemoveObject (NSObject obj);
	public virtual void RemoveObjects (NSIndexSet indexSet);
	public virtual void RemoveObjects (NSObject[] objects);
	public virtual void RemoveObjects (NSRange range);
	public virtual void Replace (int objectAtIndex, NSObject newObject);
	public virtual void ReplaceObjects (NSIndexSet indexSet, NSObject[] replacementObjects);
	public virtual void SetObject (NSObject obj, int index);
	public virtual void Sort (NSComparator comparator);
	public virtual void Sort (NSSortOptions sortOptions, NSComparator comparator);
	public virtual void SortRange (NSRange range, NSSortOptions sortOptions, NSComparator comparator);
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSObject this [int idx] {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSMutableSet</h3>
<p>Added:</p><pre>
 	public NSMutableSet (NSObject[] objs);
 	public NSMutableSet (params string [] strings);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSMutableUrlRequest</h3>
<p>Added:</p><pre>
 	public virtual NSUrlRequestNetworkServiceType NetworkServiceType {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSNumber</h3>
<p>Added:</p><pre>
 	public static NSNumber FromObject (object value);
</pre>
<h3>New Type: MonoMac.Foundation.NSOrderedSet</h3>
<pre>
public class NSOrderedSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<nsobject> {
	
	public NSOrderedSet (params NSObject[] objs);
	public NSOrderedSet (params object [] objs);
	public NSOrderedSet (params string [] strings);
	public NSOrderedSet ();
	public NSOrderedSet (NSCoder coder);
	public NSOrderedSet (NSObjectFlag t);
	public NSOrderedSet (IntPtr handle);
	public NSOrderedSet (NSObject start);
	public NSOrderedSet (NSSet source);
	public NSOrderedSet (NSOrderedSet source);
	
	public static NSOrderedSet MakeNSOrderedSet<t> (T[] values) where T : NSObject;
	public virtual NSSet AsSet ();
	public virtual bool Contains (NSObject obj);
	public bool Contains (object obj);
	public virtual NSObject FirstObject ();
	public System.Collections.Generic.IEnumerator<nsobject> GetEnumerator ();
	public virtual NSOrderedSet GetReverseOrderedSet ();
	public virtual int IndexOf (NSObject obj);
	public virtual bool Intersects (NSOrderedSet other);
	public virtual bool Intersects (NSSet other);
	public virtual bool IsEqualToOrderedSet (NSOrderedSet other);
	public virtual bool IsSubset (NSOrderedSet other);
	public virtual bool IsSubset (NSSet other);
	public virtual NSObject LastObject ();
	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
	public T[] ToArray<t> () where T : NSObject;
	
	public static NSOrderedSet operator + (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSSet second);
	public static bool operator == (NSOrderedSet first, NSOrderedSet second);
	public static bool operator != (NSOrderedSet first, NSOrderedSet second);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int Count {
		get;
	}
	public NSObject this [int idx] {
		get;
	}
}
</t></nsobject></t></nsobject></pre>
<h3>Type Changed: MonoMac.Foundation.NSProcessInfo</h3>
<p>Added:</p><pre>
 	public virtual void DisableAutomaticTermination (string reason);
 	public virtual void DisableSuddenTermination ();
 	public virtual void EnableAutomaticTermination (string reason);
 	public virtual void EnableSuddenTermination ();
 	public virtual bool AutomaticTerminationSupportEnabled {
 		get;
 		set;
 	}
 	public virtual double SystemUptime {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.Foundation.NSSortOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSSortOptions {
	Concurrent,
	Stable
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSUbiquitousKeyValueStore</h3>
<p>Added:</p><pre>
 	public void SetArray (string key, NSObject[] value);
 	public void SetBool (string key, bool value);
 	public void SetData (string key, NSData value);
 	public void SetDictionary (string key, NSDictionary value);
 	public void SetDouble (string key, double value);
 	public void SetLong (string key, long value);
 	public void SetString (string key, string value);
 	public NSObject this [NSString key] {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.Foundation.NSUrlAsyncResult</h3>
<pre>
public class NSUrlAsyncResult {
	
	public NSUrlAsyncResult (NSUrlResponse response, NSData data);
	
	public NSData Data {
		get;
		set;
	}
	public NSUrlResponse Response {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSUrlConnection</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;NSUrlAsyncResult&gt; SendRequestAsync (NSUrlRequest request, NSOperationQueue queue);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSUrlCredential</h3>
<p>Removed:</p><pre>
 	public NSUrlCredential (IntPtr SecTrustRef_trust, bool ignored);
</pre>
<p>Added:</p><pre>
 	public NSUrlCredential (IntPtr trust, bool ignored);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSUrlRequest</h3>
<p>Added:</p><pre>
 	public virtual bool AllowsCellularAccess {
 		get;
 	}
 	public virtual NSUrlRequestNetworkServiceType NetworkServiceType {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.Foundation.NSUrlRequestNetworkServiceType</h3>
<pre>
[Serializable]
public enum NSUrlRequestNetworkServiceType {
	Default,
	VoIP,
	Video,
	Background,
	Voice
}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSUuid</h3>
<p>Added:</p><pre>
 	public NSUuid (byte [] bytes);
 	public byte [] GetBytes ();
</pre>
<h3>Type Changed: MonoMac.Foundation.NSValue</h3>
<p>Added:</p><pre>
 	public static NSValue FromRange (NSRange range);
</pre>
<h3>New Type: MonoMac.Foundation.ObjCException</h3>
<pre>
public class ObjCException : Exception {
	
	public ObjCException ();
	public ObjCException (NSException exc);
	
	public override string Message {
		get;
	}
	public string Name {
		get;
	}
	public NSException NSException {
		get;
	}
	public string Reason {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.Foundation.ProtocolAttribute</h3>
<pre>
public sealed class ProtocolAttribute : Attribute {
	
	public ProtocolAttribute ();
}
</pre>
<h2>Namespace: MonoMac.GameKit</h2>
<h3>Type Changed: MonoMac.GameKit.GKScore</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use Date property")]
	public virtual MonoMac.Foundation.NSDate date {
 		get;
 	}
</pre>
<h2>Namespace: MonoMac.ObjCRuntime</h2>
<h3>Type Changed: MonoMac.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_out_RectangleF_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, out System.Drawing.RectangleF arg3, IntPtr arg4, IntPtr arg5, System.Drawing.PointF arg6);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_out_RectangleF_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, out System.Drawing.RectangleF arg3, IntPtr arg4, IntPtr arg5, System.Drawing.PointF arg6);
 	public static float monomac_float_objc_msgSend (IntPtr receiver, IntPtr selector);
 	public static float monomac_float_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static IntPtr monomac_IntPtr_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static IntPtr monomac_IntPtr_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
</pre>
<h2>Namespace: MonoMac.SystemConfiguration</h2>
<h3>New Type: MonoMac.SystemConfiguration.CaptiveNetwork</h3>
<pre>
public static class CaptiveNetwork {
	
	public static string [] GetSupportedInterfaces ();
	public static bool MarkPortalOffline (string iface);
	public static bool MarkPortalOnline (string iface);
	public static bool SetSupportedSSIDs (string [] ssids);
	public static StatusCode TryGetSupportedInterfaces (out string [] supportedInterfaces);
}
</pre>
<h3>New Type: MonoMac.SystemConfiguration.NetworkReachability</h3>
<pre>
public class NetworkReachability : IDisposable, MonoMac.ObjCRuntime.INativeObject {
	
	public NetworkReachability (System.Net.IPAddress ip);
	public NetworkReachability (string address);
	public NetworkReachability (System.Net.IPAddress localAddress, System.Net.IPAddress remoteAddress);
	
	public void Dispose ();
	public virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public StatusCode GetFlags (out NetworkReachabilityFlags flags);
	public bool Schedule ();
	public bool Schedule (MonoMac.CoreFoundation.CFRunLoop runLoop, string mode);
	public bool SetCallback (Notification callback);
	public bool SetDispatchQueue (MonoMac.CoreFoundation.DispatchQueue queue);
	public StatusCode SetNotification (Notification callback);
	public bool TryGetFlags (out NetworkReachabilityFlags flags);
	public bool Unschedule ();
	public bool Unschedule (MonoMac.CoreFoundation.CFRunLoop runLoop, string mode);
	
	public IntPtr Handle {
		get;
	}
	
	[Serializable]
	public delegate void Notification (NetworkReachabilityFlags flags);
}
</pre>
<h3>New Type: MonoMac.SystemConfiguration.NetworkReachabilityFlags</h3>
<pre>
[Serializable]
[Flags]
public enum NetworkReachabilityFlags {
	TransientConnection,
	Reachable,
	ConnectionRequired,
	ConnectionOnTraffic,
	InterventionRequired,
	ConnectionOnDemand,
	IsLocalAddress,
	IsDirect,
	ConnectionAutomatic
}
</pre>
<h3>New Type: MonoMac.SystemConfiguration.StatusCode</h3>
<pre>
[Serializable]
public enum StatusCode {
	OK,
	Failed,
	InvalidArgument,
	AccessError,
	NoKey,
	KeyExists,
	Locked,
	NeedLock,
	NoStoreSession,
	NoStoreServer,
	NotifierActive,
	NoPrefsSession,
	PrefsBusy,
	NoConfigFile,
	NoLink,
	Stale,
	MaxLink,
	ReachabilityUnknown,
	ConnectionNoService,
	ConnectionIgnore
}
</pre>
<h3>New Type: MonoMac.SystemConfiguration.StatusCodeError</h3>
<pre>
public static class StatusCodeError {
	
	public static string GetErrorDescription (StatusCode statusCode);
}
</pre>
<h3>New Type: MonoMac.SystemConfiguration.SystemConfigurationException</h3>
<pre>
public class SystemConfigurationException : Exception {
	
	public SystemConfigurationException (StatusCode statusErrorCode);
	
	public StatusCode StatusErrorCode {
		get;
	}
}
</pre>
<h2>Namespace: MonoMac.WebKit</h2>
<h3>New Type: MonoMac.WebKit.DomBlob</h3>
<pre>
public class DomBlob : DomObject {
	
	public DomBlob (MonoMac.Foundation.NSCoder coder);
	public DomBlob (MonoMac.Foundation.NSObjectFlag t);
	public DomBlob (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual ulong Size {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.WebKit.DomFile</h3>
<pre>
public class DomFile : DomBlob {
	
	public DomFile (MonoMac.Foundation.NSCoder coder);
	public DomFile (MonoMac.Foundation.NSObjectFlag t);
	public DomFile (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Name {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.WebKit.DomFileList</h3>
<pre>
public class DomFileList : DomObject {
	
	public DomFileList (MonoMac.Foundation.NSCoder coder);
	public DomFileList (MonoMac.Foundation.NSObjectFlag t);
	public DomFileList (IntPtr handle);
	
	public virtual DomFile GetItem (int index);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint Length {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.WebKit.DomHtmlFormElement</h3>
<pre>
public class DomHtmlFormElement : DomHtmlElement {
	
	public DomHtmlFormElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlFormElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlFormElement (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
	public virtual void Submit ();
	
	public virtual string AcceptCharset {
		get;
		set;
	}
	public virtual string Action {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual DomHtmlCollection Elements {
		get;
	}
	public virtual string Encoding {
		get;
		set;
	}
	public virtual string EncodingType {
		get;
		set;
	}
	public virtual int Length {
		get;
	}
	public virtual string Method {
		get;
		set;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual string Target {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoMac.WebKit.DomHtmlInputElement</h3>
<p>Added:</p><pre>
 	public virtual DomFileList Files {
 		get;
 	}
 	public virtual DomHtmlFormElement Form {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.WebKit.DomHtmlTextAreaElement</h3>
<pre>
public class DomHtmlTextAreaElement : DomHtmlElement {
	
	public DomHtmlTextAreaElement (MonoMac.Foundation.NSCoder coder);
	public DomHtmlTextAreaElement (MonoMac.Foundation.NSObjectFlag t);
	public DomHtmlTextAreaElement (IntPtr handle);
	
	public virtual void Blur ();
	protected override void Dispose (bool disposing);
	public virtual void Focus ();
	public virtual void Select ();
	
	public virtual string AccessKey {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int Columns {
		get;
		set;
	}
	public virtual string DefaultValue {
		get;
		set;
	}
	public virtual bool Disabled {
		get;
		set;
	}
	public virtual DomHtmlFormElement Form {
		get;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual bool ReadOnly {
		get;
		set;
	}
	public virtual int Rows {
		get;
		set;
	}
	public virtual int TabIndex {
		get;
		set;
	}
	public virtual string Type {
		get;
	}
	public virtual string Value {
		get;
		set;
	}
}
</pre>
</body>
</html>
