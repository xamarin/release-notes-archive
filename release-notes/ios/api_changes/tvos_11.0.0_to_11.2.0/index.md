---
id: 88E0E482-0233-474F-93A6-4581E426D725
title: "tvOS 11.0.0 to 11.2.0"
---

# API diff

 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


   


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
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<div> <!-- start type MPMediaType -->
<h3>New Type MediaPlayer.MPMediaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPMediaType {
	<span class='added added-field ' data-is-non-breaking="">Any = 18446744073709551615,</span>
	<span class='added added-field ' data-is-non-breaking="">AnyAudio = 255,</span>
	<span class='added added-field ' data-is-non-breaking="">AudioBook = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AudioITunesU = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeVideo = 8192,</span>
	<span class='added added-field ' data-is-non-breaking="">Movie = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Music = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MusicVideo = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Podcast = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TVShow = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TypeAnyVideo = 65280,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoITunesU = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoPodcast = 1024,</span>
}
</pre>
</div> <!-- end type MPMediaType -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.0.0"</span> <span class='added '>"11.2.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
</div>



   


 <hr>
