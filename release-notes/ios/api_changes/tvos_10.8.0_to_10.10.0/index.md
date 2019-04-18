---
id: 707102C9-E3E6-4A54-8663-AABB9E81B510
title: "tvOS 10.8.0 to 10.10.0"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.TVOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.TVOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.TVOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.TVOS/System.Data.html)

   


 [System.IO.Compression.FileSystem.dll](#diff/xi/Xamarin.TVOS/System.IO.Compression.FileSystem.html)

   


 [Mono.Security.dll](#diff/xi/Xamarin.TVOS/Mono.Security.html)

   


 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.TVOS/mscorlib.html'>mscorlib.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type Object --> <div>
<h3>Type Changed: System.Object</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	protected <span class='removed removed-inline '>override</span> <span class='added '>virtual</span> void ~Object ()
</div></pre>

</div> <!-- end type Object -->
<!-- start type Tuple`1 --> <div>
<h3>Type Changed: System.Tuple`1</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`1 -->
<!-- start type Tuple`2 --> <div>
<h3>Type Changed: System.Tuple`2</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`2 -->
<!-- start type Tuple`3 --> <div>
<h3>Type Changed: System.Tuple`3</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`3 -->
<!-- start type Tuple`4 --> <div>
<h3>Type Changed: System.Tuple`4</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`4 -->
<!-- start type Tuple`5 --> <div>
<h3>Type Changed: System.Tuple`5</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`5 -->
<!-- start type Tuple`6 --> <div>
<h3>Type Changed: System.Tuple`6</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`6 -->
<!-- start type Tuple`7 --> <div>
<h3>Type Changed: System.Tuple`7</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`7 -->
<!-- start type Tuple`8 --> <div>
<h3>Type Changed: System.Tuple`8</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Runtime.CompilerServices.ITuple</span>
</pre>
</div>

</div> <!-- end type Tuple`8 -->
<div> <!-- start type TupleExtensions -->
<h3>New Type System.TupleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class TupleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1&gt; (System.Tuple&lt;T1&gt; value, T1 item1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2&gt; (System.Tuple&lt;T1,T2&gt; value, T1 item1, T2 item2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3&gt; (System.Tuple&lt;T1,T2,T3&gt; value, T1 item1, T2 item2, T3 item3);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4&gt; (System.Tuple&lt;T1,T2,T3,T4&gt; value, T1 item1, T2 item2, T3 item3, T4 item4);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5&gt; (System.Tuple&lt;T1,T2,T3,T4,T5&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16, T17 item17);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16, T17 item17, T18 item18);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16, T17 item17, T18 item18, T19 item19);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16, T17 item17, T18 item18, T19 item19, T20 item20);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Deconstruct&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20, T21&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20,T21&gt;&gt;&gt; value, T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8, T9 item9, T10 item10, T11 item11, T12 item12, T13 item13, T14 item14, T15 item15, T16 item16, T17 item17, T18 item18, T19 item19, T20 item20, T21 item21);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1&gt; ToTuple&lt;T1&gt; (System.ValueTuple&lt;T1&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2&gt; ToTuple&lt;T1, T2&gt; (System.ValueTuple&lt;T1,T2&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3&gt; ToTuple&lt;T1, T2, T3&gt; (System.ValueTuple&lt;T1,T2,T3&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4&gt; ToTuple&lt;T1, T2, T3, T4&gt; (System.ValueTuple&lt;T1,T2,T3,T4&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5&gt; ToTuple&lt;T1, T2, T3, T4, T5&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19,T20&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20,T21&gt;&gt;&gt; ToTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20, T21&gt; (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19,T20,T21&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1&gt; ToValueTuple&lt;T1&gt; (System.Tuple&lt;T1&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2&gt; ToValueTuple&lt;T1, T2&gt; (System.Tuple&lt;T1,T2&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3&gt; ToValueTuple&lt;T1, T2, T3&gt; (System.Tuple&lt;T1,T2,T3&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4&gt; ToValueTuple&lt;T1, T2, T3, T4&gt; (System.Tuple&lt;T1,T2,T3,T4&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5&gt; ToValueTuple&lt;T1, T2, T3, T4, T5&gt; (System.Tuple&lt;T1,T2,T3,T4,T5&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19,T20&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20&gt;&gt;&gt; value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8,T9,T10,T11,T12,T13,T14,System.ValueTuple&lt;T15,T16,T17,T18,T19,T20,T21&gt;&gt;&gt; ToValueTuple&lt;T1, T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T16, T17, T18, T19, T20, T21&gt; (System.Tuple&lt;T1,T2,T3,T4,T5,T6,T7,System.Tuple&lt;T8,T9,T10,T11,T12,T13,T14,System.Tuple&lt;T15,T16,T17,T18,T19,T20,T21&gt;&gt;&gt; value);</span>
}
</pre>
</div> <!-- end type TupleExtensions -->
<div> <!-- start type ValueTuple -->
<h3>New Type System.ValueTuple</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;ValueTuple&gt;, System.IEquatable&lt;ValueTuple&gt;, Runtime.CompilerServices.ITuple {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (ValueTuple other);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ValueTuple Create ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1&gt; Create&lt;T1&gt; (T1 item1);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2&gt; Create&lt;T1, T2&gt; (T1 item1, T2 item2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3&gt; Create&lt;T1, T2, T3&gt; (T1 item1, T2 item2, T3 item3);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4&gt; Create&lt;T1, T2, T3, T4&gt; (T1 item1, T2 item2, T3 item3, T4 item4);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5&gt; Create&lt;T1, T2, T3, T4, T5&gt; (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt; Create&lt;T1, T2, T3, T4, T5, T6&gt; (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; Create&lt;T1, T2, T3, T4, T5, T6, T7&gt; (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,System.ValueTuple&lt;T8&gt;&gt; Create&lt;T1, T2, T3, T4, T5, T6, T7, T8&gt; (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, T8 item8);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (ValueTuple other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple -->
<div> <!-- start type ValueTuple`1 -->
<h3>New Type System.ValueTuple`1</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`1, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`1 (T1 item1);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`1 -->
<div> <!-- start type ValueTuple`2 -->
<h3>New Type System.ValueTuple`2</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`2, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`2 (T1 item1, T2 item2);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`2 -->
<div> <!-- start type ValueTuple`3 -->
<h3>New Type System.ValueTuple`3</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`3, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`3 (T1 item1, T2 item2, T3 item3);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`3 -->
<div> <!-- start type ValueTuple`4 -->
<h3>New Type System.ValueTuple`4</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`4, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3,T4&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3,T4&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`4 (T1 item1, T2 item2, T3 item3, T4 item4);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	<span class='added added-field ' data-is-non-breaking="">public T4 Item4;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3,T4&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3,T4&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`4 -->
<div> <!-- start type ValueTuple`5 -->
<h3>New Type System.ValueTuple`5</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`5, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`5 (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	<span class='added added-field ' data-is-non-breaking="">public T4 Item4;</span>
	<span class='added added-field ' data-is-non-breaking="">public T5 Item5;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3,T4,T5&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3,T4,T5&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`5 -->
<div> <!-- start type ValueTuple`6 -->
<h3>New Type System.ValueTuple`6</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`6, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`6 (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	<span class='added added-field ' data-is-non-breaking="">public T4 Item4;</span>
	<span class='added added-field ' data-is-non-breaking="">public T5 Item5;</span>
	<span class='added added-field ' data-is-non-breaking="">public T6 Item6;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`6 -->
<div> <!-- start type ValueTuple`7 -->
<h3>New Type System.ValueTuple`7</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`7, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`7 (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	<span class='added added-field ' data-is-non-breaking="">public T4 Item4;</span>
	<span class='added added-field ' data-is-non-breaking="">public T5 Item5;</span>
	<span class='added added-field ' data-is-non-breaking="">public T6 Item6;</span>
	<span class='added added-field ' data-is-non-breaking="">public T7 Item7;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`7 -->
<div> <!-- start type ValueTuple`8 -->
<h3>New Type System.ValueTuple`8</h3>
<pre class='added' data-is-non-breaking="">
public struct ValueTuple`8, Collections.IStructuralComparable, Collections.IStructuralEquatable, IComparable, System.IComparable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,TRest&gt;&gt;, System.IEquatable&lt;System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,TRest&gt;&gt;, Runtime.CompilerServices.ITuple {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValueTuple`8 (T1 item1, T2 item2, T3 item3, T4 item4, T5 item5, T6 item6, T7 item7, TRest rest);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public T1 Item1;</span>
	<span class='added added-field ' data-is-non-breaking="">public T2 Item2;</span>
	<span class='added added-field ' data-is-non-breaking="">public T3 Item3;</span>
	<span class='added added-field ' data-is-non-breaking="">public T4 Item4;</span>
	<span class='added added-field ' data-is-non-breaking="">public T5 Item5;</span>
	<span class='added added-field ' data-is-non-breaking="">public T6 Item6;</span>
	<span class='added added-field ' data-is-non-breaking="">public T7 Item7;</span>
	<span class='added added-field ' data-is-non-breaking="">public TRest Rest;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual int CompareTo (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,TRest&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (System.ValueTuple&lt;T1,T2,T3,T4,T5,T6,T7,TRest&gt; other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type ValueTuple`8 -->

</div> <!-- end namespace System -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type RuntimeHelpers --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.RuntimeHelpers</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryEnsureSufficientExecutionStack ();</span>
</pre>
</div>

</div> <!-- end type RuntimeHelpers -->
<div> <!-- start type ITuple -->
<h3>New Type System.Runtime.CompilerServices.ITuple</h3>
<pre class='added' data-is-non-breaking="">
public interface ITuple {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual object Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Length { get; }</span>
}
</pre>
</div> <!-- end type ITuple -->
<div> <!-- start type TupleElementNamesAttribute -->
<h3>New Type System.Runtime.CompilerServices.TupleElementNamesAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class TupleElementNamesAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TupleElementNamesAttribute (string[] transformNames);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IList&lt;string&gt; TransformNames { get; }</span>
}
</pre>
</div> <!-- end type TupleElementNamesAttribute -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<!-- start type Marshal --> <div>
<h3>Type Changed: System.Runtime.InteropServices.Marshal</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string PtrToStringUTF8 (IntPtr ptr);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string PtrToStringUTF8 (IntPtr ptr, int byteLen);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr StringToAllocatedMemoryUTF8 (string s);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ZeroFreeCoTaskMemUTF8 (IntPtr s);</span>
</pre>
</div>

</div> <!-- end type Marshal -->
<!-- start type UnmanagedType --> <div>
<h3>Type Changed: System.Runtime.InteropServices.UnmanagedType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LPUTF8Str = 48,</span>
</pre>
</div>

</div> <!-- end type UnmanagedType -->

</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type DSACryptoServiceProvider --> <div>
<h3>Type Changed: System.Security.Cryptography.DSACryptoServiceProvider</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashData (System.IO.Stream data, HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashData (byte[] data, int offset, int count, HashAlgorithmName hashAlgorithm);</span>
</pre>
</div>

</div> <!-- end type DSACryptoServiceProvider -->
<h3>Removed Type <span class='breaking' data-is-breaking="">System.Security.Cryptography.IncrementalHash</span></h3>
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
</script><h1 id='diff/xi/Xamarin.TVOS/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type FileSystemWatcher --> <div>
<h3>Type Changed: System.IO.FileSystemWatcher</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Dispose ();</span>
</pre>

</div> <!-- end type FileSystemWatcher -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type GZipStream --> <div>
<h3>Type Changed: System.IO.Compression.GZipStream</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public override System.IAsyncResult BeginRead (byte[] <span class='removed removed-inline removed-breaking-inline'>buffer</span> <span class='added '>array</span>, int offset, int count, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>cback</span> <span class='added '>asyncCallback</span>, object <span class='removed removed-inline removed-breaking-inline'>state</span> <span class='added '>asyncState</span>)
</div><div data-is-breaking="">	public override System.IAsyncResult BeginWrite (byte[] <span class='removed removed-inline removed-breaking-inline'>buffer</span> <span class='added '>array</span>, int offset, int count, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>cback</span> <span class='added '>asyncCallback</span>, object <span class='removed removed-inline removed-breaking-inline'>state</span> <span class='added '>asyncState</span>)
</div><div data-is-breaking="">	public override int EndRead (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>async_result</span> <span class='added '>asyncResult</span>)
</div><div data-is-breaking="">	public override void EndWrite (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>async_result</span> <span class='added '>asyncResult</span>)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task CopyToAsync (System.IO.Stream destination, int bufferSize, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task FlushAsync (System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task&lt;int&gt; ReadAsync (byte[] array, int offset, int count, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int ReadByte ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Threading.Tasks.Task WriteAsync (byte[] array, int offset, int count, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type GZipStream -->

</div> <!-- end namespace System.IO.Compression -->
<!-- start namespace System.Net.Sockets --> <div> 
<h2>Namespace System.Net.Sockets</h2>
<!-- start type Socket --> <div>
<h3>Type Changed: System.Net.Sockets.Socket</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public System.IAsyncResult BeginConnect (System.Net.IPAddress address, int port, System.AsyncCallback <span class='removed removed-inline removed-breaking-inline'>callback</span> <span class='added '>requestCallback</span>, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginReceive (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline removed-breaking-inline'>socket_flags</span> <span class='added '>socketFlags</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginReceive (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline removed-breaking-inline'>flags</span> <span class='added '>socketFlags</span>, out SocketError <span class='removed removed-inline removed-breaking-inline'>error</span> <span class='added '>errorCode</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public System.IAsyncResult BeginSend (byte[] buffer, int offset, int size, SocketFlags <span class='removed removed-inline removed-breaking-inline'>socket_flags</span> <span class='added '>socketFlags</span>, System.AsyncCallback callback, object state)
</div><div data-is-breaking="">	public int EndReceive (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>)
</div><div data-is-breaking="">	public int EndSend (System.IAsyncResult <span class='removed removed-inline removed-breaking-inline'>result</span> <span class='added '>asyncResult</span>)
</div></pre>

</div> <!-- end type Socket -->
<!-- start type TcpListener --> <div>
<h3>Type Changed: System.Net.Sockets.TcpListener</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~TcpListener ();</span>
</pre>

</div> <!-- end type TcpListener -->
<!-- start type UdpClient --> <div>
<h3>Type Changed: System.Net.Sockets.UdpClient</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~UdpClient ();</span>
</pre>

</div> <!-- end type UdpClient -->
<div> <!-- start type SocketClientAccessPolicyProtocol -->
<h3>New Type System.Net.Sockets.SocketClientAccessPolicyProtocol</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SocketClientAccessPolicyProtocol {
	<span class='added added-field ' data-is-non-breaking="">Http = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Tcp = 0,</span>
}
</pre>
</div> <!-- end type SocketClientAccessPolicyProtocol -->

</div> <!-- end namespace System.Net.Sockets -->
<!-- start namespace Mono.Security.Interface --> <div>
<h2>Removed Namespace Mono.Security.Interface</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.Alert</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.AlertDescription</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.AlertLevel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.CertificateValidationHelper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.CipherAlgorithmType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.CipherSuiteCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.ExchangeAlgorithmType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.HashAlgorithmType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.IBufferOffsetSize</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.ICertificateValidator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.IMonoSslStream</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.IMonoTlsEventSink</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoEncryptionPolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoLocalCertificateSelectionCallback</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoRemoteCertificateValidationCallback</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoSslPolicyErrors</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsConnectionInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsProviderFactory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.TlsException</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.TlsProtocolCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.TlsProtocols</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.ValidationResult</span></h3></div> <!-- end namespace Mono.Security.Interface -->

<!-- start namespace Mono.Security.Protocol.Ntlm --> <div>
<h2>Removed Namespace Mono.Security.Protocol.Ntlm</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.ChallengeResponse</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.ChallengeResponse2</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.MessageBase</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.NtlmAuthLevel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.NtlmFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.NtlmSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.Type1Message</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.Type2Message</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Protocol.Ntlm.Type3Message</span></h3></div> <!-- end namespace Mono.Security.Protocol.Ntlm -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Core.html'>System.Core.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Linq --> <div> 
<h2>Namespace System.Linq</h2>
<!-- start type Enumerable --> <div>
<h3>Type Changed: System.Linq.Enumerable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; SkipLast&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; TakeLast&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.HashSet&lt;TSource&gt; ToHashSet&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.HashSet&lt;TSource&gt; ToHashSet&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, System.Collections.Generic.IEqualityComparer&lt;TSource&gt; comparer);</span>
</pre>
</div>

</div> <!-- end type Enumerable -->
<!-- start type Queryable --> <div>
<h3>Type Changed: System.Linq.Queryable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Linq.IQueryable&lt;TSource&gt; SkipLast&lt;TSource&gt; (System.Linq.IQueryable&lt;TSource&gt; source, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Linq.IQueryable&lt;TSource&gt; TakeLast&lt;TSource&gt; (System.Linq.IQueryable&lt;TSource&gt; source, int count);</span>
</pre>
</div>

</div> <!-- end type Queryable -->

</div> <!-- end namespace System.Linq -->
<!-- start namespace System.Linq.Expressions --> <div> 
<h2>Namespace System.Linq.Expressions</h2>
<!-- start type DynamicExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.DynamicExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool CanReduce { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override Expression Reduce ();</span>
</pre>
</div>

</div> <!-- end type DynamicExpression -->
<!-- start type DynamicExpressionVisitor --> <div>
<h3>Type Changed: System.Linq.Expressions.DynamicExpressionVisitor</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>public</span> DynamicExpressionVisitor ()
</div></pre>

</div> <!-- end type DynamicExpressionVisitor -->
<!-- start type ElementInit --> <div>
<h3>Type Changed: System.Linq.Expressions.ElementInit</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ArgumentCount { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Expression GetArgument (int index);</span>
</pre>
</div>

</div> <!-- end type ElementInit -->
<!-- start type IndexExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.IndexExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ArgumentCount { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Expression GetArgument (int index);</span>
</pre>
</div>

</div> <!-- end type IndexExpression -->
<!-- start type InvocationExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.InvocationExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ArgumentCount { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Expression GetArgument (int index);</span>
</pre>
</div>

</div> <!-- end type InvocationExpression -->
<!-- start type MethodCallExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.MethodCallExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ArgumentCount { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Expression GetArgument (int index);</span>
</pre>
</div>

</div> <!-- end type MethodCallExpression -->
<!-- start type NewExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.NewExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ArgumentCount { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Expression GetArgument (int index);</span>
</pre>
</div>

</div> <!-- end type NewExpression -->

</div> <!-- end namespace System.Linq.Expressions -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type RuntimeOps --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.RuntimeOps</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("do not use this method")]
	public static IRuntimeVariables CreateRuntimeVariables ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("do not use this method")]
	public static IRuntimeVariables CreateRuntimeVariables (object[] data, long[] indexes);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("do not use this method")]
	public static IRuntimeVariables MergeRuntimeVariables (IRuntimeVariables first, IRuntimeVariables second, int[] indexes);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("do not use this method")]
	public static System.Linq.Expressions.Expression Quote (System.Linq.Expressions.Expression expression, object hoistedLocals, object[] locals);</span>
</pre>
</div>

</div> <!-- end type RuntimeOps -->
<div> <!-- start type Closure -->
<h3>New Type System.Runtime.CompilerServices.Closure</h3>
<pre class='added' data-is-non-breaking="">
public sealed class Closure {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Closure (object[] constants, object[] locals);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public object[] Constants;</span>
	<span class='added added-field ' data-is-non-breaking="">public object[] Locals;</span>
}
</pre>
</div> <!-- end type Closure -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<div> <!-- start type SHA256CryptoServiceProvider -->
<h3>New Type System.Security.Cryptography.SHA256CryptoServiceProvider</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SHA256CryptoServiceProvider : System.Security.Cryptography.SHA256, System.IDisposable, ICryptoTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SHA256CryptoServiceProvider ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void HashCore (byte[] array, int ibStart, int cbSize);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashFinal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void Initialize ();</span>
}
</pre>
</div> <!-- end type SHA256CryptoServiceProvider -->
<div> <!-- start type SHA384CryptoServiceProvider -->
<h3>New Type System.Security.Cryptography.SHA384CryptoServiceProvider</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SHA384CryptoServiceProvider : System.Security.Cryptography.SHA384, System.IDisposable, ICryptoTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SHA384CryptoServiceProvider ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void HashCore (byte[] array, int ibStart, int cbSize);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashFinal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void Initialize ();</span>
}
</pre>
</div> <!-- end type SHA384CryptoServiceProvider -->
<div> <!-- start type SHA512CryptoServiceProvider -->
<h3>New Type System.Security.Cryptography.SHA512CryptoServiceProvider</h3>
<pre class='added' data-is-non-breaking="">
public sealed class SHA512CryptoServiceProvider : System.Security.Cryptography.SHA512, System.IDisposable, ICryptoTransform {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SHA512CryptoServiceProvider ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void HashCore (byte[] array, int ibStart, int cbSize);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override byte[] HashFinal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void Initialize ();</span>
}
</pre>
</div> <!-- end type SHA512CryptoServiceProvider -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/System.Data.html'>System.Data.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Data.Common --> <div> 
<h2>Namespace System.Data.Common</h2>
<div> <!-- start type DbColumn -->
<h3>New Type System.Data.Common.DbColumn</h3>
<pre class='added' data-is-non-breaking="">
public abstract class DbColumn {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected DbColumn ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">protected bool? AllowDBNull { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string BaseCatalogName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string BaseColumnName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string BaseSchemaName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string BaseServerName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string BaseTableName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string ColumnName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected int? ColumnOrdinal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected int? ColumnSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected System.Type DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string DataTypeName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsAliased { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsAutoIncrement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsHidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsIdentity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsKey { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsLong { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected bool? IsUnique { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual object Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected int? NumericPrecision { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected int? NumericScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected string UdtAssemblyQualifiedName { get; set; }</span>
}
</pre>
</div> <!-- end type DbColumn -->
<div> <!-- start type IDbColumnSchemaGenerator -->
<h3>New Type System.Data.Common.IDbColumnSchemaGenerator</h3>
<pre class='added' data-is-non-breaking="">
public interface IDbColumnSchemaGenerator {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.ObjectModel.ReadOnlyCollection&lt;DbColumn&gt; GetColumnSchema ();</span>
}
</pre>
</div> <!-- end type IDbColumnSchemaGenerator -->

</div> <!-- end namespace System.Data.Common -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/System.IO.Compression.FileSystem.html'>System.IO.Compression.FileSystem.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.IO.Compression --> <div> 
<h2>Namespace System.IO.Compression</h2>
<!-- start type ZipFile --> <div>
<h3>Type Changed: System.IO.Compression.ZipFile</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ExtractToDirectory (string sourceArchiveFileName, string destinationDirectoryName, bool overwrite);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ExtractToDirectory (string sourceArchiveFileName, string destinationDirectoryName, System.Text.Encoding entryNameEncoding, bool overwrite);</span>
</pre>
</div>

</div> <!-- end type ZipFile -->
<!-- start type ZipFileExtensions --> <div>
<h3>Type Changed: System.IO.Compression.ZipFileExtensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ExtractToDirectory (ZipArchive source, string destinationDirectoryName, bool overwrite);</span>
</pre>
</div>

</div> <!-- end type ZipFileExtensions -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/Mono.Security.html'>Mono.Security.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Mono.Security.Interface --> <div> 
<h2>Namespace Mono.Security.Interface</h2>
<div> <!-- start type Alert -->
<h3>New Type Mono.Security.Interface.Alert</h3>
<pre class='added' data-is-non-breaking="">
public class Alert {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Alert (AlertDescription description);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Alert (AlertLevel level, AlertDescription description);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AlertDescription Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsCloseNotify { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsWarning { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AlertLevel Level { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetAlertMessage (AlertDescription description);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type Alert -->
<div> <!-- start type AlertDescription -->
<h3>New Type Mono.Security.Interface.AlertDescription</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AlertDescription {
	<span class='added added-field ' data-is-non-breaking="">AccessDenied = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">BadCertificate = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">BadRecordMAC = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateExpired = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateRevoked = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateUnknown = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">CloseNotify = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DecodeError = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">DecompressionFailure = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">DecryptError = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">DecryptionFailed_RESERVED = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">ExportRestriction = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">HandshakeFailure = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">IlegalParameter = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">InsuficientSecurity = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">NoCertificate_RESERVED = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">NoRenegotiation = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">ProtocolVersion = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordOverflow = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">UnexpectedMessage = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownCA = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedCertificate = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedExtension = 110,</span>
	<span class='added added-field ' data-is-non-breaking="">UserCancelled = 90,</span>
}
</pre>
</div> <!-- end type AlertDescription -->
<div> <!-- start type AlertLevel -->
<h3>New Type Mono.Security.Interface.AlertLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AlertLevel {
	<span class='added added-field ' data-is-non-breaking="">Fatal = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Warning = 1,</span>
}
</pre>
</div> <!-- end type AlertLevel -->
<div> <!-- start type CertificateValidationHelper -->
<h3>New Type Mono.Security.Interface.CertificateValidationHelper</h3>
<pre class='added' data-is-non-breaking="">
public static class CertificateValidationHelper {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static bool SupportsTrustAnchors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SupportsX509Chain { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ICertificateValidator GetValidator (MonoTlsSettings settings);</span>
}
</pre>
</div> <!-- end type CertificateValidationHelper -->
<div> <!-- start type CipherAlgorithmType -->
<h3>New Type Mono.Security.Interface.CipherAlgorithmType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CipherAlgorithmType {
	<span class='added added-field ' data-is-non-breaking="">Aes128 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Aes256 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AesGcm128 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AesGcm256 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CipherAlgorithmType -->
<div> <!-- start type CipherSuiteCode -->
<h3>New Type Mono.Security.Interface.CipherSuiteCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CipherSuiteCode {
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_3DES_EDE_CBC_SHA = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_128_CBC_SHA = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_128_CBC_SHA256 = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_128_GCM_SHA256 = 162,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_256_CBC_SHA = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_256_CBC_SHA256 = 106,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_AES_256_GCM_SHA384 = 163,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_128_CBC_SHA = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_128_CBC_SHA256 = 189,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_128_GCM_SHA256 = 49280,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_256_CBC_SHA = 135,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_256_CBC_SHA256 = 195,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_CAMELLIA_256_GCM_SHA384 = 49281,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_DES_CBC_SHA = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_DSS_WITH_SEED_CBC_SHA = 153,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_3DES_EDE_CBC_SHA = 143,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_128_CBC_SHA = 144,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_128_CBC_SHA256 = 178,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_128_CCM = 49318,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_128_GCM_SHA256 = 170,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_256_CBC_SHA = 145,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_256_CBC_SHA384 = 179,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_256_CCM = 49319,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_AES_256_GCM_SHA384 = 171,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_CAMELLIA_128_CBC_SHA256 = 49302,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_CAMELLIA_128_GCM_SHA256 = 49296,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_CAMELLIA_256_CBC_SHA384 = 49303,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_CAMELLIA_256_GCM_SHA384 = 49297,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_ESTREAM_SALSA20_SHA1 = 58396,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_NULL_SHA = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_NULL_SHA256 = 180,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_NULL_SHA384 = 181,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_RC4_128_SHA = 142,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_PSK_WITH_SALSA20_SHA1 = 58397,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_3DES_EDE_CBC_SHA = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_128_CBC_SHA = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_128_CCM = 49310,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_128_CCM_8 = 49314,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 = 158,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_256_CBC_SHA = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 = 107,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_256_CCM = 49311,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_256_CCM_8 = 49315,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 = 159,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA256 = 190,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_128_GCM_SHA256 = 49276,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA = 136,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA256 = 196,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CAMELLIA_256_GCM_SHA384 = 49277,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_CHACHA20_POLY1305_SHA256 = 52245,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_DES_CBC_SHA = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_ESTREAM_SALSA20_SHA1 = 58398,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_SALSA20_SHA1 = 58399,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DHE_RSA_WITH_SEED_CBC_SHA = 154,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_EXPORT_WITH_DES40_CBC_SHA = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_3DES_EDE_CBC_SHA = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_128_CBC_SHA = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_128_CBC_SHA256 = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_128_GCM_SHA256 = 164,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_256_CBC_SHA = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_256_CBC_SHA256 = 104,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_AES_256_GCM_SHA384 = 165,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_128_CBC_SHA = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_128_CBC_SHA256 = 187,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_128_GCM_SHA256 = 49282,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_256_CBC_SHA = 133,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_256_CBC_SHA256 = 193,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_CAMELLIA_256_GCM_SHA384 = 49283,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_DES_CBC_SHA = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_DSS_WITH_SEED_CBC_SHA = 151,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_EXPORT_WITH_DES40_CBC_SHA = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_3DES_EDE_CBC_SHA = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_128_CBC_SHA = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_128_CBC_SHA256 = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_128_GCM_SHA256 = 160,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_256_CBC_SHA = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_256_CBC_SHA256 = 105,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_AES_256_GCM_SHA384 = 161,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_128_CBC_SHA = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_128_CBC_SHA256 = 188,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_128_GCM_SHA256 = 49278,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_256_CBC_SHA = 134,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_256_CBC_SHA256 = 194,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_CAMELLIA_256_GCM_SHA384 = 49279,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_DES_CBC_SHA = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_RSA_WITH_SEED_CBC_SHA = 152,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_EXPORT_WITH_DES40_CBC_SHA = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_EXPORT_WITH_RC4_40_MD5 = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_3DES_EDE_CBC_SHA = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_128_CBC_SHA = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_128_CBC_SHA256 = 108,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_128_GCM_SHA256 = 166,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_256_CBC_SHA = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_256_CBC_SHA256 = 109,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_AES_256_GCM_SHA384 = 167,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_128_CBC_SHA = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_128_CBC_SHA256 = 191,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_128_GCM_SHA256 = 49284,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_256_CBC_SHA = 137,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_256_CBC_SHA256 = 197,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_CAMELLIA_256_GCM_SHA384 = 49285,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_DES_CBC_SHA = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_RC4_128_MD5 = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_DH_anon_WITH_SEED_CBC_SHA = 155,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA = 49160,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA = 49161,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 = 49187,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 = 49195,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA = 49162,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384 = 49188,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 = 49196,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CAMELLIA_128_CBC_SHA256 = 49266,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CAMELLIA_128_GCM_SHA256 = 49286,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CAMELLIA_256_CBC_SHA384 = 49267,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CAMELLIA_256_GCM_SHA384 = 49287,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 = 52244,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_ESTREAM_SALSA20_SHA1 = 58388,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_NULL_SHA = 49158,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_RC4_128_SHA = 49159,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_SALSA20_SHA1 = 58389,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_3DES_EDE_CBC_SHA = 49204,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_AES_128_CBC_SHA = 49205,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_AES_128_CBC_SHA256 = 49207,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_AES_256_CBC_SHA = 49206,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_AES_256_CBC_SHA384 = 49208,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_CAMELLIA_128_CBC_SHA256 = 49306,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_CAMELLIA_256_CBC_SHA384 = 49307,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_ESTREAM_SALSA20_SHA1 = 58392,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_NULL_SHA = 49209,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_NULL_SHA256 = 49210,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_NULL_SHA384 = 49211,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_RC4_128_SHA = 49203,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_PSK_WITH_SALSA20_SHA1 = 58393,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA = 49170,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA = 49171,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 = 49191,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 = 49199,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA = 49172,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 = 49192,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 = 49200,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CAMELLIA_128_CBC_SHA256 = 49270,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CAMELLIA_128_GCM_SHA256 = 49290,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CAMELLIA_256_CBC_SHA384 = 49271,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CAMELLIA_256_GCM_SHA384 = 49291,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 = 52243,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_ESTREAM_SALSA20_SHA1 = 58386,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_NULL_SHA = 49168,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_RC4_128_SHA = 49169,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_SALSA20_SHA1 = 58387,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA = 49155,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA = 49156,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256 = 49189,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 = 49197,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA = 49157,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384 = 49190,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 = 49198,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_CAMELLIA_128_CBC_SHA256 = 49268,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_CAMELLIA_128_GCM_SHA256 = 49288,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_CAMELLIA_256_CBC_SHA384 = 49269,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_CAMELLIA_256_GCM_SHA384 = 49289,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_NULL_SHA = 49153,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_ECDSA_WITH_RC4_128_SHA = 49154,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA = 49165,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_128_CBC_SHA = 49166,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256 = 49193,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 = 49201,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_256_CBC_SHA = 49167,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384 = 49194,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 = 49202,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_CAMELLIA_128_CBC_SHA256 = 49272,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_CAMELLIA_128_GCM_SHA256 = 49292,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_CAMELLIA_256_CBC_SHA384 = 49273,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_CAMELLIA_256_GCM_SHA384 = 49293,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_NULL_SHA = 49163,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_RSA_WITH_RC4_128_SHA = 49164,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_anon_WITH_3DES_EDE_CBC_SHA = 49175,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_anon_WITH_AES_128_CBC_SHA = 49176,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_anon_WITH_AES_256_CBC_SHA = 49177,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_anon_WITH_NULL_SHA = 49173,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDH_anon_WITH_RC4_128_SHA = 49174,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_EMPTY_RENEGOTIATION_INFO_SCSV = 255,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_FALLBACK_SCSV = 22016,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_NULL_WITH_NULL_NULL = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_DHE_WITH_AES_128_CCM_8 = 49322,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_DHE_WITH_AES_256_CCM_8 = 49323,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_3DES_EDE_CBC_SHA = 139,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_128_CBC_SHA = 140,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_128_CBC_SHA256 = 174,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_128_CCM = 49316,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_128_CCM_8 = 49320,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_128_GCM_SHA256 = 168,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_256_CBC_SHA = 141,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_256_CBC_SHA384 = 175,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_256_CCM = 49317,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_256_CCM_8 = 49321,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_AES_256_GCM_SHA384 = 169,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_CAMELLIA_128_CBC_SHA256 = 49300,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_CAMELLIA_128_GCM_SHA256 = 49294,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_CAMELLIA_256_CBC_SHA384 = 49301,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_CAMELLIA_256_GCM_SHA384 = 49295,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_ESTREAM_SALSA20_SHA1 = 58390,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_NULL_SHA = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_NULL_SHA256 = 176,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_NULL_SHA384 = 177,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_RC4_128_SHA = 138,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_PSK_WITH_SALSA20_SHA1 = 58391,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_EXPORT_WITH_DES40_CBC_SHA = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_EXPORT_WITH_RC2_CBC_40_MD5 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_EXPORT_WITH_RC4_40_MD5 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_3DES_EDE_CBC_SHA = 147,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_128_CBC_SHA = 148,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_128_CBC_SHA256 = 182,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_128_GCM_SHA256 = 172,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_256_CBC_SHA = 149,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_256_CBC_SHA384 = 183,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_AES_256_GCM_SHA384 = 173,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_CAMELLIA_128_CBC_SHA256 = 49304,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_CAMELLIA_128_GCM_SHA256 = 49298,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_CAMELLIA_256_CBC_SHA384 = 49305,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_CAMELLIA_256_GCM_SHA384 = 49299,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_ESTREAM_SALSA20_SHA1 = 58394,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_NULL_SHA = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_NULL_SHA256 = 184,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_NULL_SHA384 = 185,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_RC4_128_SHA = 146,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_PSK_WITH_SALSA20_SHA1 = 58395,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_3DES_EDE_CBC_SHA = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_128_CBC_SHA = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_128_CBC_SHA256 = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_128_CCM = 49308,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_128_CCM_8 = 49312,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_128_GCM_SHA256 = 156,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_256_CBC_SHA = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_256_CBC_SHA256 = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_256_CCM = 49309,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_256_CCM_8 = 49313,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_AES_256_GCM_SHA384 = 157,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_128_CBC_SHA = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_128_CBC_SHA256 = 186,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_128_GCM_SHA256 = 49274,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_256_CBC_SHA = 132,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_256_CBC_SHA256 = 192,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_CAMELLIA_256_GCM_SHA384 = 49275,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_DES_CBC_SHA = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_ESTREAM_SALSA20_SHA1 = 58384,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_IDEA_CBC_SHA = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_NULL_MD5 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_NULL_SHA = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_NULL_SHA256 = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_RC4_128_MD5 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_RC4_128_SHA = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_SALSA20_SHA1 = 58385,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_RSA_WITH_SEED_CBC_SHA = 150,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_DSS_WITH_3DES_EDE_CBC_SHA = 49180,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_DSS_WITH_AES_128_CBC_SHA = 49183,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_DSS_WITH_AES_256_CBC_SHA = 49186,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_RSA_WITH_3DES_EDE_CBC_SHA = 49179,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_RSA_WITH_AES_128_CBC_SHA = 49182,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_RSA_WITH_AES_256_CBC_SHA = 49185,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_WITH_3DES_EDE_CBC_SHA = 49178,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_WITH_AES_128_CBC_SHA = 49181,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_SRP_SHA_WITH_AES_256_CBC_SHA = 49184,</span>
}
</pre>
</div> <!-- end type CipherSuiteCode -->
<div> <!-- start type ExchangeAlgorithmType -->
<h3>New Type Mono.Security.Interface.ExchangeAlgorithmType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ExchangeAlgorithmType {
	<span class='added added-field ' data-is-non-breaking="">Dhe = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">EcDhe = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Rsa = 2,</span>
}
</pre>
</div> <!-- end type ExchangeAlgorithmType -->
<div> <!-- start type HashAlgorithmType -->
<h3>New Type Mono.Security.Interface.HashAlgorithmType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HashAlgorithmType {
	<span class='added added-field ' data-is-non-breaking="">Md5 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Md5Sha1 = 254,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sha1 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Sha224 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Sha256 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Sha384 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Sha512 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 255,</span>
}
</pre>
</div> <!-- end type HashAlgorithmType -->
<div> <!-- start type IBufferOffsetSize -->
<h3>New Type Mono.Security.Interface.IBufferOffsetSize</h3>
<pre class='added' data-is-non-breaking="">
public interface IBufferOffsetSize {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual byte[] Buffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Offset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Size { get; }</span>
}
</pre>
</div> <!-- end type IBufferOffsetSize -->
<div> <!-- start type ICertificateValidator -->
<h3>New Type Mono.Security.Interface.ICertificateValidator</h3>
<pre class='added' data-is-non-breaking="">
public interface ICertificateValidator {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoTlsSettings Settings { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SelectClientCertificate (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection localCertificates, System.Security.Cryptography.X509Certificates.X509Certificate remoteCertificate, string[] acceptableIssuers, System.Security.Cryptography.X509Certificates.X509Certificate clientCertificate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ValidationResult ValidateCertificate (string targetHost, bool serverMode, System.Security.Cryptography.X509Certificates.X509CertificateCollection certificates);</span>
}
</pre>
</div> <!-- end type ICertificateValidator -->
<div> <!-- start type IMonoSslStream -->
<h3>New Type Mono.Security.Interface.IMonoSslStream</h3>
<pre class='added' data-is-non-breaking="">
public interface IMonoSslStream : System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Net.Security.AuthenticatedStream AuthenticatedStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CheckCertRevocationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Authentication.CipherAlgorithmType CipherAlgorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int CipherStrength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Authentication.HashAlgorithmType HashAlgorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int HashStrength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Cryptography.X509Certificates.X509Certificate InternalLocalCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAuthenticated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsEncrypted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsMutuallyAuthenticated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsServer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsSigned { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Authentication.ExchangeAlgorithmType KeyExchangeAlgorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int KeyExchangeStrength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Length { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Cryptography.X509Certificates.X509Certificate LocalCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Position { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MonoTlsProvider Provider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int ReadTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Cryptography.X509Certificates.X509Certificate RemoteCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Authentication.SslProtocols SslProtocol { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Net.TransportContext TransportContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int WriteTimeout { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsClient (string targetHost);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsClient (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection clientCertificates, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (string targetHost);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection clientCertificates, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsServer (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AuthenticateAsServer (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate, bool clientCertificateRequired, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate, bool clientCertificateRequired, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsClient (string targetHost, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsClient (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection clientCertificates, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsServer (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginAuthenticateAsServer (System.Security.Cryptography.X509Certificates.X509Certificate serverCertificate, bool clientCertificateRequired, System.Security.Authentication.SslProtocols enabledSslProtocols, bool checkCertificateRevocation, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginRead (byte[] buffer, int offset, int count, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginWrite (byte[] buffer, int offset, int count, System.AsyncCallback asyncCallback, object asyncState);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndAuthenticateAsClient (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndAuthenticateAsServer (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int EndRead (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndWrite (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MonoTlsConnectionInfo GetConnectionInfo ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Read (byte[] buffer, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLength (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (byte[] buffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Write (byte[] buffer, int offset, int count);</span>
}
</pre>
</div> <!-- end type IMonoSslStream -->
<div> <!-- start type IMonoTlsEventSink -->
<h3>New Type Mono.Security.Interface.IMonoTlsEventSink</h3>
<pre class='added' data-is-non-breaking="">
public interface IMonoTlsEventSink {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Error (System.Exception exception);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReceivedCloseNotify ();</span>
}
</pre>
</div> <!-- end type IMonoTlsEventSink -->
<div> <!-- start type MonoEncryptionPolicy -->
<h3>New Type Mono.Security.Interface.MonoEncryptionPolicy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MonoEncryptionPolicy {
	<span class='added added-field ' data-is-non-breaking="">AllowNoEncryption = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NoEncryption = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RequireEncryption = 0,</span>
}
</pre>
</div> <!-- end type MonoEncryptionPolicy -->
<div> <!-- start type MonoLocalCertificateSelectionCallback -->
<h3>New Type Mono.Security.Interface.MonoLocalCertificateSelectionCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MonoLocalCertificateSelectionCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MonoLocalCertificateSelectionCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection localCertificates, System.Security.Cryptography.X509Certificates.X509Certificate remoteCertificate, string[] acceptableIssuers, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Security.Cryptography.X509Certificates.X509Certificate EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Security.Cryptography.X509Certificates.X509Certificate Invoke (string targetHost, System.Security.Cryptography.X509Certificates.X509CertificateCollection localCertificates, System.Security.Cryptography.X509Certificates.X509Certificate remoteCertificate, string[] acceptableIssuers);</span>
}
</pre>
</div> <!-- end type MonoLocalCertificateSelectionCallback -->
<div> <!-- start type MonoRemoteCertificateValidationCallback -->
<h3>New Type Mono.Security.Interface.MonoRemoteCertificateValidationCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MonoRemoteCertificateValidationCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MonoRemoteCertificateValidationCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string targetHost, System.Security.Cryptography.X509Certificates.X509Certificate certificate, System.Security.Cryptography.X509Certificates.X509Chain chain, MonoSslPolicyErrors sslPolicyErrors, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (string targetHost, System.Security.Cryptography.X509Certificates.X509Certificate certificate, System.Security.Cryptography.X509Certificates.X509Chain chain, MonoSslPolicyErrors sslPolicyErrors);</span>
}
</pre>
</div> <!-- end type MonoRemoteCertificateValidationCallback -->
<div> <!-- start type MonoSslPolicyErrors -->
<h3>New Type Mono.Security.Interface.MonoSslPolicyErrors</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MonoSslPolicyErrors {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RemoteCertificateChainErrors = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RemoteCertificateNameMismatch = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RemoteCertificateNotAvailable = 1,</span>
}
</pre>
</div> <!-- end type MonoSslPolicyErrors -->
<div> <!-- start type MonoTlsConnectionInfo -->
<h3>New Type Mono.Security.Interface.MonoTlsConnectionInfo</h3>
<pre class='added' data-is-non-breaking="">
public class MonoTlsConnectionInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MonoTlsConnectionInfo ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CipherAlgorithmType CipherAlgorithmType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CipherSuiteCode CipherSuiteCode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ExchangeAlgorithmType ExchangeAlgorithmType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HashAlgorithmType HashAlgorithmType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string PeerDomainName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public TlsProtocols ProtocolVersion { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type MonoTlsConnectionInfo -->
<div> <!-- start type MonoTlsProvider -->
<h3>New Type Mono.Security.Interface.MonoTlsProvider</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MonoTlsProvider {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Guid ID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Security.Authentication.SslProtocols SupportedProtocols { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsConnectionInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsMonoExtensions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsSslStream { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IMonoSslStream CreateSslStream (System.IO.Stream innerStream, bool leaveInnerStreamOpen, MonoTlsSettings settings);</span>
}
</pre>
</div> <!-- end type MonoTlsProvider -->
<div> <!-- start type MonoTlsProviderFactory -->
<h3>New Type Mono.Security.Interface.MonoTlsProviderFactory</h3>
<pre class='added' data-is-non-breaking="">
public static class MonoTlsProviderFactory {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static bool IsInitialized { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static System.Net.HttpListener CreateHttpListener (System.Security.Cryptography.X509Certificates.X509Certificate certificate, MonoTlsProvider provider, MonoTlsSettings settings);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Net.HttpWebRequest CreateHttpsRequest (System.Uri requestUri, MonoTlsProvider provider, MonoTlsSettings settings);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use GetProvider() instead.")]
	public static MonoTlsProvider GetDefaultProvider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMonoSslStream GetMonoSslStream (System.Net.Security.SslStream stream);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MonoTlsProvider GetProvider ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MonoTlsProvider GetProvider (string provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Initialize ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Initialize (string provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsProviderSupported (string provider);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use Initialize(string provider) instead.")]
	public static void SetDefaultProvider (string name);</span>
}
</pre>
</div> <!-- end type MonoTlsProviderFactory -->
<div> <!-- start type MonoTlsSettings -->
<h3>New Type Mono.Security.Interface.MonoTlsSettings</h3>
<pre class='added' data-is-non-breaking="">
public sealed class MonoTlsSettings {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MonoTlsSettings ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool CallbackNeedsCertificateChain { get; set; }</span>

	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("Do not use outside System.dll!")]
	public ICertificateValidator CertificateValidator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool CheckCertificateName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool CheckCertificateRevocationStatus { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoLocalCertificateSelectionCallback ClientCertificateSelectionCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoTlsSettings DefaultSettings { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CipherSuiteCode[] EnabledCiphers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public TlsProtocols? EnabledProtocols { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoRemoteCertificateValidationCallback RemoteCertificateValidationCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SkipSystemValidators { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509CertificateCollection TrustAnchors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? UseServicePointManagerCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public object UserSettings { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public MonoTlsSettings Clone ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Do not use outside System.dll!")]
	public MonoTlsSettings CloneWithValidator (ICertificateValidator validator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MonoTlsSettings CopyDefaultSettings ();</span>
}
</pre>
</div> <!-- end type MonoTlsSettings -->
<div> <!-- start type TlsException -->
<h3>New Type Mono.Security.Interface.TlsException</h3>
<pre class='added' data-is-non-breaking="">
public sealed class TlsException : System.Exception, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (Alert alert);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (AlertDescription description);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (Alert alert, string message);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (AlertDescription description, string message);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (AlertLevel level, AlertDescription description);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TlsException (AlertDescription description, string format, object[] args);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Alert Alert { get; }</span>
}
</pre>
</div> <!-- end type TlsException -->
<div> <!-- start type TlsProtocolCode -->
<h3>New Type Mono.Security.Interface.TlsProtocolCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TlsProtocolCode {
	<span class='added added-field ' data-is-non-breaking="">Tls10 = 769,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls11 = 770,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls12 = 771,</span>
}
</pre>
</div> <!-- end type TlsProtocolCode -->
<div> <!-- start type TlsProtocols -->
<h3>New Type Mono.Security.Interface.TlsProtocols</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum TlsProtocols {
	<span class='added added-field ' data-is-non-breaking="">ClientMask = 2688,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerMask = 1344,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls10 = 192,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls10Client = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls10Server = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls11 = 768,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls11Client = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls11Server = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls12 = 3072,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls12Client = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls12Server = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">Zero = 0,</span>
}
</pre>
</div> <!-- end type TlsProtocols -->
<div> <!-- start type ValidationResult -->
<h3>New Type Mono.Security.Interface.ValidationResult</h3>
<pre class='added' data-is-non-breaking="">
public class ValidationResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ValidationResult (bool trusted, bool user_denied, int error_code, MonoSslPolicyErrors? policy_errors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int ErrorCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoSslPolicyErrors? PolicyErrors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Trusted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UserDenied { get; }</span>
}
</pre>
</div> <!-- end type ValidationResult -->

</div> <!-- end namespace Mono.Security.Interface -->
<!-- start namespace Mono.Security.Protocol.Ntlm --> <div> 
<h2>New Namespace Mono.Security.Protocol.Ntlm</h2>

<div> <!-- start type ChallengeResponse -->
<h3>New Type Mono.Security.Protocol.Ntlm.ChallengeResponse</h3>
<pre class='added' data-is-non-breaking="">
public class ChallengeResponse : System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ChallengeResponse ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ChallengeResponse (string password, byte[] challenge);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] Challenge { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte[] LM { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte[] NT { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Password { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~ChallengeResponse ();</span>
}
</pre>
</div> <!-- end type ChallengeResponse -->
<div> <!-- start type ChallengeResponse2 -->
<h3>New Type Mono.Security.Protocol.Ntlm.ChallengeResponse2</h3>
<pre class='added' data-is-non-breaking="">
public static class ChallengeResponse2 {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Compute (Type2Message type2, NtlmAuthLevel level, string username, string password, string domain, byte[] lm, byte[] ntlm);</span>
}
</pre>
</div> <!-- end type ChallengeResponse2 -->
<div> <!-- start type MessageBase -->
<h3>New Type Mono.Security.Protocol.Ntlm.MessageBase</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MessageBase {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MessageBase (int messageType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NtlmFlags Flags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected bool CheckHeader (byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Decode (byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual byte[] GetBytes ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected byte[] PrepareMessage (int messageSize);</span>
}
</pre>
</div> <!-- end type MessageBase -->
<div> <!-- start type NtlmAuthLevel -->
<h3>New Type Mono.Security.Protocol.Ntlm.NtlmAuthLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NtlmAuthLevel {
	<span class='added added-field ' data-is-non-breaking="">LM_and_NTLM = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">LM_and_NTLM_and_try_NTLMv2_Session = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NTLM_only = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NTLMv2_only = 3,</span>
}
</pre>
</div> <!-- end type NtlmAuthLevel -->
<div> <!-- start type NtlmFlags -->
<h3>New Type Mono.Security.Protocol.Ntlm.NtlmFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NtlmFlags {
	<span class='added added-field ' data-is-non-breaking="">Negotiate128 = 536870912,</span>
	<span class='added added-field ' data-is-non-breaking="">Negotiate56 = -2147483648,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateAlwaysSign = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateDomainSupplied = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateNtlm = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateNtlm2Key = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateOem = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateUnicode = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NegotiateWorkstationSupplied = 8192,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestTarget = 4,</span>
}
</pre>
</div> <!-- end type NtlmFlags -->
<div> <!-- start type NtlmSettings -->
<h3>New Type Mono.Security.Protocol.Ntlm.NtlmSettings</h3>
<pre class='added' data-is-non-breaking="">
public static class NtlmSettings {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NtlmAuthLevel DefaultAuthLevel { get; set; }</span>
}
</pre>
</div> <!-- end type NtlmSettings -->
<div> <!-- start type Type1Message -->
<h3>New Type Mono.Security.Protocol.Ntlm.Type1Message</h3>
<pre class='added' data-is-non-breaking="">
public class Type1Message : Mono.Security.Protocol.Ntlm.MessageBase {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Type1Message ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Type1Message (byte[] message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Domain { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Host { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Decode (byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] GetBytes ();</span>
}
</pre>
</div> <!-- end type Type1Message -->
<div> <!-- start type Type2Message -->
<h3>New Type Mono.Security.Protocol.Ntlm.Type2Message</h3>
<pre class='added' data-is-non-breaking="">
public class Type2Message : Mono.Security.Protocol.Ntlm.MessageBase {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Type2Message ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Type2Message (byte[] message);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte[] Nonce { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte[] TargetInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string TargetName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Decode (byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] GetBytes ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~Type2Message ();</span>
}
</pre>
</div> <!-- end type Type2Message -->
<div> <!-- start type Type3Message -->
<h3>New Type Mono.Security.Protocol.Ntlm.Type3Message</h3>
<pre class='added' data-is-non-breaking="">
public class Type3Message : Mono.Security.Protocol.Ntlm.MessageBase {
	// constructors

	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Use of this API is highly discouraged, it selects legacy-mode LM/NTLM authentication, which sends your password in very weak encryption over the wire even if the server supports the more secure NTLMv2 / NTLMv2 Session. You need to use the new `Type3Message (Type2Message)' constructor to use the more secure NTLMv2 / NTLMv2 Session authentication modes. These require the Type 2 message from the server to compute the response.")]
	public Type3Message ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Type3Message (Type2Message type2);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Type3Message (byte[] message);</span>
	// properties

	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("Use of this API is highly discouraged, it selects legacy-mode LM/NTLM authentication, which sends your password in very weak encryption over the wire even if the server supports the more secure NTLMv2 / NTLMv2 Session. You need to use the new `Type3Message (Type2Message)' constructor to use the more secure NTLMv2 / NTLMv2 Session authentication modes. These require the Type 2 message from the server to compute the response.")]
	public byte[] Challenge { get; set; }</span>

	<span class='added added-property ' data-is-non-breaking="">[Obsolete ("Use NtlmSettings.DefaultAuthLevel")]
	public static NtlmAuthLevel DefaultAuthLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Domain { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Host { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte[] LM { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NtlmAuthLevel Level { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte[] NT { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Password { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Username { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Decode (byte[] message);</span>
	<span class='added added-method ' data-is-non-breaking="">public override byte[] GetBytes ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~Type3Message ();</span>
}
</pre>
</div> <!-- end type Type3Message -->
</div> <!-- end namespace Mono.Security.Protocol.Ntlm -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/Xamarin.TVOS.html'>Xamarin.TVOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAudioPlayerNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleBufferAsync (AVAudioPcmBuffer buffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleFileAsync (AVAudioFile file, AVAudioTime when);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleSegmentAsync (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayerNode -->
<!-- start type AVAudioSessionInterruptionEventArgs --> <div>
<h3>Type Changed: AVFoundation.AVAudioSessionInterruptionEventArgs</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? WasSuspended { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioSessionInterruptionEventArgs -->
<!-- start type AVAudioUnit --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AVAudioUnit&gt; FromComponentDescriptionAsync (AudioUnit.AudioComponentDescription audioComponentDescription, AudioUnit.AudioComponentInstantiationOptions options);</span>
</pre>
</div>

</div> <!-- end type AVAudioUnit -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AUAudioUnit&gt; FromComponentDescriptionAsync (AudioComponentDescription componentDescription, AudioComponentInstantiationOptions options);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGRect --> <div>
<h3>Type Changed: CoreGraphics.CGRect</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CGRect Infinite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CGRect Null { get; }</span>
</pre>
</div>

</div> <!-- end type CGRect -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSExtensionContext --> <div>
<h3>Type Changed: Foundation.NSExtensionContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; CompleteRequestAsync (NSExtensionItem[] returningItems);</span>
</pre>
</div>

</div> <!-- end type NSExtensionContext -->
<!-- start type NSFileVersion --> <div>
<h3>Type Changed: Foundation.NSFileVersion</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSFileVersion[]&gt; GetNonlocalVersionsAsync (NSUrl url);</span>
</pre>
</div>

</div> <!-- end type NSFileVersion -->
<!-- start type NSHttpCookieStorage --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSHttpCookie[]&gt; GetCookiesForTaskAsync (NSUrlSessionTask task);</span>
</pre>
</div>

</div> <!-- end type NSHttpCookieStorage -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSObject&gt; LoadItemAsync (string typeIdentifier, NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSObject&gt; LoadPreviewImageAsync (NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetParagraphPositions (uint paragraphStartPosition, uint paragraphEndPosition, uint contentsEndPosition, NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetParagraphRange (NSRange range);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSUrlCredentialStorage --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSDictionary&gt; GetCredentialsAsync (NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrlCredential&gt; GetDefaultCredentialAsync (NSUrlProtectionSpace space, NSUrlSessionTask task);</span>
</pre>
</div>

</div> <!-- end type NSUrlCredentialStorage -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCController --> <div>
<h3>Type Changed: GameController.GCController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task StartWirelessControllerDiscoveryAsync ();</span>
</pre>
</div>

</div> <!-- end type GCController -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKAchievement --> <div>
<h3>Type Changed: GameKit.GKAchievement</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players, UIKit.UIViewController result);</span>
</pre>
</div>

</div> <!-- end type GKAchievement -->
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKIdentityVerificationSignatureResult&gt; GenerateIdentityVerificationSignatureAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKMatch --> <div>
<h3>Type Changed: GameKit.GKMatch</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKPlayer&gt; ChooseBestHostingPlayerAsync ();</span>
</pre>
</div>

</div> <!-- end type GKMatch -->
<!-- start type GKScore --> <div>
<h3>Type Changed: GameKit.GKScore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players, UIKit.UIViewController result);</span>
</pre>
</div>

</div> <!-- end type GKScore -->
<div> <!-- start type GKChallengeComposeResult -->
<h3>New Type GameKit.GKChallengeComposeResult</h3>
<pre class='added' data-is-non-breaking="">
public class GKChallengeComposeResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKChallengeComposeResult (UIKit.UIViewController composeController, bool issuedChallenge, string[] sentPlayerIDs);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UIKit.UIViewController ComposeController { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IssuedChallenge { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] SentPlayerIDs { get; set; }</span>
}
</pre>
</div> <!-- end type GKChallengeComposeResult -->
<div> <!-- start type GKIdentityVerificationSignatureResult -->
<h3>New Type GameKit.GKIdentityVerificationSignatureResult</h3>
<pre class='added' data-is-non-breaking="">
public class GKIdentityVerificationSignatureResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKIdentityVerificationSignatureResult (Foundation.NSUrl publicKeyUrl, Foundation.NSData signature, Foundation.NSData salt, ulong timestamp);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl PublicKeyUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Salt { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Signature { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ulong Timestamp { get; set; }</span>
}
</pre>
</div> <!-- end type GKIdentityVerificationSignatureResult -->

</div> <!-- end namespace GameKit -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKDirections --> <div>
<h3>Type Changed: MapKit.MKDirections</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKDirectionsResponse&gt; CalculateDirectionsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKETAResponse&gt; CalculateETAAsync ();</span>
</pre>
</div>

</div> <!-- end type MKDirections -->
<!-- start type MKLocalSearchRequest --> <div>
<h3>Type Changed: MapKit.MKLocalSearchRequest</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKLocalSearchRequest (MKLocalSearchCompletion completion);</span>
</pre>
</div>

</div> <!-- end type MKLocalSearchRequest -->
<!-- start type MKMapSnapshotter --> <div>
<h3>Type Changed: MapKit.MKMapSnapshotter</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKMapSnapshot&gt; StartAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKMapSnapshot&gt; StartAsync (CoreFoundation.DispatchQueue queue);</span>
</pre>
</div>

</div> <!-- end type MKMapSnapshotter -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromCGImageAsync (CoreGraphics.CGImage cgImage, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromDataAsync (Foundation.NSData data, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromNameAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromNameAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromNamesAsync (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromNamesAsync (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromUrlAsync (Foundation.NSUrl url, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromUrlsAsync (Foundation.NSUrl[] urls, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromUrlsAsync (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.8.0"</span> <span class='added '>"10.10.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetCGRect (IntPtr handle, string symbol);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<!-- start type MonoPInvokeCallbackAttribute --> <div>
<h3>Type Changed: ObjCRuntime.MonoPInvokeCallbackAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Type DelegateType { get; set; }</span>
</pre>
</div>

</div> <!-- end type MonoPInvokeCallbackAttribute -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetResourceManager --> <div>
<h3>Type Changed: Photos.PHAssetResourceManager</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task WriteDataAsync (PHAssetResource forResource, Foundation.NSUrl fileURL, PHAssetResourceRequestOptions options);</span>
</pre>
</div>

</div> <!-- end type PHAssetResourceManager -->

</div> <!-- end namespace Photos -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'SCNSceneRenderer_Extensions.PrepareAsync' instead")]
	public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'SCNSceneRenderer_Extensions.PresentSceneAsync' instead")]
	public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->
<!-- start type SCNSceneRenderer_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (ISCNSceneRenderer This, Foundation.NSObject[] objects);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task PresentSceneAsync (ISCNSceneRenderer This, SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer_Extensions -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNView -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKEffectNode --> <div>
<h3>Type Changed: SpriteKit.SKEffectNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKEffectNode -->
<!-- start type SKEmitterNode --> <div>
<h3>Type Changed: SpriteKit.SKEmitterNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKEmitterNode -->
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RunActionAsync (SKAction action);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKSpriteNode --> <div>
<h3>Type Changed: SpriteKit.SKSpriteNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKSpriteNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace TVMLKit --> <div> 
<h2>Namespace TVMLKit</h2>
<!-- start type TVApplicationController --> <div>
<h3>Type Changed: TVMLKit.TVApplicationController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; EvaluateAsync (System.Action&lt;JavaScriptCore.JSContext&gt; evaluation);</span>
</pre>
</div>

</div> <!-- end type TVApplicationController -->
<!-- start type TVViewElement --> <div>
<h3>Type Changed: TVMLKit.TVViewElement</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;TVViewElementDispatchResult&gt; DispatchEventAsync (string eventName, bool canBubble, bool isCancellable, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; extraInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;TVViewElementDispatchResult&gt; DispatchEventAsync (TVElementEventType type, bool canBubble, bool isCancellable, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; extraInfo);</span>
</pre>
</div>

</div> <!-- end type TVViewElement -->
<div> <!-- start type TVViewElementDispatchResult -->
<h3>New Type TVMLKit.TVViewElementDispatchResult</h3>
<pre class='added' data-is-non-breaking="">
public class TVViewElementDispatchResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVViewElementDispatchResult (bool isDispatched, bool isCancelled);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsCancelled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDispatched { get; set; }</span>
}
</pre>
</div> <!-- end type TVViewElementDispatchResult -->

</div> <!-- end namespace TVMLKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;bool&gt; OpenUrlAsync (Foundation.NSUrl url, UIApplicationOpenUrlOptions options);</span>
</pre>
</div>

</div> <!-- end type UIApplication -->
<!-- start type UIEdgeInsets --> <div>
<h3>Type Changed: UIKit.UIEdgeInsets</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (UIEdgeInsets insets1, UIEdgeInsets insets2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (UIEdgeInsets insets1, UIEdgeInsets insets2);</span>
</pre>
</div>

</div> <!-- end type UIEdgeInsets -->
<!-- start type UIFocusAnimationCoordinator --> <div>
<h3>Type Changed: UIKit.UIFocusAnimationCoordinator</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedAnimationsAsync (System.Action animations);</span>
</pre>
</div>

</div> <!-- end type UIFocusAnimationCoordinator -->

</div> <!-- end namespace UIKit -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace NUnitLite.Runner --> <div> 
<h2>Namespace NUnitLite.Runner</h2>
<!-- start type TextUI --> <div>
<h3>Type Changed: NUnitLite.Runner.TextUI</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public void TopLevelHandler (object sender, System.UnhandledExceptionEventArgs e);</span>
</pre>

</div> <!-- end type TextUI -->

</div> <!-- end namespace NUnitLite.Runner -->
</div>



   


 <hr>
