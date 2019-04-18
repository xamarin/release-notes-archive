---
id: 7BD26AB5-6438-45F2-AFF2-C5680737E076
title: "iOS to tvOS"
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
</script># Xamarin.iOS.dll

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAsset --> <div>
<h3>Type Changed: AVFoundation.AVAsset</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetChapterMetadataGroups")]
	public virtual AVMetadataItem[] ChapterMetadataGroups (Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);</span>
</pre>

</div> <!-- end type AVAsset -->
<!-- start type AVAssetTrack --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetAssociatedTracks")]
	public virtual Foundation.NSString GetAssociatedTracksOfType (Foundation.NSString avAssetTrackTrackAssociationType);</span>
</pre>

</div> <!-- end type AVAssetTrack -->
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual AVAudioInputNode InputNode { get; }</span>
</pre>

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioPlayerDelegate --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerDelegate</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);</span>
</pre>

</div> <!-- end type AVAudioPlayerDelegate -->
<!-- start type AVAudioPlayerDelegate_Extensions --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerDelegate_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void EndInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);</span>
</pre>

</div> <!-- end type AVAudioPlayerDelegate_Extensions -->
<!-- start type AVAudioSession --> <div>
<h3>Type Changed: AVFoundation.AVAudioSession</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CategoryAudioProcessing { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nint CurrentHardwareInputNumberOfChannels { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nint CurrentHardwareOutputNumberOfChannels { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double CurrentHardwareSampleRate { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public IAVAudioSessionDelegate Delegate { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool InputIsAvailable { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double PreferredHardwareSampleRate { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual AVAudioSessionRecordPermission RecordPermission { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Deprecated since iOS 6, Use AVAudioSession.Notification.ObserveInterruptionInstead")]
	public event System.EventHandler BeginInterruption;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Deprecated since iOS 6, Use AVAudioSession.Notification.ObserveAudioRouteChange")]
	public event System.EventHandler&lt;AVCategoryEventArgs&gt; CategoryChanged;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Deprecated since iOS 6, Use AVAudioSession.Notification.ObserveInterruptionInstead")]
	public event System.EventHandler EndInterruption;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Deprecated since iOS 6, Use AVAudioSession.Notification.ObserveAudioRouteChange")]
	public event System.EventHandler&lt;AVStatusEventArgs&gt; InputAvailabilityChanged;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Use AVAudioSession.Notification.ObserveAudioRouteChange, this event does nothing")]
	public event System.EventHandler&lt;AVChannelsEventArgs&gt; InputChannelsChanged;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Use AVAudioSession.Notification.ObserveAudioRouteChange, this event does nothing")]
	public event System.EventHandler&lt;AVChannelsEventArgs&gt; OutputChannelsChanged;</span>

	<span class='removed removed-event breaking' data-is-breaking="">[Obsolete ("Deprecated since iOS 6, Use AVAudioSession.Notification.ObserveAudioRouteChange")]
	public event System.EventHandler&lt;AVSampleRateEventArgs&gt; SampleRateChanged;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RequestRecordPermission (AVPermissionGranted responseCallback);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public Foundation.NSError SetActive (bool active, AVAudioSessionSetActiveOptions options);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool SetActive (bool beActive, AVAudioSessionFlags flags, out Foundation.NSError outError);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool SetPreferredHardwareSampleRate (double sampleRate, out Foundation.NSError outError);</span>
</pre>

</div> <!-- end type AVAudioSession -->
<!-- start type AVAudioSessionPortDescription --> <div>
<h3>Type Changed: AVFoundation.AVAudioSessionPortDescription</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">[Obsolete ("Use DataSourceDescriptions instead")]
	public virtual AVAudioSessionChannelDescription[] DataSources { get; }</span>
</pre>

</div> <!-- end type AVAudioSessionPortDescription -->
<!-- start type AVMediaType --> <div>
<h3>Type Changed: AVFoundation.AVMediaType</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TimedMetadata { get; }</span>
</pre>

</div> <!-- end type AVMediaType -->
<!-- start type AVMusicTrack --> <div>
<h3>Type Changed: AVFoundation.AVMusicTrack</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint DestinationMidiEndpoint { get; set; }</span>
</pre>

</div> <!-- end type AVMusicTrack -->
<!-- start type AVMutableCompositionTrack --> <div>
<h3>Type Changed: AVFoundation.AVMutableCompositionTrack</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use InsertTimeRanges overload accepting an NSValue array")]
	public virtual bool InsertTimeRanges (Foundation.NSValue cmTimeRanges, AVAssetTrack[] tracks, CoreMedia.CMTime startTime, out Foundation.NSError error);</span>
</pre>

</div> <!-- end type AVMutableCompositionTrack -->
<!-- start type AVOutputSettingsAssistant --> <div>
<h3>Type Changed: AVFoundation.AVOutputSettingsAssistant</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public AVOutputSettingsAssistant Preset1280x720 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public AVOutputSettingsAssistant Preset1920x1080 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public AVOutputSettingsAssistant Preset3840x2160 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public AVOutputSettingsAssistant Preset640x480 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public AVOutputSettingsAssistant Preset960x540 { get; }</span>
</pre>

</div> <!-- end type AVOutputSettingsAssistant -->
<!-- start type AVPlayerItem --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVMetadataItem[] ExternalMetadata { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVKit.AVInterstitialTimeRange[] InterstitialTimeRanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVKit.AVNavigationMarkersGroup[] NavigationMarkerGroups { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItem -->
<!-- start type AVPlayerItemMetadataCollector --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemMetadataCollector</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public AVPlayerItemMetadataCollector ();</span>
</pre>

</div> <!-- end type AVPlayerItemMetadataCollector -->
<!-- start type AVTextStyleRule --> <div>
<h3>Type Changed: AVFoundation.AVTextStyleRule</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public AVTextStyleRule ();</span>
</pre>

</div> <!-- end type AVTextStyleRule -->
<h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioRecorder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioRecorderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioRecorderDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioSessionDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioSessionFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioSessionInterruptionFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAudioSessionRecordPermission</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAudioChannel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAudioDataOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAutoExposureBracketedStillImageSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAutoFocusRangeRestriction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureAutoFocusSystem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureBracketedStillImageSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureConnection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureDevice</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureDeviceFormat</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureDeviceInput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureDevicePosition</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureDeviceTransportControlsPlaybackMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureExposureMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureFileOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureFileOutputRecordingDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureFlashMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureFocusMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureInput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureInputPort</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureManualExposureBracketedStillImageSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureMetadataInput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureMetadataOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureMetadataOutputObjectsDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureMetadataOutputObjectsDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureMovieFileOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureSessionInterruptionReason</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureSessionRuntimeErrorEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureStillImageOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureTorchMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoDataOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoOrientation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoPreviewLayer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureVideoStabilizationMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVCaptureWhiteBalanceMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVFrameRateRange</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVMetadataFaceObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVMetadataMachineReadableCodeObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVMetadataObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVPermissionGranted</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVQueuedSampleBufferRenderingStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVRequestAccessStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVSampleBufferDisplayLayer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.AVVideoFieldMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVAudioRecorderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVAudioSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVCaptureAudioDataOutputSampleBufferDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVCaptureFileOutputRecordingDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVCaptureMetadataOutputObjectsDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVFoundation.IAVCaptureVideoDataOutputSampleBufferDelegate</span></h3>
</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool AllowsPictureInPicturePlayback { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGRect VideoBounds { get; }</span>
</pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AllowedSubtitleOptionLanguages { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFullSubtitles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresLinearPlayback { get; set; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void PrepareForPrerollAds ();</span>
</pre>

</div> <!-- end type AVPlayerViewController -->
<!-- start type AVPlayerViewControllerDelegate --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidStartPictureInPicture (AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidStopPictureInPicture (AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FailedToStartPictureInPicture (AVPlayerViewController playerViewController, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RestoreUserInterfaceForPictureInPicture (AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldAutomaticallyDismissAtPictureInPictureStart (AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillStartPictureInPicture (AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillStopPictureInPicture (AVPlayerViewController playerViewController);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidPresentInterstitialTimeRange (AVPlayerViewController playerViewController, AVInterstitialTimeRange interstitial);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectExternalSubtitleOptionLanguage (AVPlayerViewController playerViewController, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectMediaSelectionOption (AVPlayerViewController playerViewController, AVFoundation.AVMediaSelectionOption mediaSelectionOption, AVFoundation.AVMediaSelectionGroup mediaSelectionGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillPresentInterstitialTimeRange (AVPlayerViewController playerViewController, AVInterstitialTimeRange interstitial);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillResumePlaybackAfterUserNavigatedFromTime (AVPlayerViewController playerViewController, CoreMedia.CMTime oldTime, CoreMedia.CMTime targetTime);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate -->
<!-- start type AVPlayerViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void FailedToStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RestoreUserInterfaceForPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool ShouldAutomaticallyDismissAtPictureInPictureStart (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillStartPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillStopPictureInPicture (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidPresentInterstitialTimeRange (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, AVInterstitialTimeRange interstitial);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectExternalSubtitleOptionLanguage (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectMediaSelectionOption (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, AVFoundation.AVMediaSelectionOption mediaSelectionOption, AVFoundation.AVMediaSelectionGroup mediaSelectionGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillPresentInterstitialTimeRange (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, AVInterstitialTimeRange interstitial);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillResumePlaybackAfterUserNavigatedFromTime (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, CoreMedia.CMTime oldTime, CoreMedia.CMTime targetTime);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate_Extensions -->
<h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVKitError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVKitErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVPictureInPictureController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVPictureInPictureControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVPictureInPictureControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.AVPlayerViewControlsStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AVKit.IAVPictureInPictureControllerDelegate</span></h3><div> <!-- start type AVInterstitialTimeRange -->
<h3>New Type AVKit.AVInterstitialTimeRange</h3>
<pre class='added' data-is-non-breaking="">
public class AVInterstitialTimeRange : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVInterstitialTimeRange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVInterstitialTimeRange (CoreMedia.CMTimeRange timeRange);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVInterstitialTimeRange (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVInterstitialTimeRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVInterstitialTimeRange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTimeRange TimeRange { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type AVInterstitialTimeRange -->
<div> <!-- start type AVNavigationMarkersGroup -->
<h3>New Type AVKit.AVNavigationMarkersGroup</h3>
<pre class='added' data-is-non-breaking="">
public class AVNavigationMarkersGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVNavigationMarkersGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVNavigationMarkersGroup (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVNavigationMarkersGroup (string title, AVFoundation.AVDateRangeMetadataGroup[] navigationMarkers);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVNavigationMarkersGroup (string title, AVFoundation.AVTimedMetadataGroup[] navigationMarkers);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVDateRangeMetadataGroup[] DateRangeNavigationMarkers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVTimedMetadataGroup[] TimedNavigationMarkers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
}
</pre>
</div> <!-- end type AVNavigationMarkersGroup -->

</div> <!-- end namespace AVKit -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioQueue --> <div>
<h3>Type Changed: AudioToolbox.AudioQueue</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">[Obsolete ("Use AudioStreamDescription instead")]
	public AudioStreamBasicDescription AudioStreamPacketDescription { get; }</span>
</pre>

</div> <!-- end type AudioQueue -->
<!-- start type MusicSequence --> <div>
<h3>Type Changed: AudioToolbox.MusicSequence</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public MusicPlayerStatus SetMidiEndpoint (CoreMidi.MidiEndpoint endpoint);</span>
</pre>

</div> <!-- end type MusicSequence -->
<!-- start type MusicTrack --> <div>
<h3>Type Changed: AudioToolbox.MusicTrack</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public MusicPlayerStatus SetDestMidiEndpoint (CoreMidi.MidiEndpoint endpoint);</span>
</pre>

</div> <!-- end type MusicTrack -->
<h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.AccessoryInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.AudioSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.AudioSessionException</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.AudioSessionPropertyEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.AudioSessionRouteChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioToolbox.InputSourceInfo</span></h3>
</div> <!-- end namespace AudioToolbox -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RequestViewController (System.Action&lt;UIKit.UIViewController&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;UIKit.UIViewController&gt; RequestViewControllerAsync ();</span>
</pre>

</div> <!-- end type AUAudioUnit -->
<!-- start type AudioUnit --> <div>
<h3>Type Changed: AudioUnit.AudioUnit</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("This API is not available on iOS")]
	public static uint GetCurrentInputDevice ();</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use SetFormat instead as it has the ability of returning a status code")]
	public void SetAudioFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);</span>
</pre>

</div> <!-- end type AudioUnit -->
<h3>Removed Type <span class='breaking' data-is-breaking="">AudioUnit.AudioObjectPropertyElement</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioUnit.AudioObjectPropertyScope</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioUnit.AudioObjectPropertySelector</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AudioUnit.AudioUnitPropertyIDType</span></h3>
</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKContainer --> <div>
<h3>Type Changed: CloudKit.CKContainer</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DiscoverAllContactUserInfos (System.Action&lt;CKDiscoveredUserInfo[],Foundation.NSError&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;CKDiscoveredUserInfo[]&gt; DiscoverAllContactUserInfosAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FetchAllLongLivedOperationIDs (System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; FetchAllLongLivedOperationIDsAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FetchLongLivedOperation (string[] operationID, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; FetchLongLivedOperationAsync (string[] operationID);</span>
</pre>

</div> <!-- end type CKContainer -->
<!-- start type CKDiscoveredUserInfo --> <div>
<h3>Type Changed: CloudKit.CKDiscoveredUserInfo</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Contacts.CNContact DisplayContact { get; }</span>
</pre>

</div> <!-- end type CKDiscoveredUserInfo -->
<!-- start type CKErrorFields --> <div>
<h3>Type Changed: CloudKit.CKErrorFields</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ErrorDomain { get; }</span>
</pre>

</div> <!-- end type CKErrorFields -->
<!-- start type CKNotification --> <div>
<h3>Type Changed: CloudKit.CKNotification</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertActionLocalizationKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertBody { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertLaunchImage { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] AlertLocalizationArgs { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertLocalizationKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSNumber Badge { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Category { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string SoundName { get; }</span>
</pre>

</div> <!-- end type CKNotification -->
<!-- start type CKNotificationInfo --> <div>
<h3>Type Changed: CloudKit.CKNotificationInfo</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertActionLocalizationKey { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertBody { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertLaunchImage { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] AlertLocalizationArgs { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string AlertLocalizationKey { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Category { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShouldBadge { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShouldSendContentAvailable { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string SoundName { get; set; }</span>
</pre>

</div> <!-- end type CKNotificationInfo -->
<!-- start type CKRecordID --> <div>
<h3>Type Changed: CloudKit.CKRecordID</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public CKRecordID ();</span>
</pre>

</div> <!-- end type CKRecordID -->
<!-- start type CKRecordZoneID --> <div>
<h3>Type Changed: CloudKit.CKRecordZoneID</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public CKRecordZoneID ();</span>
</pre>

</div> <!-- end type CKRecordZoneID -->
<h3>Removed Type <span class='breaking' data-is-breaking="">CloudKit.CKDiscoverAllContactsOperation</span></h3>
</div> <!-- end namespace CloudKit -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBCentralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManager</h3>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CBPeripheralsEventArgs&gt; RetrievedConnectedPeripherals;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CBPeripheralsEventArgs&gt; RetrievedPeripherals;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RetrieveConnectedPeripherals ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void RetrievePeripherals (CBUUID peripheralUuid);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void RetrievePeripherals (CBUUID[] peripheralUuids);</span>
</pre>

</div> <!-- end type CBCentralManager -->
<!-- start type CBCentralManagerDelegate --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);</span>
</pre>

</div> <!-- end type CBCentralManagerDelegate -->
<!-- start type CBCentralManagerDelegate_Extensions --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManagerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RetrievedConnectedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RetrievedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);</span>
</pre>

</div> <!-- end type CBCentralManagerDelegate_Extensions -->
<!-- start type CBMutableCharacteristic --> <div>
<h3>Type Changed: CoreBluetooth.CBMutableCharacteristic</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CBMutableCharacteristic (CBUUID uuid, CBCharacteristicProperties properties, Foundation.NSData value, CBAttributePermissions permissions);</span>
</pre>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public override CBUUID UUID { get; set; }</span>
</pre>

</div> <!-- end type CBMutableCharacteristic -->
<!-- start type CBMutableDescriptor --> <div>
<h3>Type Changed: CoreBluetooth.CBMutableDescriptor</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CBMutableDescriptor (CBUUID uuid, Foundation.NSObject descriptorValue);</span>
</pre>

</div> <!-- end type CBMutableDescriptor -->
<!-- start type CBMutableService --> <div>
<h3>Type Changed: CoreBluetooth.CBMutableService</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CBMutableService (CBUUID uuid, bool primary);</span>
</pre>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public override bool Primary { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public override CBUUID UUID { get; set; }</span>
</pre>

</div> <!-- end type CBMutableService -->
<!-- start type CBPeer --> <div>
<h3>Type Changed: CoreBluetooth.CBPeer</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("This type is not meant to be created by user code.")]
	public CBPeer ();</span>
</pre>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CBUUID UUID { get; }</span>
</pre>

</div> <!-- end type CBPeer -->
<!-- start type CBPeripheral --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheral</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool IsConnected { get; }</span>
</pre>
<p>Removed event:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler InvalidatedService;</span>
</pre>

</div> <!-- end type CBPeripheral -->
<!-- start type CBPeripheralDelegate --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void InvalidatedService (CBPeripheral peripheral);</span>
</pre>

</div> <!-- end type CBPeripheralDelegate -->
<!-- start type CBPeripheralDelegate_Extensions --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralDelegate_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void InvalidatedService (ICBPeripheralDelegate This, CBPeripheral peripheral);</span>
</pre>

</div> <!-- end type CBPeripheralDelegate_Extensions -->
<!-- start type CBPeripheralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManager</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CBPeripheralManager (ICBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CBPeripheralManager (ICBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);</span>
</pre>

</div> <!-- end type CBPeripheralManager -->
<!-- start type CBUUID --> <div>
<h3>Type Changed: CoreBluetooth.CBUUID</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString AppearanceString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DeviceNameString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString GenericAccessProfileString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString GenericAttributeProfileString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PeripheralPreferredConnectionParametersString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PeripheralPrivacyFlagString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ReconnectionAddressString { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ServiceChangedString { get; }</span>
</pre>

</div> <!-- end type CBUUID -->
<h3>Removed Type <span class='breaking' data-is-breaking="">CoreBluetooth.CBPeripheralsEventArgs</span></h3>
</div> <!-- end namespace CoreBluetooth -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSManagedObject --> <div>
<h3>Type Changed: CoreData.NSManagedObject</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual IntPtr ObservationInfo { get; set; }</span>
</pre>

</div> <!-- end type NSManagedObject -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<p>Removed interface:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">Foundation.INSLocking</span>
</pre>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool TryLock { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Lock ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Unlock ();</span>
</pre>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSMergeConflict --> <div>
<h3>Type Changed: CoreData.NSMergeConflict</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("Default constructor is not available")]
	public NSMergeConflict ();</span>
</pre>

</div> <!-- end type NSMergeConflict -->
<!-- start type NSMergePolicy --> <div>
<h3>Type Changed: CoreData.NSMergePolicy</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("Default constructor is not available")]
	public NSMergePolicy ();</span>
</pre>

</div> <!-- end type NSMergePolicy -->
<!-- start type NSPersistentStore --> <div>
<h3>Type Changed: CoreData.NSPersistentStore</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("Default constructor is not available")]
	public NSPersistentStore ();</span>
</pre>

</div> <!-- end type NSPersistentStore -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<p>Removed interface:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">Foundation.INSLocking</span>
</pre>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidImportUbiquitousContentChangesNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PersistentStoreUbiquitousContentNameKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PersistentStoreUbiquitousContentUrlLKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PersistentStoreUbiquitousPeerTokenOption { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString RebuildFromUbiquitousContentOption { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString RemoveUbiquitousMetadataOption { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool TryLock { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString eUbiquitousContainerIdentifierKey { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Lock ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool RemoveUbiquitousContentAndPersistentStore (Foundation.NSUrl storeUrl, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Unlock ();</span>
</pre>
<!-- start type NSPersistentStoreCoordinator.Notifications --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator.Notifications</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveDidImportUbiquitousContentChanges (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>

</div> <!-- end type NSPersistentStoreCoordinator.Notifications -->

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSPersistentStoreCoordinatorStoreChangeEventArgs --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinatorStoreChangeEventArgs</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public NSPersistentStoreUbiquitousTransitionType EventType { get; }</span>
</pre>

</div> <!-- end type NSPersistentStoreCoordinatorStoreChangeEventArgs -->
<h3>Removed Type <span class='breaking' data-is-breaking="">CoreData.NSPersistentStoreUbiquitousTransitionType</span></h3>
</div> <!-- end namespace CoreData -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGColor --> <div>
<h3>Type Changed: CoreGraphics.CGColor</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CGColor (string name);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CGColor (nfloat gray, nfloat alpha);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CGColor (nfloat red, nfloat green, nfloat blue);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CGColor (nfloat red, nfloat green, nfloat blue, nfloat alpha);</span>
</pre>

</div> <!-- end type CGColor -->
<!-- start type CGColorSpace --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpace</h3>
<p>Removed field:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">[Obsolete ("Use a real `null` value instead of this managed wrapper over a null native instance")]
	public static CGColorSpace Null;</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("This method has been renamed CreateDeviceCmyk()")]
	public static CGColorSpace CreateDeviceCMYK ();</span>
</pre>

</div> <!-- end type CGColorSpace -->
<!-- start type CGSize --> <div>
<h3>Type Changed: CoreGraphics.CGSize</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use ToCGPoint instead")]
	public CGPoint ToPointF ();</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use ToRoundedCGSize instead")]
	public CGSize ToSize ();</span>
</pre>

</div> <!-- end type CGSize -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIAccordionFoldTransition --> <div>
<h3>Type Changed: CoreImage.CIAccordionFoldTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAccordionFoldTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIAccordionFoldTransition -->
<!-- start type CIAdditionCompositing --> <div>
<h3>Type Changed: CoreImage.CIAdditionCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAdditionCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CIAdditionCompositing -->
<!-- start type CIAffineClamp --> <div>
<h3>Type Changed: CoreImage.CIAffineClamp</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAffineClamp (IntPtr handle)
</div></pre>

</div> <!-- end type CIAffineClamp -->
<!-- start type CIAffineTile --> <div>
<h3>Type Changed: CoreImage.CIAffineTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAffineTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIAffineTile -->
<!-- start type CIAffineTransform --> <div>
<h3>Type Changed: CoreImage.CIAffineTransform</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAffineTransform (IntPtr handle)
</div></pre>

</div> <!-- end type CIAffineTransform -->
<!-- start type CIAreaAverage --> <div>
<h3>Type Changed: CoreImage.CIAreaAverage</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaAverage (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaAverage -->
<!-- start type CIAreaHistogram --> <div>
<h3>Type Changed: CoreImage.CIAreaHistogram</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaHistogram (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaHistogram -->
<!-- start type CIAreaMaximum --> <div>
<h3>Type Changed: CoreImage.CIAreaMaximum</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaMaximum (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaMaximum -->
<!-- start type CIAreaMaximumAlpha --> <div>
<h3>Type Changed: CoreImage.CIAreaMaximumAlpha</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaMaximumAlpha (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaMaximumAlpha -->
<!-- start type CIAreaMinimum --> <div>
<h3>Type Changed: CoreImage.CIAreaMinimum</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaMinimum (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaMinimum -->
<!-- start type CIAreaMinimumAlpha --> <div>
<h3>Type Changed: CoreImage.CIAreaMinimumAlpha</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAreaMinimumAlpha (IntPtr handle)
</div></pre>

</div> <!-- end type CIAreaMinimumAlpha -->
<!-- start type CIAztecCodeGenerator --> <div>
<h3>Type Changed: CoreImage.CIAztecCodeGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIAztecCodeGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIAztecCodeGenerator -->
<!-- start type CIBarsSwipeTransition --> <div>
<h3>Type Changed: CoreImage.CIBarsSwipeTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBarsSwipeTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIBarsSwipeTransition -->
<!-- start type CIBlendWithAlphaMask --> <div>
<h3>Type Changed: CoreImage.CIBlendWithAlphaMask</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBlendWithAlphaMask (IntPtr handle)
</div></pre>

</div> <!-- end type CIBlendWithAlphaMask -->
<!-- start type CIBlendWithMask --> <div>
<h3>Type Changed: CoreImage.CIBlendWithMask</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBlendWithMask (IntPtr handle)
</div></pre>

</div> <!-- end type CIBlendWithMask -->
<!-- start type CIBloom --> <div>
<h3>Type Changed: CoreImage.CIBloom</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBloom (IntPtr handle)
</div></pre>

</div> <!-- end type CIBloom -->
<!-- start type CIBoxBlur --> <div>
<h3>Type Changed: CoreImage.CIBoxBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBoxBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIBoxBlur -->
<!-- start type CIBumpDistortion --> <div>
<h3>Type Changed: CoreImage.CIBumpDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBumpDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIBumpDistortion -->
<!-- start type CIBumpDistortionLinear --> <div>
<h3>Type Changed: CoreImage.CIBumpDistortionLinear</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIBumpDistortionLinear (IntPtr handle)
</div></pre>

</div> <!-- end type CIBumpDistortionLinear -->
<!-- start type CICheckerboardGenerator --> <div>
<h3>Type Changed: CoreImage.CICheckerboardGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICheckerboardGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CICheckerboardGenerator -->
<!-- start type CICircleSplashDistortion --> <div>
<h3>Type Changed: CoreImage.CICircleSplashDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICircleSplashDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CICircleSplashDistortion -->
<!-- start type CICircularScreen --> <div>
<h3>Type Changed: CoreImage.CICircularScreen</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICircularScreen (IntPtr handle)
</div></pre>

</div> <!-- end type CICircularScreen -->
<!-- start type CICircularWrap --> <div>
<h3>Type Changed: CoreImage.CICircularWrap</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICircularWrap (IntPtr handle)
</div></pre>

</div> <!-- end type CICircularWrap -->
<!-- start type CICmykHalftone --> <div>
<h3>Type Changed: CoreImage.CICmykHalftone</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICmykHalftone (IntPtr handle)
</div></pre>

</div> <!-- end type CICmykHalftone -->
<!-- start type CICode128BarcodeGenerator --> <div>
<h3>Type Changed: CoreImage.CICode128BarcodeGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICode128BarcodeGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CICode128BarcodeGenerator -->
<!-- start type CICodeGenerator --> <div>
<h3>Type Changed: CoreImage.CICodeGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICodeGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CICodeGenerator -->
<!-- start type CIColorBlendMode --> <div>
<h3>Type Changed: CoreImage.CIColorBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorBlendMode -->
<!-- start type CIColorBurnBlendMode --> <div>
<h3>Type Changed: CoreImage.CIColorBurnBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorBurnBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorBurnBlendMode -->
<!-- start type CIColorClamp --> <div>
<h3>Type Changed: CoreImage.CIColorClamp</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorClamp (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorClamp -->
<!-- start type CIColorControls --> <div>
<h3>Type Changed: CoreImage.CIColorControls</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorControls (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorControls -->
<!-- start type CIColorCrossPolynomial --> <div>
<h3>Type Changed: CoreImage.CIColorCrossPolynomial</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorCrossPolynomial (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorCrossPolynomial -->
<!-- start type CIColorCube --> <div>
<h3>Type Changed: CoreImage.CIColorCube</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorCube (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorCube -->
<!-- start type CIColorCubeWithColorSpace --> <div>
<h3>Type Changed: CoreImage.CIColorCubeWithColorSpace</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorCubeWithColorSpace (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorCubeWithColorSpace -->
<!-- start type CIColorDodgeBlendMode --> <div>
<h3>Type Changed: CoreImage.CIColorDodgeBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorDodgeBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorDodgeBlendMode -->
<!-- start type CIColorInvert --> <div>
<h3>Type Changed: CoreImage.CIColorInvert</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorInvert (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorInvert -->
<!-- start type CIColorMap --> <div>
<h3>Type Changed: CoreImage.CIColorMap</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorMap (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorMap -->
<!-- start type CIColorMatrix --> <div>
<h3>Type Changed: CoreImage.CIColorMatrix</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorMatrix (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorMatrix -->
<!-- start type CIColorMonochrome --> <div>
<h3>Type Changed: CoreImage.CIColorMonochrome</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorMonochrome (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorMonochrome -->
<!-- start type CIColorPolynomial --> <div>
<h3>Type Changed: CoreImage.CIColorPolynomial</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorPolynomial (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorPolynomial -->
<!-- start type CIColorPosterize --> <div>
<h3>Type Changed: CoreImage.CIColorPosterize</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColorPosterize (IntPtr handle)
</div></pre>

</div> <!-- end type CIColorPosterize -->
<!-- start type CIColumnAverage --> <div>
<h3>Type Changed: CoreImage.CIColumnAverage</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIColumnAverage (IntPtr handle)
</div></pre>

</div> <!-- end type CIColumnAverage -->
<!-- start type CIComicEffect --> <div>
<h3>Type Changed: CoreImage.CIComicEffect</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIComicEffect (IntPtr handle)
</div></pre>

</div> <!-- end type CIComicEffect -->
<!-- start type CIConstantColorGenerator --> <div>
<h3>Type Changed: CoreImage.CIConstantColorGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConstantColorGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIConstantColorGenerator -->
<!-- start type CIConvolution3X3 --> <div>
<h3>Type Changed: CoreImage.CIConvolution3X3</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolution3X3 (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolution3X3 -->
<!-- start type CIConvolution5X5 --> <div>
<h3>Type Changed: CoreImage.CIConvolution5X5</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolution5X5 (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolution5X5 -->
<!-- start type CIConvolution7X7 --> <div>
<h3>Type Changed: CoreImage.CIConvolution7X7</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolution7X7 (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolution7X7 -->
<!-- start type CIConvolution9Horizontal --> <div>
<h3>Type Changed: CoreImage.CIConvolution9Horizontal</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolution9Horizontal (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolution9Horizontal -->
<!-- start type CIConvolution9Vertical --> <div>
<h3>Type Changed: CoreImage.CIConvolution9Vertical</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolution9Vertical (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolution9Vertical -->
<!-- start type CIConvolutionCore --> <div>
<h3>Type Changed: CoreImage.CIConvolutionCore</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIConvolutionCore (IntPtr handle)
</div></pre>

</div> <!-- end type CIConvolutionCore -->
<!-- start type CICopyMachineTransition --> <div>
<h3>Type Changed: CoreImage.CICopyMachineTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICopyMachineTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CICopyMachineTransition -->
<!-- start type CICrop --> <div>
<h3>Type Changed: CoreImage.CICrop</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICrop (IntPtr handle)
</div></pre>

</div> <!-- end type CICrop -->
<!-- start type CICrystallize --> <div>
<h3>Type Changed: CoreImage.CICrystallize</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CICrystallize (IntPtr handle)
</div></pre>

</div> <!-- end type CICrystallize -->
<!-- start type CIDarkenBlendMode --> <div>
<h3>Type Changed: CoreImage.CIDarkenBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDarkenBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIDarkenBlendMode -->
<!-- start type CIDepthOfField --> <div>
<h3>Type Changed: CoreImage.CIDepthOfField</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDepthOfField (IntPtr handle)
</div></pre>

</div> <!-- end type CIDepthOfField -->
<!-- start type CIDifferenceBlendMode --> <div>
<h3>Type Changed: CoreImage.CIDifferenceBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDifferenceBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIDifferenceBlendMode -->
<!-- start type CIDiscBlur --> <div>
<h3>Type Changed: CoreImage.CIDiscBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDiscBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIDiscBlur -->
<!-- start type CIDisintegrateWithMaskTransition --> <div>
<h3>Type Changed: CoreImage.CIDisintegrateWithMaskTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDisintegrateWithMaskTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIDisintegrateWithMaskTransition -->
<!-- start type CIDisplacementDistortion --> <div>
<h3>Type Changed: CoreImage.CIDisplacementDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDisplacementDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIDisplacementDistortion -->
<!-- start type CIDissolveTransition --> <div>
<h3>Type Changed: CoreImage.CIDissolveTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDissolveTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIDissolveTransition -->
<!-- start type CIDivideBlendMode --> <div>
<h3>Type Changed: CoreImage.CIDivideBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDivideBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIDivideBlendMode -->
<!-- start type CIDotScreen --> <div>
<h3>Type Changed: CoreImage.CIDotScreen</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDotScreen (IntPtr handle)
</div></pre>

</div> <!-- end type CIDotScreen -->
<!-- start type CIDroste --> <div>
<h3>Type Changed: CoreImage.CIDroste</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIDroste (IntPtr handle)
</div></pre>

</div> <!-- end type CIDroste -->
<!-- start type CIEdgeWork --> <div>
<h3>Type Changed: CoreImage.CIEdgeWork</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIEdgeWork (IntPtr handle)
</div></pre>

</div> <!-- end type CIEdgeWork -->
<!-- start type CIEdges --> <div>
<h3>Type Changed: CoreImage.CIEdges</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIEdges (IntPtr handle)
</div></pre>

</div> <!-- end type CIEdges -->
<!-- start type CIEightfoldReflectedTile --> <div>
<h3>Type Changed: CoreImage.CIEightfoldReflectedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIEightfoldReflectedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIEightfoldReflectedTile -->
<!-- start type CIExclusionBlendMode --> <div>
<h3>Type Changed: CoreImage.CIExclusionBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIExclusionBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIExclusionBlendMode -->
<!-- start type CIExposureAdjust --> <div>
<h3>Type Changed: CoreImage.CIExposureAdjust</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIExposureAdjust (IntPtr handle)
</div></pre>

</div> <!-- end type CIExposureAdjust -->
<!-- start type CIFaceBalance --> <div>
<h3>Type Changed: CoreImage.CIFaceBalance</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFaceBalance (IntPtr handle)
</div></pre>

</div> <!-- end type CIFaceBalance -->
<!-- start type CIFalseColor --> <div>
<h3>Type Changed: CoreImage.CIFalseColor</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFalseColor (IntPtr handle)
</div></pre>

</div> <!-- end type CIFalseColor -->
<!-- start type CIFlashTransition --> <div>
<h3>Type Changed: CoreImage.CIFlashTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFlashTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIFlashTransition -->
<!-- start type CIFormat --> <div>
<h3>Type Changed: CoreImage.CIFormat</h3>
<p>Removed values:</p>
<pre class='removed' data-is-breaking="">
	<span class='removed removed-field breaking' data-is-breaking="">[Obsolete ("This value can not be shared across Mac/iOS binaries, future proof with kBGRA8 instead")]
	BGRA8 = 2,</span>

	<span class='removed removed-field breaking' data-is-breaking="">[Obsolete ("This value can not be shared across Mac/iOS binaries, future proof with kRGBA8 instead")]
	RGBA8 = 3,</span>
</pre>

</div> <!-- end type CIFormat -->
<!-- start type CIFourfoldReflectedTile --> <div>
<h3>Type Changed: CoreImage.CIFourfoldReflectedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFourfoldReflectedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIFourfoldReflectedTile -->
<!-- start type CIFourfoldRotatedTile --> <div>
<h3>Type Changed: CoreImage.CIFourfoldRotatedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFourfoldRotatedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIFourfoldRotatedTile -->
<!-- start type CIFourfoldTranslatedTile --> <div>
<h3>Type Changed: CoreImage.CIFourfoldTranslatedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIFourfoldTranslatedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIFourfoldTranslatedTile -->
<!-- start type CIGammaAdjust --> <div>
<h3>Type Changed: CoreImage.CIGammaAdjust</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGammaAdjust (IntPtr handle)
</div></pre>

</div> <!-- end type CIGammaAdjust -->
<!-- start type CIGaussianBlur --> <div>
<h3>Type Changed: CoreImage.CIGaussianBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGaussianBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIGaussianBlur -->
<!-- start type CIGaussianGradient --> <div>
<h3>Type Changed: CoreImage.CIGaussianGradient</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGaussianGradient (IntPtr handle)
</div></pre>

</div> <!-- end type CIGaussianGradient -->
<!-- start type CIGlassDistortion --> <div>
<h3>Type Changed: CoreImage.CIGlassDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGlassDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIGlassDistortion -->
<!-- start type CIGlassLozenge --> <div>
<h3>Type Changed: CoreImage.CIGlassLozenge</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGlassLozenge (IntPtr handle)
</div></pre>

</div> <!-- end type CIGlassLozenge -->
<!-- start type CIGlideReflectedTile --> <div>
<h3>Type Changed: CoreImage.CIGlideReflectedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGlideReflectedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIGlideReflectedTile -->
<!-- start type CIGloom --> <div>
<h3>Type Changed: CoreImage.CIGloom</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIGloom (IntPtr handle)
</div></pre>

</div> <!-- end type CIGloom -->
<!-- start type CIHardLightBlendMode --> <div>
<h3>Type Changed: CoreImage.CIHardLightBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHardLightBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIHardLightBlendMode -->
<!-- start type CIHatchedScreen --> <div>
<h3>Type Changed: CoreImage.CIHatchedScreen</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHatchedScreen (IntPtr handle)
</div></pre>

</div> <!-- end type CIHatchedScreen -->
<!-- start type CIHeightFieldFromMask --> <div>
<h3>Type Changed: CoreImage.CIHeightFieldFromMask</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHeightFieldFromMask (IntPtr handle)
</div></pre>

</div> <!-- end type CIHeightFieldFromMask -->
<!-- start type CIHexagonalPixellate --> <div>
<h3>Type Changed: CoreImage.CIHexagonalPixellate</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHexagonalPixellate (IntPtr handle)
</div></pre>

</div> <!-- end type CIHexagonalPixellate -->
<!-- start type CIHighlightShadowAdjust --> <div>
<h3>Type Changed: CoreImage.CIHighlightShadowAdjust</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHighlightShadowAdjust (IntPtr handle)
</div></pre>

</div> <!-- end type CIHighlightShadowAdjust -->
<!-- start type CIHistogramDisplayFilter --> <div>
<h3>Type Changed: CoreImage.CIHistogramDisplayFilter</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHistogramDisplayFilter (IntPtr handle)
</div></pre>

</div> <!-- end type CIHistogramDisplayFilter -->
<!-- start type CIHoleDistortion --> <div>
<h3>Type Changed: CoreImage.CIHoleDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHoleDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIHoleDistortion -->
<!-- start type CIHueAdjust --> <div>
<h3>Type Changed: CoreImage.CIHueAdjust</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHueAdjust (IntPtr handle)
</div></pre>

</div> <!-- end type CIHueAdjust -->
<!-- start type CIHueBlendMode --> <div>
<h3>Type Changed: CoreImage.CIHueBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIHueBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIHueBlendMode -->
<!-- start type CIKaleidoscope --> <div>
<h3>Type Changed: CoreImage.CIKaleidoscope</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIKaleidoscope (IntPtr handle)
</div></pre>

</div> <!-- end type CIKaleidoscope -->
<!-- start type CILanczosScaleTransform --> <div>
<h3>Type Changed: CoreImage.CILanczosScaleTransform</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILanczosScaleTransform (IntPtr handle)
</div></pre>

</div> <!-- end type CILanczosScaleTransform -->
<!-- start type CILenticularHaloGenerator --> <div>
<h3>Type Changed: CoreImage.CILenticularHaloGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILenticularHaloGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CILenticularHaloGenerator -->
<!-- start type CILightTunnel --> <div>
<h3>Type Changed: CoreImage.CILightTunnel</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILightTunnel (IntPtr handle)
</div></pre>

</div> <!-- end type CILightTunnel -->
<!-- start type CILightenBlendMode --> <div>
<h3>Type Changed: CoreImage.CILightenBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILightenBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CILightenBlendMode -->
<!-- start type CILineOverlay --> <div>
<h3>Type Changed: CoreImage.CILineOverlay</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILineOverlay (IntPtr handle)
</div></pre>

</div> <!-- end type CILineOverlay -->
<!-- start type CILineScreen --> <div>
<h3>Type Changed: CoreImage.CILineScreen</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILineScreen (IntPtr handle)
</div></pre>

</div> <!-- end type CILineScreen -->
<!-- start type CILinearBurnBlendMode --> <div>
<h3>Type Changed: CoreImage.CILinearBurnBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILinearBurnBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CILinearBurnBlendMode -->
<!-- start type CILinearDodgeBlendMode --> <div>
<h3>Type Changed: CoreImage.CILinearDodgeBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILinearDodgeBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CILinearDodgeBlendMode -->
<!-- start type CILinearGradient --> <div>
<h3>Type Changed: CoreImage.CILinearGradient</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILinearGradient (IntPtr handle)
</div></pre>

</div> <!-- end type CILinearGradient -->
<!-- start type CILinearToSRGBToneCurve --> <div>
<h3>Type Changed: CoreImage.CILinearToSRGBToneCurve</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILinearToSRGBToneCurve (IntPtr handle)
</div></pre>

</div> <!-- end type CILinearToSRGBToneCurve -->
<!-- start type CILuminosityBlendMode --> <div>
<h3>Type Changed: CoreImage.CILuminosityBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CILuminosityBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CILuminosityBlendMode -->
<!-- start type CIMaskToAlpha --> <div>
<h3>Type Changed: CoreImage.CIMaskToAlpha</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMaskToAlpha (IntPtr handle)
</div></pre>

</div> <!-- end type CIMaskToAlpha -->
<!-- start type CIMaskedVariableBlur --> <div>
<h3>Type Changed: CoreImage.CIMaskedVariableBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMaskedVariableBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIMaskedVariableBlur -->
<!-- start type CIMaximumComponent --> <div>
<h3>Type Changed: CoreImage.CIMaximumComponent</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMaximumComponent (IntPtr handle)
</div></pre>

</div> <!-- end type CIMaximumComponent -->
<!-- start type CIMaximumCompositing --> <div>
<h3>Type Changed: CoreImage.CIMaximumCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMaximumCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CIMaximumCompositing -->
<!-- start type CIMedianFilter --> <div>
<h3>Type Changed: CoreImage.CIMedianFilter</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMedianFilter (IntPtr handle)
</div></pre>

</div> <!-- end type CIMedianFilter -->
<!-- start type CIMinimumComponent --> <div>
<h3>Type Changed: CoreImage.CIMinimumComponent</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMinimumComponent (IntPtr handle)
</div></pre>

</div> <!-- end type CIMinimumComponent -->
<!-- start type CIMinimumCompositing --> <div>
<h3>Type Changed: CoreImage.CIMinimumCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMinimumCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CIMinimumCompositing -->
<!-- start type CIModTransition --> <div>
<h3>Type Changed: CoreImage.CIModTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIModTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIModTransition -->
<!-- start type CIMotionBlur --> <div>
<h3>Type Changed: CoreImage.CIMotionBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMotionBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIMotionBlur -->
<!-- start type CIMultiplyBlendMode --> <div>
<h3>Type Changed: CoreImage.CIMultiplyBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMultiplyBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIMultiplyBlendMode -->
<!-- start type CIMultiplyCompositing --> <div>
<h3>Type Changed: CoreImage.CIMultiplyCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIMultiplyCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CIMultiplyCompositing -->
<!-- start type CINoiseReduction --> <div>
<h3>Type Changed: CoreImage.CINoiseReduction</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CINoiseReduction (IntPtr handle)
</div></pre>

</div> <!-- end type CINoiseReduction -->
<!-- start type CIOpTile --> <div>
<h3>Type Changed: CoreImage.CIOpTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIOpTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIOpTile -->
<!-- start type CIOverlayBlendMode --> <div>
<h3>Type Changed: CoreImage.CIOverlayBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIOverlayBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIOverlayBlendMode -->
<!-- start type CIPageCurlTransition --> <div>
<h3>Type Changed: CoreImage.CIPageCurlTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPageCurlTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIPageCurlTransition -->
<!-- start type CIPageCurlWithShadowTransition --> <div>
<h3>Type Changed: CoreImage.CIPageCurlWithShadowTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPageCurlWithShadowTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIPageCurlWithShadowTransition -->
<!-- start type CIParallelogramTile --> <div>
<h3>Type Changed: CoreImage.CIParallelogramTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIParallelogramTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIParallelogramTile -->
<!-- start type CIPdf417BarcodeGenerator --> <div>
<h3>Type Changed: CoreImage.CIPdf417BarcodeGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPdf417BarcodeGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIPdf417BarcodeGenerator -->
<!-- start type CIPerspectiveCorrection --> <div>
<h3>Type Changed: CoreImage.CIPerspectiveCorrection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPerspectiveCorrection (IntPtr handle)
</div></pre>

</div> <!-- end type CIPerspectiveCorrection -->
<!-- start type CIPerspectiveTile --> <div>
<h3>Type Changed: CoreImage.CIPerspectiveTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPerspectiveTile (IntPtr handle)
</div></pre>

</div> <!-- end type CIPerspectiveTile -->
<!-- start type CIPerspectiveTransform --> <div>
<h3>Type Changed: CoreImage.CIPerspectiveTransform</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPerspectiveTransform (IntPtr handle)
</div></pre>

</div> <!-- end type CIPerspectiveTransform -->
<!-- start type CIPerspectiveTransformWithExtent --> <div>
<h3>Type Changed: CoreImage.CIPerspectiveTransformWithExtent</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPerspectiveTransformWithExtent (IntPtr handle)
</div></pre>

</div> <!-- end type CIPerspectiveTransformWithExtent -->
<!-- start type CIPhotoEffect --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffect</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffect (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffect -->
<!-- start type CIPhotoEffectChrome --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectChrome</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectChrome (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectChrome -->
<!-- start type CIPhotoEffectFade --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectFade</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectFade (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectFade -->
<!-- start type CIPhotoEffectInstant --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectInstant</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectInstant (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectInstant -->
<!-- start type CIPhotoEffectMono --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectMono</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectMono (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectMono -->
<!-- start type CIPhotoEffectNoir --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectNoir</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectNoir (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectNoir -->
<!-- start type CIPhotoEffectProcess --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectProcess</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectProcess (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectProcess -->
<!-- start type CIPhotoEffectTonal --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectTonal</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectTonal (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectTonal -->
<!-- start type CIPhotoEffectTransfer --> <div>
<h3>Type Changed: CoreImage.CIPhotoEffectTransfer</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPhotoEffectTransfer (IntPtr handle)
</div></pre>

</div> <!-- end type CIPhotoEffectTransfer -->
<!-- start type CIPinLightBlendMode --> <div>
<h3>Type Changed: CoreImage.CIPinLightBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPinLightBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIPinLightBlendMode -->
<!-- start type CIPinchDistortion --> <div>
<h3>Type Changed: CoreImage.CIPinchDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPinchDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIPinchDistortion -->
<!-- start type CIPixellate --> <div>
<h3>Type Changed: CoreImage.CIPixellate</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPixellate (IntPtr handle)
</div></pre>

</div> <!-- end type CIPixellate -->
<!-- start type CIPointillize --> <div>
<h3>Type Changed: CoreImage.CIPointillize</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIPointillize (IntPtr handle)
</div></pre>

</div> <!-- end type CIPointillize -->
<!-- start type CIQRCodeGenerator --> <div>
<h3>Type Changed: CoreImage.CIQRCodeGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIQRCodeGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIQRCodeGenerator -->
<!-- start type CIRadialGradient --> <div>
<h3>Type Changed: CoreImage.CIRadialGradient</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIRadialGradient (IntPtr handle)
</div></pre>

</div> <!-- end type CIRadialGradient -->
<!-- start type CIRandomGenerator --> <div>
<h3>Type Changed: CoreImage.CIRandomGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIRandomGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIRandomGenerator -->
<!-- start type CIRippleTransition --> <div>
<h3>Type Changed: CoreImage.CIRippleTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIRippleTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CIRippleTransition -->
<!-- start type CIRowAverage --> <div>
<h3>Type Changed: CoreImage.CIRowAverage</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIRowAverage (IntPtr handle)
</div></pre>

</div> <!-- end type CIRowAverage -->
<!-- start type CISRGBToneCurveToLinear --> <div>
<h3>Type Changed: CoreImage.CISRGBToneCurveToLinear</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISRGBToneCurveToLinear (IntPtr handle)
</div></pre>

</div> <!-- end type CISRGBToneCurveToLinear -->
<!-- start type CISaturationBlendMode --> <div>
<h3>Type Changed: CoreImage.CISaturationBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISaturationBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CISaturationBlendMode -->
<!-- start type CIScreenBlendMode --> <div>
<h3>Type Changed: CoreImage.CIScreenBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIScreenBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CIScreenBlendMode -->
<!-- start type CISepiaTone --> <div>
<h3>Type Changed: CoreImage.CISepiaTone</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISepiaTone (IntPtr handle)
</div></pre>

</div> <!-- end type CISepiaTone -->
<!-- start type CIShadedMaterial --> <div>
<h3>Type Changed: CoreImage.CIShadedMaterial</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIShadedMaterial (IntPtr handle)
</div></pre>

</div> <!-- end type CIShadedMaterial -->
<!-- start type CISharpenLuminance --> <div>
<h3>Type Changed: CoreImage.CISharpenLuminance</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISharpenLuminance (IntPtr handle)
</div></pre>

</div> <!-- end type CISharpenLuminance -->
<!-- start type CISixfoldReflectedTile --> <div>
<h3>Type Changed: CoreImage.CISixfoldReflectedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISixfoldReflectedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CISixfoldReflectedTile -->
<!-- start type CISixfoldRotatedTile --> <div>
<h3>Type Changed: CoreImage.CISixfoldRotatedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISixfoldRotatedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CISixfoldRotatedTile -->
<!-- start type CISmoothLinearGradient --> <div>
<h3>Type Changed: CoreImage.CISmoothLinearGradient</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISmoothLinearGradient (IntPtr handle)
</div></pre>

</div> <!-- end type CISmoothLinearGradient -->
<!-- start type CISoftLightBlendMode --> <div>
<h3>Type Changed: CoreImage.CISoftLightBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISoftLightBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CISoftLightBlendMode -->
<!-- start type CISourceAtopCompositing --> <div>
<h3>Type Changed: CoreImage.CISourceAtopCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISourceAtopCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CISourceAtopCompositing -->
<!-- start type CISourceInCompositing --> <div>
<h3>Type Changed: CoreImage.CISourceInCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISourceInCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CISourceInCompositing -->
<!-- start type CISourceOutCompositing --> <div>
<h3>Type Changed: CoreImage.CISourceOutCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISourceOutCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CISourceOutCompositing -->
<!-- start type CISourceOverCompositing --> <div>
<h3>Type Changed: CoreImage.CISourceOverCompositing</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISourceOverCompositing (IntPtr handle)
</div></pre>

</div> <!-- end type CISourceOverCompositing -->
<!-- start type CISpotColor --> <div>
<h3>Type Changed: CoreImage.CISpotColor</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISpotColor (IntPtr handle)
</div></pre>

</div> <!-- end type CISpotColor -->
<!-- start type CISpotLight --> <div>
<h3>Type Changed: CoreImage.CISpotLight</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISpotLight (IntPtr handle)
</div></pre>

</div> <!-- end type CISpotLight -->
<!-- start type CIStarShineGenerator --> <div>
<h3>Type Changed: CoreImage.CIStarShineGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIStarShineGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIStarShineGenerator -->
<!-- start type CIStraightenFilter --> <div>
<h3>Type Changed: CoreImage.CIStraightenFilter</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIStraightenFilter (IntPtr handle)
</div></pre>

</div> <!-- end type CIStraightenFilter -->
<!-- start type CIStretchCrop --> <div>
<h3>Type Changed: CoreImage.CIStretchCrop</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIStretchCrop (IntPtr handle)
</div></pre>

</div> <!-- end type CIStretchCrop -->
<!-- start type CIStripesGenerator --> <div>
<h3>Type Changed: CoreImage.CIStripesGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIStripesGenerator (IntPtr handle)
</div></pre>

</div> <!-- end type CIStripesGenerator -->
<!-- start type CISubtractBlendMode --> <div>
<h3>Type Changed: CoreImage.CISubtractBlendMode</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISubtractBlendMode (IntPtr handle)
</div></pre>

</div> <!-- end type CISubtractBlendMode -->
<!-- start type CISunbeamsGenerator --> <div>
<h3>Type Changed: CoreImage.CISunbeamsGenerator</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISunbeamsGenerator (IntPtr handle)
</div></pre>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public float CropAmount { get; set; }</span>
</pre>

</div> <!-- end type CISunbeamsGenerator -->
<!-- start type CISwipeTransition --> <div>
<h3>Type Changed: CoreImage.CISwipeTransition</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CISwipeTransition (IntPtr handle)
</div></pre>

</div> <!-- end type CISwipeTransition -->
<!-- start type CITemperatureAndTint --> <div>
<h3>Type Changed: CoreImage.CITemperatureAndTint</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITemperatureAndTint (IntPtr handle)
</div></pre>

</div> <!-- end type CITemperatureAndTint -->
<!-- start type CIToneCurve --> <div>
<h3>Type Changed: CoreImage.CIToneCurve</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIToneCurve (IntPtr handle)
</div></pre>

</div> <!-- end type CIToneCurve -->
<!-- start type CITorusLensDistortion --> <div>
<h3>Type Changed: CoreImage.CITorusLensDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITorusLensDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CITorusLensDistortion -->
<!-- start type CITriangleKaleidoscope --> <div>
<h3>Type Changed: CoreImage.CITriangleKaleidoscope</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITriangleKaleidoscope (IntPtr handle)
</div></pre>

</div> <!-- end type CITriangleKaleidoscope -->
<!-- start type CITriangleTile --> <div>
<h3>Type Changed: CoreImage.CITriangleTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITriangleTile (IntPtr handle)
</div></pre>

</div> <!-- end type CITriangleTile -->
<!-- start type CITwelvefoldReflectedTile --> <div>
<h3>Type Changed: CoreImage.CITwelvefoldReflectedTile</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITwelvefoldReflectedTile (IntPtr handle)
</div></pre>

</div> <!-- end type CITwelvefoldReflectedTile -->
<!-- start type CITwirlDistortion --> <div>
<h3>Type Changed: CoreImage.CITwirlDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CITwirlDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CITwirlDistortion -->
<!-- start type CIUnsharpMask --> <div>
<h3>Type Changed: CoreImage.CIUnsharpMask</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIUnsharpMask (IntPtr handle)
</div></pre>

</div> <!-- end type CIUnsharpMask -->
<!-- start type CIVibrance --> <div>
<h3>Type Changed: CoreImage.CIVibrance</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIVibrance (IntPtr handle)
</div></pre>

</div> <!-- end type CIVibrance -->
<!-- start type CIVignette --> <div>
<h3>Type Changed: CoreImage.CIVignette</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIVignette (IntPtr handle)
</div></pre>

</div> <!-- end type CIVignette -->
<!-- start type CIVignetteEffect --> <div>
<h3>Type Changed: CoreImage.CIVignetteEffect</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIVignetteEffect (IntPtr handle)
</div></pre>

</div> <!-- end type CIVignetteEffect -->
<!-- start type CIVortexDistortion --> <div>
<h3>Type Changed: CoreImage.CIVortexDistortion</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIVortexDistortion (IntPtr handle)
</div></pre>

</div> <!-- end type CIVortexDistortion -->
<!-- start type CIWhitePointAdjust --> <div>
<h3>Type Changed: CoreImage.CIWhitePointAdjust</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIWhitePointAdjust (IntPtr handle)
</div></pre>

</div> <!-- end type CIWhitePointAdjust -->
<!-- start type CIZoomBlur --> <div>
<h3>Type Changed: CoreImage.CIZoomBlur</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	<span class='removed removed-inline removed-breaking-inline'>public</span> <span class='added '>protected</span> CIZoomBlur (IntPtr handle)
</div></pre>

</div> <!-- end type CIZoomBlur -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLLocation --> <div>
<h3>Type Changed: CoreLocation.CLLocation</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double Course { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ErrorUserInfoAlternateRegionKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double Speed { get; }</span>
</pre>

</div> <!-- end type CLLocation -->
<!-- start type CLLocationManager --> <div>
<h3>Type Changed: CoreLocation.CLLocationManager</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CLActivityType ActivityType { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool AllowsBackgroundLocationUpdates { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool DeferredLocationUpdatesAvailable { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CLHeading Heading { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool HeadingAvailable { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double HeadingFilter { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CLDeviceOrientation HeadingOrientation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool IsRangingAvailable { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double MaximumRegionMonitoringDistance { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSSet MonitoredRegions { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool PausesLocationUpdatesAutomatically { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Purpose { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSSet RangedRegions { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool RegionMonitoringAvailable { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool RegionMonitoringEnabled { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public CLLocationManagerEventArgs ShouldDisplayHeadingCalibration { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static bool SignificantLocationChangeMonitoringAvailable { get; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;Foundation.NSErrorEventArgs&gt; DeferredUpdatesFinished;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionStateDeterminedEventArgs&gt; DidDetermineState;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionBeaconsRangedEventArgs&gt; DidRangeBeacons;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; DidStartMonitoringForRegion;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLVisitedEventArgs&gt; DidVisit;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler LocationUpdatesPaused;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler LocationUpdatesResumed;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionErrorEventArgs&gt; MonitoringFailed;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionBeaconsFailedEventArgs&gt; RangingBeaconsDidFailForRegion;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; RegionEntered;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; RegionLeft;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLHeadingUpdatedEventArgs&gt; UpdatedHeading;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;CLLocationUpdatedEventArgs&gt; UpdatedLocation;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void AllowDeferredLocationUpdatesUntil (double distance, double timeout);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DisallowDeferredLocationUpdates ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DismissHeadingCalibrationDisplay ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool IsMonitoringAvailable (ObjCRuntime.Class regionClass);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool IsMonitoringAvailable (System.Type t);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RequestAlwaysAuthorization ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RequestState (CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartMonitoring (CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartMonitoringSignificantLocationChanges ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartMonitoringVisits ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartRangingBeacons (CLBeaconRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartUpdatingHeading ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartUpdatingLocation ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StopMonitoring (CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StopMonitoringSignificantLocationChanges ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StopMonitoringVisits ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StopRangingBeacons (CLBeaconRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StopUpdatingHeading ();</span>
</pre>

</div> <!-- end type CLLocationManager -->
<!-- start type CLLocationManagerDelegate --> <div>
<h3>Type Changed: CoreLocation.CLLocationManagerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DeferredUpdatesFinished (CLLocationManager manager, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidDetermineState (CLLocationManager manager, CLRegionState state, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRangeBeacons (CLLocationManager manager, CLBeacon[] beacons, CLBeaconRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidStartMonitoringForRegion (CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidVisit (CLLocationManager manager, CLVisit visit);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LocationUpdatesPaused (CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LocationUpdatesResumed (CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void MonitoringFailed (CLLocationManager manager, CLRegion region, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RangingBeaconsDidFailForRegion (CLLocationManager manager, CLBeaconRegion region, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RegionEntered (CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RegionLeft (CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldDisplayHeadingCalibration (CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void UpdatedHeading (CLLocationManager manager, CLHeading newHeading);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void UpdatedLocation (CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);</span>
</pre>

</div> <!-- end type CLLocationManagerDelegate -->
<!-- start type CLLocationManagerDelegate_Extensions --> <div>
<h3>Type Changed: CoreLocation.CLLocationManagerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DeferredUpdatesFinished (ICLLocationManagerDelegate This, CLLocationManager manager, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidDetermineState (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegionState state, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidRangeBeacons (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeacon[] beacons, CLBeaconRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidStartMonitoringForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidVisit (ICLLocationManagerDelegate This, CLLocationManager manager, CLVisit visit);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void LocationUpdatesPaused (ICLLocationManagerDelegate This, CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void LocationUpdatesResumed (ICLLocationManagerDelegate This, CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void MonitoringFailed (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RangingBeaconsDidFailForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeaconRegion region, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RegionEntered (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void RegionLeft (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool ShouldDisplayHeadingCalibration (ICLLocationManagerDelegate This, CLLocationManager manager);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void UpdatedHeading (ICLLocationManagerDelegate This, CLLocationManager manager, CLHeading newHeading);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void UpdatedLocation (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);</span>
</pre>

</div> <!-- end type CLLocationManagerDelegate_Extensions -->
<!-- start type CLRegion --> <div>
<h3>Type Changed: CoreLocation.CLRegion</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CLRegion (CLLocationCoordinate2D center, double radius, string identifier);</span>
</pre>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CLLocationCoordinate2D Center { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double Radius { get; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool Contains (CLLocationCoordinate2D coordinate);</span>
</pre>

</div> <!-- end type CLRegion -->
<h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLBeacon</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLBeaconRegion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLHeading</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLHeadingUpdatedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLLocationManagerEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLLocationUpdatedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLProximity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionBeaconsFailedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionBeaconsRangedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionErrorEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLRegionStateDeterminedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLVisit</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreLocation.CLVisitedEventArgs</span></h3>
</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMTimeRange --> <div>
<h3>Type Changed: CoreMedia.CMTimeRange</h3>
<p>Removed field:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">[Obsolete ("Use InvalidRange")]
	public static CMTimeRange Invalid;</span>
</pre>

</div> <!-- end type CMTimeRange -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreSpotlight --> <div> 
<h2>Namespace CoreSpotlight</h2>
<h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSCustomAttributeKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSFileProtection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSIndexErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSIndexErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSIndexExtensionRequestHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSLocalizedString</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSPerson</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableIndex</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableIndexDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableIndexDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableIndexFetchHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableIndex_CSOptionalBatchingExtension</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.CSSearchableItemAttributeSet</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreSpotlight.ICSSearchableIndexDelegate</span></h3>
</div> <!-- end namespace CoreSpotlight -->
<!-- start namespace CoreText --> <div> 
<h2>Namespace CoreText</h2>
<!-- start type CTFontManager --> <div>
<h3>Type Changed: CoreText.CTFontManager</h3>
<p>Removed field:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">public static Foundation.NSString ErrorDomain;</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("API not available on iOS, it will always return false")]
	public static bool IsFontSupported (Foundation.NSUrl url);</span>
</pre>

</div> <!-- end type CTFontManager -->

</div> <!-- end namespace CoreText -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVImageBuffer --> <div>
<h3>Type Changed: CoreVideo.CVImageBuffer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; }</span>
</pre>

</div> <!-- end type CVImageBuffer -->
<!-- start type CVPixelBuffer --> <div>
<h3>Type Changed: CoreVideo.CVPixelBuffer</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use Lock(CVPixelBufferLock) instead")]
	public CVReturn Lock (CVOptionFlags lockFlags);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use Unlock(CVPixelBufferLock)")]
	public CVReturn Unlock (CVOptionFlags unlockFlags);</span>
</pre>

</div> <!-- end type CVPixelBuffer -->
<!-- start type CVPixelBufferPool --> <div>
<h3>Type Changed: CoreVideo.CVPixelBufferPool</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString AlphaChannelIsOpaque { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CGColorSpaceKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocationBottomFieldKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocationTopFieldKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_Bottom { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_BottomLeft { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_Center { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_DV420 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_Left { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_Top { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaLocation_TopLeft { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaSubsamplingKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaSubsampling_411 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaSubsampling_420 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ChromaSubsampling_422 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CleanApertureHeightKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CleanApertureHorizontalOffsetKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CleanApertureKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CleanApertureVerticalOffsetKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CleanApertureWidthKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimariesKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_P22 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_P3_D65 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DisplayDimensionsKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DisplayHeightKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DisplayWidthKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldCountKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldDetailKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldDetailSpatialFirstLineEarly { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldDetailSpatialFirstLineLate { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldDetailTemporalBottomFirst { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FieldDetailTemporalTopFirst { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString GammaLevelKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString MovieTimeKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString NonPropagatedAttachmentsKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PixelAspectRatioHorizontalSpacingKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PixelAspectRatioKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PixelAspectRatioVerticalSpacingKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PreferredCleanApertureKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString PropagatedAttachmentsKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TimeScaleKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TimeValueKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TransferFunctionKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TransferFunction_ITU_R_709_2 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TransferFunction_SMPTE_240M_1995 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TransferFunction_UseGamma { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrixKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_601_4 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_709_2 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString YCbCrMatrix_SMPTE_240M_1995 { get; }</span>
</pre>

</div> <!-- end type CVPixelBufferPool -->
<!-- start type CVPixelFormatDescription --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatDescription</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSDictionary Create (int pixelFormat);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void Register (Foundation.NSDictionary description, int pixelFormat);</span>
</pre>

</div> <!-- end type CVPixelFormatDescription -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSAttributedString --> <div>
<h3>Type Changed: Foundation.NSAttributedString</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static NSAttributedString CreateFrom (UIKit.NSTextAttachment attachment);</span>
</pre>

</div> <!-- end type NSAttributedString -->
<!-- start type NSError --> <div>
<h3>Type Changed: Foundation.NSError</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString CoreMotionErrorDomain { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString EABluetoothAccessoryPickerErrorDomain { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString MapKitErrorDomain { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString WatchKitErrorDomain { get; }</span>
</pre>

</div> <!-- end type NSError -->
<!-- start type NSFileManagerDelegate --> <div>
<h3>Type Changed: Foundation.NSFileManagerDelegate</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("API removed after iOS 2.0 / OSX 10.5. It will never be called by the OS.")]
	public virtual bool ShouldProceedAfterError (NSFileManager fm, NSDictionary errorInfo);</span>
</pre>

</div> <!-- end type NSFileManagerDelegate -->
<!-- start type NSFileManagerDelegate_Extensions --> <div>
<h3>Type Changed: Foundation.NSFileManagerDelegate_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("API removed after iOS 2.0 / OSX 10.5. It will never be called by the OS.")]
	public static bool ShouldProceedAfterError (INSFileManagerDelegate This, NSFileManager fm, NSDictionary errorInfo);</span>
</pre>

</div> <!-- end type NSFileManagerDelegate_Extensions -->
<!-- start type NSMutableAttributedString --> <div>
<h3>Type Changed: Foundation.NSMutableAttributedString</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public bool ReadFromFile (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ReadFromFile (NSUrl url, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);</span>
</pre>

</div> <!-- end type NSMutableAttributedString -->
<!-- start type NSNetService --> <div>
<h3>Type Changed: Foundation.NSNetService</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NSNetService ();</span>
</pre>

</div> <!-- end type NSNetService -->
<!-- start type NSObject --> <div>
<h3>Type Changed: Foundation.NSObject</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Do not use; this API does not properly retain/release existing/new values, so leaks and/or crashes may occur.")]
	public NSObject GetNativeField (string name);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool IsNewRefcountEnabled ();</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Do not use; this API does not properly retain/release existing/new values, so leaks and/or crashes may occur.")]
	public void SetNativeField (string name, NSObject value);</span>
</pre>

</div> <!-- end type NSObject -->
<!-- start type NSOperation --> <div>
<h3>Type Changed: Foundation.NSOperation</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use WaitUntilFinished method")]
	public virtual void WaitUntilFinishedNS ();</span>
</pre>

</div> <!-- end type NSOperation -->
<!-- start type NSStringDrawingContext --> <div>
<h3>Type Changed: Foundation.NSStringDrawingContext</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nfloat ActualTrackingAdjustment { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nfloat MinimumTrackingAdjustment { get; set; }</span>
</pre>

</div> <!-- end type NSStringDrawingContext -->
<!-- start type NSUrlConnection --> <div>
<h3>Type Changed: Foundation.NSUrlConnection</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual NewsstandKit.NKAssetDownload NewsstandAssetDownload { get; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>

</div> <!-- end type NSUrlConnection -->
<!-- start type NSUrlSession --> <div>
<h3>Type Changed: Foundation.NSUrlSession</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks.")]
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks.")]
	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionActiveTasks&gt; GetTasksAsync ();</span>
</pre>

</div> <!-- end type NSUrlSession -->
<!-- start type NSUrl_PromisedItems --> <div>
<h3>Type Changed: Foundation.NSUrl_PromisedItems</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use overload with an 'out NSObject value' parameter.")]
	public static bool GetPromisedItemResourceValue (NSUrl This, NSObject value, NSString key, out NSError error);</span>
</pre>

</div> <!-- end type NSUrl_PromisedItems -->
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreSpotlight.CSSearchableItemAttributeSet ContentAttributeSet { get; set; }</span>
</pre>

</div> <!-- end type NSUserActivity -->
<!-- start type NSUserDefaults --> <div>
<h3>Type Changed: Foundation.NSUserDefaults</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString CompletedInitialSyncNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString DidChangeAccountsNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString DidChangeNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString SizeLimitExceededNotification { get; }</span>
</pre>
<h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSUserDefaults.Notifications</span></h3>
</div> <!-- end type NSUserDefaults -->
<!-- start type NSValueTransformer --> <div>
<h3>Type Changed: Foundation.NSValueTransformer</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString CompletedInitialSyncNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString DidChangeAccountsNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString SizeLimitExceededNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static NSString UserDefaultsDidChangeNotification { get; }</span>
</pre>
<h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSValueTransformer.Notifications</span></h3>
</div> <!-- end type NSValueTransformer -->
<h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSBundleExecutableArchitecture</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSDistributedNotificationCenter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSTextWritingDirection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSUrlSessionActiveTasks</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Foundation.NSUrlSessionPendingTasks</span></h3>
</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCController --> <div>
<h3>Type Changed: GameController.GCController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCMicroGamepad MicroGamepad { get; }</span>
</pre>
</div>

</div> <!-- end type GCController -->
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual OpenTK.Quaterniond Attitude { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual OpenTK.Vector3d RotationRate { get; }</span>
</pre>

</div> <!-- end type GCMotion -->
<div> <!-- start type GCEventViewController -->
<h3>New Type GameController.GCEventViewController</h3>
<pre class='added' data-is-non-breaking="">
public class GCEventViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GCEventViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GCEventViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GCEventViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GCEventViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GCEventViewController (string nibName, Foundation.NSBundle bundle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ControllerUserInteractionEnabled { get; set; }</span>
}
</pre>
</div> <!-- end type GCEventViewController -->
<div> <!-- start type GCMicroGamepad -->
<h3>New Type GameController.GCMicroGamepad</h3>
<pre class='added' data-is-non-breaking="">
public class GCMicroGamepad : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GCMicroGamepad (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GCMicroGamepad (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonInput ButtonA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonInput ButtonX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCController Controller { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerDirectionPad Dpad { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportsAbsoluteDpadValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCMicroGamepadSnapshot SaveSnapshot { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCMicroGamepadValueChangedHandler ValueChangedHandler { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type GCMicroGamepad -->
<div> <!-- start type GCMicroGamepadSnapShotDataV100 -->
<h3>New Type GameController.GCMicroGamepadSnapShotDataV100</h3>
<pre class='added' data-is-non-breaking="">
public struct GCMicroGamepadSnapShotDataV100 {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float ButtonA;</span>
	<span class='added added-field ' data-is-non-breaking="">public float ButtonX;</span>
	<span class='added added-field ' data-is-non-breaking="">public float DPadX;</span>
	<span class='added added-field ' data-is-non-breaking="">public float DPadY;</span>
	<span class='added added-field ' data-is-non-breaking="">public ushort Size;</span>
	<span class='added added-field ' data-is-non-breaking="">public ushort Version;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData ToNSData ();</span>
}
</pre>
</div> <!-- end type GCMicroGamepadSnapShotDataV100 -->
<div> <!-- start type GCMicroGamepadSnapshot -->
<h3>New Type GameController.GCMicroGamepadSnapshot</h3>
<pre class='added' data-is-non-breaking="">
public class GCMicroGamepadSnapshot : GameController.GCMicroGamepad, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GCMicroGamepadSnapshot ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GCMicroGamepadSnapshot (Foundation.NSData data);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GCMicroGamepadSnapshot (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GCMicroGamepadSnapshot (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GCMicroGamepadSnapshot (GCController controller, Foundation.NSData data);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData SnapshotData { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool TryGetSnapshotData (Foundation.NSData data, out GCMicroGamepadSnapShotDataV100 snapshotData);</span>
}
</pre>
</div> <!-- end type GCMicroGamepadSnapshot -->
<div> <!-- start type GCMicroGamepadValueChangedHandler -->
<h3>New Type GameController.GCMicroGamepadValueChangedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GCMicroGamepadValueChangedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GCMicroGamepadValueChangedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (GCMicroGamepad gamepad, GCControllerElement element, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (GCMicroGamepad gamepad, GCControllerElement element);</span>
}
</pre>
</div> <!-- end type GCMicroGamepadValueChangedHandler -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKAchievement --> <div>
<h3>Type Changed: GameKit.GKAchievement</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool Hidden { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string PlayerID { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIKit.UIViewController ChallengeComposeController (GKPlayer[] playerIDs, string message, GKChallengeComposeHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void IssueChallengeToPlayers (string[] playerIDs, string message);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ReportAchievement (System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task ReportAchievementAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SelectChallengeablePlayerIDs (string[] playerIDs, System.Action&lt;System.String[],Foundation.NSError&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; SelectChallengeablePlayerIDsAsync (string[] playerIDs);</span>
</pre>

</div> <!-- end type GKAchievement -->
<!-- start type GKChallenge --> <div>
<h3>Type Changed: GameKit.GKChallenge</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string IssuingPlayerID { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string ReceivingPlayerID { get; }</span>
</pre>

</div> <!-- end type GKChallenge -->
<!-- start type GKGameCenterViewController --> <div>
<h3>Type Changed: GameKit.GKGameCenterViewController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string LeaderboardCategory { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string LeaderboardIdentifier { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual GKLeaderboardTimeScope LeaderboardTimeScope { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual GKGameCenterViewControllerState ViewState { get; set; }</span>
</pre>

</div> <!-- end type GKGameCenterViewController -->
<!-- start type GKInvite --> <div>
<h3>Type Changed: GameKit.GKInvite</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Inviter { get; }</span>
</pre>

</div> <!-- end type GKInvite -->
<!-- start type GKInviteEventListener --> <div>
<h3>Type Changed: GameKit.GKInviteEventListener</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRequestMatch (GKPlayer player, string[] playerIDs);</span>
</pre>

</div> <!-- end type GKInviteEventListener -->
<!-- start type GKInviteEventListener_Extensions --> <div>
<h3>Type Changed: GameKit.GKInviteEventListener_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, string[] playerIDs);</span>
</pre>

</div> <!-- end type GKInviteEventListener_Extensions -->
<!-- start type GKLeaderboard --> <div>
<h3>Type Changed: GameKit.GKLeaderboard</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Category { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void LoadCategories (GKCategoryHandler categoryHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static System.Threading.Tasks.Task&lt;GKCategoryResult&gt; LoadCategoriesAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LoadImage (GKImageLoadedHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;UIKit.UIImage&gt; LoadImageAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void SetDefaultLeaderboard (string leaderboardIdentifier, System.Action&lt;Foundation.NSError&gt; notificationHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string leaderboardIdentifier);</span>
</pre>

</div> <!-- end type GKLeaderboard -->
<!-- start type GKLeaderboardSet --> <div>
<h3>Type Changed: GameKit.GKLeaderboardSet</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LoadImage (GKImageLoadedHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;UIKit.UIImage&gt; LoadImageAsync ();</span>
</pre>

</div> <!-- end type GKLeaderboardSet -->
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] Friends { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Authenticate (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DeleteSavedGames (string name, System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FetchSavedGames (System.Action&lt;GKSavedGame[],Foundation.NSError&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LoadDefaultLeaderboardCategoryID (System.Action&lt;System.String,Foundation.NSError&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;string&gt; LoadDefaultLeaderboardCategoryIDAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void LoadFriends (GKFriendsHandler handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; LoadFriendsAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ResolveConflictingSavedGames (GKSavedGame[] conflictingSavedGames, Foundation.NSData data, System.Action&lt;GKSavedGame[],Foundation.NSError&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SaveGameData (Foundation.NSData data, string name, System.Action&lt;GKSavedGame,Foundation.NSError&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);</span>
</pre>

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKLocalPlayerListener --> <div>
<h3>Type Changed: GameKit.GKLocalPlayerListener</h3>
<p>Removed interface:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">IGKSavedGameListener</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRequestMatch (GKPlayer player, string[] playerIDs);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HasConflictingSavedGames (GKPlayer player, GKSavedGame[] savedGames);</span>
</pre>

</div> <!-- end type GKLocalPlayerListener -->
<!-- start type GKMatch --> <div>
<h3>Type Changed: GameKit.GKMatch</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] PlayersIDs { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public GKMatchReinvitation ShouldReinvitePlayer { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;GKDataEventArgs&gt; DataReceived;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;GKStateEventArgs&gt; StateChanged;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ChooseBestHostPlayer (System.Action&lt;string&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;string&gt; ChooseBestHostPlayerAsync ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool SendData (Foundation.NSData data, string[] players, GKMatchSendDataMode mode, Foundation.NSError error);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool SendData (Foundation.NSData data, string[] players, GKMatchSendDataMode mode, out Foundation.NSError error);</span>
</pre>

</div> <!-- end type GKMatch -->
<!-- start type GKMatchDelegate --> <div>
<h3>Type Changed: GameKit.GKMatchDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DataReceived (GKMatch match, Foundation.NSData data, string playerId);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldReinvitePlayer (GKMatch match, string playerId);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StateChanged (GKMatch match, string playerId, GKPlayerConnectionState state);</span>
</pre>

</div> <!-- end type GKMatchDelegate -->
<!-- start type GKMatchDelegate_Extensions --> <div>
<h3>Type Changed: GameKit.GKMatchDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DataReceived (IGKMatchDelegate This, GKMatch match, Foundation.NSData data, string playerId);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool ShouldReinvitePlayer (IGKMatchDelegate This, GKMatch match, string playerId);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void StateChanged (IGKMatchDelegate This, GKMatch match, string playerId, GKPlayerConnectionState state);</span>
</pre>

</div> <!-- end type GKMatchDelegate_Extensions -->
<!-- start type GKMatchRequest --> <div>
<h3>Type Changed: GameKit.GKMatchRequest</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual System.Action&lt;System.String,GameKit.GKInviteeResponse&gt; InviteeResponseHandler { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] PlayersToInvite { get; set; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use RecipientResponseHandler property")]
	public virtual void SetRecipientResponseHandler (System.Action&lt;GKPlayer,GameKit.GKInviteRecipientResponse&gt; handler);</span>
</pre>

</div> <!-- end type GKMatchRequest -->
<!-- start type GKMatchmaker --> <div>
<h3>Type Changed: GameKit.GKMatchmaker</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual GKInviteHandler InviteHandler { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void CancelInvite (string playerID);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FindPlayers (GKMatchRequest request, GKFriendsHandler playerHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; FindPlayersAsync (GKMatchRequest request);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use InviteHandler property")]
	public virtual void SetInviteHandler (GKInviteHandler handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void StartBrowsingForNearbyPlayers (System.Action&lt;System.String,System.Boolean&gt; reachableHandler);</span>
</pre>

</div> <!-- end type GKMatchmaker -->
<!-- start type GKMatchmakerViewController --> <div>
<h3>Type Changed: GameKit.GKMatchmakerViewController</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string DefaultInvitationMessage { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;GKPlayersEventArgs&gt; DidFindPlayers;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;GKPlayerEventArgs&gt; ReceivedAcceptFromHostedPlayer;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetHostedPlayerConnected (string playerID, bool connected);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetHostedPlayerReady (string playerID);</span>
</pre>

</div> <!-- end type GKMatchmakerViewController -->
<!-- start type GKMatchmakerViewControllerDelegate --> <div>
<h3>Type Changed: GameKit.GKMatchmakerViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidFindPlayers (GKMatchmakerViewController viewController, string[] playerIDs);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ReceivedAcceptFromHostedPlayer (GKMatchmakerViewController viewController, string playerID);</span>
</pre>

</div> <!-- end type GKMatchmakerViewControllerDelegate -->
<!-- start type GKMatchmakerViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: GameKit.GKMatchmakerViewControllerDelegate_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void ReceivedAcceptFromHostedPlayer (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, string playerID);</span>
</pre>

</div> <!-- end type GKMatchmakerViewControllerDelegate_Extensions -->
<!-- start type GKPeerPickerConnectionType --> <div>
<h3>Type Changed: GameKit.GKPeerPickerConnectionType</h3>
<p>Removed values:</p>
<pre class='removed' data-is-breaking="">
	<span class='removed removed-field breaking' data-is-breaking="">Nearby = 2,</span>
	<span class='removed removed-field breaking' data-is-breaking="">Online = 1,</span>
</pre>

</div> <!-- end type GKPeerPickerConnectionType -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: GameKit.GKPlayer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool IsFriend { get; }</span>
</pre>

</div> <!-- end type GKPlayer -->
<!-- start type GKScore --> <div>
<h3>Type Changed: GameKit.GKScore</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Category { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIKit.UIViewController ChallengeComposeController (string[] playerIDs, string message, GKChallengeComposeHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void IssueChallengeToPlayers (string[] playerIDs, string message);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ReportScore (System.Action&lt;Foundation.NSError&gt; errorHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task ReportScoreAsync ();</span>
</pre>

</div> <!-- end type GKScore -->
<!-- start type GKTurnBasedEventListener --> <div>
<h3>Type Changed: GameKit.GKTurnBasedEventListener</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
</pre>

</div> <!-- end type GKTurnBasedEventListener -->
<!-- start type GKTurnBasedEventListener_Extensions --> <div>
<h3>Type Changed: GameKit.GKTurnBasedEventListener_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidRequestMatchWithPlayers (IGKTurnBasedEventListener This, GKPlayer player, string[] playerIDsToInvite);</span>
</pre>

</div> <!-- end type GKTurnBasedEventListener_Extensions -->
<!-- start type GKTurnBasedMatch --> <div>
<h3>Type Changed: GameKit.GKTurnBasedMatch</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, System.Action&lt;Foundation.NSError&gt; noCompletion);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task EndTurnWithNextParticipantAsync (GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, System.Action&lt;Foundation.NSError&gt; onCompletion);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData);</span>
</pre>

</div> <!-- end type GKTurnBasedMatch -->
<!-- start type GKTurnBasedMatchmakerViewControllerDelegate --> <div>
<h3>Type Changed: GameKit.GKTurnBasedMatchmakerViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FoundMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PlayerQuitForMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);</span>
</pre>

</div> <!-- end type GKTurnBasedMatchmakerViewControllerDelegate -->
<!-- start type GKTurnBasedParticipant --> <div>
<h3>Type Changed: GameKit.GKTurnBasedParticipant</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string PlayerID { get; }</span>
</pre>

</div> <!-- end type GKTurnBasedParticipant -->
<!-- start type GKVoiceChat --> <div>
<h3>Type Changed: GameKit.GKVoiceChat</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string[] PlayerIDs { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual GKPlayerStateUpdateHandler PlayerStateUpdateHandler { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use SetMute(bool,string) method")]
	public virtual void SetMute (bool isMuted, GKPlayer player);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetMute (bool isMuted, string playerID);</span>
</pre>

</div> <!-- end type GKVoiceChat -->
<!-- start type IGKLocalPlayerListener --> <div>
<h3>Type Changed: GameKit.IGKLocalPlayerListener</h3>
<p>Removed interface:</p>

<pre>
	<span class='removed removed-interface breaking' data-is-breaking="">IGKSavedGameListener</span>
</pre>

</div> <!-- end type IGKLocalPlayerListener -->
<!-- start type IGKMatchmakerViewControllerDelegate --> <div>
<h3>Type Changed: GameKit.IGKMatchmakerViewControllerDelegate</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidFindPlayers (GKMatchmakerViewController viewController, string[] playerIDs);</span>
</pre>

</div> <!-- end type IGKMatchmakerViewControllerDelegate -->
<!-- start type IGKTurnBasedMatchmakerViewControllerDelegate --> <div>
<h3>Type Changed: GameKit.IGKTurnBasedMatchmakerViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FoundMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PlayerQuitForMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);</span>
</pre>

</div> <!-- end type IGKTurnBasedMatchmakerViewControllerDelegate -->
<h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKAchievementViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKAchievementViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKCategoryHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKCategoryResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKChallengeEventHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKChallengeEventHandlerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKChallengeEventHandlerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKChallengePredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKDataEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKDataReceivedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKFriendRequestComposeViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKFriendRequestComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKFriendsHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKInviteHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKLeaderboardViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKLeaderboardViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKMatchReinvitation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerChangedStateEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerConnectionEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerPickerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerPickerControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPlayerEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPlayerStateUpdateHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPlayersEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSavedGame</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSavedGameListener</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSavedGameListener_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKSessionDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKStateEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKTurnBasedEventHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKTurnBasedEventHandlerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKTurnBasedEventHandlerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKVoiceChatClient</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKVoiceChatClient_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKVoiceChatService</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKAchievementViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKChallengeEventHandlerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKFriendRequestComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKLeaderboardViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKPeerPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKSavedGameListener</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKTurnBasedEventHandlerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.IGKVoiceChatClient</span></h3>
</div> <!-- end namespace GameKit -->
<!-- start namespace JavaScriptCore --> <div> 
<h2>Namespace JavaScriptCore</h2>
<!-- start type JSManagedValue --> <div>
<h3>Type Changed: JavaScriptCore.JSManagedValue</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public JSManagedValue ();</span>
</pre>

</div> <!-- end type JSManagedValue -->

</div> <!-- end namespace JavaScriptCore -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual MKAnnotationViewDragState DragState { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool Draggable { get; set; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetDragState (MKAnnotationViewDragState newDragState, bool animated);</span>
</pre>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKDirections --> <div>
<h3>Type Changed: MapKit.MKDirections</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public MKDirections ();</span>
</pre>

</div> <!-- end type MKDirections -->
<!-- start type MKLocalSearchCompleter --> <div>
<h3>Type Changed: MapKit.MKLocalSearchCompleter</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public MKLocalSearchCompleter ();</span>
</pre>

</div> <!-- end type MKLocalSearchCompleter -->
<!-- start type MKLocalSearchCompletion --> <div>
<h3>Type Changed: MapKit.MKLocalSearchCompletion</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public MKLocalSearchCompletion ();</span>
</pre>

</div> <!-- end type MKLocalSearchCompletion -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public void OpenInMaps (MKLaunchOptions launchOptions);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool OpenMaps (MKMapItem[] mapItems, MKLaunchOptions launchOptions);</span>
</pre>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public MKMapViewOverlay GetViewForOverlay { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool PitchEnabled { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool RotateEnabled { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsCompass { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsScale { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;MKMapViewAccessoryTappedEventArgs&gt; CalloutAccessoryControlTapped;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;MKMapViewDragStateEventArgs&gt; ChangedDragState;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual MKOverlayView ViewForOverlay (IMKOverlay overlay);</span>
</pre>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void CalloutAccessoryControlTapped (MKMapView mapView, MKAnnotationView view, UIKit.UIControl control);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ChangedDragState (MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, IMKOverlay overlay);</span>
</pre>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void CalloutAccessoryControlTapped (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView view, UIKit.UIControl control);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void ChangedDragState (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidAddOverlayViews (IMKMapViewDelegate This, MKMapView mapView, MKOverlayView overlayViews);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static MKOverlayView GetViewForOverlay (IMKMapViewDelegate This, MKMapView mapView, IMKOverlay overlay);</span>
</pre>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<!-- start type MKPinAnnotationView --> <div>
<h3>Type Changed: MapKit.MKPinAnnotationView</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual MKPinAnnotationColor PinColor { get; set; }</span>
</pre>

</div> <!-- end type MKPinAnnotationView -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate, MKPlacemarkAddress addressDictionary);</span>
</pre>

</div> <!-- end type MKPlacemark -->
<!-- start type MKUserLocation --> <div>
<h3>Type Changed: MapKit.MKUserLocation</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreLocation.CLHeading Heading { get; }</span>
</pre>

</div> <!-- end type MKUserLocation -->
<h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.IMKReverseGeocoderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKAnnotationViewDragState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKCircleView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKDirectionsMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKLaunchOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKMapViewAccessoryTappedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKMapViewDragStateEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKMapViewOverlay</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKOverlayPathView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKOverlayView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKOverlayViewsEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKPinAnnotationColor</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKPlacemarkAddress</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKPolygonView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKPolylineView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKReverseGeocoder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKReverseGeocoderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MapKit.MKUserTrackingBarButtonItem</span></h3>
</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPMediaPlaylistProperty --> <div>
<h3>Type Changed: MediaPlayer.MPMediaPlaylistProperty</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString AuthorDisplayName { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DescriptionText { get; }</span>
</pre>

</div> <!-- end type MPMediaPlaylistProperty -->
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public MPNowPlayingInfo NowPlaying { get; set; }</span>
</pre>

</div> <!-- end type MPNowPlayingInfoCenter -->
<h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.IMPMediaPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.IMPPlayableContentDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.IMPPlayableContentDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.ItemsPickedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPContentItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaEntity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaGrouping</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaItemArtwork</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaItemCollection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaItemEnumerator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaLibrary</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaLibraryAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPickerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPickerControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPlaylist</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPlaylistAttribute</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPlaylistCreationMetadata</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPredicateComparison</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaPropertyPredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaQuerySection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMediaType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieAccessLog</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieAccessLogEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieControlStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieErrorLog</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieErrorLogEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieFinishReason</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieLoadState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieMediaType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlaybackState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerFinishedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerFullScreenEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerThumbnailEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerTimedMetadataEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMoviePlayerViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieRepeatMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieScalingMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieSourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMovieTimeOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMusicPlaybackState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMusicPlayerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMusicRepeatMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPMusicShuffleMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPNowPlayingInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentDataSource_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPPlayableContentManagerContext</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPTimedMetadata</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPVolumeSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MediaPlayer.MPVolumeView</span></h3>
</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLPixelFormat --> <div>
<h3>Type Changed: Metal.MTLPixelFormat</h3>
<p>Removed value:</p>
<pre class='removed' data-is-breaking="">
	<span class='removed removed-field breaking' data-is-breaking="">R8Unorm_sRGB = 11,</span>
</pre>

</div> <!-- end type MTLPixelFormat -->

</div> <!-- end namespace Metal -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<!-- start type MPSImageLanczosScale --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLanczosScale</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual MPSScaleTransform? ScaleTransform { get; set; }</span>
</pre>

</div> <!-- end type MPSImageLanczosScale -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Removed fields:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string AccountsLibrary = "/System/Library/Frameworks/Accounts.framework/Accounts";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string AddressBookLibrary = "/System/Library/Frameworks/AddressBook.framework/AddressBook";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string AddressBookUILibrary = "/System/Library/Frameworks/AddressBookUI.framework/AddressBookUI";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string AssetsLibraryLibrary = "/System/Library/Frameworks/AssetsLibrary.framework/AssetsLibrary";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string ContactsLibrary = "/System/Library/Frameworks/Contacts.framework/Contacts";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string ContactsUILibrary = "/System/Library/Frameworks/ContactsUI.framework/ContactsUI";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string CoreAudioKitLibrary = "/System/Library/Frameworks/CoreAudioKit.framework/CoreAudioKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string CoreMidiLibrary = "/System/Library/Frameworks/CoreMIDI.framework/CoreMIDI";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string CoreMotionLibrary = "/System/Library/Frameworks/CoreMotion.framework/CoreMotion";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string CoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string CoreTelephonyLibrary = "/System/Library/Frameworks/CoreTelephony.framework/CoreTelephony";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string EventKitLibrary = "/System/Library/Frameworks/EventKit.framework/EventKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string HealthKitLibrary = "/System/Library/Frameworks/HealthKit.framework/HealthKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string HealthKitUILibrary = "/System/Library/Frameworks/HealthKitUI.framework/HealthKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string HomeKitLibrary = "/System/Library/Frameworks/HomeKit.framework/HomeKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string LocalAuthenticationLibrary = "/System/Library/Frameworks/LocalAuthentication.framework/LocalAuthentication";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string MessageUILibrary = "/System/Library/Frameworks/MessageUI.framework/MessageUI";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string NetworkExtensionLibrary = "/System/Library/Frameworks/NetworkExtension.framework/NetworkExtension";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string NewsstandKitLibrary = "/System/Library/Frameworks/NewsstandKit.framework/NewsstandKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string PhotosLibrary = "/System/Library/Frameworks/Photos.framework/Photos";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string PhotosUILibrary = "/System/Library/Frameworks/PhotosUI.framework/PhotosUI";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string PushKitLibrary = "/System/Library/Frameworks/PushKit.framework/PushKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string QuickLookLibrary = "/System/Library/Frameworks/QuickLook.framework/QuickLook";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string ReplayKitLibrary = "/System/Library/Frameworks/ReplayKit.framework/ReplayKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string SafariServicesLibrary = "/System/Library/Frameworks/SafariServices.framework/SafariServices";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string SystemLibrary = "/usr/lib/libSystem.dylib";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string WatchConnectivityLibrary = "/System/Library/Frameworks/WatchConnectivity.framework/WatchConnectivity";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string WatchKitLibrary = "/System/Library/Frameworks/WatchKit.framework/WatchKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string WebKitLibrary = "/System/Library/Frameworks/WebKit.framework/WebKit";</span>
	<span class='removed removed-field breaking' data-is-breaking="">public static const string iAdLibrary = "/System/Library/Frameworks/iAd.framework/iAd";</span>
</pre>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"9.3"</span> <span class='added '>"9.2"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string TVMLKitLibrary = "/System/Library/Frameworks/TVMLKit.framework/TVMLKit";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string TVServicesLibrary = "/System/Library/Frameworks/TVServices.framework/TVServices";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.AvailabilityAttribute</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.BlockFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.MacAttribute</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.Platform</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.PlatformHelper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ObjCRuntime.iOSAttribute</span></h3>
</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace OpenGLES --> <div> 
<h2>Namespace OpenGLES</h2>
<!-- start type EAGLContext --> <div>
<h3>Type Changed: OpenGLES.EAGLContext</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public EAGLContext ();</span>
</pre>

</div> <!-- end type EAGLContext -->

</div> <!-- end namespace OpenGLES -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNAction --> <div>
<h3>Type Changed: SceneKit.SCNAction</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use TimingFunction property")]
	public virtual void SetTimingFunction (System.Action&lt;float&gt; timingFunction);</span>
</pre>

</div> <!-- end type SCNAction -->
<!-- start type SCNGeometry --> <div>
<h3>Type Changed: SceneKit.SCNGeometry</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use the Create(SCNGeometrySource[], SCNGeometryElement[]) method instead, as it has a strongly typed return")]
	public static Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);</span>
</pre>

</div> <!-- end type SCNGeometry -->
<!-- start type SCNLight --> <div>
<h3>Type Changed: SceneKit.SCNLight</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public virtual Foundation.NSObject GetAttribute (Foundation.NSString lightAttribute);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public virtual void SetAttribute (Foundation.NSObject value, Foundation.NSString attribuetKey);</span>
</pre>

</div> <!-- end type SCNLight -->
<!-- start type SCNSceneLoadingOptions --> <div>
<h3>Type Changed: SceneKit.SCNSceneLoadingOptions</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public bool? ConvertToYUp { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public float? ConvertUnitsToMeters { get; set; }</span>
</pre>

</div> <!-- end type SCNSceneLoadingOptions -->
<!-- start type SCNSceneRenderer_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static SCNHitTestResult[] HitTest (ISCNSceneRenderer This, CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);</span>
</pre>

</div> <!-- end type SCNSceneRenderer_Extensions -->
<!-- start type SCNSceneSourceLoading --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceLoading</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ConvertToYUpKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString ConvertUnitsToMetersKey { get; }</span>
</pre>

</div> <!-- end type SCNSceneSourceLoading -->
<h3>Removed Type <span class='breaking' data-is-breaking="">SceneKit.ISCNSceneExportDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SceneKit.SCNSceneExportDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SceneKit.SCNSceneExportDelegate_Extensions</span></h3>
</div> <!-- end namespace SceneKit -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKAction --> <div>
<h3>Type Changed: SpriteKit.SKAction</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use FalloffBy method")]
	public static SKAction Falloff (float to, double duration);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use TimingFunction property")]
	public virtual void SetTimingFunction (SKActionTimingFunction timingFunction);</span>
</pre>

</div> <!-- end type SKAction -->
<!-- start type SKFieldNode --> <div>
<h3>Type Changed: SpriteKit.SKFieldNode</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use the method CreateVortexField instead")]
	public static SKFieldNode CraeteVortexField ();</span>
</pre>

</div> <!-- end type SKFieldNode -->
<!-- start type SKShapeNode --> <div>
<h3>Type Changed: SpriteKit.SKShapeNode</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static SKShapeNode FromPoints (ref CoreGraphics.CGPoint points, uint numPoints);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static SKShapeNode FromSplinePoints (ref CoreGraphics.CGPoint points, uint numPoints);</span>
</pre>

</div> <!-- end type SKShapeNode -->
<!-- start type SKView --> <div>
<h3>Type Changed: SpriteKit.SKView</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SKView ();</span>
</pre>

</div> <!-- end type SKView -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SKCloudServiceController ();</span>
</pre>

</div> <!-- end type SKCloudServiceController -->
<!-- start type SKPayment --> <div>
<h3>Type Changed: StoreKit.SKPayment</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use FromProduct (SKProduct) instead.")]
	public static SKPayment PaymentWithProduct (SKProduct product);</span>

	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use FromProductIdentifier (string) instead.")]
	public static SKPayment PaymentWithProduct (string identifier);</span>
</pre>

</div> <!-- end type SKPayment -->
<!-- start type SKPaymentTransactionObserver --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use RestoreCompletedTransactionsFinished (SKPaymentQueue) instead.")]
	public virtual void PaymentQueueRestoreCompletedTransactionsFinished (SKPaymentQueue queue);</span>
</pre>

</div> <!-- end type SKPaymentTransactionObserver -->
<!-- start type SKPaymentTransactionObserver_Extensions --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use RestoreCompletedTransactionsFinished (SKPaymentQueue) instead.")]
	public static void PaymentQueueRestoreCompletedTransactionsFinished (ISKPaymentTransactionObserver This, SKPaymentQueue queue);</span>
</pre>

</div> <!-- end type SKPaymentTransactionObserver_Extensions -->
<h3>Removed Type <span class='breaking' data-is-breaking="">StoreKit.ISKStoreProductViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">StoreKit.SKStoreProductViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">StoreKit.SKStoreProductViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">StoreKit.SKStoreProductViewControllerDelegate_Extensions</span></h3>
</div> <!-- end namespace StoreKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type INSTextLayoutOrientationProvider --> <div>
<h3>Type Changed: UIKit.INSTextLayoutOrientationProvider</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public abstract NSTextLayoutOrientation LayoutOrientation { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div></pre>

</div> <!-- end type INSTextLayoutOrientationProvider -->
<!-- start type IUIViewControllerPreviewing --> <div>
<h3>Type Changed: UIKit.IUIViewControllerPreviewing</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public abstract Foundation.NSObject WeakDelegate { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div></pre>

</div> <!-- end type IUIViewControllerPreviewing -->
<!-- start type NSIdentifier --> <div>
<h3>Type Changed: UIKit.NSIdentifier</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Use GetIdentifier method")]
	public static string Identifier (NSLayoutConstraint This);</span>
</pre>

</div> <!-- end type NSIdentifier -->
<!-- start type NSTextContainer --> <div>
<h3>Type Changed: UIKit.NSTextContainer</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public virtual NSTextLayoutOrientation LayoutOrientation { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div></pre>

</div> <!-- end type NSTextContainer -->
<!-- start type NSTextStorage --> <div>
<h3>Type Changed: UIKit.NSTextStorage</h3>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public virtual nint ChangeInLength { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div><div data-is-breaking="">	public virtual Foundation.NSRange EditedRange { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div></pre>

</div> <!-- end type NSTextStorage -->
<!-- start type UIAccessibilityCustomAction --> <div>
<h3>Type Changed: UIKit.UIAccessibilityCustomAction</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public UIAccessibilityCustomAction ();</span>
</pre>

</div> <!-- end type UIAccessibilityCustomAction -->
<!-- start type UIAdaptivePresentationControllerDelegate --> <div>
<h3>Type Changed: UIKit.UIAdaptivePresentationControllerDelegate</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Incorrect signature. Use the overload with a UITraitCollection parameter.")]
	public virtual UIViewController GetAdaptivePresentationStyle (UIPresentationController controller, UIModalPresentationStyle style);</span>
</pre>

</div> <!-- end type UIAdaptivePresentationControllerDelegate -->
<!-- start type UIAdaptivePresentationControllerDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIAdaptivePresentationControllerDelegate_Extensions</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">[Obsolete ("Incorrect signature. Use the overload with a UITraitCollection parameter.")]
	public static UIViewController GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);</span>
</pre>

</div> <!-- end type UIAdaptivePresentationControllerDelegate_Extensions -->
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nint ApplicationIconBadgeNumber { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ApplicationSupportsShakeToEdit { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static double BackgroundFetchIntervalMinimum { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static double BackgroundFetchIntervalNever { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIBackgroundRefreshStatus BackgroundRefreshStatus { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString BackgroundRefreshStatusDidChangeNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIUserNotificationSettings CurrentUserNotificationSettings { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidChangeStatusBarFrameNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidChangeStatusBarOrientationNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIRemoteNotificationType EnabledRemoteNotificationTypes { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString LaunchOptionsLocalNotificationKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString LaunchOptionsNewsstandDownloadsKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString LaunchOptionsRemoteNotificationKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString LaunchOptionsShortcutItemKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool NetworkActivityIndicatorVisible { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UILocalNotification[] ScheduledLocalNotifications { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIApplicationShortcutItem[] ShortcutItems { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGRect StatusBarFrame { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString StatusBarFrameUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool StatusBarHidden { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIInterfaceOrientation StatusBarOrientation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual double StatusBarOrientationAnimationDuration { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString StatusBarOrientationUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIStatusBarStyle StatusBarStyle { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString WillChangeStatusBarFrameNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString WillChangeStatusBarOrientationNotification { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void CancelAllLocalNotifications ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void CancelLocalNotification (UILocalNotification notification);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ClearKeepAliveTimeout ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PresentLocalNotificationNow (UILocalNotification notification);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RegisterForRemoteNotificationTypes (UIRemoteNotificationType types);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RegisterUserNotificationSettings (UIUserNotificationSettings notificationSettings);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScheduleLocalNotification (UILocalNotification notification);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool SetKeepAliveTimeout (double timeout, System.Action handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetMinimumBackgroundFetchInterval (double minimumBackgroundFetchInterval);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetNewsstandIconImage (UIImage image);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetStatusBarHidden (bool hidden, bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetStatusBarHidden (bool state, UIStatusBarAnimation animation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetStatusBarOrientation (UIInterfaceOrientation orientation, bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetStatusBarStyle (UIStatusBarStyle statusBarStyle, bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask SupportedInterfaceOrientationsForWindow (UIWindow window);</span>
</pre>
<!-- start type UIApplication.Notifications --> <div>
<h3>Type Changed: UIKit.UIApplication.Notifications</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveDidChangeStatusBarFrame (System.EventHandler&lt;UIStatusBarFrameChangeEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveDidChangeStatusBarOrientation (System.EventHandler&lt;UIStatusBarOrientationChangeEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveWillChangeStatusBarFrame (System.EventHandler&lt;UIStatusBarFrameChangeEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveWillChangeStatusBarOrientation (System.EventHandler&lt;UIStatusBarOrientationChangeEventArgs&gt; handler);</span>
</pre>

</div> <!-- end type UIApplication.Notifications -->

</div> <!-- end type UIApplication -->
<!-- start type UIApplicationDelegate --> <div>
<h3>Type Changed: UIKit.UIApplicationDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool AccessibilityPerformMagicTap ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ChangedStatusBarFrame (UIApplication application, CoreGraphics.CGRect oldStatusBarFrame);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidChangeStatusBarOrientation (UIApplication application, UIInterfaceOrientation oldStatusBarOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidReceiveRemoteNotification (UIApplication application, Foundation.NSDictionary userInfo, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRegisterUserNotificationSettings (UIApplication application, UIUserNotificationSettings notificationSettings);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIApplication application, UIWindow forWindow);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HandleAction (UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HandleAction (UIApplication application, string actionIdentifier, UILocalNotification localNotification, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HandleAction (UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, Foundation.NSDictionary responseInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HandleAction (UIApplication application, string actionIdentifier, UILocalNotification localNotification, Foundation.NSDictionary responseInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool HandleOpenURL (UIApplication application, Foundation.NSUrl url);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool OpenUrl (UIApplication application, Foundation.NSUrl url, string sourceApplication, Foundation.NSObject annotation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PerformActionForShortcutItem (UIApplication application, UIApplicationShortcutItem shortcutItem, UIOperationHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PerformFetch (UIApplication application, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ReceivedLocalNotification (UIApplication application, UILocalNotification notification);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillChangeStatusBarFrame (UIApplication application, CoreGraphics.CGRect newStatusBarFrame);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillChangeStatusBarOrientation (UIApplication application, UIInterfaceOrientation newStatusBarOrientation, double duration);</span>
</pre>

</div> <!-- end type UIApplicationDelegate -->
<!-- start type UIApplicationDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIApplicationDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool AccessibilityPerformMagicTap (IUIApplicationDelegate This);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void ChangedStatusBarFrame (IUIApplicationDelegate This, UIApplication application, CoreGraphics.CGRect oldStatusBarFrame);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidChangeStatusBarOrientation (IUIApplicationDelegate This, UIApplication application, UIInterfaceOrientation oldStatusBarOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidReceiveRemoteNotification (IUIApplicationDelegate This, UIApplication application, Foundation.NSDictionary userInfo, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidRegisterUserNotificationSettings (IUIApplicationDelegate This, UIApplication application, UIUserNotificationSettings notificationSettings);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUIApplicationDelegate This, UIApplication application, UIWindow forWindow);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, UILocalNotification localNotification, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, Foundation.NSDictionary remoteNotificationInfo, Foundation.NSDictionary responseInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, UILocalNotification localNotification, Foundation.NSDictionary responseInfo, System.Action completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool HandleOpenURL (IUIApplicationDelegate This, UIApplication application, Foundation.NSUrl url);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool OpenUrl (IUIApplicationDelegate This, UIApplication application, Foundation.NSUrl url, string sourceApplication, Foundation.NSObject annotation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void PerformActionForShortcutItem (IUIApplicationDelegate This, UIApplication application, UIApplicationShortcutItem shortcutItem, UIOperationHandler completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void PerformFetch (IUIApplicationDelegate This, UIApplication application, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void ReceivedLocalNotification (IUIApplicationDelegate This, UIApplication application, UILocalNotification notification);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillChangeStatusBarFrame (IUIApplicationDelegate This, UIApplication application, CoreGraphics.CGRect newStatusBarFrame);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillChangeStatusBarOrientation (IUIApplicationDelegate This, UIApplication application, UIInterfaceOrientation newStatusBarOrientation, double duration);</span>
</pre>

</div> <!-- end type UIApplicationDelegate_Extensions -->
<!-- start type UIApplicationLaunchEventArgs --> <div>
<h3>Type Changed: UIKit.UIApplicationLaunchEventArgs</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public Foundation.NSDictionary RemoteNotifications { get; }</span>
</pre>

</div> <!-- end type UIApplicationLaunchEventArgs -->
<!-- start type UIBarButtonItem --> <div>
<h3>Type Changed: UIKit.UIBarButtonItem</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIImage GetBackButtonBackgroundImage (UIControlState forState, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual nfloat GetBackButtonBackgroundVerticalPositionAdjustment (UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIOffset GetBackButtonTitlePositionAdjustment (UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonBackgroundImage (UIImage backgroundImage, UIControlState forState, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonBackgroundVerticalPositionAdjustment (nfloat adjustment, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);</span>
</pre>
<!-- start type UIBarButtonItem.UIBarButtonItemAppearance --> <div>
<h3>Type Changed: UIKit.UIBarButtonItem.UIBarButtonItemAppearance</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIImage GetBackButtonBackgroundImage (UIControlState forState, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual nfloat GetBackButtonBackgroundVerticalPositionAdjustment (UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIOffset GetBackButtonTitlePositionAdjustment (UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonBackgroundImage (UIImage backgroundImage, UIControlState forState, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonBackgroundVerticalPositionAdjustment (nfloat adjustment, UIBarMetrics barMetrics);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetBackButtonTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);</span>
</pre>

</div> <!-- end type UIBarButtonItem.UIBarButtonItemAppearance -->

</div> <!-- end type UIBarButtonItem -->
<!-- start type UIBarItem --> <div>
<h3>Type Changed: UIKit.UIBarItem</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage LandscapeImagePhone { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIEdgeInsets LandscapeImagePhoneInsets { get; set; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHeaderElements { get; set; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public UITextAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetTitleTextAttributes (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>
<!-- start type UIBarItem.UIBarItemAppearance --> <div>
<h3>Type Changed: UIKit.UIBarItem.UIBarItemAppearance</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITextAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIStringAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTitleTextAttributes (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>

</div> <!-- end type UIBarItem.UIBarItemAppearance -->

</div> <!-- end type UIBarItem -->
<!-- start type UIButton --> <div>
<h3>Type Changed: UIKit.UIButton</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIFont Font { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UILineBreakMode LineBreakMode { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsTouchWhenHighlighted { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGSize TitleShadowOffset { get; set; }</span>
</pre>

</div> <!-- end type UIButton -->
<!-- start type UICollectionViewController --> <div>
<h3>Type Changed: UIKit.UICollectionViewController</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidZoom (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrollAnimationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Scrolled (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrolledToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldScrollToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillEndDragging (UIScrollView scrollView, CoreGraphics.CGPoint velocity, ref CoreGraphics.CGPoint targetContentOffset);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, nfloat atScale);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);</span>
</pre>

</div> <!-- end type UICollectionViewController -->
<!-- start type UICollectionViewDelegate --> <div>
<h3>Type Changed: UIKit.UICollectionViewDelegate</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>UIKit.UIScrollViewDelegate</span>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidZoom (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrollAnimationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Scrolled (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrolledToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldScrollToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillEndDragging (UIScrollView scrollView, CoreGraphics.CGPoint velocity, ref CoreGraphics.CGPoint targetContentOffset);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, nfloat atScale);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);</span>
</pre>

</div> <!-- end type UICollectionViewDelegate -->
<!-- start type UICollectionViewSource --> <div>
<h3>Type Changed: UIKit.UICollectionViewSource</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DecelerationStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidZoom (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingEnded (UIScrollView scrollView, bool willDecelerate);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DraggingStarted (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrollAnimationEnded (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Scrolled (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ScrolledToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldScrollToTop (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIView ViewForZoomingInScrollView (UIScrollView scrollView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillEndDragging (UIScrollView scrollView, CoreGraphics.CGPoint velocity, ref CoreGraphics.CGPoint targetContentOffset);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingEnded (UIScrollView scrollView, UIView withView, nfloat atScale);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ZoomingStarted (UIScrollView scrollView, UIView view);</span>
</pre>

</div> <!-- end type UICollectionViewSource -->
<!-- start type UICollectionViewTransitionLayout --> <div>
<h3>Type Changed: UIKit.UICollectionViewTransitionLayout</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public UICollectionViewTransitionLayout ();</span>
</pre>

</div> <!-- end type UICollectionViewTransitionLayout -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor DarkTextColor { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor GroupTableViewBackgroundColor { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor LightTextColor { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor ScrollViewTexturedBackgroundColor { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor UnderPageBackgroundColor { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static UIColor ViewFlipsideBackgroundColor { get; }</span>
</pre>

</div> <!-- end type UIColor -->
<!-- start type UIDevice --> <div>
<h3>Type Changed: UIKit.UIDevice</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual float BatteryLevel { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString BatteryLevelDidChangeNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool BatteryMonitoringEnabled { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIDeviceBatteryState BatteryState { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString BatteryStateDidChangeNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool GeneratesDeviceOrientationNotifications { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIDeviceOrientation Orientation { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString OrientationDidChangeNotification { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void BeginGeneratingDeviceOrientationNotifications ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void EndGeneratingDeviceOrientationNotifications ();</span>
</pre>
<!-- start type UIDevice.Notifications --> <div>
<h3>Type Changed: UIKit.UIDevice.Notifications</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveBatteryLevelDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveBatteryStateDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static Foundation.NSObject ObserveOrientationDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>

</div> <!-- end type UIDevice.Notifications -->

</div> <!-- end type UIDevice -->
<!-- start type UIFont --> <div>
<h3>Type Changed: UIKit.UIFont</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static nfloat ButtonFontSize { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static nfloat LabelFontSize { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static nfloat SmallSystemFontSize { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static nfloat SystemFontSize { get; }</span>
</pre>

</div> <!-- end type UIFont -->
<!-- start type UIImage --> <div>
<h3>Type Changed: UIKit.UIImage</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nint LeftCapWidth { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nint TopCapHeight { get; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHeaderElements { get; set; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public void SaveToPhotosAlbum (UIImage.SaveStatus status);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIImage StretchableImage (nint leftCapWidth, nint topCapHeight);</span>
</pre>
<h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImage.SaveStatus</span></h3>
</div> <!-- end type UIImage -->
<!-- start type UIImageView --> <div>
<h3>Type Changed: UIKit.UIImageView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsImageWhenAncestorFocused { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide FocusedFrameGuide { get; }</span>
</pre>
</div>

</div> <!-- end type UIImageView -->
<!-- start type UIInputViewController --> <div>
<h3>Type Changed: UIKit.UIInputViewController</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void RequestSupplementaryLexicon (System.Action&lt;UILexicon&gt; completionHandler);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual System.Threading.Tasks.Task&lt;UILexicon&gt; RequestSupplementaryLexiconAsync ();</span>
</pre>

</div> <!-- end type UIInputViewController -->
<!-- start type UIKeyboard --> <div>
<h3>Type Changed: UIKit.UIKeyboard</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIKeyboard ();</span>
</pre>
</div>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString AnimationCurveUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString AnimationDurationUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString BoundsUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CenterBeginUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString CenterEndUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidChangeFrameNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidHideNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString DidShowNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FrameBeginUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString FrameEndUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString IsLocalUserInfoKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString WillChangeFrameNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString WillHideNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString WillShowNotification { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static uint AnimationCurveFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static double AnimationDurationFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static CoreGraphics.CGRect BoundsFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static CoreGraphics.CGPoint CenterBeginFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static CoreGraphics.CGPoint CenterEndFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static CoreGraphics.CGRect FrameBeginFromNotification (Foundation.NSNotification n);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static CoreGraphics.CGRect FrameEndFromNotification (Foundation.NSNotification n);</span>
</pre>
<h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIKeyboard.Notifications</span></h3>
</div> <!-- end type UIKeyboard -->
<!-- start type UILabel --> <div>
<h3>Type Changed: UIKit.UILabel</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool AdjustsLetterSpacingToFitWidth { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nfloat MinimumFontSize { get; set; }</span>
</pre>

</div> <!-- end type UILabel -->
<!-- start type UILongPressGestureRecognizer --> <div>
<h3>Type Changed: UIKit.UILongPressGestureRecognizer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint NumberOfTouchesRequired { get; set; }</span>
</pre>

</div> <!-- end type UILongPressGestureRecognizer -->
<!-- start type UINavigationBar --> <div>
<h3>Type Changed: UIKit.UINavigationBar</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage BackIndicatorImage { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage BackIndicatorTransitionMaskImage { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIBarStyle BarStyle { get; set; }</span>
</pre>
<!-- start type UINavigationBar.UINavigationBarAppearance --> <div>
<h3>Type Changed: UIKit.UINavigationBar.UINavigationBarAppearance</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage BackIndicatorImage { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage BackIndicatorTransitionMaskImage { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITextAttributes GetTitleTextAttributes ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetTitleTextAttributes (UITextAttributes attributes);</span>
</pre>

</div> <!-- end type UINavigationBar.UINavigationBarAppearance -->

</div> <!-- end type UINavigationBar -->
<!-- start type UINavigationController --> <div>
<h3>Type Changed: UIKit.UINavigationController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIPanGestureRecognizer BarHideOnSwipeGestureRecognizer { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITapGestureRecognizer BarHideOnTapGestureRecognizer { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBarsOnSwipe { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBarsOnTap { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBarsWhenKeyboardAppears { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBarsWhenVerticallyCompact { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIGestureRecognizer InteractivePopGestureRecognizer { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIToolbar Toolbar { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ToolbarHidden { get; set; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetToolbarHidden (bool hidden, bool animated);</span>
</pre>

</div> <!-- end type UINavigationController -->
<!-- start type UINavigationControllerDelegate --> <div>
<h3>Type Changed: UIKit.UINavigationControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);</span>
</pre>

</div> <!-- end type UINavigationControllerDelegate -->
<!-- start type UINavigationControllerDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UINavigationControllerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientation GetPreferredInterfaceOrientation (IUINavigationControllerDelegate This, UINavigationController navigationController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUINavigationControllerDelegate This, UINavigationController navigationController);</span>
</pre>

</div> <!-- end type UINavigationControllerDelegate_Extensions -->
<!-- start type UINavigationItem --> <div>
<h3>Type Changed: UIKit.UINavigationItem</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIBarButtonItem BackBarButtonItem { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBackButton { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool LeftItemsSupplementBackButton { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual string Prompt { get; set; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetHidesBackButton (bool hides, bool animated);</span>
</pre>

</div> <!-- end type UINavigationItem -->
<!-- start type UIPageViewController --> <div>
<h3>Type Changed: UIKit.UIPageViewController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UIPageViewController,UIKit.UIInterfaceOrientation&gt; GetPreferredInterfaceOrientationForPresentation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public UIPageViewSpineLocationCallback GetSpineLocation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UIPageViewController,UIKit.UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations { get; set; }</span>
</pre>

</div> <!-- end type UIPageViewController -->
<!-- start type UIPageViewControllerDelegate --> <div>
<h3>Type Changed: UIKit.UIPageViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (UIPageViewController pageViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIPageViewControllerSpineLocation GetSpineLocation (UIPageViewController pageViewController, UIInterfaceOrientation orientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UIPageViewController pageViewController);</span>
</pre>

</div> <!-- end type UIPageViewControllerDelegate -->
<!-- start type UIPageViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIPageViewControllerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIPageViewControllerSpineLocation GetSpineLocation (IUIPageViewControllerDelegate This, UIPageViewController pageViewController, UIInterfaceOrientation orientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);</span>
</pre>

</div> <!-- end type UIPageViewControllerDelegate_Extensions -->
<!-- start type UIPanGestureRecognizer --> <div>
<h3>Type Changed: UIKit.UIPanGestureRecognizer</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint MaximumNumberOfTouches { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint MinimumNumberOfTouches { get; set; }</span>
</pre>

</div> <!-- end type UIPanGestureRecognizer -->
<!-- start type UIResponder --> <div>
<h3>Type Changed: UIKit.UIResponder</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITextInputAssistantItem InputAssistantItem { get; }</span>
</pre>

</div> <!-- end type UIResponder -->
<!-- start type UIScreen --> <div>
<h3>Type Changed: UIKit.UIScreen</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGRect ApplicationFrame { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIScreenMode[] AvailableModes { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nfloat Brightness { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIScreenMode PreferredMode { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool WantsSoftwareDimming { get; set; }</span>
</pre>
<p>Modified properties:</p>
<pre>
<div data-is-breaking="">	public virtual UIScreenMode CurrentMode { get; <span class='removed removed-inline removed-breaking-inline'>set;</span> }
</div></pre>

</div> <!-- end type UIScreen -->
<!-- start type UIScrollView --> <div>
<h3>Type Changed: UIKit.UIScrollView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool PagingEnabled { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIPinchGestureRecognizer PinchGestureRecognizer { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ScrollsToTop { get; set; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIGestureRecognizer DirectionalPressGestureRecognizer { get; }</span>
</pre>
</div>

</div> <!-- end type UIScrollView -->
<!-- start type UISearchBar --> <div>
<h3>Type Changed: UIKit.UISearchBar</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public UISearchBar ();</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public UISearchBar (CoreGraphics.CGRect frame);</span>
</pre>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIBarStyle BarStyle { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITextInputAssistantItem InputAssistantItem { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool SearchResultsButtonSelected { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsBookmarkButton { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsCancelButton { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShowsSearchResultsButton { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler BookmarkButtonClicked;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler CancelButtonClicked;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler ListButtonClicked;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public UITextAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void SetScopeBarButtonTitle (UITextAttributes attributes, UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetShowsCancelButton (bool showsCancelButton, bool animated);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopeBarButtonTitle (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>
<!-- start type UISearchBar.UISearchBarAppearance --> <div>
<h3>Type Changed: UIKit.UISearchBar.UISearchBarAppearance</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public UITextAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void SetScopeBarButtonTitle (UITextAttributes attributes, UIControlState state);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopeBarButtonTitle (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>

</div> <!-- end type UISearchBar.UISearchBarAppearance -->

</div> <!-- end type UISearchBar -->
<!-- start type UISearchBarDelegate --> <div>
<h3>Type Changed: UIKit.UISearchBarDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void BookmarkButtonClicked (UISearchBar searchBar);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void CancelButtonClicked (UISearchBar searchBar);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ListButtonClicked (UISearchBar searchBar);</span>
</pre>

</div> <!-- end type UISearchBarDelegate -->
<!-- start type UISearchBarDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UISearchBarDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void BookmarkButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void CancelButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void ListButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);</span>
</pre>

</div> <!-- end type UISearchBarDelegate_Extensions -->
<!-- start type UISearchController --> <div>
<h3>Type Changed: UIKit.UISearchController</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool DimsBackgroundDuringPresentation { get; set; }</span>
</pre>

</div> <!-- end type UISearchController -->
<!-- start type UISegmentedControl --> <div>
<h3>Type Changed: UIKit.UISegmentedControl</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UISegmentedControlStyle ControlStyle { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public UITextAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetTitleTextAttributes (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>
<!-- start type UISegmentedControl.UISegmentedControlAppearance --> <div>
<h3>Type Changed: UIKit.UISegmentedControl.UISegmentedControlAppearance</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public UITextAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetTitleTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetTitleTextAttributes (UIStringAttributes attributes, UIControlState state);</span>
</pre>
</div>

</div> <!-- end type UISegmentedControl.UISegmentedControlAppearance -->

</div> <!-- end type UISegmentedControl -->
<!-- start type UISplitViewController --> <div>
<h3>Type Changed: UIKit.UISplitViewController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UISplitViewController,UIKit.UIInterfaceOrientation&gt; GetPreferredInterfaceOrientationForPresentation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public UISplitViewControllerHidePredicate ShouldHideViewController { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UISplitViewController,UIKit.UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UISplitViewHideEventArgs&gt; WillHideViewController;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UISplitViewPresentEventArgs&gt; WillPresentViewController;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UISplitViewShowEventArgs&gt; WillShowViewController;</span>
</pre>

</div> <!-- end type UISplitViewController -->
<!-- start type UISplitViewControllerDelegate --> <div>
<h3>Type Changed: UIKit.UISplitViewControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (UISplitViewController splitViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldHideViewController (UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UISplitViewController splitViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillHideViewController (UISplitViewController svc, UIViewController aViewController, UIBarButtonItem barButtonItem, UIPopoverController pc);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillPresentViewController (UISplitViewController svc, UIPopoverController pc, UIViewController aViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillShowViewController (UISplitViewController svc, UIViewController aViewController, UIBarButtonItem button);</span>
</pre>

</div> <!-- end type UISplitViewControllerDelegate -->
<!-- start type UISplitViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UISplitViewControllerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static bool ShouldHideViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillHideViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController aViewController, UIBarButtonItem barButtonItem, UIPopoverController pc);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillPresentViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIPopoverController pc, UIViewController aViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillShowViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController aViewController, UIBarButtonItem button);</span>
</pre>

</div> <!-- end type UISplitViewControllerDelegate_Extensions -->
<!-- start type UIStoryboardPopoverSegue --> <div>
<h3>Type Changed: UIKit.UIStoryboardPopoverSegue</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public UIStoryboardPopoverSegue ();</span>
</pre>

</div> <!-- end type UIStoryboardPopoverSegue -->
<!-- start type UIStoryboardSegue --> <div>
<h3>Type Changed: UIKit.UIStoryboardSegue</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">[Obsolete ("iOS9 does not allow creating an empty instance")]
	public UIStoryboardSegue ();</span>
</pre>

</div> <!-- end type UIStoryboardSegue -->
<!-- start type UISwipeGestureRecognizer --> <div>
<h3>Type Changed: UIKit.UISwipeGestureRecognizer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint NumberOfTouchesRequired { get; set; }</span>
</pre>

</div> <!-- end type UISwipeGestureRecognizer -->
<!-- start type UITabBar --> <div>
<h3>Type Changed: UIKit.UITabBar</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIBarStyle BarStyle { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool IsCustomizing { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITabBarItemPositioning ItemPositioning { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIColor SelectedImageTintColor { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarItemsEventArgs&gt; DidBeginCustomizingItems;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarFinalItemsEventArgs&gt; DidEndCustomizingItems;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarItemsEventArgs&gt; WillBeginCustomizingItems;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarFinalItemsEventArgs&gt; WillEndCustomizingItems;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void BeginCustomizingItems (UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool EndCustomizing (bool animated);</span>
</pre>
<!-- start type UITabBar.UITabBarAppearance --> <div>
<h3>Type Changed: UIKit.UITabBar.UITabBarAppearance</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIColor SelectedImageTintColor { get; set; }</span>
</pre>

</div> <!-- end type UITabBar.UITabBarAppearance -->

</div> <!-- end type UITabBar -->
<!-- start type UITabBarController --> <div>
<h3>Type Changed: UIKit.UITabBarController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIViewController[] CustomizableViewControllers { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UITabBarController,UIKit.UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UINavigationController MoreNavigationController { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public System.Func&lt;UITabBarController,UIKit.UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations { get; set; }</span>
</pre>
<p>Removed events:</p>

<pre>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; FinishedCustomizingViewControllers;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarCustomizeEventArgs&gt; OnCustomizingViewControllers;</span>
	<span class='removed removed-event breaking' data-is-breaking="">public event System.EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; OnEndCustomizingViewControllers;</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
</pre>

</div> <!-- end type UITabBarController -->
<!-- start type UITabBarControllerDelegate --> <div>
<h3>Type Changed: UIKit.UITabBarControllerDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void FinishedCustomizingViewControllers (UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UITabBarController tabBarController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void OnCustomizingViewControllers (UITabBarController tabBarController, UIViewController[] viewControllers);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void OnEndCustomizingViewControllers (UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UITabBarController tabBarController);</span>
</pre>

</div> <!-- end type UITabBarControllerDelegate -->
<!-- start type UITabBarControllerDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITabBarControllerDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void FinishedCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientation GetPreferredInterfaceOrientation (IUITabBarControllerDelegate This, UITabBarController tabBarController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void OnCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void OnEndCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUITabBarControllerDelegate This, UITabBarController tabBarController);</span>
</pre>

</div> <!-- end type UITabBarControllerDelegate_Extensions -->
<!-- start type UITabBarDelegate --> <div>
<h3>Type Changed: UIKit.UITabBarDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillBeginCustomizingItems (UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillEndCustomizingItems (UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
</pre>

</div> <!-- end type UITabBarDelegate -->
<!-- start type UITabBarDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITabBarDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidBeginCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidEndCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillBeginCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillEndCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items, bool changed);</span>
</pre>

</div> <!-- end type UITabBarDelegate_Extensions -->
<!-- start type UITabBarItem --> <div>
<h3>Type Changed: UIKit.UITabBarItem</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage FinishedSelectedImage { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIImage FinishedUnselectedImage { get; }</span>
</pre>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);</span>
</pre>

</div> <!-- end type UITabBarItem -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString IndexSearch { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIColor SeparatorColor { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIVisualEffect SeparatorEffect { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITableViewCellSeparatorStyle SeparatorStyle { get; set; }</span>
</pre>
<!-- start type UITableView.UITableViewAppearance --> <div>
<h3>Type Changed: UIKit.UITableView.UITableViewAppearance</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIColor SeparatorColor { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIVisualEffect SeparatorEffect { get; set; }</span>
</pre>

</div> <!-- end type UITableView.UITableViewAppearance -->

</div> <!-- end type UITableView -->
<!-- start type UITableViewCell --> <div>
<h3>Type Changed: UIKit.UITableViewCell</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIEdgeInsets SeparatorInset { get; set; }</span>
</pre>

</div> <!-- end type UITableViewCell -->
<!-- start type UITableViewController --> <div>
<h3>Type Changed: UIKit.UITableViewController</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIRefreshControl RefreshControl { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewCellAccessory AccessoryForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidEndEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual nint SectionFor (UITableView tableView, string title, nint atIndex);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string TitleForDeleteConfirmation (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillBeginEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
</pre>

</div> <!-- end type UITableViewController -->
<!-- start type UITableViewDataSource --> <div>
<h3>Type Changed: UIKit.UITableViewDataSource</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual nint SectionFor (UITableView tableView, string title, nint atIndex);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
</pre>

</div> <!-- end type UITableViewDataSource -->
<!-- start type UITableViewDataSource_Extensions --> <div>
<h3>Type Changed: UIKit.UITableViewDataSource_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static nint SectionFor (IUITableViewDataSource This, UITableView tableView, string title, nint atIndex);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static string[] SectionIndexTitles (IUITableViewDataSource This, UITableView tableView);</span>
</pre>

</div> <!-- end type UITableViewDataSource_Extensions -->
<!-- start type UITableViewDelegate --> <div>
<h3>Type Changed: UIKit.UITableViewDelegate</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewCellAccessory AccessoryForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidEndEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string TitleForDeleteConfirmation (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillBeginEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
</pre>

</div> <!-- end type UITableViewDelegate -->
<!-- start type UITableViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITableViewDelegate_Extensions</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static UITableViewCellAccessory AccessoryForRow (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void DidEndEditing (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static UITableViewRowAction[] EditActionsForRow (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static string TitleForDeleteConfirmation (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void WillBeginEditing (IUITableViewDelegate This, UITableView tableView, Foundation.NSIndexPath indexPath);</span>
</pre>

</div> <!-- end type UITableViewDelegate_Extensions -->
<!-- start type UITableViewSource --> <div>
<h3>Type Changed: UIKit.UITableViewSource</h3>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewCellAccessory AccessoryForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidEndEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string TitleForDeleteConfirmation (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillBeginEditing (UITableView tableView, Foundation.NSIndexPath indexPath);</span>
</pre>

</div> <!-- end type UITableViewSource -->
<!-- start type UITapGestureRecognizer --> <div>
<h3>Type Changed: UIKit.UITapGestureRecognizer</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual uint NumberOfTouchesRequired { get; set; }</span>
</pre>

</div> <!-- end type UITapGestureRecognizer -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextBackgroundColorKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextColorKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextFontKey { get; }</span>
</pre>

</div> <!-- end type UITextField -->
<!-- start type UITextInputMode --> <div>
<h3>Type Changed: UIKit.UITextInputMode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static UITextInputMode CurrentInputMode { get; }</span>
</pre>

</div> <!-- end type UITextInputMode -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIDataDetectorType DataDetectorTypes { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextBackgroundColorKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextColorKey { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString TextFontKey { get; }</span>
</pre>

</div> <!-- end type UITextView -->
<!-- start type UITouch --> <div>
<h3>Type Changed: UIKit.UITouch</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual nfloat AltitudeAngle { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITouchProperties EstimatedProperties { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UITouchProperties EstimatedPropertiesExpectingUpdates { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSNumber EstimationUpdateIndex { get; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual nfloat GetAzimuthAngle (UIView view);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual CoreGraphics.CGVector GetAzimuthUnitVector (UIView view);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual CoreGraphics.CGPoint GetPreciseLocation (UIView view);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual CoreGraphics.CGPoint GetPrecisePreviousLocation (UIView view);</span>
</pre>

</div> <!-- end type UITouch -->
<!-- start type UIVibrancyEffect --> <div>
<h3>Type Changed: UIKit.UIVibrancyEffect</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static UIVibrancyEffect CreateForNotificationCenter ();</span>
</pre>

</div> <!-- end type UIVibrancyEffect -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGRect ContentStretch { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ExclusiveTouch { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool MultipleTouchEnabled { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIView ViewForBaselineLayout { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIViewPrintFormatter ViewPrintFormatter { get; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHeaderElements { get; set; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DrawRect (CoreGraphics.CGRect area, UIViewPrintFormatter formatter);</span>
</pre>

</div> <!-- end type UIView -->
<!-- start type UIViewController --> <div>
<h3>Type Changed: UIKit.UIViewController</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool AutomaticallyForwardAppearanceAndRotationMethodsToChildViewControllers { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CoreGraphics.CGSize ContentSizeForViewInPopover { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool HidesBottomBarWhenPushed { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIInterfaceOrientation InterfaceOrientation { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ModalPresentationCapturesStatusBarAppearance { get; set; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIViewController ModalViewController { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIPopoverPresentationController PopoverPresentationController { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIStatusBarAnimation PreferredStatusBarUpdateAnimation { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIView RotatingFooterView { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UIView RotatingHeaderView { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual UISearchDisplayController SearchDisplayController { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool ShouldAutomaticallyForwardRotationMethods { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual bool WantsFullScreenLayout { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static void AttemptRotationToDeviceOrientation ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIViewController ChildViewControllerForStatusBarHidden ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIViewController ChildViewControllerForStatusBarStyle ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidAnimateFirstHalfOfRotation (UIInterfaceOrientation toInterfaceOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DidRotate (UIInterfaceOrientation fromInterfaceOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DismissModalViewController (bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void DismissMoviePlayerViewController ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIInterfaceOrientation PreferredInterfaceOrientationForPresentation ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual UIStatusBarStyle PreferredStatusBarStyle ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool PrefersStatusBarHidden ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public static void PrepareForInterstitialAds ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void PresentMoviePlayerViewController (MediaPlayer.MPMoviePlayerViewController moviePlayerViewController);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetNeedsStatusBarAppearanceUpdate ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetToolbarItems (UIBarButtonItem[] items, bool animated);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldAutorotate ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ViewDidUnload ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void ViewWillUnload ();</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillAnimateFirstHalfOfRotation (UIInterfaceOrientation toInterfaceOrientation, double duration);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillAnimateRotation (UIInterfaceOrientation toInterfaceOrientation, double duration);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillAnimateSecondHalfOfRotation (UIInterfaceOrientation fromInterfaceOrientation, double duration);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void WillRotate (UIInterfaceOrientation toInterfaceOrientation, double duration);</span>
</pre>

</div> <!-- end type UIViewController -->
<!-- start type UIWindow --> <div>
<h3>Type Changed: UIKit.UIWindow</h3>
<p>Removed properties:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString KeyboardDidChangeFrameNotification { get; }</span>
	<span class='removed removed-property breaking' data-is-breaking="">public static Foundation.NSString KeyboardWillChangeFrameNotification { get; }</span>
</pre>

</div> <!-- end type UIWindow -->
<!-- start type UIWindowLevel --> <div>
<h3>Type Changed: UIKit.UIWindowLevel</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public static nfloat StatusBar { get; }</span>
</pre>

</div> <!-- end type UIWindowLevel -->
<h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIAccelerometerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIActionSheetDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIActivityItemSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIAlertViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIDocumentInteractionControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIDocumentMenuDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIDocumentPickerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIImagePickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPickerViewAccessibilityDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPickerViewDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPickerViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPickerViewModel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPopoverPresentationControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPrintInteractionControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIPrinterPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUISearchDisplayDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIToolbarDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIVideoEditorControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.IUIWebViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.NSAttributedStringAttachmentConveniences</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.NSFileProviderExtension</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAcceleration</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAccelerometer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAccelerometerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAccelerometerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAccelerometerEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActionSheet</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActionSheetDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActionSheetDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActionSheetStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityCategory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityItemProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityItemSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityItemSource_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIActivityViewControllerCompletion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAlertView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAlertViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAlertViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAlertViewPredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIAlertViewStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIApplicationShortcutIcon</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIApplicationShortcutIconType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIApplicationShortcutItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIBackgroundFetchResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIBackgroundRefreshStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIBarStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIButtonEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDataDetectorType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDatePicker</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDatePickerMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDeviceBatteryState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDeviceOrientation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDeviceOrientationExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocument</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentChangeKind</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentInteractionController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentInteractionControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentInteractionControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentInteractionProbe</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentInteractionRectangle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentMenuDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentMenuDocumentPickedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentMenuOrder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentMenuViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickerExtensionViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickerMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentPickerViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentSaveOperation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentSendingToApplicationEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIDocumentViewForPreview</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerCameraCaptureMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerCameraDevice</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerCameraFlashMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerQualityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerControllerSourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerImagePickedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIImagePickerMediaPickedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIInterfaceOrientation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIInterfaceOrientationExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIInterfaceOrientationMask</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIKeyboardEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UILexicon</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UILexiconEntry</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UILocalNotification</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UILocalizedIndexedCollation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIManagedDocument</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMarkupTextPrintFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMenuController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMenuControllerArrowDirection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMenuItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMutableApplicationShortcutItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMutableUserNotificationAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIMutableUserNotificationCategory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIOperationHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPageViewSpineLocationCallback</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPasteboard</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPasteboardChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPathEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewAccessibilityDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewAccessibilityDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPickerViewModel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPinchGestureRecognizer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPopoverPresentationController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPopoverPresentationControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPopoverPresentationControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrint</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInfoDuplex</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInfoOrientation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInfoOutputType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteraction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionPaperList</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintInteractionResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintPageRenderer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrintPaper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterContactPrinterHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterCutterBehavior</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterJobTypes</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterPickerCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterPickerController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterPickerControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIPrinterPickerControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIReferenceLibraryViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIRefreshControl</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIRemoteNotificationType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIRotationGestureRecognizer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIScreenEdgePanGestureRecognizer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISearchDisplayController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISearchDisplayDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISearchDisplayDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISegmentedControlStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISimpleTextPrintFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISlider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISplitViewControllerHidePredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISplitViewHideEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISplitViewPresentEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISplitViewShowEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStatusBarAnimation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStatusBarFrameChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStatusBarOrientationChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStatusBarStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStepper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIStringDrawing</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UISwitch</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITabBarCustomizeChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITabBarCustomizeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITabBarFinalItemsEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITabBarItemsEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITableViewCellSeparatorStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITableViewRowAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITableViewRowActionStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITextAttributes</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UITextInputAssistantItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIToolbar</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIToolbarDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIToolbarPosition</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationActionBehavior</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationActionContext</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationActivationMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationCategory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIUserNotificationType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIVideo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIVideoEditorController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIVideoEditorControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIVideoEditorControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIViewPrintFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebErrorArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebLoaderControl</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebPaginationBreakingMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebPaginationMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">UIKit.UIWebViewNavigationType</span></h3>
</div> <!-- end namespace UIKit -->
<!-- start namespace Accounts --> <div>
<h2>Removed Namespace Accounts</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccount</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccountCredential</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccountCredentialRenewResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccountStore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccountStoreSaveCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACAccountType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACFacebookAudience</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACFacebookAudienceValue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACFacebookKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACRequestCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.ACTencentWeiboKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Accounts.AccountStoreOptions</span></h3></div> <!-- end namespace Accounts -->

<!-- start namespace AddressBook --> <div>
<h2>Removed Namespace AddressBook</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABAddressBook</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABAddressBookError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABAddressBookErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMultiValueEntry`1</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMultiValue`1</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMutableDateMultiValue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMutableDictionaryMultiValue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMutableMultiValue`1</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABMutableStringMultiValue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPerson</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonAddressKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonCompositeNameFormat</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonDateLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonImageFormat</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonInstantMessageKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonInstantMessageService</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonKind</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonPhoneLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonProperty</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonRelatedNamesLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonSocialProfileService</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonSortBy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPersonUrlLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABPropertyType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABRecord</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABRecordType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABSourceProperty</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ABSourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.ExternalChangeEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.InstantMessageService</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.PersonAddress</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBook.SocialProfile</span></h3></div> <!-- end namespace AddressBook -->

<!-- start namespace AddressBookUI --> <div>
<h2>Removed Namespace AddressBookUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABAddressFormatting</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABNewPersonCompleteEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABNewPersonViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABNewPersonViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerNavigationController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerNavigationControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerPerformAction2EventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerPerformActionEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerSelectPerson2EventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPeoplePickerSelectPersonEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPersonPredicateKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPersonViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPersonViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABPersonViewPerformDefaultActionEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABUnknownPersonCreatedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABUnknownPersonViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABUnknownPersonViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.ABUnknownPersonViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.DisplayedPropertiesCollection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.IABNewPersonViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.IABPeoplePickerNavigationControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.IABPersonViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AddressBookUI.IABUnknownPersonViewControllerDelegate</span></h3></div> <!-- end namespace AddressBookUI -->

<!-- start namespace AssetsLibrary --> <div>
<h2>Removed Namespace AssetsLibrary</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAsset</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetLibraryChangedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetOrientation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetRepresentation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsEnumerator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsFilter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsGroupType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsLibrary</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAssetsLibraryGroupsEnumerationResultsDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">AssetsLibrary.ALAuthorizationStatus</span></h3></div> <!-- end namespace AssetsLibrary -->

<!-- start namespace Contacts --> <div>
<h2>Removed Namespace Contacts</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContact</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactDisplayNameOrder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactFetchRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactFormatterStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactProperty</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactRelation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactSortOrder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactStore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactStoreEnumerateContactsHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactStoreRequestAccessHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactVCardSerialization</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContactsUserDefaults</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContainer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContainerKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContainerType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNContainer_PredicatesExtension</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNEntityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNErrorUserInfoKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNGroupKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNGroup_PredicatesExtension</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNInstantMessageAddress</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNInstantMessageAddressKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNInstantMessageAddressOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNInstantMessageServiceKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNInstantMessageServiceOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNLabelContactRelationKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNLabelKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNLabelPhoneNumberKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNLabeledValue`1</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNMutableContact</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNMutableGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNMutablePostalAddress</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPhoneNumber</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPostalAddress</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPostalAddressFormatter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPostalAddressFormatterStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPostalAddressKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNPostalAddressKeyOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSaveRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSocialProfile</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSocialProfileKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSocialProfileOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSocialProfileServiceKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.CNSocialProfileServiceOption</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Contacts.ICNKeyDescriptor</span></h3></div> <!-- end namespace Contacts -->

<!-- start namespace ContactsUI --> <div>
<h2>Removed Namespace ContactsUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactPickerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactPickerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactPickerViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.CNContactViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.ICNContactPickerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ContactsUI.ICNContactViewControllerDelegate</span></h3></div> <!-- end namespace ContactsUI -->

<!-- start namespace CoreAudioKit --> <div>
<h2>Removed Namespace CoreAudioKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">CoreAudioKit.AUViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreAudioKit.CABTMidiCentralViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreAudioKit.CABTMidiLocalPeripheralViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreAudioKit.CAInterAppAudioSwitcherView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreAudioKit.CAInterAppAudioTransportView</span></h3></div> <!-- end namespace CoreAudioKit -->

<!-- start namespace CoreMidi --> <div>
<h2>Removed Namespace CoreMidi</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.IOErrorEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.Midi</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiClient</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiDevice</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiEndpoint</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiEntity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiException</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiNetworkConnection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiNetworkConnectionPolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiNetworkHost</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiNetworkSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiPacket</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiPacketsEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.MidiPort</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.ObjectAddedOrRemovedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMidi.ObjectPropertyChangedEventArgs</span></h3></div> <!-- end namespace CoreMidi -->

<!-- start namespace CoreMotion --> <div>
<h2>Removed Namespace CoreMotion</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAcceleration</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAccelerometerData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAccelerometerHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAltimeter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAltitudeData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAttitude</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMAttitudeReferenceFrame</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMCalibratedMagneticField</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMDeviceMotion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMDeviceMotionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMGyroData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMGyroHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMLogItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMagneticField</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMagneticFieldCalibrationAccuracy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMagnetometerData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMagnetometerHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionActivity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionActivityConfidence</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionActivityHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionActivityManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionActivityQueryHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMMotionManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMPedometer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMPedometerData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMQuaternion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMRecordedAccelerometerData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMRotationMatrix</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMRotationRate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMSensorDataList</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMSensorRecorder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMStepCounter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMStepQueryHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreMotion.CMStepUpdateHandler</span></h3></div> <!-- end namespace CoreMotion -->

<!-- start namespace CoreTelephony --> <div>
<h2>Removed Namespace CoreTelephony</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTCall</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTCallCenter</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTCarrier</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTCellularData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTCellularDataRestrictedState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTErrorDomain</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTRadioAccessTechnology</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTSubscriber</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTSubscriberInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">CoreTelephony.CTTelephonyNetworkInfo</span></h3></div> <!-- end namespace CoreTelephony -->

<!-- start namespace EventKit --> <div>
<h2>Removed Namespace EventKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKAlarm</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKAlarmProximity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKCalendar</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKCalendarEventAvailability</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKCalendarItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKCalendarType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKDay</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEntityMask</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEntityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEventAvailability</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEventSearchCallback</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEventStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKEventStore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKParticipant</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKParticipantRole</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKParticipantScheduleStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKParticipantStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKParticipantType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKRecurrenceDayOfWeek</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKRecurrenceEnd</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKRecurrenceFrequency</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKRecurrenceRule</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKReminder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKReminderPriority</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKSourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKSpan</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKStructuredLocation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKit.EKWeekday</span></h3></div> <!-- end namespace EventKit -->

<!-- start namespace EventKitUI --> <div>
<h2>Removed Namespace EventKitUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKCalendarChooser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKCalendarChooserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKCalendarChooserDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKCalendarChooserDisplayStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKCalendarChooserSelectionStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditViewAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventEditViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventViewAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.EKEventViewEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.IEKCalendarChooserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.IEKEventEditViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">EventKitUI.IEKEventViewDelegate</span></h3></div> <!-- end namespace EventKitUI -->

<!-- start namespace ExternalAccessory --> <div>
<h2>Removed Namespace ExternalAccessory</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAAccessory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAAccessoryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAAccessoryDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAAccessoryEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAAccessoryManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EABluetoothAccessoryPickerError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EABluetoothAccessoryPickerErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EASession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryConfigurationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryDidFinishEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.EAWiFiUnconfiguredAccessoryProperties</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.IEAAccessoryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ExternalAccessory.IEAWiFiUnconfiguredAccessoryBrowserDelegate</span></h3></div> <!-- end namespace ExternalAccessory -->

<!-- start namespace HealthKit --> <div>
<h2>Removed Namespace HealthKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKActivitySummary</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKActivitySummaryQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKActivitySummaryType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKAnchoredObjectQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKAnchoredObjectResultHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKAnchoredObjectResultHandler2</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKAnchoredObjectUpdateHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKBiologicalSex</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKBiologicalSexObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKBloodType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKBloodTypeObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKBodyTemperatureSensorLocation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategorySample</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryTypeIdentifier</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryTypeIdentifierKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValueAppleStandHour</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValueCervicalMucusQuality</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValueMenstrualFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValueOvulationTestResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCategoryValueSleepAnalysis</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCharacteristicType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCharacteristicTypeIdentifier</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCharacteristicTypeIdentifierKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCorrelation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCorrelationQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCorrelationQueryResultHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCorrelationType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKCorrelationTypeKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKDeletedObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKDevice</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKDevicePropertyKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKFitzpatrickSkinType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKFitzpatrickSkinTypeObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKHealthStore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKHeartRateSensorLocation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKMetadata</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKMetadataKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKMetricPrefix</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKObjectType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKObserverQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKObserverQueryUpdateHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKPredicateKeyPath</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantityAggregationStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantitySample</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantityTypeIdentifier</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuantityTypeIdentifierKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQueryAnchor</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKQueryOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSample</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSampleQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSampleQueryResultsHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSampleType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSourceQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSourceQueryCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKSourceRevision</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatistics</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsCollection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsCollectionEnumerator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsCollectionQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsCollectionQueryInitialResultsHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsCollectionQueryStatisticsUpdateHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsQuery</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStatisticsQueryHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKStoreSampleAddedCallback</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKUnit</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKUpdateFrequency</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKWorkout</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKWorkoutActivityType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKWorkoutEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKWorkoutEventType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HealthKit.HKWorkoutType</span></h3></div> <!-- end namespace HealthKit -->

<!-- start namespace HealthKitUI --> <div>
<h2>Removed Namespace HealthKitUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">HealthKitUI.HKActivityRingView</span></h3></div> <!-- end namespace HealthKitUI -->

<!-- start namespace HomeKit --> <div>
<h2>Removed Namespace HomeKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryBrowser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryBrowserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryBrowserDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryBrowserEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryCategory</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryCategoryType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryServiceUpdateCharacteristicEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAccessoryUpdateEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMActionSet</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMActionSetType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristic</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicMetadata</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicMetadataFormat</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicMetadataUnits</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicProperties</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueAirParticulate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueAirQuality</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueCurrentSecuritySystemState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueDoorState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueHeatingCooling</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueLockMechanism</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueLockMechanismState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValuePositionState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueRotationDirection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueTargetSecuritySystemState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicValueTemperatureUnit</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMCharacteristicWriteAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMErrors</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMEventTrigger</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHome</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeAccessControl</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeAccessoryEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeActionSetEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeErrorAccessoryEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeManagerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeManagerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeManagerEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeRoomAccessoryEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeRoomEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeRoomZoneEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeServiceGroupEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeServiceServiceGroupEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeTriggerEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeUserEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMHomeZoneEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMLocationEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMRoom</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMService</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMServiceGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMServiceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMSignificantEvent</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMTimerTrigger</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMTrigger</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMUser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.HMZone</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.IHMAccessoryBrowserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.IHMAccessoryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.IHMHomeDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">HomeKit.IHMHomeManagerDelegate</span></h3></div> <!-- end namespace HomeKit -->

<!-- start namespace LocalAuthentication --> <div>
<h2>Removed Namespace LocalAuthentication</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LAAccessControlOperation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LAContext</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LAContextReplyHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LACredentialType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LAPolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">LocalAuthentication.LAStatus</span></h3></div> <!-- end namespace LocalAuthentication -->

<!-- start namespace MessageUI --> <div>
<h2>Removed Namespace MessageUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.IMFMailComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.IMFMessageComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFComposeResultEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMailComposeViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMessageAvailabilityChangedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMessageComposeResultEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMessageComposeViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MFMessageComposeViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MessageUI.MessageComposeResult</span></h3></div> <!-- end namespace MessageUI -->

<!-- start namespace MultipeerConnectivity --> <div>
<h2>Removed Namespace MultipeerConnectivity</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.IMCAdvertiserAssistantDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.IMCBrowserViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.IMCNearbyServiceAdvertiserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.IMCNearbyServiceBrowserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.IMCSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCAdvertiserAssistant</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCAdvertiserAssistantDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCAdvertiserAssistantDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCBrowserViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCBrowserViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCBrowserViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCEncryptionPreference</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceAdvertiser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceAdvertiserInvitationHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceBrowser</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceBrowserDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCNearbyServiceBrowserDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCPeerID</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSessionDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSessionNearbyConnectionDataForPeerCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSessionSendDataMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">MultipeerConnectivity.MCSessionState</span></h3></div> <!-- end namespace MultipeerConnectivity -->

<!-- start namespace NetworkExtension --> <div>
<h2>Removed Namespace NetworkExtension</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.INWTcpConnectionAuthenticationDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyFlowError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyProviderManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyTcpFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppProxyUdpFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEAppRule</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEDatagramRead</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEDatagramReadResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEDnsSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEEvaluateConnectionRule</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEEvaluateConnectionRuleAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterBrowserFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterControlProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterControlVerdict</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterDataProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterDataVerdict</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterManagerError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterNewFlowVerdict</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterProviderConfiguration</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterRemediationVerdict</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterSocketFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFilterVerdict</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEFlowMetaData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperCommand</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperCommandType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperConfidence</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperOptionInternal</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperResponse</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotHelperResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEHotspotNetwork</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEIPv4Route</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEIPv4Settings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEIPv6Route</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEIPv6Settings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRule</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleConnect</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleDisconnect</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleEvaluateConnection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleIgnore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEOnDemandRuleInterfaceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEPacketTunnelFlow</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEPacketTunnelNetworkSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEPacketTunnelProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEProviderStopReason</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEProxyServer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEProxySettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelNetworkSettings</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProvider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProviderError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProviderManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProviderProtocol</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProviderRoutingMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NETunnelProviderSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnConnection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnConnectionStartOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2CertificateType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2DeadPeerDetectionRate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2DiffieHellman</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2EncryptionAlgorithm</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2IntegrityAlgorithm</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIke2SecurityAssociationParameters</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnIkeAuthenticationMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnProtocol</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnProtocolIke2</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnProtocolIpSec</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NEVpnStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NSMutableURLRequest_NEHotspotHelper</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWBonjourServiceEndpoint</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWEndpoint</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWHostEndpoint</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWPath</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWPathStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWTcpConnection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWTcpConnectionAuthenticationDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWTcpConnectionAuthenticationDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWTcpConnectionState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWTlsParameters</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWUdpSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NetworkExtension.NWUdpSessionState</span></h3></div> <!-- end namespace NetworkExtension -->

<!-- start namespace NewsstandKit --> <div>
<h2>Removed Namespace NewsstandKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">NewsstandKit.NKAssetDownload</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NewsstandKit.NKIssue</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NewsstandKit.NKIssueContentStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NewsstandKit.NKLibrary</span></h3></div> <!-- end namespace NewsstandKit -->

<!-- start namespace NotificationCenter --> <div>
<h2>Removed Namespace NotificationCenter</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.INCWidgetProviding</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.NCUpdateResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.NCWidgetController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.NCWidgetProviding</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.NCWidgetProviding_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">NotificationCenter.UIVibrancyEffect_NotificationCenter</span></h3></div> <!-- end namespace NotificationCenter -->

<!-- start namespace PassKit --> <div>
<h2>Removed Namespace PassKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.IPKAddPassesViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.IPKAddPaymentPassViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.IPKPaymentAuthorizationViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPassButton</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPassButtonStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPassesViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPassesViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPassesViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPaymentPassError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPaymentPassRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPaymentPassRequestConfiguration</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPaymentPassViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddPaymentPassViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAddressField</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKAutomaticPassPresentationSuppressionResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKContact</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKEncryptionScheme</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKMerchantCapability</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPass</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPassKitErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPassLibrary</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPassLibraryAddPassesStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPassLibraryUserInfoKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPassType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPayment</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentAuthorizationEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentAuthorizationViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentAuthorizationViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentAuthorizationViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentButton</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentButtonStyle</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentButtonType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentMethodSelectedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentMethodType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentNetwork</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentPass</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentPassActivationState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentSelectedContactEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentShippingAddressSelected</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentShippingAddressSelectedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentShippingMethodSelected</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentShippingMethodSelectedEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentSummaryItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentSummaryItemType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKPaymentToken</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKShippingMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PassKit.PKShippingType</span></h3></div> <!-- end namespace PassKit -->

<!-- start namespace Photos --> <div>
<h2>Removed Namespace Photos</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Photos.IPHPhotoLibraryChangeObserver</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAdjustmentData</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAsset</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetBurstSelectionType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetChangeRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetCollection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetCollectionChangeRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetCollectionSubtype</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetCollectionType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetContentEditingInputExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetCreationRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetEditOperation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetImageProgressHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetMediaSubtype</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetMediaType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetResource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetResourceCreationOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetResourceManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetResourceRequestOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetResourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetSourceType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAssetVideoProgressHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHAuthorizationStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCachingImageManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHChange</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHChangeDetailEnumerator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollection</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollectionEditOperation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollectionList</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollectionListChangeRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollectionListSubtype</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHCollectionListType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHContentEditingHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHContentEditingInput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHContentEditingInputRequestOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHContentEditingOutput</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHFetchOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHFetchResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHFetchResultChangeDetails</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHFetchResultEnumerator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageContentMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageDataHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageManagerRequestAvAssetHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageManagerRequestExportHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageManagerRequestLivePhoto</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageManagerRequestPlayerHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageRequestOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageRequestOptionsDeliveryMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageRequestOptionsResizeMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageRequestOptionsVersion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHImageResultHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHLivePhoto</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHLivePhotoInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHLivePhotoRequestOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHObjectChangeDetails</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHObjectPlaceholder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHPhotoLibrary</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHPhotoLibraryChangeObserver</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHProgressHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHVideoRequestOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHVideoRequestOptionsDeliveryMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Photos.PHVideoRequestOptionsVersion</span></h3></div> <!-- end namespace Photos -->

<!-- start namespace PhotosUI --> <div>
<h2>Removed Namespace PhotosUI</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.IPHContentEditingController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.IPHLivePhotoViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHContentEditingController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHLivePhotoBadgeOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHLivePhotoView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHLivePhotoViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHLivePhotoViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PhotosUI.PHLivePhotoViewPlaybackStyle</span></h3></div> <!-- end namespace PhotosUI -->

<!-- start namespace PushKit --> <div>
<h2>Removed Namespace PushKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.IPKPushRegistryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushCredentials</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushPayload</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushRegistry</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushRegistryDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushRegistryDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">PushKit.PKPushType</span></h3></div> <!-- end namespace PushKit -->

<!-- start namespace QuickLook --> <div>
<h2>Removed Namespace QuickLook</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.IQLPreviewControllerDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.IQLPreviewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.IQLPreviewItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLFrame</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLOpenUrl</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLPreviewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLPreviewControllerDataSource</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLPreviewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLPreviewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLPreviewItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">QuickLook.QLTransition</span></h3></div> <!-- end namespace QuickLook -->

<!-- start namespace ReplayKit --> <div>
<h2>Removed Namespace ReplayKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.IRPPreviewViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.IRPScreenRecorderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPPreviewViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPPreviewViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPPreviewViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPRecordingError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPRecordingErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPScreenRecorder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPScreenRecorderDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">ReplayKit.RPScreenRecorderDelegate_Extensions</span></h3></div> <!-- end namespace ReplayKit -->

<!-- start namespace SafariServices --> <div>
<h2>Removed Namespace SafariServices</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.ISFSafariViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFContentBlockerErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFContentBlockerErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFContentBlockerManager</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFSafariViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFSafariViewControllerDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SFSafariViewControllerDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SSReadingList</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">SafariServices.SSReadingListError</span></h3></div> <!-- end namespace SafariServices -->

<!-- start namespace Social --> <div>
<h2>Removed Namespace Social</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLComposeServiceViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLComposeSheetConfigurationItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLComposeViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLComposeViewControllerResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLRequestMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLRequestResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLServiceKind</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Social.SLServiceType</span></h3></div> <!-- end namespace Social -->

<!-- start namespace Twitter --> <div>
<h2>Removed Namespace Twitter</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWRequest</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWRequestHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWRequestMethod</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWRequestResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWTweetComposeViewController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">Twitter.TWTweetComposeViewControllerResult</span></h3></div> <!-- end namespace Twitter -->

<!-- start namespace VideoToolbox --> <div>
<h2>Removed Namespace VideoToolbox</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTColorPrimaries</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTCompressionProperties</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTCompressionPropertyKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTCompressionSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTCompressionSessionOptionFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDataRateLimit</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecodeFrameFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecodeInfoFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecompressionProperties</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecompressionPropertyKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecompressionResolutionKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecompressionResolutionOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDecompressionSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDeinterlaceMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTDownsamplingMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTEncodeFrameOptionKey</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTEncodeFrameOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTEncodeInfoFlags</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTFieldCount</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTFieldDetail</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTFieldMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTFrameSilo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTH264EntropyMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTH264EntropyModeKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTMultiPassStorage</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTMultiPassStorageCreationOptionKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTMultiPassStorageCreationOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTOnlyTheseFrames</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPixelTransferProperties</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPixelTransferPropertyKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTProfileLevel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTProfileLevelKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPropertyKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPropertyOptions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPropertyReadWriteStatusKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPropertyType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTPropertyTypeKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTReadWriteStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTScalingMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTStatus</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTTransferFunction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTUtilities</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTVideoDecoderSpecification</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTVideoDecoderSpecificationKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTVideoEncoder</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTVideoEncoderSpecification</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTVideoEncoderSpecificationKeys</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">VideoToolbox.VTYCbCrMatrix</span></h3></div> <!-- end namespace VideoToolbox -->

<!-- start namespace WatchConnectivity --> <div>
<h2>Removed Namespace WatchConnectivity</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.IWCSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSession</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionActivationState</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionFile</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionFileTransfer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionReplyDataHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionReplyHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchConnectivity.WCSessionUserInfoTransfer</span></h3></div> <!-- end namespace WatchConnectivity -->

<!-- start namespace WatchKit --> <div>
<h2>Removed Namespace WatchKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.IWKImageAnimatable</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKAccessibility</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKAccessibilityImageRegion</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceButton</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceDate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceDevice</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceGroup</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceImage</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceLabel</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceMap</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceMapPinColor</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceObject</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceSeparator</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceSlider</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceSwitch</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceTable</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKInterfaceTimer</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKMenuItemIcon</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKTextInputMode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKUserNotificationInterfaceController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WatchKit.WKUserNotificationInterfaceType</span></h3></div> <!-- end namespace WatchKit -->

<!-- start namespace WebKit --> <div>
<h2>Removed Namespace WebKit</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.IWKNavigationDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.IWKScriptMessageHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.IWKUIDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKBackForwardList</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKBackForwardListItem</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKErrorCode</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKErrorCodeExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKFrameInfo</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKJavascriptEvaluationResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigation</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationActionPolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationResponse</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationResponsePolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKNavigationType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKPreferences</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKProcessPool</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKScriptMessage</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKScriptMessageHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKSecurityOrigin</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKSelectionGranularity</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKUIDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKUIDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKUserContentController</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKUserScript</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKUserScriptInjectionTime</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWebView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWebViewConfiguration</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWebsiteDataRecord</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWebsiteDataStore</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWebsiteDataType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">WebKit.WKWindowFeatures</span></h3></div> <!-- end namespace WebKit -->

<!-- start namespace iAd --> <div>
<h2>Removed Namespace iAd</h2>

<h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADAdType</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADBannerView</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADBannerViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADBannerViewDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADClient</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADClientConversionDetailsResult</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADClientError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADConversionDetails</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADError</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADErrorEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADErrorExtensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADInterstitialAd</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADInterstitialAdDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADInterstitialAdDelegate_Extensions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADInterstitialPresentationPolicy</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.ADPredicate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.AdAction</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.AdErrorEventArgs</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.AttributedToiAdCompletionHandler</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.IADBannerViewDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.IADInterstitialAdDelegate</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.IAdAdditions</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.IAdPreroll</span></h3><h3>Removed Type <span class='breaking' data-is-breaking="">iAd.iAdPreroll_AVPlayerViewController</span></h3></div> <!-- end namespace iAd -->

<!-- start namespace TVMLKit --> <div> 
<h2>New Namespace TVMLKit</h2>

<div> <!-- start type ITVApplicationControllerDelegate -->
<h3>New Type TVMLKit.ITVApplicationControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ITVApplicationControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ITVApplicationControllerDelegate -->
<div> <!-- start type ITVInterfaceCreating -->
<h3>New Type TVMLKit.ITVInterfaceCreating</h3>
<pre class='added' data-is-non-breaking="">
public interface ITVInterfaceCreating : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ITVInterfaceCreating -->
<div> <!-- start type TVApplicationController -->
<h3>New Type TVMLKit.TVApplicationController</h3>
<pre class='added' data-is-non-breaking="">
public class TVApplicationController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TVApplicationController (TVApplicationControllerContext context, UIKit.UIWindow window, ITVApplicationControllerDelegate delegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVApplicationControllerContext Context { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ITVApplicationControllerDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UINavigationController NavigationController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIWindow Window { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Evaluate (System.Action&lt;JavaScriptCore.JSContext&gt; evaluation, System.Action&lt;bool&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stop ();</span>
}
</pre>
</div> <!-- end type TVApplicationController -->
<div> <!-- start type TVApplicationControllerContext -->
<h3>New Type TVMLKit.TVApplicationControllerContext</h3>
<pre class='added' data-is-non-breaking="">
public class TVApplicationControllerContext : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVApplicationControllerContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationControllerContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationControllerContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl JavaScriptApplicationUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; LaunchOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StorageIdentifier { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type TVApplicationControllerContext -->
<div> <!-- start type TVApplicationControllerDelegate -->
<h3>New Type TVMLKit.TVApplicationControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class TVApplicationControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, ITVApplicationControllerDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVApplicationControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVApplicationControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (TVApplicationController appController, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishLaunching (TVApplicationController appController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStop (TVApplicationController appController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EvaluateAppJavaScript (TVApplicationController appController, JavaScriptCore.JSContext jsContext);</span>
}
</pre>
</div> <!-- end type TVApplicationControllerDelegate -->
<div> <!-- start type TVApplicationControllerDelegate_Extensions -->
<h3>New Type TVMLKit.TVApplicationControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class TVApplicationControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidFail (ITVApplicationControllerDelegate This, TVApplicationController appController, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinishLaunching (ITVApplicationControllerDelegate This, TVApplicationController appController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStop (ITVApplicationControllerDelegate This, TVApplicationController appController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EvaluateAppJavaScript (ITVApplicationControllerDelegate This, TVApplicationController appController, JavaScriptCore.JSContext jsContext);</span>
}
</pre>
</div> <!-- end type TVApplicationControllerDelegate_Extensions -->
<div> <!-- start type TVColor -->
<h3>New Type TVMLKit.TVColor</h3>
<pre class='added' data-is-non-breaking="">
public class TVColor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVColor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVColor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVColor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor Color { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVColorType ColorType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor[] GradientColors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] GradientPoints { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type TVColor -->
<div> <!-- start type TVColorType -->
<h3>New Type TVMLKit.TVColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVColorType {
	<span class='added added-field ' data-is-non-breaking="">LinearGradientLeftToRight = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LinearGradientTopToBottom = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Plain = 1,</span>
}
</pre>
</div> <!-- end type TVColorType -->
<div> <!-- start type TVElementAlignment -->
<h3>New Type TVMLKit.TVElementAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementAlignment {
	<span class='added added-field ' data-is-non-breaking="">Center = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type TVElementAlignment -->
<div> <!-- start type TVElementContentAlignment -->
<h3>New Type TVMLKit.TVElementContentAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementContentAlignment {
	<span class='added added-field ' data-is-non-breaking="">Bottom = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Center = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Top = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type TVElementContentAlignment -->
<div> <!-- start type TVElementEventType -->
<h3>New Type TVMLKit.TVElementEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementEventType {
	<span class='added added-field ' data-is-non-breaking="">Change = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Highlight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HoldSelect = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Play = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Select = 2,</span>
}
</pre>
</div> <!-- end type TVElementEventType -->
<div> <!-- start type TVElementFactory -->
<h3>New Type TVMLKit.TVElementFactory</h3>
<pre class='added' data-is-non-breaking="">
public class TVElementFactory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVElementFactory ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVElementFactory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVElementFactory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void RegisterViewElementClass (ObjCRuntime.Class elementClass, string elementName);</span>
}
</pre>
</div> <!-- end type TVElementFactory -->
<div> <!-- start type TVElementPosition -->
<h3>New Type TVMLKit.TVElementPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementPosition {
	<span class='added added-field ' data-is-non-breaking="">Bottom = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomLeft = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomRight = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Center = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Footer = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Header = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Top = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeft = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TopRight = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type TVElementPosition -->
<div> <!-- start type TVElementResettableProperty -->
<h3>New Type TVMLKit.TVElementResettableProperty</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementResettableProperty {
	<span class='added added-field ' data-is-non-breaking="">AutoHighlightIdentifier = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UpdateType = 0,</span>
}
</pre>
</div> <!-- end type TVElementResettableProperty -->
<div> <!-- start type TVElementUpdateType -->
<h3>New Type TVMLKit.TVElementUpdateType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVElementUpdateType {
	<span class='added added-field ' data-is-non-breaking="">Children = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Self = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtree = 1,</span>
}
</pre>
</div> <!-- end type TVElementUpdateType -->
<div> <!-- start type TVImageElement -->
<h3>New Type TVMLKit.TVImageElement</h3>
<pre class='added' data-is-non-breaking="">
public class TVImageElement : TVMLKit.TVViewElement, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVImageElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVImageElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVImageElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVImageType ImageType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSUrl&gt; SourceSet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; }</span>
}
</pre>
</div> <!-- end type TVImageElement -->
<div> <!-- start type TVImageType -->
<h3>New Type TVMLKit.TVImageType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVImageType {
	<span class='added added-field ' data-is-non-breaking="">Decoration = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fullscreen = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Hero = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 0,</span>
}
</pre>
</div> <!-- end type TVImageType -->
<div> <!-- start type TVInterfaceCreating_Extensions -->
<h3>New Type TVMLKit.TVInterfaceCreating_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class TVInterfaceCreating_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIKit.UIImage GetImageForResource (ITVInterfaceCreating This, string resourceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl GetUrlForResource (ITVInterfaceCreating This, string resourceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIKit.UIViewController GetViewControllerForElement (ITVInterfaceCreating This, TVViewElement element, UIKit.UIViewController existingViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIKit.UIView GetViewForElement (ITVInterfaceCreating This, TVViewElement element, UIKit.UIView existingView);</span>
}
</pre>
</div> <!-- end type TVInterfaceCreating_Extensions -->
<div> <!-- start type TVInterfaceFactory -->
<h3>New Type TVMLKit.TVInterfaceFactory</h3>
<pre class='added' data-is-non-breaking="">
public class TVInterfaceFactory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, ITVInterfaceCreating {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVInterfaceFactory ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVInterfaceFactory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVInterfaceFactory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ITVInterfaceCreating ExtendedInterfaceCreator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static TVInterfaceFactory SharedInterfaceFactory { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIImage GetImageForResource (string resourceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetUrlForResource (string resourceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIViewController GetViewControllerForElement (TVViewElement element, UIKit.UIViewController existingViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIView GetViewForElement (TVViewElement element, UIKit.UIView existingView);</span>
}
</pre>
</div> <!-- end type TVInterfaceFactory -->
<div> <!-- start type TVMLKitError -->
<h3>New Type TVMLKit.TVMLKitError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVMLKitError {
	<span class='added added-field ' data-is-non-breaking="">FailedToLaunch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">InternetUnavailable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Last = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 1,</span>
}
</pre>
</div> <!-- end type TVMLKitError -->
<div> <!-- start type TVMLKitErrorExtensions -->
<h3>New Type TVMLKit.TVMLKitErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class TVMLKitErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (TVMLKitError self);</span>
}
</pre>
</div> <!-- end type TVMLKitErrorExtensions -->
<div> <!-- start type TVStyleFactory -->
<h3>New Type TVMLKit.TVStyleFactory</h3>
<pre class='added' data-is-non-breaking="">
public class TVStyleFactory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVStyleFactory ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVStyleFactory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVStyleFactory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void RegisterStyle (string styleName, TVViewElementStyleType type, bool inherited);</span>
}
</pre>
</div> <!-- end type TVStyleFactory -->
<div> <!-- start type TVTextElement -->
<h3>New Type TVMLKit.TVTextElement</h3>
<pre class='added' data-is-non-breaking="">
public class TVTextElement : TVMLKit.TVViewElement, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVTextElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVTextElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVTextElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVTextElementStyle TextStyle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAttributedString (UIKit.UIFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAttributedString (UIKit.UIFont font, UIKit.UIColor foregroundColor, UIKit.UITextAlignment alignment);</span>
}
</pre>
</div> <!-- end type TVTextElement -->
<div> <!-- start type TVTextElementStyle -->
<h3>New Type TVMLKit.TVTextElementStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVTextElementStyle {
	<span class='added added-field ' data-is-non-breaking="">Decoration = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Description = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title = 1,</span>
}
</pre>
</div> <!-- end type TVTextElementStyle -->
<div> <!-- start type TVViewElement -->
<h3>New Type TVMLKit.TVViewElement</h3>
<pre class='added' data-is-non-breaking="">
public class TVViewElement : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVViewElement ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVViewElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVViewElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSString&gt; Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AutoHighlightIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVViewElement[] ChildViewElements { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Disabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ElementIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ElementName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVViewElement ParentViewElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVViewElementStyle Style { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVElementUpdateType UpdateType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DispatchEvent (string eventName, bool canBubble, bool isCancellable, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; extraInfo, System.Action&lt;System.Boolean,System.Boolean&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DispatchEvent (TVElementEventType type, bool canBubble, bool isCancellable, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; extraInfo, System.Action&lt;System.Boolean,System.Boolean&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (TVElementResettableProperty resettableProperty);</span>
}
</pre>
</div> <!-- end type TVViewElement -->
<div> <!-- start type TVViewElementStyle -->
<h3>New Type TVMLKit.TVViewElementStyle</h3>
<pre class='added' data-is-non-breaking="">
public class TVViewElementStyle : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVViewElementStyle ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVViewElementStyle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVViewElementStyle (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual TVElementAlignment Alignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVColor BackgroundColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVColor Color { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVElementContentAlignment ContentAlignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FontSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString FontWeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVColor HighlightColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ImageTreatmentName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat InteritemSpacing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIEdgeInsets Margin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaxHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaxTextLines { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaxWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIEdgeInsets Padding { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVElementPosition Position { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RatingStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UITextAlignment TextAlignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TextHighlightStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TextMinimumScaleFactor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TextStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVColor TintColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ValueForStyleProperty (string name);</span>
}
</pre>
</div> <!-- end type TVViewElementStyle -->
<div> <!-- start type TVViewElementStyleType -->
<h3>New Type TVMLKit.TVViewElementStyleType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVViewElementStyleType {
	<span class='added added-field ' data-is-non-breaking="">Color = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">EdgeInsets = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Integer = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Point = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Transform = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Url = 6,</span>
}
</pre>
</div> <!-- end type TVViewElementStyleType -->
</div> <!-- end namespace TVMLKit -->

<!-- start namespace TVServices --> <div> 
<h2>New Namespace TVServices</h2>

<div> <!-- start type ITVTopShelfProvider -->
<h3>New Type TVServices.ITVTopShelfProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface ITVTopShelfProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual TVContentItem[] TopShelfItems { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVTopShelfContentStyle TopShelfStyle { get; }</span>
}
</pre>
</div> <!-- end type ITVTopShelfProvider -->
<div> <!-- start type TVContentIdentifier -->
<h3>New Type TVServices.TVContentIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public class TVContentIdentifier : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVContentIdentifier (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVContentIdentifier (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVContentIdentifier (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TVContentIdentifier (string identifier, TVContentIdentifier container);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVContentIdentifier Container { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type TVContentIdentifier -->
<div> <!-- start type TVContentItem -->
<h3>New Type TVServices.TVContentItem</h3>
<pre class='added' data-is-non-breaking="">
public class TVContentItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public TVContentItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVContentItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected TVContentItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TVContentItem (TVContentIdentifier ident);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber BadgeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVContentIdentifier ContentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber CurrentPosition { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl DisplayUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Duration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ExpirationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber HasPlayedToEnd { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVContentItemImageShape ImageShape { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl ImageUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate LastAccessedDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl PlayUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual TVContentItem[] TopShelfItems { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type TVContentItem -->
<div> <!-- start type TVContentItemImageShape -->
<h3>New Type TVServices.TVContentItemImageShape</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVContentItemImageShape {
	<span class='added added-field ' data-is-non-breaking="">ExtraWide = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Hdtv = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Poster = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Sdtv = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Wide = 5,</span>
}
</pre>
</div> <!-- end type TVContentItemImageShape -->
<div> <!-- start type TVContentItemImageShapeExtensions -->
<h3>New Type TVServices.TVContentItemImageShapeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class TVContentItemImageShapeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGSize GetSize (TVContentItemImageShape self, TVTopShelfContentStyle style);</span>
}
</pre>
</div> <!-- end type TVContentItemImageShapeExtensions -->
<div> <!-- start type TVTopShelfContentStyle -->
<h3>New Type TVServices.TVTopShelfContentStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TVTopShelfContentStyle {
	<span class='added added-field ' data-is-non-breaking="">Inset = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Sectioned = 2,</span>
}
</pre>
</div> <!-- end type TVTopShelfContentStyle -->
<div> <!-- start type TVTopShelfItems -->
<h3>New Type TVServices.TVTopShelfItems</h3>
<pre class='added' data-is-non-breaking="">
public static class TVTopShelfItems {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidChangeNotification { get; }</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type TVTopShelfItems -->
</div> <!-- end namespace TVServices -->

</div>
