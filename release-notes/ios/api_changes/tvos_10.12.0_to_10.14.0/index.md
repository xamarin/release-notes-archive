---
id: 84BA0790-5ABE-4844-939D-5051BC8150E8
title: "tvOS 10.12.0 to 10.14.0"
---

# API diff

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
</script><h1 id='diff/xi/Xamarin.TVOS/Xamarin.TVOS.html'>Xamarin.TVOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfo NowPlaying { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<div> <!-- start type MPMediaItem -->
<h3>New Type MediaPlayer.MPMediaItem</h3>
<pre class='added' data-is-non-breaking="">
public static class MPMediaItem {
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
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RatingProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReleaseDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SkipCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserGroupingProperty { get; }</span>
}
</pre>
</div> <!-- end type MPMediaItem -->
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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.12.0"</span> <span class='added '>"10.14.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
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
<!-- start namespace MonoTouch.NUnit --> <div> 
<h2>Namespace MonoTouch.NUnit</h2>
<!-- start type NUnitOutputTextWriter --> <div>
<h3>Type Changed: MonoTouch.NUnit.NUnitOutputTextWriter</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter, UI.XmlMode xmlMode);</span>
</pre>
</div>

</div> <!-- end type NUnitOutputTextWriter -->

</div> <!-- end namespace MonoTouch.NUnit -->
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string LogFile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public XmlMode XmlMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->
<div> <!-- start type XmlMode -->
<h3>New Type MonoTouch.NUnit.UI.XmlMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum XmlMode {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Wrapped = 1,</span>
}
</pre>
</div> <!-- end type XmlMode -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
</div>



   


 <hr>
