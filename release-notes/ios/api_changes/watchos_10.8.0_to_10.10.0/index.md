---
id: 4F0755DB-A593-4199-882D-8E48C9E4FE10
title: "watchOS 10.8.0 to 10.10.0"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.WatchOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.WatchOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.WatchOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.WatchOS/System.Data.html)

   


 [System.IO.Compression.FileSystem.dll](#diff/xi/Xamarin.WatchOS/System.IO.Compression.FileSystem.html)

   


 [Xamarin.WatchOS.dll](#diff/xi/Xamarin.WatchOS/Xamarin.WatchOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.WatchOS/MonoTouch.NUnitLite.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.WatchOS/mscorlib.html'>mscorlib.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.WatchOS/System.html'>System.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.WatchOS/System.Core.html'>System.Core.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.WatchOS/System.Data.html'>System.Data.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.WatchOS/System.IO.Compression.FileSystem.html'>System.IO.Compression.FileSystem.dll</h1>

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
</script><h1 id='diff/xi/Xamarin.WatchOS/Xamarin.WatchOS.html'>Xamarin.WatchOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAudioPlayer --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual AVAudioFormat Format { get; }</span>
</pre>

</div> <!-- end type AVAudioPlayer -->
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

</div> <!-- end namespace AVFoundation -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContainer --> <div>
<h3>Type Changed: Contacts.CNContainer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainerOfContact (string contactIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainerOfGroup (string groupIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainers (string[] identifiers);</span>
</pre>
</div>

</div> <!-- end type CNContainer -->
<!-- start type CNContainer_PredicatesExtension --> <div>
<h3>Type Changed: Contacts.CNContainer_PredicatesExtension</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainerOfContact instead")]
	public static Foundation.NSPredicate GetPredicateForContainerOfContact (CNContainer This, string contactIdentifier);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainerOfGroup instead")]
	public static Foundation.NSPredicate GetPredicateForContainerOfGroup (CNContainer This, string groupIdentifier);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainers instead")]
	public static Foundation.NSPredicate GetPredicateForContainers (CNContainer This, string[] identifiers);</span>
</div></pre>

</div> <!-- end type CNContainer_PredicatesExtension -->
<!-- start type CNGroup --> <div>
<h3>Type Changed: Contacts.CNGroup</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForGroups (string[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForGroupsInContainer (string containerIdentifier);</span>
</pre>
</div>

</div> <!-- end type CNGroup -->
<!-- start type CNGroup_PredicatesExtension --> <div>
<h3>Type Changed: Contacts.CNGroup_PredicatesExtension</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNGroup.CreatePredicateForGroups instead")]
	public static Foundation.NSPredicate GetPredicateForGroups (CNGroup This, string[] identifiers);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNGroup.CreatePredicateForGroupsInContainer instead")]
	public static Foundation.NSPredicate GetPredicateForGroupsInContainer (CNGroup This, string containerIdentifier);</span>
</div></pre>

</div> <!-- end type CNGroup_PredicatesExtension -->

</div> <!-- end namespace Contacts -->
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
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKIdentityVerificationSignatureResult&gt; GenerateIdentityVerificationSignatureAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer -->
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
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INPreferences --> <div>
<h3>Type Changed: Intents.INPreferences</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INPreferences ();</span>
</pre>
</div>

</div> <!-- end type INPreferences -->

</div> <!-- end namespace Intents -->
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
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKPassLibrary --> <div>
<h3>Type Changed: PassKit.PKPassLibrary</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;PKPassLibraryAddPassesStatus&gt; AddPassesAsync (PKPass[] passes);</span>
</pre>
</div>

</div> <!-- end type PKPassLibrary -->

</div> <!-- end namespace PassKit -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
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
<h3>Removed Type <span class='breaking' data-is-breaking="">SpriteKit.SKVideoNode</span></h3>
</div> <!-- end namespace SpriteKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
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

</div> <!-- end namespace UIKit -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKInterfaceController --> <div>
<h3>Type Changed: WatchKit.WKInterfaceController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentAddPassesControllerAsync (PassKit.PKPass[] passes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; PresentAudioRecorderControllerAsync (Foundation.NSUrl outputUrl, WKAudioRecorderPreset preset, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKPresentMediaPlayerResult&gt; PresentMediaPlayerControllerAsync (Foundation.NSUrl url, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSArray&gt; PresentTextInputControllerAsync (System.Func&lt;Foundation.NSString,Foundation.NSArray&gt; suggestionsHandler, WKTextInputMode inputMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSArray&gt; PresentTextInputControllerAsync (string[] suggestions, WKTextInputMode inputMode);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceController -->
<!-- start type WKInterfaceSCNScene --> <div>
<h3>Type Changed: WatchKit.WKInterfaceSCNScene</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SceneKit.SCNScene scene, SpriteKit.SKTransition transition, SceneKit.SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceSCNScene -->
<div> <!-- start type WKPresentMediaPlayerResult -->
<h3>New Type WatchKit.WKPresentMediaPlayerResult</h3>
<pre class='added' data-is-non-breaking="">
public class WKPresentMediaPlayerResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKPresentMediaPlayerResult (bool didPlayToEnd, double endTime);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool DidPlayToEnd { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double EndTime { get; set; }</span>
}
</pre>
</div> <!-- end type WKPresentMediaPlayerResult -->

</div> <!-- end namespace WatchKit -->
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
</script><h1 id='diff/xi/Xamarin.WatchOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

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
