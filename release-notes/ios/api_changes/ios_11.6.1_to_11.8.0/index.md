---
id: E4FEC771-926E-427A-B6F5-B6894484234D
title: "iOS 11.6.1 to 11.8.0"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.iOS/mscorlib.html)

   


 [System.Core.dll](#diff/xi/Xamarin.iOS/System.Core.html)

   


 [Mono.Security.dll](#diff/xi/Xamarin.iOS/Mono.Security.html)

   


 [System.Net.Http.dll](#diff/xi/Xamarin.iOS/System.Net.Http.html)

   


 [Xamarin.iOS.dll](#diff/xi/Xamarin.iOS/Xamarin.iOS.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.iOS/mscorlib.html'>mscorlib.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Core.html'>System.Core.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/Mono.Security.html'>Mono.Security.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.iOS/System.Net.Http.html'>System.Net.Http.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Net.Http --> <div> 
<h2>Namespace System.Net.Http</h2>
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: System.Net.Http.NSUrlSessionHandler</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionHandler (Foundation.NSUrlSessionConfiguration configuration);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->

</div> <!-- end namespace System.Net.Http -->
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
</script><h1 id='diff/xi/Xamarin.iOS/Xamarin.iOS.html'>Xamarin.iOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace ARKit --> <div> 
<h2>Namespace ARKit</h2>
<!-- start type ARFaceGeometry --> <div>
<h3>Type Changed: ARKit.ARFaceGeometry</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetTextureCoordinates' method instead.")]
	public virtual OpenTK.Vector2 TextureCoordinates { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetTriangleIndices' method instead.")]
	public virtual short TriangleIndices { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetVertices' method instead.")]
	public virtual OpenTK.NVector3 Vertices { get; }</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawVertices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.Vector2[] GetTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public short[] GetTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.NVector3[] GetVertices ();</span>
</pre>
</div>

</div> <!-- end type ARFaceGeometry -->

</div> <!-- end namespace ARKit -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
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

</div> <!-- end namespace Foundation -->
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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.6.1"</span> <span class='added '>"11.8.0"</span>;
</div></pre>

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
<!-- start type SecSharedCredential --> <div>
<h3>Type Changed: Security.SecSharedCredential</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload accepting a 'SecSharedCredentialInfo' argument.")]
	public static void RequestSharedWebCredential (string domainName, string account, System.Action&lt;System.String[],Foundation.NSError&gt; handler);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestSharedWebCredential (string domainName, string account, System.Action&lt;SecSharedCredentialInfo[],Foundation.NSError&gt; handler);</span>
</pre>
</div>

</div> <!-- end type SecSharedCredential -->
<div> <!-- start type SecSharedCredentialInfo -->
<h3>New Type Security.SecSharedCredentialInfo</h3>
<pre class='added' data-is-non-breaking="">
public class SecSharedCredentialInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SecSharedCredentialInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecSharedCredentialInfo (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Account { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Password { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? Port { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Server { get; set; }</span>
}
</pre>
</div> <!-- end type SecSharedCredentialInfo -->

</div> <!-- end namespace Security -->
</div>



   


 <hr>
