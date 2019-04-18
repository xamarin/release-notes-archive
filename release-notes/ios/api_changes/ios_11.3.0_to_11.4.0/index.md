---
id: 94F5C387-364B-49C9-A3BF-AC81674CA70A
title: "iOS 11.3.0 to 11.4.0"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.iOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.iOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.iOS/System.Core.html)

   


 [System.IO.Compression.dll](#diff/xi/Xamarin.iOS/System.IO.Compression.html)

   


 [Mono.Security.dll](#diff/xi/Xamarin.iOS/Mono.Security.html)

   


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
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type Exception --> <div>
<h3>Type Changed: System.Exception</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> Exception InnerException { get; }
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> Reflection.MethodBase TargetSite { get; }
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> Type GetType ()
</div></pre>

</div> <!-- end type Exception -->

</div> <!-- end namespace System -->
<!-- start namespace System.Collections --> <div> 
<h2>Namespace System.Collections</h2>
<!-- start type DictionaryEntry --> <div>
<h3>Type Changed: System.Collections.DictionaryEntry</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Deconstruct (object key, object value);</span>
</pre>
</div>

</div> <!-- end type DictionaryEntry -->

</div> <!-- end namespace System.Collections -->
<!-- start namespace System.Collections.Generic --> <div> 
<h2>Namespace System.Collections.Generic</h2>
<!-- start type Dictionary`2 --> <div>
<h3>Type Changed: System.Collections.Generic.Dictionary`2</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public TValue GetValueOrDefault (TKey key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public TValue GetValueOrDefault (TKey key, TValue defaultValue);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Remove (TKey key, TValue value);</span>
</pre>
</div>

</div> <!-- end type Dictionary`2 -->
<!-- start type KeyValuePair`2 --> <div>
<h3>Type Changed: System.Collections.Generic.KeyValuePair`2</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Deconstruct (TKey key, TValue value);</span>
</pre>
</div>

</div> <!-- end type KeyValuePair`2 -->
<div> <!-- start type CollectionExtensions -->
<h3>New Type System.Collections.Generic.CollectionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CollectionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static TValue GetValueOrDefault&lt;TKey, TValue&gt; (System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt; dictionary, TKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static TValue GetValueOrDefault&lt;TKey, TValue&gt; (System.Collections.Generic.IReadOnlyDictionary&lt;TKey,TValue&gt; dictionary, TKey key, TValue defaultValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Remove&lt;TKey, TValue&gt; (System.Collections.Generic.IDictionary&lt;TKey,TValue&gt; dictionary, TKey key, TValue value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryAdd&lt;TKey, TValue&gt; (System.Collections.Generic.IDictionary&lt;TKey,TValue&gt; dictionary, TKey key, TValue value);</span>
}
</pre>
</div> <!-- end type CollectionExtensions -->
<div> <!-- start type KeyValuePair -->
<h3>New Type System.Collections.Generic.KeyValuePair</h3>
<pre class='added' data-is-non-breaking="">
public static class KeyValuePair {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.KeyValuePair&lt;TKey,TValue&gt; Create&lt;TKey, TValue&gt; (TKey key, TValue value);</span>
}
</pre>
</div> <!-- end type KeyValuePair -->

</div> <!-- end namespace System.Collections.Generic -->
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<!-- start type EventListener --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventListener</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>public</span> EventListener ()
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	protected <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> void OnEventWritten (EventWrittenEventArgs eventData)
</div></pre>

</div> <!-- end type EventListener -->

</div> <!-- end namespace System.Diagnostics.Tracing -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<div> <!-- start type IsByRefLikeAttribute -->
<h3>New Type System.Runtime.CompilerServices.IsByRefLikeAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class IsByRefLikeAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IsByRefLikeAttribute ();</span>
}
</pre>
</div> <!-- end type IsByRefLikeAttribute -->
<div> <!-- start type IsReadOnlyAttribute -->
<h3>New Type System.Runtime.CompilerServices.IsReadOnlyAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class IsReadOnlyAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IsReadOnlyAttribute ();</span>
}
</pre>
</div> <!-- end type IsReadOnlyAttribute -->
<div> <!-- start type RuntimeFeature -->
<h3>New Type System.Runtime.CompilerServices.RuntimeFeature</h3>
<pre class='added' data-is-non-breaking="">
public static class RuntimeFeature {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const string PortablePdb = "PortablePdb";</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSupported (string feature);</span>
}
</pre>
</div> <!-- end type RuntimeFeature -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Runtime.ExceptionServices --> <div> 
<h2>Namespace System.Runtime.ExceptionServices</h2>
<!-- start type ExceptionDispatchInfo --> <div>
<h3>Type Changed: System.Runtime.ExceptionServices.ExceptionDispatchInfo</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Throw (System.Exception source);</span>
</pre>
</div>

</div> <!-- end type ExceptionDispatchInfo -->

</div> <!-- end namespace System.Runtime.ExceptionServices -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<div> <!-- start type EXCEPINFO -->
<h3>New Type System.Runtime.InteropServices.EXCEPINFO</h3>
<pre class='added' data-is-non-breaking="">
public struct EXCEPINFO {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public string bstrDescription;</span>
	<span class='added added-field ' data-is-non-breaking="">public string bstrHelpFile;</span>
	<span class='added added-field ' data-is-non-breaking="">public string bstrSource;</span>
	<span class='added added-field ' data-is-non-breaking="">public int dwHelpContext;</span>
	<span class='added added-field ' data-is-non-breaking="">public IntPtr pfnDeferredFillIn;</span>
	<span class='added added-field ' data-is-non-breaking="">public IntPtr pvReserved;</span>
	<span class='added added-field ' data-is-non-breaking="">public short wCode;</span>
	<span class='added added-field ' data-is-non-breaking="">public short wReserved;</span>
}
</pre>
</div> <!-- end type EXCEPINFO -->

</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Security.Policy --> <div> 
<h2>Namespace System.Security.Policy</h2>
<!-- start type PolicyException --> <div>
<h3>Type Changed: System.Security.Policy.PolicyException</h3>
<p>Removed interface:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">System.Runtime.InteropServices._Exception</span>
</pre>

</div> <!-- end type PolicyException -->

</div> <!-- end namespace System.Security.Policy -->
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
</script><h1 id='diff/xi/Xamarin.iOS/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Net --> <div> 
<h2>Namespace System.Net</h2>
<!-- start type SecurityProtocolType --> <div>
<h3>Type Changed: System.Net.SecurityProtocolType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SystemDefault = 0,</span>
</pre>
</div>

</div> <!-- end type SecurityProtocolType -->

</div> <!-- end namespace System.Net -->
<!-- start namespace System.Net.Security --> <div> 
<h2>Namespace System.Net.Security</h2>
<!-- start type SslStream --> <div>
<h3>Type Changed: System.Net.Security.SslStream</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> System.Net.TransportContext TransportContext { get; }
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Write (byte[] buffer)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ShutdownAsync ();</span>
</pre>
</div>

</div> <!-- end type SslStream -->

</div> <!-- end namespace System.Net.Security -->
<!-- start namespace System.Text.RegularExpressions --> <div> 
<h2>Namespace System.Text.RegularExpressions</h2>
<!-- start type Group --> <div>
<h3>Type Changed: System.Text.RegularExpressions.Group</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
</pre>
</div>

</div> <!-- end type Group -->

</div> <!-- end namespace System.Text.RegularExpressions -->
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
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type ECDiffieHellmanPublicKey --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDiffieHellmanPublicKey</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected ECDiffieHellmanPublicKey ();</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportExplicitParameters ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportParameters ();</span>
</pre>
</div>

</div> <!-- end type ECDiffieHellmanPublicKey -->

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
</script><h1 id='diff/xi/Xamarin.iOS/System.IO.Compression.html'>System.IO.Compression.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type ZipArchiveEntry --> <div>
<h3>Type Changed: System.IO.Compression.ZipArchiveEntry</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int ExternalAttributes { get; set; }</span>
</pre>
</div>

</div> <!-- end type ZipArchiveEntry -->

</div> <!-- end namespace System.IO.Compression -->
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
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property breaking' data-is-breaking="">public virtual System.Net.Security.SslStream SslStream { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task ShutdownAsync ();</span>
</pre>
</div>

</div> <!-- end type IMonoSslStream -->
<!-- start type MonoTlsProviderFactory --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsProviderFactory</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetProvider() instead.")]
	public static MonoTlsProvider GetDefaultProvider ();</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use Initialize(string provider) instead.")]
	public static void SetDefaultProvider (string name);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMonoSslStream GetMonoSslStream (System.Net.HttpListenerContext context);</span>
</pre>
</div>

</div> <!-- end type MonoTlsProviderFactory -->
<!-- start type MonoTlsSettings --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.DateTime? CertificateValidationTime { get; set; }</span>
</pre>
</div>

</div> <!-- end type MonoTlsSettings -->

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
</script><h1 id='diff/xi/Xamarin.iOS/Xamarin.iOS.html'>Xamarin.iOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.3.0"</span> <span class='added '>"11.4.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<div> <!-- start type BindAsAttribute -->
<h3>New Type ObjCRuntime.BindAsAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class BindAsAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public BindAsAttribute (System.Type type);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public System.Type OriginalType;</span>
	<span class='added added-field ' data-is-non-breaking="">public System.Type Type;</span>
}
</pre>
</div> <!-- end type BindAsAttribute -->

</div> <!-- end namespace ObjCRuntime -->
</div>



   


 <hr>
