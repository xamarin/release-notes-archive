---
id: 7f98426c-d87b-495c-bc74-426fc2a0c55c
title: "From 3.0.0 to 3.2.0"
---


<html><head><meta http-equiv="Content-Type" content="text/html; charset=windows-1252"></head><body><div>
<style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style>
<script type="text/javascript">
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
</script>
<h1>XamMac.dll</h1>
<a href="javascript: hideNonBreakingChanges (); " class="hide-nonbreaking">Hide non-breaking changes</a>
<a href="javascript: showNonBreakingChanges (); " class="restore-nonbreaking" style="display: none;">Show non-breaking changes</a>
<br>
<div data-is-topmost="">
<!-- start namespace MonoMac --> <div> 
<h2>Namespace MonoMac</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Modified fields:</p>
<pre><div data-is-breaking="">	public const string Version = <span class="removed removed-inline removed-breaking-inline">"3.0.0"</span> <span class="added ">"3.2.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>	<span class="added added-field " data-is-non-breaking="">public static const string PrintCoreLibrary = "/System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/PrintCore.framework/PrintCore";</span>
</pre>
</div>

</div> <!-- end type Constants -->

</div> <!-- end namespace MonoMac -->
<!-- start namespace MonoMac.AVFoundation --> <div> 
<h2>Namespace MonoMac.AVFoundation</h2>
<!-- start type AVAsset --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAsset</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual string[] AvailableMediaCharacteristicsWithMediaSelectionOptions { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVMetadataItem CreationDate { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVAssetTrackGroup[] TrackGroups { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string[] languages);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual AVMediaSelectionGroup MediaSelectionGroupForMediaCharacteristic (string avMediaCharacteristic);</span>
</pre>
</div>
<!-- start type AVAsset.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAsset.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveChapterMetadataGroupsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveContainsFragmentsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDurationDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMediaSelectionGroupsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWasDefragmented (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAsset.Notifications -->

</div> <!-- end type AVAsset -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSString AudioTimePitchAlgorithm { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVVideoCompositing CustomVideoCompositor { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString Preset3840x2160 { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
<!-- start type AVAssetImageGenerator --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetImageGenerator</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual AVAsset Asset { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVVideoCompositing CustomVideoCompositor { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetImageGenerator -->
<!-- start type AVAssetReaderTrackOutput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetReaderTrackOutput</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSString AudioTimePitchAlgorithm { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVAssetReaderTrackOutput -->
<!-- start type AVAssetTrack --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetTrack</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual bool CanProvideSampleCursors { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime MinFrameDuration { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursor (MonoMac.CoreMedia.CMTime presentationTimeStamp);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursorAtFirstSampleInDecodeOrder ();</span>
	<span class="added added-method " data-is-non-breaking="">public virtual AVSampleCursor MakeSampleCursorAtLastSampleInDecodeOrder ();</span>
</pre>
</div>
<!-- start type AVAssetTrack.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetTrack.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSegmentsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTimeRangeDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTrackAssociationsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAssetTrack.Notifications -->

</div> <!-- end type AVAssetTrack -->
<!-- start type AVAssetWriter --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAssetWriter</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual void AddInputGroup (AVAssetWriterInputGroup inputGroup);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual bool CanAddInputGroup (AVAssetWriterInputGroup inputGroup);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void FinishWriting (MonoMac.Foundation.NSAction completionHandler);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task FinishWritingAsync ();</span>
</pre>
</div>

</div> <!-- end type AVAssetWriter -->
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioEngine</h3>
<!-- start type AVAudioEngine.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioEngine.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveConfigurationChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioEngine.Notifications -->

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioPlayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioPlayer</h3>
<div>
<p>Added constructors:</p>
<pre>	<span class="added added-constructor " data-is-non-breaking="">public AVAudioPlayer (MonoMac.Foundation.NSData data, string fileTypeHint, MonoMac.Foundation.NSError outError);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVAudioPlayer (MonoMac.Foundation.NSUrl url, string fileTypeHint, MonoMac.Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayer -->
<!-- start type AVAudioRecorder --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioRecorder</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual AVAudioFormat Format { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioRecorder -->
<!-- start type AVAudioUnitComponent --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioUnitComponent</h3>
<!-- start type AVAudioUnitComponent.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVAudioUnitComponent.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTagsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioUnitComponent.Notifications -->

</div> <!-- end type AVAudioUnitComponent -->
<!-- start type AVCaptureAudioChannel --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureAudioChannel</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual float Volume { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVCaptureAudioChannel -->
<!-- start type AVCaptureAudioDataOutput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureAudioDataOutput</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public AudioSettings AudioSettings { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSDictionary WeakAudioSettings { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, MonoMac.CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureAudioDataOutput -->
<!-- start type AVCaptureConnection --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureConnection</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual bool SupportsVideoFieldMode { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVVideoFieldMode VideoFieldMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVCaptureConnection -->
<!-- start type AVCaptureDevice --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureDevice</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDeviceFormat ActiveFormat { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDeviceInputSource ActiveInputSource { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDeviceFormat[] Formats { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool HasFlash { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool HasTorch { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool InUseByAnotherApplication { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDeviceInputSource[] InputSources { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDevice[] LinkedDevices { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool Suspended { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVCaptureDeviceTransportControlsPlaybackMode TransportControlsPlaybackMode { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual float TransportControlsSpeed { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool TransportControlsSupported { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual int WeakTransportType { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual void SetTransportControlsPlaybackMode (AVCaptureDeviceTransportControlsPlaybackMode mode, float speed);</span>
</pre>
</div>
<!-- start type AVCaptureDevice.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureDevice.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWasConnected (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWasDisconnected (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureDevice.Notifications -->

</div> <!-- end type AVCaptureDevice -->
<!-- start type AVCaptureFileOutput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureFileOutput</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual IAVCaptureFileOutputDelegate Delegate { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool RecordingPaused { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutput -->
<!-- start type AVCaptureFileOutputRecordingDelegate --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureFileOutputRecordingDelegate</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual void DidPauseRecording (AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void DidResumeRecording (AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void WillFinishRecording (AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections, MonoMac.Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutputRecordingDelegate -->
<!-- start type AVCaptureFileOutputRecordingDelegate_Extensions --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static void DidPauseRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class="added added-method " data-is-non-breaking="">public static void DidResumeRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections);</span>
	<span class="added added-method " data-is-non-breaking="">public static void WillFinishRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, AVCaptureConnection[] connections, MonoMac.Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type AVCaptureFileOutputRecordingDelegate_Extensions -->
<!-- start type AVCaptureInput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureInput</h3>
<!-- start type AVCaptureInput.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureInput.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObservePortFormatDescriptionDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureInput.Notifications -->

</div> <!-- end type AVCaptureInput -->
<!-- start type AVCaptureMovieFileOutput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureMovieFileOutput</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.Foundation.NSDictionary GetOutputSettings (AVCaptureConnection connection);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void SetOutputSettings (MonoMac.Foundation.NSDictionary outputSettings, AVCaptureConnection connection);</span>
</pre>
</div>

</div> <!-- end type AVCaptureMovieFileOutput -->
<!-- start type AVCaptureSession --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureSession</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString Preset320x240 { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString Preset960x540 { get; }</span>
</pre>
</div>
<!-- start type AVCaptureSession.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureSession.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidStartRunning (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidStopRunning (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRuntimeError (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;AVCaptureSessionRuntimeErrorEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureSession.Notifications -->

</div> <!-- end type AVCaptureSession -->
<!-- start type AVCaptureVideoDataOutput --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Obsoleted methods:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegate (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, MonoMac.CoreFoundation.DispatchQueue sampleBufferCallbackQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureVideoDataOutput -->
<!-- start type AVFragmentedMovieTrack --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVFragmentedMovieTrack</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TimeRangeDidChangeNotification { get; }</span>
</pre>
</div>

</div> <!-- end type AVFragmentedMovieTrack -->
<!-- start type AVMovie --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVMovie</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ReferenceRestrictionsKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVMovie -->
<!-- start type AVMutableMovieTrack --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVMutableMovieTrack</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual bool AppendSampleBuffer (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, MonoMac.CoreMedia.CMTime outDecodeTime, MonoMac.CoreMedia.CMTime presentationTime, MonoMac.Foundation.NSError error);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual bool InsertMediaTimeRange (MonoMac.CoreMedia.CMTimeRange mediaTimeRange, MonoMac.CoreMedia.CMTimeRange trackTimeRange);</span>
</pre>
</div>

</div> <!-- end type AVMutableMovieTrack -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayer</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual bool AppliesMediaSelectionCriteriaAutomatically { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual bool OutputObscuredDueToInsufficientExternalProtection { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual AVPlayerMediaSelectionCriteria MediaSelectionCriteriaForMediaCharacteristic (MonoMac.Foundation.NSString avMediaCharacteristic);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void Seek (MonoMac.Foundation.NSDate date);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void Seek (MonoMac.Foundation.NSDate date, AVCompletion onComplete);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.Foundation.NSDate date);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual void SetMediaSelectionCriteria (AVPlayerMediaSelectionCriteria criteria, MonoMac.Foundation.NSString avMediaCharacteristic);</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->
<!-- start type AVPlayerItem --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItem</h3>
<!-- start type AVPlayerItem.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidPlayToEndTime (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveItemFailedToPlayToEndTime (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;AVPlayerItemErrorEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNewAccessLogEntry (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNewErrorLogEntry (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObservePlaybackStalled (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTimeJumped (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVPlayerItem.Notifications -->

</div> <!-- end type AVPlayerItem -->
<!-- start type AVPlayerItemVideoOutputSettings --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItemVideoOutputSettings</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public bool? AllowWideColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemVideoOutputSettings -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVSampleBufferDisplayLayer</h3>
<!-- start type AVSampleBufferDisplayLayer.Notifications --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVSampleBufferDisplayLayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFailedToDecode (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer.Notifications -->

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVVideo --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVVideo</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AllowFrameReorderingKey { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AverageNonDroppableFrameRateKey { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString EncoderSpecificationKey { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ExpectedSourceFrameRateKey { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString H264EntropyModeCABAC { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString H264EntropyModeCAVLC { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString H264EntropyModeKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideo -->
<!-- start type AVVideoColorPrimaries --> <div>
<h3>Type Changed: MonoMac.AVFoundation.AVVideoColorPrimaries</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString P3_D65 { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoColorPrimaries -->
<div> <!-- start type AVAssetExportPresetApple -->
<h3>New Type MonoMac.AVFoundation.AVAssetExportPresetApple</h3>
<pre class="added" data-is-non-breaking="">public static class AVAssetExportPresetApple {
	// properties
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4V1080pHD { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4V480pSD { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4V720pHD { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4VAppleTV { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4VCellular { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4VWiFi { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString M4ViPod { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ProRes422Lpcm { get; }</span>
}
</pre>
</div> <!-- end type AVAssetExportPresetApple -->
<div> <!-- start type AVAudioTimePitchAlgorithm -->
<h3>New Type MonoMac.AVFoundation.AVAudioTimePitchAlgorithm</h3>
<pre class="added" data-is-non-breaking="">public static class AVAudioTimePitchAlgorithm {
	// properties
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString Spectral { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TimeDomain { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString Varispeed { get; }</span>
}
</pre>
</div> <!-- end type AVAudioTimePitchAlgorithm -->
<div> <!-- start type AVCaptureFileOutputDelegate -->
<h3>New Type MonoMac.AVFoundation.AVCaptureFileOutputDelegate</h3>
<pre class="added" data-is-non-breaking="">public abstract class AVCaptureFileOutputDelegate : MonoMac.Foundation.NSObject, IAVCaptureFileOutputDelegate, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public AVCaptureFileOutputDelegate ();</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVCaptureFileOutputDelegate (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVCaptureFileOutputDelegate (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVCaptureFileOutputDelegate (IntPtr handle);</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual bool ShouldProvideSampleAccurateRecordingStart (AVCaptureOutput captureOutput);</span>
}
</pre>
</div> <!-- end type AVCaptureFileOutputDelegate -->
<div> <!-- start type AVCaptureFileOutputDelegate_Extensions -->
<h3>New Type MonoMac.AVFoundation.AVCaptureFileOutputDelegate_Extensions</h3>
<pre class="added" data-is-non-breaking="">public static class AVCaptureFileOutputDelegate_Extensions {
	// methods
	<span class="added added-method " data-is-non-breaking="">public static void DidOutputSampleBuffer (IAVCaptureFileOutputDelegate This, AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);</span>
}
</pre>
</div> <!-- end type AVCaptureFileOutputDelegate_Extensions -->
<div> <!-- start type AVContentAuthorizationStatus -->
<h3>New Type MonoMac.AVFoundation.AVContentAuthorizationStatus</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum AVContentAuthorizationStatus {
	<span class="added added-field " data-is-non-breaking="">Busy = 4,</span>
	<span class="added added-field " data-is-non-breaking="">Cancelled = 2,</span>
	<span class="added added-field " data-is-non-breaking="">Completed = 1,</span>
	<span class="added added-field " data-is-non-breaking="">NotAvailable = 5,</span>
	<span class="added added-field " data-is-non-breaking="">NotPossible = 6,</span>
	<span class="added added-field " data-is-non-breaking="">TimedOut = 3,</span>
	<span class="added added-field " data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type AVContentAuthorizationStatus -->
<div> <!-- start type AVOutputSettingsAssistant -->
<h3>New Type MonoMac.AVFoundation.AVOutputSettingsAssistant</h3>
<pre class="added" data-is-non-breaking="">public class AVOutputSettingsAssistant : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public AVOutputSettingsAssistant (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVOutputSettingsAssistant (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVOutputSettingsAssistant (IntPtr handle);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public AudioSettings AudioSettings { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static string[] AvailableOutputSettingsPresets { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public AVVideoSettingsCompressed CompressedVideoSettings { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual string OutputFileType { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMAudioFormatDescription SourceAudioFormat { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime SourceVideoAverageFrameDuration { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMVideoFormatDescription SourceVideoFormat { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime SourceVideoMinFrameDuration { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public AVVideoSettingsUncompressed UnCompressedVideoSettings { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSDictionary WeakAudioSettings { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSDictionary WeakVideoSettings { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public static AVOutputSettingsAssistant FromPreset (string presetIdentifier);</span>
}
</pre>
</div> <!-- end type AVOutputSettingsAssistant -->
<div> <!-- start type AVSampleBufferGenerator -->
<h3>New Type MonoMac.AVFoundation.AVSampleBufferGenerator</h3>
<pre class="added" data-is-non-breaking="">public class AVSampleBufferGenerator : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferGenerator (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferGenerator (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferGenerator (IntPtr handle);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferGenerator (AVAsset asset, MonoMac.CoreMedia.CMTimebase timebase);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMSampleBuffer CreateSampleBuffer (AVSampleBufferRequest request);</span>
	<span class="added added-method " data-is-non-breaking="">public static void NotifyOfDataReady (MonoMac.CoreMedia.CMSampleBuffer sbuf, System.Action&lt;System.Boolean,MonoMac.Foundation.NSError&gt; completionHandler);</span>
	<span class="added added-method " data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;bool&gt; NotifyOfDataReadyAsync (MonoMac.CoreMedia.CMSampleBuffer sbuf);</span>
}
</pre>
</div> <!-- end type AVSampleBufferGenerator -->
<div> <!-- start type AVSampleBufferRequest -->
<h3>New Type MonoMac.AVFoundation.AVSampleBufferRequest</h3>
<pre class="added" data-is-non-breaking="">public class AVSampleBufferRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferRequest (AVSampleCursor startCursor);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferRequest (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferRequest (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleBufferRequest (IntPtr handle);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleBufferRequestDirection Direction { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursor LimitCursor { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual int MaxSampleCount { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleBufferRequestMode Mode { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime OverrideTime { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual int PreferredMinSampleCount { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursor StartCursor { get; }</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequest -->
<div> <!-- start type AVSampleBufferRequestDirection -->
<h3>New Type MonoMac.AVFoundation.AVSampleBufferRequestDirection</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum AVSampleBufferRequestDirection {
	<span class="added added-field " data-is-non-breaking="">Forward = 1,</span>
	<span class="added added-field " data-is-non-breaking="">None = 0,</span>
	<span class="added added-field " data-is-non-breaking="">Reverse = -1,</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequestDirection -->
<div> <!-- start type AVSampleBufferRequestMode -->
<h3>New Type MonoMac.AVFoundation.AVSampleBufferRequestMode</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum AVSampleBufferRequestMode {
	<span class="added added-field " data-is-non-breaking="">Immediate = 0,</span>
	<span class="added added-field " data-is-non-breaking="">Scheduled = 1,</span>
}
</pre>
</div> <!-- end type AVSampleBufferRequestMode -->
<div> <!-- start type AVSampleCursor -->
<h3>New Type MonoMac.AVFoundation.AVSampleCursor</h3>
<pre class="added" data-is-non-breaking="">public class AVSampleCursor : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleCursor (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleCursor (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public AVSampleCursor (IntPtr handle);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursorChunkInfo CurrentChunkInfo { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursorStorageRange CurrentChunkStorageRange { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.Foundation.NSUrl CurrentChunkStorageUrl { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursorSyncInfo CurrentSampleDependencyInfo { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime CurrentSampleDuration { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual long CurrentSampleIndexInChunk { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursorStorageRange CurrentSampleStorageRange { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual AVSampleCursorSyncInfo CurrentSampleSyncInfo { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime DecodeTimeStamp { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime PresentationTimeStamp { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual int SamplesRequiredForDecoderRefresh { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.Foundation.NSComparisonResult ComparePositionInDecodeOrder (AVSampleCursor positionOfCursor);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMFormatDescription CopyCurrentSampleFormatDescription ();</span>
	<span class="added added-method " data-is-non-breaking="">public virtual bool SamplesWithEarlierDecodeTimeStampsMayHaveLaterPresentationTimeStampsThan (AVSampleCursor positionOfCursor);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual bool SamplesWithLaterDecodeTimeStampsMayHaveEarlierPresentationTimeStampsThan (AVSampleCursor positionOfCursor);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime StepByDecodeTime (MonoMac.CoreMedia.CMTime deltaDecodeTime, bool wasPinned);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual MonoMac.CoreMedia.CMTime StepByPresentationTime (MonoMac.CoreMedia.CMTime deltaPresentationTime, bool wasPinned);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual long StepInDecodeOrder (long stepCount);</span>
	<span class="added added-method " data-is-non-breaking="">public virtual long StepInPresentationOrder (long stepCount);</span>
}
</pre>
</div> <!-- end type AVSampleCursor -->
<div> <!-- start type AVSampleCursorChunkInfo -->
<h3>New Type MonoMac.AVFoundation.AVSampleCursorChunkInfo</h3>
<pre class="added" data-is-non-breaking="">public struct AVSampleCursorChunkInfo {
	// fields
	<span class="added added-field " data-is-non-breaking="">public bool HasUniformFormatDescriptions;</span>
	<span class="added added-field " data-is-non-breaking="">public bool HasUniformSampleDurations;</span>
	<span class="added added-field " data-is-non-breaking="">public bool HasUniformSampleSizes;</span>
	<span class="added added-field " data-is-non-breaking="">public long SampleCount;</span>
}
</pre>
</div> <!-- end type AVSampleCursorChunkInfo -->
<div> <!-- start type AVSampleCursorDependencyInfo -->
<h3>New Type MonoMac.AVFoundation.AVSampleCursorDependencyInfo</h3>
<pre class="added" data-is-non-breaking="">public struct AVSampleCursorDependencyInfo {
	// fields
	<span class="added added-field " data-is-non-breaking="">public bool DependsOnOthers;</span>
	<span class="added added-field " data-is-non-breaking="">public bool HasDependentSamples;</span>
	<span class="added added-field " data-is-non-breaking="">public bool HasRedundantCoding;</span>
	<span class="added added-field " data-is-non-breaking="">public bool IndicatesWhetherItDependsOnOthers;</span>
	<span class="added added-field " data-is-non-breaking="">public bool IndicatesWhetherItHasDependentSamples;</span>
	<span class="added added-field " data-is-non-breaking="">public bool IndicatesWhetherItHasRedundantCoding;</span>
}
</pre>
</div> <!-- end type AVSampleCursorDependencyInfo -->
<div> <!-- start type AVSampleCursorStorageRange -->
<h3>New Type MonoMac.AVFoundation.AVSampleCursorStorageRange</h3>
<pre class="added" data-is-non-breaking="">public struct AVSampleCursorStorageRange {
	// fields
	<span class="added added-field " data-is-non-breaking="">public long Length;</span>
	<span class="added added-field " data-is-non-breaking="">public long Offset;</span>
}
</pre>
</div> <!-- end type AVSampleCursorStorageRange -->
<div> <!-- start type AVSampleCursorSyncInfo -->
<h3>New Type MonoMac.AVFoundation.AVSampleCursorSyncInfo</h3>
<pre class="added" data-is-non-breaking="">public struct AVSampleCursorSyncInfo {
	// fields
	<span class="added added-field " data-is-non-breaking="">public bool IsDroppable;</span>
	<span class="added added-field " data-is-non-breaking="">public bool IsFullSync;</span>
	<span class="added added-field " data-is-non-breaking="">public bool IsPartialSync;</span>
}
</pre>
</div> <!-- end type AVSampleCursorSyncInfo -->
<div> <!-- start type IAVCaptureFileOutputDelegate -->
<h3>New Type MonoMac.AVFoundation.IAVCaptureFileOutputDelegate</h3>
<pre class="added" data-is-non-breaking="">public interface IAVCaptureFileOutputDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class="added added-method " data-is-non-breaking="">public virtual bool ShouldProvideSampleAccurateRecordingStart (AVCaptureOutput captureOutput);</span>
}
</pre>
</div> <!-- end type IAVCaptureFileOutputDelegate -->

</div> <!-- end namespace MonoMac.AVFoundation -->
<!-- start namespace MonoMac.AVKit --> <div> 
<h2>Namespace MonoMac.AVKit</h2>
<div> <!-- start type AVCaptureViewControlsStyle -->
<h3>New Type MonoMac.AVKit.AVCaptureViewControlsStyle</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum AVCaptureViewControlsStyle {
	<span class="added added-field " data-is-non-breaking="">Default = 0,</span>
	<span class="added added-field " data-is-non-breaking="">Floating = 1,</span>
	<span class="added added-field " data-is-non-breaking="">Inline = 0,</span>
	<span class="added added-field " data-is-non-breaking="">InlineDeviceSelection = 2,</span>
}
</pre>
</div> <!-- end type AVCaptureViewControlsStyle -->
<div> <!-- start type AVPlayerViewTrimResult -->
<h3>New Type MonoMac.AVKit.AVPlayerViewTrimResult</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum AVPlayerViewTrimResult {
	<span class="added added-field " data-is-non-breaking="">CancelButton = 1,</span>
	<span class="added added-field " data-is-non-breaking="">OKButton = 0,</span>
}
</pre>
</div> <!-- end type AVPlayerViewTrimResult -->

</div> <!-- end namespace MonoMac.AVKit -->
<!-- start namespace MonoMac.AppKit --> <div> 
<h2>Namespace MonoMac.AppKit</h2>
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAnimation --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAnimation</h3>
<!-- start type NSAnimation.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSAnimation.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveProgressMark (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSAnimationProgressMarkEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSAnimation.Notifications -->

</div> <!-- end type NSAnimation -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: MonoMac.AppKit.NSApplication</h3>
<div>
<p>Added field:</p>
<pre>	<span class="added added-field " data-is-non-breaking="">public static bool IgnoreMissingAssembliesDuringRegistration;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSApplication.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSApplication.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidBecomeActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeScreenParameters (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidFinishLaunching (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSApplicationDidFinishLaunchingEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidFinishRestoringWindows (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidHide (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidResignActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidUnhide (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidUpdate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillBecomeActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillFinishLaunching (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillHide (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillResignActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillTerminate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillUnhide (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillUpdate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSApplication.Notifications -->

</div> <!-- end type NSApplication -->
<!-- start type NSBrowser --> <div>
<h3>Type Changed: MonoMac.AppKit.NSBrowser</h3>
<!-- start type NSBrowser.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSBrowser.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColumnConfigurationChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSBrowser.Notifications -->

</div> <!-- end type NSBrowser -->
<!-- start type NSCell --> <div>
<h3>Type Changed: MonoMac.AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSCell.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSCell.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveControlTintChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSCell.Notifications -->

</div> <!-- end type NSCell -->
<!-- start type NSColor --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColor</h3>
<!-- start type NSColor.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColor.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSystemColorsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSColor.Notifications -->

</div> <!-- end type NSColor -->
<!-- start type NSColorPanel --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColorPanel</h3>
<!-- start type NSColorPanel.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSColorPanel.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColorChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSColorPanel.Notifications -->

</div> <!-- end type NSColorPanel -->
<!-- start type NSComboBox --> <div>
<h3>Type Changed: MonoMac.AppKit.NSComboBox</h3>
<!-- start type NSComboBox.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSComboBox.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillDismiss (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillPopUp (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSComboBox.Notifications -->

</div> <!-- end type NSComboBox -->
<!-- start type NSControl --> <div>
<h3>Type Changed: MonoMac.AppKit.NSControl</h3>
<!-- start type NSControl.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSControl.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTextDidBeginEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTextDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTextDidEndEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSControlTextEditingEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSControl.Notifications -->

</div> <!-- end type NSControl -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: MonoMac.AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSDrawer.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSDrawer.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidClose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidOpen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillClose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillOpen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSDrawer.Notifications -->

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFont</h3>
<!-- start type NSFont.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFont.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAntialiasThresholdChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFontSetChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFont.Notifications -->

</div> <!-- end type NSFont -->
<!-- start type NSFontCollection --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFontCollection</h3>
<!-- start type NSFontCollection.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSFontCollection.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSFontCollectionChangedEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFontCollection.Notifications -->

</div> <!-- end type NSFontCollection -->
<!-- start type NSHelpManager --> <div>
<h3>Type Changed: MonoMac.AppKit.NSHelpManager</h3>
<!-- start type NSHelpManager.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSHelpManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveContextHelpModeDidActivate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveContextHelpModeDidDeactivate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSHelpManager.Notifications -->

</div> <!-- end type NSHelpManager -->
<!-- start type NSImageRep --> <div>
<h3>Type Changed: MonoMac.AppKit.NSImageRep</h3>
<!-- start type NSImageRep.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSImageRep.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRegistryDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSImageRep.Notifications -->

</div> <!-- end type NSImageRep -->
<!-- start type NSLayoutConstraint --> <div>
<h3>Type Changed: MonoMac.AppKit.NSLayoutConstraint</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLayoutConstraint -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: MonoMac.AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSMenu.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSMenu.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidAddItem (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidBeginTracking (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeItem (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndTracking (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidRemoveItem (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemIndexEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidSendAction (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillSendAction (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSMenuItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSMenu.Notifications -->

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: MonoMac.AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOutlineView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSOutlineView</h3>
<!-- start type NSOutlineView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSOutlineView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColumnDidMove (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColumnDidResize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveItemDidCollapse (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveItemDidExpand (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveItemWillCollapse (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveItemWillExpand (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSOutlineViewItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSOutlineView.Notifications -->

</div> <!-- end type NSOutlineView -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButton</h3>
<!-- start type NSPopUpButton.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButton.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillPopUp (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton.Notifications -->

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopUpButtonCell --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButtonCell</h3>
<!-- start type NSPopUpButtonCell.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopUpButtonCell.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillPopUp (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopUpButtonCell.Notifications -->

</div> <!-- end type NSPopUpButtonCell -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopover</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSPopover.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPopover.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidClose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidShow (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillClose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPopoverCloseEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillShow (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPopover.Notifications -->

</div> <!-- end type NSPopover -->
<!-- start type NSPrintInfo --> <div>
<h3>Type Changed: MonoMac.AppKit.NSPrintInfo</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public MonoMac.PrintCore.PMPageFormat GetPageFormat ();</span>
	<span class="added added-method " data-is-non-breaking="">public MonoMac.PrintCore.PMPrintSession GetPrintSession ();</span>
	<span class="added added-method " data-is-non-breaking="">public MonoMac.PrintCore.PMPrintSettings GetPrintSettings ();</span>
</pre>
</div>

</div> <!-- end type NSPrintInfo -->
<!-- start type NSRuleEditor --> <div>
<h3>Type Changed: MonoMac.AppKit.NSRuleEditor</h3>
<!-- start type NSRuleEditor.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSRuleEditor.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSRuleEditor.Notifications -->

</div> <!-- end type NSRuleEditor -->
<!-- start type NSScreen --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScreen</h3>
<!-- start type NSScreen.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScreen.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColorSpaceDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScreen.Notifications -->

</div> <!-- end type NSScreen -->
<!-- start type NSScrollView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScrollView</h3>
<!-- start type NSScrollView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScrollView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndLiveMagnify (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndLiveScroll (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidLiveScroll (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillStartLiveMagnify (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScrollView.Notifications -->

</div> <!-- end type NSScrollView -->
<!-- start type NSScroller --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScroller</h3>
<!-- start type NSScroller.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSScroller.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObservePreferredStyleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSScroller.Notifications -->

</div> <!-- end type NSScroller -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSpellChecker --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSpellChecker</h3>
<!-- start type NSSpellChecker.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSpellChecker.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticCapitalization (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticPeriodSubstitution (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticSpellingCorrection (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticTextCompletion (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeAutomaticTextReplacement (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSSpellChecker.Notifications -->

</div> <!-- end type NSSpellChecker -->
<!-- start type NSSplitView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSplitView</h3>
<!-- start type NSSplitView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSSplitView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNSSplitViewDidResizeSubviews (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNSSplitViewWillResizeSubviews (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSSplitViewDividerIndexEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSSplitView.Notifications -->

</div> <!-- end type NSSplitView -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTableView</h3>
<!-- start type NSTableView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTableView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColumnDidMove (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnMoveEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveColumnDidResize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSViewColumnResizeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionIsChanging (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTableView.Notifications -->

</div> <!-- end type NSTableView -->
<!-- start type NSText --> <div>
<h3>Type Changed: MonoMac.AppKit.NSText</h3>
<!-- start type NSText.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSText.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidBeginEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextDidEndEditingEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSText.Notifications -->

</div> <!-- end type NSText -->
<!-- start type NSTextAlternatives --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextAlternatives</h3>
<!-- start type NSTextAlternatives.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextAlternatives.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedAlternativeString (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextAlternativesSelectedAlternativeStringEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextAlternatives.Notifications -->

</div> <!-- end type NSTextAlternatives -->
<!-- start type NSTextContainer --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextContainer</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSTextContainer -->
<!-- start type NSTextInputContext --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextInputContext</h3>
<!-- start type NSTextInputContext.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextInputContext.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveKeyboardSelectionDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextInputContext.Notifications -->

</div> <!-- end type NSTextInputContext -->
<!-- start type NSTextStorage --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextStorage</h3>
<!-- start type NSTextStorage.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextStorage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidProcessEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillProcessEditing (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextStorage.Notifications -->

</div> <!-- end type NSTextStorage -->
<!-- start type NSTextView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextView</h3>
<!-- start type NSTextView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTextView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeSelection (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextViewDidChangeSelectionEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeTypingAttributes (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillChangeNotifyingTextView (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSTextViewWillChangeNotifyingTextViewEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextView.Notifications -->

</div> <!-- end type NSTextView -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: MonoMac.AppKit.NSToolbar</h3>
<!-- start type NSToolbar.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSToolbar.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNSToolbarDidRemoveItem (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSToolbarItemEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveNSToolbarWillAddItem (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSToolbarItemEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSToolbar.Notifications -->

</div> <!-- end type NSToolbar -->
<!-- start type NSTouch --> <div>
<h3>Type Changed: MonoMac.AppKit.NSTouch</h3>
<p>Obsoleted constructors:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-constructor" data-is-non-breaking="">[Obsolete ("This type is not meant to be user-created")]
	public NSTouch ();</span>
</div></pre>

</div> <!-- end type NSTouch -->
<!-- start type NSView --> <div>
<h3>Type Changed: MonoMac.AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSView.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveBoundsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFrameChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveGlobalFrameChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUpdatedTrackingAreas (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSView.Notifications -->

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString AnnouncementRequestedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationActivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationDeactivatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationHiddenNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ApplicationShownNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString CreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DrawerCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString FocusedWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString HelpTagCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString LayoutChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MainWindowChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString MovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ResizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCollapsedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowCountChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString RowExpandedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedCellsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedChildrenMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedColumnsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedRowsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SelectedTextChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString SheetCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString TitleChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementDestroyedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UIElementFocusedChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString UnitsChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString ValueChangedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowCreatedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowDeminiaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMiniaturizedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowMovedNotification { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString WindowResizedNotification { get; }</span>
</pre>
</div>
<!-- start type NSWindow.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWindow.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnouncementRequested (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationActivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationDeactivated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationHidden (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveApplicationShown (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidBecomeKey (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidBecomeMain (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeBackingProperties (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWindowBackingPropertiesEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeScreen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeScreenProfile (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidDeminiaturize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndLiveResize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEndSheet (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEnterFullScreen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidEnterVersionBrowser (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidExitFullScreen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidExitVersionBrowser (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidExpose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWindowExposeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidMiniaturize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidMove (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidResignKey (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidResignMain (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidResize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidUpdate (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDrawerCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveFocusedWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveHelpTagCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveLayoutChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMainWindowChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCollapsed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowCountChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveRowExpanded (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedCellsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedChildrenMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedColumnsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedRowsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectedTextChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSheetCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveTitleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementDestroyed (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUIElementFocusedChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveUnitsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveValueChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillBeginSheet (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillClose (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillEnterFullScreen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillEnterVersionBrowser (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillExitFullScreen (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillExitVersionBrowser (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillMiniaturize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillMove (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillStartLiveResize (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowCreated (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowDeminiaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMiniaturized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowMoved (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWindowResized (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSWindow.Notifications -->

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWorkspace</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static MonoMac.Foundation.NSString DisplayOptionsDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type NSWorkspace.Notifications --> <div>
<h3>Type Changed: MonoMac.AppKit.NSWorkspace.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveActiveSpaceDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidActivateApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeFileLabels (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidDeactivateApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidHideApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidLaunchApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidMount (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidPerformFileOperation (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceFileOperationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidRenameVolume (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceRenamedEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidTerminateApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidUnhideApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidUnmount (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidWake (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDisplayOptionsDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDisplayOptionsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveScreensDidSleep (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveScreensDidWake (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSessionDidBecomeActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSessionDidResignActive (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillLaunchApplication (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceApplicationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillPowerOff (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillSleep (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillUnmount (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSWorkspaceMountEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSWorkspace.Notifications -->

</div> <!-- end type NSWorkspace -->
<div> <!-- start type NSToolbarItemGroup -->
<h3>New Type MonoMac.AppKit.NSToolbarItemGroup</h3>
<pre class="added" data-is-non-breaking="">public class NSToolbarItemGroup : MonoMac.AppKit.NSToolbarItem, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public NSToolbarItemGroup ();</span>
	<span class="added added-constructor " data-is-non-breaking="">public NSToolbarItemGroup (MonoMac.Foundation.NSCoder coder);</span>
	<span class="added added-constructor " data-is-non-breaking="">public NSToolbarItemGroup (MonoMac.Foundation.NSObjectFlag t);</span>
	<span class="added added-constructor " data-is-non-breaking="">public NSToolbarItemGroup (IntPtr handle);</span>
	<span class="added added-constructor " data-is-non-breaking="">public NSToolbarItemGroup (string itemIdentifier);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public virtual NSToolbarItem[] Subitems { get; set; }</span>
}
</pre>
</div> <!-- end type NSToolbarItemGroup -->

</div> <!-- end namespace MonoMac.AppKit -->
<!-- start namespace MonoMac.CoreAnimation --> <div> 
<h2>Namespace MonoMac.CoreAnimation</h2>
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: MonoMac.CoreAnimation.CAScrollLayer</h3>
<p>Obsoleted properties:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-property" data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static MonoMac.Foundation.NSString ScrollBoth { get; }</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-property" data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static MonoMac.Foundation.NSString ScrollHorizontally { get; }</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-property" data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static MonoMac.Foundation.NSString ScrollNone { get; }</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-property" data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static MonoMac.Foundation.NSString ScrollVertically { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public CAScroll Scroll { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<div> <!-- start type CAScroll -->
<h3>New Type MonoMac.CoreAnimation.CAScroll</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum CAScroll {
	<span class="added added-field " data-is-non-breaking="">Both = 3,</span>
	<span class="added added-field " data-is-non-breaking="">Horizontally = 2,</span>
	<span class="added added-field " data-is-non-breaking="">None = 0,</span>
	<span class="added added-field " data-is-non-breaking="">Vertically = 1,</span>
}
</pre>
</div> <!-- end type CAScroll -->
<div> <!-- start type CAScrollExtensions -->
<h3>New Type MonoMac.CoreAnimation.CAScrollExtensions</h3>
<pre class="added" data-is-non-breaking="">public static class CAScrollExtensions {
	// methods
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSString GetConstant (CAScroll self);</span>
	<span class="added added-method " data-is-non-breaking="">public static CAScroll GetValue (MonoMac.Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CAScrollExtensions -->

</div> <!-- end namespace MonoMac.CoreAnimation -->
<!-- start namespace MonoMac.CoreData --> <div> 
<h2>Namespace MonoMac.CoreData</h2>
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: MonoMac.CoreData.NSManagedObjectContext</h3>
<!-- start type NSManagedObjectContext.Notifications --> <div>
<h3>Type Changed: MonoMac.CoreData.NSManagedObjectContext.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidSave (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveObjectsDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillSave (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext.Notifications -->

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator</h3>
<!-- start type NSPersistentStoreCoordinator.Notifications --> <div>
<h3>Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidImportUbiquitousContentChanges (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveStoresDidChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveStoresWillChange (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPersistentStoreCoordinatorStoreChangeEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveWillRemoveStore (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator.Notifications -->

</div> <!-- end type NSPersistentStoreCoordinator -->

</div> <!-- end namespace MonoMac.CoreData -->
<!-- start namespace MonoMac.CoreGraphics --> <div> 
<h2>Namespace MonoMac.CoreGraphics</h2>
<div> <!-- start type CGCaptureOptions -->
<h3>New Type MonoMac.CoreGraphics.CGCaptureOptions</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum CGCaptureOptions {
	<span class="added added-field " data-is-non-breaking="">NoFill = 1,</span>
	<span class="added added-field " data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CGCaptureOptions -->
<div> <!-- start type CGDisplay -->
<h3>New Type MonoMac.CoreGraphics.CGDisplay</h3>
<pre class="added" data-is-non-breaking="">public static class CGDisplay {
	// properties
	<span class="added added-property " data-is-non-breaking="">public static int MainDisplayID { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public static int ShieldingWindowLevel { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public static int Capture (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int Capture (int display, CGCaptureOptions options);</span>
	<span class="added added-method " data-is-non-breaking="">public static int CaptureAllDisplays ();</span>
	<span class="added added-method " data-is-non-breaking="">public static System.Drawing.RectangleF GetBounds (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetDisplayID (int displayMask);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetGammaTableCapacity (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetHeight (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetOpenGLDisplayMask (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetShieldingWindowID (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetTypeID ();</span>
	<span class="added added-method " data-is-non-breaking="">public static int GetWidth (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int HideCursor (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static bool IsCaptured (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int MoveCursor (int display, System.Drawing.PointF point);</span>
	<span class="added added-method " data-is-non-breaking="">public static int Release (int display);</span>
	<span class="added added-method " data-is-non-breaking="">public static int ReleaseAllDisplays ();</span>
	<span class="added added-method " data-is-non-breaking="">public static void RestoreColorSyncSettings ();</span>
	<span class="added added-method " data-is-non-breaking="">public static int SetDisplayTransfer (int display, float redMin, float redMax, float redGamma, float greenMin, float greenMax, float greenGamma, float blueMin, float blueMax, float blueGamma);</span>
	<span class="added added-method " data-is-non-breaking="">public static int ShowCursor (int display);</span>
}
</pre>
</div> <!-- end type CGDisplay -->

</div> <!-- end namespace MonoMac.CoreGraphics -->
<!-- start namespace MonoMac.CoreMidi --> <div> 
<h2>Namespace MonoMac.CoreMidi</h2>
<!-- start type MidiObject --> <div>
<h3>Type Changed: MonoMac.CoreMidi.MidiObject</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MidiError FindByUniqueId (int uniqueId, MidiObject result);</span>
</pre>
</div>

</div> <!-- end type MidiObject -->

</div> <!-- end namespace MonoMac.CoreMidi -->
<!-- start namespace MonoMac.Foundation --> <div> 
<h2>Namespace MonoMac.Foundation</h2>
<!-- start type NSArray --> <div>
<h3>Type Changed: MonoMac.Foundation.NSArray</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSArray FromNSObjects&lt;T&gt; (System.Func&lt;T,MonoMac.Foundation.NSObject&gt; nsobjectificator, T[] items);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSCalendar --> <div>
<h3>Type Changed: MonoMac.Foundation.NSCalendar</h3>
<!-- start type NSCalendar.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSCalendar.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDayChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSCalendar.Notifications -->

</div> <!-- end type NSCalendar -->
<!-- start type NSFileCoordinator --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileCoordinator</h3>
<p>Obsoleted constructors:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-constructor" data-is-non-breaking="">[Obsolete ("Use .ctor(INSFilePresenter) instead")]
	public NSFileCoordinator (NSFilePresenter filePresenterOrNil);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>	<span class="added added-constructor " data-is-non-breaking="">public NSFileCoordinator (INSFilePresenter filePresenterOrNil);</span>
</pre>
</div>

</div> <!-- end type NSFileCoordinator -->
<!-- start type NSFileHandle --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileHandle</h3>
<!-- start type NSFileHandle.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileHandle.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveConnectionAccepted (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleConnectionAcceptedEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDataAvailable (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveReadCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveReadToEndOfFileCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileHandle.Notifications -->

</div> <!-- end type NSFileHandle -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileManager</h3>
<!-- start type NSFileManager.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFileManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveUbiquityIdentityDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileManager.Notifications -->

</div> <!-- end type NSFileManager -->
<!-- start type NSFormatter --> <div>
<h3>Type Changed: MonoMac.Foundation.NSFormatter</h3>
<p>Obsoleted methods:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use IsPartialStringValid (ref string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out string error) instead")]
	public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, NSString error);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, string error);</span>
</pre>
</div>

</div> <!-- end type NSFormatter -->
<!-- start type NSLocale --> <div>
<h3>Type Changed: MonoMac.Foundation.NSLocale</h3>
<!-- start type NSLocale.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSLocale.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveCurrentLocaleDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSLocale.Notifications -->

</div> <!-- end type NSLocale -->
<!-- start type NSMetadataQuery --> <div>
<h3>Type Changed: MonoMac.Foundation.NSMetadataQuery</h3>
<!-- start type NSMetadataQuery.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSMetadataQuery.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidFinishGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidStartGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidUpdate (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveGatheringProgress (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSMetadataQuery.Notifications -->

</div> <!-- end type NSMetadataQuery -->
<!-- start type NSObject --> <div>
<h3>Type Changed: MonoMac.Foundation.NSObject</h3>
<p>Obsoleted methods:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use Bind (NSString binding, NSObject observable, string keyPath, [NullAllowed] NSDictionary options) instead")]
	public virtual void Bind (string binding, NSObject observable, string keyPath, NSDictionary options);</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use GetBindingInfo (NSString binding) instead")]
	public virtual NSDictionary BindingInfo (string binding);</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use GetBindingOptionDescriptions (NSString aBinding) instead")]
	public virtual NSObject[] BindingOptionDescriptions (string aBinding);</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use GetBindingValueClass (NSString binding) instead")]
	public virtual MonoMac.ObjCRuntime.Class BindingValueClass (string binding);</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use SetDefaultPlaceholder (NSObject placeholder, NSObject marker, NSString binding) instead")]
	public static void SetDefaultPlaceholder (NSObject placeholder, NSObject marker, string binding);</span>
</div><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use Unbind (NSString binding) instead")]
	public virtual void Unbind (string binding);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public void Bind (NSString binding, NSObject observable, string keyPath, NSDictionary options);</span>
	<span class="added added-method " data-is-non-breaking="">public NSDictionary GetBindingInfo (NSString binding);</span>
	<span class="added added-method " data-is-non-breaking="">public NSObject[] GetBindingOptionDescriptions (NSString aBinding);</span>
	<span class="added added-method " data-is-non-breaking="">public MonoMac.ObjCRuntime.Class GetBindingValueClass (NSString binding);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject GetDefaultPlaceholder (NSObject marker, NSString binding);</span>
	<span class="added added-method " data-is-non-breaking="">public static void SetDefaultPlaceholder (NSObject placeholder, NSObject marker, NSString binding);</span>
	<span class="added added-method " data-is-non-breaking="">public void Unbind (NSString binding);</span>
</pre>
</div>

</div> <!-- end type NSObject -->
<!-- start type NSProcessInfo --> <div>
<h3>Type Changed: MonoMac.Foundation.NSProcessInfo</h3>
<!-- start type NSProcessInfo.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSProcessInfo.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveThermalStateDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSProcessInfo.Notifications -->

</div> <!-- end type NSProcessInfo -->
<!-- start type NSString --> <div>
<h3>Type Changed: MonoMac.Foundation.NSString</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public bool IsEqualTo (IntPtr handle);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSTask --> <div>
<h3>Type Changed: MonoMac.Foundation.NSTask</h3>
<div>
<p>Added property:</p>
<pre>	<span class="added added-property " data-is-non-breaking="">public static NSString DidTerminateNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSTask -->
<!-- start type NSUbiquitousKeyValueStore --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUbiquitousKeyValueStore</h3>
<!-- start type NSUbiquitousKeyValueStore.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUbiquitousKeyValueStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidChangeExternally (NSObject objectToObserve, System.EventHandler&lt;NSUbiquitousKeyValueStoreChangeEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUbiquitousKeyValueStore.Notifications -->

</div> <!-- end type NSUbiquitousKeyValueStore -->
<!-- start type NSUndoManager --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUndoManager</h3>
<!-- start type NSUndoManager.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUndoManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveCheckpoint (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidOpenUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveWillCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveWillRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveWillUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUndoManager.Notifications -->

</div> <!-- end type NSUndoManager -->
<!-- start type NSUrlCredentialStorage --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUrlCredentialStorage</h3>
<!-- start type NSUrlCredentialStorage.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUrlCredentialStorage.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUrlCredentialStorage.Notifications -->

</div> <!-- end type NSUrlCredentialStorage -->
<!-- start type NSUrlSession --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUrlSession</h3>
<p>Obsoleted methods:</p>
<pre><div data-is-non-breaking="">	<span class="obsolete obsolete-method" data-is-non-breaking="">[Obsolete ("Use the overload with a `INSUrlSessionDelegate` parameter.")]
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, INSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</pre>
</div>

</div> <!-- end type NSUrlSession -->
<!-- start type NSUserDefaults --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUserDefaults</h3>
<!-- start type NSUserDefaults.Notifications --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUserDefaults.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static NSObject ObserveDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUserDefaults.Notifications -->

</div> <!-- end type NSUserDefaults -->
<!-- start type NSUserNotificationActivationType --> <div>
<h3>Type Changed: MonoMac.Foundation.NSUserNotificationActivationType</h3>
<div>
<p>Added values:</p>
<pre class="added" data-is-non-breaking="">	<span class="added added-field " data-is-non-breaking="">AdditionalActionClicked = 4,</span>
	<span class="added added-field " data-is-non-breaking="">Replied = 3,</span>
</pre>
</div>

</div> <!-- end type NSUserNotificationActivationType -->
<div> <!-- start type NSStringTransformExtensions -->
<h3>New Type MonoMac.Foundation.NSStringTransformExtensions</h3>
<pre class="added" data-is-non-breaking="">public static class NSStringTransformExtensions {
	// methods
	<span class="added added-method " data-is-non-breaking="">public static NSString GetConstant (NSStringTransform self);</span>
	<span class="added added-method " data-is-non-breaking="">public static NSStringTransform GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSStringTransformExtensions -->

</div> <!-- end namespace MonoMac.Foundation -->
<!-- start namespace MonoMac.GameKit --> <div> 
<h2>Namespace MonoMac.GameKit</h2>
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: MonoMac.GameKit.GKLocalPlayer</h3>
<!-- start type GKLocalPlayer.Notifications --> <div>
<h3>Type Changed: MonoMac.GameKit.GKLocalPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAuthenticationDidChangeNotificationName (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer.Notifications -->

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: MonoMac.GameKit.GKPlayer</h3>
<!-- start type GKPlayer.Notifications --> <div>
<h3>Type Changed: MonoMac.GameKit.GKPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDidChangeNotificationName (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKPlayer.Notifications -->

</div> <!-- end type GKPlayer -->

</div> <!-- end namespace MonoMac.GameKit -->
<!-- start namespace MonoMac.MediaAccessibility --> <div> 
<h2>Namespace MonoMac.MediaAccessibility</h2>
<!-- start type MAAudibleMedia --> <div>
<h3>Type Changed: MonoMac.MediaAccessibility.MAAudibleMedia</h3>
<!-- start type MAAudibleMedia.Notifications --> <div>
<h3>Type Changed: MonoMac.MediaAccessibility.MAAudibleMedia.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSettingsChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MAAudibleMedia.Notifications -->

</div> <!-- end type MAAudibleMedia -->

</div> <!-- end namespace MonoMac.MediaAccessibility -->
<!-- start namespace MonoMac.ObjCRuntime --> <div> 
<h2>Namespace MonoMac.ObjCRuntime</h2>
<!-- start type Dlfcn --> <div>
<h3>Type Changed: MonoMac.ObjCRuntime.Dlfcn</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static IntPtr CachePointer (IntPtr handle, string constant, IntPtr* storage);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<!-- start type Messaging --> <div>
<h3>Type Changed: MonoMac.ObjCRuntime.Messaging</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorChunkInfo AVSampleCursorChunkInfo_objc_msgSend (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorChunkInfo AVSampleCursorChunkInfo_objc_msgSendSuper (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorChunkInfo_objc_msgSendSuper_stret (MonoMac.AVFoundation.AVSampleCursorChunkInfo retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorChunkInfo_objc_msgSend_stret (MonoMac.AVFoundation.AVSampleCursorChunkInfo retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorStorageRange AVSampleCursorStorageRange_objc_msgSend (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorStorageRange AVSampleCursorStorageRange_objc_msgSendSuper (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorStorageRange_objc_msgSendSuper_stret (MonoMac.AVFoundation.AVSampleCursorStorageRange retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorStorageRange_objc_msgSend_stret (MonoMac.AVFoundation.AVSampleCursorStorageRange retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorSyncInfo AVSampleCursorSyncInfo_objc_msgSend (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.AVFoundation.AVSampleCursorSyncInfo AVSampleCursorSyncInfo_objc_msgSendSuper (IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorSyncInfo_objc_msgSendSuper_stret (MonoMac.AVFoundation.AVSampleCursorSyncInfo retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static void AVSampleCursorSyncInfo_objc_msgSend_stret (MonoMac.AVFoundation.AVSampleCursorSyncInfo retval, IntPtr receiver, IntPtr selector);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.CoreMedia.CMTime CMTime_objc_msgSendSuper_CMTime_out_Boolean (IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTime arg1, bool arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static void CMTime_objc_msgSendSuper_stret_CMTime_out_Boolean (MonoMac.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTime arg1, bool arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.CoreMedia.CMTime CMTime_objc_msgSend_CMTime_out_Boolean (IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTime arg1, bool arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static void CMTime_objc_msgSend_stret_CMTime_out_Boolean (MonoMac.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTime arg1, bool arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static long Int64_objc_msgSendSuper_Int64 (IntPtr receiver, IntPtr selector, long arg1);</span>
	<span class="added added-method " data-is-non-breaking="">public static long Int64_objc_msgSend_Int64 (IntPtr receiver, IntPtr selector, long arg1);</span>
	<span class="added added-method " data-is-non-breaking="">public static bool bool_objc_msgSendSuper_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, MonoMac.CoreMedia.CMTimeRange arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static bool bool_objc_msgSendSuper_IntPtr_out_CMTime_out_CMTime_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.CoreMedia.CMTime arg2, MonoMac.CoreMedia.CMTime arg3, IntPtr arg4);</span>
	<span class="added added-method " data-is-non-breaking="">public static bool bool_objc_msgSend_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, MonoMac.CoreMedia.CMTimeRange arg2);</span>
	<span class="added added-method " data-is-non-breaking="">public static bool bool_objc_msgSend_IntPtr_out_CMTime_out_CMTime_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.CoreMedia.CMTime arg2, MonoMac.CoreMedia.CMTime arg3, IntPtr arg4);</span>
</pre>
</div>

</div> <!-- end type Messaging -->

</div> <!-- end namespace MonoMac.ObjCRuntime -->
<!-- start namespace MonoMac.PdfKit --> <div> 
<h2>Namespace MonoMac.PdfKit</h2>
<!-- start type PdfView --> <div>
<h3>Type Changed: MonoMac.PdfKit.PdfView</h3>
<!-- start type PdfView.Notifications --> <div>
<h3>Type Changed: MonoMac.PdfKit.PdfView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnotationHit (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;PdfViewAnnotationHitEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveAnnotationWillHit (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveChangedHistory (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveCopyPermission (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDisplayBoxChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDisplayModeChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveDocumentChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObservePageChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveScaleChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveSelectionChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type PdfView.Notifications -->

</div> <!-- end type PdfView -->

</div> <!-- end namespace MonoMac.PdfKit -->
<!-- start namespace MonoMac.SceneKit --> <div> 
<h2>Namespace MonoMac.SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNLayer</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (MonoMac.Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (MonoMac.Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNSceneRenderer</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (MonoMac.Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->
<!-- start type SCNSceneRenderer_Extensions --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNSceneRenderer_Extensions</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (ISCNSceneRenderer This, MonoMac.Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer_Extensions -->
<!-- start type SCNView --> <div>
<h3>Type Changed: MonoMac.SceneKit.SCNView</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (MonoMac.Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNView -->

</div> <!-- end namespace MonoMac.SceneKit -->
<!-- start namespace MonoMac.WebKit --> <div> 
<h2>Namespace MonoMac.WebKit</h2>
<!-- start type WebHistoryItem --> <div>
<h3>Type Changed: MonoMac.WebKit.WebHistoryItem</h3>
<!-- start type WebHistoryItem.Notifications --> <div>
<h3>Type Changed: MonoMac.WebKit.WebHistoryItem.Notifications</h3>
<div>
<p>Added method:</p>
<pre>	<span class="added added-method " data-is-non-breaking="">public static MonoMac.Foundation.NSObject ObserveChanged (MonoMac.Foundation.NSObject objectToObserve, System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WebHistoryItem.Notifications -->

</div> <!-- end type WebHistoryItem -->

</div> <!-- end namespace MonoMac.WebKit -->
<!-- start namespace MonoMac.PrintCore --> <div> 
<h2>New Namespace MonoMac.PrintCore</h2>

<div> <!-- start type PMDuplexMode -->
<h3>New Type MonoMac.PrintCore.PMDuplexMode</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum PMDuplexMode {
	<span class="added added-field " data-is-non-breaking="">NoTumble = 2,</span>
	<span class="added added-field " data-is-non-breaking="">None = 1,</span>
	<span class="added added-field " data-is-non-breaking="">SimplexTumble = 4,</span>
	<span class="added added-field " data-is-non-breaking="">Tumble = 3,</span>
}
</pre>
</div> <!-- end type PMDuplexMode -->
<div> <!-- start type PMOrientation -->
<h3>New Type MonoMac.PrintCore.PMOrientation</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum PMOrientation {
	<span class="added added-field " data-is-non-breaking="">Landscape = 2,</span>
	<span class="added added-field " data-is-non-breaking="">Portrait = 1,</span>
	<span class="added added-field " data-is-non-breaking="">ReverseLandscape = 4,</span>
	<span class="added added-field " data-is-non-breaking="">ReversePortrait = 3,</span>
}
</pre>
</div> <!-- end type PMOrientation -->
<div> <!-- start type PMPageFormat -->
<h3>New Type MonoMac.PrintCore.PMPageFormat</h3>
<pre class="added" data-is-non-breaking="">public class PMPageFormat : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPageFormat (PMPaper paper);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public PMRect AdjustedPageRect { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMRect AdjustedPaperRect { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMOrientation Orientation { get; set; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode TryCreate (PMPageFormat pageFormat, PMPaper paper);</span>
}
</pre>
</div> <!-- end type PMPageFormat -->
<div> <!-- start type PMPaper -->
<h3>New Type MonoMac.PrintCore.PMPaper</h3>
<pre class="added" data-is-non-breaking="">public class PMPaper : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class="added added-property " data-is-non-breaking="">public double Height { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public string ID { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMPaperMargins? Margins { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Width { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public string GetLocalizedName (PMPrinter printer);</span>
}
</pre>
</div> <!-- end type PMPaper -->
<div> <!-- start type PMPaperMargins -->
<h3>New Type MonoMac.PrintCore.PMPaperMargins</h3>
<pre class="added" data-is-non-breaking="">public struct PMPaperMargins {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPaperMargins (double top, double bottom, double left, double right);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public double Bottom { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Left { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Right { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Top { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMPaperMargins -->
<div> <!-- start type PMPrintCoreBase -->
<h3>New Type MonoMac.PrintCore.PMPrintCoreBase</h3>
<pre class="added" data-is-non-breaking="">public class PMPrintCoreBase : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class="added added-property " data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class="added added-method " data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class="added added-method " data-is-non-breaking="">protected override void ~PMPrintCoreBase ();</span>
}
</pre>
</div> <!-- end type PMPrintCoreBase -->
<div> <!-- start type PMPrintException -->
<h3>New Type MonoMac.PrintCore.PMPrintException</h3>
<pre class="added" data-is-non-breaking="">public class PMPrintException : System.Exception, System.Runtime.InteropServices._Exception, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPrintException (PMStatusCode code);</span>
}
</pre>
</div> <!-- end type PMPrintException -->
<div> <!-- start type PMPrintSession -->
<h3>New Type MonoMac.PrintCore.PMPrintSession</h3>
<pre class="added" data-is-non-breaking="">public class PMPrintSession : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPrintSession ();</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public PMStatusCode SessionError { get; set; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public void AssignDefaultPageFormat (PMPageFormat pageFormat);</span>
	<span class="added added-method " data-is-non-breaking="">public void AssignDefaultSettings (PMPrintSettings settings);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode CreatePrinterList (string[] printerList, int index, PMPrinter printer);</span>
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrintSession session);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode ValidatePrintSettings (PMPrintSettings settings, bool changed);</span>
}
</pre>
</div> <!-- end type PMPrintSession -->
<div> <!-- start type PMPrintSettings -->
<h3>New Type MonoMac.PrintCore.PMPrintSettings</h3>
<pre class="added" data-is-non-breaking="">public class PMPrintSettings : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPrintSettings ();</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public bool Collate { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public uint Copies { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMDuplexMode DuplexMode { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public uint FirstPage { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public uint LastPage { get; set; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Scale { get; set; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode CopySettings (PMPrintSettings destination);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode GetPageRange (uint minPage, uint maxPage);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode SetPageRange (uint minPage, uint maxPage);</span>
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrintSettings settings);</span>
}
</pre>
</div> <!-- end type PMPrintSettings -->
<div> <!-- start type PMPrinter -->
<h3>New Type MonoMac.PrintCore.PMPrinter</h3>
<pre class="added" data-is-non-breaking="">public class PMPrinter : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMPrinter ();</span>
	<span class="added added-constructor " data-is-non-breaking="">public PMPrinter (string printerId);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public MonoMac.Foundation.NSUrl DeviceUrl { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public bool IsDefault { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public bool IsFavorite { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public bool IsPostScriptCapable { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public bool IsPostScriptPrinter { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public bool IsRemote { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public string MakeAndModel { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public string Name { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMPaper[] PaperList { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public PMPrinterState PrinterState { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public PMResolution GetOutputResolution (PMPrintSettings settings);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode SetDefault ();</span>
	<span class="added added-method " data-is-non-breaking="">public void SetOutputResolution (PMPrintSettings settings, PMResolution res);</span>
	<span class="added added-method " data-is-non-breaking="">public static PMPrinter TryCreate (string printerId);</span>
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode TryCreate (PMPrinter printer);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode TryGetDeviceUrl (MonoMac.Foundation.NSUrl url);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode TryGetMimeTypes (PMPrintSettings settings, string[] mimeTypes);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode TryGetPaperList (PMPaper[] paperList);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode TryPrintFile (PMPrintSettings settings, PMPageFormat pageFormat, MonoMac.Foundation.NSUrl fileUrl, string mimeType);</span>
	<span class="added added-method " data-is-non-breaking="">public PMStatusCode TryPrintFromProvider (PMPrintSettings settings, PMPageFormat pageFormat, MonoMac.CoreGraphics.CGDataProvider provider, string mimeType);</span>
}
</pre>
</div> <!-- end type PMPrinter -->
<div> <!-- start type PMPrinterState -->
<h3>New Type MonoMac.PrintCore.PMPrinterState</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum PMPrinterState {
	<span class="added added-field " data-is-non-breaking="">Idle = 3,</span>
	<span class="added added-field " data-is-non-breaking="">Processing = 4,</span>
	<span class="added added-field " data-is-non-breaking="">Stopped = 5,</span>
}
</pre>
</div> <!-- end type PMPrinterState -->
<div> <!-- start type PMRect -->
<h3>New Type MonoMac.PrintCore.PMRect</h3>
<pre class="added" data-is-non-breaking="">public struct PMRect {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMRect (double top, double bottom, double left, double right);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public double Bottom { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Left { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Right { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double Top { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMRect -->
<div> <!-- start type PMResolution -->
<h3>New Type MonoMac.PrintCore.PMResolution</h3>
<pre class="added" data-is-non-breaking="">public struct PMResolution {
	// constructors
	<span class="added added-constructor " data-is-non-breaking="">public PMResolution (double horizontal, double vertical);</span>
	// properties
	<span class="added added-property " data-is-non-breaking="">public double HorizontalResolution { get; }</span>
	<span class="added added-property " data-is-non-breaking="">public double VerticalResolution { get; }</span>
	// methods
	<span class="added added-method " data-is-non-breaking="">public override string ToString ();</span>
}
</pre>
</div> <!-- end type PMResolution -->
<div> <!-- start type PMServer -->
<h3>New Type MonoMac.PrintCore.PMServer</h3>
<pre class="added" data-is-non-breaking="">public class PMServer : MonoMac.PrintCore.PMPrintCoreBase, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode CreatePrinterList (PMPrinter[] printerList);</span>
	<span class="added added-method " data-is-non-breaking="">public static PMStatusCode LaunchPrinterBrowser ();</span>
}
</pre>
</div> <!-- end type PMServer -->
<div> <!-- start type PMStatusCode -->
<h3>New Type MonoMac.PrintCore.PMStatusCode</h3>
<pre class="added" data-is-non-breaking="">[Serializable]
public enum PMStatusCode {
	<span class="added added-field " data-is-non-breaking="">AllocationFailure = -108,</span>
	<span class="added added-field " data-is-non-breaking="">CloseFailed = -9785,</span>
	<span class="added added-field " data-is-non-breaking="">CreateMessageFailed = -9620,</span>
	<span class="added added-field " data-is-non-breaking="">CvmSymbolNotFound = -9662,</span>
	<span class="added added-field " data-is-non-breaking="">DeleteSubTicketFailed = -9585,</span>
	<span class="added added-field " data-is-non-breaking="">DocumentNotFound = -9644,</span>
	<span class="added added-field " data-is-non-breaking="">DontSwitchPdeError = -9531,</span>
	<span class="added added-field " data-is-non-breaking="">EditRequestFailed = -9544,</span>
	<span class="added added-field " data-is-non-breaking="">FeatureNotInstalled = -9533,</span>
	<span class="added added-field " data-is-non-breaking="">FileOrDirOperationFailed = -9634,</span>
	<span class="added added-field " data-is-non-breaking="">FontNameTooLong = -9704,</span>
	<span class="added added-field " data-is-non-breaking="">FontNotFound = -9703,</span>
	<span class="added added-field " data-is-non-breaking="">GeneralCGError = -9705,</span>
	<span class="added added-field " data-is-non-breaking="">GeneralError = -30870,</span>
	<span class="added added-field " data-is-non-breaking="">IOAttrNotAvailable = -9787,</span>
	<span class="added added-field " data-is-non-breaking="">IOMSymbolNotFound = -9661,</span>
	<span class="added added-field " data-is-non-breaking="">InternalError = -30870,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidAllocator = -30890,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidCalibrationTarget = -30898,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidConnection = -30887,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidCvmContext = -9665,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidFileType = -30895,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidIOMContext = -9664,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidIndex = -30882,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidItem = -30892,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidJobID = -9666,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidJobTemplate = -30885,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidKey = -30888,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidLookupSpec = -9542,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidObject = -30896,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPMContext = -9663,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPageFormat = -30876,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPaper = -30897,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidParameter = -50,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPbmRef = -9540,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPdeContext = -9530,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPreset = -30899,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPrintSession = -30879,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPrintSettings = -30875,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPrinter = -30880,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPrinterAddress = -9780,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidPrinterInfo = -30886,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidReply = -30894,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidState = -9706,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidSubTicket = -9584,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidTicket = -30891,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidType = -30893,</span>
	<span class="added added-field " data-is-non-breaking="">InvalidValue = -30889,</span>
	<span class="added added-field " data-is-non-breaking="">ItemIsLocked = -9586,</span>
	<span class="added added-field " data-is-non-breaking="">JobBusy = -9642,</span>
	<span class="added added-field " data-is-non-breaking="">JobCanceled = -9643,</span>
	<span class="added added-field " data-is-non-breaking="">JobGetTicketBadFormatError = -9672,</span>
	<span class="added added-field " data-is-non-breaking="">JobGetTicketReadError = -9673,</span>
	<span class="added added-field " data-is-non-breaking="">JobManagerAborted = -9671,</span>
	<span class="added added-field " data-is-non-breaking="">JobNotFound = -9641,</span>
	<span class="added added-field " data-is-non-breaking="">JobStreamEndError = -9670,</span>
	<span class="added added-field " data-is-non-breaking="">JobStreamOpenFailed = -9668,</span>
	<span class="added added-field " data-is-non-breaking="">JobStreamReadFailed = -9669,</span>
	<span class="added added-field " data-is-non-breaking="">KeyNotFound = -9589,</span>
	<span class="added added-field " data-is-non-breaking="">KeyNotUnique = -9590,</span>
	<span class="added added-field " data-is-non-breaking="">KeyOrValueNotFound = -9623,</span>
	<span class="added added-field " data-is-non-breaking="">LockIgnored = -30878,</span>
	<span class="added added-field " data-is-non-breaking="">MessagingError = -9624,</span>
	<span class="added added-field " data-is-non-breaking="">NoDefaultItem = -9500,</span>
	<span class="added added-field " data-is-non-breaking="">NoDefaultPrinter = -30872,</span>
	<span class="added added-field " data-is-non-breaking="">NoDefaultSettings = -9501,</span>
	<span class="added added-field " data-is-non-breaking="">NoPrinterJobID = -9667,</span>
	<span class="added added-field " data-is-non-breaking="">NoSelectedPrinters = -9541,</span>
	<span class="added added-field " data-is-non-breaking="">NoSuchEntry = -30874,</span>
	<span class="added added-field " data-is-non-breaking="">NotImplemented = -30873,</span>
	<span class="added added-field " data-is-non-breaking="">ObjectInUse = -30881,</span>
	<span class="added added-field " data-is-non-breaking="">Ok = 0,</span>
	<span class="added added-field " data-is-non-breaking="">OpenFailed = -9781,</span>
	<span class="added added-field " data-is-non-breaking="">OutOfScope = -30871,</span>
	<span class="added added-field " data-is-non-breaking="">PMSymbolNotFound = -9660,</span>
	<span class="added added-field " data-is-non-breaking="">PermissionError = -9636,</span>
	<span class="added added-field " data-is-non-breaking="">PluginNotFound = -9701,</span>
	<span class="added added-field " data-is-non-breaking="">PluginRegisterationFailed = -9702,</span>
	<span class="added added-field " data-is-non-breaking="">PrBrowserNoUI = -9545,</span>
	<span class="added added-field " data-is-non-breaking="">QueueAlreadyExists = -9639,</span>
	<span class="added added-field " data-is-non-breaking="">QueueJobFailed = -9640,</span>
	<span class="added added-field " data-is-non-breaking="">QueueNotFound = -9638,</span>
	<span class="added added-field " data-is-non-breaking="">ReadFailed = -9782,</span>
	<span class="added added-field " data-is-non-breaking="">ReadGotZeroData = -9788,</span>
	<span class="added added-field " data-is-non-breaking="">ServerAlreadyRunning = -9631,</span>
	<span class="added added-field " data-is-non-breaking="">ServerAttributeRestricted = -9633,</span>
	<span class="added added-field " data-is-non-breaking="">ServerCommunicationFailed = -9621,</span>
	<span class="added added-field " data-is-non-breaking="">ServerNotFound = -9630,</span>
	<span class="added added-field " data-is-non-breaking="">ServerSuspended = -9632,</span>
	<span class="added added-field " data-is-non-breaking="">StatusFailed = -9784,</span>
	<span class="added added-field " data-is-non-breaking="">StringConversionFailure = -30883,</span>
	<span class="added added-field " data-is-non-breaking="">SubTicketNotFound = -9583,</span>
	<span class="added added-field " data-is-non-breaking="">SyncRequestFailed = -9543,</span>
	<span class="added added-field " data-is-non-breaking="">TemplateIsLocked = -9588,</span>
	<span class="added added-field " data-is-non-breaking="">TicketIsLocked = -9587,</span>
	<span class="added added-field " data-is-non-breaking="">TicketTypeNotFound = -9580,</span>
	<span class="added added-field " data-is-non-breaking="">UnableToFindProcess = -9532,</span>
	<span class="added added-field " data-is-non-breaking="">UnexpectedImagingError = -9707,</span>
	<span class="added added-field " data-is-non-breaking="">UnknownDataType = -9591,</span>
	<span class="added added-field " data-is-non-breaking="">UnknownMessage = -9637,</span>
	<span class="added added-field " data-is-non-breaking="">UnsupportedConnection = -9786,</span>
	<span class="added added-field " data-is-non-breaking="">UpdateTicketFailed = -9581,</span>
	<span class="added added-field " data-is-non-breaking="">UserOrGroupNotFound = -9635,</span>
	<span class="added added-field " data-is-non-breaking="">ValidateTicketFailed = -9582,</span>
	<span class="added added-field " data-is-non-breaking="">ValueOutOfRange = -30877,</span>
	<span class="added added-field " data-is-non-breaking="">WriteFailed = -9783,</span>
	<span class="added added-field " data-is-non-breaking="">XMLParseError = -30884,</span>
}
</pre>
</div> <!-- end type PMStatusCode -->
</div> <!-- end namespace MonoMac.PrintCore -->

</div> <!-- end topmost div -->
</div>
</body></html>
