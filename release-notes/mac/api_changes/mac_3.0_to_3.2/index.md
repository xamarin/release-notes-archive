---
id: 02B5E6C8-FBFF-46C5-947B-AACD92CD1173
title: "Mac 3.0 to 3.2"
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
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAsset --> <div>
<h3>Type Changed: AVFoundation.AVAsset</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AvailableMediaCharacteristicsWithMediaSelectionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVMetadataItem CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAssetTrackGroup[] TrackGroups { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string[] languages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVMediaSelectionGroup MediaSelectionGroupForMediaCharacteristic (string avMediaCharacteristic);</span>
</pre>
</div>
<!-- start type AVAsset.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAsset.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChapterMetadataGroupsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveContainsFragmentsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDurationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMediaSelectionGroupsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasDefragmented (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAsset.Notifications -->

</div> <!-- end type AVAsset -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString AudioTimePitchAlgorithm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVVideoCompositing CustomVideoCompositor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Preset3840x2160 { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
<!-- start type AVAssetImageGenerator --> <div>
<h3>Type Changed: AVFoundation.AVAssetImageGenerator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAsset Asset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVVideoCompositing CustomVideoCompositor { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetImageGenerator -->
<!-- start type AVAssetReaderTrackOutput --> <div>
<h3>Type Changed: AVFoundation.AVAssetReaderTrackOutput</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString AudioTimePitchAlgorithm { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVAssetReaderTrackOutput -->
<!-- start type AVAssetTrack --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanProvideSampleCursors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime MinFrameDuration { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursor (CoreMedia.CMTime presentationTimeStamp);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursorAtFirstSampleInDecodeOrder ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursorAtLastSampleInDecodeOrder ();</span>
</pre>
</div>
<!-- start type AVAssetTrack.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSegmentsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimeRangeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTrackAssociationsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAssetTrack.Notifications -->

</div> <!-- end type AVAssetTrack -->
<!-- start type AVAssetWriter --> <div>
<h3>Type Changed: AVFoundation.AVAssetWriter</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddInputGroup (AVAssetWriterInputGroup inputGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanAddInputGroup (AVAssetWriterInputGroup inputGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishWriting (System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task FinishWritingAsync ();</span>
</pre>
</div>

</div> <!-- end type AVAssetWriter -->
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine</h3>
<!-- start type AVAudioEngine.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioEngine.Notifications -->

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioRecorder --> <div>
<h3>Type Changed: AVFoundation.AVAudioRecorder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioFormat Format { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioRecorder -->
<!-- start type AVAudioUnitComponent --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponent</h3>
<!-- start type AVAudioUnitComponent.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponent.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTagsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioUnitComponent.Notifications -->

</div> <!-- end type AVAudioUnitComponent -->
<!-- start type AVCaptureAudioChannel --> <div>
<h3>Type Changed: AVFoundation.AVCaptureAudioChannel</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Volume { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVCaptureAudioChannel -->
<!-- start type AVCaptureAudioDataOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureAudioDataOutput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public AudioSettings AudioSettings { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakAudioSettings { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegateQueue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureAudioDataOutput -->
<!-- start type AVCaptureConnection --> <div>
<h3>Type Changed: AVFoundation.AVCaptureConnection</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsVideoFieldMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVVideoFieldMode VideoFieldMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVCaptureConnection -->
<!-- start type AVCaptureDevice --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDeviceFormat ActiveFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDeviceInputSource ActiveInputSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDeviceFormat[] Formats { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasFlash { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasTorch { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InUseByAnotherApplication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDeviceInputSource[] InputSources { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDevice[] LinkedDevices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Suspended { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureDeviceTransportControlsPlaybackMode TransportControlsPlaybackMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float TransportControlsSpeed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TransportControlsSupported { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int WeakTransportType { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTransportControlsPlaybackMode (AVCaptureDeviceTransportControlsPlaybackMode mode, float speed);</span>
</pre>
</div>
<!-- start type AVCaptureDevice.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasConnected (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasDisconnected (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureDevice.Notifications -->

</div> <!-- end type AVCaptureDevice -->
<!-- start type AVCaptureFileOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureFileOutput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVCaptureFileOutputDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RecordingPaused { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutput -->
<!-- start type AVCaptureFileOutputRecordingDelegate --> <div>
<h3>Type Changed: AVFoundation.AVCaptureFileOutputRecordingDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidPauseRecording (AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidResumeRecording (AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillFinishRecording (AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutputRecordingDelegate -->
<!-- start type AVCaptureFileOutputRecordingDelegate_Extensions --> <div>
<h3>Type Changed: AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidPauseRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidResumeRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillFinishRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutputRecordingDelegate_Extensions -->
<!-- start type AVCaptureInput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureInput</h3>
<!-- start type AVCaptureInput.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureInput.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePortFormatDescriptionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureInput.Notifications -->

</div> <!-- end type AVCaptureInput -->
<!-- start type AVCaptureMovieFileOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureMovieFileOutput</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDictionary GetOutputSettings (AVCaptureConnection connection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetOutputSettings (Foundation.NSDictionary outputSettings, AVCaptureConnection connection);</span>
</pre>
</div>

</div> <!-- end type AVCaptureMovieFileOutput -->
<!-- start type AVCaptureSession --> <div>
<h3>Type Changed: AVFoundation.AVCaptureSession</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Preset320x240 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Preset960x540 { get; }</span>
</pre>
</div>
<!-- start type AVCaptureSession.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureSession.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidStartRunning (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidStopRunning (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRuntimeError (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVCaptureSessionRuntimeErrorEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureSession.Notifications -->

</div> <!-- end type AVCaptureSession -->
<!-- start type AVCaptureVideoDataOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegate (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureVideoDataOutput -->
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVCaptureVideoPreviewLayer (AVCaptureSession session, AVCaptureVideoPreviewLayer.InitMode mode);</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVFragmentedMovieTrack --> <div>
<h3>Type Changed: AVFoundation.AVFragmentedMovieTrack</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeRangeDidChangeNotification { get; }</span>
</pre>
</div>

</div> <!-- end type AVFragmentedMovieTrack -->
<!-- start type AVMovie --> <div>
<h3>Type Changed: AVFoundation.AVMovie</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReferenceRestrictionsKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVMovie -->
<!-- start type AVMutableMovieTrack --> <div>
<h3>Type Changed: AVFoundation.AVMutableMovieTrack</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AppendSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer, CoreMedia.CMTime outDecodeTime, CoreMedia.CMTime presentationTime, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool InsertMediaTimeRange (CoreMedia.CMTimeRange mediaTimeRange, CoreMedia.CMTimeRange trackTimeRange);</span>
</pre>
</div>

</div> <!-- end type AVMutableMovieTrack -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AppliesMediaSelectionCriteriaAutomatically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OutputObscuredDueToInsufficientExternalProtection { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVPlayerMediaSelectionCriteria MediaSelectionCriteriaForMediaCharacteristic (Foundation.NSString avMediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Seek (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Seek (Foundation.NSDate date, AVCompletion onComplete);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetMediaSelectionCriteria (AVPlayerMediaSelectionCriteria criteria, Foundation.NSString avMediaCharacteristic);</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->
<!-- start type AVPlayerItem --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem</h3>
<!-- start type AVPlayerItem.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemFailedToPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVPlayerItemErrorEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNewAccessLogEntry (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNewErrorLogEntry (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePlaybackStalled (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimeJumped (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVPlayerItem.Notifications -->

</div> <!-- end type AVPlayerItem -->
<!-- start type AVPlayerItemAccessLogEvent --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemAccessLogEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double IndicatedAverageBitrate { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemAccessLogEvent -->
<!-- start type AVPlayerItemVideoOutputSettings --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemVideoOutputSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? AllowWideColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemVideoOutputSettings -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<!-- start type AVSampleBufferDisplayLayer.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFailedToDecode (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer.Notifications -->

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVUrlAsset --> <div>
<h3>Type Changed: AVFoundation.AVUrlAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MayRequireContentKeysForMediaDataProcessing { get; }</span>
</pre>
</div>

</div> <!-- end type AVUrlAsset -->
<!-- start type AVVideo --> <div>
<h3>Type Changed: AVFoundation.AVVideo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AllowFrameReorderingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AverageNonDroppableFrameRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EncoderSpecificationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExpectedSourceFrameRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264EntropyModeCABAC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264EntropyModeCAVLC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264EntropyModeKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideo -->
<!-- start type AVVideoColorPrimaries --> <div>
<h3>Type Changed: AVFoundation.AVVideoColorPrimaries</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString P3_D65 { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoColorPrimaries -->
<div> <!-- start type AVAssetExportPresetApple -->
<h3>New Type AVFoundation.AVAssetExportPresetApple</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAssetExportPresetApple {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4V1080pHD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4V480pSD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4V720pHD { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4VAppleTV { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4VCellular { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4VWiFi { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString M4ViPod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProRes422Lpcm { get; }</span>
}
</pre>
</div> <!-- end type AVAssetExportPresetApple -->
<div> <!-- start type AVAudioTimePitchAlgorithm -->
<h3>New Type AVFoundation.AVAudioTimePitchAlgorithm</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAudioTimePitchAlgorithm {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Spectral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeDomain { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Varispeed { get; }</span>
}
</pre>
</div> <!-- end type AVAudioTimePitchAlgorithm -->
<div> <!-- start type AVCaptureFileOutputDelegate -->
<h3>New Type AVFoundation.AVCaptureFileOutputDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVCaptureFileOutputDelegate : Foundation.NSObject, IAVCaptureFileOutputDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureFileOutputDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureFileOutputDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureFileOutputDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldProvideSampleAccurateRecordingStart (AVCaptureOutput captureOutput);</span>
}
</pre>
</div> <!-- end type AVCaptureFileOutputDelegate -->
<div> <!-- start type AVCaptureFileOutputDelegate_Extensions -->
<h3>New Type AVFoundation.AVCaptureFileOutputDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVCaptureFileOutputDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidOutputSampleBuffer (IAVCaptureFileOutputDelegate This, AVCaptureOutput captureOutput, CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);</span>
}
</pre>
</div> <!-- end type AVCaptureFileOutputDelegate_Extensions -->
<div> <!-- start type AVContentAuthorizationStatus -->
<h3>New Type AVFoundation.AVContentAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Busy = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Completed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAvailable = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">NotPossible = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedOut = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type AVContentAuthorizationStatus -->
<div> <!-- start type AVContentKeyRequest -->
<h3>New Type AVFoundation.AVContentKeyRequest</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeyRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanProvidePersistableContentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData InitializationData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProtocolVersions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVContentKeyRequestStatus Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void MakeStreamingContentKeyRequestData (Foundation.NSData appIdentifier, Foundation.NSData contentIdentifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; MakeStreamingContentKeyRequestDataAsync (Foundation.NSData appIdentifier, Foundation.NSData contentIdentifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Process (AVContentKeyResponse keyResponse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Process (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RespondByRequestingPersistableContentKeyRequest ();</span>
}
</pre>
</div> <!-- end type AVContentKeyRequest -->
<div> <!-- start type AVContentKeyRequestRetryReason -->
<h3>New Type AVFoundation.AVContentKeyRequestRetryReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeyRequestRetryReason {
	<span class='added added-field ' data-is-non-breaking="">ReceivedObsoleteContentKey = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReceivedResponseWithExpiredLease = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedOut = 0,</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestRetryReason -->
<div> <!-- start type AVContentKeyRequestRetryReasonExtensions -->
<h3>New Type AVFoundation.AVContentKeyRequestRetryReasonExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeyRequestRetryReasonExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVContentKeyRequestRetryReason self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeyRequestRetryReason GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestRetryReasonExtensions -->
<div> <!-- start type AVContentKeyRequestStatus -->
<h3>New Type AVFoundation.AVContentKeyRequestStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeyRequestStatus {
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Renewed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Requesting = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Retried = 3,</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestStatus -->
<div> <!-- start type AVContentKeyRequest_AVContentKeyRequestRenewal -->
<h3>New Type AVFoundation.AVContentKeyRequest_AVContentKeyRequestRenewal</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeyRequest_AVContentKeyRequestRenewal {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool GetRenewsExpiringResponseData (AVContentKeyRequest This);</span>
}
</pre>
</div> <!-- end type AVContentKeyRequest_AVContentKeyRequestRenewal -->
<div> <!-- start type AVContentKeyResponse -->
<h3>New Type AVFoundation.AVContentKeyResponse</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeyResponse : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeyResponse Create (Foundation.NSData fairPlayStreamingKeyResponseData);</span>
}
</pre>
</div> <!-- end type AVContentKeyResponse -->
<div> <!-- start type AVContentKeySession -->
<h3>New Type AVFoundation.AVContentKeySession</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeySession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ContentProtectionSessionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVContentKeySessionDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreFoundation.DispatchQueue DelegateQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVContentKeySystem KeySystem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString KeySystemConstant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl StorageUrl { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySession Create (AVContentKeySystem keySystem, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySession Create (Foundation.NSString keySystem, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Expire ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary[] GetPendingExpiredSessionReports (Foundation.NSData appIdentifier, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ProcessContentKeyRequest (Foundation.NSObject identifier, Foundation.NSData initializationData, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemovePendingExpiredSessionReports (Foundation.NSDictionary[] expiredSessionReports, Foundation.NSData appIdentifier, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RenewExpiringResponseData (AVContentKeyRequest contentKeyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDelegate (IAVContentKeySessionDelegate newDelegate, CoreFoundation.DispatchQueue delegateQueue);</span>
}
</pre>
</div> <!-- end type AVContentKeySession -->
<div> <!-- start type AVContentKeySessionDelegate -->
<h3>New Type AVFoundation.AVContentKeySessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVContentKeySessionDelegate : Foundation.NSObject, IAVContentKeySessionDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChange (AVContentKeySession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (AVContentKeySession session, AVContentKeyRequest keyRequest, Foundation.NSError err);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvidePersistableContentKeyRequest (AVContentKeySession session, AVPersistableContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideRenewingContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRetryContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest, string retryReason);</span>
}
</pre>
</div> <!-- end type AVContentKeySessionDelegate -->
<div> <!-- start type AVContentKeySessionDelegate_Extensions -->
<h3>New Type AVFoundation.AVContentKeySessionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySessionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidChange (IAVContentKeySessionDelegate This, AVContentKeySession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFail (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest, Foundation.NSError err);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidProvidePersistableContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVPersistableContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidProvideRenewingContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldRetryContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest, string retryReason);</span>
}
</pre>
</div> <!-- end type AVContentKeySessionDelegate_Extensions -->
<div> <!-- start type AVContentKeySession_AVContentKeyRecipients -->
<h3>New Type AVFoundation.AVContentKeySession_AVContentKeyRecipients</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySession_AVContentKeyRecipients {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Add (AVContentKeySession This, IAVContentKeyRecipient recipient);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IAVContentKeyRecipient[] GetContentKeyRecipients (AVContentKeySession This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Remove (AVContentKeySession This, IAVContentKeyRecipient recipient);</span>
}
</pre>
</div> <!-- end type AVContentKeySession_AVContentKeyRecipients -->
<div> <!-- start type AVContentKeySystem -->
<h3>New Type AVFoundation.AVContentKeySystem</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeySystem {
	<span class='added added-field ' data-is-non-breaking="">FairPlayStreaming = 0,</span>
}
</pre>
</div> <!-- end type AVContentKeySystem -->
<div> <!-- start type AVContentKeySystemExtensions -->
<h3>New Type AVFoundation.AVContentKeySystemExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySystemExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVContentKeySystem self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySystem GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVContentKeySystemExtensions -->
<div> <!-- start type AVMetadataFaceObject -->
<h3>New Type AVFoundation.AVMetadataFaceObject</h3>
<pre class='added' data-is-non-breaking="">
public class AVMetadataFaceObject : AVFoundation.AVMetadataObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVMetadataFaceObject ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVMetadataFaceObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVMetadataFaceObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint FaceID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasRollAngle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasYawAngle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RollAngle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YawAngle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type AVMetadataFaceObject -->
<div> <!-- start type AVMetadataObject -->
<h3>New Type AVFoundation.AVMetadataObject</h3>
<pre class='added' data-is-non-breaking="">
public class AVMetadataObject : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVMetadataObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVMetadataObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Time { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeFace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakType { get; }</span>
}
</pre>
</div> <!-- end type AVMetadataObject -->
<div> <!-- start type AVOutputSettingsAssistant -->
<h3>New Type AVFoundation.AVOutputSettingsAssistant</h3>
<pre class='added' data-is-non-breaking="">
public class AVOutputSettingsAssistant : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVOutputSettingsAssistant (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVOutputSettingsAssistant (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AudioSettings AudioSettings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] AvailableOutputSettingsPresets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVVideoSettingsCompressed CompressedVideoSettings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string OutputFileType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMAudioFormatDescription SourceAudioFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime SourceVideoAverageFrameDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMVideoFormatDescription SourceVideoFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime SourceVideoMinFrameDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVVideoSettingsUncompressed UnCompressedVideoSettings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakAudioSettings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakVideoSettings { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVOutputSettingsAssistant FromPreset (string presetIdentifier);</span>
}
</pre>
</div> <!-- end type AVOutputSettingsAssistant -->
<div> <!-- start type AVPersistableContentKeyRequest -->
<h3>New Type AVFoundation.AVPersistableContentKeyRequest</h3>
<pre class='added' data-is-non-breaking="">
public class AVPersistableContentKeyRequest : AVFoundation.AVContentKeyRequest, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPersistableContentKeyRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPersistableContentKeyRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetPersistableContentKey (Foundation.NSData keyVendorResponse, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, Foundation.NSError outError);</span>
}
</pre>
</div> <!-- end type AVPersistableContentKeyRequest -->
<div> <!-- start type AVSampleBufferGenerator -->
<h3>New Type AVFoundation.AVSampleBufferGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleBufferGenerator : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferGenerator (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferGenerator (AVAsset asset, CoreMedia.CMTimebase timebase);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreMedia.CMSampleBuffer CreateSampleBuffer (AVSampleBufferRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void NotifyOfDataReady (CoreMedia.CMSampleBuffer sbuf, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; NotifyOfDataReadyAsync (CoreMedia.CMSampleBuffer sbuf);</span>
}
</pre>
</div> <!-- end type AVSampleBufferGenerator -->
<div> <!-- start type AVSampleBufferRequest -->
<h3>New Type AVFoundation.AVSampleBufferRequest</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleBufferRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferRequest (AVSampleCursor startCursor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleBufferRequestDirection Direction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursor LimitCursor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaxSampleCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleBufferRequestMode Mode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime OverrideTime { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PreferredMinSampleCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursor StartCursor { get; }</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequest -->
<div> <!-- start type AVSampleBufferRequestDirection -->
<h3>New Type AVFoundation.AVSampleBufferRequestDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVSampleBufferRequestDirection {
	<span class='added added-field ' data-is-non-breaking="">Forward = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Reverse = -1,</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequestDirection -->
<div> <!-- start type AVSampleBufferRequestMode -->
<h3>New Type AVFoundation.AVSampleBufferRequestMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVSampleBufferRequestMode {
	<span class='added added-field ' data-is-non-breaking="">Immediate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Scheduled = 1,</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequestMode -->
<div> <!-- start type AVSampleCursor -->
<h3>New Type AVFoundation.AVSampleCursor</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleCursor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleCursor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleCursor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursorChunkInfo CurrentChunkInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursorStorageRange CurrentChunkStorageRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl CurrentChunkStorageUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursorSyncInfo CurrentSampleDependencyInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime CurrentSampleDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long CurrentSampleIndexInChunk { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursorStorageRange CurrentSampleStorageRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVSampleCursorSyncInfo CurrentSampleSyncInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime DecodeTimeStamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime PresentationTimeStamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SamplesRequiredForDecoderRefresh { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSComparisonResult ComparePositionInDecodeOrder (AVSampleCursor positionOfCursor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreMedia.CMFormatDescription CopyCurrentSampleFormatDescription ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SamplesWithEarlierDecodeTimeStampsMayHaveLaterPresentationTimeStampsThan (AVSampleCursor positionOfCursor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SamplesWithLaterDecodeTimeStampsMayHaveEarlierPresentationTimeStampsThan (AVSampleCursor positionOfCursor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreMedia.CMTime StepByDecodeTime (CoreMedia.CMTime deltaDecodeTime, bool wasPinned);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreMedia.CMTime StepByPresentationTime (CoreMedia.CMTime deltaPresentationTime, bool wasPinned);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long StepInDecodeOrder (long stepCount);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual long StepInPresentationOrder (long stepCount);</span>
}
</pre>
</div> <!-- end type AVSampleCursor -->
<div> <!-- start type AVSampleCursorChunkInfo -->
<h3>New Type AVFoundation.AVSampleCursorChunkInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorChunkInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformFormatDescriptions;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformSampleDurations;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformSampleSizes;</span>
	<span class='added added-field ' data-is-non-breaking="">public long SampleCount;</span>
}
</pre>
</div> <!-- end type AVSampleCursorChunkInfo -->
<div> <!-- start type AVSampleCursorDependencyInfo -->
<h3>New Type AVFoundation.AVSampleCursorDependencyInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorDependencyInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool DependsOnOthers;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasDependentSamples;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasRedundantCoding;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItDependsOnOthers;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItHasDependentSamples;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItHasRedundantCoding;</span>
}
</pre>
</div> <!-- end type AVSampleCursorDependencyInfo -->
<div> <!-- start type AVSampleCursorStorageRange -->
<h3>New Type AVFoundation.AVSampleCursorStorageRange</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorStorageRange {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public long Length;</span>
	<span class='added added-field ' data-is-non-breaking="">public long Offset;</span>
}
</pre>
</div> <!-- end type AVSampleCursorStorageRange -->
<div> <!-- start type AVSampleCursorSyncInfo -->
<h3>New Type AVFoundation.AVSampleCursorSyncInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorSyncInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool IsDroppable;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IsFullSync;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IsPartialSync;</span>
}
</pre>
</div> <!-- end type AVSampleCursorSyncInfo -->
<div> <!-- start type IAVCaptureFileOutputDelegate -->
<h3>New Type AVFoundation.IAVCaptureFileOutputDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVCaptureFileOutputDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldProvideSampleAccurateRecordingStart (AVCaptureOutput captureOutput);</span>
}
</pre>
</div> <!-- end type IAVCaptureFileOutputDelegate -->
<div> <!-- start type IAVContentKeyRecipient -->
<h3>New Type AVFoundation.IAVContentKeyRecipient</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVContentKeyRecipient : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MayRequireContentKeysForMediaDataProcessing { get; }</span>
}
</pre>
</div> <!-- end type IAVContentKeyRecipient -->
<div> <!-- start type IAVContentKeySessionDelegate -->
<h3>New Type AVFoundation.IAVContentKeySessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVContentKeySessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
}
</pre>
</div> <!-- end type IAVContentKeySessionDelegate -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSMenu ActionPopUpButtonMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanBeginTrimming { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFrameSteppingButtons { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFullScreenToggleButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsSharingServiceButton { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginTrimming (System.Action&lt;AVPlayerViewTrimResult&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FlashChapter (uint chapterNumber, string chapterTitle);</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->
<div> <!-- start type AVCaptureView -->
<h3>New Type AVKit.AVCaptureView</h3>
<pre class='added' data-is-non-breaking="">
public class AVCaptureView : AppKit.NSView, AppKit.INSAccessibility, AppKit.INSAccessibilityElementProtocol, AppKit.INSAppearanceCustomization, AppKit.INSDraggingDestination, AppKit.INSTouchBarProvider, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVCaptureView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVCaptureView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureViewControlsStyle ControlsStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVCaptureViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVCaptureFileOutput FileOutput { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVCaptureSession Session { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakVideoGravity { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSession (AVFoundation.AVCaptureSession session, bool showVideoPreview, bool showAudioPreview);</span>
}
</pre>
</div> <!-- end type AVCaptureView -->
<div> <!-- start type AVCaptureViewControlsStyle -->
<h3>New Type AVKit.AVCaptureViewControlsStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVCaptureViewControlsStyle {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Floating = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inline = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">InlineDeviceSelection = 2,</span>
}
</pre>
</div> <!-- end type AVCaptureViewControlsStyle -->
<div> <!-- start type AVCaptureViewDelegate -->
<h3>New Type AVKit.AVCaptureViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVCaptureViewDelegate : Foundation.NSObject, IAVCaptureViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartRecording (AVCaptureView captureView, AVFoundation.AVCaptureFileOutput fileOutput);</span>
}
</pre>
</div> <!-- end type AVCaptureViewDelegate -->
<div> <!-- start type AVPlayerViewTrimResult -->
<h3>New Type AVKit.AVPlayerViewTrimResult</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVPlayerViewTrimResult {
	<span class='added added-field ' data-is-non-breaking="">CancelButton = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">OKButton = 0,</span>
}
</pre>
</div> <!-- end type AVPlayerViewTrimResult -->
<div> <!-- start type IAVCaptureViewDelegate -->
<h3>New Type AVKit.IAVCaptureViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVCaptureViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartRecording (AVCaptureView captureView, AVFoundation.AVCaptureFileOutput fileOutput);</span>
}
</pre>
</div> <!-- end type IAVCaptureViewDelegate -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<!-- start type ACAccountStore.Notifications --> <div>
<h3>Type Changed: Accounts.ACAccountStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore.Notifications -->

</div> <!-- end type ACAccountStore -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAnimation --> <div>
<h3>Type Changed: AppKit.NSAnimation</h3>
<!-- start type NSAnimation.Notifications --> <div>
<h3>Type Changed: AppKit.NSAnimation.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveProgressMark (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSAnimationProgressMarkEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSAnimation.Notifications -->

</div> <!-- end type NSAnimation -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static bool IgnoreMissingAssembliesDuringRegistration;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSApplication.Notifications --> <div>
<h3>Type Changed: AppKit.NSApplication.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeScreenParameters (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidFinishLaunching (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSApplicationDidFinishLaunchingEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidFinishRestoringWindows (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidHide (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidResignActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUnhide (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUpdate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillBecomeActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillFinishLaunching (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillHide (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillResignActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillTerminate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillUnhide (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillUpdate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSApplication.Notifications -->

</div> <!-- end type NSApplication -->
<!-- start type NSBrowser --> <div>
<h3>Type Changed: AppKit.NSBrowser</h3>
<!-- start type NSBrowser.Notifications --> <div>
<h3>Type Changed: AppKit.NSBrowser.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColumnConfigurationChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSBrowser.Notifications -->

</div> <!-- end type NSBrowser -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSCell.Notifications --> <div>
<h3>Type Changed: AppKit.NSCell.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveControlTintChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSCell.Notifications -->

</div> <!-- end type NSCell -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<!-- start type NSColor.Notifications --> <div>
<h3>Type Changed: AppKit.NSColor.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSystemColorsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSColor.Notifications -->

</div> <!-- end type NSColor -->
<!-- start type NSColorPanel --> <div>
<h3>Type Changed: AppKit.NSColorPanel</h3>
<!-- start type NSColorPanel.Notifications --> <div>
<h3>Type Changed: AppKit.NSColorPanel.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColorChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSColorPanel.Notifications -->

</div> <!-- end type NSColorPanel -->
<!-- start type NSComboBox --> <div>
<h3>Type Changed: AppKit.NSComboBox</h3>
<!-- start type NSComboBox.Notifications --> <div>
<h3>Type Changed: AppKit.NSComboBox.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionIsChanging (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillDismiss (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillPopUp (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSComboBox.Notifications -->

</div> <!-- end type NSComboBox -->
<!-- start type NSControl --> <div>
<h3>Type Changed: AppKit.NSControl</h3>
<!-- start type NSControl.Notifications --> <div>
<h3>Type Changed: AppKit.NSControl.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidBeginEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidEndEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSControl.Notifications -->

</div> <!-- end type NSControl -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSDrawer.Notifications --> <div>
<h3>Type Changed: AppKit.NSDrawer.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidClose (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidOpen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillClose (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillOpen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSDrawer.Notifications -->

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: AppKit.NSFont</h3>
<!-- start type NSFont.Notifications --> <div>
<h3>Type Changed: AppKit.NSFont.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAntialiasThresholdChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFontSetChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFont.Notifications -->

</div> <!-- end type NSFont -->
<!-- start type NSFontCollection --> <div>
<h3>Type Changed: AppKit.NSFontCollection</h3>
<!-- start type NSFontCollection.Notifications --> <div>
<h3>Type Changed: AppKit.NSFontCollection.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSFontCollectionChangedEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFontCollection.Notifications -->

</div> <!-- end type NSFontCollection -->
<!-- start type NSHelpManager --> <div>
<h3>Type Changed: AppKit.NSHelpManager</h3>
<!-- start type NSHelpManager.Notifications --> <div>
<h3>Type Changed: AppKit.NSHelpManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveContextHelpModeDidActivate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveContextHelpModeDidDeactivate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSHelpManager.Notifications -->

</div> <!-- end type NSHelpManager -->
<!-- start type NSImageRep --> <div>
<h3>Type Changed: AppKit.NSImageRep</h3>
<!-- start type NSImageRep.Notifications --> <div>
<h3>Type Changed: AppKit.NSImageRep.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRegistryDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSImageRep.Notifications -->

</div> <!-- end type NSImageRep -->
<!-- start type NSLayoutConstraint --> <div>
<h3>Type Changed: AppKit.NSLayoutConstraint</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLayoutConstraint -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSMenu.Notifications --> <div>
<h3>Type Changed: AppKit.NSMenu.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidAddItem (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginTracking (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeItem (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndTracking (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidRemoveItem (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidSendAction (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillSendAction (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSMenu.Notifications -->

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOutlineView --> <div>
<h3>Type Changed: AppKit.NSOutlineView</h3>
<!-- start type NSOutlineView.Notifications --> <div>
<h3>Type Changed: AppKit.NSOutlineView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColumnDidMove (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColumnDidResize (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemDidCollapse (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemDidExpand (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemWillCollapse (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemWillExpand (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionIsChanging (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSOutlineView.Notifications -->

</div> <!-- end type NSOutlineView -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: AppKit.NSPopUpButton</h3>
<!-- start type NSPopUpButton.Notifications --> <div>
<h3>Type Changed: AppKit.NSPopUpButton.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillPopUp (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton.Notifications -->

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopUpButtonCell --> <div>
<h3>Type Changed: AppKit.NSPopUpButtonCell</h3>
<!-- start type NSPopUpButtonCell.Notifications --> <div>
<h3>Type Changed: AppKit.NSPopUpButtonCell.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillPopUp (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopUpButtonCell.Notifications -->

</div> <!-- end type NSPopUpButtonCell -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSPopover.Notifications --> <div>
<h3>Type Changed: AppKit.NSPopover.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidClose (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidShow (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillClose (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillShow (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopover.Notifications -->

</div> <!-- end type NSPopover -->
<!-- start type NSPrintInfo --> <div>
<h3>Type Changed: AppKit.NSPrintInfo</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public PrintCore.PMPageFormat GetPageFormat ();</span>
	<span class='added added-method ' data-is-non-breaking="">public PrintCore.PMPrintSession GetPrintSession ();</span>
	<span class='added added-method ' data-is-non-breaking="">public PrintCore.PMPrintSettings GetPrintSettings ();</span>
</pre>
</div>

</div> <!-- end type NSPrintInfo -->
<!-- start type NSRuleEditor --> <div>
<h3>Type Changed: AppKit.NSRuleEditor</h3>
<!-- start type NSRuleEditor.Notifications --> <div>
<h3>Type Changed: AppKit.NSRuleEditor.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSRuleEditor.Notifications -->

</div> <!-- end type NSRuleEditor -->
<!-- start type NSRulerView --> <div>
<h3>Type Changed: AppKit.NSRulerView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSRulerView -->
<!-- start type NSScreen --> <div>
<h3>Type Changed: AppKit.NSScreen</h3>
<!-- start type NSScreen.Notifications --> <div>
<h3>Type Changed: AppKit.NSScreen.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColorSpaceDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScreen.Notifications -->

</div> <!-- end type NSScreen -->
<!-- start type NSScrollView --> <div>
<h3>Type Changed: AppKit.NSScrollView</h3>
<!-- start type NSScrollView.Notifications --> <div>
<h3>Type Changed: AppKit.NSScrollView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndLiveMagnify (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndLiveScroll (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidLiveScroll (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillStartLiveMagnify (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScrollView.Notifications -->

</div> <!-- end type NSScrollView -->
<!-- start type NSScroller --> <div>
<h3>Type Changed: AppKit.NSScroller</h3>
<!-- start type NSScroller.Notifications --> <div>
<h3>Type Changed: AppKit.NSScroller.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePreferredStyleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScroller.Notifications -->

</div> <!-- end type NSScroller -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSpellChecker --> <div>
<h3>Type Changed: AppKit.NSSpellChecker</h3>
<!-- start type NSSpellChecker.Notifications --> <div>
<h3>Type Changed: AppKit.NSSpellChecker.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticCapitalization (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticPeriodSubstitution (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticSpellingCorrection (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticTextCompletion (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticTextReplacement (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSSpellChecker.Notifications -->

</div> <!-- end type NSSpellChecker -->
<!-- start type NSSplitView --> <div>
<h3>Type Changed: AppKit.NSSplitView</h3>
<!-- start type NSSplitView.Notifications --> <div>
<h3>Type Changed: AppKit.NSSplitView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNSSplitViewDidResizeSubviews (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNSSplitViewWillResizeSubviews (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSSplitView.Notifications -->

</div> <!-- end type NSSplitView -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<!-- start type NSTableView.Notifications --> <div>
<h3>Type Changed: AppKit.NSTableView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColumnDidMove (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveColumnDidResize (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionIsChanging (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTableView.Notifications -->

</div> <!-- end type NSTableView -->
<!-- start type NSText --> <div>
<h3>Type Changed: AppKit.NSText</h3>
<!-- start type NSText.Notifications --> <div>
<h3>Type Changed: AppKit.NSText.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBeginEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextDidEndEditingEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSText.Notifications -->

</div> <!-- end type NSText -->
<!-- start type NSTextAlternatives --> <div>
<h3>Type Changed: AppKit.NSTextAlternatives</h3>
<!-- start type NSTextAlternatives.Notifications --> <div>
<h3>Type Changed: AppKit.NSTextAlternatives.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedAlternativeString (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextAlternativesSelectedAlternativeStringEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextAlternatives.Notifications -->

</div> <!-- end type NSTextAlternatives -->
<!-- start type NSTextContainer --> <div>
<h3>Type Changed: AppKit.NSTextContainer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSTextContainer -->
<!-- start type NSTextInputContext --> <div>
<h3>Type Changed: AppKit.NSTextInputContext</h3>
<!-- start type NSTextInputContext.Notifications --> <div>
<h3>Type Changed: AppKit.NSTextInputContext.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveKeyboardSelectionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextInputContext.Notifications -->

</div> <!-- end type NSTextInputContext -->
<!-- start type NSTextStorage --> <div>
<h3>Type Changed: AppKit.NSTextStorage</h3>
<!-- start type NSTextStorage.Notifications --> <div>
<h3>Type Changed: AppKit.NSTextStorage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidProcessEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillProcessEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextStorage.Notifications -->

</div> <!-- end type NSTextStorage -->
<!-- start type NSTextView --> <div>
<h3>Type Changed: AppKit.NSTextView</h3>
<!-- start type NSTextView.Notifications --> <div>
<h3>Type Changed: AppKit.NSTextView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeSelection (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextViewDidChangeSelectionEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeTypingAttributes (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillChangeNotifyingTextView (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextViewWillChangeNotifyingTextViewEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextView.Notifications -->

</div> <!-- end type NSTextView -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<!-- start type NSToolbar.Notifications --> <div>
<h3>Type Changed: AppKit.NSToolbar.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNSToolbarDidRemoveItem (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSToolbarItemEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNSToolbarWillAddItem (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSToolbarItemEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSToolbar.Notifications -->

</div> <!-- end type NSToolbar -->
<!-- start type NSTouch --> <div>
<h3>Type Changed: AppKit.NSTouch</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This type is not meant to be user-created")]
	public NSTouch ();</span>
</div></pre>

</div> <!-- end type NSTouch -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSView.Notifications --> <div>
<h3>Type Changed: AppKit.NSView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBoundsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFrameChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGlobalFrameChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUpdatedTrackingAreas (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSView.Notifications -->

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RowExpandedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueChangedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowMovedNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSWindow.Notifications --> <div>
<h3>Type Changed: AppKit.NSWindow.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementRequested (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationActivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationDeactivated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveApplicationShown (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeMain (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeBackingProperties (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWindowBackingPropertiesEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeScreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeScreenProfile (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDeminiaturize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndLiveResize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEndSheet (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEnterFullScreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEnterVersionBrowser (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidExitFullScreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidExitVersionBrowser (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidExpose (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWindowExposeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidMiniaturize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidMove (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidResignKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidResignMain (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidResize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUpdate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDrawerCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHelpTagCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLayoutChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMainWindowChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCollapsed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowCountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRowExpanded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedCellsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedChildrenMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedColumnsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedRowsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectedTextChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSheetCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTitleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementDestroyed (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUIElementFocusedChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnitsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveValueChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillBeginSheet (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillClose (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillEnterFullScreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillEnterVersionBrowser (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillExitFullScreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillExitVersionBrowser (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillMiniaturize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillMove (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillStartLiveResize (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowCreated (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowDeminiaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMiniaturized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowMoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWindowResized (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSWindow.Notifications -->

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayOptionsDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type NSWorkspace.Notifications --> <div>
<h3>Type Changed: AppKit.NSWorkspace.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveActiveSpaceDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidActivateApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeFileLabels (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDeactivateApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidHideApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidLaunchApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidMount (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidPerformFileOperation (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceFileOperationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidRenameVolume (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceRenamedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidTerminateApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUnhideApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidUnmount (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidWake (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayOptionsDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayOptionsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScreensDidSleep (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScreensDidWake (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSessionDidBecomeActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSessionDidResignActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillLaunchApplication (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillPowerOff (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillSleep (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillUnmount (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSWorkspace.Notifications -->

</div> <!-- end type NSWorkspace -->
<div> <!-- start type NSToolbarItemGroup -->
<h3>New Type AppKit.NSToolbarItemGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSToolbarItemGroup : AppKit.NSToolbarItem, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbarItemGroup ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSToolbarItemGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSToolbarItemGroup (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbarItemGroup (string itemIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSToolbarItem[] Subitems { get; set; }</span>
}
</pre>
</div> <!-- end type NSToolbarItemGroup -->

</div> <!-- end namespace AppKit -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<!-- start type AUAudioUnit.Notifications --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioComponentInstanceInvalidation (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioComponentRegistrationsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit.Notifications -->

</div> <!-- end type AUAudioUnit -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKContainer --> <div>
<h3>Type Changed: CloudKit.CKContainer</h3>
<!-- start type CKContainer.Notifications --> <div>
<h3>Type Changed: CloudKit.CKContainer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAccountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type CKContainer.Notifications -->

</div> <!-- end type CKContainer -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactStore --> <div>
<h3>Type Changed: Contacts.CNContactStore</h3>
<!-- start type CNContactStore.Notifications --> <div>
<h3>Type Changed: Contacts.CNContactStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNotificationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type CNContactStore.Notifications -->

</div> <!-- end type CNContactStore -->
<!-- start type CNMutablePostalAddress --> <div>
<h3>Type Changed: Contacts.CNMutablePostalAddress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubAdministrativeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubLocality { get; set; }</span>
</pre>
</div>

</div> <!-- end type CNMutablePostalAddress -->
<!-- start type CNPostalAddress --> <div>
<h3>Type Changed: Contacts.CNPostalAddress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubAdministrativeArea { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubLocality { get; }</span>
</pre>
</div>

</div> <!-- end type CNPostalAddress -->
<!-- start type CNPostalAddressKey --> <div>
<h3>Type Changed: Contacts.CNPostalAddressKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SubAdministrativeArea { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SubLocality { get; }</span>
</pre>
</div>

</div> <!-- end type CNPostalAddressKey -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollBoth { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollHorizontally { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollNone { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollVertically { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CAScroll Scroll { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<div> <!-- start type CAScroll -->
<h3>New Type CoreAnimation.CAScroll</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CAScroll {
	<span class='added added-field ' data-is-non-breaking="">Both = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Horizontally = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertically = 1,</span>
}
</pre>
</div> <!-- end type CAScroll -->
<div> <!-- start type CAScrollExtensions -->
<h3>New Type CoreAnimation.CAScrollExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CAScrollExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CAScroll self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CAScroll GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CAScrollExtensions -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<!-- start type NSManagedObjectContext.Notifications --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidSave (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveObjectsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillSave (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext.Notifications -->

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<!-- start type NSPersistentStoreCoordinator.Notifications --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidImportUbiquitousContentChanges (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresWillChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPersistentStoreCoordinatorStoreChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillRemoveStore (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator.Notifications -->

</div> <!-- end type NSPersistentStoreCoordinator -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreFoundation --> <div> 
<h2>Namespace CoreFoundation</h2>
<!-- start type CFNetworkErrors --> <div>
<h3>Type Changed: CoreFoundation.CFNetworkErrors</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FileOutsideSafeArea = -1104,</span>
</pre>
</div>

</div> <!-- end type CFNetworkErrors -->

</div> <!-- end namespace CoreFoundation -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<div> <!-- start type CGCaptureOptions -->
<h3>New Type CoreGraphics.CGCaptureOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGCaptureOptions {
	<span class='added added-field ' data-is-non-breaking="">NoFill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CGCaptureOptions -->
<div> <!-- start type CGDisplay -->
<h3>New Type CoreGraphics.CGDisplay</h3>
<pre class='added' data-is-non-breaking="">
public static class CGDisplay {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static int MainDisplayID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int ShieldingWindowLevel { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static int Capture (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int Capture (int display, CGCaptureOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int CaptureAllDisplays ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGRect GetBounds (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetDisplayID (int displayMask);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetGammaTableCapacity (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetHeight (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetOpenGLDisplayMask (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetShieldingWindowID (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetTypeID ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetWidth (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int HideCursor (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsCaptured (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int MoveCursor (int display, CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int Release (int display);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int ReleaseAllDisplays ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RestoreColorSyncSettings ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static int SetDisplayTransfer (int display, float redMin, float redMax, float redGamma, float greenMin, float greenMax, float greenGamma, float blueMin, float blueMax, float blueGamma);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int ShowCursor (int display);</span>
}
</pre>
</div> <!-- end type CGDisplay -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreMidi --> <div> 
<h2>Namespace CoreMidi</h2>
<!-- start type MidiObject --> <div>
<h3>Type Changed: CoreMidi.MidiObject</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MidiError FindByUniqueId (int uniqueId, MidiObject result);</span>
</pre>
</div>

</div> <!-- end type MidiObject -->

</div> <!-- end namespace CoreMidi -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVPixelFormatType --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Argb2101010LEPacked = 1815162994,</span>
</pre>
</div>

</div> <!-- end type CVPixelFormatType -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<!-- start type EKEventStore.Notifications --> <div>
<h3>Type Changed: EventKit.EKEventStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type EKEventStore.Notifications -->

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSArray --> <div>
<h3>Type Changed: Foundation.NSArray</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSArray FromNSObjects&lt;T&gt; (System.Func&lt;T,Foundation.NSObject&gt; nsobjectificator, T[] items);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSCalendar --> <div>
<h3>Type Changed: Foundation.NSCalendar</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a NSCalendarOptions parameter")]
	public NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a NSCalendarOptions parameter")]
	public NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);</span>
</div></pre>
<!-- start type NSCalendar.Notifications --> <div>
<h3>Type Changed: Foundation.NSCalendar.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDayChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSCalendar.Notifications -->

</div> <!-- end type NSCalendar -->
<!-- start type NSFileCoordinator --> <div>
<h3>Type Changed: Foundation.NSFileCoordinator</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(INSFilePresenter) instead")]
	public NSFileCoordinator (NSFilePresenter filePresenterOrNil);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileCoordinator (INSFilePresenter filePresenterOrNil);</span>
</pre>
</div>

</div> <!-- end type NSFileCoordinator -->
<!-- start type NSFileHandle --> <div>
<h3>Type Changed: Foundation.NSFileHandle</h3>
<!-- start type NSFileHandle.Notifications --> <div>
<h3>Type Changed: Foundation.NSFileHandle.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveConnectionAccepted (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleConnectionAcceptedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDataAvailable (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveReadCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveReadToEndOfFileCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileHandle.Notifications -->

</div> <!-- end type NSFileHandle -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<!-- start type NSFileManager.Notifications --> <div>
<h3>Type Changed: Foundation.NSFileManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveUbiquityIdentityDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileManager.Notifications -->

</div> <!-- end type NSFileManager -->
<!-- start type NSFormatter --> <div>
<h3>Type Changed: Foundation.NSFormatter</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use IsPartialStringValid (ref string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out string error) instead")]
	public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, NSString error);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, string error);</span>
</pre>
</div>

</div> <!-- end type NSFormatter -->
<!-- start type NSHttpCookieStorage --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage</h3>
<!-- start type NSHttpCookieStorage.Notifications --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveAcceptPolicyChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCookiesChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSHttpCookieStorage.Notifications -->

</div> <!-- end type NSHttpCookieStorage -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use RegisterCloudKitShare (CloudKitRegistrationPreparationAction) instead")]
	public virtual void RegisterCloudKitShare (System.Action&lt;CloudKitRegistrationPreparationHandler&gt; preparationHandler);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterCloudKitShare (CloudKitRegistrationPreparationAction preparationHandler);</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSLocale --> <div>
<h3>Type Changed: Foundation.NSLocale</h3>
<!-- start type NSLocale.Notifications --> <div>
<h3>Type Changed: Foundation.NSLocale.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCurrentLocaleDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSLocale.Notifications -->

</div> <!-- end type NSLocale -->
<!-- start type NSMetadataQuery --> <div>
<h3>Type Changed: Foundation.NSMetadataQuery</h3>
<!-- start type NSMetadataQuery.Notifications --> <div>
<h3>Type Changed: Foundation.NSMetadataQuery.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidFinishGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidStartGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidUpdate (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveGatheringProgress (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSMetadataQuery.Notifications -->

</div> <!-- end type NSMetadataQuery -->
<!-- start type NSObject --> <div>
<h3>Type Changed: Foundation.NSObject</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use Bind (NSString binding, NSObject observable, string keyPath, [NullAllowed] NSDictionary options) instead")]
	public virtual void Bind (string binding, NSObject observable, string keyPath, NSDictionary options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetBindingInfo (NSString binding) instead")]
	public virtual NSDictionary BindingInfo (string binding);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetBindingOptionDescriptions (NSString aBinding) instead")]
	public virtual NSObject[] BindingOptionDescriptions (string aBinding);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetBindingValueClass (NSString binding) instead")]
	public virtual ObjCRuntime.Class BindingValueClass (string binding);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use SetDefaultPlaceholder (NSObject placeholder, NSObject marker, NSString binding) instead")]
	public static void SetDefaultPlaceholder (NSObject placeholder, NSObject marker, string binding);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use Unbind (NSString binding) instead")]
	public virtual void Unbind (string binding);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Bind (NSString binding, NSObject observable, string keyPath, NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public NSDictionary GetBindingInfo (NSString binding);</span>
	<span class='added added-method ' data-is-non-breaking="">public NSObject[] GetBindingOptionDescriptions (NSString aBinding);</span>
	<span class='added added-method ' data-is-non-breaking="">public ObjCRuntime.Class GetBindingValueClass (NSString binding);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject GetDefaultPlaceholder (NSObject marker, NSString binding);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDefaultPlaceholder (NSObject placeholder, NSObject marker, NSString binding);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unbind (NSString binding);</span>
</pre>
</div>

</div> <!-- end type NSObject -->
<!-- start type NSProcessInfo --> <div>
<h3>Type Changed: Foundation.NSProcessInfo</h3>
<!-- start type NSProcessInfo.Notifications --> <div>
<h3>Type Changed: Foundation.NSProcessInfo.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveThermalStateDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSProcessInfo.Notifications -->

</div> <!-- end type NSProcessInfo -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool IsEqualTo (IntPtr handle);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSTask --> <div>
<h3>Type Changed: Foundation.NSTask</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DidTerminateNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSTask -->
<!-- start type NSUbiquitousKeyValueStore --> <div>
<h3>Type Changed: Foundation.NSUbiquitousKeyValueStore</h3>
<!-- start type NSUbiquitousKeyValueStore.Notifications --> <div>
<h3>Type Changed: Foundation.NSUbiquitousKeyValueStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChangeExternally (NSObject objectToObserve, System.EventHandler&lt;NSUbiquitousKeyValueStoreChangeEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUbiquitousKeyValueStore.Notifications -->

</div> <!-- end type NSUbiquitousKeyValueStore -->
<!-- start type NSUndoManager --> <div>
<h3>Type Changed: Foundation.NSUndoManager</h3>
<!-- start type NSUndoManager.Notifications --> <div>
<h3>Type Changed: Foundation.NSUndoManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCheckpoint (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidOpenUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUndoManager.Notifications -->

</div> <!-- end type NSUndoManager -->
<!-- start type NSUrlCredentialStorage --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage</h3>
<!-- start type NSUrlCredentialStorage.Notifications --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUrlCredentialStorage.Notifications -->

</div> <!-- end type NSUrlCredentialStorage -->
<!-- start type NSUrlError --> <div>
<h3>Type Changed: Foundation.NSUrlError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FileOutsideSafeArea = -1104,</span>
</pre>
</div>

</div> <!-- end type NSUrlError -->
<!-- start type NSUrlSession --> <div>
<h3>Type Changed: Foundation.NSUrlSession</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a `INSUrlSessionDelegate` parameter.")]
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, INSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</pre>
</div>

</div> <!-- end type NSUrlSession -->
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: Foundation.NSUrlSessionHandler</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public long MaxInputInMemory { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->
<!-- start type NSUserDefaults --> <div>
<h3>Type Changed: Foundation.NSUserDefaults</h3>
<!-- start type NSUserDefaults.Notifications --> <div>
<h3>Type Changed: Foundation.NSUserDefaults.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUserDefaults.Notifications -->

</div> <!-- end type NSUserDefaults -->
<!-- start type NSUserNotificationActivationType --> <div>
<h3>Type Changed: Foundation.NSUserNotificationActivationType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AdditionalActionClicked = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Replied = 3,</span>
</pre>
</div>

</div> <!-- end type NSUserNotificationActivationType -->
<div> <!-- start type CloudKitRegistrationPreparationAction -->
<h3>New Type Foundation.CloudKitRegistrationPreparationAction</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CloudKitRegistrationPreparationAction : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CloudKitRegistrationPreparationAction (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CloudKitRegistrationPreparationHandler handler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CloudKitRegistrationPreparationHandler handler);</span>
}
</pre>
</div> <!-- end type CloudKitRegistrationPreparationAction -->
<div> <!-- start type NSStringTransformExtensions -->
<h3>New Type Foundation.NSStringTransformExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSStringTransformExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSStringTransform self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSStringTransform GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSStringTransformExtensions -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCController --> <div>
<h3>Type Changed: GameController.GCController</h3>
<!-- start type GCController.Notifications --> <div>
<h3>Type Changed: GameController.GCController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GCController.Notifications -->

</div> <!-- end type GCController -->
<!-- start type GCControllerButtonInput --> <div>
<h3>Type Changed: GameController.GCControllerButtonInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonValueChanged PressedChangedHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonValueChanged ValueChangedHandler { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the PressedChangedHandler property")]
	public virtual void SetPressedChangedHandler (GCControllerButtonValueChanged handler);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ValueChangedHandler property")]
	public virtual void SetValueChangedHandler (GCControllerButtonValueChanged handler);</span>
</div></pre>

</div> <!-- end type GCControllerButtonInput -->
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;GCMotion&gt; ValueChangedHandler { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ValueChangedHandler property")]
	public virtual void SetValueChangedHandler (System.Action&lt;GCMotion&gt; handler);</span>
</div></pre>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<!-- start type GKLocalPlayer.Notifications --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAuthenticationDidChangeNotificationName (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer.Notifications -->

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: GameKit.GKPlayer</h3>
<!-- start type GKPlayer.Notifications --> <div>
<h3>Type Changed: GameKit.GKPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeNotificationName (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKPlayer.Notifications -->

</div> <!-- end type GKPlayer -->

</div> <!-- end namespace GameKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExifSubsecTimeOriginal { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INIntentErrorCode --> <div>
<h3>Type Changed: Intents.INIntentErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExtensionBringUpFailed = 5001,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtensionLaunchingTimeout = 5000,</span>
</pre>
</div>

</div> <!-- end type INIntentErrorCode -->

</div> <!-- end namespace Intents -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TouchIdAuthenticationAllowableReuseDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double TouchIdAuthenticationMaximumAllowableReuseDuration { get; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MediaAccessibility --> <div> 
<h2>Namespace MediaAccessibility</h2>
<!-- start type MAAudibleMedia --> <div>
<h3>Type Changed: MediaAccessibility.MAAudibleMedia</h3>
<!-- start type MAAudibleMedia.Notifications --> <div>
<h3>Type Changed: MediaAccessibility.MAAudibleMedia.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSettingsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MAAudibleMedia.Notifications -->

</div> <!-- end type MAAudibleMedia -->

</div> <!-- end namespace MediaAccessibility -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyAssetUrl { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<div> <!-- start type MTLCommandBuffer_Extensions -->
<h3>New Type Metal.MTLCommandBuffer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLCommandBuffer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static double GetGpuEndTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetGpuStartTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetKernelEndTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetKernelStartTime (IMTLCommandBuffer This);</span>
}
</pre>
</div> <!-- end type MTLCommandBuffer_Extensions -->

</div> <!-- end namespace Metal -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromTextureAsync (ModelIO.MDLTexture texture, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromTextureAsync (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAsset (IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLComponent[] Components { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMDLComponent GetComponent (ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLLightProbe[] PlaceLightProbes (float density, MDLProbePlacement type, IMDLLightProbeIrradianceDataSource dataSource);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use the overload that takes an 'MDLLightProbeIrradianceDataSource' instead.")]
	public static MDLLightProbe[] PlaceLightProbes (float density, MDLProbePlacement type, MDLLightProbeIrradianceDataSource dataSource);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetComponent (IMDLComponent component, ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetComponent (IMDLComponent component, System.Type type);</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 vector, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator, MDLMesh.MDLMeshVectorType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCylinder (OpenTK.Vector3 extent, OpenTK.Vector2i segments, bool inwardNormals, bool topCap, bool bottomCap, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateIcosahedron (OpenTK.Vector3 extent, bool inwardNormals, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreatePlane (OpenTK.Vector3 extent, OpenTK.Vector2i segments, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLObject --> <div>
<h3>Type Changed: ModelIO.MDLObject</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLComponent[] Components { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetComponent (Type type)")]
	public virtual IMDLComponent IsComponentConforming (ObjCRuntime.Protocol protocol);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetComponent (IMDLComponent component, System.Type type);</span>
</pre>
</div>

</div> <!-- end type MDLObject -->
<!-- start type MDLObjectContainer --> <div>
<h3>Type Changed: ModelIO.MDLObjectContainer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLObject GetObject (uint index);</span>
</pre>
</div>

</div> <!-- end type MDLObjectContainer -->
<!-- start type MDLTransform --> <div>
<h3>Type Changed: ModelIO.MDLTransform</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetMatrix (OpenTK.Matrix4 matrix, double time);</span>
</pre>
</div>

</div> <!-- end type MDLTransform -->
<!-- start type MDLVertexAttributeData --> <div>
<h3>Type Changed: ModelIO.MDLVertexAttributeData</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BufferSize { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLVertexAttributeData -->
<div> <!-- start type MDLObjectContainerComponent_Extensions -->
<h3>New Type ModelIO.MDLObjectContainerComponent_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MDLObjectContainerComponent_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static uint GetCount (IMDLObjectContainerComponent This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLObject GetObject (IMDLObjectContainerComponent This, uint index);</span>
}
</pre>
</div> <!-- end type MDLObjectContainerComponent_Extensions -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NEFilterManager --> <div>
<h3>Type Changed: NetworkExtension.NEFilterManager</h3>
<!-- start type NEFilterManager.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEFilterManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEFilterManager.Notifications -->

</div> <!-- end type NEFilterManager -->
<!-- start type NEPacketTunnelProvider --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelProvider</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload accepting a INWTcpConnectionAuthenticationDelegate argument")]
	public virtual NWTcpConnection CreateTcpConnection (NWEndpoint remoteEndpoint, bool enableTls, NWTlsParameters tlsParameters, NWTcpConnectionAuthenticationDelegate delegate);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NWTcpConnection CreateTcpConnection (NWEndpoint remoteEndpoint, bool enableTls, NWTlsParameters tlsParameters, INWTcpConnectionAuthenticationDelegate delegate);</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelProvider -->
<!-- start type NEVpnConnection --> <div>
<h3>Type Changed: NetworkExtension.NEVpnConnection</h3>
<!-- start type NEVpnConnection.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEVpnConnection.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEVpnConnection.Notifications -->

</div> <!-- end type NEVpnConnection -->
<!-- start type NEVpnManager --> <div>
<h3>Type Changed: NetworkExtension.NEVpnManager</h3>
<!-- start type NEVpnManager.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEVpnManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEVpnManager.Notifications -->

</div> <!-- end type NEVpnManager -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.0.0"</span> <span class='added '>"3.2.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string PrintCoreLibrary = "/System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/PrintCore.framework/PrintCore";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr CachePointer (IntPtr handle, string constant, IntPtr* storage);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<!-- start type Protocol --> <div>
<h3>Type Changed: ObjCRuntime.Protocol</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public Protocol (System.Type type);</span>
</pre>
</div>

</div> <!-- end type Protocol -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfView --> <div>
<h3>Type Changed: PdfKit.PdfView</h3>
<!-- start type PdfView.Notifications --> <div>
<h3>Type Changed: PdfKit.PdfView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationHit (Foundation.NSObject objectToObserve, System.EventHandler&lt;PdfViewAnnotationHitEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnotationWillHit (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChangedHistory (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCopyPermission (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayBoxChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDisplayModeChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDocumentChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePageChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScaleChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type PdfView.Notifications -->

</div> <!-- end type PdfView -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLivePhotos = 213,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->

</div> <!-- end namespace Photos -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariApplication --> <div>
<h3>Type Changed: SafariServices.SFSafariApplication</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DispatchMessage (string messageName, string identifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DispatchMessageAsync (string messageName, string identifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo);</span>
</pre>
</div>

</div> <!-- end type SFSafariApplication -->
<!-- start type SFSafariExtensionHandler --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandler</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MessageReceivedFromContainingApp (string messageName, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ValidateContextMenuItem (string command, SFSafariPage page, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo, SFExtensionValidationHandler validationHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFExtensionValidationResult&gt; ValidateContextMenuItemAsync (string command, SFSafariPage page, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandler -->
<!-- start type SFSafariExtensionHandling_Extensions --> <div>
<h3>Type Changed: SafariServices.SFSafariExtensionHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void MessageReceivedFromContainingApp (ISFSafariExtensionHandling This, string messageName, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ValidateContextMenuItem (ISFSafariExtensionHandling This, string command, SFSafariPage page, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo, SFExtensionValidationHandler validationHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SFExtensionValidationResult&gt; ValidateContextMenuItemAsync (ISFSafariExtensionHandling This, string command, SFSafariPage page, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; userInfo);</span>
</pre>
</div>

</div> <!-- end type SFSafariExtensionHandling_Extensions -->
<!-- start type SFSafariToolbarItem --> <div>
<h3>Type Changed: SafariServices.SFSafariToolbarItem</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBadgeText (string badgeText);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetEnabled (bool enabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetImage (AppKit.NSImage image);</span>
</pre>
</div>

</div> <!-- end type SFSafariToolbarItem -->
<div> <!-- start type SFExtensionValidationHandler -->
<h3>New Type SafariServices.SFExtensionValidationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SFExtensionValidationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFExtensionValidationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool shouldHide, Foundation.NSString text, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool shouldHide, Foundation.NSString text);</span>
}
</pre>
</div> <!-- end type SFExtensionValidationHandler -->
<div> <!-- start type SFExtensionValidationResult -->
<h3>New Type SafariServices.SFExtensionValidationResult</h3>
<pre class='added' data-is-non-breaking="">
public class SFExtensionValidationResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFExtensionValidationResult (bool shouldHide, Foundation.NSString text);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool ShouldHide { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString Text { get; set; }</span>
}
</pre>
</div> <!-- end type SFExtensionValidationResult -->

</div> <!-- end namespace SafariServices -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNView -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecCertificate --> <div>
<h3>Type Changed: Security.SecCertificate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public string GetCommonName ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetEmailAddresses ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetNormalizedIssuerSequence ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetNormalizedSubjectSequence ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetSerialNumber ();</span>
</pre>
</div>

</div> <!-- end type SecCertificate -->
<!-- start type SecPadding --> <div>
<h3>Type Changed: Security.SecPadding</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Hash algorithm is deprecated")]
	PKCS1MD2 = 32768,</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Hash algorithm is deprecated")]
	PKCS1MD5 = 32769,</span>
</div></pre>

</div> <!-- end type SecPadding -->
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsExtractable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsSensitive { get; set; }</span>
</pre>
</div>

</div> <!-- end type SecRecord -->
<!-- start type SecStatusCode --> <div>
<h3>Type Changed: Security.SecStatusCode</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use InvalidCRLAuthority")]
	InvaldCRLAuthority = -67827,</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use InvalidTupleCredentials")]
	InvalidTupleCredendtials = -67852,</span>
</div></pre>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLAuthority = -67827,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTupleCredentials = -67852,</span>
</pre>
</div>

</div> <!-- end type SecStatusCode -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKEffectNode --> <div>
<h3>Type Changed: SpriteKit.SKEffectNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKEffectNode -->
<!-- start type SKEmitterNode --> <div>
<h3>Type Changed: SpriteKit.SKEmitterNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKEmitterNode -->
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKNode Create (string filename);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (SKNode node);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKShapeNode --> <div>
<h3>Type Changed: SpriteKit.SKShapeNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKShapeNode -->
<!-- start type SKSpriteNode --> <div>
<h3>Type Changed: SpriteKit.SKSpriteNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKSpriteNode -->
<!-- start type SKTileMapNode --> <div>
<h3>Type Changed: SpriteKit.SKTileMapNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKTileMapNode -->
<!-- start type SKUniform --> <div>
<h3>Type Changed: SpriteKit.SKUniform</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, SKTexture texture);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, float value);</span>
</pre>
</div>

</div> <!-- end type SKUniform -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKDownload --> <div>
<h3>Type Changed: StoreKit.SKDownload</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKPaymentTransaction Transaction { get; }</span>
</pre>
</div>

</div> <!-- end type SKDownload -->
<!-- start type SKError --> <div>
<h3>Type Changed: StoreKit.SKError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Revoked = 8,</span>
</pre>
</div>

</div> <!-- end type SKError -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type DomCssRuleType --> <div>
<h3>Type Changed: WebKit.DomCssRuleType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NamespaceRule = 10,</span>
</pre>
</div>

</div> <!-- end type DomCssRuleType -->
<!-- start type WKPreferences --> <div>
<h3>Type Changed: WebKit.WKPreferences</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabFocusesLinks { get; set; }</span>
</pre>
</div>

</div> <!-- end type WKPreferences -->
<!-- start type WebHistoryItem --> <div>
<h3>Type Changed: WebKit.WebHistoryItem</h3>
<!-- start type WebHistoryItem.Notifications --> <div>
<h3>Type Changed: WebKit.WebHistoryItem.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WebHistoryItem.Notifications -->

</div> <!-- end type WebHistoryItem -->

</div> <!-- end namespace WebKit -->
<!-- start namespace PrintCore --> <div> 
<h2>New Namespace PrintCore</h2>

<div> <!-- start type PMDuplexMode -->
<h3>New Type PrintCore.PMDuplexMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PMDuplexMode {
	<span class='added added-field ' data-is-non-breaking="">NoTumble = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">SimplexTumble = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Tumble = 3,</span>
}
</pre>
</div> <!-- end type PMDuplexMode -->
<div> <!-- start type PMOrientation -->
<h3>New Type PrintCore.PMOrientation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PMOrientation {
	<span class='added added-field ' data-is-non-breaking="">Landscape = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Portrait = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReverseLandscape = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ReversePortrait = 3,</span>
}
</pre>
</div> <!-- end type PMOrientation -->
<div> <!-- start type PMPageFormat -->
<h3>New Type PrintCore.PMPageFormat</h3>
<pre class='added' data-is-non-breaking="">
public class PMPageFormat : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPageFormat (PMPaper paper);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PMRect AdjustedPageRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMRect AdjustedPaperRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMOrientation Orientation { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode TryCreate (PMPageFormat pageFormat, PMPaper paper);</span>
}
</pre>
</div> <!-- end type PMPageFormat -->
<div> <!-- start type PMPaper -->
<h3>New Type PrintCore.PMPaper</h3>
<pre class='added' data-is-non-breaking="">
public class PMPaper : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public double Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMPaperMargins? Margins { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public string GetLocalizedName (PMPrinter printer);</span>
}
</pre>
</div> <!-- end type PMPaper -->
<div> <!-- start type PMPaperMargins -->
<h3>New Type PrintCore.PMPaperMargins</h3>
<pre class='added' data-is-non-breaking="">
public struct PMPaperMargins {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPaperMargins (double top, double bottom, double left, double right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public double Bottom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Left { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Right { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Top { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMPaperMargins -->
<div> <!-- start type PMPrintCoreBase -->
<h3>New Type PrintCore.PMPrintCoreBase</h3>
<pre class='added' data-is-non-breaking="">
public class PMPrintCoreBase : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~PMPrintCoreBase ();</span>
}
</pre>
</div> <!-- end type PMPrintCoreBase -->
<div> <!-- start type PMPrintException -->
<h3>New Type PrintCore.PMPrintException</h3>
<pre class='added' data-is-non-breaking="">
public class PMPrintException : System.Exception, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPrintException (PMStatusCode code);</span>
}
</pre>
</div> <!-- end type PMPrintException -->
<div> <!-- start type PMPrintSession -->
<h3>New Type PrintCore.PMPrintSession</h3>
<pre class='added' data-is-non-breaking="">
public class PMPrintSession : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPrintSession ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public PMStatusCode SessionError { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AssignDefaultPageFormat (PMPageFormat pageFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AssignDefaultSettings (PMPrintSettings settings);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode CreatePrinterList (string[] printerList, int index, PMPrinter printer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrintSession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode ValidatePrintSettings (PMPrintSettings settings, bool changed);</span>
}
</pre>
</div> <!-- end type PMPrintSession -->
<div> <!-- start type PMPrintSettings -->
<h3>New Type PrintCore.PMPrintSettings</h3>
<pre class='added' data-is-non-breaking="">
public class PMPrintSettings : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPrintSettings ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool Collate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint Copies { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMDuplexMode DuplexMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint FirstPage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint LastPage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Scale { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode CopySettings (PMPrintSettings destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode GetPageRange (uint minPage, uint maxPage);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode SetPageRange (uint minPage, uint maxPage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrintSettings settings);</span>
}
</pre>
</div> <!-- end type PMPrintSettings -->
<div> <!-- start type PMPrinter -->
<h3>New Type PrintCore.PMPrinter</h3>
<pre class='added' data-is-non-breaking="">
public class PMPrinter : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMPrinter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PMPrinter (string printerId);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl DeviceUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsDefault { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsFavorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsPostScriptCapable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsPostScriptPrinter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsRemote { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MakeAndModel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMPaper[] PaperList { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PMPrinterState PrinterState { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public PMResolution GetOutputResolution (PMPrintSettings settings);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode SetDefault ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetOutputResolution (PMPrintSettings settings, PMResolution res);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PMPrinter TryCreate (string printerId);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrinter printer);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode TryGetDeviceUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode TryGetMimeTypes (PMPrintSettings settings, string[] mimeTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode TryGetPaperList (PMPaper[] paperList);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode TryPrintFile (PMPrintSettings settings, PMPageFormat pageFormat, Foundation.NSUrl fileUrl, string mimeType);</span>
	<span class='added added-method ' data-is-non-breaking="">public PMStatusCode TryPrintFromProvider (PMPrintSettings settings, PMPageFormat pageFormat, CoreGraphics.CGDataProvider provider, string mimeType);</span>
}
</pre>
</div> <!-- end type PMPrinter -->
<div> <!-- start type PMPrinterState -->
<h3>New Type PrintCore.PMPrinterState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PMPrinterState {
	<span class='added added-field ' data-is-non-breaking="">Idle = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Processing = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 5,</span>
}
</pre>
</div> <!-- end type PMPrinterState -->
<div> <!-- start type PMRect -->
<h3>New Type PrintCore.PMRect</h3>
<pre class='added' data-is-non-breaking="">
public struct PMRect {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMRect (double top, double bottom, double left, double right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public double Bottom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Left { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Right { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Top { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMRect -->
<div> <!-- start type PMResolution -->
<h3>New Type PrintCore.PMResolution</h3>
<pre class='added' data-is-non-breaking="">
public struct PMResolution {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PMResolution (double horizontal, double vertical);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public double HorizontalResolution { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double VerticalResolution { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMResolution -->
<div> <!-- start type PMServer -->
<h3>New Type PrintCore.PMServer</h3>
<pre class='added' data-is-non-breaking="">
public class PMServer : PrintCore.PMPrintCoreBase, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode CreatePrinterList (PMPrinter[] printerList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PMStatusCode LaunchPrinterBrowser ();</span>
}
</pre>
</div> <!-- end type PMServer -->
<div> <!-- start type PMStatusCode -->
<h3>New Type PrintCore.PMStatusCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PMStatusCode {
	<span class='added added-field ' data-is-non-breaking="">AllocationFailure = -108,</span>
	<span class='added added-field ' data-is-non-breaking="">CloseFailed = -9785,</span>
	<span class='added added-field ' data-is-non-breaking="">CreateMessageFailed = -9620,</span>
	<span class='added added-field ' data-is-non-breaking="">CvmSymbolNotFound = -9662,</span>
	<span class='added added-field ' data-is-non-breaking="">DeleteSubTicketFailed = -9585,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentNotFound = -9644,</span>
	<span class='added added-field ' data-is-non-breaking="">DontSwitchPdeError = -9531,</span>
	<span class='added added-field ' data-is-non-breaking="">EditRequestFailed = -9544,</span>
	<span class='added added-field ' data-is-non-breaking="">FeatureNotInstalled = -9533,</span>
	<span class='added added-field ' data-is-non-breaking="">FileOrDirOperationFailed = -9634,</span>
	<span class='added added-field ' data-is-non-breaking="">FontNameTooLong = -9704,</span>
	<span class='added added-field ' data-is-non-breaking="">FontNotFound = -9703,</span>
	<span class='added added-field ' data-is-non-breaking="">GeneralCGError = -9705,</span>
	<span class='added added-field ' data-is-non-breaking="">GeneralError = -30870,</span>
	<span class='added added-field ' data-is-non-breaking="">IOAttrNotAvailable = -9787,</span>
	<span class='added added-field ' data-is-non-breaking="">IOMSymbolNotFound = -9661,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = -30870,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAllocator = -30890,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCalibrationTarget = -30898,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidConnection = -30887,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCvmContext = -9665,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFileType = -30895,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIOMContext = -9664,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIndex = -30882,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidItem = -30892,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidJobID = -9666,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidJobTemplate = -30885,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKey = -30888,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidLookupSpec = -9542,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidObject = -30896,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPMContext = -9663,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPageFormat = -30876,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPaper = -30897,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidParameter = -50,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPbmRef = -9540,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPdeContext = -9530,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPreset = -30899,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrintSession = -30879,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrintSettings = -30875,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrinter = -30880,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrinterAddress = -9780,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrinterInfo = -30886,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidReply = -30894,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidState = -9706,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSubTicket = -9584,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTicket = -30891,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidType = -30893,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidValue = -30889,</span>
	<span class='added added-field ' data-is-non-breaking="">ItemIsLocked = -9586,</span>
	<span class='added added-field ' data-is-non-breaking="">JobBusy = -9642,</span>
	<span class='added added-field ' data-is-non-breaking="">JobCanceled = -9643,</span>
	<span class='added added-field ' data-is-non-breaking="">JobGetTicketBadFormatError = -9672,</span>
	<span class='added added-field ' data-is-non-breaking="">JobGetTicketReadError = -9673,</span>
	<span class='added added-field ' data-is-non-breaking="">JobManagerAborted = -9671,</span>
	<span class='added added-field ' data-is-non-breaking="">JobNotFound = -9641,</span>
	<span class='added added-field ' data-is-non-breaking="">JobStreamEndError = -9670,</span>
	<span class='added added-field ' data-is-non-breaking="">JobStreamOpenFailed = -9668,</span>
	<span class='added added-field ' data-is-non-breaking="">JobStreamReadFailed = -9669,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyNotFound = -9589,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyNotUnique = -9590,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyOrValueNotFound = -9623,</span>
	<span class='added added-field ' data-is-non-breaking="">LockIgnored = -30878,</span>
	<span class='added added-field ' data-is-non-breaking="">MessagingError = -9624,</span>
	<span class='added added-field ' data-is-non-breaking="">NoDefaultItem = -9500,</span>
	<span class='added added-field ' data-is-non-breaking="">NoDefaultPrinter = -30872,</span>
	<span class='added added-field ' data-is-non-breaking="">NoDefaultSettings = -9501,</span>
	<span class='added added-field ' data-is-non-breaking="">NoPrinterJobID = -9667,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSelectedPrinters = -9541,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSuchEntry = -30874,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = -30873,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectInUse = -30881,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OpenFailed = -9781,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfScope = -30871,</span>
	<span class='added added-field ' data-is-non-breaking="">PMSymbolNotFound = -9660,</span>
	<span class='added added-field ' data-is-non-breaking="">PermissionError = -9636,</span>
	<span class='added added-field ' data-is-non-breaking="">PluginNotFound = -9701,</span>
	<span class='added added-field ' data-is-non-breaking="">PluginRegisterationFailed = -9702,</span>
	<span class='added added-field ' data-is-non-breaking="">PrBrowserNoUI = -9545,</span>
	<span class='added added-field ' data-is-non-breaking="">QueueAlreadyExists = -9639,</span>
	<span class='added added-field ' data-is-non-breaking="">QueueJobFailed = -9640,</span>
	<span class='added added-field ' data-is-non-breaking="">QueueNotFound = -9638,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadFailed = -9782,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadGotZeroData = -9788,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerAlreadyRunning = -9631,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerAttributeRestricted = -9633,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerCommunicationFailed = -9621,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerNotFound = -9630,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerSuspended = -9632,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusFailed = -9784,</span>
	<span class='added added-field ' data-is-non-breaking="">StringConversionFailure = -30883,</span>
	<span class='added added-field ' data-is-non-breaking="">SubTicketNotFound = -9583,</span>
	<span class='added added-field ' data-is-non-breaking="">SyncRequestFailed = -9543,</span>
	<span class='added added-field ' data-is-non-breaking="">TemplateIsLocked = -9588,</span>
	<span class='added added-field ' data-is-non-breaking="">TicketIsLocked = -9587,</span>
	<span class='added added-field ' data-is-non-breaking="">TicketTypeNotFound = -9580,</span>
	<span class='added added-field ' data-is-non-breaking="">UnableToFindProcess = -9532,</span>
	<span class='added added-field ' data-is-non-breaking="">UnexpectedImagingError = -9707,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownDataType = -9591,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownMessage = -9637,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedConnection = -9786,</span>
	<span class='added added-field ' data-is-non-breaking="">UpdateTicketFailed = -9581,</span>
	<span class='added added-field ' data-is-non-breaking="">UserOrGroupNotFound = -9635,</span>
	<span class='added added-field ' data-is-non-breaking="">ValidateTicketFailed = -9582,</span>
	<span class='added added-field ' data-is-non-breaking="">ValueOutOfRange = -30877,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteFailed = -9783,</span>
	<span class='added added-field ' data-is-non-breaking="">XMLParseError = -30884,</span>
}
</pre>
</div> <!-- end type PMStatusCode -->
</div> <!-- end namespace PrintCore -->

</div>
