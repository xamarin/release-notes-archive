---
id: 39F6B646-074E-4F16-9F94-33830DC12B97
title: "Mac 3.4 to 3.99.3"
---

<style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script># Xamarin.Mac.dll

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UpdatesNowPlayingInfoCenter { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : AppKit.NSView, AppKit.INSAccessibility, AppKit.INSAccessibilityElementProtocol, AppKit.INSAppearanceCustomization, AppKit.INSDraggingDestination, AppKit.INSTouchBarProvider, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RoutePickerButtonBordered { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSColor GetRoutePickerButtonColor (AVRoutePickerViewButtonState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetRoutePickerButtonColor (AppKit.NSColor color, AVRoutePickerViewButtonState state);</span>
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonState -->
<h3>New Type AVKit.AVRoutePickerViewButtonState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveHighlighted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalHighlighted = 1,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonState -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : Foundation.NSObject, IAVRoutePickerViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAccount (ACAccount account, ACAccountStoreRemoveCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RemoveAccountAsync (ACAccount account);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore -->
<div> <!-- start type ACAccountStoreRemoveCompletionHandler -->
<h3>New Type Accounts.ACAccountStoreRemoveCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ACAccountStoreRemoveCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ACAccountStoreRemoveCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool success, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool success, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type ACAccountStoreRemoveCompletionHandler -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CustomTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LanguageTextAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PageRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSAccessibilitySubroles --> <div>
<h3>Type Changed: AppKit.NSAccessibilitySubroles</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TabButtonSubrole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilitySubroles -->
<!-- start type NSAccessibility_Extensions --> <div>
<h3>Type Changed: AppKit.NSAccessibility_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityElement[] GetAccessibilityChildrenInNavigationOrder (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomAction[] GetAccessibilityCustomActions (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomRotor[] GetAccessibilityCustomRotors (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityChildrenInNavigationOrder (INSAccessibility This, NSAccessibilityElement[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomActions (INSAccessibility This, NSAccessibilityCustomAction[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (INSAccessibility This, NSAccessibilityCustomRotor[] value);</span>
</pre>
</div>

</div> <!-- end type NSAccessibility_Extensions -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationOpenUrlsEventArgs&gt; OpenUrls;</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrls (NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenUrls (INSApplicationDelegate This, NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBezierPath --> <div>
<h3>Type Changed: AppKit.NSBezierPath</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (uint[], NSFont)' instead.")]
	public void AppendPathWithGlyphs (uint[] glyphs, NSFont font);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (CGPoint[])' instead.")]
	public void AppendPathWithPoints (CoreGraphics.CGPoint[] points);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Append (NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (CoreGraphics.CGPoint[] points);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (uint[] glyphs, NSFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AppendBezierPathWithCGGlyph (ushort glyph, NSFont font);</span>
</pre>
</div>

</div> <!-- end type NSBezierPath -->
<!-- start type NSButton --> <div>
<h3>Type Changed: AppKit.NSButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSButton -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCollectionViewPrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewTransitionLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewTransitionLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set currentLayout and newLayout.")]
	public NSCollectionViewTransitionLayout ();</span>
</div></pre>

</div> <!-- end type NSCollectionViewTransitionLayout -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBrownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemOrangeColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPinkColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPurpleColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemRedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemYellowColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorType Type { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name, Foundation.NSBundle bundle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSColor GetColor (NSColorType type);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorPickerTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSColorPickerTouchBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorSpace[] AllowedColorSpaces { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSColorPickerTouchBarItem -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentSharing { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (NSSharingServicePicker sharingServicePicker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShareDocument (NSSharingService sharingService, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; ShareDocumentAsync (NSSharingService sharingService);</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDocumentController --> <div>
<h3>Type Changed: AppKit.NSDocumentController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsAutomaticShareMenu { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMenuItem StandardShareMenuItem { get; }</span>
</pre>
</div>

</div> <!-- end type NSDocumentController -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: AppKit.NSFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSFont FromCTFont (CoreText.CTFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAdvancement (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGSize[] GetAdvancements (ushort[] glyphs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundingRect (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGRect[] GetBoundingRects (ushort[] glyphs);</span>
</pre>
</div>

</div> <!-- end type NSFont -->
<!-- start type NSFontDescriptor --> <div>
<h3>Type Changed: AppKit.NSFontDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFontAssetRequest { get; }</span>
</pre>
</div>

</div> <!-- end type NSFontDescriptor -->
<!-- start type NSFontSymbolicTraits --> <div>
<h3>Type Changed: AppKit.NSFontSymbolicTraits</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TraitLooseLeading = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">TraitTightLeading = 32768,</span>
</pre>
</div>

</div> <!-- end type NSFontSymbolicTraits -->
<!-- start type NSGlyphInfo --> <div>
<h3>Type Changed: AppKit.NSGlyphInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BaseString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort GlyphId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGlyphInfo GetGlyphInfo (ushort glyph, NSFont font, string string);</span>
</pre>
</div>

</div> <!-- end type NSGlyphInfo -->
<!-- start type NSGroupTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSGroupTouchBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions EffectiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection GroupUserInterfaceLayoutDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredItemWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersEqualWidths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions[] PrioritizedCompressionOptions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateAlertStyleGroupItem (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items, NSUserInterfaceCompressionOptions allowedCompressionOptions);</span>
</pre>
</div>

</div> <!-- end type NSGroupTouchBarItem -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: AppKit.NSImageName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarRemoveTemplate = 116,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSLayoutAnchor`1 --> <div>
<h3>Type Changed: AppKit.NSLayoutAnchor`1</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutConstraint[] ConstraintsAffectingLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAmbiguousLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSLayoutAnchor`1 -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutXAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutYAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: AppKit.NSLevelIndicator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor CriticalFillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DrawsTieredCapacityLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor FillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLevelIndicatorPlaceholderVisibility PlaceholderVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingPlaceholderImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor WarningFillColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsKeyEquivalentWhenHidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLLayer --> <div>
<h3>Type Changed: AppKit.NSOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSOpenGLLayer -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: AppKit.NSPasteboard</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFont { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameGeneral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameRuler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeFileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeUrl { get; }</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: AppKit.NSPopUpButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAppearanceCustomization</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'GetAppearance' and 'SetAppearance' methods instead.")]
	public virtual NSPopoverAppearance Appearance { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAppearance EffectiveAppearance { get; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: AppKit.NSResponder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSegmentDistribution SegmentDistribution { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTextAlignment GetAlignment (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetTag (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetToolTip (nint forSegment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlignment (NSTextAlignment alignment, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetShowsMenuIndicator (bool showsMenuIndicator, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTag (nint tag, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetToolTip (string toolTip, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShowsMenuIndicator (nint segment);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSliderTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSSliderTouchBarItem</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
</pre>
</div>

</div> <!-- end type NSSliderTouchBarItem -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceValidations</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStatusBarButton --> <div>
<h3>Type Changed: AppKit.NSStatusBarButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>

</div> <!-- end type NSStatusBarButton -->
<!-- start type NSStoryboard --> <div>
<h3>Type Changed: AppKit.NSStoryboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSStoryboard MainStoryboard { get; }</span>
</pre>
</div>

</div> <!-- end type NSStoryboard -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesAutomaticRowHeights { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSText --> <div>
<h3>Type Changed: AppKit.NSText</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovementUserInfoKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSText -->
<!-- start type NSTextList --> <div>
<h3>Type Changed: AppKit.NSTextList</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextList (NSTextListMarkerFormats format, NSTextListOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSTextList -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbar ();</span>
</pre>
</div>

</div> <!-- end type NSToolbar -->
<!-- start type NSTouchBar --> <div>
<h3>Type Changed: AppKit.NSTouchBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EscapeKeyReplacementItemIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTouchBar -->
<!-- start type NSTouchBarItemIdentifier --> <div>
<h3>Type Changed: AppKit.NSTouchBarItemIdentifier</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CandidateList = 10,</span>
</pre>
</div>

</div> <!-- end type NSTouchBarItemIdentifier -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTab Tab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabGroup TabGroup { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the EndSheet(NSWindow,NSModalResponse) overload.")]
	public virtual void EndSheet (NSWindow sheetWindow, nint returnCode);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSheet (NSWindow sheetWindow, NSModalResponse returnCode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabOverview (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SwitchControlEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool VoiceOverEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type DownloadFontAssetsRequestCompletionHandler -->
<h3>New Type AppKit.DownloadFontAssetsRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DownloadFontAssetsRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DownloadFontAssetsRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DownloadFontAssetsRequestCompletionHandler -->
<div> <!-- start type INSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.INSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityCustomRotorItemSearchDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type INSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type INSAccessibilityElementLoading -->
<h3>New Type AppKit.INSAccessibilityElementLoading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityElementLoading : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityElement GetAccessibilityElement (Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type INSAccessibilityElementLoading -->
<div> <!-- start type INSCollectionViewPrefetching -->
<h3>New Type AppKit.INSCollectionViewPrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewPrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type INSCollectionViewPrefetching -->
<div> <!-- start type INSUserInterfaceCompression -->
<h3>New Type AppKit.INSUserInterfaceCompression</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceCompression : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceCompression -->
<div> <!-- start type NSAboutPanelOption -->
<h3>New Type AppKit.NSAboutPanelOption</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAboutPanelOption {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationIcon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Credits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Version { get; }</span>
}
</pre>
</div> <!-- end type NSAboutPanelOption -->
<div> <!-- start type NSAccessibilityAnnotationAttributeKey -->
<h3>New Type AppKit.NSAccessibilityAnnotationAttributeKey</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityAnnotationAttributeKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLocation { get; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationAttributeKey -->
<div> <!-- start type NSAccessibilityAnnotationPosition -->
<h3>New Type AppKit.NSAccessibilityAnnotationPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityAnnotationPosition {
	<span class='added added-field ' data-is-non-breaking="">End = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FullRange = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationPosition -->
<div> <!-- start type NSAccessibilityCustomAction -->
<h3>New Type AppKit.NSAccessibilityCustomAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, System.Func&lt;bool&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, Foundation.NSObject target, ObjCRuntime.Selector selector);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;bool&gt; Handler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Selector { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomAction -->
<div> <!-- start type NSAccessibilityCustomRotor -->
<h3>New Type AppKit.NSAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (NSAccessibilityCustomRotorType rotorType, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (string label, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityElementLoading ItemLoadingDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityCustomRotorItemSearchDelegate ItemSearchDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotor -->
<div> <!-- start type NSAccessibilityCustomRotorItemResult -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorItemResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (NSAccessibilityElement targetElement);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (Foundation.INSSecureCoding itemLoadingToken, string customLabel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSSecureCoding ItemLoadingToken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement TargetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemResult -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSAccessibilityCustomRotorItemSearchDelegate : Foundation.NSObject, INSAccessibilityCustomRotorItemSearchDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type NSAccessibilityCustomRotorSearchDirection -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorSearchDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchDirection -->
<div> <!-- start type NSAccessibilityCustomRotorSearchParameters -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchParameters</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorSearchParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FilterString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorSearchDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchParameters -->
<div> <!-- start type NSAccessibilityCustomRotorType -->
<h3>New Type AppKit.NSAccessibilityCustomRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorType {
	<span class='added added-field ' data-is-non-breaking="">Annotation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BoldText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlinedText = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 20,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorType -->
<div> <!-- start type NSAccessibilityElementLoading_Extensions -->
<h3>New Type AppKit.NSAccessibilityElementLoading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityElementLoading_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSRange GetAccessibilityRangeInTargetElement (INSAccessibilityElementLoading This, Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type NSAccessibilityElementLoading_Extensions -->
<div> <!-- start type NSApplicationOpenUrlsEventArgs -->
<h3>New Type AppKit.NSApplicationOpenUrlsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationOpenUrlsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationOpenUrlsEventArgs (Foundation.NSUrl[] urls);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl[] Urls { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationOpenUrlsEventArgs -->
<div> <!-- start type NSCollectionViewPrefetching_Extensions -->
<h3>New Type AppKit.NSCollectionViewPrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewPrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (INSCollectionViewPrefetching This, NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type NSCollectionViewPrefetching_Extensions -->
<div> <!-- start type NSColorType -->
<h3>New Type AppKit.NSColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSColorType {
	<span class='added added-field ' data-is-non-breaking="">Catalog = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ComponentBased = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pattern = 1,</span>
}
</pre>
</div> <!-- end type NSColorType -->
<div> <!-- start type NSFontAssetRequest -->
<h3>New Type AppKit.NSFontAssetRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSFontAssetRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (NSFontDescriptor[] fontDescriptors, NSFontAssetRequestOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFontDescriptor[] DownloadedFontDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSProgress Progress { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DownloadFontAssets (DownloadFontAssetsRequestCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type NSFontAssetRequest -->
<div> <!-- start type NSFontAssetRequestOptions -->
<h3>New Type AppKit.NSFontAssetRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontAssetRequestOptions {
	<span class='added added-field ' data-is-non-breaking="">UsesStandardUI = 1,</span>
}
</pre>
</div> <!-- end type NSFontAssetRequestOptions -->
<div> <!-- start type NSFontError -->
<h3>New Type AppKit.NSFontError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFontError {
	<span class='added added-field ' data-is-non-breaking="">AssetDownloadError = 66304,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMaximum = 66335,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMinimum = 66304,</span>
}
</pre>
</div> <!-- end type NSFontError -->
<div> <!-- start type NSFontPanelModeMask -->
<h3>New Type AppKit.NSFontPanelModeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontPanelModeMask {
	<span class='added added-field ' data-is-non-breaking="">AllEffects = 1048320,</span>
	<span class='added added-field ' data-is-non-breaking="">AllModes = 4294967295,</span>
	<span class='added added-field ' data-is-non-breaking="">Collection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentColorEffect = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Face = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShadowEffect = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StandardModes = 65535,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikethroughEffect = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorEffect = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineEffect = 256,</span>
}
</pre>
</div> <!-- end type NSFontPanelModeMask -->
<div> <!-- start type NSLevelIndicatorPlaceholderVisibility -->
<h3>New Type AppKit.NSLevelIndicatorPlaceholderVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLevelIndicatorPlaceholderVisibility {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WhileEditing = 2,</span>
}
</pre>
</div> <!-- end type NSLevelIndicatorPlaceholderVisibility -->
<div> <!-- start type NSObject_NSFontPanelValidationAdditions -->
<h3>New Type AppKit.NSObject_NSFontPanelValidationAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_NSFontPanelValidationAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFontPanelModeMask GetValidModes (Foundation.NSObject This, NSFontPanel fontPanel);</span>
}
</pre>
</div> <!-- end type NSObject_NSFontPanelValidationAdditions -->
<div> <!-- start type NSRulerViewUnits -->
<h3>New Type AppKit.NSRulerViewUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSRulerViewUnits {
	<span class='added added-field ' data-is-non-breaking="">Centimeters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inches = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Picas = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
}
</pre>
</div> <!-- end type NSRulerViewUnits -->
<div> <!-- start type NSRulerViewUnitsExtensions -->
<h3>New Type AppKit.NSRulerViewUnitsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRulerViewUnitsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSRulerViewUnits self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRulerViewUnits GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSRulerViewUnitsExtensions -->
<div> <!-- start type NSSegmentDistribution -->
<h3>New Type AppKit.NSSegmentDistribution</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSegmentDistribution {
	<span class='added added-field ' data-is-non-breaking="">Fill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FillEqually = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FillProportionally = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fit = 0,</span>
}
</pre>
</div> <!-- end type NSSegmentDistribution -->
<div> <!-- start type NSTextListMarkerFormats -->
<h3>New Type AppKit.NSTextListMarkerFormats</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTextListMarkerFormats {
	<span class='added added-field ' data-is-non-breaking="">Box = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Check = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimal = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Disc = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hyphen = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseAlpha = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseHexadecimal = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseLatin = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseRoman = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Octal = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseAlpha = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseHexadecimal = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseLatin = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseRoman = 15,</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormats -->
<div> <!-- start type NSTextListMarkerFormatsExtensions -->
<h3>New Type AppKit.NSTextListMarkerFormatsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextListMarkerFormatsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSTextListMarkerFormats self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextListMarkerFormats GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormatsExtensions -->
<div> <!-- start type NSUserInterfaceCompressionOptions -->
<h3>New Type AppKit.NSUserInterfaceCompressionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserInterfaceCompressionOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSSet&lt;NSUserInterfaceCompressionOptions&gt; options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions BreakEqualWidthsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Empty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideImagesOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideTextOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions ReduceMetricsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions StandardOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByAdding (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByRemoving (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSUserInterfaceCompressionOptions options);</span>
}
</pre>
</div> <!-- end type NSUserInterfaceCompressionOptions -->
<div> <!-- start type NSWindowTab -->
<h3>New Type AppKit.NSWindowTab</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTab : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView AccessoryView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; set; }</span>
}
</pre>
</div> <!-- end type NSWindowTab -->
<div> <!-- start type NSWindowTabGroup -->
<h3>New Type AppKit.NSWindowTabGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTabGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OverviewVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow SelectedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabBarVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] Windows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (NSWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Insert (NSWindow window, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (NSWindow window);</span>
}
</pre>
</div> <!-- end type NSWindowTabGroup -->

</div> <!-- end namespace AppKit -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioChannelLabel --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLabel</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HoaAcn = 500,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn0 = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn1 = 131073,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn10 = 131082,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn11 = 131083,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn12 = 131084,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn13 = 131085,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn14 = 131086,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn15 = 131087,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn2 = 131074,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn3 = 131075,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn4 = 131076,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn5 = 131077,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn6 = 131078,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn65024 = 196096,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn7 = 131079,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn8 = 131080,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn9 = 131081,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLabel -->
<!-- start type AudioChannelLayoutTag --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLayoutTag</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_N3D = 12517376,</span>
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_SN3D = 12451840,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLayoutTag -->
<!-- start type AudioFormatType --> <div>
<h3>Type Changed: AudioToolbox.AudioFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Flac = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">Opus = 1869641075,</span>
</pre>
</div>

</div> <!-- end type AudioFormatType -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKFetchRecordZoneChangesOptions --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZoneChangesOptions</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CKFetchRecordZoneChangesOptions -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContact --> <div>
<h3>Type Changed: Contacts.CNContact</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
</pre>
</div>

</div> <!-- end type CNContact -->
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
	<span class='added added-field ' data-is-non-breaking="">VCardMalformed = 700,</span>
</pre>
</div>

</div> <!-- end type CNErrorCode -->
<!-- start type CNLabelContactRelationKey --> <div>
<h3>Type Changed: Contacts.CNLabelContactRelationKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Daughter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Son { get; }</span>
</pre>
</div>

</div> <!-- end type CNLabelContactRelationKey -->
<!-- start type CNMutableContact --> <div>
<h3>Type Changed: Contacts.CNMutableContact</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
</pre>
</div>

</div> <!-- end type CNMutableContact -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAConstraint --> <div>
<h3>Type Changed: CoreAnimation.CAConstraint</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAConstraint -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CACornerMask MaskedCorners { get; set; }</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsNextDrawableTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaySyncEnabled { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAOpenGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAOpenGLLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->
<div> <!-- start type CACornerMask -->
<h3>New Type CoreAnimation.CACornerMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CACornerMask {
	<span class='added added-field ' data-is-non-breaking="">MaxXMaxYCorner = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxXMinYCorner = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMaxYCorner = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMinYCorner = 1,</span>
}
</pre>
</div> <!-- end type CACornerMask -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreAudioKit --> <div> 
<h2>Namespace CoreAudioKit</h2>
<div> <!-- start type AUAudioUnitViewConfiguration -->
<h3>New Type CoreAudioKit.AUAudioUnitViewConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class AUAudioUnitViewConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (nfloat width, nfloat height, bool hostHasController);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HostHasController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewConfiguration -->
<div> <!-- start type AUAudioUnitViewControllerExtensions -->
<h3>New Type CoreAudioKit.AUAudioUnitViewControllerExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AUAudioUnitViewControllerExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSIndexSet GetSupportedViewConfigurations (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration[] availableViewConfigurations);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SelectViewConfiguration (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration viewConfiguration);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewControllerExtensions -->

</div> <!-- end namespace CoreAudioKit -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CoreSpotlightExporter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UbiquitousContainerIdentifierKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSPropertyDescription&gt; UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: CoreImage.CIImageAccumulator</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("The default initializer does not work in recent iOS version (11b4).")]
	public CIImageAccumulator ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the overload acceping a 'CIFormat' enum instead of an 'int'.")]
	public CIImageAccumulator (CoreGraphics.CGRect rectangle, int ciImageFormat);</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload acceping a 'CIFormat' enum instead of an 'int'.")]
	public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, int ciImageFormat);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, CIFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeDescriptor -->
<h3>New Type CoreImage.CIBarcodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIBarcodeDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CIBarcodeDescriptor -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithBlueMask -->
<div> <!-- start type CIBlendWithRedMask -->
<h3>New Type CoreImage.CIBlendWithRedMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithRedMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithRedMask -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->
<!-- start type CLPlacemark --> <div>
<h3>Type Changed: CoreLocation.CLPlacemark</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Contacts.CNPostalAddress PostalAddress { get; }</span>
</pre>
</div>

</div> <!-- end type CLPlacemark -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMAttachmentBearer --> <div>
<h3>Type Changed: CoreMedia.CMAttachmentBearer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVBuffer --> <div>
<h3>Type Changed: CoreVideo.CVBuffer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CVBuffer -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKAlarm --> <div>
<h3>Type Changed: EventKit.EKAlarm</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the static methods FromDate or FromTimeInterval to create alarms")]
	public EKAlarm ();</span>
</div></pre>

</div> <!-- end type EKAlarm -->
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public EKEventStore (EKSource[] sources);</span>
</pre>
</div>

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace FinderSync --> <div> 
<h2>Namespace FinderSync</h2>
<!-- start type FIFinderSync --> <div>
<h3>Type Changed: FinderSync.FIFinderSync</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetValues (string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SupportedServiceNames (Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSync -->
<!-- start type FIFinderSyncController --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDate GetLastUsedDate (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetTagData (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLastUsedDate (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetLastUsedDateAsync (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTagData (Foundation.NSData tagData, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetTagDataAsync (Foundation.NSData tagData, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncController -->
<!-- start type FIFinderSyncProtocol_Extensions --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncProtocol_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetValues (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] SupportedServiceNames (IFIFinderSyncProtocol This, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncProtocol_Extensions -->
<div> <!-- start type GetValuesCompletionHandler -->
<h3>New Type FinderSync.GetValuesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GetValuesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GetValuesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GetValuesCompletionHandler -->

</div> <!-- end namespace FinderSync -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSActivityOptions --> <div>
<h3>Type Changed: Foundation.NSActivityOptions</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	IdleDisplaySleepDisabled = <span class='removed removed-inline removed-breaking-inline'>256</span> <span class='added '>1099511627776</span>
</div></pre>

</div> <!-- end type NSActivityOptions -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Not intended to be directly instantiated, this is an abstract class.")]
	public NSDimension ();</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnmountVolume (NSUrl url, NSFileManagerUnmountOptions mask, System.Action&lt;NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UnmountVolumeAsync (NSUrl url, NSFileManagerUnmountOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSFileManager -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type ProtocolAttribute --> <div>
<h3>Type Changed: Foundation.ProtocolAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string FormalSince { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProtocolAttribute -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type NSFileProviderMessageInterface -->
<h3>New Type Foundation.NSFileProviderMessageInterface</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderMessageInterface : Foundation.NSObject, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileProviderMessageInterface (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderMessageInterface (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFileProviderMessageInterface -->
<div> <!-- start type NotImplementedAttribute -->
<h3>New Type Foundation.NotImplementedAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class NotImplementedAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NotImplementedAttribute (string message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
}
</pre>
</div> <!-- end type NotImplementedAttribute -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAttitudeAndRotationRate { get; }</span>
</pre>
</div>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestination --> <div>
<h3>Type Changed: ImageIO.CGImageDestination</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAuxiliaryDataInfo (CGImageDestination dest, CGImageAuxiliaryDataType auxiliaryImageDataType, CGImageAuxiliaryDataInfo auxiliaryDataInfo);</span>
</pre>
</div>

</div> <!-- end type CGImageDestination -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileContentsDictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Images { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NamedColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Width { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->
<!-- start type CGImageSource --> <div>
<h3>Type Changed: ImageIO.CGImageSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo CopyAuxiliaryDataInfo (CGImageSource imageSource, uint index, CGImageAuxiliaryDataType auxiliaryImageDataType);</span>
</pre>
</div>

</div> <!-- end type CGImageSource -->
<div> <!-- start type CGImageAuxiliaryDataInfo -->
<h3>New Type ImageIO.CGImageAuxiliaryDataInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGImageAuxiliaryDataInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData DepthData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary DepthDataDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CGImageMetadata Metadata { get; set; }</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataInfo -->
<div> <!-- start type CGImageAuxiliaryDataType -->
<h3>New Type ImageIO.CGImageAuxiliaryDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGImageAuxiliaryDataType {
	<span class='added added-field ' data-is-non-breaking="">Depth = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disparity = 1,</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataType -->
<div> <!-- start type CGImageAuxiliaryDataTypeExtensions -->
<h3>New Type ImageIO.CGImageAuxiliaryDataTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CGImageAuxiliaryDataTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CGImageAuxiliaryDataType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGImageAuxiliaryDataType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataTypeExtensions -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InteractionNotAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedReason { get; set; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<!-- start type LAStatus --> <div>
<h3>Type Changed: LocalAuthentication.LAStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NotInteractive = -1004,</span>
</pre>
</div>

</div> <!-- end type LAStatus -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationView ClusterAnnotationView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ClusteringIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationViewCollisionMode CollisionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float DisplayPriority { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareForDisplay ();</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapType --> <div>
<h3>Type Changed: MapKit.MKMapType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MutedStandard = 5,</span>
</pre>
</div>

</div> <!-- end type MKMapType -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MKCreateClusterAnnotation CreateClusterAnnotation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKAnnotationView DequeueReusableAnnotation (string identifier, IMKAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Register (ObjCRuntime.Class viewClass, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (System.Type viewType, string identifier);</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation CreateClusterAnnotation (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MKClusterAnnotation CreateClusterAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate, Contacts.CNPostalAddress postalAddress);</span>
</pre>
</div>

</div> <!-- end type MKPlacemark -->
<div> <!-- start type MKAnnotationViewCollisionMode -->
<h3>New Type MapKit.MKAnnotationViewCollisionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKAnnotationViewCollisionMode {
	<span class='added added-field ' data-is-non-breaking="">Circle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rectangle = 0,</span>
}
</pre>
</div> <!-- end type MKAnnotationViewCollisionMode -->
<div> <!-- start type MKClusterAnnotation -->
<h3>New Type MapKit.MKClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class MKClusterAnnotation : Foundation.NSObject, Foundation.INSObjectProtocol, IMKAnnotation, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKClusterAnnotation (IMKAnnotation[] memberAnnotations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMKAnnotation[] MemberAnnotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);</span>
}
</pre>
</div> <!-- end type MKClusterAnnotation -->
<div> <!-- start type MKCreateClusterAnnotation -->
<h3>New Type MapKit.MKCreateClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MKCreateClusterAnnotation : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCreateClusterAnnotation (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation[] memberAnnotations, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation Invoke (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
}
</pre>
</div> <!-- end type MKCreateClusterAnnotation -->
<div> <!-- start type MKFeatureDisplayPriority -->
<h3>New Type MapKit.MKFeatureDisplayPriority</h3>
<pre class='added' data-is-non-breaking="">
public static class MKFeatureDisplayPriority {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float Required;</span>
}
</pre>
</div> <!-- end type MKFeatureDisplayPriority -->
<div> <!-- start type MKFeatureVisibility -->
<h3>New Type MapKit.MKFeatureVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKFeatureVisibility {
	<span class='added added-field ' data-is-non-breaking="">Adaptive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type MKFeatureVisibility -->
<div> <!-- start type MKMapViewDefault -->
<h3>New Type MapKit.MKMapViewDefault</h3>
<pre class='added' data-is-non-breaking="">
public static class MKMapViewDefault {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationViewReuseIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClusterAnnotationViewReuseIdentifier { get; }</span>
}
</pre>
</div> <!-- end type MKMapViewDefault -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaLibrary --> <div> 
<h2>Namespace MediaLibrary</h2>
<!-- start type MediaLibraryTypeIdentifierKey --> <div>
<h3>Type Changed: MediaLibrary.MediaLibraryTypeIdentifierKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosAnimatedGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLivePhotosGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLongExposureGroupTypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MediaLibraryTypeIdentifierKey -->

</div> <!-- end namespace MediaLibrary -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPContentItem --> <div>
<h3>Type Changed: MediaPlayer.MPContentItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExplicitContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StreamingContent { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPContentItem -->
<!-- start type MPFeedbackCommand --> <div>
<h3>Type Changed: MediaPlayer.MPFeedbackCommand</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedShortTitle { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPFeedbackCommand -->
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfo NowPlaying { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<!-- start type MPRemoteCommandHandlerStatus --> <div>
<h3>Type Changed: MediaPlayer.MPRemoteCommandHandlerStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DeviceNotFound = 120,</span>
</pre>
</div>

</div> <!-- end type MPRemoteCommandHandlerStatus -->
<div> <!-- start type MPMediaItem -->
<h3>New Type MediaPlayer.MPMediaItem</h3>
<pre class='added' data-is-non-breaking="">
public class MPMediaItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumArtistPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumArtistProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTrackCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTrackNumberProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtistPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtistProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtworkProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetURLProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BeatsPerMinuteProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BookmarkTimeProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CommentsProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ComposerPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ComposerProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DateAddedProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DiscCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DiscNumberProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GenrePersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GenreProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HasProtectedAssetProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsCloudItemProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsCompilationProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsExplicitProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LastPlayedDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LyricsProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MediaTypeProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlayCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackDurationProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackStoreIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PodcastPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PodcastTitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPersistentID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RatingProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReleaseDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SkipCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserGroupingProperty { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanFilterByProperty (Foundation.NSString property);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetObject (Foundation.NSObject key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);</span>
}
</pre>
</div> <!-- end type MPMediaItem -->
<div> <!-- start type MPMediaItemEnumerator -->
<h3>New Type MediaPlayer.MPMediaItemEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MPMediaItemEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string property, Foundation.NSObject value, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string property, Foundation.NSObject value, bool stop);</span>
}
</pre>
</div> <!-- end type MPMediaItemEnumerator -->
<div> <!-- start type MPNowPlayingInfo -->
<h3>New Type MediaPlayer.MPNowPlayingInfo</h3>
<pre class='added' data-is-non-breaking="">
public class MPNowPlayingInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPNowPlayingInfo ();</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public string AlbumTitle;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? AlbumTrackCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? AlbumTrackNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Artist;</span>
	<span class='added added-field ' data-is-non-breaking="">public MPMediaItemArtwork Artwork;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? ChapterCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? ChapterNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Composer;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? DefaultPlaybackRate;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? DiscCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? DiscNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? ElapsedPlaybackTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Genre;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong? PersistentID;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? PlaybackDuration;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? PlaybackQueueCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? PlaybackQueueIndex;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? PlaybackRate;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Title;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl AssetUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOptionGroup[] AvailableLanguageOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CollectionIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOption[] CurrentLanguageOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExternalContentIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExternalUserProfileIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsLiveStream { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoMediaType? MediaType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? PlaybackProgress { get; set; }</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfo -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.12"</span> <span class='added '>"10.13"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.4.0"</span> <span class='added '>"3.99.3"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string PhotosUILibrary = "/System/Library/Frameworks/Photos.framework/PhotosUI";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNFloat (IntPtr handle, string symbol, nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNInt (IntPtr handle, string symbol, nint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNUInt (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfAnnotation --> <div>
<h3>Type Changed: PdfKit.PdfAnnotation</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, Foundation.NSString annotationType, Foundation.NSDictionary properties);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, PdfAnnotationKey annotationType, Foundation.NSDictionary properties);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual PdfPage Page { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual string Type { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAction Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSTextAlignment Alignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsToggleToOff { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary AnnotationKeyValues { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PdfAnnotationKey AnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetCellState ButtonWidgetState { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ButtonWidgetStateString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Choices { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Comb { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination Destination { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle EndLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint EndPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FieldName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSFont Font { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor FontColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Highlighted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfTextAnnotationIconType IconType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPasswordField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ListChoice { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfMarkupType MarkupType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaximumLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Multiline { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Open { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSBezierPath[] Paths { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSValue[] QuadrilateralPoints { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RadiosInUnison { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle StartLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint StartPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Values { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType WidgetControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetDefaultStringValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetFieldType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetStringValue { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddBezierPath (AppKit.NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfLineStyle GetLineStyle (string fromName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetName (PdfLineStyle style);</span>
	<span class='added added-method ' data-is-non-breaking="">public T GetValue&lt;T&gt; (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveBezierPath (AppKit.NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void RemoveValue (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveValue (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (CoreGraphics.CGRect rect, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (CoreGraphics.CGRect rect, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (bool boolean, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (bool boolean, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (string str, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue&lt;T&gt; (T value, PdfAnnotationKey key);</span>
</pre>
</div>

</div> <!-- end type PdfAnnotation -->
<!-- start type PdfAnnotationButtonWidget --> <div>
<h3>Type Changed: PdfKit.PdfAnnotationButtonWidget</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual bool AllowsToggleToOff { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type PdfAnnotationButtonWidget -->
<!-- start type PdfAnnotationTextWidget --> <div>
<h3>Type Changed: PdfKit.PdfAnnotationTextWidget</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedStringValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsMultiline { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfAnnotationTextWidget -->
<!-- start type PdfBorder --> <div>
<h3>Type Changed: PdfKit.PdfBorder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakBorderKeyValues { get; }</span>
</pre>
</div>

</div> <!-- end type PdfBorder -->
<!-- start type PdfDestination --> <div>
<h3>Type Changed: PdfKit.PdfDestination</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Zoom { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfDestination -->
<!-- start type PdfDocument --> <div>
<h3>Type Changed: PdfKit.PdfDocument</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCommenting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsContentAccessibility { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentAssembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsFormFieldEntry { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidFindMatchNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUnlockNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFDocument Document { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate GetClassForAnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Type PageType { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidBeginDocumentFind;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUnlock;</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Find (string, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection[] Find (string text, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Find (string, PdfSelection, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection Find (string text, PdfSelection selection, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string, NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string text, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string [], NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string[] text, nint options);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public PdfSelection[] Find (string text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfSelection Find (string text, PdfSelection selection, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FindAsync (string text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FindAsync (string[] text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfDocumentAttributes GetDocumentAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSPrintOperation GetPrintOperation (AppKit.NSPrintInfo printInfo, PdfPrintScalingMode scaleMode, bool doRotate);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetDocumentAttributes (PdfDocumentAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (Foundation.NSUrl url, PdfDocumentWriteOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (string path, PdfDocumentWriteOptions options);</span>
</pre>
</div>

</div> <!-- end type PdfDocument -->
<!-- start type PdfDocumentDelegate --> <div>
<h3>Type Changed: PdfKit.PdfDocumentDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBeginDocumentFind (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnlock (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForAnnotationType (string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForPage ();</span>
</pre>
</div>

</div> <!-- end type PdfDocumentDelegate -->
<!-- start type PdfDocumentDelegate_Extensions --> <div>
<h3>Type Changed: PdfKit.PdfDocumentDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidBeginDocumentFind (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnlock (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForAnnotationType (IPdfDocumentDelegate This, string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForPage (IPdfDocumentDelegate This);</span>
</pre>
</div>

</div> <!-- end type PdfDocumentDelegate_Extensions -->
<!-- start type PdfPage --> <div>
<h3>Type Changed: PdfKit.PdfPage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFPage Page { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSImage GetThumbnail (CoreGraphics.CGSize size, PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform GetTransform (PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TransformContext (CoreGraphics.CGContext context, PdfDisplayBox box);</span>
</pre>
</div>

</div> <!-- end type PdfPage -->
<!-- start type PdfSelection --> <div>
<h3>Type Changed: PdfKit.PdfSelection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExtendSelectionForLineBoundaries ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetNumberOfTextRanges (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetRange (uint index, PdfPage page);</span>
</pre>
</div>

</div> <!-- end type PdfSelection -->
<!-- start type PdfThumbnailView --> <div>
<h3>Type Changed: PdfKit.PdfThumbnailView</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfThumbnailView (CoreGraphics.CGRect frame);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DocumentEditedNotification { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type PdfThumbnailView -->
<!-- start type PdfView --> <div>
<h3>Type Changed: PdfKit.PdfView</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfView (CoreGraphics.CGRect frame);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSAnimationDelegate</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AcceptsDraggedFiles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDisplayDirection DisplayDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysRtl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfInterpolationQuality InterpolationQuality { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaxScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSEdgeInsets PageBreakMargins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PrintPermissionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScaleFactorForSizeToFit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VisiblePagesChangedNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidEnd (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidReachProgressMark (AppKit.NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidStop (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AnimationShouldStart (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float ComputeAnimationCurve (AppKit.NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPage (PdfPage page, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPagePost (PdfPage page, CoreGraphics.CGContext context);</span>
</pre>
</div>
<!-- start type PdfView.Notifications --> <div>
<h3>Type Changed: PdfKit.PdfView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type PdfView.Notifications -->

</div> <!-- end type PdfView -->
<div> <!-- start type ClassForAnnotationTypeDelegate -->
<h3>New Type PdfKit.ClassForAnnotationTypeDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ClassForAnnotationTypeDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string annotationType, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class Invoke (string annotationType);</span>
}
</pre>
</div> <!-- end type ClassForAnnotationTypeDelegate -->
<div> <!-- start type PdfAnnotationHighlightingMode -->
<h3>New Type PdfKit.PdfAnnotationHighlightingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationHighlightingMode {
	<span class='added added-field ' data-is-non-breaking="">Invert = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Outline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Push = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingMode -->
<div> <!-- start type PdfAnnotationHighlightingModeExtensions -->
<h3>New Type PdfKit.PdfAnnotationHighlightingModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationHighlightingModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationHighlightingMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationHighlightingMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingModeExtensions -->
<div> <!-- start type PdfAnnotationKey -->
<h3>New Type PdfKit.PdfAnnotationKey</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationKey {
	<span class='added added-field ' data-is-non-breaking="">Action = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">AdditionalActions = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceDictionary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceState = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Border = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BorderStyle = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Color = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Contents = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Date = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DefaultAppearance = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Destination = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Flags = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HighlightingMode = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">IconName = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">Inklist = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InteriorColor = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">LineEndingStyles = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">LinePoints = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Name = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Page = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Parent = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">QuadPoints = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Quadding = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Rect = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtype = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">TextLabel = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetAppearanceDictionary = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBackgroundColor = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBorderColor = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetCaption = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDefaultValue = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDownCaption = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldFlags = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldType = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetMaxLen = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetOptions = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRolloverCaption = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRotation = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetTextLabelUI = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetValue = 41,</span>
}
</pre>
</div> <!-- end type PdfAnnotationKey -->
<div> <!-- start type PdfAnnotationKeyExtensions -->
<h3>New Type PdfKit.PdfAnnotationKeyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationKeyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationKey self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationKey GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationKeyExtensions -->
<div> <!-- start type PdfAnnotationLineEndingStyle -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationLineEndingStyle {
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedArrow = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OpenArrow = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 1,</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyle -->
<div> <!-- start type PdfAnnotationLineEndingStyleExtensions -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationLineEndingStyleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationLineEndingStyle self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationLineEndingStyle GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyleExtensions -->
<div> <!-- start type PdfAnnotationSubtype -->
<h3>New Type PdfKit.PdfAnnotationSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationSubtype {
	<span class='added added-field ' data-is-non-breaking="">Circle = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FreeText = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Highlight = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Ink = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Line = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Stamp = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikeOut = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Underline = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Widget = 12,</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtype -->
<div> <!-- start type PdfAnnotationSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtypeExtensions -->
<div> <!-- start type PdfAnnotationTextIconType -->
<h3>New Type PdfKit.PdfAnnotationTextIconType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationTextIconType {
	<span class='added added-field ' data-is-non-breaking="">Comment = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Help = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Key = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NewParagraph = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Note = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 5,</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconType -->
<div> <!-- start type PdfAnnotationTextIconTypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationTextIconTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationTextIconTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationTextIconType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationTextIconType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconTypeExtensions -->
<div> <!-- start type PdfAnnotationWidgetSubtype -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationWidgetSubtype {
	<span class='added added-field ' data-is-non-breaking="">Button = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Choice = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Signature = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtype -->
<div> <!-- start type PdfAnnotationWidgetSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationWidgetSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationWidgetSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationWidgetSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtypeExtensions -->
<div> <!-- start type PdfAppearanceCharacteristics -->
<h3>New Type PdfKit.PdfAppearanceCharacteristics</h3>
<pre class='added' data-is-non-breaking="">
public class PdfAppearanceCharacteristics : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAppearanceCharacteristics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BorderColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType ControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DownCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RolloverCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakAppearanceCharacteristicsKeyValues { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristics -->
<div> <!-- start type PdfAppearanceCharacteristicsKeys -->
<h3>New Type PdfKit.PdfAppearanceCharacteristicsKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAppearanceCharacteristicsKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BackgroundColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BorderColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RolloverCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RotationKey { get; }</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristicsKeys -->
<div> <!-- start type PdfBorderKeys -->
<h3>New Type PdfKit.PdfBorderKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfBorderKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DashPatternKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LineWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StyleKey { get; }</span>
}
</pre>
</div> <!-- end type PdfBorderKeys -->
<div> <!-- start type PdfDisplayDirection -->
<h3>New Type PdfKit.PdfDisplayDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDisplayDirection {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type PdfDisplayDirection -->
<div> <!-- start type PdfDocumentAttributes -->
<h3>New Type PdfKit.PdfDocumentAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentAttributes : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate CreationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Creator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Keywords { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate ModificationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Producer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subject { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Title { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentAttributes -->
<div> <!-- start type PdfDocumentWriteOptions -->
<h3>New Type PdfKit.PdfDocumentWriteOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentWriteOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string OwnerPassword { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UserPassword { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentWriteOptions -->
<div> <!-- start type PdfInterpolationQuality -->
<h3>New Type PdfKit.PdfInterpolationQuality</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfInterpolationQuality {
	<span class='added added-field ' data-is-non-breaking="">High = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PdfInterpolationQuality -->
<div> <!-- start type PdfWidgetCellState -->
<h3>New Type PdfKit.PdfWidgetCellState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfWidgetCellState {
	<span class='added added-field ' data-is-non-breaking="">Mixed = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">On = 1,</span>
}
</pre>
</div> <!-- end type PdfWidgetCellState -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAnimated = 214,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLongExposures = 215,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage DisplaySizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHContentEditingInput -->
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, PHLivePhotoEditingOption options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, PHLivePhotoEditingOption options);</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type IPHPhotoLibraryChangeObserver -->
<h3>New Type Photos.IPHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHPhotoLibraryChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type IPHPhotoLibraryChangeObserver -->
<div> <!-- start type PHAsset -->
<h3>New Type Photos.PHAsset</h3>
<pre class='added' data-is-non-breaking="">
public class PHAsset : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BurstIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LocalIdentifierNotFound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RepresentsBurst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType SourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SyncFailureHidden { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHAsset -->
<div> <!-- start type PHAssetCollection -->
<h3>New Type Photos.PHAssetCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollection : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetCollection ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation ApproximateLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionType AssetCollectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EstimatedAssetCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);</span>
}
</pre>
</div> <!-- end type PHAssetCollection -->
<div> <!-- start type PHAssetImageProgressHandler -->
<h3>New Type Photos.PHAssetImageProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetImageProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetImageProgressHandler -->
<div> <!-- start type PHAssetPlaybackStyle -->
<h3>New Type Photos.PHAssetPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageAnimated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LivePhoto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoLooping = 5,</span>
}
</pre>
</div> <!-- end type PHAssetPlaybackStyle -->
<div> <!-- start type PHAuthorizationStatus -->
<h3>New Type Photos.PHAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type PHAuthorizationStatus -->
<div> <!-- start type PHChange -->
<h3>New Type Photos.PHChange</h3>
<pre class='added' data-is-non-breaking="">
public class PHChange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);</span>
}
</pre>
</div> <!-- end type PHChange -->
<div> <!-- start type PHChangeDetailEnumerator -->
<h3>New Type Photos.PHChangeDetailEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChangeDetailEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (uint fromIndex, uint toIndex);</span>
}
</pre>
</div> <!-- end type PHChangeDetailEnumerator -->
<div> <!-- start type PHCloudIdentifier -->
<h3>New Type Photos.PHCloudIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public class PHCloudIdentifier : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (string stringValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHCloudIdentifier NotFoundIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHCloudIdentifier -->
<div> <!-- start type PHCollection -->
<h3>New Type Photos.PHCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollection : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainAssets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainCollections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollection -->
<div> <!-- start type PHCollectionList -->
<h3>New Type Photos.PHCollectionList</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionList : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCollectionList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListSubtype CollectionListSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListType CollectionListType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollectionList -->
<div> <!-- start type PHFetchOptions -->
<h3>New Type Photos.PHFetchOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FetchLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAllBurstAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType IncludeAssetSourceTypes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeHiddenAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsIncrementalChangeDetails { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHFetchOptions -->
<div> <!-- start type PHFetchResult -->
<h3>New Type Photos.PHFetchResult</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResult : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LastObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject firstObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSIndexSet idx, Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAt (nint index);</span>
}
</pre>
</div> <!-- end type PHFetchResult -->
<div> <!-- start type PHFetchResultChangeDetails -->
<h3>New Type Photos.PHFetchResultChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResultChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet ChangedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] ChangedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasIncrementalChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasMoves { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet InsertedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] InsertedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet RemovedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] RemovedObjects { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);</span>
}
</pre>
</div> <!-- end type PHFetchResultChangeDetails -->
<div> <!-- start type PHFetchResultEnumerator -->
<h3>New Type Photos.PHFetchResultEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject element, uint elementIndex, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSObject element, uint elementIndex, bool stop);</span>
}
</pre>
</div> <!-- end type PHFetchResultEnumerator -->
<div> <!-- start type PHImageDataHandler -->
<h3>New Type Photos.PHImageDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageDataHandler -->
<div> <!-- start type PHImageKeys -->
<h3>New Type Photos.PHImageKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PHImageKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Cancelled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsDegraded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloud { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultRequestID { get; }</span>
}
</pre>
</div> <!-- end type PHImageKeys -->
<div> <!-- start type PHImageManager -->
<h3>New Type Photos.PHImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHImageManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize MaximumSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelImageRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageForAsset (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);</span>
}
</pre>
</div> <!-- end type PHImageManager -->
<div> <!-- start type PHImageRequestOptions -->
<h3>New Type Photos.PHImageRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect NormalizedCropRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Synchronous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHImageRequestOptions -->
<div> <!-- start type PHImageRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHImageRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Opportunistic = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsDeliveryMode -->
<div> <!-- start type PHImageRequestOptionsResizeMode -->
<h3>New Type Photos.PHImageRequestOptionsResizeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	<span class='added added-field ' data-is-non-breaking="">Exact = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsResizeMode -->
<div> <!-- start type PHImageRequestOptionsVersion -->
<h3>New Type Photos.PHImageRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unadjusted = 1,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsVersion -->
<div> <!-- start type PHImageResultHandler -->
<h3>New Type Photos.PHImageResultHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageResultHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AppKit.NSImage result, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AppKit.NSImage result, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageResultHandler -->
<div> <!-- start type PHLivePhotoEditingOption -->
<h3>New Type Photos.PHLivePhotoEditingOption</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingOption : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldRenderAtPlaybackTime { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingOption -->
<div> <!-- start type PHObject -->
<h3>New Type Photos.PHObject</h3>
<pre class='added' data-is-non-breaking="">
public class PHObject : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHObject -->
<div> <!-- start type PHObjectChangeDetails -->
<h3>New Type Photos.PHObjectChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AssetContentChanged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ObjectWasDeleted { get; }</span>
}
</pre>
</div> <!-- end type PHObjectChangeDetails -->
<div> <!-- start type PHPhotoLibrary -->
<h3>New Type Photos.PHPhotoLibrary</h3>
<pre class='added' data-is-non-breaking="">
public class PHPhotoLibrary : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHPhotoLibrary SharedPhotoLibrary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformChanges (System.Action changeHandler, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PerformChangesAndWait (System.Action changeHandler, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestAuthorization (System.Action&lt;PHAuthorizationStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;PHAuthorizationStatus&gt; RequestAuthorizationAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary -->
<div> <!-- start type PHPhotoLibraryChangeObserver -->
<h3>New Type Photos.PHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PHPhotoLibraryChangeObserver : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHPhotoLibraryChangeObserver, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type PHPhotoLibraryChangeObserver -->
<div> <!-- start type PHPhotoLibrary_CloudIdentifiers -->
<h3>New Type Photos.PHPhotoLibrary_CloudIdentifiers</h3>
<pre class='added' data-is-non-breaking="">
public static class PHPhotoLibrary_CloudIdentifiers {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCloudIdentifier[] GetCloudIdentifiers (PHPhotoLibrary This, string[] localIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetLocalIdentifiers (PHPhotoLibrary This, PHCloudIdentifier[] cloudIdentifiers);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary_CloudIdentifiers -->
<div> <!-- start type PHProject -->
<h3>New Type Photos.PHProject</h3>
<pre class='added' data-is-non-breaking="">
public class PHProject : Photos.PHAssetCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProject ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; }</span>
}
</pre>
</div> <!-- end type PHProject -->
<div> <!-- start type PHProjectChangeRequest -->
<h3>New Type Photos.PHProjectChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest (PHProject project);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetKeyAsset (PHAsset keyAsset);</span>
}
</pre>
</div> <!-- end type PHProjectChangeRequest -->
<div> <!-- start type PHProjectCreationSource -->
<h3>New Type Photos.PHProjectCreationSource</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectCreationSource {
	<span class='added added-field ' data-is-non-breaking="">Album = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Memory = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Project = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectBook = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCalendar = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCard = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectExtension = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectPrintOrder = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectSlideshow = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserSelection = 1,</span>
}
</pre>
</div> <!-- end type PHProjectCreationSource -->
<div> <!-- start type PHProjectSectionType -->
<h3>New Type Photos.PHProjectSectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectSectionType {
	<span class='added added-field ' data-is-non-breaking="">Auxiliary = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type PHProjectSectionType -->
<div> <!-- start type PHProjectTextElementType -->
<h3>New Type Photos.PHProjectTextElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectTextElementType {
	<span class='added added-field ' data-is-non-breaking="">Body = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title = 1,</span>
}
</pre>
</div> <!-- end type PHProjectTextElementType -->

</div> <!-- end namespace Photos -->
<!-- start namespace QTKit --> <div> 
<h2>Namespace QTKit</h2>
<!-- start type QTCaptureLayer --> <div>
<h3>Type Changed: QTKit.QTCaptureLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTCaptureLayer -->
<!-- start type QTMovieLayer --> <div>
<h3>Type Changed: QTKit.QTMovieLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTMovieLayer -->

</div> <!-- end namespace QTKit -->
<!-- start namespace QuartzComposer --> <div> 
<h2>Namespace QuartzComposer</h2>
<!-- start type QCCompositionLayer --> <div>
<h3>Type Changed: QuartzComposer.QCCompositionLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QCCompositionLayer -->

</div> <!-- end namespace QuartzComposer -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariApplication --> <div>
<h3>Type Changed: SafariServices.SFSafariApplication</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetHostApplication (System.Action&lt;AppKit.NSRunningApplication&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AppKit.NSRunningApplication&gt; GetHostApplicationAsync ();</span>
</pre>
</div>

</div> <!-- end type SFSafariApplication -->
<!-- start type SFSafariToolbarItem --> <div>
<h3>Type Changed: SafariServices.SFSafariToolbarItem</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLabel (string label);</span>
</pre>
</div>

</div> <!-- end type SFSafariToolbarItem -->
<div> <!-- start type SFSafariServicesVersion -->
<h3>New Type SafariServices.SFSafariServicesVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SFSafariServicesVersion {
	<span class='added added-field ' data-is-non-breaking="">V10_0 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">V10_1 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">V11_0 = 2,</span>
}
</pre>
</div> <!-- end type SFSafariServicesVersion -->

</div> <!-- end namespace SafariServices -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLineBreakMode LineBreakMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLines { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredMaxLayoutWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKLabelNode FromText (Foundation.NSAttributedString attributedText);</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->
<div> <!-- start type SKRenderer -->
<h3>New Type SpriteKit.SKRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class SKRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IgnoresSiblingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldCullNonVisibleNodes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsDrawCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsNodeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsPhysics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsQuadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKRenderer FromDevice (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLRenderCommandEncoder renderCommandEncoder, Metal.MTLRenderPassDescriptor renderPassDescriptor, Metal.IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double currentTime);</span>
}
</pre>
</div> <!-- end type SKRenderer -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, AppKit.INSTouchBarProvider, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKErrorCode --> <div>
<h3>Type Changed: WebKit.WKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreCompileFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreLookUpFailed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreRemoveFailed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreVersionMismatch = 9,</span>
</pre>
</div>

</div> <!-- end type WKErrorCode -->
<!-- start type WKFrameInfo --> <div>
<h3>Type Changed: WebKit.WKFrameInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKWebView WebView { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type WKFrameInfo -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddContentRuleList (WKContentRuleList contentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllContentRuleLists ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (WKContentRuleList contentRuleList);</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebView --> <div>
<h3>Type Changed: WebKit.WKWebView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool HandlesUrlScheme (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot (WKSnapshotConfiguration snapshotConfiguration, System.Action&lt;AppKit.NSImage,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AppKit.NSImage&gt; TakeSnapshotAsync (WKSnapshotConfiguration snapshotConfiguration);</span>
</pre>
</div>

</div> <!-- end type WKWebView -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWKUrlSchemeHandler GetUrlSchemeHandler (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetUrlSchemeHandler (IWKUrlSchemeHandler urlSchemeHandler, string urlScheme);</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKHttpCookieStore HttpCookieStore { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WebView --> <div>
<h3>Type Changed: WebKit.WebView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSelectedDomRange (DomRange range, AppKit.NSSelectionAffinity selectionAffinity);</span>
</pre>
</div>

</div> <!-- end type WebView -->
<div> <!-- start type IWKHttpCookieStoreObserver -->
<h3>New Type WebKit.IWKHttpCookieStoreObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKHttpCookieStoreObserver : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IWKHttpCookieStoreObserver -->
<div> <!-- start type IWKUrlSchemeHandler -->
<h3>New Type WebKit.IWKUrlSchemeHandler</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeHandler : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeHandler -->
<div> <!-- start type IWKUrlSchemeTask -->
<h3>New Type WebKit.IWKUrlSchemeTask</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeTask : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrlRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFailWithError (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveResponse (Foundation.NSUrlResponse response);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeTask -->
<div> <!-- start type WKContentRuleList -->
<h3>New Type WebKit.WKContentRuleList</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleList : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type WKContentRuleList -->
<div> <!-- start type WKContentRuleListStore -->
<h3>New Type WebKit.WKContentRuleListStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleListStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WKContentRuleListStore DefaultStore { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompileContentRuleList (string identifier, string encodedContentRuleList, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; CompileContentRuleListAsync (string identifier, string encodedContentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static WKContentRuleListStore FromUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAvailableContentRuleListIdentifiers (System.Action&lt;System.String[]&gt; callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; GetAvailableContentRuleListIdentifiersAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LookUpContentRuleList (string identifier, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; LookUpContentRuleListAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveContentRuleListAsync (string identifier);</span>
}
</pre>
</div> <!-- end type WKContentRuleListStore -->
<div> <!-- start type WKHttpCookieStore -->
<h3>New Type WebKit.WKHttpCookieStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKHttpCookieStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteCookieAsync (Foundation.NSHttpCookie cookie);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAllCookies (System.Action&lt;Foundation.NSHttpCookie[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSHttpCookie[]&gt; GetAllCookiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetCookieAsync (Foundation.NSHttpCookie cookie);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStore -->
<div> <!-- start type WKHttpCookieStoreObserver_Extensions -->
<h3>New Type WebKit.WKHttpCookieStoreObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKHttpCookieStoreObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CookiesDidChangeInCookieStore (IWKHttpCookieStoreObserver This, WKHttpCookieStore cookieStore);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStoreObserver_Extensions -->
<div> <!-- start type WKSnapshotConfiguration -->
<h3>New Type WebKit.WKSnapshotConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class WKSnapshotConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SnapshotWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type WKSnapshotConfiguration -->

</div> <!-- end namespace WebKit -->
<!-- start namespace CoreML --> <div> 
<h2>New Namespace CoreML</h2>

<div> <!-- start type IMLFeatureProvider -->
<h3>New Type CoreML.IMLFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLFeatureProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type IMLFeatureProvider -->
<div> <!-- start type MLDictionaryConstraint -->
<h3>New Type CoreML.MLDictionaryConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType KeyType { get; }</span>
}
</pre>
</div> <!-- end type MLDictionaryConstraint -->
<div> <!-- start type MLDictionaryFeatureProvider -->
<h3>New Type CoreML.MLDictionaryFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryFeatureProvider : Foundation.NSObject, IMLFeatureProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; dictionary, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureValue&gt; Dictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLFeatureValue Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type MLDictionaryFeatureProvider -->
<div> <!-- start type MLFeatureDescription -->
<h3>New Type CoreML.MLFeatureDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLDictionaryConstraint DictionaryConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLImageConstraint ImageConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayConstraint MultiArrayConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAllowed (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureDescription -->
<div> <!-- start type MLFeatureType -->
<h3>New Type CoreML.MLFeatureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLFeatureType {
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Int64 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiArray = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 3,</span>
}
</pre>
</div> <!-- end type MLFeatureType -->
<div> <!-- start type MLFeatureValue -->
<h3>New Type CoreML.MLFeatureValue</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; DictionaryValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer ImageBufferValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Int64Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArray MultiArrayValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Undefined { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue CreateUndefined (MLFeatureType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDictionary (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; value, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDouble (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromInt64 (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromMultiArray (MLMultiArray value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromPixelBuffer (CoreVideo.CVPixelBuffer value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromString (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureValue -->
<div> <!-- start type MLImageConstraint -->
<h3>New Type CoreML.MLImageConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLImageConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelFormatType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsHigh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsWide { get; }</span>
}
</pre>
</div> <!-- end type MLImageConstraint -->
<div> <!-- start type MLModel -->
<h3>New Type CoreML.MLModel</h3>
<pre class='added' data-is-non-breaking="">
public class MLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLModelDescription ModelDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl CompileModel (Foundation.NSUrl modelUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLModel FromUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, MLPredictionOptions options, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLModel -->
<div> <!-- start type MLModelDescription -->
<h3>New Type CoreML.MLModelDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelDescription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; InputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLModelMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; OutputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedFeatureName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedProbabilitiesName { get; }</span>
}
</pre>
</div> <!-- end type MLModelDescription -->
<div> <!-- start type MLModelError -->
<h3>New Type CoreML.MLModelError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLModelError {
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">IO = 3,</span>
}
</pre>
</div> <!-- end type MLModelError -->
<div> <!-- start type MLModelErrorExtensions -->
<h3>New Type CoreML.MLModelErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLModelErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MLModelError self);</span>
}
</pre>
</div> <!-- end type MLModelErrorExtensions -->
<div> <!-- start type MLModelMetadata -->
<h3>New Type CoreML.MLModelMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelMetadata : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CreatorDefined { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string License { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string VersionString { get; }</span>
}
</pre>
</div> <!-- end type MLModelMetadata -->
<div> <!-- start type MLMultiArray -->
<h3>New Type CoreML.MLMultiArray</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSNumber[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr DataPointer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Strides { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, nint idx);</span>
}
</pre>
</div> <!-- end type MLMultiArray -->
<div> <!-- start type MLMultiArrayConstraint -->
<h3>New Type CoreML.MLMultiArrayConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArrayConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
}
</pre>
</div> <!-- end type MLMultiArrayConstraint -->
<div> <!-- start type MLMultiArrayDataType -->
<h3>New Type CoreML.MLMultiArrayDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLMultiArrayDataType {
	<span class='added added-field ' data-is-non-breaking="">Double = 65600,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 65568,</span>
	<span class='added added-field ' data-is-non-breaking="">Int32 = 131104,</span>
}
</pre>
</div> <!-- end type MLMultiArrayDataType -->
<div> <!-- start type MLPredictionOptions -->
<h3>New Type CoreML.MLPredictionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class MLPredictionOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLPredictionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
}
</pre>
</div> <!-- end type MLPredictionOptions -->
</div> <!-- end namespace CoreML -->

<!-- start namespace PhotosUI --> <div> 
<h2>New Namespace PhotosUI</h2>

<div> <!-- start type IPHContentEditingController -->
<h3>New Type PhotosUI.IPHContentEditingController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHContentEditingController : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldShowCancelConfirmation { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleAdjustmentData (Photos.PHAdjustmentData adjustmentData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelContentEditing ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishContentEditing (System.Action&lt;Photos.PHContentEditingOutput&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartContentEditing (Photos.PHContentEditingInput contentEditingInput, AppKit.NSImage placeholderImage);</span>
}
</pre>
</div> <!-- end type IPHContentEditingController -->
<div> <!-- start type IPHProjectExtensionController -->
<h3>New Type PhotosUI.IPHProjectExtensionController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHProjectExtensionController : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginProject (PHProjectExtensionContext extensionContext, PHProjectInfo projectInfo, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishProject (System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeProject (PHProjectExtensionContext extensionContext, System.Action&lt;Foundation.NSError&gt; completion);</span>
}
</pre>
</div> <!-- end type IPHProjectExtensionController -->
<div> <!-- start type PHProjectAssetElement -->
<h3>New Type PhotosUI.PHProjectAssetElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectAssetElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Annotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHCloudIdentifier CloudAssetIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect CropRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectRegionOfInterest[] RegionsOfInterest { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectAssetElement -->
<div> <!-- start type PHProjectElement -->
<h3>New Type PhotosUI.PHProjectElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectElement : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Placement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectElement -->
<div> <!-- start type PHProjectExtensionContext -->
<h3>New Type PhotosUI.PHProjectExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectExtensionContext : Foundation.NSExtensionContext, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectExtensionContext (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHPhotoLibrary PhotoLibrary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProject Project { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionContext -->
<div> <!-- start type PHProjectExtensionController_Extensions -->
<h3>New Type PhotosUI.PHProjectExtensionController_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectExtensionController_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHProjectTypeDescription[] GetSupportedProjectTypes (IPHProjectExtensionController This);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionController_Extensions -->
<div> <!-- start type PHProjectInfo -->
<h3>New Type PhotosUI.PHProjectInfo</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectCreationSource CreationSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSection[] Sections { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectInfo -->
<div> <!-- start type PHProjectJournalEntryElement -->
<h3>New Type PhotosUI.PHProjectJournalEntryElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectJournalEntryElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectAssetElement AssetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Date { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElement TextElement { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectJournalEntryElement -->
<div> <!-- start type PHProjectRegionOfInterest -->
<h3>New Type PhotosUI.PHProjectRegionOfInterest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectRegionOfInterest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectRegionOfInterest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectRegionOfInterest -->
<div> <!-- start type PHProjectSection -->
<h3>New Type PhotosUI.PHProjectSection</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSection : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSection (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionContent[] SectionContents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectSectionType SectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSection -->
<div> <!-- start type PHProjectSectionContent -->
<h3>New Type PhotosUI.PHProjectSectionContent</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSectionContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSectionContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double AspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHCloudIdentifier[] CloudAssetIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectElement[] Elements { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSectionContent -->
<div> <!-- start type PHProjectTextElement -->
<h3>New Type PhotosUI.PHProjectTextElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTextElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectTextElementType TextElementType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTextElement -->
<div> <!-- start type PHProjectType -->
<h3>New Type PhotosUI.PHProjectType</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectType {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Undefined { get; }</span>
}
</pre>
</div> <!-- end type PHProjectType -->
<div> <!-- start type PHProjectTypeDescription -->
<h3>New Type PhotosUI.PHProjectTypeDescription</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTypeDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image, PHProjectTypeDescription[] subtypeDescriptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTypeDescription[] SubtypeDescriptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTypeDescription -->
</div> <!-- end namespace PhotosUI -->

<!-- start namespace Vision --> <div> 
<h2>New Namespace Vision</h2>

<div> <!-- start type IVNFaceObservationAccepting -->
<h3>New Type Vision.IVNFaceObservationAccepting</h3>
<pre class='added' data-is-non-breaking="">
public interface IVNFaceObservationAccepting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type IVNFaceObservationAccepting -->
<div> <!-- start type VNBarcodeObservation -->
<h3>New Type Vision.VNBarcodeObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNBarcodeObservation : Vision.VNRectangleObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor BarcodeDescriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PayloadStringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology Symbology { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakSymbology { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNBarcodeObservation -->
<div> <!-- start type VNBarcodeSymbology -->
<h3>New Type Vision.VNBarcodeSymbology</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNBarcodeSymbology {
	<span class='added added-field ' data-is-non-breaking="">Aztec = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Code128 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39Checksum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAscii = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAsciiChecksum = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93i = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DataMatrix = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean13 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5Checksum = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Itf14 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Pdf417 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">QR = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Upce = 16,</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbology -->
<div> <!-- start type VNBarcodeSymbologyExtensions -->
<h3>New Type Vision.VNBarcodeSymbologyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNBarcodeSymbologyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VNBarcodeSymbology self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (VNBarcodeSymbology[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology[] GetValues (Foundation.NSString[] constants);</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbologyExtensions -->
<div> <!-- start type VNClassificationObservation -->
<h3>New Type Vision.VNClassificationObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNClassificationObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNClassificationObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type VNClassificationObservation -->
<div> <!-- start type VNCoreMLFeatureValueObservation -->
<h3>New Type Vision.VNCoreMLFeatureValueObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLFeatureValueObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLFeatureValueObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreML.MLFeatureValue FeatureValue { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLFeatureValueObservation -->
<div> <!-- start type VNCoreMLModel -->
<h3>New Type Vision.VNCoreMLModel</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNCoreMLModel FromMLModel (CoreML.MLModel model, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNCoreMLModel -->
<div> <!-- start type VNCoreMLRequest -->
<h3>New Type Vision.VNCoreMLRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNImageCropAndScaleOption ImageCropAndScaleOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNCoreMLModel Model { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLRequest -->
<div> <!-- start type VNDetectBarcodesRequest -->
<h3>New Type Vision.VNDetectBarcodesRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNDetectBarcodesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectBarcodesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static VNBarcodeSymbology[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology[] Symbologies { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected static Foundation.NSString[] WeakSupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString[] WeakSymbologies { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectBarcodesRequest -->
<div> <!-- start type VNDetectFaceLandmarksRequest -->
<h3>New Type Vision.VNDetectFaceLandmarksRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceLandmarksRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVNFaceObservationAccepting {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceLandmarksRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceLandmarksRequest -->
<div> <!-- start type VNDetectFaceRectanglesRequest -->
<h3>New Type Vision.VNDetectFaceRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceRectanglesRequest -->
<div> <!-- start type VNDetectHorizonRequest -->
<h3>New Type Vision.VNDetectHorizonRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectHorizonRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectHorizonRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectHorizonRequest -->
<div> <!-- start type VNDetectRectanglesRequest -->
<h3>New Type Vision.VNDetectRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumObservations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumConfidence { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float QuadratureTolerance { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectRectanglesRequest -->
<div> <!-- start type VNDetectTextRectanglesRequest -->
<h3>New Type Vision.VNDetectTextRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectTextRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectTextRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportCharacterBoxes { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectTextRectanglesRequest -->
<div> <!-- start type VNDetectedObjectObservation -->
<h3>New Type Vision.VNDetectedObjectObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectedObjectObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectedObjectObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BoundingBox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNDetectedObjectObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNDetectedObjectObservation -->
<div> <!-- start type VNErrorCode -->
<h3>New Type Vision.VNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">IOError = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidImage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModel = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOperation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOption = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingOption = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationFailed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBoundsError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfMemory = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestCancelled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownError = 11,</span>
}
</pre>
</div> <!-- end type VNErrorCode -->
<div> <!-- start type VNErrorCodeExtensions -->
<h3>New Type Vision.VNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VNErrorCode self);</span>
}
</pre>
</div> <!-- end type VNErrorCodeExtensions -->
<div> <!-- start type VNFaceLandmarkRegion -->
<h3>New Type Vision.VNFaceLandmarkRegion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarkRegion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PointCount { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion -->
<div> <!-- start type VNFaceLandmarkRegion2D -->
<h3>New Type Vision.VNFaceLandmarkRegion2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarkRegion2D : Vision.VNFaceLandmarkRegion, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] NormalizedPoints { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] GetPointsInImage (CoreGraphics.CGSize imageSize);</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion2D -->
<div> <!-- start type VNFaceLandmarks -->
<h3>New Type Vision.VNFaceLandmarks</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarks : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks -->
<div> <!-- start type VNFaceLandmarks2D -->
<h3>New Type Vision.VNFaceLandmarks2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarks2D : Vision.VNFaceLandmarks, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D AllPoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D FaceContour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D InnerLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftPupil { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D MedianLine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D Nose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D NoseCrest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D OuterLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightPupil { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks2D -->
<div> <!-- start type VNFaceObservation -->
<h3>New Type Vision.VNFaceObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNFaceObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarks2D Landmarks { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNFaceObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNFaceObservation -->
<div> <!-- start type VNHomographicImageRegistrationRequest -->
<h3>New Type Vision.VNHomographicImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNHomographicImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNHomographicImageRegistrationRequest -->
<div> <!-- start type VNHorizonObservation -->
<h3>New Type Vision.VNHorizonObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNHorizonObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHorizonObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Angle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
}
</pre>
</div> <!-- end type VNHorizonObservation -->
<div> <!-- start type VNImageAlignmentObservation -->
<h3>New Type Vision.VNImageAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageAlignmentObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageAlignmentObservation -->
<div> <!-- start type VNImageBasedRequest -->
<h3>New Type Vision.VNImageBasedRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageBasedRequest : Vision.VNRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageBasedRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect RegionOfInterest { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageBasedRequest -->
<div> <!-- start type VNImageCropAndScaleOption -->
<h3>New Type Vision.VNImageCropAndScaleOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNImageCropAndScaleOption {
	<span class='added added-field ' data-is-non-breaking="">CenterCrop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFill = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFit = 1,</span>
}
</pre>
</div> <!-- end type VNImageCropAndScaleOption -->
<div> <!-- start type VNImageHomographicAlignmentObservation -->
<h3>New Type Vision.VNImageHomographicAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageHomographicAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageHomographicAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 WarpTransform { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageHomographicAlignmentObservation -->
<div> <!-- start type VNImageOptions -->
<h3>New Type Vision.VNImageOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreImage.CIContext CIContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary WeakProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageOptions -->
<div> <!-- start type VNImageRegistrationRequest -->
<h3>New Type Vision.VNImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageRegistrationRequest : Vision.VNTargetedImageRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageRegistrationRequest -->
<div> <!-- start type VNImageRequestHandler -->
<h3>New Type Vision.VNImageRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNImageRequestHandler -->
<div> <!-- start type VNImageTranslationAlignmentObservation -->
<h3>New Type Vision.VNImageTranslationAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageTranslationAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageTranslationAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AlignmentTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageTranslationAlignmentObservation -->
<div> <!-- start type VNObservation -->
<h3>New Type Vision.VNObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNObservation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type VNObservation -->
<div> <!-- start type VNPixelBufferObservation -->
<h3>New Type Vision.VNPixelBufferObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNPixelBufferObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNPixelBufferObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
}
</pre>
</div> <!-- end type VNPixelBufferObservation -->
<div> <!-- start type VNRectangleObservation -->
<h3>New Type Vision.VNRectangleObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNRectangleObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRectangleObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNRectangleObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNRectangleObservation -->
<div> <!-- start type VNRequest -->
<h3>New Type Vision.VNRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestCompletionHandler CompletionHandler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreferBackgroundProcessing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice PreferredMetalContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual T[] GetResults&lt;T&gt; ();</span>
}
</pre>
</div> <!-- end type VNRequest -->
<div> <!-- start type VNRequestCompletionHandler -->
<h3>New Type Vision.VNRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate VNRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (VNRequest request, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (VNRequest request, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNRequestCompletionHandler -->
<div> <!-- start type VNRequestTrackingLevel -->
<h3>New Type Vision.VNRequestTrackingLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNRequestTrackingLevel {
	<span class='added added-field ' data-is-non-breaking="">Accurate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
}
</pre>
</div> <!-- end type VNRequestTrackingLevel -->
<div> <!-- start type VNSequenceRequestHandler -->
<h3>New Type Vision.VNSequenceRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNSequenceRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNSequenceRequestHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNSequenceRequestHandler -->
<div> <!-- start type VNTargetedImageRequest -->
<h3>New Type Vision.VNTargetedImageRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTargetedImageRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTargetedImageRequest -->
<div> <!-- start type VNTextObservation -->
<h3>New Type Vision.VNTextObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNTextObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTextObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRectangleObservation[] CharacterBoxes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNTextObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNTextObservation -->
<div> <!-- start type VNTrackObjectRequest -->
<h3>New Type Vision.VNTrackObjectRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackObjectRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackObjectRequest -->
<div> <!-- start type VNTrackRectangleRequest -->
<h3>New Type Vision.VNTrackRectangleRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackRectangleRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackRectangleRequest -->
<div> <!-- start type VNTrackingRequest -->
<h3>New Type Vision.VNTrackingRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTrackingRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackingRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNDetectedObjectObservation InputObservation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LastFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestTrackingLevel TrackingLevel { get; set; }</span>
}
</pre>
</div> <!-- end type VNTrackingRequest -->
<div> <!-- start type VNTranslationalImageRegistrationRequest -->
<h3>New Type Vision.VNTranslationalImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTranslationalImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTranslationalImageRegistrationRequest -->
<div> <!-- start type VNUtils -->
<h3>New Type Vision.VNUtils</h3>
<pre class='added' data-is-non-breaking="">
public static class VNUtils {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGRect NormalizedIdentityRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (CoreGraphics.CGPoint normalizedPoint, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetImageRect (CoreGraphics.CGRect normalizedRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetNormalizedFaceBoundingBoxPoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetNormalizedRect (CoreGraphics.CGRect imageRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsIdentityRect (CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type VNUtils -->
</div> <!-- end namespace Vision -->

</div>
