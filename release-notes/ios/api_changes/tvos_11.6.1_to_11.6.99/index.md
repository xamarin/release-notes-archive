---
id: 1BBB2CE4-BA75-4C92-9069-B3919FD9E55B
title: "tvOS 11.6.1 to 11.6.99"
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

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVDisplayManager --> <div>
<h3>Type Changed: AVKit.AVDisplayManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplayCriteriaMatchingEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ModeSwitchEndNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ModeSwitchSettingsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ModeSwitchStartNotification { get; }</span>
</pre>
</div>

</div> <!-- end type AVDisplayManager -->

</div> <!-- end namespace AVKit -->
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
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessory --> <div>
<h3>Type Changed: HomeKit.HMAccessory</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsIdentify { get; }</span>
</pre>
</div>

</div> <!-- end type HMAccessory -->

</div> <!-- end namespace HomeKit -->
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
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"11.2"</span> <span class='added '>"11.3"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.6.1"</span> <span class='added '>"11.6.99"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
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
<!-- start namespace VideoSubscriberAccount --> <div> 
<h2>Namespace VideoSubscriberAccount</h2>
<!-- start type VSSubscription --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSSubscription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BillingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type VSSubscription -->

</div> <!-- end namespace VideoSubscriberAccount -->
</div>



   


 <hr>
