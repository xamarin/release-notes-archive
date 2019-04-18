---
id: 5997DFF8-1984-49F1-AC73-CCBDE48F44D9
title: "Mac 4.0 to 4.2"
---

# API diff

 [(Mobile profile) mscorlib.dll](#diff/xm/Xamarin.Mac/mscorlib.html)

   


 [(Mobile profile) System.Core.dll](#diff/xm/Xamarin.Mac/System.Core.html)

   


 [(Mobile profile) Mono.Security.dll](#diff/xm/Xamarin.Mac/Mono.Security.html)

   


 [(Mobile profile) Xamarin.Mac.dll](#diff/xm/Xamarin.Mac/Xamarin.Mac.html)

   


 [(Full profile) Xamarin.Mac.dll](#diff/xm/4.5/Xamarin.Mac.html)

   


   


 <hr>

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
</script><h1 id='diff/xm/Xamarin.Mac/mscorlib.html'>mscorlib.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<!-- start type Marshal --> <div>
<h3>Type Changed: System.Runtime.InteropServices.Marshal</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static IntPtr BufferToBSTR (System.Array ptr, int slen);</span>
</pre>

</div> <!-- end type Marshal -->

</div> <!-- end namespace System.Runtime.InteropServices -->
</div>



   


 <hr>

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
</script><h1 id='diff/xm/Xamarin.Mac/System.Core.html'>System.Core.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.Win32.SafeHandles --> <div> 
<h2>Namespace Microsoft.Win32.SafeHandles</h2>
<!-- start type SafeNCryptHandle --> <div>
<h3>Type Changed: Microsoft.Win32.SafeHandles.SafeNCryptHandle</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected SafeNCryptHandle (IntPtr handle, System.Runtime.InteropServices.SafeHandle parentHandle);</span>
</pre>
</div>

</div> <!-- end type SafeNCryptHandle -->
<!-- start type SafeNCryptKeyHandle --> <div>
<h3>Type Changed: Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SafeNCryptKeyHandle (IntPtr handle, System.Runtime.InteropServices.SafeHandle parentHandle);</span>
</pre>
</div>

</div> <!-- end type SafeNCryptKeyHandle -->

</div> <!-- end namespace Microsoft.Win32.SafeHandles -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type ECDsaCng --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDsaCng</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngAlgorithm HashAlgorithm { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void FromXmlString (string xml, ECKeyXmlFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] SignData (byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] SignData (System.IO.Stream data);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] SignData (byte[] data, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToXmlString (ECKeyXmlFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool VerifyData (byte[] data, byte[] signature);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool VerifyData (System.IO.Stream data, byte[] signature);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool VerifyData (byte[] data, int offset, int count, byte[] signature);</span>
</pre>
</div>

</div> <!-- end type ECDsaCng -->
<div> <!-- start type ECKeyXmlFormat -->
<h3>New Type System.Security.Cryptography.ECKeyXmlFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ECKeyXmlFormat {
	<span class='added added-field ' data-is-non-breaking="">Rfc4050 = 0,</span>
}
</pre>
</div> <!-- end type ECKeyXmlFormat -->

</div> <!-- end namespace System.Security.Cryptography -->
</div>



   


 <hr>

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
</script><h1 id='diff/xm/Xamarin.Mac/Mono.Security.html'>Mono.Security.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Mono.Security.Interface --> <div> 
<h2>Namespace Mono.Security.Interface</h2>
<!-- start type IMonoSslStream --> <div>
<h3>Type Changed: Mono.Security.Interface.IMonoSslStream</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Flush ();</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task WriteAsync (byte[] buffer, int offset, int count, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type IMonoSslStream -->
<h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.BufferOffsetSize</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.IBufferOffsetSize</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.IMonoTlsEventSink</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.SecretParameters</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.SecureBuffer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.TlsBuffer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.TlsMultiBuffer</span></h3>
</div> <!-- end namespace Mono.Security.Interface -->
</div>



   


 <hr>

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
</script><h1 id='diff/xm/Xamarin.Mac/Xamarin.Mac.html'>Xamarin.Mac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAssetResourceLoadingContentInformationRequest --> <div>
<h3>Type Changed: AVFoundation.AVAssetResourceLoadingContentInformationRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AllowedContentTypes { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetResourceLoadingContentInformationRequest -->
<!-- start type AVContentKeyRequest --> <div>
<h3>Type Changed: AVFoundation.AVContentKeyRequest</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("This API is not available on this platform.")]
	public virtual void RespondByRequestingPersistableContentKeyRequest ();</span>
</div></pre>

</div> <!-- end type AVContentKeyRequest -->
<!-- start type AVError --> <div>
<h3>Type Changed: AVFoundation.AVError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentIsUnavailable = -11863,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentNotUpdated = -11866,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatUnsupported = -11864,</span>
	<span class='added added-field ' data-is-non-breaking="">MalformedDepth = -11865,</span>
	<span class='added added-field ' data-is-non-breaking="">NoCompatibleAlternatesForExternalDisplay = -11868,</span>
	<span class='added added-field ' data-is-non-breaking="">NoLongerPlayable = -11867,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSourceTrack = -11869,</span>
</pre>
</div>

</div> <!-- end type AVError -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TopLevelUIElementAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LaunchUserNotificationKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetLayoutAttributes' instead.")]
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributest (string kind, Foundation.NSIndexPath indexPath);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSCollectionViewLayoutAttributes GetLayoutAttributes (string kind, Foundation.NSIndexPath indexPath);</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewDelegate --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegate</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDragOperation ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegate -->
<!-- start type NSCollectionViewDelegateFlowLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegateFlowLayout</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDragOperation ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegateFlowLayout -->
<!-- start type NSCollectionViewDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegate_Extensions</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public static NSDragOperation ValidateDrop (this INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSDragOperation ValidateDropOperation (this INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegate_Extensions -->
<!-- start type NSGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSGestureRecognizer</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSGestureRecognizerState State { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type NSGestureRecognizer -->
<!-- start type NSLayoutManager --> <div>
<h3>Type Changed: AppKit.NSLayoutManager</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetIntAttribute' instead.")]
	public virtual nint IntAttributeforGlyphAtIndex (nint attributeTag, nint glyphIndex);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetIntAttribute (nint attributeTag, nint glyphIndex);</span>
</pre>
</div>

</div> <!-- end type NSLayoutManager -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMenuItem (string title, string charCode, System.EventHandler handler, System.Func&lt;NSMenuItem,System.Boolean&gt; validator);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Func&lt;NSMenuItem,System.Boolean&gt; ValidateMenuItem { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLPixelFormatAttribute --> <div>
<h3>Type Changed: AppKit.NSOpenGLPixelFormatAttribute</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use 'TripleBuffer' instead.")]
	TrippleBuffer = 3,</span>
</div></pre>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TripleBuffer = 3,</span>
</pre>
</div>

</div> <!-- end type NSOpenGLPixelFormatAttribute -->
<!-- start type NSStackViewVisibilityPriority --> <div>
<h3>Type Changed: AppKit.NSStackViewVisibilityPriority</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use 'MustHold' instead.")]
	Musthold = 1000,</span>
</div></pre>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MustHold = 1000,</span>
</pre>
</div>

</div> <!-- end type NSStackViewVisibilityPriority -->

</div> <!-- end namespace AppKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactFormatter --> <div>
<h3>Type Changed: Contacts.CNContactFormatter</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CNContactFormatter -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumDrawableCount { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Center.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentCenter { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Justified.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentJustified { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Left.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentLeft { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'TextAlignmentMode' instead.")]
	public virtual string AlignmentMode { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Natural.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentNatural { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Right.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentRight { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.End.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionEnd { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.Middle.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionMiddle { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.Start.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionStart { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'TextTruncationMode' instead.")]
	public virtual string TruncationMode { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.None.GetConstant ()' instead.")]
	public static Foundation.NSString TruncationNone { get; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CATextLayerAlignmentMode TextAlignmentMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CATextLayerTruncationMode TextTruncationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakAlignmentMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakTruncationMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<div> <!-- start type CATextLayerAlignmentMode -->
<h3>New Type CoreAnimation.CATextLayerAlignmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CATextLayerAlignmentMode {
	<span class='added added-field ' data-is-non-breaking="">Center = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Justified = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Natural = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 1,</span>
}
</pre>
</div> <!-- end type CATextLayerAlignmentMode -->
<div> <!-- start type CATextLayerAlignmentModeExtensions -->
<h3>New Type CoreAnimation.CATextLayerAlignmentModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CATextLayerAlignmentModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (this CATextLayerAlignmentMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CATextLayerAlignmentMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CATextLayerAlignmentModeExtensions -->
<div> <!-- start type CATextLayerTruncationMode -->
<h3>New Type CoreAnimation.CATextLayerTruncationMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CATextLayerTruncationMode {
	<span class='added added-field ' data-is-non-breaking="">End = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Middle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type CATextLayerTruncationMode -->
<div> <!-- start type CATextLayerTruncationModeExtensions -->
<h3>New Type CoreAnimation.CATextLayerTruncationModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CATextLayerTruncationModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (this CATextLayerTruncationMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CATextLayerTruncationMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CATextLayerTruncationModeExtensions -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGEvent --> <div>
<h3>Type Changed: CoreGraphics.CGEvent</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'Timestamp' instead.")]
	public ulong Timestampe { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ulong Timestamp { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGEvent -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIAreaMaximum --> <div>
<h3>Type Changed: CoreImage.CIAreaMaximum</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMaximum (string name);</span>
</pre>
</div>

</div> <!-- end type CIAreaMaximum -->
<!-- start type CIFilterInputKey --> <div>
<h3>Type Changed: CoreImage.CIFilterInputKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DepthImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisparityImage { get; }</span>
</pre>
</div>

</div> <!-- end type CIFilterInputKey -->
<!-- start type CIImageInitializationOptions --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? ApplyOrientationProperty { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDepth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDisparity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NearestSampling { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIImageInitializationOptions -->
<!-- start type CIImageInitializationOptionsWithMetadata --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptionsWithMetadata</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>

</div> <!-- end type CIImageInitializationOptionsWithMetadata -->
<!-- start type CIMotionBlur --> <div>
<h3>Type Changed: CoreImage.CIMotionBlur</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>CoreImage.CIFilter</span> <span class='added '>CoreImage.CILinearBlur</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public float Radius { get; set; }</span>
</pre>

</div> <!-- end type CIMotionBlur -->
<!-- start type CIVector --> <div>
<h3>Type Changed: CoreImage.CIVector</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIVector (nfloat[] values, nint count);</span>
</pre>
</div>

</div> <!-- end type CIVector -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIAreaMaximum, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Extent { get; set; }</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSAttributedString Text { get; set; }</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIBarcodeDescriptor BarcodeDescriptor { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float AspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float B { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float C { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Scale { get; set; }</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIBlendWithRedMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIBokehBlur : CoreImage.CILinearBlur, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float RingAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float RingSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Softness { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube0Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube1Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float CubeDimension { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage MaskImage { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CurvesData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector CurvesDomain { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Aperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVFoundation.AVCameraCalibrationData CalibrationData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector ChinPositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage DisparityImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector FocusRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector LeftEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float LumaNoiseScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector NosePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector RightEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthDisparityConverter -->
<h3>New Type CoreImage.CIDepthDisparityConverter</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIDepthDisparityConverter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthDisparityConverter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthDisparityConverter (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (string name);</span>
}
</pre>
</div> <!-- end type CIDepthDisparityConverter -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIDisparityToDepth : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float LumaSigma { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage SmallImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float SpatialSigma { get; set; }</span>
}
</pre>
</div> <!-- end type CIEdgePreserveUpsampleFilter -->
<div> <!-- start type CIImageGenerator -->
<h3>New Type CoreImage.CIImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageGenerator (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIImageGenerator -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIImage Image2 { get; set; }</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CILinearBlur -->
<h3>New Type CoreImage.CILinearBlur</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CILinearBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILinearBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILinearBlur (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CILinearBlur -->
<div> <!-- start type CIMorphology -->
<h3>New Type CoreImage.CIMorphology</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIMorphology : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphology (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphology (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CIMorphology -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIMorphologyMaximum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIMorphologyMinimum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CITextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FontName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float FontSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Text { get; set; }</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreML --> <div> 
<h2>Namespace CoreML</h2>
<!-- start type MLModelError --> <div>
<h3>Type Changed: CoreML.MLModelError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CustomLayer = 4,</span>
</pre>
</div>

</div> <!-- end type MLModelError -->
<div> <!-- start type IMLCustomLayer -->
<h3>New Type CoreML.IMLCustomLayer</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLCustomLayer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EvaluateOnCpu (MLMultiArray[] inputs, MLMultiArray[] outputs, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSArray[] GetOutputShapes (Foundation.NSArray[] inputShapes, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetWeightData (Foundation.NSData[] weights, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IMLCustomLayer -->
<div> <!-- start type MLCustomLayer_Extensions -->
<h3>New Type CoreML.MLCustomLayer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLCustomLayer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Encode (this IMLCustomLayer This, Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture[] inputs, Metal.IMTLTexture[] outputs, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLCustomLayer_Extensions -->

</div> <!-- end namespace CoreML -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSDictionary --> <div>
<h3>Type Changed: Foundation.NSDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDictionary (NSDictionary other, bool copyItems);</span>
</pre>
</div>

</div> <!-- end type NSDictionary -->
<!-- start type NSMutableDictionary --> <div>
<h3>Type Changed: Foundation.NSMutableDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMutableDictionary (NSDictionary other, bool copyItems);</span>
</pre>
</div>

</div> <!-- end type NSMutableDictionary -->
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: Foundation.NSUrlSessionHandler</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionHandler (NSUrlSessionConfiguration configuration);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->

</div> <!-- end namespace Foundation -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual LABiometryType BiometryType { get; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<div> <!-- start type LABiometryType -->
<h3>New Type LocalAuthentication.LABiometryType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum LABiometryType {
	<span class='added added-field ' data-is-non-breaking="">FaceId = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchId = 1,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Use 'FaceId' instead.")]
	TypeFaceId = 2,</span>
}
</pre>
</div> <!-- end type LABiometryType -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type BlockLiteral --> <div>
<h3>Type Changed: ObjCRuntime.BlockLiteral</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetupBlockUnsafe (System.Delegate trampoline, System.Delegate userDelegate);</span>
</pre>
</div>

</div> <!-- end type BlockLiteral -->
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"4.0.0"</span> <span class='added '>"4.2.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string MetalPerformanceShadersLibrary = "/System/Library/Frameworks/MetalPerformanceShaders.framework/MetalPerformanceShaders";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'SetInt64' for long values instead.")]
	public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, ulong value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfAnnotation --> <div>
<h3>Type Changed: PdfKit.PdfAnnotation</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor InteriorColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StampName { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfAnnotation -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'FrameProcessor2' instead.")]
	public virtual PHLivePhotoFrameProcessingBlock FrameProcessor { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameProcessingBlock2 FrameProcessor2 { get; set; }</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type PHLivePhotoFrameProcessingBlock2 -->
<h3>New Type Photos.PHLivePhotoFrameProcessingBlock2</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHLivePhotoFrameProcessingBlock2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoFrameProcessingBlock2 (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IPHLivePhotoFrame frame, ref Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage EndInvoke (ref Foundation.NSError error, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage Invoke (IPHLivePhotoFrame frame, ref Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameProcessingBlock2 -->

</div> <!-- end namespace Photos -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecCertificate --> <div>
<h3>Type Changed: Security.SecCertificate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetSerialNumber (out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type SecCertificate -->
<!-- start type SecKeyAlgorithm --> <div>
<h3>Type Changed: Security.SecKeyAlgorithm</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha224AesGcm = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha256AesGcm = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha384AesGcm = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha512AesGcm = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha224AesGcm = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha256AesGcm = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha384AesGcm = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha512AesGcm = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha1 = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha224 = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha256 = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha384 = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha512 = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha1 = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha224 = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha256 = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha384 = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha512 = 67,</span>
</pre>
</div>

</div> <!-- end type SecKeyAlgorithm -->
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool PersistentReference { get; set; }</span>
</pre>
</div>

</div> <!-- end type SecRecord -->
<!-- start type SecStatusCode --> <div>
<h3>Type Changed: Security.SecStatusCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MissingEntitlement = -34018,</span>
</pre>
</div>

</div> <!-- end type SecStatusCode -->
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 = 52393,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 = 52392,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->
<!-- start type SslContext --> <div>
<h3>Type Changed: Security.SslContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public int SetError (SecStatusCode status);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetOcspResponse (Foundation.NSData response);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetSessionTickets (bool enabled);</span>
</pre>
</div>

</div> <!-- end type SslContext -->
<!-- start type SslProtocol --> <div>
<h3>Type Changed: Security.SslProtocol</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Tls_1_3 = 10,</span>
</pre>
</div>

</div> <!-- end type SslProtocol -->
<!-- start type SslSessionOption --> <div>
<h3>Type Changed: Security.SslSessionOption</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EnableSessionTickets = 9,</span>
</pre>
</div>

</div> <!-- end type SslSessionOption -->

</div> <!-- end namespace Security -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKProduct --> <div>
<h3>Type Changed: StoreKit.SKProduct</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscount IntroductoryPrice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
</pre>
</div>

</div> <!-- end type SKProduct -->
<div> <!-- start type SKProductDiscount -->
<h3>New Type StoreKit.SKProductDiscount</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductDiscount : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductDiscount ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfPeriods { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscountPaymentMode PaymentMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Price { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSLocale PriceLocale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
}
</pre>
</div> <!-- end type SKProductDiscount -->
<div> <!-- start type SKProductDiscountPaymentMode -->
<h3>New Type StoreKit.SKProductDiscountPaymentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductDiscountPaymentMode {
	<span class='added added-field ' data-is-non-breaking="">FreeTrial = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PayAsYouGo = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PayUpFront = 1,</span>
}
</pre>
</div> <!-- end type SKProductDiscountPaymentMode -->
<div> <!-- start type SKProductPeriodUnit -->
<h3>New Type StoreKit.SKProductPeriodUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductPeriodUnit {
	<span class='added added-field ' data-is-non-breaking="">Day = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Month = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Week = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Year = 3,</span>
}
</pre>
</div> <!-- end type SKProductPeriodUnit -->
<div> <!-- start type SKProductSubscriptionPeriod -->
<h3>New Type StoreKit.SKProductSubscriptionPeriod</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductSubscriptionPeriod : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductSubscriptionPeriod ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfUnits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductPeriodUnit Unit { get; }</span>
}
</pre>
</div> <!-- end type SKProductSubscriptionPeriod -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>New Namespace MetalPerformanceShaders</h2>

<div> <!-- start type IMPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.IMPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSCnnConvolutionDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type IMPSCnnConvolutionDataSource -->
<div> <!-- start type IMPSDeviceProvider -->
<h3>New Type MetalPerformanceShaders.IMPSDeviceProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSDeviceProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLDevice GetMTLDevice ();</span>
}
</pre>
</div> <!-- end type IMPSDeviceProvider -->
<div> <!-- start type IMPSHandle -->
<h3>New Type MetalPerformanceShaders.IMPSHandle</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSHandle : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
}
</pre>
</div> <!-- end type IMPSHandle -->
<div> <!-- start type IMPSImageAllocator -->
<h3>New Type MetalPerformanceShaders.IMPSImageAllocator</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageAllocator : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetImage (Metal.IMTLCommandBuffer cmdBuf, MPSImageDescriptor descriptor, MPSKernel kernel);</span>
}
</pre>
</div> <!-- end type IMPSImageAllocator -->
<div> <!-- start type IMPSImageSizeEncodingState -->
<h3>New Type MetalPerformanceShaders.IMPSImageSizeEncodingState</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageSizeEncodingState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type IMPSImageSizeEncodingState -->
<div> <!-- start type IMPSImageTransformProvider -->
<h3>New Type MetalPerformanceShaders.IMPSImageTransformProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageTransformProvider : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSScaleTransform GetTransform (MPSImage image, IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type IMPSImageTransformProvider -->
<div> <!-- start type IMPSNNPadding -->
<h3>New Type MetalPerformanceShaders.IMPSNNPadding</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSNNPadding : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
}
</pre>
</div> <!-- end type IMPSNNPadding -->
<div> <!-- start type MPSAlphaType -->
<h3>New Type MetalPerformanceShaders.MPSAlphaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSAlphaType {
	<span class='added added-field ' data-is-non-breaking="">AlphaIsOne = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPremultiplied = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Premultiplied = 2,</span>
}
</pre>
</div> <!-- end type MPSAlphaType -->
<div> <!-- start type MPSBinaryImageKernel -->
<h3>New Type MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSBinaryImageKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSBinaryImageKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSBinaryImageKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode PrimaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset PrimaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode SecondaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SecondaryOffset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture primaryTexture, Metal.IMTLTexture secondaryTexture, Metal.IMTLTexture destinationTexture);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture primaryTexture, out Foundation.NSObject inPlaceSecondaryTexture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, out Foundation.NSObject inPlacePrimaryTexture, Metal.IMTLTexture secondaryTexture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion PrimarySourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion SecondarySourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSBinaryImageKernel -->
<div> <!-- start type MPSCnnBinaryConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolution -->
<div> <!-- start type MPSCnnBinaryConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseBetaScaling = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionFlags -->
<div> <!-- start type MPSCnnBinaryConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolutionNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionNode -->
<div> <!-- start type MPSCnnBinaryConvolutionType -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionType {
	<span class='added added-field ' data-is-non-breaking="">And = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BinaryWeights = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Xnor = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionType -->
<div> <!-- start type MPSCnnBinaryFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnected : MetalPerformanceShaders.MPSCnnBinaryConvolution, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnected -->
<div> <!-- start type MPSCnnBinaryFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnectedNode : MetalPerformanceShaders.MPSCnnBinaryConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnectedNode -->
<div> <!-- start type MPSCnnBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode PrimaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset PrimaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode SecondaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SecondaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryKernel -->
<div> <!-- start type MPSCnnConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage, out MPSCnnConvolutionState state);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolution -->
<div> <!-- start type MPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnConvolutionDataSource : Foundation.NSObject, Foundation.INSObjectProtocol, IMPSCnnConvolutionDataSource, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetLookupTableForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRangesForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource -->
<div> <!-- start type MPSCnnConvolutionDataSource_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSCnnConvolutionDataSource_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetLookupTableForUInt8Kernel (this IMPSCnnConvolutionDataSource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetRangesForUInt8Kernel (this IMPSCnnConvolutionDataSource This);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource_Extensions -->
<div> <!-- start type MPSCnnConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SupportsSecureCoding { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor CreateCnnConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor GetConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels, MPSCnnNeuron neuronFilter);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBatchNormalizationParameters (float[] mean, float[] variance, float[] gamma, float[] beta, float epsilon);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData A);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDescriptor -->
<div> <!-- start type MPSCnnConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSCnnConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionFlags -->
<div> <!-- start type MPSCnnConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionStateNode ConvolutionState { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionNode -->
<div> <!-- start type MPSCnnConvolutionState -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, IMPSImageSizeEncodingState, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SourceOffset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionState -->
<div> <!-- start type MPSCnnConvolutionStateNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionStateNode : MetalPerformanceShaders.MPSNNStateNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionStateNode -->
<div> <!-- start type MPSCnnConvolutionTranspose -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTranspose</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTranspose : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSCnnConvolutionState convolutionState);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTranspose -->
<div> <!-- start type MPSCnnConvolutionTransposeNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTransposeNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTransposeNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTransposeNode (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionTransposeNode Create (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTransposeNode -->
<div> <!-- start type MPSCnnCrossChannelNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Metal.IMTLDevice device, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSize { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalization -->
<div> <!-- start type MPSCnnCrossChannelNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSizeInFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnCrossChannelNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalizationNode -->
<div> <!-- start type MPSCnnDepthWiseConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnDepthWiseConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDepthWiseConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDepthWiseConvolutionDescriptor -->
<div> <!-- start type MPSCnnDilatedPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint dilationRateX, uint dilationRateY, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMax -->
<div> <!-- start type MPSCnnDilatedPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY, uint dilationRateX, uint dilationRateY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMaxNode -->
<div> <!-- start type MPSCnnFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnected : MetalPerformanceShaders.MPSCnnConvolution, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnected -->
<div> <!-- start type MPSCnnFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnectedNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnectedNode -->
<div> <!-- start type MPSCnnKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnKernel</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode EdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion GetSourceRegion (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSCnnKernel -->
<div> <!-- start type MPSCnnLocalContrastNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalization -->
<div> <!-- start type MPSCnnLocalContrastNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLocalContrastNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalizationNode -->
<div> <!-- start type MPSCnnLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMax -->
<div> <!-- start type MPSCnnLogSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLogSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMaxNode -->
<div> <!-- start type MPSCnnNeuron -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuron</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnNeuron : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuron -->
<div> <!-- start type MPSCnnNeuronAbsolute -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsolute : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsolute -->
<div> <!-- start type MPSCnnNeuronAbsoluteNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsoluteNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsoluteNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsoluteNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronAbsoluteNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsoluteNode -->
<div> <!-- start type MPSCnnNeuronElu -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronElu</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronElu : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronElu -->
<div> <!-- start type MPSCnnNeuronEluNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronEluNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronEluNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronEluNode -->
<div> <!-- start type MPSCnnNeuronHardSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoid -->
<div> <!-- start type MPSCnnNeuronHardSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoidNode -->
<div> <!-- start type MPSCnnNeuronLinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinear : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinear -->
<div> <!-- start type MPSCnnNeuronLinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinearNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinearNode -->
<div> <!-- start type MPSCnnNeuronNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float C { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronNode -->
<div> <!-- start type MPSCnnNeuronPReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Metal.IMTLDevice device, float[] a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLU -->
<div> <!-- start type MPSCnnNeuronPReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLUNode (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronPReLUNode Create (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLUNode -->
<div> <!-- start type MPSCnnNeuronReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLU -->
<div> <!-- start type MPSCnnNeuronReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLUNode -->
<div> <!-- start type MPSCnnNeuronReLun -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLun</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLun : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLun -->
<div> <!-- start type MPSCnnNeuronReLunNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLunNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLunNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLunNode -->
<div> <!-- start type MPSCnnNeuronSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoid -->
<div> <!-- start type MPSCnnNeuronSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSigmoidNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoidNode -->
<div> <!-- start type MPSCnnNeuronSoftPlus -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlus</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlus : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlus -->
<div> <!-- start type MPSCnnNeuronSoftPlusNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlusNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlusNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlusNode -->
<div> <!-- start type MPSCnnNeuronSoftSign -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSign</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSign : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSign -->
<div> <!-- start type MPSCnnNeuronSoftSignNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSignNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSignNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSignNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftSignNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSignNode -->
<div> <!-- start type MPSCnnNeuronTanH -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanH : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanH -->
<div> <!-- start type MPSCnnNeuronTanHNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanHNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanHNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanHNode -->
<div> <!-- start type MPSCnnNeuronType -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnNeuronType {
	<span class='added added-field ' data-is-non-breaking="">Absolute = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Elu = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HardSigmoid = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PReLU = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLU = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLun = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Sigmoid = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftPlus = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftSign = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TanH = 5,</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronType -->
<div> <!-- start type MPSCnnNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNormalizationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNormalizationNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNormalizationNode -->
<div> <!-- start type MPSCnnPooling -->
<h3>New Type MetalPerformanceShaders.MPSCnnPooling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPooling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPooling -->
<div> <!-- start type MPSCnnPoolingAverage -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverage : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeY { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverage -->
<div> <!-- start type MPSCnnPoolingAverageNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverageNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverageNode -->
<div> <!-- start type MPSCnnPoolingL2Norm -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2Norm</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2Norm : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2Norm -->
<div> <!-- start type MPSCnnPoolingL2NormNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2NormNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2NormNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2NormNode -->
<div> <!-- start type MPSCnnPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMax -->
<div> <!-- start type MPSCnnPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMaxNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMaxNode -->
<div> <!-- start type MPSCnnPoolingNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size, uint stride);</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingNode -->
<div> <!-- start type MPSCnnSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMax -->
<div> <!-- start type MPSCnnSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMaxNode -->
<div> <!-- start type MPSCnnSpatialNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalization -->
<div> <!-- start type MPSCnnSpatialNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSpatialNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalizationNode -->
<div> <!-- start type MPSCnnSubPixelConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnSubPixelConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSubPixelConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSubPixelConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnSubPixelConvolutionDescriptor -->
<div> <!-- start type MPSCnnUpsampling -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsampling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsampling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsampling -->
<div> <!-- start type MPSCnnUpsamplingBilinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinear : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinear -->
<div> <!-- start type MPSCnnUpsamplingBilinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinearNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinearNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingBilinearNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinearNode -->
<div> <!-- start type MPSCnnUpsamplingNearest -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearest</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearest : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearest -->
<div> <!-- start type MPSCnnUpsamplingNearestNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearestNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearestNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearestNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingNearestNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearestNode -->
<div> <!-- start type MPSCopyAllocator -->
<h3>New Type MetalPerformanceShaders.MPSCopyAllocator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MPSCopyAllocator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCopyAllocator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MPSKernel filter, Foundation.NSObject commandBuffer, Foundation.NSObject sourceTexture, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Invoke (MPSKernel filter, Foundation.NSObject commandBuffer, Foundation.NSObject sourceTexture);</span>
}
</pre>
</div> <!-- end type MPSCopyAllocator -->
<div> <!-- start type MPSDataLayout -->
<h3>New Type MetalPerformanceShaders.MPSDataLayout</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataLayout {
	<span class='added added-field ' data-is-non-breaking="">FeatureChannelsPerHeightPerWidth = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HeightPerWidthPerFeatureChannels = 0,</span>
}
</pre>
</div> <!-- end type MPSDataLayout -->
<div> <!-- start type MPSDataType -->
<h3>New Type MetalPerformanceShaders.MPSDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataType {
	<span class='added added-field ' data-is-non-breaking="">Float16 = 268435472,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 268435488,</span>
	<span class='added added-field ' data-is-non-breaking="">FloatBit = 268435456,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalizedBit = 1073741824,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm1 = 1073741825,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1073741832,</span>
}
</pre>
</div> <!-- end type MPSDataType -->
<div> <!-- start type MPSGRUDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSGRUDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSGRUDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSGRUDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipOutputGates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float GatePnormValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputGateWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSGRUDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSGRUDescriptor -->
<div> <!-- start type MPSImage -->
<h3>New Type MetalPerformanceShaders.MPSImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImage : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLDevice device, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLTexture texture, uint featureChannels);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Precision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture Texture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureType TextureType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSPurgeableState SetPurgeableState (MPSPurgeableState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
}
</pre>
</div> <!-- end type MPSImage -->
<div> <!-- start type MPSImageAdd -->
<h3>New Type MetalPerformanceShaders.MPSImageAdd</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAdd : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAdd -->
<div> <!-- start type MPSImageAreaMax -->
<h3>New Type MetalPerformanceShaders.MPSImageAreaMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAreaMax : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAreaMax -->
<div> <!-- start type MPSImageAreaMin -->
<h3>New Type MetalPerformanceShaders.MPSImageAreaMin</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAreaMin : MetalPerformanceShaders.MPSImageAreaMax, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMin (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMin (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAreaMin -->
<div> <!-- start type MPSImageArithmetic -->
<h3>New Type MetalPerformanceShaders.MPSImageArithmetic</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageArithmetic : MetalPerformanceShaders.MPSBinaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PrimaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize PrimaryStrideInPixels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float SecondaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize SecondaryStrideInPixels { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageArithmetic -->
<div> <!-- start type MPSImageBilinearScale -->
<h3>New Type MetalPerformanceShaders.MPSImageBilinearScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageBilinearScale : MetalPerformanceShaders.MPSImageScale, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageBilinearScale -->
<div> <!-- start type MPSImageBox -->
<h3>New Type MetalPerformanceShaders.MPSImageBox</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageBox : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBox (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBox (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageBox -->
<div> <!-- start type MPSImageConversion -->
<h3>New Type MetalPerformanceShaders.MPSImageConversion</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageConversion : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Metal.IMTLDevice device, MPSAlphaType srcAlpha, MPSAlphaType destAlpha, nfloat[] backgroundColor, CoreGraphics.CGColorConversionInfo conversionInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType DestinationAlpha { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType SourceAlpha { get; }</span>
}
</pre>
</div> <!-- end type MPSImageConversion -->
<div> <!-- start type MPSImageConvolution -->
<h3>New Type MetalPerformanceShaders.MPSImageConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageConvolution : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageConvolution -->
<div> <!-- start type MPSImageCopyToMatrix -->
<h3>New Type MetalPerformanceShaders.MPSImageCopyToMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageCopyToMatrix : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Metal.IMTLDevice device, MPSDataLayout dataLayout);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataLayout DataLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationMatrixBatchIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin DestinationMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSMatrix destinationMatrix);</span>
}
</pre>
</div> <!-- end type MPSImageCopyToMatrix -->
<div> <!-- start type MPSImageDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSImageDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat ChannelFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLCpuCacheMode CpuCacheMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLStorageMode StorageMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels, uint numberOfImages, Metal.MTLTextureUsage usage);</span>
}
</pre>
</div> <!-- end type MPSImageDescriptor -->
<div> <!-- start type MPSImageDilate -->
<h3>New Type MetalPerformanceShaders.MPSImageDilate</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDilate : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDilate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDilate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] values);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageDilate -->
<div> <!-- start type MPSImageDivide -->
<h3>New Type MetalPerformanceShaders.MPSImageDivide</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDivide : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageDivide -->
<div> <!-- start type MPSImageEdgeMode -->
<h3>New Type MetalPerformanceShaders.MPSImageEdgeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSImageEdgeMode {
	<span class='added added-field ' data-is-non-breaking="">Clamp = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Zero = 0,</span>
}
</pre>
</div> <!-- end type MPSImageEdgeMode -->
<div> <!-- start type MPSImageErode -->
<h3>New Type MetalPerformanceShaders.MPSImageErode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageErode : MetalPerformanceShaders.MPSImageDilate, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageErode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageErode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] values);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageErode -->
<div> <!-- start type MPSImageFeatureChannelFormat -->
<h3>New Type MetalPerformanceShaders.MPSImageFeatureChannelFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSImageFeatureChannelFormat {
	<span class='added added-field ' data-is-non-breaking="">Float16 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm16 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1,</span>
}
</pre>
</div> <!-- end type MPSImageFeatureChannelFormat -->
<div> <!-- start type MPSImageFindKeypoints -->
<h3>New Type MetalPerformanceShaders.MPSImageFindKeypoints</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageFindKeypoints : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Metal.IMTLDevice device, MPSImageKeypointRangeInfo info);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageKeypointRangeInfo KeypointRangeInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.MTLRegion regions, uint numberOfRegions, Metal.IMTLBuffer keypointCountBuffer, uint keypointCountBufferOffset, Metal.IMTLBuffer keypointDataBuffer, uint keypointDataBufferOffset);</span>
}
</pre>
</div> <!-- end type MPSImageFindKeypoints -->
<div> <!-- start type MPSImageGaussianBlur -->
<h3>New Type MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageGaussianBlur : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianBlur (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Metal.IMTLDevice device, float sigma);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Sigma { get; }</span>
}
</pre>
</div> <!-- end type MPSImageGaussianBlur -->
<div> <!-- start type MPSImageGaussianPyramid -->
<h3>New Type MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageGaussianPyramid : MetalPerformanceShaders.MPSImagePyramid, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageGaussianPyramid -->
<div> <!-- start type MPSImageHistogram -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogram</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogram : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogram (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogram (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector4 MinPixelThresholdValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ZeroHistogram { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer histogram, uint histogramOffset);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetHistogramSize (Metal.MTLPixelFormat sourceFormat);</span>
}
</pre>
</div> <!-- end type MPSImageHistogram -->
<div> <!-- start type MPSImageHistogramEqualization -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogramEqualization : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramEqualization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramEqualization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTransformToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer histogram, uint histogramOffset);</span>
}
</pre>
</div> <!-- end type MPSImageHistogramEqualization -->
<div> <!-- start type MPSImageHistogramInfo -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageHistogramInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool HistogramForAlpha;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector4 MaxPixelValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector4 MinPixelValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint NumberOfHistogramEntries;</span>
}
</pre>
</div> <!-- end type MPSImageHistogramInfo -->
<div> <!-- start type MPSImageHistogramSpecification -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogramSpecification : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramSpecification (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramSpecification (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTransformToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer sourceHistogram, uint sourceHistogramOffset, Metal.IMTLBuffer desiredHistogram, uint desiredHistogramOffset);</span>
}
</pre>
</div> <!-- end type MPSImageHistogramSpecification -->
<div> <!-- start type MPSImageIntegral -->
<h3>New Type MetalPerformanceShaders.MPSImageIntegral</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageIntegral : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegral (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegral (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageIntegral -->
<div> <!-- start type MPSImageIntegralOfSquares -->
<h3>New Type MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageIntegralOfSquares : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegralOfSquares (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegralOfSquares (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageIntegralOfSquares -->
<div> <!-- start type MPSImageKeypointRangeInfo -->
<h3>New Type MetalPerformanceShaders.MPSImageKeypointRangeInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageKeypointRangeInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint MaximumKeypoints;</span>
	<span class='added added-field ' data-is-non-breaking="">public float MinimumThresholdValue;</span>
}
</pre>
</div> <!-- end type MPSImageKeypointRangeInfo -->
<div> <!-- start type MPSImageLanczosScale -->
<h3>New Type MetalPerformanceShaders.MPSImageLanczosScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageLanczosScale : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLanczosScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLanczosScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform? ScaleTransform { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageLanczosScale -->
<div> <!-- start type MPSImageLaplacian -->
<h3>New Type MetalPerformanceShaders.MPSImageLaplacian</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageLaplacian : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageLaplacian -->
<div> <!-- start type MPSImageMedian -->
<h3>New Type MetalPerformanceShaders.MPSImageMedian</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageMedian : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMedian (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMedian (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Metal.IMTLDevice device, uint kernelDiameter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelDiameter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static uint MaxKernelDiameter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static uint MinKernelDiameter { get; }</span>
}
</pre>
</div> <!-- end type MPSImageMedian -->
<div> <!-- start type MPSImageMultiply -->
<h3>New Type MetalPerformanceShaders.MPSImageMultiply</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageMultiply : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageMultiply -->
<div> <!-- start type MPSImagePyramid -->
<h3>New Type MetalPerformanceShaders.MPSImagePyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImagePyramid : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, float centerWeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImagePyramid -->
<div> <!-- start type MPSImageReadWriteParams -->
<h3>New Type MetalPerformanceShaders.MPSImageReadWriteParams</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageReadWriteParams {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint FeatureChannelOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint NumberOfFeatureChannelsToReadWrite;</span>
}
</pre>
</div> <!-- end type MPSImageReadWriteParams -->
<div> <!-- start type MPSImageScale -->
<h3>New Type MetalPerformanceShaders.MPSImageScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageScale : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform ScaleTransform { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageScale -->
<div> <!-- start type MPSImageSobel -->
<h3>New Type MetalPerformanceShaders.MPSImageSobel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageSobel : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSobel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSobel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Metal.IMTLDevice device, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] ColorTransform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageSobel -->
<div> <!-- start type MPSImageStatisticsMean -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMean</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMean : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMean -->
<div> <!-- start type MPSImageStatisticsMeanAndVariance -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMeanAndVariance</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMeanAndVariance : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMeanAndVariance -->
<div> <!-- start type MPSImageStatisticsMinAndMax -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMinAndMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMinAndMax : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMinAndMax -->
<div> <!-- start type MPSImageSubtract -->
<h3>New Type MetalPerformanceShaders.MPSImageSubtract</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageSubtract : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageSubtract -->
<div> <!-- start type MPSImageTent -->
<h3>New Type MetalPerformanceShaders.MPSImageTent</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageTent : MetalPerformanceShaders.MPSImageBox, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageTent -->
<div> <!-- start type MPSImageThresholdBinary -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdBinary : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinary (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Metal.IMTLDevice device, float thresholdValue, float maximumValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdBinary -->
<div> <!-- start type MPSImageThresholdBinaryInverse -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdBinaryInverse : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinaryInverse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinaryInverse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Metal.IMTLDevice device, float thresholdValue, float maximumValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdBinaryInverse -->
<div> <!-- start type MPSImageThresholdToZero -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdToZero : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZero (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZero (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdToZero -->
<div> <!-- start type MPSImageThresholdToZeroInverse -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdToZeroInverse : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZeroInverse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZeroInverse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdToZeroInverse -->
<div> <!-- start type MPSImageThresholdTruncate -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdTruncate : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdTruncate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdTruncate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdTruncate -->
<div> <!-- start type MPSImageTranspose -->
<h3>New Type MetalPerformanceShaders.MPSImageTranspose</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageTranspose : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTranspose (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTranspose (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageTranspose -->
<div> <!-- start type MPSKernel -->
<h3>New Type MetalPerformanceShaders.MPSKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSKernel : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSKernelOptions Options { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Metal.MTLRegion RectNoClip { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSKernel CopyWithZone (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Supports (Metal.IMTLDevice device);</span>
}
</pre>
</div> <!-- end type MPSKernel -->
<div> <!-- start type MPSKernelOptions -->
<h3>New Type MetalPerformanceShaders.MPSKernelOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSKernelOptions {
	<span class='added added-field ' data-is-non-breaking="">MPSKernelOptionsAllowReducedPrecision = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SkipApiValidation = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Verbose = 16,</span>
}
</pre>
</div> <!-- end type MPSKernelOptions -->
<div> <!-- start type MPSLSTMDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSLSTMDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSLSTMDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSLSTMDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreMemoryWeightsDiagonal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamA { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamB { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamC { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType CellToOutputNeuronType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSLSTMDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSLSTMDescriptor -->
<div> <!-- start type MPSMatrix -->
<h3>New Type MetalPerformanceShaders.MPSMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrix : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrix (Metal.IMTLBuffer buffer, MPSMatrixDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrix -->
<div> <!-- start type MPSMatrixBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin PrimarySourceMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SecondarySourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixBinaryKernel -->
<div> <!-- start type MPSMatrixCopy -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopy</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopy : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Metal.IMTLDevice device, uint copyRows, uint copyColumns, bool areSourcesTransposed, bool areDestinationsTransposed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreDestinationsTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreSourcesTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyColumns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyRows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer cmdBuf, MPSMatrixCopyDescriptor copyDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixCopyDescriptor copyDescriptor, MPSVector rowPermuteIndices, uint rowPermuteOffset, MPSVector columnPermuteIndices, uint columnPermuteOffset);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopy -->
<div> <!-- start type MPSMatrixCopyDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopyDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (Metal.IMTLDevice device, uint count);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSVector offsets, uint byteOffset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixCopyDescriptor Create (MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCopyOperation (uint index, MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyDescriptor -->
<div> <!-- start type MPSMatrixCopyOffsets -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyOffsets</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSMatrixCopyOffsets {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationRowOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceRowOffset;</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyOffsets -->
<div> <!-- start type MPSMatrixDecompositionCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionCholesky : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device, bool lower, uint order);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionCholesky -->
<div> <!-- start type MPSMatrixDecompositionLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionLU : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device, uint rows, uint columns);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, MPSMatrix pivotIndices, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionLU -->
<div> <!-- start type MPSMatrixDecompositionStatus -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSMatrixDecompositionStatus {
	<span class='added added-field ' data-is-non-breaking="">Failure = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPositiveDefinite = -3,</span>
	<span class='added added-field ' data-is-non-breaking="">Singular = -2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionStatus -->
<div> <!-- start type MPSMatrixDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor Create (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint matrices, uint rowBytes, uint matrixBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesForColumns (uint columns, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesFromColumns (uint columns, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSMatrixDescriptor -->
<div> <!-- start type MPSMatrixFindTopK -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFindTopK</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFindTopK : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Metal.IMTLDevice device, uint numberOfTopKValues);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfTopKValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFindTopK Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultIndexMatrix, MPSMatrix resultValueMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixFindTopK -->
<div> <!-- start type MPSMatrixFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFullyConnected : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceOutputFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFullyConnected Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix weightMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixFullyConnected -->
<div> <!-- start type MPSMatrixLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixLogSoftMax : MetalPerformanceShaders.MPSMatrixSoftMax, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrixLogSoftMax -->
<div> <!-- start type MPSMatrixMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixMultiplication : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, uint resultRows, uint resultColumns, uint interiorColumns);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, bool transposeLeft, bool transposeRight, uint resultRows, uint resultColumns, uint interiorColumns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin LeftMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin RightMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix leftMatrix, MPSMatrix rightMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixMultiplication -->
<div> <!-- start type MPSMatrixNeuron -->
<h3>New Type MetalPerformanceShaders.MPSMatrixNeuron</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixNeuron : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixNeuron Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData parametersA);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixNeuron -->
<div> <!-- start type MPSMatrixSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSoftMax : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixSoftMax Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSoftMax -->
<div> <!-- start type MPSMatrixSolveCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveCholesky : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device, bool upper, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveCholesky -->
<div> <!-- start type MPSMatrixSolveLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveLU : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device, bool transpose, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix pivotIndices, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveLU -->
<div> <!-- start type MPSMatrixSolveTriangular -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveTriangular</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveTriangular : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device, bool right, bool upper, bool transpose, bool unit, uint order, uint numberOfRightHandSides, double alpha);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveTriangular -->
<div> <!-- start type MPSMatrixSum -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSum</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSum : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Metal.IMTLDevice device, uint count, uint rows, uint columns, bool transpose);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Transpose { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer buffer, MPSMatrix[] sourceMatrices, MPSMatrix resultMatrix, MPSVector scaleVector, MPSVector offsetVector, MPSVector biasVector, uint startIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixSum -->
<div> <!-- start type MPSMatrixUnaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixUnaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixUnaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixUnaryKernel -->
<div> <!-- start type MPSMatrixVectorMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixVectorMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixVectorMultiplication : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, uint rows, uint columns);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, bool transpose, uint rows, uint columns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector inputVector, MPSVector resultVector);</span>
}
</pre>
</div> <!-- end type MPSMatrixVectorMultiplication -->
<div> <!-- start type MPSNNAdditionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNAdditionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNAdditionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNAdditionNode -->
<div> <!-- start type MPSNNBilinearScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBilinearScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBilinearScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNBilinearScaleNode -->
<div> <!-- start type MPSNNBinaryArithmeticNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBinaryArithmeticNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBinaryArithmeticNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode left, MPSNNImageNode right);</span>
}
</pre>
</div> <!-- end type MPSNNBinaryArithmeticNode -->
<div> <!-- start type MPSNNConcatenationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNConcatenationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNConcatenationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNConcatenationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNConcatenationNode Create (MPSNNImageNode[] sourceNodes);</span>
}
</pre>
</div> <!-- end type MPSNNConcatenationNode -->
<div> <!-- start type MPSNNDefaultPadding -->
<h3>New Type MetalPerformanceShaders.MPSNNDefaultPadding</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDefaultPadding : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IMPSNNPadding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDefaultPadding (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding Create (MPSNNPaddingMethod method);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding CreatePaddingForTensorflowAveragePooling ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImageDescriptor GetDestinationImageDescriptor (MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetLabel ();</span>
}
</pre>
</div> <!-- end type MPSNNDefaultPadding -->
<div> <!-- start type MPSNNDivisionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNDivisionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDivisionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNDivisionNode -->
<div> <!-- start type MPSNNFilterNode -->
<h3>New Type MetalPerformanceShaders.MPSNNFilterNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNFilterNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding PaddingPolicy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNImageNode ResultImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode ResultState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode[] ResultStates { get; }</span>
}
</pre>
</div> <!-- end type MPSNNFilterNode -->
<div> <!-- start type MPSNNGraph -->
<h3>New Type MetalPerformanceShaders.MPSNNGraph</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNGraph : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Metal.IMTLDevice device, MPSNNImageNode resultImage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] IntermediateImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOutputStateTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle ResultHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] ResultStateHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceStateHandles { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSState[] sourceStates, Foundation.NSMutableArray&lt;MPSImage&gt; intermediateImages, Foundation.NSMutableArray&lt;MPSState&gt; destinationStates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage Execute (MPSImage[] sourceImages, System.Action&lt;MPSImage,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages, out MPSImage result);</span>
}
</pre>
</div> <!-- end type MPSNNGraph -->
<div> <!-- start type MPSNNImageNode -->
<h3>New Type MetalPerformanceShaders.MPSNNImageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNImageNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNImageNode (IMPSHandle handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExportFromGraph { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat Format { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator ImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode Create (IMPSHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode GetExportedNode (IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type MPSNNImageNode -->
<div> <!-- start type MPSNNLanczosScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNLanczosScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNLanczosScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNLanczosScaleNode -->
<div> <!-- start type MPSNNMultiplicationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNMultiplicationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNMultiplicationNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNMultiplicationNode -->
<div> <!-- start type MPSNNPaddingMethod -->
<h3>New Type MetalPerformanceShaders.MPSNNPaddingMethod</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSNNPaddingMethod {
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomLeft = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomRight = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopLeft = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignBottomRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignCentered = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignReserved = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignTopLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 16384,</span>
	<span class='added added-field ' data-is-non-breaking="">ExcludeEdges = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeFull = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeMask = 2032,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeReserved = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeSame = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeValidOnly = 0,</span>
}
</pre>
</div> <!-- end type MPSNNPaddingMethod -->
<div> <!-- start type MPSNNPadding_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSNNPadding_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSNNPadding_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetDestinationImageDescriptor (this IMPSNNPadding This, MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetLabel (this IMPSNNPadding This);</span>
}
</pre>
</div> <!-- end type MPSNNPadding_Extensions -->
<div> <!-- start type MPSNNScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNScaleNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
}
</pre>
</div> <!-- end type MPSNNScaleNode -->
<div> <!-- start type MPSNNStateNode -->
<h3>New Type MetalPerformanceShaders.MPSNNStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNStateNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
}
</pre>
</div> <!-- end type MPSNNStateNode -->
<div> <!-- start type MPSNNSubtractionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNSubtractionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNSubtractionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNSubtractionNode -->
<div> <!-- start type MPSOffset -->
<h3>New Type MetalPerformanceShaders.MPSOffset</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSOffset {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public nint X;</span>
	<span class='added added-field ' data-is-non-breaking="">public nint Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public nint Z;</span>
}
</pre>
</div> <!-- end type MPSOffset -->
<div> <!-- start type MPSOrigin -->
<h3>New Type MetalPerformanceShaders.MPSOrigin</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSOrigin {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double X;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Z;</span>
}
</pre>
</div> <!-- end type MPSOrigin -->
<div> <!-- start type MPSPurgeableState -->
<h3>New Type MetalPerformanceShaders.MPSPurgeableState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSPurgeableState {
	<span class='added added-field ' data-is-non-breaking="">AllocationDeferred = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Empty = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">KeepCurrent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonVolatile = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Volatile = 3,</span>
}
</pre>
</div> <!-- end type MPSPurgeableState -->
<div> <!-- start type MPSRegion -->
<h3>New Type MetalPerformanceShaders.MPSRegion</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSRegion {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public MPSOrigin Origin;</span>
	<span class='added added-field ' data-is-non-breaking="">public MPSSize Size;</span>
}
</pre>
</div> <!-- end type MPSRegion -->
<div> <!-- start type MPSRnnBidirectionalCombineMode -->
<h3>New Type MetalPerformanceShaders.MPSRnnBidirectionalCombineMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnBidirectionalCombineMode {
	<span class='added added-field ' data-is-non-breaking="">Add = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Concatenate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnBidirectionalCombineMode -->
<div> <!-- start type MPSRnnDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnSequenceDirection LayerSequenceDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseFloat32Weights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseLayerInputUnitTransformMode { get; set; }</span>
}
</pre>
</div> <!-- end type MPSRnnDescriptor -->
<div> <!-- start type MPSRnnImageInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnImageInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnImageInferenceLayer : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnImageInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceSequence, MPSImage[] destinationForwardImages, MPSImage[] destinationBackwardImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSImage[] destinationImages, MPSRnnRecurrentImageState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentImageState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnImageInferenceLayer -->
<div> <!-- start type MPSRnnMatrixInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnMatrixInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnMatrixInferenceLayer : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnMatrixInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceSequence, MPSMatrix[] destinationForwardMatrices, MPSMatrix[] destinationBackwardMatrices);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSRnnRecurrentMatrixState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentMatrixState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnMatrixInferenceLayer -->
<div> <!-- start type MPSRnnRecurrentImageState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentImageState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentImageState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetMemoryCellImage (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetRecurrentOutputImage (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentImageState -->
<div> <!-- start type MPSRnnRecurrentMatrixState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentMatrixState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentMatrixState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetMemoryCellMatrix (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetRecurrentOutputMatrix (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentMatrixState -->
<div> <!-- start type MPSRnnSequenceDirection -->
<h3>New Type MetalPerformanceShaders.MPSRnnSequenceDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnSequenceDirection {
	<span class='added added-field ' data-is-non-breaking="">Backward = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Forward = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnSequenceDirection -->
<div> <!-- start type MPSRnnSingleGateDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnSingleGateDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnSingleGateDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnSingleGateDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSRnnSingleGateDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSRnnSingleGateDescriptor -->
<div> <!-- start type MPSScaleTransform -->
<h3>New Type MetalPerformanceShaders.MPSScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSScaleTransform {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double ScaleX;</span>
	<span class='added added-field ' data-is-non-breaking="">public double ScaleY;</span>
	<span class='added added-field ' data-is-non-breaking="">public double TranslateX;</span>
	<span class='added added-field ' data-is-non-breaking="">public double TranslateY;</span>
}
</pre>
</div> <!-- end type MPSScaleTransform -->
<div> <!-- start type MPSSize -->
<h3>New Type MetalPerformanceShaders.MPSSize</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSSize {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double Depth;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Height;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Width;</span>
}
</pre>
</div> <!-- end type MPSSize -->
<div> <!-- start type MPSState -->
<h3>New Type MetalPerformanceShaders.MPSState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSState : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsTemporary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
}
</pre>
</div> <!-- end type MPSState -->
<div> <!-- start type MPSTemporaryImage -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryImage : MetalPerformanceShaders.MPSImage, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, Metal.MTLTextureDescriptor textureDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryImage -->
<div> <!-- start type MPSTemporaryMatrix -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryMatrix : MetalPerformanceShaders.MPSMatrix, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryMatrix Create (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor matrixDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryMatrix -->
<div> <!-- start type MPSTemporaryVector -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryVector : MetalPerformanceShaders.MPSVector, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryVector Create (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryVector -->
<div> <!-- start type MPSUnaryImageKernel -->
<h3>New Type MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSUnaryImageKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSUnaryImageKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSUnaryImageKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode EdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset Offset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture sourceTexture, Metal.IMTLTexture destinationTexture);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, out Foundation.NSObject texture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion SourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSUnaryImageKernel -->
<div> <!-- start type MPSVector -->
<h3>New Type MetalPerformanceShaders.MPSVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVector : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSVector (Metal.IMTLBuffer buffer, MPSVectorDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
}
</pre>
</div> <!-- end type MPSVector -->
<div> <!-- start type MPSVectorDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSVectorDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVectorDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, uint vectors, uint vectorBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetVectorBytes (uint length, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSVectorDescriptor -->
</div> <!-- end namespace MetalPerformanceShaders -->

</div>



   


 <hr>

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
</script><h1 id='diff/xm/4.5/Xamarin.Mac.html'>Xamarin.Mac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAssetResourceLoadingContentInformationRequest --> <div>
<h3>Type Changed: AVFoundation.AVAssetResourceLoadingContentInformationRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AllowedContentTypes { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetResourceLoadingContentInformationRequest -->
<!-- start type AVContentKeyRequest --> <div>
<h3>Type Changed: AVFoundation.AVContentKeyRequest</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("This API is not available on this platform.")]
	public virtual void RespondByRequestingPersistableContentKeyRequest ();</span>
</div></pre>

</div> <!-- end type AVContentKeyRequest -->
<!-- start type AVError --> <div>
<h3>Type Changed: AVFoundation.AVError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentIsUnavailable = -11863,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentNotUpdated = -11866,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatUnsupported = -11864,</span>
	<span class='added added-field ' data-is-non-breaking="">MalformedDepth = -11865,</span>
	<span class='added added-field ' data-is-non-breaking="">NoCompatibleAlternatesForExternalDisplay = -11868,</span>
	<span class='added added-field ' data-is-non-breaking="">NoLongerPlayable = -11867,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSourceTrack = -11869,</span>
</pre>
</div>

</div> <!-- end type AVError -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TopLevelUIElementAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LaunchUserNotificationKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetLayoutAttributes' instead.")]
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributest (string kind, Foundation.NSIndexPath indexPath);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSCollectionViewLayoutAttributes GetLayoutAttributes (string kind, Foundation.NSIndexPath indexPath);</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewDelegate --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegate</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDragOperation ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegate -->
<!-- start type NSCollectionViewDelegateFlowLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegateFlowLayout</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDragOperation ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegateFlowLayout -->
<!-- start type NSCollectionViewDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSCollectionViewDelegate_Extensions</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'ValidateDropOperation (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation)' instead.")]
	public static NSDragOperation ValidateDrop (this INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, out Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSDragOperation ValidateDropOperation (this INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref Foundation.NSIndexPath proposedDropIndexPath, ref NSCollectionViewDropOperation proposedDropOperation);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewDelegate_Extensions -->
<!-- start type NSGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSGestureRecognizer</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSGestureRecognizerState State { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type NSGestureRecognizer -->
<!-- start type NSLayoutManager --> <div>
<h3>Type Changed: AppKit.NSLayoutManager</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetIntAttribute' instead.")]
	public virtual nint IntAttributeforGlyphAtIndex (nint attributeTag, nint glyphIndex);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetIntAttribute (nint attributeTag, nint glyphIndex);</span>
</pre>
</div>

</div> <!-- end type NSLayoutManager -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMenuItem (string title, string charCode, System.EventHandler handler, System.Func&lt;NSMenuItem,System.Boolean&gt; validator);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Func&lt;NSMenuItem,System.Boolean&gt; ValidateMenuItem { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLPixelFormatAttribute --> <div>
<h3>Type Changed: AppKit.NSOpenGLPixelFormatAttribute</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use 'TripleBuffer' instead.")]
	TrippleBuffer = 3,</span>
</div></pre>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TripleBuffer = 3,</span>
</pre>
</div>

</div> <!-- end type NSOpenGLPixelFormatAttribute -->
<!-- start type NSStackViewVisibilityPriority --> <div>
<h3>Type Changed: AppKit.NSStackViewVisibilityPriority</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use 'MustHold' instead.")]
	Musthold = 1000,</span>
</div></pre>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MustHold = 1000,</span>
</pre>
</div>

</div> <!-- end type NSStackViewVisibilityPriority -->

</div> <!-- end namespace AppKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactFormatter --> <div>
<h3>Type Changed: Contacts.CNContactFormatter</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CNContactFormatter -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumDrawableCount { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Center.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentCenter { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Justified.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentJustified { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Left.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentLeft { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'TextAlignmentMode' instead.")]
	public virtual string AlignmentMode { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Natural.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentNatural { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerAlignmentMode.Right.GetConstant ()' instead.")]
	public static Foundation.NSString AlignmentRight { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.End.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionEnd { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.Middle.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionMiddle { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.Start.GetConstant ()' instead.")]
	public static Foundation.NSString TruncantionStart { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'TextTruncationMode' instead.")]
	public virtual string TruncationMode { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'CATextLayerTruncationMode.None.GetConstant ()' instead.")]
	public static Foundation.NSString TruncationNone { get; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CATextLayerAlignmentMode TextAlignmentMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CATextLayerTruncationMode TextTruncationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakAlignmentMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakTruncationMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<div> <!-- start type CATextLayerAlignmentMode -->
<h3>New Type CoreAnimation.CATextLayerAlignmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CATextLayerAlignmentMode {
	<span class='added added-field ' data-is-non-breaking="">Center = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Justified = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Natural = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 1,</span>
}
</pre>
</div> <!-- end type CATextLayerAlignmentMode -->
<div> <!-- start type CATextLayerAlignmentModeExtensions -->
<h3>New Type CoreAnimation.CATextLayerAlignmentModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CATextLayerAlignmentModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (this CATextLayerAlignmentMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CATextLayerAlignmentMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CATextLayerAlignmentModeExtensions -->
<div> <!-- start type CATextLayerTruncationMode -->
<h3>New Type CoreAnimation.CATextLayerTruncationMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CATextLayerTruncationMode {
	<span class='added added-field ' data-is-non-breaking="">End = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Middle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type CATextLayerTruncationMode -->
<div> <!-- start type CATextLayerTruncationModeExtensions -->
<h3>New Type CoreAnimation.CATextLayerTruncationModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CATextLayerTruncationModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (this CATextLayerTruncationMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CATextLayerTruncationMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CATextLayerTruncationModeExtensions -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGEvent --> <div>
<h3>Type Changed: CoreGraphics.CGEvent</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'Timestamp' instead.")]
	public ulong Timestampe { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ulong Timestamp { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGEvent -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIAreaMaximum --> <div>
<h3>Type Changed: CoreImage.CIAreaMaximum</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMaximum (string name);</span>
</pre>
</div>

</div> <!-- end type CIAreaMaximum -->
<!-- start type CIFilterInputKey --> <div>
<h3>Type Changed: CoreImage.CIFilterInputKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DepthImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisparityImage { get; }</span>
</pre>
</div>

</div> <!-- end type CIFilterInputKey -->
<!-- start type CIImageInitializationOptions --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? ApplyOrientationProperty { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDepth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDisparity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NearestSampling { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIImageInitializationOptions -->
<!-- start type CIImageInitializationOptionsWithMetadata --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptionsWithMetadata</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>

</div> <!-- end type CIImageInitializationOptionsWithMetadata -->
<!-- start type CIMotionBlur --> <div>
<h3>Type Changed: CoreImage.CIMotionBlur</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>CoreImage.CIFilter</span> <span class='added '>CoreImage.CILinearBlur</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public float Radius { get; set; }</span>
</pre>

</div> <!-- end type CIMotionBlur -->
<!-- start type CIVector --> <div>
<h3>Type Changed: CoreImage.CIVector</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIVector (nfloat[] values, nint count);</span>
</pre>
</div>

</div> <!-- end type CIVector -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIAreaMaximum, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Extent { get; set; }</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSAttributedString Text { get; set; }</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIBarcodeDescriptor BarcodeDescriptor { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float AspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float B { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float C { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Scale { get; set; }</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIBlendWithRedMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIBokehBlur : CoreImage.CILinearBlur, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float RingAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float RingSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Softness { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube0Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube1Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float CubeDimension { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage MaskImage { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CurvesData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector CurvesDomain { get; set; }</span>
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
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Aperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVFoundation.AVCameraCalibrationData CalibrationData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector ChinPositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage DisparityImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector FocusRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector LeftEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float LumaNoiseScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector NosePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector RightEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthDisparityConverter -->
<h3>New Type CoreImage.CIDepthDisparityConverter</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIDepthDisparityConverter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthDisparityConverter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthDisparityConverter (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (string name);</span>
}
</pre>
</div> <!-- end type CIDepthDisparityConverter -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIDisparityToDepth : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float LumaSigma { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage SmallImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float SpatialSigma { get; set; }</span>
}
</pre>
</div> <!-- end type CIEdgePreserveUpsampleFilter -->
<div> <!-- start type CIImageGenerator -->
<h3>New Type CoreImage.CIImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageGenerator (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIImageGenerator -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIImage Image2 { get; set; }</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CILinearBlur -->
<h3>New Type CoreImage.CILinearBlur</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CILinearBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILinearBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILinearBlur (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CILinearBlur -->
<div> <!-- start type CIMorphology -->
<h3>New Type CoreImage.CIMorphology</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIMorphology : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphology (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphology (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CIMorphology -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIMorphologyMaximum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CIMorphologyMinimum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
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
public class CITextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FontName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float FontSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Text { get; set; }</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreML --> <div> 
<h2>Namespace CoreML</h2>
<!-- start type MLModelError --> <div>
<h3>Type Changed: CoreML.MLModelError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CustomLayer = 4,</span>
</pre>
</div>

</div> <!-- end type MLModelError -->
<div> <!-- start type IMLCustomLayer -->
<h3>New Type CoreML.IMLCustomLayer</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLCustomLayer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EvaluateOnCpu (MLMultiArray[] inputs, MLMultiArray[] outputs, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSArray[] GetOutputShapes (Foundation.NSArray[] inputShapes, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetWeightData (Foundation.NSData[] weights, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IMLCustomLayer -->
<div> <!-- start type MLCustomLayer_Extensions -->
<h3>New Type CoreML.MLCustomLayer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLCustomLayer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Encode (this IMLCustomLayer This, Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture[] inputs, Metal.IMTLTexture[] outputs, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLCustomLayer_Extensions -->

</div> <!-- end namespace CoreML -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSDictionary --> <div>
<h3>Type Changed: Foundation.NSDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDictionary (NSDictionary other, bool copyItems);</span>
</pre>
</div>

</div> <!-- end type NSDictionary -->
<!-- start type NSMutableDictionary --> <div>
<h3>Type Changed: Foundation.NSMutableDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMutableDictionary (NSDictionary other, bool copyItems);</span>
</pre>
</div>

</div> <!-- end type NSMutableDictionary -->
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: Foundation.NSUrlSessionHandler</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionHandler (NSUrlSessionConfiguration configuration);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->

</div> <!-- end namespace Foundation -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual LABiometryType BiometryType { get; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<div> <!-- start type LABiometryType -->
<h3>New Type LocalAuthentication.LABiometryType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum LABiometryType {
	<span class='added added-field ' data-is-non-breaking="">FaceId = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchId = 1,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Use 'FaceId' instead.")]
	TypeFaceId = 2,</span>
}
</pre>
</div> <!-- end type LABiometryType -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type BlockLiteral --> <div>
<h3>Type Changed: ObjCRuntime.BlockLiteral</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetupBlockUnsafe (System.Delegate trampoline, System.Delegate userDelegate);</span>
</pre>
</div>

</div> <!-- end type BlockLiteral -->
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"4.0.0"</span> <span class='added '>"4.2.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string MetalPerformanceShadersLibrary = "/System/Library/Frameworks/MetalPerformanceShaders.framework/MetalPerformanceShaders";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'SetInt64' for long values instead.")]
	public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, ulong value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfAnnotation --> <div>
<h3>Type Changed: PdfKit.PdfAnnotation</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor InteriorColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StampName { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfAnnotation -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'FrameProcessor2' instead.")]
	public virtual PHLivePhotoFrameProcessingBlock FrameProcessor { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameProcessingBlock2 FrameProcessor2 { get; set; }</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type PHLivePhotoFrameProcessingBlock2 -->
<h3>New Type Photos.PHLivePhotoFrameProcessingBlock2</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHLivePhotoFrameProcessingBlock2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoFrameProcessingBlock2 (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IPHLivePhotoFrame frame, ref Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage EndInvoke (ref Foundation.NSError error, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage Invoke (IPHLivePhotoFrame frame, ref Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameProcessingBlock2 -->

</div> <!-- end namespace Photos -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecCertificate --> <div>
<h3>Type Changed: Security.SecCertificate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetSerialNumber (out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type SecCertificate -->
<!-- start type SecKeyAlgorithm --> <div>
<h3>Type Changed: Security.SecKeyAlgorithm</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha224AesGcm = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha256AesGcm = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha384AesGcm = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha512AesGcm = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha224AesGcm = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha256AesGcm = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha384AesGcm = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha512AesGcm = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha1 = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha224 = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha256 = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha384 = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha512 = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha1 = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha224 = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha256 = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha384 = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha512 = 67,</span>
</pre>
</div>

</div> <!-- end type SecKeyAlgorithm -->
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool PersistentReference { get; set; }</span>
</pre>
</div>

</div> <!-- end type SecRecord -->
<!-- start type SecStatusCode --> <div>
<h3>Type Changed: Security.SecStatusCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MissingEntitlement = -34018,</span>
</pre>
</div>

</div> <!-- end type SecStatusCode -->
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 = 52393,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 = 52392,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->
<!-- start type SslContext --> <div>
<h3>Type Changed: Security.SslContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public int SetError (SecStatusCode status);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetOcspResponse (Foundation.NSData response);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetSessionTickets (bool enabled);</span>
</pre>
</div>

</div> <!-- end type SslContext -->
<!-- start type SslProtocol --> <div>
<h3>Type Changed: Security.SslProtocol</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Tls_1_3 = 10,</span>
</pre>
</div>

</div> <!-- end type SslProtocol -->
<!-- start type SslSessionOption --> <div>
<h3>Type Changed: Security.SslSessionOption</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EnableSessionTickets = 9,</span>
</pre>
</div>

</div> <!-- end type SslSessionOption -->

</div> <!-- end namespace Security -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKProduct --> <div>
<h3>Type Changed: StoreKit.SKProduct</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscount IntroductoryPrice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
</pre>
</div>

</div> <!-- end type SKProduct -->
<div> <!-- start type SKProductDiscount -->
<h3>New Type StoreKit.SKProductDiscount</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductDiscount : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductDiscount ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfPeriods { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscountPaymentMode PaymentMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Price { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSLocale PriceLocale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
}
</pre>
</div> <!-- end type SKProductDiscount -->
<div> <!-- start type SKProductDiscountPaymentMode -->
<h3>New Type StoreKit.SKProductDiscountPaymentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductDiscountPaymentMode {
	<span class='added added-field ' data-is-non-breaking="">FreeTrial = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PayAsYouGo = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PayUpFront = 1,</span>
}
</pre>
</div> <!-- end type SKProductDiscountPaymentMode -->
<div> <!-- start type SKProductPeriodUnit -->
<h3>New Type StoreKit.SKProductPeriodUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductPeriodUnit {
	<span class='added added-field ' data-is-non-breaking="">Day = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Month = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Week = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Year = 3,</span>
}
</pre>
</div> <!-- end type SKProductPeriodUnit -->
<div> <!-- start type SKProductSubscriptionPeriod -->
<h3>New Type StoreKit.SKProductSubscriptionPeriod</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductSubscriptionPeriod : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductSubscriptionPeriod ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfUnits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductPeriodUnit Unit { get; }</span>
}
</pre>
</div> <!-- end type SKProductSubscriptionPeriod -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>New Namespace MetalPerformanceShaders</h2>

<div> <!-- start type IMPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.IMPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSCnnConvolutionDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type IMPSCnnConvolutionDataSource -->
<div> <!-- start type IMPSDeviceProvider -->
<h3>New Type MetalPerformanceShaders.IMPSDeviceProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSDeviceProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLDevice GetMTLDevice ();</span>
}
</pre>
</div> <!-- end type IMPSDeviceProvider -->
<div> <!-- start type IMPSHandle -->
<h3>New Type MetalPerformanceShaders.IMPSHandle</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSHandle : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
}
</pre>
</div> <!-- end type IMPSHandle -->
<div> <!-- start type IMPSImageAllocator -->
<h3>New Type MetalPerformanceShaders.IMPSImageAllocator</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageAllocator : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetImage (Metal.IMTLCommandBuffer cmdBuf, MPSImageDescriptor descriptor, MPSKernel kernel);</span>
}
</pre>
</div> <!-- end type IMPSImageAllocator -->
<div> <!-- start type IMPSImageSizeEncodingState -->
<h3>New Type MetalPerformanceShaders.IMPSImageSizeEncodingState</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageSizeEncodingState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type IMPSImageSizeEncodingState -->
<div> <!-- start type IMPSImageTransformProvider -->
<h3>New Type MetalPerformanceShaders.IMPSImageTransformProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageTransformProvider : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSScaleTransform GetTransform (MPSImage image, IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type IMPSImageTransformProvider -->
<div> <!-- start type IMPSNNPadding -->
<h3>New Type MetalPerformanceShaders.IMPSNNPadding</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSNNPadding : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
}
</pre>
</div> <!-- end type IMPSNNPadding -->
<div> <!-- start type MPSAlphaType -->
<h3>New Type MetalPerformanceShaders.MPSAlphaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSAlphaType {
	<span class='added added-field ' data-is-non-breaking="">AlphaIsOne = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPremultiplied = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Premultiplied = 2,</span>
}
</pre>
</div> <!-- end type MPSAlphaType -->
<div> <!-- start type MPSBinaryImageKernel -->
<h3>New Type MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSBinaryImageKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSBinaryImageKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSBinaryImageKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode PrimaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset PrimaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode SecondaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SecondaryOffset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture primaryTexture, Metal.IMTLTexture secondaryTexture, Metal.IMTLTexture destinationTexture);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture primaryTexture, out Foundation.NSObject inPlaceSecondaryTexture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, out Foundation.NSObject inPlacePrimaryTexture, Metal.IMTLTexture secondaryTexture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion PrimarySourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion SecondarySourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSBinaryImageKernel -->
<div> <!-- start type MPSCnnBinaryConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolution -->
<div> <!-- start type MPSCnnBinaryConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseBetaScaling = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionFlags -->
<div> <!-- start type MPSCnnBinaryConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolutionNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionNode -->
<div> <!-- start type MPSCnnBinaryConvolutionType -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionType {
	<span class='added added-field ' data-is-non-breaking="">And = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BinaryWeights = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Xnor = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionType -->
<div> <!-- start type MPSCnnBinaryFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnected : MetalPerformanceShaders.MPSCnnBinaryConvolution, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnected -->
<div> <!-- start type MPSCnnBinaryFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnectedNode : MetalPerformanceShaders.MPSCnnBinaryConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnectedNode -->
<div> <!-- start type MPSCnnBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode PrimaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset PrimaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode SecondaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SecondaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryKernel -->
<div> <!-- start type MPSCnnConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage, out MPSCnnConvolutionState state);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolution -->
<div> <!-- start type MPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnConvolutionDataSource : Foundation.NSObject, Foundation.INSObjectProtocol, IMPSCnnConvolutionDataSource, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetLookupTableForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRangesForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource -->
<div> <!-- start type MPSCnnConvolutionDataSource_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSCnnConvolutionDataSource_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetLookupTableForUInt8Kernel (this IMPSCnnConvolutionDataSource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetRangesForUInt8Kernel (this IMPSCnnConvolutionDataSource This);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource_Extensions -->
<div> <!-- start type MPSCnnConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SupportsSecureCoding { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor CreateCnnConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor GetConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels, MPSCnnNeuron neuronFilter);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBatchNormalizationParameters (float[] mean, float[] variance, float[] gamma, float[] beta, float epsilon);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData A);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDescriptor -->
<div> <!-- start type MPSCnnConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSCnnConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionFlags -->
<div> <!-- start type MPSCnnConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionStateNode ConvolutionState { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionNode -->
<div> <!-- start type MPSCnnConvolutionState -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, IMPSImageSizeEncodingState, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SourceOffset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionState -->
<div> <!-- start type MPSCnnConvolutionStateNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionStateNode : MetalPerformanceShaders.MPSNNStateNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionStateNode -->
<div> <!-- start type MPSCnnConvolutionTranspose -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTranspose</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTranspose : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSCnnConvolutionState convolutionState);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTranspose -->
<div> <!-- start type MPSCnnConvolutionTransposeNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTransposeNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTransposeNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTransposeNode (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionTransposeNode Create (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTransposeNode -->
<div> <!-- start type MPSCnnCrossChannelNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Metal.IMTLDevice device, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSize { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalization -->
<div> <!-- start type MPSCnnCrossChannelNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSizeInFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnCrossChannelNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalizationNode -->
<div> <!-- start type MPSCnnDepthWiseConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnDepthWiseConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDepthWiseConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDepthWiseConvolutionDescriptor -->
<div> <!-- start type MPSCnnDilatedPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint dilationRateX, uint dilationRateY, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMax -->
<div> <!-- start type MPSCnnDilatedPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY, uint dilationRateX, uint dilationRateY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMaxNode -->
<div> <!-- start type MPSCnnFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnected : MetalPerformanceShaders.MPSCnnConvolution, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnected -->
<div> <!-- start type MPSCnnFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnectedNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnectedNode -->
<div> <!-- start type MPSCnnKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnKernel</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode EdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion GetSourceRegion (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSCnnKernel -->
<div> <!-- start type MPSCnnLocalContrastNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalization -->
<div> <!-- start type MPSCnnLocalContrastNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLocalContrastNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalizationNode -->
<div> <!-- start type MPSCnnLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMax -->
<div> <!-- start type MPSCnnLogSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLogSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMaxNode -->
<div> <!-- start type MPSCnnNeuron -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuron</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnNeuron : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuron -->
<div> <!-- start type MPSCnnNeuronAbsolute -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsolute : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsolute -->
<div> <!-- start type MPSCnnNeuronAbsoluteNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsoluteNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsoluteNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsoluteNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronAbsoluteNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsoluteNode -->
<div> <!-- start type MPSCnnNeuronElu -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronElu</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronElu : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronElu -->
<div> <!-- start type MPSCnnNeuronEluNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronEluNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronEluNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronEluNode -->
<div> <!-- start type MPSCnnNeuronHardSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoid -->
<div> <!-- start type MPSCnnNeuronHardSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoidNode -->
<div> <!-- start type MPSCnnNeuronLinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinear : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinear -->
<div> <!-- start type MPSCnnNeuronLinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinearNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinearNode -->
<div> <!-- start type MPSCnnNeuronNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float C { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronNode -->
<div> <!-- start type MPSCnnNeuronPReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Metal.IMTLDevice device, float[] a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLU -->
<div> <!-- start type MPSCnnNeuronPReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLUNode (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronPReLUNode Create (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLUNode -->
<div> <!-- start type MPSCnnNeuronReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLU -->
<div> <!-- start type MPSCnnNeuronReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLUNode -->
<div> <!-- start type MPSCnnNeuronReLun -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLun</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLun : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLun -->
<div> <!-- start type MPSCnnNeuronReLunNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLunNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLunNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLunNode -->
<div> <!-- start type MPSCnnNeuronSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoid -->
<div> <!-- start type MPSCnnNeuronSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSigmoidNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoidNode -->
<div> <!-- start type MPSCnnNeuronSoftPlus -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlus</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlus : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlus -->
<div> <!-- start type MPSCnnNeuronSoftPlusNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlusNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlusNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlusNode -->
<div> <!-- start type MPSCnnNeuronSoftSign -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSign</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSign : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSign -->
<div> <!-- start type MPSCnnNeuronSoftSignNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSignNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSignNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSignNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftSignNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSignNode -->
<div> <!-- start type MPSCnnNeuronTanH -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanH : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanH -->
<div> <!-- start type MPSCnnNeuronTanHNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanHNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanHNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanHNode -->
<div> <!-- start type MPSCnnNeuronType -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnNeuronType {
	<span class='added added-field ' data-is-non-breaking="">Absolute = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Elu = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HardSigmoid = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PReLU = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLU = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLun = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Sigmoid = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftPlus = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftSign = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TanH = 5,</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronType -->
<div> <!-- start type MPSCnnNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNormalizationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNormalizationNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNormalizationNode -->
<div> <!-- start type MPSCnnPooling -->
<h3>New Type MetalPerformanceShaders.MPSCnnPooling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPooling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint StrideInPixelsY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPooling -->
<div> <!-- start type MPSCnnPoolingAverage -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverage : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeY { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverage -->
<div> <!-- start type MPSCnnPoolingAverageNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverageNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverageNode -->
<div> <!-- start type MPSCnnPoolingL2Norm -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2Norm</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2Norm : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2Norm -->
<div> <!-- start type MPSCnnPoolingL2NormNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2NormNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2NormNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2NormNode -->
<div> <!-- start type MPSCnnPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMax -->
<div> <!-- start type MPSCnnPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMaxNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMaxNode -->
<div> <!-- start type MPSCnnPoolingNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size, uint stride);</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingNode -->
<div> <!-- start type MPSCnnSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMax -->
<div> <!-- start type MPSCnnSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMaxNode -->
<div> <!-- start type MPSCnnSpatialNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalization -->
<div> <!-- start type MPSCnnSpatialNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSpatialNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalizationNode -->
<div> <!-- start type MPSCnnSubPixelConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnSubPixelConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSubPixelConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSubPixelConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnSubPixelConvolutionDescriptor -->
<div> <!-- start type MPSCnnUpsampling -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsampling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsampling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsampling -->
<div> <!-- start type MPSCnnUpsamplingBilinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinear : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinear -->
<div> <!-- start type MPSCnnUpsamplingBilinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinearNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinearNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingBilinearNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinearNode -->
<div> <!-- start type MPSCnnUpsamplingNearest -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearest</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearest : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearest -->
<div> <!-- start type MPSCnnUpsamplingNearestNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearestNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearestNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearestNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingNearestNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearestNode -->
<div> <!-- start type MPSCopyAllocator -->
<h3>New Type MetalPerformanceShaders.MPSCopyAllocator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MPSCopyAllocator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCopyAllocator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MPSKernel filter, Foundation.NSObject commandBuffer, Foundation.NSObject sourceTexture, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Invoke (MPSKernel filter, Foundation.NSObject commandBuffer, Foundation.NSObject sourceTexture);</span>
}
</pre>
</div> <!-- end type MPSCopyAllocator -->
<div> <!-- start type MPSDataLayout -->
<h3>New Type MetalPerformanceShaders.MPSDataLayout</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataLayout {
	<span class='added added-field ' data-is-non-breaking="">FeatureChannelsPerHeightPerWidth = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HeightPerWidthPerFeatureChannels = 0,</span>
}
</pre>
</div> <!-- end type MPSDataLayout -->
<div> <!-- start type MPSDataType -->
<h3>New Type MetalPerformanceShaders.MPSDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataType {
	<span class='added added-field ' data-is-non-breaking="">Float16 = 268435472,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 268435488,</span>
	<span class='added added-field ' data-is-non-breaking="">FloatBit = 268435456,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalizedBit = 1073741824,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm1 = 1073741825,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1073741832,</span>
}
</pre>
</div> <!-- end type MPSDataType -->
<div> <!-- start type MPSGRUDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSGRUDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSGRUDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSGRUDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipOutputGates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float GatePnormValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputGateWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSGRUDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSGRUDescriptor -->
<div> <!-- start type MPSImage -->
<h3>New Type MetalPerformanceShaders.MPSImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImage : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLDevice device, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLTexture texture, uint featureChannels);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Precision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture Texture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureType TextureType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSPurgeableState SetPurgeableState (MPSPurgeableState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
}
</pre>
</div> <!-- end type MPSImage -->
<div> <!-- start type MPSImageAdd -->
<h3>New Type MetalPerformanceShaders.MPSImageAdd</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAdd : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAdd -->
<div> <!-- start type MPSImageAreaMax -->
<h3>New Type MetalPerformanceShaders.MPSImageAreaMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAreaMax : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAreaMax -->
<div> <!-- start type MPSImageAreaMin -->
<h3>New Type MetalPerformanceShaders.MPSImageAreaMin</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAreaMin : MetalPerformanceShaders.MPSImageAreaMax, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMin (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAreaMin (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAreaMin -->
<div> <!-- start type MPSImageArithmetic -->
<h3>New Type MetalPerformanceShaders.MPSImageArithmetic</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageArithmetic : MetalPerformanceShaders.MPSBinaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PrimaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize PrimaryStrideInPixels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float SecondaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize SecondaryStrideInPixels { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageArithmetic -->
<div> <!-- start type MPSImageBilinearScale -->
<h3>New Type MetalPerformanceShaders.MPSImageBilinearScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageBilinearScale : MetalPerformanceShaders.MPSImageScale, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageBilinearScale -->
<div> <!-- start type MPSImageBox -->
<h3>New Type MetalPerformanceShaders.MPSImageBox</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageBox : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBox (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBox (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageBox -->
<div> <!-- start type MPSImageConversion -->
<h3>New Type MetalPerformanceShaders.MPSImageConversion</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageConversion : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Metal.IMTLDevice device, MPSAlphaType srcAlpha, MPSAlphaType destAlpha, nfloat[] backgroundColor, CoreGraphics.CGColorConversionInfo conversionInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType DestinationAlpha { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType SourceAlpha { get; }</span>
}
</pre>
</div> <!-- end type MPSImageConversion -->
<div> <!-- start type MPSImageConvolution -->
<h3>New Type MetalPerformanceShaders.MPSImageConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageConvolution : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageConvolution -->
<div> <!-- start type MPSImageCopyToMatrix -->
<h3>New Type MetalPerformanceShaders.MPSImageCopyToMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageCopyToMatrix : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Metal.IMTLDevice device, MPSDataLayout dataLayout);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataLayout DataLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationMatrixBatchIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin DestinationMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSMatrix destinationMatrix);</span>
}
</pre>
</div> <!-- end type MPSImageCopyToMatrix -->
<div> <!-- start type MPSImageDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSImageDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat ChannelFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLCpuCacheMode CpuCacheMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLStorageMode StorageMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels, uint numberOfImages, Metal.MTLTextureUsage usage);</span>
}
</pre>
</div> <!-- end type MPSImageDescriptor -->
<div> <!-- start type MPSImageDilate -->
<h3>New Type MetalPerformanceShaders.MPSImageDilate</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDilate : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDilate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDilate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] values);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImageDilate -->
<div> <!-- start type MPSImageDivide -->
<h3>New Type MetalPerformanceShaders.MPSImageDivide</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDivide : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageDivide -->
<div> <!-- start type MPSImageEdgeMode -->
<h3>New Type MetalPerformanceShaders.MPSImageEdgeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSImageEdgeMode {
	<span class='added added-field ' data-is-non-breaking="">Clamp = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Zero = 0,</span>
}
</pre>
</div> <!-- end type MPSImageEdgeMode -->
<div> <!-- start type MPSImageErode -->
<h3>New Type MetalPerformanceShaders.MPSImageErode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageErode : MetalPerformanceShaders.MPSImageDilate, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageErode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageErode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] values);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageErode -->
<div> <!-- start type MPSImageFeatureChannelFormat -->
<h3>New Type MetalPerformanceShaders.MPSImageFeatureChannelFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSImageFeatureChannelFormat {
	<span class='added added-field ' data-is-non-breaking="">Float16 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm16 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1,</span>
}
</pre>
</div> <!-- end type MPSImageFeatureChannelFormat -->
<div> <!-- start type MPSImageFindKeypoints -->
<h3>New Type MetalPerformanceShaders.MPSImageFindKeypoints</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageFindKeypoints : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Metal.IMTLDevice device, MPSImageKeypointRangeInfo info);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageKeypointRangeInfo KeypointRangeInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.MTLRegion regions, uint numberOfRegions, Metal.IMTLBuffer keypointCountBuffer, uint keypointCountBufferOffset, Metal.IMTLBuffer keypointDataBuffer, uint keypointDataBufferOffset);</span>
}
</pre>
</div> <!-- end type MPSImageFindKeypoints -->
<div> <!-- start type MPSImageGaussianBlur -->
<h3>New Type MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageGaussianBlur : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianBlur (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Metal.IMTLDevice device, float sigma);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Sigma { get; }</span>
}
</pre>
</div> <!-- end type MPSImageGaussianBlur -->
<div> <!-- start type MPSImageGaussianPyramid -->
<h3>New Type MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageGaussianPyramid : MetalPerformanceShaders.MPSImagePyramid, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageGaussianPyramid -->
<div> <!-- start type MPSImageHistogram -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogram</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogram : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogram (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogram (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector4 MinPixelThresholdValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ZeroHistogram { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer histogram, uint histogramOffset);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetHistogramSize (Metal.MTLPixelFormat sourceFormat);</span>
}
</pre>
</div> <!-- end type MPSImageHistogram -->
<div> <!-- start type MPSImageHistogramEqualization -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogramEqualization : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramEqualization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramEqualization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTransformToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer histogram, uint histogramOffset);</span>
}
</pre>
</div> <!-- end type MPSImageHistogramEqualization -->
<div> <!-- start type MPSImageHistogramInfo -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageHistogramInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool HistogramForAlpha;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector4 MaxPixelValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector4 MinPixelValue;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint NumberOfHistogramEntries;</span>
}
</pre>
</div> <!-- end type MPSImageHistogramInfo -->
<div> <!-- start type MPSImageHistogramSpecification -->
<h3>New Type MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageHistogramSpecification : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramSpecification (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageHistogramSpecification (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Metal.IMTLDevice device, ref MPSImageHistogramInfo histogramInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageHistogramInfo HistogramInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTransformToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.IMTLBuffer sourceHistogram, uint sourceHistogramOffset, Metal.IMTLBuffer desiredHistogram, uint desiredHistogramOffset);</span>
}
</pre>
</div> <!-- end type MPSImageHistogramSpecification -->
<div> <!-- start type MPSImageIntegral -->
<h3>New Type MetalPerformanceShaders.MPSImageIntegral</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageIntegral : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegral (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegral (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageIntegral -->
<div> <!-- start type MPSImageIntegralOfSquares -->
<h3>New Type MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageIntegralOfSquares : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegralOfSquares (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageIntegralOfSquares (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageIntegralOfSquares -->
<div> <!-- start type MPSImageKeypointRangeInfo -->
<h3>New Type MetalPerformanceShaders.MPSImageKeypointRangeInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageKeypointRangeInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint MaximumKeypoints;</span>
	<span class='added added-field ' data-is-non-breaking="">public float MinimumThresholdValue;</span>
}
</pre>
</div> <!-- end type MPSImageKeypointRangeInfo -->
<div> <!-- start type MPSImageLanczosScale -->
<h3>New Type MetalPerformanceShaders.MPSImageLanczosScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageLanczosScale : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLanczosScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLanczosScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform? ScaleTransform { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageLanczosScale -->
<div> <!-- start type MPSImageLaplacian -->
<h3>New Type MetalPerformanceShaders.MPSImageLaplacian</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageLaplacian : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageLaplacian -->
<div> <!-- start type MPSImageMedian -->
<h3>New Type MetalPerformanceShaders.MPSImageMedian</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageMedian : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMedian (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMedian (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Metal.IMTLDevice device, uint kernelDiameter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelDiameter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static uint MaxKernelDiameter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static uint MinKernelDiameter { get; }</span>
}
</pre>
</div> <!-- end type MPSImageMedian -->
<div> <!-- start type MPSImageMultiply -->
<h3>New Type MetalPerformanceShaders.MPSImageMultiply</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageMultiply : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageMultiply -->
<div> <!-- start type MPSImagePyramid -->
<h3>New Type MetalPerformanceShaders.MPSImagePyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImagePyramid : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, float centerWeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImagePyramid -->
<div> <!-- start type MPSImageReadWriteParams -->
<h3>New Type MetalPerformanceShaders.MPSImageReadWriteParams</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageReadWriteParams {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint FeatureChannelOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint NumberOfFeatureChannelsToReadWrite;</span>
}
</pre>
</div> <!-- end type MPSImageReadWriteParams -->
<div> <!-- start type MPSImageScale -->
<h3>New Type MetalPerformanceShaders.MPSImageScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageScale : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform ScaleTransform { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageScale -->
<div> <!-- start type MPSImageSobel -->
<h3>New Type MetalPerformanceShaders.MPSImageSobel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageSobel : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSobel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSobel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Metal.IMTLDevice device, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] ColorTransform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageSobel -->
<div> <!-- start type MPSImageStatisticsMean -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMean</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMean : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMean -->
<div> <!-- start type MPSImageStatisticsMeanAndVariance -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMeanAndVariance</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMeanAndVariance : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMeanAndVariance -->
<div> <!-- start type MPSImageStatisticsMinAndMax -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMinAndMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMinAndMax : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMinAndMax -->
<div> <!-- start type MPSImageSubtract -->
<h3>New Type MetalPerformanceShaders.MPSImageSubtract</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageSubtract : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageSubtract -->
<div> <!-- start type MPSImageTent -->
<h3>New Type MetalPerformanceShaders.MPSImageTent</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageTent : MetalPerformanceShaders.MPSImageBox, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageTent -->
<div> <!-- start type MPSImageThresholdBinary -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdBinary : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinary (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Metal.IMTLDevice device, float thresholdValue, float maximumValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdBinary -->
<div> <!-- start type MPSImageThresholdBinaryInverse -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdBinaryInverse : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinaryInverse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdBinaryInverse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Metal.IMTLDevice device, float thresholdValue, float maximumValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdBinaryInverse -->
<div> <!-- start type MPSImageThresholdToZero -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdToZero : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZero (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZero (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdToZero -->
<div> <!-- start type MPSImageThresholdToZeroInverse -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdToZeroInverse : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZeroInverse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdToZeroInverse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdToZeroInverse -->
<div> <!-- start type MPSImageThresholdTruncate -->
<h3>New Type MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageThresholdTruncate : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdTruncate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageThresholdTruncate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Metal.IMTLDevice device, float thresholdValue, float[] transform);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ThresholdValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float[] Transform { get; }</span>
}
</pre>
</div> <!-- end type MPSImageThresholdTruncate -->
<div> <!-- start type MPSImageTranspose -->
<h3>New Type MetalPerformanceShaders.MPSImageTranspose</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageTranspose : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTranspose (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageTranspose (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageTranspose -->
<div> <!-- start type MPSKernel -->
<h3>New Type MetalPerformanceShaders.MPSKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSKernel : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSKernelOptions Options { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Metal.MTLRegion RectNoClip { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSKernel CopyWithZone (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Supports (Metal.IMTLDevice device);</span>
}
</pre>
</div> <!-- end type MPSKernel -->
<div> <!-- start type MPSKernelOptions -->
<h3>New Type MetalPerformanceShaders.MPSKernelOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSKernelOptions {
	<span class='added added-field ' data-is-non-breaking="">MPSKernelOptionsAllowReducedPrecision = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SkipApiValidation = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Verbose = 16,</span>
}
</pre>
</div> <!-- end type MPSKernelOptions -->
<div> <!-- start type MPSLSTMDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSLSTMDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSLSTMDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSLSTMDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreMemoryWeightsDiagonal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamA { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamB { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamC { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType CellToOutputNeuronType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSLSTMDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSLSTMDescriptor -->
<div> <!-- start type MPSMatrix -->
<h3>New Type MetalPerformanceShaders.MPSMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrix : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrix (Metal.IMTLBuffer buffer, MPSMatrixDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrix -->
<div> <!-- start type MPSMatrixBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin PrimarySourceMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SecondarySourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixBinaryKernel -->
<div> <!-- start type MPSMatrixCopy -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopy</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopy : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Metal.IMTLDevice device, uint copyRows, uint copyColumns, bool areSourcesTransposed, bool areDestinationsTransposed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreDestinationsTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreSourcesTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyColumns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyRows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer cmdBuf, MPSMatrixCopyDescriptor copyDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixCopyDescriptor copyDescriptor, MPSVector rowPermuteIndices, uint rowPermuteOffset, MPSVector columnPermuteIndices, uint columnPermuteOffset);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopy -->
<div> <!-- start type MPSMatrixCopyDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopyDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (Metal.IMTLDevice device, uint count);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSVector offsets, uint byteOffset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixCopyDescriptor Create (MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCopyOperation (uint index, MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyDescriptor -->
<div> <!-- start type MPSMatrixCopyOffsets -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyOffsets</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSMatrixCopyOffsets {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationRowOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceRowOffset;</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyOffsets -->
<div> <!-- start type MPSMatrixDecompositionCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionCholesky : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device, bool lower, uint order);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionCholesky -->
<div> <!-- start type MPSMatrixDecompositionLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionLU : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device, uint rows, uint columns);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, MPSMatrix pivotIndices, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionLU -->
<div> <!-- start type MPSMatrixDecompositionStatus -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSMatrixDecompositionStatus {
	<span class='added added-field ' data-is-non-breaking="">Failure = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPositiveDefinite = -3,</span>
	<span class='added added-field ' data-is-non-breaking="">Singular = -2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionStatus -->
<div> <!-- start type MPSMatrixDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor Create (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint matrices, uint rowBytes, uint matrixBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesForColumns (uint columns, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesFromColumns (uint columns, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSMatrixDescriptor -->
<div> <!-- start type MPSMatrixFindTopK -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFindTopK</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFindTopK : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Metal.IMTLDevice device, uint numberOfTopKValues);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfTopKValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFindTopK Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultIndexMatrix, MPSMatrix resultValueMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixFindTopK -->
<div> <!-- start type MPSMatrixFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFullyConnected : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceOutputFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFullyConnected Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix weightMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixFullyConnected -->
<div> <!-- start type MPSMatrixLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixLogSoftMax : MetalPerformanceShaders.MPSMatrixSoftMax, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrixLogSoftMax -->
<div> <!-- start type MPSMatrixMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixMultiplication : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, uint resultRows, uint resultColumns, uint interiorColumns);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, bool transposeLeft, bool transposeRight, uint resultRows, uint resultColumns, uint interiorColumns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin LeftMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin RightMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix leftMatrix, MPSMatrix rightMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixMultiplication -->
<div> <!-- start type MPSMatrixNeuron -->
<h3>New Type MetalPerformanceShaders.MPSMatrixNeuron</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixNeuron : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixNeuron Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData parametersA);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixNeuron -->
<div> <!-- start type MPSMatrixSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSoftMax : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixSoftMax Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSoftMax -->
<div> <!-- start type MPSMatrixSolveCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveCholesky : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device, bool upper, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveCholesky -->
<div> <!-- start type MPSMatrixSolveLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveLU : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device, bool transpose, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix pivotIndices, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveLU -->
<div> <!-- start type MPSMatrixSolveTriangular -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveTriangular</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveTriangular : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device, bool right, bool upper, bool transpose, bool unit, uint order, uint numberOfRightHandSides, double alpha);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveTriangular -->
<div> <!-- start type MPSMatrixSum -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSum</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSum : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Metal.IMTLDevice device, uint count, uint rows, uint columns, bool transpose);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Transpose { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer buffer, MPSMatrix[] sourceMatrices, MPSMatrix resultMatrix, MPSVector scaleVector, MPSVector offsetVector, MPSVector biasVector, uint startIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixSum -->
<div> <!-- start type MPSMatrixUnaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixUnaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixUnaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixUnaryKernel -->
<div> <!-- start type MPSMatrixVectorMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixVectorMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixVectorMultiplication : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, uint rows, uint columns);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, bool transpose, uint rows, uint columns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector inputVector, MPSVector resultVector);</span>
}
</pre>
</div> <!-- end type MPSMatrixVectorMultiplication -->
<div> <!-- start type MPSNNAdditionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNAdditionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNAdditionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNAdditionNode -->
<div> <!-- start type MPSNNBilinearScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBilinearScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBilinearScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNBilinearScaleNode -->
<div> <!-- start type MPSNNBinaryArithmeticNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBinaryArithmeticNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBinaryArithmeticNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode left, MPSNNImageNode right);</span>
}
</pre>
</div> <!-- end type MPSNNBinaryArithmeticNode -->
<div> <!-- start type MPSNNConcatenationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNConcatenationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNConcatenationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNConcatenationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNConcatenationNode Create (MPSNNImageNode[] sourceNodes);</span>
}
</pre>
</div> <!-- end type MPSNNConcatenationNode -->
<div> <!-- start type MPSNNDefaultPadding -->
<h3>New Type MetalPerformanceShaders.MPSNNDefaultPadding</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDefaultPadding : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IMPSNNPadding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDefaultPadding (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding Create (MPSNNPaddingMethod method);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding CreatePaddingForTensorflowAveragePooling ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImageDescriptor GetDestinationImageDescriptor (MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetLabel ();</span>
}
</pre>
</div> <!-- end type MPSNNDefaultPadding -->
<div> <!-- start type MPSNNDivisionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNDivisionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDivisionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNDivisionNode -->
<div> <!-- start type MPSNNFilterNode -->
<h3>New Type MetalPerformanceShaders.MPSNNFilterNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNFilterNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding PaddingPolicy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNImageNode ResultImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode ResultState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode[] ResultStates { get; }</span>
}
</pre>
</div> <!-- end type MPSNNFilterNode -->
<div> <!-- start type MPSNNGraph -->
<h3>New Type MetalPerformanceShaders.MPSNNGraph</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNGraph : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Metal.IMTLDevice device, MPSNNImageNode resultImage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] IntermediateImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOutputStateTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle ResultHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] ResultStateHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceStateHandles { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSState[] sourceStates, Foundation.NSMutableArray&lt;MPSImage&gt; intermediateImages, Foundation.NSMutableArray&lt;MPSState&gt; destinationStates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage Execute (MPSImage[] sourceImages, System.Action&lt;MPSImage,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages, out MPSImage result);</span>
}
</pre>
</div> <!-- end type MPSNNGraph -->
<div> <!-- start type MPSNNImageNode -->
<h3>New Type MetalPerformanceShaders.MPSNNImageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNImageNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNImageNode (IMPSHandle handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExportFromGraph { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat Format { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator ImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode Create (IMPSHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode GetExportedNode (IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type MPSNNImageNode -->
<div> <!-- start type MPSNNLanczosScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNLanczosScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNLanczosScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNLanczosScaleNode -->
<div> <!-- start type MPSNNMultiplicationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNMultiplicationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNMultiplicationNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNMultiplicationNode -->
<div> <!-- start type MPSNNPaddingMethod -->
<h3>New Type MetalPerformanceShaders.MPSNNPaddingMethod</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSNNPaddingMethod {
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomLeft = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomRight = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopLeft = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignBottomRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignCentered = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignReserved = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignTopLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 16384,</span>
	<span class='added added-field ' data-is-non-breaking="">ExcludeEdges = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeFull = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeMask = 2032,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeReserved = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeSame = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeValidOnly = 0,</span>
}
</pre>
</div> <!-- end type MPSNNPaddingMethod -->
<div> <!-- start type MPSNNPadding_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSNNPadding_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSNNPadding_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetDestinationImageDescriptor (this IMPSNNPadding This, MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetLabel (this IMPSNNPadding This);</span>
}
</pre>
</div> <!-- end type MPSNNPadding_Extensions -->
<div> <!-- start type MPSNNScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNScaleNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
}
</pre>
</div> <!-- end type MPSNNScaleNode -->
<div> <!-- start type MPSNNStateNode -->
<h3>New Type MetalPerformanceShaders.MPSNNStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNStateNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
}
</pre>
</div> <!-- end type MPSNNStateNode -->
<div> <!-- start type MPSNNSubtractionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNSubtractionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNSubtractionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNSubtractionNode -->
<div> <!-- start type MPSOffset -->
<h3>New Type MetalPerformanceShaders.MPSOffset</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSOffset {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public nint X;</span>
	<span class='added added-field ' data-is-non-breaking="">public nint Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public nint Z;</span>
}
</pre>
</div> <!-- end type MPSOffset -->
<div> <!-- start type MPSOrigin -->
<h3>New Type MetalPerformanceShaders.MPSOrigin</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSOrigin {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double X;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Z;</span>
}
</pre>
</div> <!-- end type MPSOrigin -->
<div> <!-- start type MPSPurgeableState -->
<h3>New Type MetalPerformanceShaders.MPSPurgeableState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSPurgeableState {
	<span class='added added-field ' data-is-non-breaking="">AllocationDeferred = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Empty = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">KeepCurrent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonVolatile = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Volatile = 3,</span>
}
</pre>
</div> <!-- end type MPSPurgeableState -->
<div> <!-- start type MPSRegion -->
<h3>New Type MetalPerformanceShaders.MPSRegion</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSRegion {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public MPSOrigin Origin;</span>
	<span class='added added-field ' data-is-non-breaking="">public MPSSize Size;</span>
}
</pre>
</div> <!-- end type MPSRegion -->
<div> <!-- start type MPSRnnBidirectionalCombineMode -->
<h3>New Type MetalPerformanceShaders.MPSRnnBidirectionalCombineMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnBidirectionalCombineMode {
	<span class='added added-field ' data-is-non-breaking="">Add = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Concatenate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnBidirectionalCombineMode -->
<div> <!-- start type MPSRnnDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnSequenceDirection LayerSequenceDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseFloat32Weights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseLayerInputUnitTransformMode { get; set; }</span>
}
</pre>
</div> <!-- end type MPSRnnDescriptor -->
<div> <!-- start type MPSRnnImageInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnImageInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnImageInferenceLayer : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnImageInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceSequence, MPSImage[] destinationForwardImages, MPSImage[] destinationBackwardImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSImage[] destinationImages, MPSRnnRecurrentImageState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentImageState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnImageInferenceLayer -->
<div> <!-- start type MPSRnnMatrixInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnMatrixInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnMatrixInferenceLayer : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnMatrixInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceSequence, MPSMatrix[] destinationForwardMatrices, MPSMatrix[] destinationBackwardMatrices);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSRnnRecurrentMatrixState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentMatrixState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnMatrixInferenceLayer -->
<div> <!-- start type MPSRnnRecurrentImageState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentImageState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentImageState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetMemoryCellImage (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetRecurrentOutputImage (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentImageState -->
<div> <!-- start type MPSRnnRecurrentMatrixState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentMatrixState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentMatrixState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetMemoryCellMatrix (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetRecurrentOutputMatrix (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentMatrixState -->
<div> <!-- start type MPSRnnSequenceDirection -->
<h3>New Type MetalPerformanceShaders.MPSRnnSequenceDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnSequenceDirection {
	<span class='added added-field ' data-is-non-breaking="">Backward = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Forward = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnSequenceDirection -->
<div> <!-- start type MPSRnnSingleGateDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnSingleGateDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnSingleGateDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnSingleGateDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSRnnSingleGateDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSRnnSingleGateDescriptor -->
<div> <!-- start type MPSScaleTransform -->
<h3>New Type MetalPerformanceShaders.MPSScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSScaleTransform {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double ScaleX;</span>
	<span class='added added-field ' data-is-non-breaking="">public double ScaleY;</span>
	<span class='added added-field ' data-is-non-breaking="">public double TranslateX;</span>
	<span class='added added-field ' data-is-non-breaking="">public double TranslateY;</span>
}
</pre>
</div> <!-- end type MPSScaleTransform -->
<div> <!-- start type MPSSize -->
<h3>New Type MetalPerformanceShaders.MPSSize</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSSize {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double Depth;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Height;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Width;</span>
}
</pre>
</div> <!-- end type MPSSize -->
<div> <!-- start type MPSState -->
<h3>New Type MetalPerformanceShaders.MPSState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSState : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsTemporary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
}
</pre>
</div> <!-- end type MPSState -->
<div> <!-- start type MPSTemporaryImage -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryImage : MetalPerformanceShaders.MPSImage, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, Metal.MTLTextureDescriptor textureDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryImage -->
<div> <!-- start type MPSTemporaryMatrix -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryMatrix : MetalPerformanceShaders.MPSMatrix, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryMatrix Create (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor matrixDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryMatrix -->
<div> <!-- start type MPSTemporaryVector -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryVector : MetalPerformanceShaders.MPSVector, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryVector Create (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryVector -->
<div> <!-- start type MPSUnaryImageKernel -->
<h3>New Type MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSUnaryImageKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSUnaryImageKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSUnaryImageKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode EdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset Offset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture sourceTexture, Metal.IMTLTexture destinationTexture);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, out Foundation.NSObject texture, MPSCopyAllocator copyAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion SourceRegionForDestinationSize (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSUnaryImageKernel -->
<div> <!-- start type MPSVector -->
<h3>New Type MetalPerformanceShaders.MPSVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVector : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSVector (Metal.IMTLBuffer buffer, MPSVectorDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
}
</pre>
</div> <!-- end type MPSVector -->
<div> <!-- start type MPSVectorDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSVectorDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVectorDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, uint vectors, uint vectorBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetVectorBytes (uint length, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSVectorDescriptor -->
</div> <!-- end namespace MetalPerformanceShaders -->

</div>



   


 <hr>
