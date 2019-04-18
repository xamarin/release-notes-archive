---
id: BD417C4E-1C2F-44AC-AE08-4394F9ED3C40
title: "Mac 3.4 to 3.8"
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
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<p>Obsoleted events:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-event' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanel2' on NSApplication.")]
	public event System.EventHandler OrderFrontStandardAboutPanel;</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-event' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanelWithOptions2' on NSApplication.")]
	public event System.EventHandler OrderFrontStandardAboutPanelWithOptions;</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-event' data-is-non-breaking="">[Obsolete ("Use the 'RegisterServicesMenu2' on NSApplication.")]
	public event System.EventHandler&lt;NSApplicationRegisterEventArgs&gt; RegisterServicesMenu;</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OrderFrontStandardAboutPanel2 (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OrderFrontStandardAboutPanelWithOptions2 (Foundation.NSDictionary optionsDictionary);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterServicesMenu2 (string[] sendTypes, string[] returnTypes);</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanel2' on NSApplication.")]
	public virtual void OrderFrontStandardAboutPanel (Foundation.NSObject sender);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanelWithOptions2' on NSApplication.")]
	public virtual void OrderFrontStandardAboutPanelWithOptions (Foundation.NSDictionary optionsDictionary);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'INSServicesMenuRequestor' protocol.")]
	public virtual bool ReadSelectionFromPasteboard (NSPasteboard pboard);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'RegisterServicesMenu2' on NSApplication.")]
	public virtual void RegisterServicesMenu (string[] sendTypes, string[] returnTypes);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'INSServicesMenuRequestor' protocol.")]
	public virtual bool WriteSelectionToPasteboard (NSPasteboard board, string[] types);</span>
</div></pre>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanel2' on NSApplication.")]
	public static void OrderFrontStandardAboutPanel (INSApplicationDelegate This, Foundation.NSObject sender);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'OrderFrontStandardAboutPanelWithOptions2' on NSApplication.")]
	public static void OrderFrontStandardAboutPanelWithOptions (INSApplicationDelegate This, Foundation.NSDictionary optionsDictionary);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'INSServicesMenuRequestor' protocol.")]
	public static bool ReadSelectionFromPasteboard (INSApplicationDelegate This, NSPasteboard pboard);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'RegisterServicesMenu2' on NSApplication.")]
	public static void RegisterServicesMenu (INSApplicationDelegate This, string[] sendTypes, string[] returnTypes);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'INSServicesMenuRequestor' protocol.")]
	public static bool WriteSelectionToPasteboard (INSApplicationDelegate This, NSPasteboard board, string[] types);</span>
</div></pre>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<div> <!-- start type INSServicesMenuRequestor -->
<h3>New Type AppKit.INSServicesMenuRequestor</h3>
<pre class='added' data-is-non-breaking="">
public interface INSServicesMenuRequestor : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSServicesMenuRequestor -->
<div> <!-- start type NSServicesMenuRequestor_Extensions -->
<h3>New Type AppKit.NSServicesMenuRequestor_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSServicesMenuRequestor_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ReadSelectionFromPasteboard (INSServicesMenuRequestor This, NSPasteboard pboard);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteSelectionToPasteboard (INSServicesMenuRequestor This, NSPasteboard pboard, string[] types);</span>
}
</pre>
</div> <!-- end type NSServicesMenuRequestor_Extensions -->

</div> <!-- end namespace AppKit -->
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
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.6.0"</span> <span class='added '>"3.8.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKUIDelegate --> <div>
<h3>Type Changed: WebKit.WKUIDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RunOpenPanel (WKWebView webView, WKOpenPanelParameters parameters, WKFrameInfo frame, System.Action&lt;Foundation.NSUrl[]&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type WKUIDelegate -->
<!-- start type WKUIDelegate_Extensions --> <div>
<h3>Type Changed: WebKit.WKUIDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void RunOpenPanel (IWKUIDelegate This, WKWebView webView, WKOpenPanelParameters parameters, WKFrameInfo frame, System.Action&lt;Foundation.NSUrl[]&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type WKUIDelegate_Extensions -->
<div> <!-- start type WKOpenPanelParameters -->
<h3>New Type WebKit.WKOpenPanelParameters</h3>
<pre class='added' data-is-non-breaking="">
public class WKOpenPanelParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKOpenPanelParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKOpenPanelParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKOpenPanelParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsMultipleSelection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type WKOpenPanelParameters -->

</div> <!-- end namespace WebKit -->
</div>
