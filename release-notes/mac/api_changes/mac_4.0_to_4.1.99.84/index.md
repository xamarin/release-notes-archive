---
id: C14CCC4B-1194-4100-B450-A7A249DEF12F
title: "Mac 4.0 to 4.1.99.84"
---

# API diff

 [(Classic profile) XamMac.dll](#diff/xm/XamMac.html)

   


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
</script><h1 id='diff/xm/XamMac.html'>XamMac.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoMac --> <div> 
<h2>Namespace MonoMac</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"4.1.1"</span> <span class='added '>"4.1.99"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoMac -->
<!-- start namespace MonoMac.AVFoundation --> <div> 
<h2>Namespace MonoMac.AVFoundation</h2>
<!-- start type AVAudioUnitComponentManager --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioUnitComponentManager</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Please use the static 'SharedInstance' property as this type is not meant to be created.")]
	public AVAudioUnitComponentManager ();</span>
</div></pre>

</div> <!-- end type AVAudioUnitComponentManager -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ulong PreferredVideoDecoderGpuRegistryId { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->

</div> <!-- end namespace MonoMac.AVFoundation -->
<!-- start namespace MonoMac.AudioUnit --> <div> 
<h2>Namespace MonoMac.AudioUnit</h2>
<!-- start type AudioUnitStatus --> <div>
<h3>Type Changed: MonoMac.AudioUnit.AudioUnitStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidParameterValue = -66743,</span>
</pre>
</div>

</div> <!-- end type AudioUnitStatus -->

</div> <!-- end namespace MonoMac.AudioUnit -->
<!-- start namespace MonoMac.CloudKit --> <div> 
<h2>Namespace MonoMac.CloudKit</h2>
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: MonoMac.CloudKit.CKErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AssetNotAvailable = 35,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->

</div> <!-- end namespace MonoMac.CloudKit -->
<!-- start namespace MonoMac.ImageIO --> <div> 
<h2>Namespace MonoMac.ImageIO</h2>
<!-- start type CGImageMetadataTagNamespaces --> <div>
<h3>Type Changed: MonoMac.ImageIO.CGImageMetadataTagNamespaces</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagNamespaces -->
<!-- start type CGImageMetadataTagPrefixes --> <div>
<h3>Type Changed: MonoMac.ImageIO.CGImageMetadataTagPrefixes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagPrefixes -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: MonoMac.ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAboutCvTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAboutCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAboutCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAboutCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAboutCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAddlModelInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkContentDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkContributionDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCopyrightNotice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCopyrightOwnerId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCopyrightOwnerName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkCreatorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkLicensorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkLicensorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkOrObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkPhysicalDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkSourceInvUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkSourceInventoryNo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtArtworkTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAudioBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAudioBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtAudioChannelCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContainerFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContainerFormatIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContainerFormatName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContributor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContributorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContributorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtContributorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtControlledVocabularyTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCopyrightYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCreatorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCreatorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtCreatorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionH { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionW { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDataOnScreenRegionY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDigitalImageGuid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDigitalSourceFileType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDigitalSourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDopesheet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDopesheetLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDopesheetLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtDopesheetLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEmbdEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEmbeddedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEmbeddedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEmbeddedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEpisode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEpisodeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEpisodeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEpisodeNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtExternalMetadataLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtFeedIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtGenre { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtGenreCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtGenreCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtGenreCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtGenreCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtHeadline { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtIPTCLastEdited { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLinkedEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLinkedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLinkedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLinkedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationShown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtLocationWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtMaxAvailHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtMaxAvailWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtModelAge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtOrganisationInImageCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtOrganisationInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonHeard { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonHeardIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonHeardName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageCharacteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPersonInImageWDetails { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtProductInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtProductInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtProductInImageGtin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtProductInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPublicationEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPublicationEventDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPublicationEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtPublicationEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRating { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRatingRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingRegionWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingScaleMaxValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingScaleMinValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingSourceLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRatingValueLogoLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRegistryEntryRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRegistryItemId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtRegistryOrganisationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtReleaseReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeasonIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeasonName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeasonNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeriesIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSeriesName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtShownEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtShownEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtShownEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtStorylineIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtStreamReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSupplyChainSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSupplyChainSourceIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtSupplyChainSourceName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTemporalCoverage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTemporalCoverageFrom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTemporalCoverageTo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTranscript { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTranscriptLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTranscriptLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtTranscriptLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoDisplayAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoEncodingProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoShotType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoShotTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoShotTypeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVideoStreamsCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtVisualColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtWorkflowTag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtWorkflowTagCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtWorkflowTagCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtWorkflowTagCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString IPTCExtWorkflowTagCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString OpenExrAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString OpenExrDictionary { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace MonoMac.ImageIO -->
<!-- start namespace MonoMac.Security --> <div> 
<h2>Namespace MonoMac.Security</h2>
<!-- start type SslStatus --> <div>
<h3>Type Changed: MonoMac.Security.SslStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SSLBadCertificateStatusResponse = -9862,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLCertificateRequired = -9863,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLConfigurationFailed = -9854,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecodeError = -9859,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecompressFail = -9857,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLHandshakeFail = -9858,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLInappropriateFallback = -9860,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLMissingExtension = -9861,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLNetworkTimeout = -9853,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLTransportReset = -9852,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnexpectedMessage = -9856,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnknownPskIdentity = -9864,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnrecognizedName = -9865,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnsupportedExtension = -9855,</span>
</pre>
</div>

</div> <!-- end type SslStatus -->
<div> <!-- start type SecStatusCodeExtensions -->
<h3>New Type MonoMac.Security.SecStatusCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecStatusCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetStatusDescription (SecStatusCode status);</span>
}
</pre>
</div> <!-- end type SecStatusCodeExtensions -->

</div> <!-- end namespace MonoMac.Security -->
<!-- start namespace MonoMac.VideoToolbox --> <div> 
<h2>Namespace MonoMac.VideoToolbox</h2>
<!-- start type VTVideoDecoderSpecification --> <div>
<h3>Type Changed: MonoMac.VideoToolbox.VTVideoDecoderSpecification</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MonoMac.Foundation.NSNumber PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MonoMac.Foundation.NSNumber RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecification -->
<!-- start type VTVideoDecoderSpecificationKeys --> <div>
<h3>Type Changed: MonoMac.VideoToolbox.VTVideoDecoderSpecificationKeys</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MonoMac.Foundation.NSString RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecificationKeys -->

</div> <!-- end namespace MonoMac.VideoToolbox -->
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
<!-- start type AVAudioUnitComponentManager --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponentManager</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Please use the static 'SharedInstance' property as this type is not meant to be created.")]
	public AVAudioUnitComponentManager ();</span>
</div></pre>

</div> <!-- end type AVAudioUnitComponentManager -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ulong PreferredVideoDecoderGpuRegistryId { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AudioUnitStatus --> <div>
<h3>Type Changed: AudioUnit.AudioUnitStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidParameterValue = -66743,</span>
</pre>
</div>

</div> <!-- end type AudioUnitStatus -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: CloudKit.CKErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AssetNotAvailable = 35,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor DetectedBarcodeDescriptor { get; }</span>
</pre>
</div>

</div> <!-- end type NSUserActivity -->

</div> <!-- end namespace Foundation -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageMetadataTagNamespaces --> <div>
<h3>Type Changed: ImageIO.CGImageMetadataTagNamespaces</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagNamespaces -->
<!-- start type CGImageMetadataTagPrefixes --> <div>
<h3>Type Changed: ImageIO.CGImageMetadataTagPrefixes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagPrefixes -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAddlModelInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkContentDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkContributionDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightNotice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightOwnerId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightOwnerName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCreatorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkLicensorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkLicensorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkOrObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkPhysicalDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSourceInvUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSourceInventoryNo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioChannelCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormatIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormatName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtControlledVocabularyTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCopyrightYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionH { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionW { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalImageGuid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalSourceFileType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalSourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbdEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtExternalMetadataLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtFeedIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenre { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtHeadline { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtIPTCLastEdited { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationShown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtMaxAvailHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtMaxAvailWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtModelAge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtOrganisationInImageCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtOrganisationInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeard { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeardIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeardName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCharacteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageWDetails { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageGtin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRating { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRatingRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingScaleMaxValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingScaleMinValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingSourceLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingValueLogoLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryEntryRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryItemId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryOrganisationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtReleaseReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeriesIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeriesName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStorylineIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStreamReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSourceIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSourceName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverageFrom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverageTo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscript { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoDisplayAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoEncodingProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotTypeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoStreamsCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVisualColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrDictionary { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INSpeakableString --> <div>
<h3>Type Changed: Intents.INSpeakableString</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (Foundation.NSCoder coder);</span>
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

</div> <!-- end type INSpeakableString -->

</div> <!-- end namespace Intents -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"4.1.1"</span> <span class='added '>"4.1.99"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariExtensionHandler --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandler</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AdditionalRequestHeaders (Foundation.NSUrl url, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSString&gt;&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandler -->
<!-- start type SFSafariExtensionHandling_Extensions --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void AdditionalRequestHeaders (ISFSafariExtensionHandling This, Foundation.NSUrl url, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSString&gt;&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandling_Extensions -->

</div> <!-- end namespace SafariServices -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslStatus --> <div>
<h3>Type Changed: Security.SslStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SSLBadCertificateStatusResponse = -9862,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLCertificateRequired = -9863,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLConfigurationFailed = -9854,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecodeError = -9859,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecompressFail = -9857,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLHandshakeFail = -9858,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLInappropriateFallback = -9860,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLMissingExtension = -9861,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLNetworkTimeout = -9853,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLTransportReset = -9852,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnexpectedMessage = -9856,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnknownPskIdentity = -9864,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnrecognizedName = -9865,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnsupportedExtension = -9855,</span>
</pre>
</div>

</div> <!-- end type SslStatus -->
<div> <!-- start type SecStatusCodeExtensions -->
<h3>New Type Security.SecStatusCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecStatusCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetStatusDescription (SecStatusCode status);</span>
}
</pre>
</div> <!-- end type SecStatusCodeExtensions -->

</div> <!-- end namespace Security -->
<!-- start namespace VideoToolbox --> <div> 
<h2>Namespace VideoToolbox</h2>
<!-- start type VTVideoDecoderSpecification --> <div>
<h3>Type Changed: VideoToolbox.VTVideoDecoderSpecification</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecification -->
<!-- start type VTVideoDecoderSpecificationKeys --> <div>
<h3>Type Changed: VideoToolbox.VTVideoDecoderSpecificationKeys</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecificationKeys -->

</div> <!-- end namespace VideoToolbox -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKOpenPanelParameters --> <div>
<h3>Type Changed: WebKit.WKOpenPanelParameters</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDirectories { get; }</span>
</pre>
</div>

</div> <!-- end type WKOpenPanelParameters -->
<!-- start type WKPreferences --> <div>
<h3>Type Changed: WebKit.WKPreferences</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKPreferences -->
<!-- start type WKProcessPool --> <div>
<h3>Type Changed: WebKit.WKProcessPool</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKProcessPool -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WKWebsiteDataType --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FetchCache { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceWorkerRegistrations { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataType -->

</div> <!-- end namespace WebKit -->
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
<!-- start type AVAudioUnitComponentManager --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponentManager</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Please use the static 'SharedInstance' property as this type is not meant to be created.")]
	public AVAudioUnitComponentManager ();</span>
</div></pre>

</div> <!-- end type AVAudioUnitComponentManager -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ulong PreferredVideoDecoderGpuRegistryId { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AudioUnitStatus --> <div>
<h3>Type Changed: AudioUnit.AudioUnitStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidParameterValue = -66743,</span>
</pre>
</div>

</div> <!-- end type AudioUnitStatus -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: CloudKit.CKErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AssetNotAvailable = 35,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor DetectedBarcodeDescriptor { get; }</span>
</pre>
</div>

</div> <!-- end type NSUserActivity -->

</div> <!-- end namespace Foundation -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageMetadataTagNamespaces --> <div>
<h3>Type Changed: ImageIO.CGImageMetadataTagNamespaces</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagNamespaces -->
<!-- start type CGImageMetadataTagPrefixes --> <div>
<h3>Type Changed: ImageIO.CGImageMetadataTagPrefixes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtension { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageMetadataTagPrefixes -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAboutCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAddlModelInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkContentDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkContributionDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightNotice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightOwnerId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCopyrightOwnerName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkCreatorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkLicensorId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkLicensorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkOrObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkPhysicalDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSourceInvUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkSourceInventoryNo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtArtworkTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtAudioChannelCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCircaDateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormatIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContainerFormatName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtContributorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtControlledVocabularyTerm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCopyrightYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtCreatorRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionH { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionW { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDataOnScreenRegionY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalImageGuid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalSourceFileType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDigitalSourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtDopesheetLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbdEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEmbeddedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEpisodeNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtExternalMetadataLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtFeedIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenre { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtGenreCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtHeadline { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtIPTCLastEdited { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExpr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExprLangId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLinkedEncodedRightsExprType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationShown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtLocationWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtMaxAvailHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtMaxAvailWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtModelAge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtOrganisationInImageCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtOrganisationInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeard { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeardIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonHeardName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCharacteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPersonInImageWDetails { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageGtin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtProductInImageName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtPublicationEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRating { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRatingRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCountryCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionCountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsAltitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionGpsLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionLocationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionLocationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionProvinceState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionSublocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingRegionWorldRegion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingScaleMaxValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingScaleMinValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingSourceLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRatingValueLogoLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryEntryRole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryItemId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtRegistryOrganisationId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtReleaseReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeasonNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeriesIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSeriesName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEvent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEventIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtShownEventName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStorylineIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStreamReady { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtStylePeriod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSourceIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtSupplyChainSourceName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverageFrom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTemporalCoverageTo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscript { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLinkLink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtTranscriptLinkLinkQualifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoBitrateMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoDisplayAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoEncodingProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoShotTypeName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVideoStreamsCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtVisualColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IPTCExtWorkflowTagCvTermRefinedAbout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrDictionary { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INSpeakableString --> <div>
<h3>Type Changed: Intents.INSpeakableString</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (Foundation.NSCoder coder);</span>
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

</div> <!-- end type INSpeakableString -->

</div> <!-- end namespace Intents -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"4.1.1"</span> <span class='added '>"4.1.99"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariExtensionHandler --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandler</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AdditionalRequestHeaders (Foundation.NSUrl url, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSString&gt;&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandler -->
<!-- start type SFSafariExtensionHandling_Extensions --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void AdditionalRequestHeaders (ISFSafariExtensionHandling This, Foundation.NSUrl url, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSString&gt;&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandling_Extensions -->

</div> <!-- end namespace SafariServices -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslStatus --> <div>
<h3>Type Changed: Security.SslStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SSLBadCertificateStatusResponse = -9862,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLCertificateRequired = -9863,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLConfigurationFailed = -9854,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecodeError = -9859,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLDecompressFail = -9857,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLHandshakeFail = -9858,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLInappropriateFallback = -9860,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLMissingExtension = -9861,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLNetworkTimeout = -9853,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLTransportReset = -9852,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnexpectedMessage = -9856,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnknownPskIdentity = -9864,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnrecognizedName = -9865,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLUnsupportedExtension = -9855,</span>
</pre>
</div>

</div> <!-- end type SslStatus -->
<div> <!-- start type SecStatusCodeExtensions -->
<h3>New Type Security.SecStatusCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecStatusCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetStatusDescription (SecStatusCode status);</span>
}
</pre>
</div> <!-- end type SecStatusCodeExtensions -->

</div> <!-- end namespace Security -->
<!-- start namespace VideoToolbox --> <div> 
<h2>Namespace VideoToolbox</h2>
<!-- start type VTVideoDecoderSpecification --> <div>
<h3>Type Changed: VideoToolbox.VTVideoDecoderSpecification</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecification -->
<!-- start type VTVideoDecoderSpecificationKeys --> <div>
<h3>Type Changed: VideoToolbox.VTVideoDecoderSpecificationKeys</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PreferredDecoderGpuRegistryId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RequiredDecoderGpuRegistryId { get; }</span>
</pre>
</div>

</div> <!-- end type VTVideoDecoderSpecificationKeys -->

</div> <!-- end namespace VideoToolbox -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKOpenPanelParameters --> <div>
<h3>Type Changed: WebKit.WKOpenPanelParameters</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDirectories { get; }</span>
</pre>
</div>

</div> <!-- end type WKOpenPanelParameters -->
<!-- start type WKPreferences --> <div>
<h3>Type Changed: WebKit.WKPreferences</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKPreferences -->
<!-- start type WKProcessPool --> <div>
<h3>Type Changed: WebKit.WKProcessPool</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKProcessPool -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WKWebsiteDataType --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FetchCache { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceWorkerRegistrations { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataType -->

</div> <!-- end namespace WebKit -->
</div>



   


 <hr>
