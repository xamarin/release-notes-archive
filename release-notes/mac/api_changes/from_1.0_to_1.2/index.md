---
id: 169281E7-DF3C-45E3-8F7F-A5EBEE5F2047
title: "From 1.0 to 1.2"
---

<html><head><title>API differences between XamMac.1.0 and XamMac.1.2</title></head>
<body>

<p>This document describes the API additions from XamMac 1.0 to Xammac
1.2.  Most of the changes are new APIs that bring the AppKit support
in line with Lion and Mountain Lion features.

<p>There are a few changes that are source-code compatible and were
introduced in preparation for our 64 bit support.

<h2>Namespace: MonoMac</h2>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Added:</p><pre>
 	public const string CoreServicesLibrary = "/System/Library/Frameworks/CoreServices.framework/CoreServices";
</pre>
<h2>Namespace: MonoMac.AppKit</h2>
<h3>Type Changed: MonoMac.AppKit.NSAnimationContext</h3>
<p>Added:</p><pre>
 	public virtual bool AllowsImplicitAnimation {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSCharacterCollection</h3>
<pre>
[Serializable]
public enum NSCharacterCollection {
	IdentityMapping,
	AdobeCns1,
	AdobeGb1,
	AdobeJapan1,
	AdobeJapan2,
	AdobeKorea1
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSCollectionViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DraggingSessionEnded (NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, NSDragOperation dragOperation);
 	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSIndexSet indexes);
 	public virtual NSPasteboardWriting PasteboardWriterForItemAtIndex (NSCollectionView collectionView, uint index);
 	public virtual void UpdateDraggingItemsForDrag (NSCollectionView collectionView, NSDraggingInfo draggingInfo);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSColor</h3>
<p>Added:</p><pre>
 	public static NSColor FromCGColor (MonoMac.CoreGraphics.CGColor cgColor);
 	public static NSColor FromGamma22White (float white, float alpha);
 	public static NSColor FromSrgb (float red, float green, float blue, float alpha);
 	public static NSColor UnderPageBackgroundColor {
 		get;
 	}
 	public virtual MonoMac.CoreGraphics.CGColor CGColor {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSControl</h3>
<p>Added:</p><pre>
 	public virtual bool AllowsExpansionToolTips {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSControlEditingSupport</h3>
<pre>
public static class NSControlEditingSupport {
	
	public static bool ValidateProposedFirstResponder (NSResponder This, NSResponder responder, NSEvent forEvent);
}
</pre>
<h3>New Type: MonoMac.AppKit.NSCorrectionIndicatorType</h3>
<pre>
[Serializable]
public enum NSCorrectionIndicatorType {
	Default,
	Reversion,
	Guesses
}
</pre>
<h3>New Type: MonoMac.AppKit.NSCorrectionResponse</h3>
<pre>
[Serializable]
public enum NSCorrectionResponse {
	None,
	Accepted,
	Rejected,
	Ignored,
	Edited,
	Reverted
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSCustomImageRep</h3>
<p>Added:</p><pre>
 	public NSCustomImageRep (System.Drawing.SizeF size, bool flipped, NSCustomImageRepDrawingHandler drawingHandler);
 	public virtual NSCustomImageRepDrawingHandler DrawingHandler {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSCustomImageRepDrawingHandler</h3>
<pre>
[Serializable]
public delegate bool NSCustomImageRepDrawingHandler (System.Drawing.RectangleF dstRect);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSDocument</h3>
<p>Added:</p><pre>
 	public virtual void BrowseDocumentVersions (MonoMac.Foundation.NSObject sender);
 	public virtual void LockDocument (MonoMac.Foundation.NSObject sender);
 	public virtual void LockDocumentWithCompletionHandler (NSDocumentLockDocumentCompletionHandler completionHandler);
 	public virtual void LockWithCompletionHandler (NSDocumentLockCompletionHandler completionHandler);
 	public virtual void MoveDocument (MonoMac.Foundation.NSObject sender);
 	public virtual void MoveDocumentToUbiquityContainer (MonoMac.Foundation.NSObject sender);
 	public virtual void MoveDocumentWithCompletionHandler (NSDocumentMoveCompletionHandler completionHandler);
 	public virtual void MoveToUrl (MonoMac.Foundation.NSUrl url, NSDocumentMoveToUrlCompletionHandler completionHandler);
 	public virtual void RenameDocument (MonoMac.Foundation.NSObject sender);
 	public virtual void UnlockDocument (MonoMac.Foundation.NSObject sender);
 	public virtual void UnlockDocumentWithCompletionHandler (NSDocumentUnlockDocumentCompletionHandler completionHandler);
 	public virtual void UnlockWithCompletionHandler (NSDocumentUnlockCompletionHandler completionHandler);
 	public static bool AutoSavesDrafts {
 		get;
 	}
 	public static bool UsesUbiquitousStorage {
 		get;
 	}
 	public virtual MonoMac.Foundation.NSUrl BackupFileUrl {
 		get;
 	}
 	public virtual string DefaultDraftName {
 		get;
 	}
 	public virtual bool IsDraft {
 		get;
 		set;
 	}
 	public virtual bool IsLocked {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSDocumentController</h3>
<p>Added:</p><pre>
 	public virtual void BeginOpenPanel (NSOpenPanel openPanel, MonoMac.Foundation.NSArray inTypes, NSDocumentControllerOpenPanelResultHandler completionHandler);
 	public virtual void BeginOpenPanelWithCompletionHandler (NSDocumentControllerOpenPanelWithCompletionHandler completionHandler);
 	public virtual NSDocument DuplicateDocumentWithContentsOfUrl (MonoMac.Foundation.NSUrl url, bool duplicateByCopying, string displayName, out MonoMac.Foundation.NSError error);
 	public virtual void OpenDocumentWithContentsOfUrl (MonoMac.Foundation.NSUrl url, bool displayDocument, OpenDocumentCompletionHandler completionHandler);
 	public virtual void ReopenDocumentForUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSUrl contentsUrl, bool displayDocument, OpenDocumentCompletionHandler completionHandler);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentControllerOpenPanelResultHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentControllerOpenPanelResultHandler (int result);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentControllerOpenPanelWithCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentControllerOpenPanelWithCompletionHandler (MonoMac.Foundation.NSArray urlsToOpen);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentLockCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentLockCompletionHandler (MonoMac.Foundation.NSError error);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentLockDocumentCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentLockDocumentCompletionHandler (bool didLock);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentMoveCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentMoveCompletionHandler (bool didMove);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentMoveToUrlCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentMoveToUrlCompletionHandler (MonoMac.Foundation.NSError error);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentUnlockCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentUnlockCompletionHandler (MonoMac.Foundation.NSError error);
</pre>
<h3>New Type: MonoMac.AppKit.NSDocumentUnlockDocumentCompletionHandler</h3>
<pre>
[Serializable]
public delegate void NSDocumentUnlockDocumentCompletionHandler (bool didUnlock);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSForm</h3>
<p>Added:</p><pre>
 	public virtual float PreferredTextFieldWidth {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSFormCell</h3>
<p>Added:</p><pre>
 	public virtual float PreferredTextFieldWidth {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSGlyphInfo</h3>
<pre>
public class NSGlyphInfo : MonoMac.Foundation.NSObject {
	
	public NSGlyphInfo ();
	public NSGlyphInfo (MonoMac.Foundation.NSCoder coder);
	public NSGlyphInfo (MonoMac.Foundation.NSObjectFlag t);
	public NSGlyphInfo (IntPtr handle);
	
	public static NSGlyphInfo Get (string glyphName, NSFont forFont, string baseString);
	public static NSGlyphInfo Get (uint characterIdentifier, NSCharacterCollection characterCollection, string baseString);
	public static NSGlyphInfo Get (uint glyph, NSFont forFont, string baseString);
	
	public virtual NSCharacterCollection CharacterCollection {
		get;
	}
	public virtual uint CharacterIdentifier {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string GlyphName {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSImage</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSObject ImageWithSize (System.Drawing.SizeF size, bool flipped, NSCustomImageRepDrawingHandler drawingHandler);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSMatrix</h3>
<p>Added:</p><pre>
 	public virtual bool AutoRecalculatesCellSize {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSNib</h3>
<p>Added:</p><pre>
 	public NSNib (MonoMac.Foundation.NSData nibData, MonoMac.Foundation.NSBundle bundle);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSOutlineView</h3>
<p>Added:</p><pre>
 	public virtual void InsertItems (MonoMac.Foundation.NSIndexSet indexes, MonoMac.Foundation.NSObject parent, NSTableViewAnimationOptions animationOptions);
 	public virtual void InsertRows (MonoMac.Foundation.NSIndexSet indexes, NSTableViewAnimationOptions animationOptions);
 	public virtual void MoveItem (int fromIndex, MonoMac.Foundation.NSObject oldParent, int toIndex, MonoMac.Foundation.NSObject newParent);
 	public virtual void MoveRow (int oldIndex, int newIndex);
 	public virtual void RemoveItems (MonoMac.Foundation.NSIndexSet indexes, MonoMac.Foundation.NSObject parent, NSTableViewAnimationOptions animationOptions);
 	public virtual void RemoveRows (MonoMac.Foundation.NSIndexSet indexes, NSTableViewAnimationOptions animationOptions);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSOutlineViewDataSource</h3>
<p>Added:</p><pre>
 	public virtual void DraggingSessionEnded (NSOutlineView outlineView, NSDraggingSession session, System.Drawing.PointF screenPoint, NSDragOperation operation);
 	public virtual void DraggingSessionWillBegin (NSOutlineView outlineView, NSDraggingSession session, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSArray draggedItems);
 	public virtual NSPasteboardWriting PasteboardWriterForItem (NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
 	public virtual void UpdateDraggingItemsForDrag (NSOutlineView outlineView, NSDraggingInfo draggingInfo);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSOutlineViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DidAddRowView (NSOutlineView outlineView, NSTableRowView rowView, int row);
 	public virtual void DidRemoveRowView (NSOutlineView outlineView, NSTableRowView rowView, int row);
 	public virtual NSTableRowView RowViewForItem (NSOutlineView outlineView, MonoMac.Foundation.NSObject item);
 	public virtual NSView ViewForTableColumn (NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPasteboard</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString PasteboardTypeTextFinderOptions {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPredicateEditorRowTemplate</h3>
<p>Added:</p><pre>
 	public NSPredicateEditorRowTemplate (params MonoMac.Foundation.NSCompoundPredicateType[] compoundTypes);
 	public NSPredicateEditorRowTemplate (System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSExpression&gt; leftExpressions, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSExpression&gt; rightExpressions, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (System.Collections.Generic.IEnumerable&lt;string&gt; leftExpressionsFromKeyPaths, System.Collections.Generic.IEnumerable&lt;string&gt; rightExpressionsFromConstants, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (string leftExpressionFromKeyPath, string rightExpressionFromConstant, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (string leftExpressionFromKeyPath, System.Collections.Generic.IEnumerable&lt;string&gt; rightExpressionsFromConstants, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSExpression&gt; leftExpressions, MonoMac.CoreData.NSAttributeType attributeType, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (System.Collections.Generic.IEnumerable&lt;string&gt; leftExpressionsFromKeyPaths, MonoMac.CoreData.NSAttributeType attributeType, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
 	public NSPredicateEditorRowTemplate (string leftExpressionFromKeyPath, MonoMac.CoreData.NSAttributeType attributeType, System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSPredicateOperatorType&gt; operators, MonoMac.Foundation.NSComparisonPredicateModifier modifier, MonoMac.Foundation.NSComparisonPredicateOptions options);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSPrintOperation</h3>
<p>Added:</p><pre>
 	public virtual NSPrintRenderingQuality PreferredRenderingQuality {
 		get;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSPrintRenderingQuality</h3>
<pre>
[Serializable]
public enum NSPrintRenderingQuality {
	Best,
	Responsive
}
</pre>
<h3>New Type: MonoMac.AppKit.NSRemoteNotifications_NSApplication</h3>
<pre>
public static class NSRemoteNotifications_NSApplication {
	
	public static MonoMac.Foundation.NSString NSApplicationLaunchUserNotificationKey {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSResponder</h3>
<p>Added:</p><pre>
 	public virtual void QuickLook (NSEvent withEvent);
 	public virtual void SmartMagnify (NSEvent withEvent);
 	public virtual MonoMac.Foundation.NSObject SupplementalTargetForAction (MonoMac.ObjCRuntime.Selector action, MonoMac.Foundation.NSObject sender);
 	public virtual bool WantsScrollEventsForSwipeTrackingOnAxis (NSEventGestureAxis axis);
</pre>
<h3>New Type: MonoMac.AppKit.NSRulerMarkerClientViewDelegation</h3>
<pre>
public static class NSRulerMarkerClientViewDelegation {
	
	public static float RulerViewLocation (NSView This, NSRulerView ruler, System.Drawing.PointF locationForPoint);
	public static System.Drawing.PointF RulerViewPoint (NSView This, NSRulerView ruler, float pointForLocation);
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSRunningApplication</h3>
<p>Added:</p><pre>
 	public static void TerminateAutomaticallyTerminableApplications ();
</pre>
<h3>Type Changed: MonoMac.AppKit.NSScrollView</h3>
<p>Added:</p><pre>
 	public virtual void MagnifyToFitRect (System.Drawing.RectangleF rect);
 	public virtual void SetMagnification (float magnification, System.Drawing.PointF centeredAtPoint);
 	public static MonoMac.Foundation.NSString DidEndLiveMagnifyNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WillStartLiveMagnifyNotification {
 		get;
 	}
 	public virtual bool AllowsMagnification {
 		get;
 		set;
 	}
 	public virtual float Magnification {
 		get;
 		set;
 	}
 	public virtual float MaxMagnification {
 		get;
 		set;
 	}
 	public virtual float MinMagnification {
 		get;
 		set;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidEndLiveMagnify (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillStartLiveMagnify (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSSegmentBackgroundStyle_NSSegmentedCell</h3>
<pre>
public static class NSSegmentBackgroundStyle_NSSegmentedCell {
	
	public static MonoMac.Foundation.NSString SharingServiceNameAddToAperture {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameAddToIPhoto {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameAddToSafariReadingList {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameComposeEmail {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameComposeMessage {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostImageOnFlickr {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostOnFacebook {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostOnSinaWeibo {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostOnTwitter {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostVideoOnTudou {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostVideoOnVimeo {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNamePostVideoOnYouku {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameSendViaAirDrop {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameUseAsDesktopPicture {
		get;
	}
	public static MonoMac.Foundation.NSString SharingServiceNameUseAsTwitterProfileImage {
		get;
	}
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSSpellChecker</h3>
<p>Added:</p><pre>
 	public virtual void DismissCorrectionIndicator (NSView forView);
 	public virtual string GetCorrection (MonoMac.Foundation.NSRange forWordRange, string inString, string language, int inSpellDocumentWithTag);
 	public virtual string GetLanguage (MonoMac.Foundation.NSRange forWordRange, string inString, MonoMac.Foundation.NSOrthography orthography);
 	public virtual void RecordResponse (NSCorrectionResponse response, string toCorrection, string forWord, string language, int inSpellDocumentWithTag);
 	public virtual void ShowCorrectionIndicatorOfType (NSCorrectionIndicatorType type, string primaryString, string [] alternativeStrings, System.Drawing.RectangleF forStringInRect, NSRulerView view, NSSpellCheckerShowCorrectionIndicatorOfTypeHandler completionHandler);
 	public static MonoMac.Foundation.NSString DidChangeAutomaticSpellingCorrectionNotification {
 		get;
 	}
 	public static MonoMac.Foundation.NSString DidChangeAutomaticTextReplacementNotification {
 		get;
 	}
 	public static bool IsAutomaticSpellingCorrectionEnabled {
 		get;
 	}
 	public static bool IsAutomaticTextReplacementEnabled {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingDocumentAuthorKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingDocumentTitleKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingDocumentURLKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingOrthographyKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingQuotesKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingReferenceDateKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingReferenceTimeZoneKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingRegularExpressionsKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString TextCheckingReplacementsKey {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticSpellingCorrection (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticTextReplacement (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSSpellCheckerShowCorrectionIndicatorOfTypeHandler</h3>
<pre>
[Serializable]
public delegate void NSSpellCheckerShowCorrectionIndicatorOfTypeHandler (string acceptedString);
</pre>
<h3>New Type: MonoMac.AppKit.NSSpellingState</h3>
<pre>
[Serializable]
[Flags]
public enum NSSpellingState {
	None,
	Spelling,
	Grammar
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSSplitView</h3>
<p>Added:</p><pre>
 	public virtual float HoldingPriorityForSubviewAtIndex (int subviewIndex);
 	public virtual void SetHoldingPriority (float priority, int subviewIndex);
</pre>
<h3>New Type: MonoMac.AppKit.NSStandardKeyBindingMethods</h3>
<pre>
public static class NSStandardKeyBindingMethods {
	
	public static void QuickLookPreviewItems (NSResponder This, MonoMac.Foundation.NSObject sender);
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSStatusBar</h3>
<p>Added:</p><pre>
 	public NSStatusItem CreateStatusItem (NSStatusItemLength length);
</pre>
<h3>New Type: MonoMac.AppKit.NSStatusItemLength</h3>
<pre>
[Serializable]
public enum NSStatusItemLength {
	Variable,
	Square
}
</pre>
<h3>New Type: MonoMac.AppKit.NSStringAttributes</h3>
<pre>
public class NSStringAttributes : MonoMac.Foundation.DictionaryContainer {
	
	public NSStringAttributes ();
	public NSStringAttributes (MonoMac.Foundation.NSDictionary dictionary);
	
	public int SetStrikethroughStyle (NSUnderlineStyle style, NSUnderlinePattern pattern, bool byWord);
	public int SetUnderlineStyle (NSUnderlineStyle style, NSUnderlinePattern pattern, bool byWord);
	
	public NSTextAttachment Attachment {
		get;
		set;
	}
	public NSColor BackgroundColor {
		get;
		set;
	}
	public Nullable<float> BaselineOffset {
		get;
		set;
	}
	public Nullable<int> CharacterShape {
		get;
		set;
	}
	public NSCursor Cursor {
		get;
		set;
	}
	public Nullable<float> Expansion {
		get;
		set;
	}
	public NSFont Font {
		get;
		set;
	}
	public NSColor ForegroundColor {
		get;
		set;
	}
	public NSGlyphInfo GlyphInfo {
		get;
		set;
	}
	public Nullable<float> KerningAdjustment {
		get;
		set;
	}
	public System.Nullable<monomac.foundation.nsligaturetype> Ligature {
		get;
		set;
	}
	public MonoMac.Foundation.NSString LinkString {
		get;
		set;
	}
	public MonoMac.Foundation.NSUrl LinkUrl {
		get;
		set;
	}
	public Nullable<bool> MarkedClauseSegment {
		get;
		set;
	}
	public Nullable<float> Obliqueness {
		get;
		set;
	}
	public NSParagraphStyle ParagraphStyle {
		get;
		set;
	}
	public NSShadow Shadow {
		get;
		set;
	}
	public Nullable<nsspellingstate> SpellingState {
		get;
		set;
	}
	public NSColor StrikethroughColor {
		get;
		set;
	}
	public Nullable<int> StrikethroughStyle {
		get;
		set;
	}
	public NSColor StrokeColor {
		get;
		set;
	}
	public Nullable<float> StrokeWidth {
		get;
		set;
	}
	public Nullable<bool> Superscript {
		get;
		set;
	}
	public NSTextAlternatives TextAlternatives {
		get;
		set;
	}
	public string ToolTip {
		get;
		set;
	}
	public NSColor UnderlineColor {
		get;
		set;
	}
	public Nullable<int> UnderlineStyle {
		get;
		set;
	}
	public Nullable<nstextlayoutorientation> VerticalGlyphForm {
		get;
		set;
	}
	public MonoMac.Foundation.NSArray WritingDirection {
		get;
		set;
	}
}
</nstextlayoutorientation></int></bool></float></int></nsspellingstate></float></bool></monomac.foundation.nsligaturetype></float></float></int></float></pre>
<h3>Type Changed: MonoMac.AppKit.NSTableView</h3>
<p>Added:</p><pre>
 	public NSTableViewToolTip GetToolTip {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSTableViewAnimationOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSTableViewAnimationOptions {
	EffectFade,
	EffectGap,
	SlideUp,
	SlideDown,
	SlideLeft,
	SlideRight
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTableViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual MonoMac.Foundation.NSString GetToolTip (NSTableView tableView, NSCell cell, ref System.Drawing.RectangleF rect, NSTableColumn tableColumn, int row, System.Drawing.PointF mouseLocation);
</pre>
<h3>New Type: MonoMac.AppKit.NSTableViewToolTip</h3>
<pre>
[Serializable]
public delegate MonoMac.Foundation.NSString NSTableViewToolTip (NSTableView tableView, NSCell cell, ref System.Drawing.RectangleF rect, NSTableColumn tableColumn, int row, System.Drawing.PointF mouseLocation);
</pre>
<h3>New Type: MonoMac.AppKit.NSTextAlternatives</h3>
<pre>
public class NSTextAlternatives : MonoMac.Foundation.NSObject {
	
	public NSTextAlternatives ();
	public NSTextAlternatives (MonoMac.Foundation.NSCoder coder);
	public NSTextAlternatives (MonoMac.Foundation.NSObjectFlag t);
	public NSTextAlternatives (IntPtr handle);
	public NSTextAlternatives (string primaryString, MonoMac.Foundation.NSArray alternativeStrings);
	
	protected override void Dispose (bool disposing);
	public virtual void NoteSelectedAlternativeString (string alternativeString);
	
	public static MonoMac.Foundation.NSString SelectedAlternativeStringNotification {
		get;
	}
	public virtual MonoMac.Foundation.NSArray AlternativeStrings {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string PrimaryString {
		get;
	}
	
	public static class Notifications {
		
		public static MonoMac.Foundation.NSObject ObserveSelectedAlternativeString (System.EventHandler<monomac.foundation.nsnotificationeventargs> handler);
	}
}
</monomac.foundation.nsnotificationeventargs></pre>
<h3>Type Changed: MonoMac.AppKit.NSTextContainer</h3>
<p>Added:</p><pre>
 	public virtual NSTextLayoutOrientation LayoutOrientation {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextField</h3>
<p>Added:</p><pre>
 	public virtual float PreferredMaxLayoutWidth {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextFinderMatchingType</h3>
<pre>
[Serializable]
public enum NSTextFinderMatchingType {
	Contains,
	StartsWith,
	FullWord,
	EndsWith
}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextFinderSupport</h3>
<pre>
public static class NSTextFinderSupport {
	
	public static void PerformTextFinderAction (NSResponder This, MonoMac.Foundation.NSObject sender);
}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextLayoutOrientation</h3>
<pre>
[Serializable]
public enum NSTextLayoutOrientation {
	Horizontal,
	Vertical
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTextView</h3>
<p>Added:</p><pre>
 	public virtual void ChangeLayoutOrientation (MonoMac.Foundation.NSObject sender);
 	public virtual MonoMac.Foundation.NSArray QuickLookPreviewableItemsInRanges (MonoMac.Foundation.NSArray ranges);
 	public virtual void SetLayoutOrientation (NSTextLayoutOrientation theOrientation);
 	public virtual void UpdateQuickLookPreviewPanel ();
 	public virtual bool IsIncrementalSearchingEnabled {
 		get;
 		set;
 	}
 	public virtual NSTextLayoutOrientation LayoutOrientation {
 		get;
 	}
 	public virtual bool UsesFindBar {
 		get;
 		set;
 	}
 	public virtual bool UsesInspectorBar {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSTextView_SharingService</h3>
<pre>
public static class NSTextView_SharingService {
	
	public static void OrderFrontSharingServicePicker (NSTextView This, MonoMac.Foundation.NSObject sender);
}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSTypesetter</h3>
<p>Removed:</p><pre>
 	public virtual void LayoutGlyphs (NSLayoutManager layoutManager, uint startGlyphIndex, uint maxLineFragments, uint nextGlyph);
</pre>
<p>Added:</p><pre>
 	public virtual void LayoutGlyphs (NSLayoutManager layoutManager, uint startGlyphIndex, uint maxLineFragments, out uint nextGlyph);
</pre>
<h3>Type Changed: MonoMac.AppKit.NSView</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF RectForSmartMagnificationAtPoint (System.Drawing.PointF atPoint, System.Drawing.RectangleF inRect);
 	public virtual void UpdateLayer ();
 	public virtual bool WantsUpdateLayer {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.AppKit.NSWindow</h3>
<p>Added:</p><pre>
 	public static MonoMac.Foundation.NSString DidChangeBackingPropertiesNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoMac.Foundation.NSObject ObserveDidBecomeKey (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidBecomeMain (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeBackingProperties (EventHandler&lt;NSWindowBackingPropertiesEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeScreen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidChangeScreenProfile (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidDeminiaturize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEndLiveResize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEndSheet (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEnterFullScreen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidEnterVersionBrowser (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidExitFullScreen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidExitVersionBrowser (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidExpose (EventHandler&lt;NSWindowExposeEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidMiniaturize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidMove (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidResignKey (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidResignMain (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidResize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveDidUpdate (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillBeginSheet (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillClose (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillEnterFullScreen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillEnterVersionBrowser (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillExitFullScreen (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillExitVersionBrowser (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillMiniaturize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillMove (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoMac.Foundation.NSObject ObserveWillStartLiveResize (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoMac.AppKit.NSWindowBackingPropertiesEventArgs</h3>
<pre>
public class NSWindowBackingPropertiesEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSWindowBackingPropertiesEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public NSColorSpace OldColorSpace {
		get;
	}
	public int OldScaleFactor {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.AppKit.NSWindowExposeEventArgs</h3>
<pre>
public class NSWindowExposeEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	
	public NSWindowExposeEventArgs (MonoMac.Foundation.NSNotification notification);
	
	public System.Drawing.RectangleF ExposedRect {
		get;
	}
}
</pre>
<h2>Namespace: MonoMac.CoreServices</h2>
<h3>New Type: MonoMac.CoreServices.FSEvent</h3>
<pre>
public struct FSEvent {
	
	public static ulong GetLastEventIdForDeviceBeforeTime (ulong device, double timeInSecondsSinceEpoch);
	public static Guid GetUuidForDevice (ulong device);
	public static bool PurgeEventsForDeviceUpToEventId (ulong device, ulong eventId);
	public override string ToString ();
	
	public static ulong CurrentEventId {
		get;
	}
	public FSEventStreamEventFlags Flags {
		get;
	}
	public ulong Id {
		get;
	}
	public string Path {
		get;
	}
	
	public const ulong SinceNowId = 18446744073709551615;
}
</pre>
<h3>New Type: MonoMac.CoreServices.FSEventStream</h3>
<pre>
public class FSEventStream : IDisposable, MonoMac.ObjCRuntime.INativeObject {
	
	public FSEventStream (MonoMac.CoreFoundation.CFAllocator allocator, MonoMac.Foundation.NSArray pathsToWatch, ulong sinceWhenId, TimeSpan latency, FSEventStreamCreateFlags flags);
	public FSEventStream (string [] pathsToWatch, TimeSpan latency, FSEventStreamCreateFlags flags);
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public uint FlushAsync ();
	public void FlushSync ();
	public void Invalidate ();
	protected virtual void OnEvents (FSEvent[] events);
	public void ScheduleWithRunLoop (MonoMac.CoreFoundation.CFRunLoop runLoop);
	public void ScheduleWithRunLoop (MonoMac.CoreFoundation.CFRunLoop runLoop, MonoMac.Foundation.NSString runLoopMode);
	public void ScheduleWithRunLoop (MonoMac.Foundation.NSRunLoop runLoop);
	public void ScheduleWithRunLoop (MonoMac.Foundation.NSRunLoop runLoop, MonoMac.Foundation.NSString runLoopMode);
	public void Show ();
	public bool Start ();
	public void Stop ();
	public override string ToString ();
	
	public string Description {
		get;
	}
	public IntPtr Handle {
		get;
	}
	public ulong LatestEventId {
		get;
	}
	public string [] PathsBeingWatched {
		get;
	}
	
	public event FSEventStreamEventsHandler Events;
}
</pre>
<h3>New Type: MonoMac.CoreServices.FSEventStreamCreateFlags</h3>
<pre>
[Serializable]
[Flags]
public enum FSEventStreamCreateFlags : uint {
	None,
	NoDefer,
	WatchRoot,
	IgnoreSelf,
	FileEvents
}
</pre>
<h3>New Type: MonoMac.CoreServices.FSEventStreamEventFlags</h3>
<pre>
[Serializable]
[Flags]
public enum FSEventStreamEventFlags : uint {
	None,
	MustScanSubDirs,
	UserDropped,
	KernelDropped,
	EventIdsWrapped,
	HistoryDone,
	RootChanged,
	Mount,
	Unmount,
	ItemCreated,
	ItemRemoved,
	ItemInodeMetaMod,
	ItemRenamed,
	ItemModified,
	ItemFinderInfoMod,
	ItemChangeOwner,
	ItemXattrMod,
	ItemIsFile,
	ItemIsDir,
	ItemIsSymlink
}
</pre>
<h3>New Type: MonoMac.CoreServices.FSEventStreamEventsArgs</h3>
<pre>
public sealed class FSEventStreamEventsArgs : EventArgs {
	
	public FSEvent[] Events {
		get;
	}
}
</pre>
<h3>New Type: MonoMac.CoreServices.FSEventStreamEventsHandler</h3>
<pre>
[Serializable]
public delegate void FSEventStreamEventsHandler (object sender, FSEventStreamEventsArgs args);
</pre>
<h2>Namespace: MonoMac.Foundation</h2>
<h3>Type Changed: MonoMac.Foundation.NSAttributedString</h3>
<p>Added:</p><pre>
 	public NSAttributedString (string str, MonoMac.AppKit.NSStringAttributes attributes);
 	public NSAttributedString (string str, MonoMac.AppKit.NSFont font, MonoMac.AppKit.NSColor foregroundColor, MonoMac.AppKit.NSColor backgroundColor, MonoMac.AppKit.NSColor strokeColor, MonoMac.AppKit.NSColor underlineColor, MonoMac.AppKit.NSColor strikethroughColor, MonoMac.AppKit.NSUnderlineStyle underlineStyle, MonoMac.AppKit.NSUnderlineStyle strikethroughStyle, MonoMac.AppKit.NSParagraphStyle paragraphStyle, float strokeWidth, MonoMac.AppKit.NSShadow shadow, NSUrl link, bool superscript, MonoMac.AppKit.NSTextAttachment attachment, NSLigatureType ligature, float baselineOffset, float kerningAdjustment, float obliqueness, float expansion, MonoMac.AppKit.NSCursor cursor, string toolTip, int characterShape, MonoMac.AppKit.NSGlyphInfo glyphInfo, NSArray writingDirection, bool markedClauseSegment, MonoMac.AppKit.NSTextLayoutOrientation verticalGlyphForm, MonoMac.AppKit.NSTextAlternatives textAlternatives, MonoMac.AppKit.NSSpellingState spellingState);
 	public MonoMac.AppKit.NSStringAttributes GetAppKitAttributes (int location, out NSRange effectiveRange);
 	public MonoMac.AppKit.NSStringAttributes GetAppKitAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
 	public static NSString CharacterShapeAttributeName {
 		get;
 	}
 	public static NSString GlyphInfoAttributeName {
 		get;
 	}
 	public static NSString SpellingStateAttributeName {
 		get;
 	}
 	public static NSString TextAlternativesAttributeName {
 		get;
 	}
 	public static NSString TextLayoutSectionOrientation {
 		get;
 	}
 	public static NSString TextLayoutSectionRange {
 		get;
 	}
 	public static NSString TextLayoutSectionsAttribute {
 		get;
 	}
 	public static int UnderlineByWordMaskAttributeName {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSBundle</h3>
<p>Added:</p><pre>
 	public virtual MonoMac.AppKit.NSImage ImageForResource (string name);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSFileManager</h3>
<p>Added:</p><pre>
 	public virtual bool TrashItem (NSUrl url, out NSUrl resultingItemUrl, out NSError error);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSFilePresenter</h3>
<p>Added:</p><pre>
 	public virtual NSUrl PrimaryPresentedItemUrl {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.Foundation.NSThread</h3>
<p>Added:</p><pre>
 	public static NSThread Start (NSAction action);
</pre>
<h3>Type Changed: MonoMac.Foundation.NSValue</h3>
<p>Added:</p><pre>
 	public static NSValue FromVector (MonoMac.SceneKit.SCNVector3 vector);
 	public static NSValue FromVector (MonoMac.SceneKit.SCNVector4 vector);
 	public virtual MonoMac.SceneKit.SCNVector3 Vector3Value {
 		get;
 	}
 	public virtual MonoMac.SceneKit.SCNVector4 Vector4Value {
 		get;
 	}
</pre>
<h2>Namespace: MonoMac.SceneKit</h2>

<p>The majority of the changes are related to the move from
OpenGL.Vector3 to SCNVector3 in preparation for 64-bit support.

<p>To preserve source code compatibility, we now have implicit
operators that convert between those types.

<h3>Type Changed: MonoMac.SceneKit.SCNGeometry</h3>
<p>Removed:</p><pre>
 	public virtual bool GetBoundingBoxMinmax (MonoMac.OpenGL.Vector3 min, MonoMac.OpenGL.Vector3 max);
 	public virtual bool GetBoundingSphereCenterradius (MonoMac.OpenGL.Vector3 center, float radius);
</pre>
<p>Added:</p><pre>
 	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
 	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNGeometryElement</h3>
<p>Removed:</p><pre>
 	public virtual SCNGeometryElement FromData (MonoMac.Foundation.NSData data, SCNGeometryPrimitiveType primitiveType, int primitiveCount, int bytesPerIndex);
</pre>
<p>Added:</p><pre>
 	public static SCNGeometryElement FromData (MonoMac.Foundation.NSData data, SCNGeometryPrimitiveType primitiveType, int primitiveCount, int bytesPerIndex);
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNGeometrySource</h3>
<p>Removed:</p><pre>
 	public static SCNGeometrySource FromNormals (MonoMac.OpenGL.Vector3[] normals);
 	public static SCNGeometrySource FromVertices (MonoMac.OpenGL.Vector3[] vertices);
</pre>
<p>Added:</p><pre>
 	public static SCNGeometrySource FromNormals (SCNVector3[] normals);
 	public static SCNGeometrySource FromVertices (SCNVector3[] vertices);
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNHitTestResult</h3>
<p>Removed:</p><pre>
 	public virtual MonoMac.OpenGL.Vector3 LocalCoordinates {
 	public virtual MonoMac.OpenGL.Vector3 LocalNormal {
 	public virtual MonoMac.OpenGL.Vector3 WorldCoordinates {
 	public virtual MonoMac.OpenGL.Vector3 WorldNormal {
</pre>
<p>Added:</p><pre>
 	public virtual SCNVector3 LocalCoordinates {
 	public virtual SCNVector3 LocalNormal {
 	public virtual SCNVector3 WorldCoordinates {
 	public virtual SCNVector3 WorldNormal {
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNMaterialProperty</h3>
<p>Added:</p><pre>
 		set;
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNNode</h3>
<p>Removed:</p><pre>
 	public virtual bool GetBoundingBoxMinmax (MonoMac.OpenGL.Vector3 min, MonoMac.OpenGL.Vector3 max);
 	public virtual bool GetBoundingSphereCenterradius (MonoMac.OpenGL.Vector3 center, float radius);
 	public virtual MonoMac.OpenGL.Vector3 Position {
 	public SCNNodeRendererDelegate RenderDelegate {
 	public virtual MonoMac.OpenGL.Vector4 Rotation {
 	public virtual MonoMac.OpenGL.Vector3 Scale {
 	public virtual MonoMac.Foundation.NSObject WeakRenderDelegate {
</pre>
<p>Added:</p><pre>
 	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
 	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
 	public virtual SCNVector3 Position {
 	public SCNNodeRendererDelegate RendererDelegate {
 	public virtual SCNVector4 Rotation {
 	public virtual SCNVector3 Scale {
 	public virtual MonoMac.Foundation.NSObject WeakRendererDelegate {
</pre>
<h3>Type Changed: MonoMac.SceneKit.SCNScene</h3>
<p>Removed:</p><pre>
 	public virtual MonoMac.Foundation.NSObject SetAttribute (MonoMac.Foundation.NSObject attribute, MonoMac.Foundation.NSString key);
</pre>
<p>Added:</p><pre>
 	public virtual void SetAttribute (MonoMac.Foundation.NSObject attribute, MonoMac.Foundation.NSString key);
</pre>
<h3>New Type: MonoMac.SceneKit.SCNVector3</h3>
<pre>
public struct SCNVector3 {
	
	public SCNVector3 (MonoMac.OpenGL.Vector3 vector);
	
	public static implicit operator SCNVector3 (MonoMac.OpenGL.Vector3 vector);
	public static explicit operator MonoMac.OpenGL.Vector3 (SCNVector3 source);
	
	public float X;
	public float Y;
	public float Z;
}
</pre>
<h3>New Type: MonoMac.SceneKit.SCNVector4</h3>
<pre>
public struct SCNVector4 {
	
	public SCNVector4 (MonoMac.OpenGL.Vector4 vector);
	
	public static implicit operator SCNVector4 (MonoMac.OpenGL.Vector4 vector);
	public static explicit operator MonoMac.OpenGL.Vector4 (SCNVector4 source);
	
	public float X;
	public float Y;
	public float Z;
	public float W;
}
</pre>
<h2>Namespace: MonoMac.WebKit</h2>
<h3>New Type: MonoMac.WebKit.WebActionMouseButton</h3>
<pre>
[Serializable]
public enum WebActionMouseButton {
	None,
	Left,
	Middle,
	Right
}
</pre>
<h3>Type Changed: MonoMac.WebKit.WebNavigationPolicyEventArgs</h3>
<p>Added:</p><pre>
 	public MonoMac.Foundation.NSDictionary ElementInfo {
 		get;
 	}
 	public uint Flags {
 		get;
 	}
 	public WebActionMouseButton MouseButton {
 		get;
 	}
 	public WebNavigationType NavigationType {
 		get;
 	}
 	public MonoMac.Foundation.NSUrl OriginalUrl {
 		get;
 	}
</pre>
<h3>Type Changed: MonoMac.WebKit.WebPolicyDelegate</h3>
<p>Added:</p><pre>
 	
 	public static MonoMac.Foundation.NSString WebActionButtonKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WebActionElementKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WebActionModifierFlagsKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WebActionNavigationTypeKey {
 		get;
 	}
 	public static MonoMac.Foundation.NSString WebActionOriginalUrlKey {
 		get;
 	}
</pre>
</body>
</html>
