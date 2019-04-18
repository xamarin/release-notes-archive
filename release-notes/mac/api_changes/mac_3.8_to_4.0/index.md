---
id: 6EF6D704-DC30-4E6D-B82D-45B7CC4B3325
title: "Mac 3.8 to 4.0"
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVMediaSelection[] AllMediaSelections { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetMetadataForFormat' with enum values AVMetadataFormat.")]
	public virtual AVMetadataItem[] MetadataForFormat (string format);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AVMediaSelectionGroup GetMediaSelectionGroupForMediaCharacteristic (AVMediaCharacteristics avMediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public AVMetadataItem[] GetMetadataForFormat (AVMetadataFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVMetadataItem[] GetMetadataForFormat (Foundation.NSString format);</span>
	<span class='added added-method ' data-is-non-breaking="">public AVAssetTrack[] GetTracks (AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public AVAssetTrack[] GetTracks (AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVAsset -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PresetHevc1920x1080 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PresetHevc3840x2160 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PresetHevcHighestQuality { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void DetermineCompatibilityOfExportPreset (string presetName, AVAsset asset, AVFileTypes outputFileType, System.Action&lt;bool&gt; isCompatibleResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;bool&gt; DetermineCompatibilityOfExportPresetAsync (string presetName, AVAsset asset, AVFileTypes outputFileType);</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
<!-- start type AVAssetExportSessionPreset --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSessionPreset</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PresetHevc1920x1080 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">PresetHevc3840x2160 = 12,</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSessionPreset -->
<!-- start type AVAssetTrack --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Decodable { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetTrack -->
<!-- start type AVAssetWriterInput --> <div>
<h3>Type Changed: AVFoundation.AVAssetWriterInput</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string MediaDataLocation { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVAssetWriterInput -->
<!-- start type AVAudioCompressedBuffer --> <div>
<h3>Type Changed: AVFoundation.AVAudioCompressedBuffer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ByteCapacity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ByteLength { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVAudioCompressedBuffer -->
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoShutdownEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InManualRenderingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingBlock ManualRenderingBlock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioFormat ManualRenderingFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ManualRenderingMaximumFrameCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingMode ManualRenderingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long ManualRenderingSampleTime { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EnableManualRenderingMode (AVAudioEngineManualRenderingMode mode, AVAudioFormat pcmFormat, uint maximumFrameCount, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingStatus RenderOffline (uint numberOfFrames, AVAudioPcmBuffer buffer, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioInputNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioInputNode</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetManualRenderingInputPcmFormat (AVAudioFormat format, AVAudioIONodeInputBlock block);</span>
</pre>
</div>

</div> <!-- end type AVAudioInputNode -->
<!-- start type AVAudioNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AudioUnit.AUAudioUnit AUAudioUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Latency { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double OutputPresentationLatency { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioNode -->
<!-- start type AVAudioPlayerNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleFile (AVAudioFile file, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleFileAsync (AVAudioFile file, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleSegment (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleSegmentAsync (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayerNode -->
<!-- start type AVAudioSettings --> <div>
<h3>Type Changed: AVFoundation.AVAudioSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileTypeKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioSettings -->
<!-- start type AVCaptureInputPort --> <div>
<h3>Type Changed: AVFoundation.AVCaptureInputPort</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created.")]
	public AVCaptureInputPort ();</span>
</div></pre>

</div> <!-- end type AVCaptureInputPort -->
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVComposition_AVCompositionTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVComposition_AVCompositionTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVCompositionTrack[] GetTracks (AVComposition This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVCompositionTrack[] GetTracks (AVComposition This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVComposition_AVCompositionTrackInspection -->
<!-- start type AVContentKeyResponse --> <div>
<h3>Type Changed: AVFoundation.AVContentKeyResponse</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeyResponse Create (Foundation.NSData keyData, Foundation.NSData initializationVector);</span>
</pre>
</div>

</div> <!-- end type AVContentKeyResponse -->
<!-- start type AVContentKeySession --> <div>
<h3>Type Changed: AVFoundation.AVContentKeySession</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySession Create (string keySystem);</span>
</pre>
</div>

</div> <!-- end type AVContentKeySession -->
<!-- start type AVContentKeySystem --> <div>
<h3>Type Changed: AVFoundation.AVContentKeySystem</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AVContentKeySystemClearKey = 1,</span>
</pre>
</div>

</div> <!-- end type AVContentKeySystem -->
<!-- start type AVFragmentedAsset_AVFragmentedAssetTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVFragmentedAsset_AVFragmentedAssetTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVFragmentedAssetTrack[] GetTracks (AVFragmentedAsset This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVFragmentedAssetTrack[] GetTracks (AVFragmentedAsset This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVFragmentedAsset_AVFragmentedAssetTrackInspection -->
<!-- start type AVFragmentedMovie_AVFragmentedMovieTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVFragmentedMovie_AVFragmentedMovieTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVFragmentedMovieTrack[] GetTracks (AVFragmentedMovie This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVFragmentedMovieTrack[] GetTracks (AVFragmentedMovie This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVFragmentedMovie_AVFragmentedMovieTrackInspection -->
<!-- start type AVMediaTypes --> <div>
<h3>Type Changed: AVFoundation.AVMediaTypes</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DepthData = 10,</span>
</pre>
</div>

</div> <!-- end type AVMediaTypes -->
<!-- start type AVMetadata --> <div>
<h3>Type Changed: AVFoundation.AVMetadata</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeySpaceAudioFile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeySpaceHlsDateRange { get; }</span>
</pre>
</div>

</div> <!-- end type AVMetadata -->
<!-- start type AVMovie_AVMovieTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVMovie_AVMovieTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVMovieTrack[] GetTracks (AVMovie This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMovieTrack[] GetTracks (AVMovie This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVMovie_AVMovieTrackInspection -->
<!-- start type AVMutableComposition_AVMutableCompositionTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVMutableComposition_AVMutableCompositionTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVMutableCompositionTrack[] GetTracks (AVMutableComposition This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMutableCompositionTrack[] GetTracks (AVMutableComposition This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVMutableComposition_AVMutableCompositionTrackInspection -->
<!-- start type AVMutableMovie_AVMutableMovieTrackInspection --> <div>
<h3>Type Changed: AVFoundation.AVMutableMovie_AVMutableMovieTrackInspection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVMutableMovieTrack[] GetTracks (AVMutableMovie This, AVMediaCharacteristics mediaCharacteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMutableMovieTrack[] GetTracks (AVMutableMovie This, AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVMutableMovie_AVMutableMovieTrackInspection -->
<!-- start type AVMutableVideoComposition --> <div>
<h3>Type Changed: AVFoundation.AVMutableVideoComposition</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int SourceTrackIdForFrameTiming { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVMutableVideoComposition -->
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVPlayerLooper --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLooper</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("This selector does not exist in the header and was wrongly added.")]
	public virtual bool LoopingEnabled { get; }</span>
</div></pre>

</div> <!-- end type AVPlayerLooper -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->
<!-- start type AVVideoColorPrimaries --> <div>
<h3>Type Changed: AVFoundation.AVVideoColorPrimaries</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Itu_R_2020 { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoColorPrimaries -->
<!-- start type AVVideoYCbCrMatrix --> <div>
<h3>Type Changed: AVFoundation.AVVideoYCbCrMatrix</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Itu_R_2020 { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoYCbCrMatrix -->
<div> <!-- start type AVAssetWriterInputMediaDataLocation -->
<h3>New Type AVFoundation.AVAssetWriterInputMediaDataLocation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAssetWriterInputMediaDataLocation {
	<span class='added added-field ' data-is-non-breaking="">BeforeMainMediaDataNotInterleaved = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InterleavedWithMainMediaData = 0,</span>
}
</pre>
</div> <!-- end type AVAssetWriterInputMediaDataLocation -->
<div> <!-- start type AVAssetWriterInputMediaDataLocationExtensions -->
<h3>New Type AVFoundation.AVAssetWriterInputMediaDataLocationExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAssetWriterInputMediaDataLocationExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVAssetWriterInputMediaDataLocation self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVAssetWriterInputMediaDataLocation GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVAssetWriterInputMediaDataLocationExtensions -->
<div> <!-- start type AVAudioEngineManualRenderingBlock -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AVAudioEngineManualRenderingBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioEngineManualRenderingBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint numberOfFrames, AudioToolbox.AudioBuffers outBuffer, int outError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingStatus EndInvoke (int outError, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingStatus Invoke (uint numberOfFrames, AudioToolbox.AudioBuffers outBuffer, int outError);</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingBlock -->
<div> <!-- start type AVAudioEngineManualRenderingError -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingError {
	<span class='added added-field ' data-is-non-breaking="">Initialized = -80801,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidMode = -80800,</span>
	<span class='added added-field ' data-is-non-breaking="">NotRunning = -80802,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingError -->
<div> <!-- start type AVAudioEngineManualRenderingMode -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingMode {
	<span class='added added-field ' data-is-non-breaking="">Offline = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Realtime = 1,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingMode -->
<div> <!-- start type AVAudioEngineManualRenderingStatus -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingStatus {
	<span class='added added-field ' data-is-non-breaking="">CannotDoInCurrentContext = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Error = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientDataFromInputNode = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingStatus -->
<div> <!-- start type AVAudioIONodeInputBlock -->
<h3>New Type AVFoundation.AVAudioIONodeInputBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AVAudioIONodeInputBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioIONodeInputBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint frameCount, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AudioToolbox.AudioBuffers EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AudioToolbox.AudioBuffers Invoke (uint frameCount);</span>
}
</pre>
</div> <!-- end type AVAudioIONodeInputBlock -->
<div> <!-- start type AVAudioPlayerNodeCompletionCallbackType -->
<h3>New Type AVFoundation.AVAudioPlayerNodeCompletionCallbackType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioPlayerNodeCompletionCallbackType {
	<span class='added added-field ' data-is-non-breaking="">Consumed = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PlayedBack = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rendered = 1,</span>
}
</pre>
</div> <!-- end type AVAudioPlayerNodeCompletionCallbackType -->
<div> <!-- start type AVAudioSessionRouteSharingPolicy -->
<h3>New Type AVFoundation.AVAudioSessionRouteSharingPolicy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioSessionRouteSharingPolicy {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Independent = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LongForm = 1,</span>
}
</pre>
</div> <!-- end type AVAudioSessionRouteSharingPolicy -->
<div> <!-- start type AVCameraCalibrationData -->
<h3>New Type AVFoundation.AVCameraCalibrationData</h3>
<pre class='added' data-is-non-breaking="">
public class AVCameraCalibrationData : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCameraCalibrationData (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCameraCalibrationData (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix4x3 ExtrinsicMatrix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix3 IntrinsicMatrix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize IntrinsicMatrixReferenceDimensions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData InverseLensDistortionLookupTable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint LensDistortionCenter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData LensDistortionLookupTable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PixelSize { get; }</span>
}
</pre>
</div> <!-- end type AVCameraCalibrationData -->
<div> <!-- start type AVCaptureDataOutputSynchronizer -->
<h3>New Type AVFoundation.AVCaptureDataOutputSynchronizer</h3>
<pre class='added' data-is-non-breaking="">
public class AVCaptureDataOutputSynchronizer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVCaptureDataOutputSynchronizer (AVCaptureOutput[] dataOutputs);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureDataOutputSynchronizer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureDataOutputSynchronizer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCaptureOutput[] DataOutputs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IAVCaptureDataOutputSynchronizerDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreFoundation.DispatchQueue DelegateCallbackQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDelegate (IAVCaptureDataOutputSynchronizerDelegate del, CoreFoundation.DispatchQueue delegateCallbackQueue);</span>
}
</pre>
</div> <!-- end type AVCaptureDataOutputSynchronizer -->
<div> <!-- start type AVCaptureDataOutputSynchronizerDelegate -->
<h3>New Type AVFoundation.AVCaptureDataOutputSynchronizerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVCaptureDataOutputSynchronizerDelegate : Foundation.NSObject, IAVCaptureDataOutputSynchronizerDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureDataOutputSynchronizerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureDataOutputSynchronizerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureDataOutputSynchronizerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputSynchronizedDataCollection (AVCaptureDataOutputSynchronizer synchronizer, AVCaptureSynchronizedDataCollection synchronizedDataCollection);</span>
}
</pre>
</div> <!-- end type AVCaptureDataOutputSynchronizerDelegate -->
<div> <!-- start type AVCaptureLensStabilizationStatus -->
<h3>New Type AVFoundation.AVCaptureLensStabilizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVCaptureLensStabilizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfRange = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unavailable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
}
</pre>
</div> <!-- end type AVCaptureLensStabilizationStatus -->
<div> <!-- start type AVCaptureOutputDataDroppedReason -->
<h3>New Type AVFoundation.AVCaptureOutputDataDroppedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVCaptureOutputDataDroppedReason {
	<span class='added added-field ' data-is-non-breaking="">Discontinuity = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LateData = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBuffers = 2,</span>
}
</pre>
</div> <!-- end type AVCaptureOutputDataDroppedReason -->
<div> <!-- start type AVCaptureSynchronizedData -->
<h3>New Type AVFoundation.AVCaptureSynchronizedData</h3>
<pre class='added' data-is-non-breaking="">
public class AVCaptureSynchronizedData : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureSynchronizedData (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureSynchronizedData (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Timestamp { get; }</span>
}
</pre>
</div> <!-- end type AVCaptureSynchronizedData -->
<div> <!-- start type AVCaptureSynchronizedDataCollection -->
<h3>New Type AVFoundation.AVCaptureSynchronizedDataCollection</h3>
<pre class='added' data-is-non-breaking="">
public class AVCaptureSynchronizedDataCollection : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureSynchronizedDataCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVCaptureSynchronizedDataCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVCaptureSynchronizedData Item { get; }</span>
	// methods

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'GetSynchronizedData' instead.")]
	public virtual AVCaptureSynchronizedData From (AVCaptureOutput captureOutput);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVCaptureSynchronizedData GetSynchronizedData (AVCaptureOutput captureOutput);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'GetSynchronizedData' instead.")]
	public virtual AVCaptureSynchronizedData ObjectForKeyedSubscript (AVCaptureOutput key);</span>
}
</pre>
</div> <!-- end type AVCaptureSynchronizedDataCollection -->
<div> <!-- start type AVDepthData -->
<h3>New Type AVFoundation.AVDepthData</h3>
<pre class='added' data-is-non-breaking="">
public class AVDepthData : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDepthData (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDepthData (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreVideo.CVPixelFormatType[] AvailableDepthDataTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVCameraCalibrationData CameraCalibrationData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVDepthDataAccuracy DepthDataAccuracy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer DepthDataMap { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVDepthDataQuality DepthDataQuality { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelFormatType DepthDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsDepthDataFiltered { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber[] WeakAvailableDepthDataTypes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AVDepthData ApplyExifOrientation (ImageIO.CGImagePropertyOrientation exifOrientation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVDepthData ConvertToDepthDataType (CoreVideo.CVPixelFormatType depthDataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVDepthData Create (Foundation.NSDictionary imageSourceAuxDataInfoDictionary, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVDepthData Create (ImageIO.CGImageAuxiliaryDataInfo dataInfo, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDictionary GetDictionaryRepresentation (string outAuxDataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVDepthData ReplaceDepthDataMap (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError outError);</span>
}
</pre>
</div> <!-- end type AVDepthData -->
<div> <!-- start type AVDepthDataAccuracy -->
<h3>New Type AVFoundation.AVDepthDataAccuracy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVDepthDataAccuracy {
	<span class='added added-field ' data-is-non-breaking="">Absolute = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Relative = 0,</span>
}
</pre>
</div> <!-- end type AVDepthDataAccuracy -->
<div> <!-- start type AVDepthDataQuality -->
<h3>New Type AVFoundation.AVDepthDataQuality</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVDepthDataQuality {
	<span class='added added-field ' data-is-non-breaking="">High = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = 0,</span>
}
</pre>
</div> <!-- end type AVDepthDataQuality -->
<div> <!-- start type AVFileTypes -->
<h3>New Type AVFoundation.AVFileTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVFileTypes {
	<span class='added added-field ' data-is-non-breaking="">AC3 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Aifc = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Aiff = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Amr = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleM4V = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleM4a = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Avci = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">CoreAudioFormat = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Dng = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">EnhancedAC3 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Heic = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Heif = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Jpeg = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Mpeg4 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MpegLayer3 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">QuickTimeMovie = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SunAU = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreeGpp = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreeGpp2 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Tiff = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Wave = 6,</span>
}
</pre>
</div> <!-- end type AVFileTypes -->
<div> <!-- start type AVFileTypesExtensions -->
<h3>New Type AVFoundation.AVFileTypesExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVFileTypesExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVFileTypes self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVFileTypes GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVFileTypesExtensions -->
<div> <!-- start type AVMediaCharacteristics -->
<h3>New Type AVFoundation.AVMediaCharacteristics</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMediaCharacteristics {
	<span class='added added-field ' data-is-non-breaking="">Audible = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ContainsOnlyForcedSubtitles = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">DescribesMusicAndSoundForAccessibility = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">DescribesVideoForAccessibility = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">DubbedTranslation = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">EasyToRead = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">FrameBased = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">IsAuxiliaryContent = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">IsMainProgramContent = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LanguageTranslation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Legible = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TranscribesSpokenDialogForAccessibility = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UsesWideGamutColorSpace = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Visual = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VoiceOverTranslation = 14,</span>
}
</pre>
</div> <!-- end type AVMediaCharacteristics -->
<div> <!-- start type AVMediaCharacteristicsExtensions -->
<h3>New Type AVFoundation.AVMediaCharacteristicsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVMediaCharacteristicsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVMediaCharacteristics self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMediaCharacteristics GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVMediaCharacteristicsExtensions -->
<div> <!-- start type AVMetadataFormat -->
<h3>New Type AVFoundation.AVMetadataFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMetadataFormat {
	<span class='added added-field ' data-is-non-breaking="">FormatHlsMetadata = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatID3Metadata = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatISOUserData = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatQuickTimeUserData = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatiTunesMetadata = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 5,</span>
}
</pre>
</div> <!-- end type AVMetadataFormat -->
<div> <!-- start type AVMetadataFormatExtensions -->
<h3>New Type AVFoundation.AVMetadataFormatExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVMetadataFormatExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVMetadataFormat self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMetadataFormat GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVMetadataFormatExtensions -->
<div> <!-- start type AVRouteDetector -->
<h3>New Type AVFoundation.AVRouteDetector</h3>
<pre class='added' data-is-non-breaking="">
public class AVRouteDetector : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRouteDetector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRouteDetector (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MultipleRoutesDetected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MultipleRoutesDetectedDidChange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RouteDetectionEnabled { get; set; }</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMultipleRoutesDetectedDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMultipleRoutesDetectedDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type AVRouteDetector -->
<div> <!-- start type AVSampleBufferAudioRenderer -->
<h3>New Type AVFoundation.AVSampleBufferAudioRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleBufferAudioRenderer : Foundation.NSObject, IAVQueuedSampleBufferRendering, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferAudioRenderer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferAudioRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferAudioRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AudioOutputDeviceUniqueId { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AudioRendererWasFlushedAutomaticallyNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Muted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PitchAlgorithm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadyForMoreMediaData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVQueuedSampleBufferRenderingStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTimebase Timebase { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Volume { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enqueue (CoreMedia.CMSampleBuffer sampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Flush (CoreMedia.CMTime time, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; FlushAsync (CoreMedia.CMTime time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestMediaData (CoreFoundation.DispatchQueue queue, System.Action handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopRequestingMediaData ();</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioRendererWasFlushedAutomatically (System.EventHandler&lt;AudioRendererWasFlushedAutomaticallyEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioRendererWasFlushedAutomatically (Foundation.NSObject objectToObserve, System.EventHandler&lt;AudioRendererWasFlushedAutomaticallyEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type AVSampleBufferAudioRenderer -->
<div> <!-- start type AVSampleBufferRenderSynchronizer -->
<h3>New Type AVFoundation.AVSampleBufferRenderSynchronizer</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleBufferRenderSynchronizer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferRenderSynchronizer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferRenderSynchronizer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferRenderSynchronizer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Rate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVQueuedSampleBufferRendering[] Renderers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTimebase Timebase { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (IAVQueuedSampleBufferRendering renderer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject AddBoundaryTimeObserver (Foundation.NSValue[] times, CoreFoundation.DispatchQueue queue, System.Action handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject AddPeriodicTimeObserver (CoreMedia.CMTime interval, CoreFoundation.DispatchQueue queue, System.Action&lt;CoreMedia.CMTime&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (IAVQueuedSampleBufferRendering renderer, CoreMedia.CMTime time, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; RemoveAsync (IAVQueuedSampleBufferRendering renderer, CoreMedia.CMTime time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveTimeObserver (Foundation.NSObject observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetRate (float rate, CoreMedia.CMTime time);</span>
}
</pre>
</div> <!-- end type AVSampleBufferRenderSynchronizer -->
<div> <!-- start type AVVideoApertureMode -->
<h3>New Type AVFoundation.AVVideoApertureMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVVideoApertureMode {
	<span class='added added-field ' data-is-non-breaking="">CleanAperture = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">EncodedPixels = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ProductionAperture = 1,</span>
}
</pre>
</div> <!-- end type AVVideoApertureMode -->
<div> <!-- start type AVVideoApertureModeExtensions -->
<h3>New Type AVFoundation.AVVideoApertureModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVVideoApertureModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVVideoApertureMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVVideoApertureMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVVideoApertureModeExtensions -->
<div> <!-- start type AVVideoCodecType -->
<h3>New Type AVFoundation.AVVideoCodecType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVVideoCodecType {
	<span class='added added-field ' data-is-non-breaking="">AppleProRes422 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleProRes4444 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">H264 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hevc = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Jpeg = 1,</span>
}
</pre>
</div> <!-- end type AVVideoCodecType -->
<div> <!-- start type AVVideoCodecTypeExtensions -->
<h3>New Type AVFoundation.AVVideoCodecTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVVideoCodecTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVVideoCodecType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVVideoCodecType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVVideoCodecTypeExtensions -->
<div> <!-- start type AudioRendererWasFlushedAutomaticallyEventArgs -->
<h3>New Type AVFoundation.AudioRendererWasFlushedAutomaticallyEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class AudioRendererWasFlushedAutomaticallyEventArgs : Foundation.NSNotificationEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AudioRendererWasFlushedAutomaticallyEventArgs (Foundation.NSNotification notification);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreMedia.CMTime AudioRendererFlushTime { get; }</span>
}
</pre>
</div> <!-- end type AudioRendererWasFlushedAutomaticallyEventArgs -->
<div> <!-- start type IAVCaptureDataOutputSynchronizerDelegate -->
<h3>New Type AVFoundation.IAVCaptureDataOutputSynchronizerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVCaptureDataOutputSynchronizerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOutputSynchronizedDataCollection (AVCaptureDataOutputSynchronizer synchronizer, AVCaptureSynchronizedDataCollection synchronizedDataCollection);</span>
}
</pre>
</div> <!-- end type IAVCaptureDataOutputSynchronizerDelegate -->
<div> <!-- start type IAVQueuedSampleBufferRendering -->
<h3>New Type AVFoundation.IAVQueuedSampleBufferRendering</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVQueuedSampleBufferRendering : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadyForMoreMediaData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTimebase Timebase { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enqueue (CoreMedia.CMSampleBuffer sampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestMediaData (CoreFoundation.DispatchQueue queue, System.Action handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopRequestingMediaData ();</span>
}
</pre>
</div> <!-- end type IAVQueuedSampleBufferRendering -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UpdatesNowPlayingInfoCenter { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAccount (ACAccount account, ACAccountStoreRemoveCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RemoveAccountAsync (ACAccount account);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore -->
<div> <!-- start type ACAccountStoreRemoveCompletionHandler -->
<h3>New Type Accounts.ACAccountStoreRemoveCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ACAccountStoreRemoveCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ACAccountStoreRemoveCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool success, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool success, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type ACAccountStoreRemoveCompletionHandler -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CustomTextAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LanguageTextAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PageRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSAccessibilitySubroles --> <div>
<h3>Type Changed: AppKit.NSAccessibilitySubroles</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SectionListSubrole { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TabButtonSubrole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilitySubroles -->
<!-- start type NSAccessibility_Extensions --> <div>
<h3>Type Changed: AppKit.NSAccessibility_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityElement[] GetAccessibilityChildrenInNavigationOrder (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomAction[] GetAccessibilityCustomActions (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSAccessibilityCustomRotor[] GetAccessibilityCustomRotors (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityChildrenInNavigationOrder (INSAccessibility This, NSAccessibilityElement[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomActions (INSAccessibility This, NSAccessibilityCustomAction[] value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (INSAccessibility This, NSAccessibilityCustomRotor[] value);</span>
</pre>
</div>

</div> <!-- end type NSAccessibility_Extensions -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationOpenUrlsEventArgs&gt; OpenUrls;</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrls (NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenUrls (INSApplicationDelegate This, NSApplication application, Foundation.NSUrl[] urls);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBezierPath --> <div>
<h3>Type Changed: AppKit.NSBezierPath</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (uint[], NSFont)' instead.")]
	public void AppendPathWithGlyphs (uint[] glyphs, NSFont font);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Append (CGPoint[])' instead.")]
	public void AppendPathWithPoints (CoreGraphics.CGPoint[] points);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Append (NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (CoreGraphics.CGPoint[] points);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Append (uint[] glyphs, NSFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AppendPathWithCGGlyph (ushort glyph, NSFont font);</span>
</pre>
</div>

</div> <!-- end type NSBezierPath -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCollectionViewPrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewTransitionLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewTransitionLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set currentLayout and newLayout.")]
	public NSCollectionViewTransitionLayout ();</span>
</div></pre>

</div> <!-- end type NSCollectionViewTransitionLayout -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemBrownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemGreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemOrangeColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPinkColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemPurpleColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemRedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor SystemYellowColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorType Type { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromName (string name, Foundation.NSBundle bundle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSColor GetColor (NSColorType type);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorPickerTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSColorPickerTouchBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorSpace[] AllowedColorSpaces { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSColorPickerTouchBarItem -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentSharing { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepare (NSSharingServicePicker sharingServicePicker);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShareDocument (NSSharingService sharingService, System.Action&lt;bool&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; ShareDocumentAsync (NSSharingService sharingService);</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDocumentController --> <div>
<h3>Type Changed: AppKit.NSDocumentController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsAutomaticShareMenu { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMenuItem StandardShareMenuItem { get; }</span>
</pre>
</div>

</div> <!-- end type NSDocumentController -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSFont --> <div>
<h3>Type Changed: AppKit.NSFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSFont FromCTFont (CoreText.CTFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAdvancement (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGSize[] GetAdvancements (ushort[] glyphs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetBoundingRect (ushort glyph);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreGraphics.CGRect[] GetBoundingRects (ushort[] glyphs);</span>
</pre>
</div>

</div> <!-- end type NSFont -->
<!-- start type NSFontDescriptor --> <div>
<h3>Type Changed: AppKit.NSFontDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFontAssetRequest { get; }</span>
</pre>
</div>

</div> <!-- end type NSFontDescriptor -->
<!-- start type NSFontSymbolicTraits --> <div>
<h3>Type Changed: AppKit.NSFontSymbolicTraits</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TraitLooseLeading = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">TraitTightLeading = 32768,</span>
</pre>
</div>

</div> <!-- end type NSFontSymbolicTraits -->
<!-- start type NSGlyphInfo --> <div>
<h3>Type Changed: AppKit.NSGlyphInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BaseString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort GlyphId { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGlyphInfo GetGlyphInfo (ushort glyph, NSFont font, string string);</span>
</pre>
</div>

</div> <!-- end type NSGlyphInfo -->
<!-- start type NSGroupTouchBarItem --> <div>
<h3>Type Changed: AppKit.NSGroupTouchBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions EffectiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection GroupUserInterfaceLayoutDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredItemWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersEqualWidths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions[] PrioritizedCompressionOptions { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateAlertStyleGroupItem (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items, NSUserInterfaceCompressionOptions allowedCompressionOptions);</span>
</pre>
</div>

</div> <!-- end type NSGroupTouchBarItem -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: AppKit.NSImageName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarRemoveTemplate = 116,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSLayoutAnchor`1 --> <div>
<h3>Type Changed: AppKit.NSLayoutAnchor`1</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutConstraint[] ConstraintsAffectingLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAmbiguousLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSLayoutAnchor`1 -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutXAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension GetAnchorWithOffset (NSLayoutYAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: AppKit.NSLevelIndicator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor CriticalFillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DrawsTieredCapacityLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Editable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor FillColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLevelIndicatorPlaceholderVisibility PlaceholderVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage RatingPlaceholderImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor WarningFillColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsKeyEquivalentWhenHidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSOpenGLLayer --> <div>
<h3>Type Changed: AppKit.NSOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSOpenGLLayer -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: AppKit.NSPasteboard</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameDrag { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameFont { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameGeneral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardNameRuler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeFileUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSPasteboardTypeUrl { get; }</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAppearanceCustomization</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'GetAppearance' and 'SetAppearance' methods instead.")]
	public virtual NSPopoverAppearance Appearance { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAppearance EffectiveAppearance { get; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: AppKit.NSResponder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeRestorableState (Foundation.NSCoder coder, Foundation.NSOperationQueue queue);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceCompression</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSegmentDistribution SegmentDistribution { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTextAlignment GetAlignment (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetTag (nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetToolTip (nint forSegment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlignment (NSTextAlignment alignment, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetShowsMenuIndicator (bool showsMenuIndicator, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTag (nint tag, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetToolTip (string toolTip, nint segment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShowsMenuIndicator (nint segment);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSliderAccessory --> <div>
<h3>Type Changed: AppKit.NSSliderAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSliderAccessory -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceValidations</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStoryboard --> <div>
<h3>Type Changed: AppKit.NSStoryboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSStoryboard MainStoryboard { get; }</span>
</pre>
</div>

</div> <!-- end type NSStoryboard -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesAutomaticRowHeights { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSText --> <div>
<h3>Type Changed: AppKit.NSText</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovementUserInfoKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSText -->
<!-- start type NSTextList --> <div>
<h3>Type Changed: AppKit.NSTextList</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextList (NSTextListMarkerFormats format, NSTextListOptions mask);</span>
</pre>
</div>

</div> <!-- end type NSTextList -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSToolbar ();</span>
</pre>
</div>

</div> <!-- end type NSToolbar -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement[] AccessibilityChildrenInNavigationOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotor[] AccessibilityCustomRotors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTab Tab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabGroup TabGroup { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabOverview (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SwitchControlEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool VoiceOverEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type DownloadFontAssetsRequestCompletionHandler -->
<h3>New Type AppKit.DownloadFontAssetsRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DownloadFontAssetsRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DownloadFontAssetsRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DownloadFontAssetsRequestCompletionHandler -->
<div> <!-- start type INSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.INSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityCustomRotorItemSearchDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type INSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type INSAccessibilityElementLoading -->
<h3>New Type AppKit.INSAccessibilityElementLoading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSAccessibilityElementLoading : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityElement GetAccessibilityElement (Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type INSAccessibilityElementLoading -->
<div> <!-- start type INSCollectionViewPrefetching -->
<h3>New Type AppKit.INSCollectionViewPrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewPrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type INSCollectionViewPrefetching -->
<div> <!-- start type INSUserInterfaceCompression -->
<h3>New Type AppKit.INSUserInterfaceCompression</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceCompression : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions ActiveCompressionOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Compress (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetMinimumSize (NSUserInterfaceCompressionOptions[] prioritizedOptions);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceCompression -->
<div> <!-- start type NSAboutPanelOption -->
<h3>New Type AppKit.NSAboutPanelOption</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAboutPanelOption {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationIcon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplicationVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Credits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Version { get; }</span>
}
</pre>
</div> <!-- end type NSAboutPanelOption -->
<div> <!-- start type NSAccessibilityAnnotationAttributeKey -->
<h3>New Type AppKit.NSAccessibilityAnnotationAttributeKey</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityAnnotationAttributeKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationLocation { get; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationAttributeKey -->
<div> <!-- start type NSAccessibilityAnnotationPosition -->
<h3>New Type AppKit.NSAccessibilityAnnotationPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityAnnotationPosition {
	<span class='added added-field ' data-is-non-breaking="">End = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FullRange = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type NSAccessibilityAnnotationPosition -->
<div> <!-- start type NSAccessibilityCustomAction -->
<h3>New Type AppKit.NSAccessibilityCustomAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomAction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, System.Func&lt;bool&gt; handler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomAction (string name, Foundation.NSObject target, ObjCRuntime.Selector selector);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;bool&gt; Handler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Selector { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomAction -->
<div> <!-- start type NSAccessibilityCustomRotor -->
<h3>New Type AppKit.NSAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (NSAccessibilityCustomRotorType rotorType, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotor (string label, INSAccessibilityCustomRotorItemSearchDelegate itemSearchDelegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityElementLoading ItemLoadingDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSAccessibilityCustomRotorItemSearchDelegate ItemSearchDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotor -->
<div> <!-- start type NSAccessibilityCustomRotorItemResult -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorItemResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (NSAccessibilityElement targetElement);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorItemResult (Foundation.INSSecureCoding itemLoadingToken, string customLabel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSSecureCoding ItemLoadingToken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityElement TargetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemResult -->
<div> <!-- start type NSAccessibilityCustomRotorItemSearchDelegate -->
<h3>New Type AppKit.NSAccessibilityCustomRotorItemSearchDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSAccessibilityCustomRotorItemSearchDelegate : Foundation.NSObject, INSAccessibilityCustomRotorItemSearchDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorItemSearchDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult GetResult (NSAccessibilityCustomRotor rotor, NSAccessibilityCustomRotorSearchParameters searchParameters);</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorItemSearchDelegate -->
<div> <!-- start type NSAccessibilityCustomRotorSearchDirection -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorSearchDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchDirection -->
<div> <!-- start type NSAccessibilityCustomRotorSearchParameters -->
<h3>New Type AppKit.NSAccessibilityCustomRotorSearchParameters</h3>
<pre class='added' data-is-non-breaking="">
public class NSAccessibilityCustomRotorSearchParameters : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSAccessibilityCustomRotorSearchParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSAccessibilityCustomRotorSearchParameters (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FilterString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityCustomRotorSearchDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorSearchParameters -->
<div> <!-- start type NSAccessibilityCustomRotorType -->
<h3>New Type AppKit.NSAccessibilityCustomRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSAccessibilityCustomRotorType {
	<span class='added added-field ' data-is-non-breaking="">Annotation = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BoldText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlinedText = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 20,</span>
}
</pre>
</div> <!-- end type NSAccessibilityCustomRotorType -->
<div> <!-- start type NSAccessibilityElementLoading_Extensions -->
<h3>New Type AppKit.NSAccessibilityElementLoading_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibilityElementLoading_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSRange GetAccessibilityRangeInTargetElement (INSAccessibilityElementLoading This, Foundation.INSSecureCoding token);</span>
}
</pre>
</div> <!-- end type NSAccessibilityElementLoading_Extensions -->
<div> <!-- start type NSApplicationOpenUrlsEventArgs -->
<h3>New Type AppKit.NSApplicationOpenUrlsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationOpenUrlsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationOpenUrlsEventArgs (Foundation.NSUrl[] urls);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl[] Urls { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationOpenUrlsEventArgs -->
<div> <!-- start type NSCollectionViewPrefetching_Extensions -->
<h3>New Type AppKit.NSCollectionViewPrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewPrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (INSCollectionViewPrefetching This, NSCollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type NSCollectionViewPrefetching_Extensions -->
<div> <!-- start type NSColorType -->
<h3>New Type AppKit.NSColorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSColorType {
	<span class='added added-field ' data-is-non-breaking="">Catalog = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ComponentBased = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Pattern = 1,</span>
}
</pre>
</div> <!-- end type NSColorType -->
<div> <!-- start type NSFontAssetRequest -->
<h3>New Type AppKit.NSFontAssetRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSFontAssetRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFontAssetRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFontAssetRequest (NSFontDescriptor[] fontDescriptors, NSFontAssetRequestOptions options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFontDescriptor[] DownloadedFontDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSProgress Progress { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DownloadFontAssets (DownloadFontAssetsRequestCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type NSFontAssetRequest -->
<div> <!-- start type NSFontAssetRequestOptions -->
<h3>New Type AppKit.NSFontAssetRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontAssetRequestOptions {
	<span class='added added-field ' data-is-non-breaking="">UsesStandardUI = 1,</span>
}
</pre>
</div> <!-- end type NSFontAssetRequestOptions -->
<div> <!-- start type NSFontError -->
<h3>New Type AppKit.NSFontError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFontError {
	<span class='added added-field ' data-is-non-breaking="">AssetDownloadError = 66304,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMaximum = 66335,</span>
	<span class='added added-field ' data-is-non-breaking="">ErrorMinimum = 66304,</span>
}
</pre>
</div> <!-- end type NSFontError -->
<div> <!-- start type NSFontPanelModeMask -->
<h3>New Type AppKit.NSFontPanelModeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSFontPanelModeMask {
	<span class='added added-field ' data-is-non-breaking="">AllEffects = 1048320,</span>
	<span class='added added-field ' data-is-non-breaking="">AllModes = 4294967295,</span>
	<span class='added added-field ' data-is-non-breaking="">Collection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">DocumentColorEffect = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">Face = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShadowEffect = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">Size = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StandardModes = 65535,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikethroughEffect = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorEffect = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineEffect = 256,</span>
}
</pre>
</div> <!-- end type NSFontPanelModeMask -->
<div> <!-- start type NSLevelIndicatorPlaceholderVisibility -->
<h3>New Type AppKit.NSLevelIndicatorPlaceholderVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLevelIndicatorPlaceholderVisibility {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WhileEditing = 2,</span>
}
</pre>
</div> <!-- end type NSLevelIndicatorPlaceholderVisibility -->
<div> <!-- start type NSObject_NSFontPanelValidationAdditions -->
<h3>New Type AppKit.NSObject_NSFontPanelValidationAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_NSFontPanelValidationAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFontPanelModeMask GetValidModes (Foundation.NSObject This, NSFontPanel fontPanel);</span>
}
</pre>
</div> <!-- end type NSObject_NSFontPanelValidationAdditions -->
<div> <!-- start type NSRulerViewUnits -->
<h3>New Type AppKit.NSRulerViewUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSRulerViewUnits {
	<span class='added added-field ' data-is-non-breaking="">Centimeters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inches = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Picas = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
}
</pre>
</div> <!-- end type NSRulerViewUnits -->
<div> <!-- start type NSRulerViewUnitsExtensions -->
<h3>New Type AppKit.NSRulerViewUnitsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRulerViewUnitsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSRulerViewUnits self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRulerViewUnits GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSRulerViewUnitsExtensions -->
<div> <!-- start type NSSegmentDistribution -->
<h3>New Type AppKit.NSSegmentDistribution</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSegmentDistribution {
	<span class='added added-field ' data-is-non-breaking="">Fill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FillEqually = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FillProportionally = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fit = 0,</span>
}
</pre>
</div> <!-- end type NSSegmentDistribution -->
<div> <!-- start type NSTextListMarkerFormats -->
<h3>New Type AppKit.NSTextListMarkerFormats</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTextListMarkerFormats {
	<span class='added added-field ' data-is-non-breaking="">Box = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Check = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimal = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Disc = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hyphen = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseAlpha = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseHexadecimal = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseLatin = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">LowercaseRoman = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Octal = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseAlpha = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseHexadecimal = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseLatin = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UppercaseRoman = 15,</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormats -->
<div> <!-- start type NSTextListMarkerFormatsExtensions -->
<h3>New Type AppKit.NSTextListMarkerFormatsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextListMarkerFormatsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSTextListMarkerFormats self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextListMarkerFormats GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTextListMarkerFormatsExtensions -->
<div> <!-- start type NSUserInterfaceCompressionOptions -->
<h3>New Type AppKit.NSUserInterfaceCompressionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserInterfaceCompressionOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (Foundation.NSSet&lt;NSUserInterfaceCompressionOptions&gt; options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserInterfaceCompressionOptions (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserInterfaceCompressionOptions (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions BreakEqualWidthsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Empty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideImagesOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions HideTextOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions ReduceMetricsOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUserInterfaceCompressionOptions StandardOptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByAdding (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSUserInterfaceCompressionOptions GetOptionsByRemoving (NSUserInterfaceCompressionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSUserInterfaceCompressionOptions options);</span>
}
</pre>
</div> <!-- end type NSUserInterfaceCompressionOptions -->
<div> <!-- start type NSWindowTab -->
<h3>New Type AppKit.NSWindowTab</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTab : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSWindowTab ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView AccessoryView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ToolTip { get; set; }</span>
}
</pre>
</div> <!-- end type NSWindowTab -->
<div> <!-- start type NSWindowTabGroup -->
<h3>New Type AppKit.NSWindowTabGroup</h3>
<pre class='added' data-is-non-breaking="">
public class NSWindowTabGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSWindowTabGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool OverviewVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow SelectedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool TabBarVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] Windows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (NSWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Insert (NSWindow window, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (NSWindow window);</span>
}
</pre>
</div> <!-- end type NSWindowTabGroup -->

</div> <!-- end namespace AppKit -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioChannelLabel --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLabel</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HoaAcn = 500,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn0 = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn1 = 131073,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn10 = 131082,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn11 = 131083,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn12 = 131084,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn13 = 131085,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn14 = 131086,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn15 = 131087,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn2 = 131074,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn3 = 131075,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn4 = 131076,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn5 = 131077,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn6 = 131078,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn65024 = 196096,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn7 = 131079,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn8 = 131080,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn9 = 131081,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLabel -->
<!-- start type AudioChannelLayoutTag --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLayoutTag</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_N3D = 12517376,</span>
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_SN3D = 12451840,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLayoutTag -->
<!-- start type AudioFileType --> <div>
<h3>Type Changed: AudioToolbox.AudioFileType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FLAC = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">RF64 = 1380333108,</span>
</pre>
</div>

</div> <!-- end type AudioFileType -->
<!-- start type AudioFormatType --> <div>
<h3>Type Changed: AudioToolbox.AudioFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Flac = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">Opus = 1869641075,</span>
</pre>
</div>

</div> <!-- end type AudioFormatType -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MidiOutputBufferSizeHint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUMidiOutputEventBlock MidiOutputEventBlock { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] MidiOutputNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ProvidesUserInterface { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ShortName { get; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUAudioUnitBus --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnitBus</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldAllocateBuffer { get; set; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnitBus -->
<!-- start type AUAudioUnit_AUAudioInputOutputUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit_AUAudioInputOutputUnit</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetDeviceId (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetDeviceInputLatency (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetDeviceOutputLatency (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsRunning (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool SetDeviceId (AUAudioUnit This, uint deviceID, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit_AUAudioInputOutputUnit -->
<!-- start type AUSpatializationAlgorithm --> <div>
<h3>Type Changed: AudioUnit.AUSpatializationAlgorithm</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HrtfHQ = 6,</span>
</pre>
</div>

</div> <!-- end type AUSpatializationAlgorithm -->
<!-- start type AudioComponent --> <div>
<h3>Type Changed: AudioUnit.AudioComponent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public AudioComponentInfo[] ComponentList { get; set; }</span>
</pre>
</div>

</div> <!-- end type AudioComponent -->
<!-- start type AudioUnit --> <div>
<h3>Type Changed: AudioUnit.AudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AudioUnitStatus ScheduleParameter (AudioUnitParameterEvent inParameterEvent, uint inNumParamEvents);</span>
</pre>
</div>

</div> <!-- end type AudioUnit -->
<!-- start type AudioUnitStatus --> <div>
<h3>Type Changed: AudioUnit.AudioUnitStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExtensionNotFound = -66744,</span>
	<span class='added added-field ' data-is-non-breaking="">MidiOutputBufferFull = -66753,</span>
</pre>
</div>

</div> <!-- end type AudioUnitStatus -->
<div> <!-- start type AUMidiOutputEventBlock -->
<h3>New Type AudioUnit.AUMidiOutputEventBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUMidiOutputEventBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUMidiOutputEventBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (long eventSampleTime, byte cable, nint length, IntPtr midiBytes, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Invoke (long eventSampleTime, byte cable, nint length, IntPtr midiBytes);</span>
}
</pre>
</div> <!-- end type AUMidiOutputEventBlock -->
<div> <!-- start type AUParameterEventType -->
<h3>New Type AudioUnit.AUParameterEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AUParameterEventType {
	<span class='added added-field ' data-is-non-breaking="">Immediate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Ramped = 2,</span>
}
</pre>
</div> <!-- end type AUParameterEventType -->
<div> <!-- start type AudioComponentInfo -->
<h3>New Type AudioUnit.AudioComponentInfo</h3>
<pre class='added' data-is-non-breaking="">
public class AudioComponentInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AudioComponentInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AudioComponentInfo (Foundation.NSDictionary dic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FactoryFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Manufacturer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ResourceUsageInfo ResourceUsage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? SandboxSafe { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subtype { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Tags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? Version { get; set; }</span>
}
</pre>
</div> <!-- end type AudioComponentInfo -->
<div> <!-- start type AudioUnitParameterEvent -->
<h3>New Type AudioUnit.AudioUnitParameterEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AudioUnitParameterEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint Element;</span>
	<span class='added added-field ' data-is-non-breaking="">public AUParameterEventType EventType;</span>
	<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct EventValues;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Parameter;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Scope;</span>

	// inner types
	public struct EventValuesStruct {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct.ImmediateStruct Immediate;</span>
		<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct.RampStruct Ramp;</span>

		// inner types
		public struct ImmediateStruct {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public uint BufferOffset;</span>
			<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
		}
		public struct RampStruct {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public uint DurationInFrames;</span>
			<span class='added added-field ' data-is-non-breaking="">public float EndValue;</span>
			<span class='added added-field ' data-is-non-breaking="">public int StartBufferOffset;</span>
			<span class='added added-field ' data-is-non-breaking="">public float StartValue;</span>
		}
	}
}
</pre>
</div> <!-- end type AudioUnitParameterEvent -->
<div> <!-- start type ResourceUsageInfo -->
<h3>New Type AudioUnit.ResourceUsageInfo</h3>
<pre class='added' data-is-non-breaking="">
public class ResourceUsageInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ResourceUsageInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ResourceUsageInfo (Foundation.NSDictionary dic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string[] IOKitUserClient { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] MachLookUpGlobalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NetworkClient { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? TemporaryExceptionReadWrite { get; set; }</span>
}
</pre>
</div> <!-- end type ResourceUsageInfo -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: CloudKit.CKErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ResponseLost = 34,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->
<!-- start type CKFetchDatabaseChangesOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchDatabaseChangesOperation</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecordZoneID&gt; WasPurged { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKFetchDatabaseChangesOperation -->
<!-- start type CKFetchRecordZoneChangesOptions --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZoneChangesOptions</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CKFetchRecordZoneChangesOptions -->
<!-- start type CKNotification --> <div>
<h3>Type Changed: CloudKit.CKNotification</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SubtitleLocalizationArgs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubtitleLocalizationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] TitleLocalizationArgs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TitleLocalizationKey { get; }</span>
</pre>
</div>

</div> <!-- end type CKNotification -->
<!-- start type CKNotificationInfo --> <div>
<h3>Type Changed: CloudKit.CKNotificationInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CollapseIdKey { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldSendMutableContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SubtitleLocalizationArgs { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubtitleLocalizationKey { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] TitleLocalizationArgs { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TitleLocalizationKey { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKNotificationInfo -->
<!-- start type CKOperation --> <div>
<h3>Type Changed: CloudKit.CKOperation</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKOperationConfiguration Configuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKOperationGroup Group { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKOperation -->
<!-- start type CKUserIdentity --> <div>
<h3>Type Changed: CloudKit.CKUserIdentity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ContactIdentifiers { get; }</span>
</pre>
</div>

</div> <!-- end type CKUserIdentity -->
<div> <!-- start type CKOperationConfiguration -->
<h3>New Type CloudKit.CKOperationConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class CKOperationConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKOperationConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKOperationConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKOperationConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKOperationConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCellularAccess { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKContainer Container { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LongLived { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSQualityOfService QualityOfService { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForRequest { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForResource { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKOperationConfiguration -->
<div> <!-- start type CKOperationGroup -->
<h3>New Type CloudKit.CKOperationGroup</h3>
<pre class='added' data-is-non-breaking="">
public class CKOperationGroup : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKOperationGroup (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKOperationGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKOperationGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKOperationConfiguration DefaultConfiguration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKOperationGroupTransferSize ExpectedReceiveSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKOperationGroupTransferSize ExpectedSendSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string OperationGroupId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Quantity { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKOperationGroup -->
<div> <!-- start type CKOperationGroupTransferSize -->
<h3>New Type CloudKit.CKOperationGroupTransferSize</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKOperationGroupTransferSize {
	<span class='added added-field ' data-is-non-breaking="">Gigabytes = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HundredsOfGigabytes = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HundredsOfMegabytes = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Kilobytes = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Megabytes = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TensOfGigabytes = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TensOfMegabytes = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKOperationGroupTransferSize -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContact --> <div>
<h3>Type Changed: Contacts.CNContact</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderWriting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] WritableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] WritableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSItemProviderRepresentationVisibility GetItemProviderVisibilityForTypeIdentifier (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.INSItemProviderReading GetObject (Foundation.NSData data, string typeIdentifier, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSProgress LoadData (string typeIdentifier, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync (string typeIdentifier, Foundation.NSProgress result);</span>
</pre>
</div>

</div> <!-- end type CNContact -->
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
	<span class='added added-field ' data-is-non-breaking="">VCardMalformed = 700,</span>
</pre>
</div>

</div> <!-- end type CNErrorCode -->
<!-- start type CNLabelContactRelationKey --> <div>
<h3>Type Changed: Contacts.CNLabelContactRelationKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Daughter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Son { get; }</span>
</pre>
</div>

</div> <!-- end type CNLabelContactRelationKey -->
<!-- start type CNMutableContact --> <div>
<h3>Type Changed: Contacts.CNMutableContact</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderWriting</span>
</pre>
</div>

</div> <!-- end type CNMutableContact -->
<!-- start type CNPostalAddressKeyOption --> <div>
<h3>Type Changed: Contacts.CNPostalAddressKeyOption</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SubAdministrativeArea = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SubLocality = 6,</span>
</pre>
</div>

</div> <!-- end type CNPostalAddressKeyOption -->
<!-- start type CNSocialProfile --> <div>
<h3>Type Changed: Contacts.CNSocialProfile</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string LocalizeProperty (CNPostalAddressKeyOption key);</span>
</pre>
</div>

</div> <!-- end type CNSocialProfile -->
<div> <!-- start type CNPostalAddressKeyOptionExtensions -->
<h3>New Type Contacts.CNPostalAddressKeyOptionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CNPostalAddressKeyOptionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CNPostalAddressKeyOption self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CNPostalAddressKeyOption GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CNPostalAddressKeyOptionExtensions -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CAAnimation FromSCNAnimation (SceneKit.SCNAnimation animation);</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAConstraint --> <div>
<h3>Type Changed: CoreAnimation.CAConstraint</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAConstraint -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CACornerMask MaskedCorners { get; set; }</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsNextDrawableTimeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaySyncEnabled { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAOpenGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAOpenGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAOpenGLLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->
<div> <!-- start type CACornerMask -->
<h3>New Type CoreAnimation.CACornerMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CACornerMask {
	<span class='added added-field ' data-is-non-breaking="">MaxXMaxYCorner = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxXMinYCorner = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMaxYCorner = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMinYCorner = 1,</span>
}
</pre>
</div> <!-- end type CACornerMask -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreAudioKit --> <div> 
<h2>Namespace CoreAudioKit</h2>
<div> <!-- start type AUAudioUnitViewConfiguration -->
<h3>New Type CoreAudioKit.AUAudioUnitViewConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class AUAudioUnitViewConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AUAudioUnitViewConfiguration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AUAudioUnitViewConfiguration (nfloat width, nfloat height, bool hostHasController);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HostHasController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewConfiguration -->
<div> <!-- start type AUAudioUnitViewControllerExtensions -->
<h3>New Type CoreAudioKit.AUAudioUnitViewControllerExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AUAudioUnitViewControllerExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSIndexSet GetSupportedViewConfigurations (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration[] availableViewConfigurations);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SelectViewConfiguration (AudioUnit.AUAudioUnit This, AUAudioUnitViewConfiguration viewConfiguration);</span>
}
</pre>
</div> <!-- end type AUAudioUnitViewControllerExtensions -->

</div> <!-- end namespace CoreAudioKit -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBCentral --> <div>
<h3>Type Changed: CoreBluetooth.CBCentral</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBPeer</span>

</div> <!-- end type CBCentral -->
<!-- start type CBCentralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManager</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBManager</span>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsScanning { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionNotifyOnConnectionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionNotifyOnNotificationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionRestoreIdentifierKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStatePeripheralsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateScanOptionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateScanServicesKey { get; }</span>
</pre>
</div>

</div> <!-- end type CBCentralManager -->
<!-- start type CBCharacteristic --> <div>
<h3>Type Changed: CoreBluetooth.CBCharacteristic</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBAttribute</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CBUUID UUID { get; set; }</span>
</pre>

</div> <!-- end type CBCharacteristic -->
<!-- start type CBDescriptor --> <div>
<h3>Type Changed: CoreBluetooth.CBDescriptor</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBAttribute</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CBUUID UUID { get; }</span>
</pre>

</div> <!-- end type CBDescriptor -->
<!-- start type CBError --> <div>
<h3>Type Changed: CoreBluetooth.CBError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnknownDevice = 12,</span>
</pre>
</div>

</div> <!-- end type CBError -->
<!-- start type CBMutableService --> <div>
<h3>Type Changed: CoreBluetooth.CBMutableService</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> CBUUID UUID { get; set; }
</div></pre>

</div> <!-- end type CBMutableService -->
<!-- start type CBPeripheral --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheral</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBPeer</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSUuid Identifier { get; }</span>
</pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanSendWriteWithoutResponse { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralOpenL2CapChannelEventArgs&gt; DidOpenL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler IsReadyToSendWriteWithoutResponse;</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenL2CapChannel (ushort psm);</span>
</pre>
</div>

</div> <!-- end type CBPeripheral -->
<!-- start type CBPeripheralDelegate --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOpenL2CapChannel (CBPeripheral peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void IsReadyToSendWriteWithoutResponse (CBPeripheral peripheral);</span>
</pre>
</div>

</div> <!-- end type CBPeripheralDelegate -->
<!-- start type CBPeripheralDelegate_Extensions --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidOpenL2CapChannel (ICBPeripheralDelegate This, CBPeripheral peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsReadyToSendWriteWithoutResponse (ICBPeripheralDelegate This, CBPeripheral peripheral);</span>
</pre>
</div>

</div> <!-- end type CBPeripheralDelegate_Extensions -->
<!-- start type CBPeripheralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManager</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBManager</span>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerOpenL2CapChannelEventArgs&gt; DidOpenL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerL2CapChannelOperationEventArgs&gt; DidPublishL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerL2CapChannelOperationEventArgs&gt; DidUnpublishL2CapChannel;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PublishL2CapChannel (bool encryptionRequired);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnpublishL2CapChannel (ushort psm);</span>
</pre>
</div>

</div> <!-- end type CBPeripheralManager -->
<!-- start type CBPeripheralManagerDelegate --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManagerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOpenL2CapChannel (CBPeripheralManager peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidPublishL2CapChannel (CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnpublishL2CapChannel (CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type CBPeripheralManagerDelegate -->
<!-- start type CBPeripheralManagerDelegate_Extensions --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManagerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidOpenL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidPublishL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnpublishL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type CBPeripheralManagerDelegate_Extensions -->
<!-- start type CBService --> <div>
<h3>Type Changed: CoreBluetooth.CBService</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBAttribute</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual CBUUID UUID { get; }</span>
</pre>

</div> <!-- end type CBService -->
<!-- start type CBUUID --> <div>
<h3>Type Changed: CoreBluetooth.CBUUID</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString L2CapPsmCharacteristicString { get; }</span>
</pre>
</div>

</div> <!-- end type CBUUID -->
<div> <!-- start type CBAttribute -->
<h3>New Type CoreBluetooth.CBAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class CBAttribute : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBAttribute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBAttribute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBUUID UUID { get; set; }</span>
}
</pre>
</div> <!-- end type CBAttribute -->
<div> <!-- start type CBL2CapChannel -->
<h3>New Type CoreBluetooth.CBL2CapChannel</h3>
<pre class='added' data-is-non-breaking="">
public class CBL2CapChannel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBL2CapChannel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBL2CapChannel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBL2CapChannel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSInputStream InputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSOutputStream OutputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBPeer Peer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort Psm { get; }</span>
}
</pre>
</div> <!-- end type CBL2CapChannel -->
<div> <!-- start type CBManager -->
<h3>New Type CoreBluetooth.CBManager</h3>
<pre class='added' data-is-non-breaking="">
public class CBManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBManagerState State { get; }</span>
}
</pre>
</div> <!-- end type CBManager -->
<div> <!-- start type CBPeer -->
<h3>New Type CoreBluetooth.CBPeer</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeer : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Identifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type CBPeer -->
<div> <!-- start type CBPeripheralManagerL2CapChannelOperationEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerL2CapChannelOperationEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerL2CapChannelOperationEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerL2CapChannelOperationEventArgs (ushort psm, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ushort Psm { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerL2CapChannelOperationEventArgs -->
<div> <!-- start type CBPeripheralManagerOpenL2CapChannelEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerOpenL2CapChannelEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerOpenL2CapChannelEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerOpenL2CapChannelEventArgs (CBL2CapChannel channel, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBL2CapChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerOpenL2CapChannelEventArgs -->
<div> <!-- start type CBPeripheralOpenL2CapChannelEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralOpenL2CapChannelEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralOpenL2CapChannelEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralOpenL2CapChannelEventArgs (CBL2CapChannel channel, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBL2CapChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralOpenL2CapChannelEventArgs -->

</div> <!-- end namespace CoreBluetooth -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BinaryStoreInsecureDecodingCompatibilityOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BinaryStoreSecureDecodingClasses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CoreSpotlightExporter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UbiquitousContainerIdentifierKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken (Foundation.NSCoder coder);</span>
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

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSPropertyDescription&gt; UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGColorConversionOptions --> <div>
<h3>Type Changed: CoreGraphics.CGColorConversionOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CGSize? TrcSize { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGColorConversionOptions -->
<!-- start type CGColorSpace --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpace</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CGColorSpace CreateIccData (CGDataProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGColorSpace CreateIccData (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGColorSpace CreateLab (nfloat[] whitepoint, nfloat[] blackpoint, nfloat[] range);</span>
</pre>
</div>

</div> <!-- end type CGColorSpace -->
<!-- start type CGColorSpaceNames --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpaceNames</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GenericLab { get; }</span>
</pre>
</div>

</div> <!-- end type CGColorSpaceNames -->
<!-- start type CGContext --> <div>
<h3>Type Changed: CoreGraphics.CGContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void ResetClip ();</span>
</pre>
</div>

</div> <!-- end type CGContext -->
<!-- start type CGContextPDF --> <div>
<h3>Type Changed: CoreGraphics.CGContextPDF</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CGContextPDF (CGDataConsumer dataConsumer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGContextPDF (CGDataConsumer dataConsumer, CGPDFInfo info);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGContextPDF (CGDataConsumer dataConsumer, CGRect mediaBox);</span>
</pre>
</div>

</div> <!-- end type CGContextPDF -->
<!-- start type CGPDFDocument --> <div>
<h3>Type Changed: CoreGraphics.CGPDFDocument</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CGPDFAccessPermissions GetAccessPermissions ();</span>
	<span class='added added-method ' data-is-non-breaking="">public CGPDFOutlineOptions GetOutline ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetOutline (CGPDFOutlineOptions options);</span>
</pre>
</div>

</div> <!-- end type CGPDFDocument -->
<!-- start type CGPDFInfo --> <div>
<h3>Type Changed: CoreGraphics.CGPDFInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CGPDFAccessPermissions? AccessPermissions { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGPDFInfo -->
<div> <!-- start type CGPDFAccessPermissions -->
<h3>New Type CoreGraphics.CGPDFAccessPermissions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGPDFAccessPermissions {
	<span class='added added-field ' data-is-non-breaking="">AllowsCommenting = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsContentAccessibility = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsContentCopying = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsDocumentAssembly = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsDocumentChanges = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsFormFieldEntry = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsHighQualityPrinting = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowsLowQualityPrinting = 1,</span>
}
</pre>
</div> <!-- end type CGPDFAccessPermissions -->
<div> <!-- start type CGPDFOutlineOptions -->
<h3>New Type CoreGraphics.CGPDFOutlineOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CGPDFOutlineOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGPDFOutlineOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGPDFOutlineOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CGRect? DestinationRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary[] OutlineChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSObject OutlineDestination { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string OutlineTitle { get; set; }</span>
}
</pre>
</div> <!-- end type CGPDFOutlineOptions -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIContext --> <div>
<h3>Type Changed: CoreImage.CIContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CIImage image, IOSurface.IOSurface surface, CoreGraphics.CGRect bounds, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIContext -->
<!-- start type CIContext_ImageRepresentation --> <div>
<h3>Type Changed: CoreImage.CIContext_ImageRepresentation</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetHeifRepresentation (CIContext This, CIImage image, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetPngRepresentation (CIContext This, CIImage image, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteHeifRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WritePngRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type CIContext_ImageRepresentation -->
<!-- start type CIImage --> <div>
<h3>Type Changed: CoreImage.CIImage</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (IOSurface.IOSurface surface);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (IOSurface.IOSurface surface, CIImageInitializationOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (IOSurface.IOSurface surface, Foundation.NSDictionary options);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFilterShape Definition { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVDepthData DepthData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatL16 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatL8 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLA16 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLA8 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLAf { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLAh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLf { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLh { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByApplyingOrientation (ImageIO.CGImagePropertyOrientation orientation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByFiltering (string filterName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImage FromSurface (IOSurface.IOSurface surface);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImage FromSurface (IOSurface.IOSurface surface, CIImageInitializationOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImage FromSurface (IOSurface.IOSurface surface, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform GetImageTransform (ImageIO.CGImagePropertyOrientation orientation);</span>
</pre>
</div>

</div> <!-- end type CIImage -->
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: CoreImage.CIImageAccumulator</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("The default initializer does not work in recent iOS version (11b4).")]
	public CIImageAccumulator ();</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the overload acceping a 'CIFormat' enum instead of an 'int'.")]
	public CIImageAccumulator (CoreGraphics.CGRect rectangle, int ciImageFormat);</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload acceping a 'CIFormat' enum instead of an 'int'.")]
	public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, int ciImageFormat);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, CIFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIImageProcessorKernel --> <div>
<h3>Type Changed: CoreImage.CIImageProcessorKernel</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool OutputIsOpaque { get; }</span>
</pre>
</div>

</div> <!-- end type CIImageProcessorKernel -->
<!-- start type CIKernel --> <div>
<h3>Type Changed: CoreImage.CIKernel</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIKernel FromFunction (string name, Foundation.NSData data, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIKernel FromFunction (string name, Foundation.NSData data, CIFormat format, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type CIKernel -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIQRCodeDescriptor SymbolDescriptor { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAztecCodeDescriptor -->
<h3>New Type CoreImage.CIAztecCodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CIAztecCodeDescriptor : CoreImage.CIBarcodeDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAztecCodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAztecCodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAztecCodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAztecCodeDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAztecCodeDescriptor (Foundation.NSData errorCorrectedPayload, bool isCompact, nint layerCount, nint dataCodewordCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint DataCodewordCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ErrorCorrectedPayload { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCompact { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint LayerCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIAztecCodeDescriptor CreateDescriptor (Foundation.NSData errorCorrectedPayload, bool isCompact, nint layerCount, nint dataCodewordCount);</span>
}
</pre>
</div> <!-- end type CIAztecCodeDescriptor -->
<div> <!-- start type CIBarcodeDescriptor -->
<h3>New Type CoreImage.CIBarcodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIBarcodeDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CIBarcodeDescriptor -->
<div> <!-- start type CIBlendKernel -->
<h3>New Type CoreImage.CIBlendKernel</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendKernel : CoreImage.CIColorKernel, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendKernel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Clear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Color { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ColorBurn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ColorDodge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ComponentAdd { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ComponentMax { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ComponentMin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ComponentMultiply { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Darken { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel DarkerColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Destination { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel DestinationAtop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel DestinationIn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel DestinationOut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel DestinationOver { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Difference { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Divide { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Exclusion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel ExclusiveOr { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel HardLight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel HardMix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Hue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Lighten { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel LighterColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel LinearBurn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel LinearDodge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel LinearLight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Luminosity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Multiply { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Overlay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel PinLight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Saturation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Screen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel SoftLight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Source { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel SourceAtop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel SourceIn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel SourceOut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel SourceOver { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel Subtract { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIBlendKernel VividLight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage Apply (CIImage foreground, CIImage background);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIBlendKernel CreateKernel (string string);</span>
}
</pre>
</div> <!-- end type CIBlendKernel -->
<div> <!-- start type CIContext_CIRenderDestination -->
<h3>New Type CoreImage.CIContext_CIRenderDestination</h3>
<pre class='added' data-is-non-breaking="">
public static class CIContext_CIRenderDestination {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool PrepareRender (CIContext This, CIImage image, CoreGraphics.CGRect fromRect, CIRenderDestination destination, CoreGraphics.CGPoint atPoint, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIRenderTask StartTaskToClear (CIContext This, CIRenderDestination destination, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIRenderTask StartTaskToRender (CIContext This, CIImage image, CIRenderDestination destination, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIRenderTask StartTaskToRender (CIContext This, CIImage image, CoreGraphics.CGRect fromRect, CIRenderDestination destination, CoreGraphics.CGPoint atPoint, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIContext_CIRenderDestination -->
<div> <!-- start type CIDataMatrixCodeDescriptor -->
<h3>New Type CoreImage.CIDataMatrixCodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CIDataMatrixCodeDescriptor : CoreImage.CIBarcodeDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDataMatrixCodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDataMatrixCodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDataMatrixCodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDataMatrixCodeDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDataMatrixCodeDescriptor (Foundation.NSData errorCorrectedPayload, nint rowCount, nint columnCount, CIDataMatrixCodeEccVersion eccVersion);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ColumnCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIDataMatrixCodeEccVersion EccVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ErrorCorrectedPayload { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint RowCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIDataMatrixCodeDescriptor CreateDescriptor (Foundation.NSData errorCorrectedPayload, nint rowCount, nint columnCount, CIDataMatrixCodeEccVersion eccVersion);</span>
}
</pre>
</div> <!-- end type CIDataMatrixCodeDescriptor -->
<div> <!-- start type CIDataMatrixCodeEccVersion -->
<h3>New Type CoreImage.CIDataMatrixCodeEccVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CIDataMatrixCodeEccVersion {
	<span class='added added-field ' data-is-non-breaking="">V000 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">V050 = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">V080 = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">V100 = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">V140 = 140,</span>
	<span class='added added-field ' data-is-non-breaking="">V200 = 200,</span>
}
</pre>
</div> <!-- end type CIDataMatrixCodeEccVersion -->
<div> <!-- start type CIImageProcessorInput_Extensions -->
<h3>New Type CoreImage.CIImageProcessorInput_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CIImageProcessorInput_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IOSurface.IOSurface GetSurface (ICIImageProcessorInput This);</span>
}
</pre>
</div> <!-- end type CIImageProcessorInput_Extensions -->
<div> <!-- start type CIImageProcessorOutput_Extensions -->
<h3>New Type CoreImage.CIImageProcessorOutput_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CIImageProcessorOutput_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IOSurface.IOSurface GetSurface (ICIImageProcessorOutput This);</span>
}
</pre>
</div> <!-- end type CIImageProcessorOutput_Extensions -->
<div> <!-- start type CIImageRepresentationOptions -->
<h3>New Type CoreImage.CIImageRepresentationOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CIImageRepresentationOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageRepresentationOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageRepresentationOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float? LossyCompressionQuality { get; set; }</span>
}
</pre>
</div> <!-- end type CIImageRepresentationOptions -->
<div> <!-- start type CIPdf417CodeDescriptor -->
<h3>New Type CoreImage.CIPdf417CodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CIPdf417CodeDescriptor : CoreImage.CIBarcodeDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIPdf417CodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIPdf417CodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIPdf417CodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIPdf417CodeDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIPdf417CodeDescriptor (Foundation.NSData errorCorrectedPayload, bool isCompact, nint rowCount, nint columnCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ColumnCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ErrorCorrectedPayload { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCompact { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint RowCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIPdf417CodeDescriptor CreateDescriptor (Foundation.NSData errorCorrectedPayload, bool isCompact, nint rowCount, nint columnCount);</span>
}
</pre>
</div> <!-- end type CIPdf417CodeDescriptor -->
<div> <!-- start type CIQRCodeDescriptor -->
<h3>New Type CoreImage.CIQRCodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CIQRCodeDescriptor : CoreImage.CIBarcodeDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIQRCodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIQRCodeDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeDescriptor (Foundation.NSData errorCorrectedPayload, nint symbolVersion, byte maskPattern, CIQRCodeErrorCorrectionLevel errorCorrectionLevel);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ErrorCorrectedPayload { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIQRCodeErrorCorrectionLevel ErrorCorrectionLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual byte MaskPattern { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SymbolVersion { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIQRCodeDescriptor CreateDescriptor (Foundation.NSData errorCorrectedPayload, nint symbolVersion, byte maskPattern, CIQRCodeErrorCorrectionLevel errorCorrectionLevel);</span>
}
</pre>
</div> <!-- end type CIQRCodeDescriptor -->
<div> <!-- start type CIQRCodeErrorCorrectionLevel -->
<h3>New Type CoreImage.CIQRCodeErrorCorrectionLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CIQRCodeErrorCorrectionLevel {
	<span class='added added-field ' data-is-non-breaking="">H = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">L = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">M = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">Q = 81,</span>
}
</pre>
</div> <!-- end type CIQRCodeErrorCorrectionLevel -->
<div> <!-- start type CIRenderDestination -->
<h3>New Type CoreImage.CIRenderDestination</h3>
<pre class='added' data-is-non-breaking="">
public class CIRenderDestination : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderDestination (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (IOSurface.IOSurface surface);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderDestination (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (Metal.IMTLTexture texture, Metal.IMTLCommandBuffer commandBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (uint texture, uint target, uint width, uint height);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (IntPtr data, uint width, uint height, uint bytesPerRow, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRenderDestination (uint width, uint height, Metal.MTLPixelFormat pixelFormat, Metal.IMTLCommandBuffer commandBuffer, System.Func&lt;Metal.IMTLTexture&gt; block);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CIRenderDestinationAlphaMode AlphaMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIBlendKernel BlendKernel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool BlendsInDestinationColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Clamped { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Dithered { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Flipped { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; }</span>
}
</pre>
</div> <!-- end type CIRenderDestination -->
<div> <!-- start type CIRenderDestinationAlphaMode -->
<h3>New Type CoreImage.CIRenderDestinationAlphaMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CIRenderDestinationAlphaMode {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Premultiplied = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unpremultiplied = 2,</span>
}
</pre>
</div> <!-- end type CIRenderDestinationAlphaMode -->
<div> <!-- start type CIRenderInfo -->
<h3>New Type CoreImage.CIRenderInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CIRenderInfo : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double KernelExecutionTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PassCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsProcessed { get; }</span>
}
</pre>
</div> <!-- end type CIRenderInfo -->
<div> <!-- start type CIRenderTask -->
<h3>New Type CoreImage.CIRenderTask</h3>
<pre class='added' data-is-non-breaking="">
public class CIRenderTask : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderTask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIRenderTask (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CIRenderInfo WaitUntilCompleted (Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIRenderTask -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->
<!-- start type CLPlacemark --> <div>
<h3>Type Changed: CoreLocation.CLPlacemark</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Contacts.CNPostalAddress PostalAddress { get; }</span>
</pre>
</div>

</div> <!-- end type CLPlacemark -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMAttachmentBearer --> <div>
<h3>Type Changed: CoreMedia.CMAttachmentBearer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CMAttachmentBearer -->
<!-- start type CMSampleBufferAttachmentSettings --> <div>
<h3>Type Changed: CoreMedia.CMSampleBufferAttachmentSettings</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CMSampleBufferAttachmentSettings ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CMSampleBufferAttachmentSettings (Foundation.NSDictionary dictionary);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsicMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber GradualDecoderRefresh { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? HevcStepwiseTemporalSubLayerAccess { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? HevcSyncSampleNalUnitType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CMHevcTemporalLevelInfoSettings HevcTemporalLevelInfo { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? HevcTemporalSubLayerAccess { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary PostNotificationWhenConsumed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? ResumeOutput { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? SampleReferenceByteOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl SampleReferenceUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? SpeedMultiplier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? TransitionId { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary TrimDurationAtEnd { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary TrimDurationAtStart { get; set; }</span>
</pre>
</div>

</div> <!-- end type CMSampleBufferAttachmentSettings -->
<!-- start type CMVideoFormatDescription --> <div>
<h3>Type Changed: CoreMedia.CMVideoFormatDescription</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CMVideoFormatDescription FromHevcParameterSets (System.Collections.Generic.List&lt;System.Byte[]&gt; parameterSets, int nalUnitHeaderLength, Foundation.NSDictionary extensions, CMFormatDescriptionError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetHevcParameterSet (uint index, uint parameterSetCount, int nalUnitHeaderLength, CMFormatDescriptionError error);</span>
</pre>
</div>

</div> <!-- end type CMVideoFormatDescription -->
<div> <!-- start type CMHevcTemporalLevelInfoSettings -->
<h3>New Type CoreMedia.CMHevcTemporalLevelInfoSettings</h3>
<pre class='added' data-is-non-breaking="">
public class CMHevcTemporalLevelInfoSettings : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CMHevcTemporalLevelInfoSettings ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CMHevcTemporalLevelInfoSettings (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ConstraintIndicatorFlags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? LevelIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ProfileCompatibilityFlags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ProfileIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ProfileSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? TemporalLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? TierFlag { get; set; }</span>
}
</pre>
</div> <!-- end type CMHevcTemporalLevelInfoSettings -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreText --> <div> 
<h2>Namespace CoreText</h2>
<!-- start type CTFontTable --> <div>
<h3>Type Changed: CoreText.CTFontTable</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorBitmapData = 1128416340,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorBitmapLocationData = 1128418371,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorPaletteTable = 1129333068,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorTable = 1129270354,</span>
	<span class='added added-field ' data-is-non-breaking="">CompactFontFormat2 = 1128678962,</span>
	<span class='added added-field ' data-is-non-breaking="">CrossReference = 2020762982,</span>
	<span class='added added-field ' data-is-non-breaking="">FondAndNfntData = 1718578788,</span>
	<span class='added added-field ' data-is-non-breaking="">HorizontalMetricsVariations = 1213612370,</span>
	<span class='added added-field ' data-is-non-breaking="">LanguageTags = 1819566439,</span>
	<span class='added added-field ' data-is-non-breaking="">MathLayoutData = 1296127048,</span>
	<span class='added added-field ' data-is-non-breaking="">Merge = 1296388679,</span>
	<span class='added added-field ' data-is-non-breaking="">Metadata = 1835365473,</span>
	<span class='added added-field ' data-is-non-breaking="">MetricsVariations = 1297498450,</span>
	<span class='added added-field ' data-is-non-breaking="">ScalableVectorGraphics = 1398163232,</span>
	<span class='added added-field ' data-is-non-breaking="">StyleAttributes = 1398030676,</span>
	<span class='added added-field ' data-is-non-breaking="">VerticalMetricsVariations = 1448493394,</span>
</pre>
</div>

</div> <!-- end type CTFontTable -->
<!-- start type CTFontVariationAxes --> <div>
<h3>Type Changed: CoreText.CTFontVariationAxes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? Hidden { get; set; }</span>
</pre>
</div>

</div> <!-- end type CTFontVariationAxes -->
<!-- start type CTFontVariationAxisKey --> <div>
<h3>Type Changed: CoreText.CTFontVariationAxisKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Hidden { get; }</span>
</pre>
</div>

</div> <!-- end type CTFontVariationAxisKey -->
<!-- start type CTStringAttributes --> <div>
<h3>Type Changed: CoreText.CTStringAttributes</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public float? BaselineOffset { get; set; }</span>
</pre>
</div>

</div> <!-- end type CTStringAttributes -->

</div> <!-- end namespace CoreText -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVBuffer --> <div>
<h3>Type Changed: CoreVideo.CVBuffer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CVBuffer -->
<!-- start type CVImageBuffer --> <div>
<h3>Type Changed: CoreVideo.CVImageBuffer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContentLightLevelInfoKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MasteringDisplayColorVolumeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_ITU_R_2100_HLG { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_2084_PQ { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_sRGB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static int GetCodePoint (CVImageBufferColorPrimaries color);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetCodePoint (CVImageBufferTransferFunction function);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int GetCodePoint (CVImageBufferYCbCrMatrix yCbCrMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferColorPrimaries GetColorPrimariesOption (int colorPrimariesCodePoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferTransferFunction GetTransferFunctionOption (int transferFunctionCodePoint);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferYCbCrMatrix GetYCbCrMatrixOption (int yCbCrMatrixCodePoint);</span>
</pre>
</div>

</div> <!-- end type CVImageBuffer -->
<!-- start type CVPixelBuffer --> <div>
<h3>Type Changed: CoreVideo.CVPixelBuffer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (IOSurface.IOSurface surface, CVPixelBufferAttributes pixelBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (IOSurface.IOSurface surface, CVReturn result, CVPixelBufferAttributes pixelBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public IOSurface.IOSurface GetIOSurface ();</span>
</pre>
</div>

</div> <!-- end type CVPixelBuffer -->
<!-- start type CVPixelBufferPool --> <div>
<h3>Type Changed: CoreVideo.CVPixelBufferPool</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContentLightLevelInfoKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MasteringDisplayColorVolumeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_ITU_R_2100_HLG { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_2084_PQ { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_sRGB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }</span>
</pre>
</div>

</div> <!-- end type CVPixelBufferPool -->
<!-- start type CVPixelFormatType --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CV420YpCbCr10BiPlanarFullRange = 2019963440,</span>
	<span class='added added-field ' data-is-non-breaking="">CV420YpCbCr10BiPlanarVideoRange = 2016686640,</span>
	<span class='added added-field ' data-is-non-breaking="">CV422YpCbCr10BiPlanarFullRange = 2019963442,</span>
	<span class='added added-field ' data-is-non-breaking="">CV422YpCbCr10BiPlanarVideoRange = 2016686642,</span>
	<span class='added added-field ' data-is-non-breaking="">CV444YpCbCr10BiPlanarFullRange = 2019963956,</span>
	<span class='added added-field ' data-is-non-breaking="">CV444YpCbCr10BiPlanarVideoRange = 2016687156,</span>
	<span class='added added-field ' data-is-non-breaking="">DepthFloat16 = 1751410032,</span>
	<span class='added added-field ' data-is-non-breaking="">DepthFloat32 = 1717855600,</span>
	<span class='added added-field ' data-is-non-breaking="">DisparityFloat16 = 1751411059,</span>
	<span class='added added-field ' data-is-non-breaking="">DisparityFloat32 = 1717856627,</span>
</pre>
</div>

</div> <!-- end type CVPixelFormatType -->
<div> <!-- start type CVImageBufferColorPrimaries -->
<h3>New Type CoreVideo.CVImageBufferColorPrimaries</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVImageBufferColorPrimaries {
	<span class='added added-field ' data-is-non-breaking="">DciP3 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Ebu3213 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR2020 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR709_2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">P22 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">P3D65 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">SmpteC = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 2,</span>
}
</pre>
</div> <!-- end type CVImageBufferColorPrimaries -->
<div> <!-- start type CVImageBufferColorPrimariesExtensions -->
<h3>New Type CoreVideo.CVImageBufferColorPrimariesExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CVImageBufferColorPrimariesExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CVImageBufferColorPrimaries self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferColorPrimaries GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CVImageBufferColorPrimariesExtensions -->
<div> <!-- start type CVImageBufferTransferFunction -->
<h3>New Type CoreVideo.CVImageBufferTransferFunction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVImageBufferTransferFunction {
	<span class='added added-field ' data-is-non-breaking="">ItuR2020 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR2100Hlg = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR709_2 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SRgb = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Smpte240M1995 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SmpteST2084PQ = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">SmpteST428_1 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UseGamma = 5,</span>
}
</pre>
</div> <!-- end type CVImageBufferTransferFunction -->
<div> <!-- start type CVImageBufferTransferFunctionExtensions -->
<h3>New Type CoreVideo.CVImageBufferTransferFunctionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CVImageBufferTransferFunctionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CVImageBufferTransferFunction self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferTransferFunction GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CVImageBufferTransferFunctionExtensions -->
<div> <!-- start type CVImageBufferYCbCrMatrix -->
<h3>New Type CoreVideo.CVImageBufferYCbCrMatrix</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVImageBufferYCbCrMatrix {
	<span class='added added-field ' data-is-non-breaking="">DciP3 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR2020 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR601_4 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR709_2 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">P3D65 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Smpte240M1995 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 2,</span>
}
</pre>
</div> <!-- end type CVImageBufferYCbCrMatrix -->
<div> <!-- start type CVImageBufferYCbCrMatrixExtensions -->
<h3>New Type CoreVideo.CVImageBufferYCbCrMatrixExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CVImageBufferYCbCrMatrixExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CVImageBufferYCbCrMatrix self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVImageBufferYCbCrMatrix GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CVImageBufferYCbCrMatrixExtensions -->
<div> <!-- start type CVMetalTextureAttributes -->
<h3>New Type CoreVideo.CVMetalTextureAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class CVMetalTextureAttributes : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVMetalTextureAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVMetalTextureAttributes (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Metal.MTLTextureUsage? Usage { get; set; }</span>
}
</pre>
</div> <!-- end type CVMetalTextureAttributes -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace CoreWlan --> <div> 
<h2>Namespace CoreWlan</h2>
<!-- start type CWInterface --> <div>
<h3>Type Changed: CoreWlan.CWInterface</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CWNetwork[] ScanForNetworksWithName (string networkName, bool includeHidden, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public CWNetwork[] ScanForNetworksWithSsid (Foundation.NSData ssid, bool includeHidden, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type CWInterface -->

</div> <!-- end namespace CoreWlan -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKAlarm --> <div>
<h3>Type Changed: EventKit.EKAlarm</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the static methods FromDate or FromTimeInterval to create alarms")]
	public EKAlarm ();</span>
</div></pre>

</div> <!-- end type EKAlarm -->
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public EKEventStore (EKSource[] sources);</span>
</pre>
</div>

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace FinderSync --> <div> 
<h2>Namespace FinderSync</h2>
<!-- start type FIFinderSync --> <div>
<h3>Type Changed: FinderSync.FIFinderSync</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetValues (string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SupportedServiceNames (Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSync -->
<!-- start type FIFinderSyncController --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSDate GetLastUsedDate (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetTagData (Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLastUsedDate (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetLastUsedDateAsync (Foundation.NSDate lastUsedDate, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTagData (Foundation.NSData tagData, Foundation.NSUrl itemUrl, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetTagDataAsync (Foundation.NSData tagData, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncController -->
<!-- start type FIFinderSyncProtocol_Extensions --> <div>
<h3>Type Changed: FinderSync.FIFinderSyncProtocol_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetValues (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl, GetValuesCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt;&gt; GetValuesAsync (IFIFinderSyncProtocol This, string[] attributes, Foundation.NSUrl itemUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] SupportedServiceNames (IFIFinderSyncProtocol This, Foundation.NSUrl itemUrl);</span>
</pre>
</div>

</div> <!-- end type FIFinderSyncProtocol_Extensions -->
<div> <!-- start type GetValuesCompletionHandler -->
<h3>New Type FinderSync.GetValuesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GetValuesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GetValuesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; values, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GetValuesCompletionHandler -->

</div> <!-- end namespace FinderSync -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSArray --> <div>
<h3>Type Changed: Foundation.NSArray</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSArray FromUrl (NSUrl url, NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (NSUrl url, NSError error);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSCocoaError --> <div>
<h3>Type Changed: Foundation.NSCocoaError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CoderInvalidValueError = 4866,</span>
</pre>
</div>

</div> <!-- end type NSCocoaError -->
<!-- start type NSDateComponentsFormatter --> <div>
<h3>Type Changed: Foundation.NSDateComponentsFormatter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ReferenceDate { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDateComponentsFormatter -->
<!-- start type NSDateFormatter --> <div>
<h3>Type Changed: Foundation.NSDateFormatter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFormattingContext FormattingContext { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDateFormatter -->
<!-- start type NSDictionary --> <div>
<h3>Type Changed: Foundation.NSDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDictionary (NSUrl url, NSError error);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; FromUrl (NSUrl url, NSError error);</span>
</pre>
</div>

</div> <!-- end type NSDictionary -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDimension (string symbol);</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSError --> <div>
<h3>Type Changed: Foundation.NSError</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DebugDescriptionErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LocalizedFailureErrorKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSError -->
<!-- start type NSFileCoordinator --> <div>
<h3>Type Changed: Foundation.NSFileCoordinator</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ItemUbiquityAttributesChanged (NSUrl url, Foundation.NSSet&lt;NSString&gt; attributes);</span>
</pre>
</div>

</div> <!-- end type NSFileCoordinator -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetFileProviderServices (NSUrl url, System.Action&lt;Foundation.NSDictionary&lt;NSString,Foundation.NSFileProviderService&gt;&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;NSString,Foundation.NSFileProviderService&gt;&gt; GetFileProviderServicesAsync (NSUrl url);</span>
</pre>
</div>

</div> <!-- end type NSFileManager -->
<!-- start type NSFilePresenter --> <div>
<h3>Type Changed: Foundation.NSFilePresenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSString&gt; PresentedItemObservedUbiquityAttributes { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PresentedItemChangedUbiquityAttributes (Foundation.NSSet&lt;NSString&gt; attributes);</span>
</pre>
</div>

</div> <!-- end type NSFilePresenter -->
<!-- start type NSFilePresenter_Extensions --> <div>
<h3>Type Changed: Foundation.NSFilePresenter_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSSet&lt;NSString&gt; GetPresentedItemObservedUbiquityAttributes (INSFilePresenter This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PresentedItemChangedUbiquityAttributes (INSFilePresenter This, Foundation.NSSet&lt;NSString&gt; attributes);</span>
</pre>
</div>

</div> <!-- end type NSFilePresenter_Extensions -->
<!-- start type NSFileVersion --> <div>
<h3>Type Changed: Foundation.NSFileVersion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersonNameComponents OriginatorNameComponents { get; }</span>
</pre>
</div>

</div> <!-- end type NSFileVersion -->
<!-- start type NSIso8601DateFormatOptions --> <div>
<h3>Type Changed: Foundation.NSIso8601DateFormatOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FractionalSeconds = 2048,</span>
</pre>
</div>

</div> <!-- end type NSIso8601DateFormatOptions -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSItemProvider (INSItemProviderWriting object);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanLoadObject (ObjCRuntime.Class aClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool CanLoadObject (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetRegisteredTypeIdentifiers (NSItemProviderFileOptions fileOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool HasConformingRepresentation (string typeIdentifier, NSItemProviderFileOptions fileOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadDataRepresentation (string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadFileRepresentation (string typeIdentifier, System.Action&lt;NSUrl,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrl&gt; LoadFileRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrl&gt; LoadFileRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadInPlaceFileRepresentation (string typeIdentifier, LoadInPlaceFileRepresentationHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;LoadInPlaceResult&gt; LoadInPlaceFileRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;LoadInPlaceResult&gt; LoadInPlaceFileRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public NSProgress LoadObject&lt;T&gt; (System.Action&lt;T,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadObject (ObjCRuntime.Class aClass, System.Action&lt;INSItemProviderReading,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;T&gt; LoadObjectAsync&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (ObjCRuntime.Class aClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;T&gt; LoadObjectAsync&lt;T&gt; (NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (ObjCRuntime.Class aClass, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterDataRepresentation (string typeIdentifier, NSItemProviderRepresentationVisibility visibility, RegisterDataRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterFileRepresentation (string typeIdentifier, NSItemProviderFileOptions fileOptions, NSItemProviderRepresentationVisibility visibility, RegisterFileRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterObject (INSItemProviderWriting object, NSItemProviderRepresentationVisibility visibility);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterObject (ObjCRuntime.Class aClass, NSItemProviderRepresentationVisibility visibility, RegisterObjectRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RegisterObject (System.Type type, NSItemProviderRepresentationVisibility visibility, RegisterObjectRepresentationLoadHandler loadHandler);</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSJsonWritingOptions --> <div>
<h3>Type Changed: Foundation.NSJsonWritingOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SortedKeys = 2,</span>
</pre>
</div>

</div> <!-- end type NSJsonWritingOptions -->
<!-- start type NSLinguisticTagger --> <div>
<h3>Type Changed: Foundation.NSLinguisticTagger</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DominantLanguage { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateTags (NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, LinguisticTagEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EnumerateTags (string str, NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSOrthography orthography, LinguisticTagEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetAvailableTagSchemes (NSLinguisticTaggerUnit unit, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetDominantLanguage (string str);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetTag (uint charIndex, NSLinguisticTaggerUnit unit, string scheme, NSRange tokenRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetTag (string str, uint charIndex, NSLinguisticTaggerUnit unit, string scheme, NSOrthography orthography, NSRange tokenRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetTags (NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSValue[] tokenRanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetTags (string str, NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSOrthography orthography, NSValue[] tokenRanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetTokenRange (uint charIndex, NSLinguisticTaggerUnit unit);</span>
</pre>
</div>

</div> <!-- end type NSLinguisticTagger -->
<!-- start type NSMetadataItem --> <div>
<h3>Type Changed: Foundation.NSMetadataItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string AcquisitionMake { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string AcquisitionModel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Album { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Altitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Aperture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] AppleLoopDescriptors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string AppleLoopsKeyFilterType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string AppleLoopsLoopMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string AppleLoopsRoot { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] ApplicationCategories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Audiences { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? AudioBitRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? AudioChannelCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string AudioEncodingApplication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? AudioSampleRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? AudioTrackNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] AuthorAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] AuthorEmailAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Authors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? BitsPerSample { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CFBundleIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CameraOwner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string City { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Codecs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Comment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Composer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] ContactKeywords { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate ContentCreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate ContentModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Contributors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Copyright { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Country { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Coverage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Creator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate DateAdded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string DeliveryType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Director { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate DownloadedDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate DueDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? DurationSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Editors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] EmailAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] EncodingApplications { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] ExecutableArchitectures { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExecutablePlatform { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExifGpsVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExifVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ExposureMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExposureProgram { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ExposureTimeSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExposureTimeString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string FinderComment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? FlashOnOff { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? FocalLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FocalLength35mm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Fonts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Genre { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string GpsAreaInformation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate GpsDateStamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDestBearing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDestDistance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDestLatitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDestLongitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDifferental { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsDop { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string GpsMapDatum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string GpsMeasureMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string GpsProcessingMethod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string GpsStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? GpsTrack { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? HasAlphaChannel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Headline { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ImageDirection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Information { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] InstantMessageAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Instructions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsApplicationManaged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsGeneralMidiSequence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsLikelyJunk { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? IsoSpeed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string KeySignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Keywords { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Kind { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Languages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate LastUsedDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Latitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] LayerNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string LensModel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Longitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Lyricist { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? MaxAperture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] MediaTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MeteringMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MusicalGenre { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MusicalInstrumentCategory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string MusicalInstrumentName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string NamedLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? NumberOfPages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Organizations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Orientation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string OriginalFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string OriginalSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? PageHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? PageWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Participants { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Performers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] PhoneNumbers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PixelCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Producer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ProfileName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Projects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Publishers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] RecipientAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] RecipientEmailAddresses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate RecordingDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? RecordingYear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? RedEyeOnOff { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ResolutionHeightDpi { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ResolutionWidthDpi { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Rights { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string SecurityMethod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Speed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? StarRating { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string StateOrProvince { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Streamable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? Tempo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string TextContent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Theme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string TimeSignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? TotalBitRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Version { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? VideoBitRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] WhereFroms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? WhiteBalance { get; }</span>
</pre>
</div>

</div> <!-- end type NSMetadataItem -->
<!-- start type NSMetadataQuery --> <div>
<h3>Type Changed: Foundation.NSMetadataQuery</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AcquisitionMakeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AcquisitionModelKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AlbumKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AltitudeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ApertureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AppleLoopDescriptorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AppleLoopsKeyFilterTypeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AppleLoopsLoopModeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AppleLoopsRootKeyKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ApplicationCategoriesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudiencesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudioBitRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudioChannelCountKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudioEncodingApplicationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudioSampleRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AudioTrackNumberKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AuthorAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AuthorEmailAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString AuthorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString BitsPerSampleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CFBundleIdentifierKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CameraOwnerKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CityKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CodecsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ColorSpaceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CommentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ComposerKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ContactKeywordsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ContentCreationDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ContentModificationDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ContributorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CopyrightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CountryKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CoverageKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString CreatorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DateAddedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DeliveryTypeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DescriptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DirectorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DownloadedDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DueDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DurationSecondsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString EditorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString EmailAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString EncodingApplicationsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExecutableArchitecturesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExecutablePlatformKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExifGpsVersionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExifVersionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExposureModeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExposureProgramKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExposureTimeSecondsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ExposureTimeStringKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FNumberKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FinderCommentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FlashOnOffKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FocalLength35mmKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FocalLengthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString FontsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GenreKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsAreaInformationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDateStampKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDestBearingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDestDistanceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDestLatitudeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDestLongitudeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDifferentalKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsDopKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsMapDatumKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsMeasureModeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsProcessingMethodKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsStatusKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString GpsTrackKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString HasAlphaChannelKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString HeadlineKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString IdentifierKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ImageDirectionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString InformationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString InstantMessageAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString InstructionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString IsApplicationManagedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString IsGeneralMidiSequenceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString IsLikelyJunkKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString IsoSpeedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString KeySignatureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString KeywordsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString KindKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LanguagesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LastUsedDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LatitudeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LayerNamesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LensModelKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LongitudeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LyricistKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MaxApertureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MediaTypesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MeteringModeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MusicalGenreKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MusicalInstrumentCategoryKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString MusicalInstrumentNameKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString NamedLocationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString NumberOfPagesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString OrganizationsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString OrientationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString OriginalFormatKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString OriginalSourceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PageHeightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PageWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ParticipantsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PerformersKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PhoneNumbersKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PixelCountKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PixelHeightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PixelWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ProducerKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ProfileNameKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ProjectsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString PublishersKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RecipientAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RecipientEmailAddressesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RecipientsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RecordingDateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RecordingYearKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RedEyeOnOffKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ResolutionHeightDpiKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ResolutionWidthDpiKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString RightsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString SecurityMethodKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString SpeedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString StarRatingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString StateOrProvinceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString StreamableKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString SubjectKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TempoKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TextContentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ThemeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TimeSignatureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TimestampKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TitleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString TotalBitRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousItemIsSharedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemCurrentUserPermissionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemCurrentUserRoleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemMostRecentEditorNameComponentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemOwnerNameComponentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemPermissionsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemPermissionsReadWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemRoleOwner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemRoleParticipant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VersionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VideoBitRateKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString WhereFromsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString WhiteBalanceKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSMetadataQuery -->
<!-- start type NSMutableString --> <div>
<h3>Type Changed: Foundation.NSMutableString</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderWriting</span>
</pre>
</div>

</div> <!-- end type NSMutableString -->
<!-- start type NSProgress --> <div>
<h3>Type Changed: Foundation.NSProgress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public nint? EstimatedTimeRemaining { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FileCompletedCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FileOperationKind { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FileTotalCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrl FileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Finished { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Throughput { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformAsCurrent (long unitCount, System.Action work);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PerformAsCurrentAsync (long unitCount);</span>
</pre>
</div>

</div> <!-- end type NSProgress -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderWriting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] WritableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] WritableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSItemProviderRepresentationVisibility GetItemProviderVisibilityForTypeIdentifier (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetObject (NSData data, string typeIdentifier, NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadData (string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (string typeIdentifier, NSProgress result);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSTextCheckingResult --> <div>
<h3>Type Changed: Foundation.NSTextCheckingResult</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetRange (string name);</span>
</pre>
</div>

</div> <!-- end type NSTextCheckingResult -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type NSUrl --> <div>
<h3>Type Changed: Foundation.NSUrl</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">INSItemProviderWriting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousItemIsSharedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemCurrentUserPermissionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemCurrentUserRoleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemMostRecentEditorNameComponentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemOwnerNameComponentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemPermissionsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemPermissionsReadWrite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemRoleOwner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString UbiquitousSharedItemRoleParticipant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeAvailableCapacityForImportantUsageKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeAvailableCapacityForOpportunisticUsageKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeIsEncryptedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeIsRootFileSystemKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsAccessPermissionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsCompressionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsExclusiveRenamingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsFileCloningKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsImmutableFilesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsSwapRenamingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] WritableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] WritableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSItemProviderRepresentationVisibility GetItemProviderVisibilityForTypeIdentifier (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl GetObject (NSData data, string typeIdentifier, NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadData (string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (string typeIdentifier, NSProgress result);</span>
</pre>
</div>

</div> <!-- end type NSUrl -->
<!-- start type NSUrlComponents --> <div>
<h3>Type Changed: Foundation.NSUrlComponents</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlQueryItem[] PercentEncodedQueryItems { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUrlComponents -->
<!-- start type NSUrlSessionConfiguration --> <div>
<h3>Type Changed: Foundation.NSUrlSessionConfiguration</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WaitsForConnectivity { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionConfiguration -->
<!-- start type NSUrlSessionDataTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionDataTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionDataTask -->
<!-- start type NSUrlSessionDownloadTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionDownloadTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionDownloadTask -->
<!-- start type NSUrlSessionStreamTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionStreamTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionStreamTask -->
<!-- start type NSUrlSessionTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual long CountOfBytesClientExpectsToReceive { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long CountOfBytesClientExpectsToSend { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate EarliestBeginDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSProgress Progress { get; }</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTask -->
<!-- start type NSUrlSessionTaskDelegate --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TaskIsWaitingForConnectivity (NSUrlSession session, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginDelayedRequest (NSUrlSession session, NSUrlSessionTask task, NSUrlRequest request, System.Action&lt;NSUrlSessionDelayedRequestDisposition,Foundation.NSUrlRequest&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate -->
<!-- start type NSUrlSessionTaskDelegate_Extensions --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void TaskIsWaitingForConnectivity (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginDelayedRequest (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlRequest request, System.Action&lt;NSUrlSessionDelayedRequestDisposition,Foundation.NSUrlRequest&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate_Extensions -->
<!-- start type NSUrlSessionUploadTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionUploadTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionUploadTask -->
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrl ReferrerUrl { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUserActivity -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type INSItemProviderWriting -->
<h3>New Type Foundation.INSItemProviderWriting</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderWriting : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadData (string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type INSItemProviderWriting -->
<div> <!-- start type ItemProviderDataCompletionHandler -->
<h3>New Type Foundation.ItemProviderDataCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ItemProviderDataCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ItemProviderDataCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSData data, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSData data, NSError error);</span>
}
</pre>
</div> <!-- end type ItemProviderDataCompletionHandler -->
<div> <!-- start type LinguisticTagEnumerator -->
<h3>New Type Foundation.LinguisticTagEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate LinguisticTagEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LinguisticTagEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string tag, NSRange tokenRange, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string tag, NSRange tokenRange, bool stop);</span>
}
</pre>
</div> <!-- end type LinguisticTagEnumerator -->
<div> <!-- start type LoadInPlaceFileRepresentationHandler -->
<h3>New Type Foundation.LoadInPlaceFileRepresentationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate LoadInPlaceFileRepresentationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LoadInPlaceFileRepresentationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSUrl fileUrl, bool isInPlace, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSUrl fileUrl, bool isInPlace, NSError error);</span>
}
</pre>
</div> <!-- end type LoadInPlaceFileRepresentationHandler -->
<div> <!-- start type LoadInPlaceResult -->
<h3>New Type Foundation.LoadInPlaceResult</h3>
<pre class='added' data-is-non-breaking="">
public class LoadInPlaceResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LoadInPlaceResult (NSUrl fileUrl, bool isInPlace);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NSUrl FileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsInPlace { get; set; }</span>
}
</pre>
</div> <!-- end type LoadInPlaceResult -->
<div> <!-- start type NSFileProviderService -->
<h3>New Type Foundation.NSFileProviderService</h3>
<pre class='added' data-is-non-breaking="">
public class NSFileProviderService : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderService (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFileProviderService (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
}
</pre>
</div> <!-- end type NSFileProviderService -->
<div> <!-- start type NSItemProviderFileOptions -->
<h3>New Type Foundation.NSItemProviderFileOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSItemProviderFileOptions {
	<span class='added added-field ' data-is-non-breaking="">OpenInPlace = 1,</span>
}
</pre>
</div> <!-- end type NSItemProviderFileOptions -->
<div> <!-- start type NSItemProviderRepresentationVisibility -->
<h3>New Type Foundation.NSItemProviderRepresentationVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSItemProviderRepresentationVisibility {
	<span class='added added-field ' data-is-non-breaking="">All = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Group = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">OwnProcess = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Team = 1,</span>
}
</pre>
</div> <!-- end type NSItemProviderRepresentationVisibility -->
<div> <!-- start type NSItemProviderWriting_Extensions -->
<h3>New Type Foundation.NSItemProviderWriting_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemProviderWriting_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSItemProviderRepresentationVisibility GetItemProviderVisibilityForTypeIdentifier (INSItemProviderWriting This, string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetWritableTypeIdentifiersForItemProvider (INSItemProviderWriting This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (INSItemProviderWriting This, string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (INSItemProviderWriting This, string typeIdentifier, NSProgress result);</span>
}
</pre>
</div> <!-- end type NSItemProviderWriting_Extensions -->
<div> <!-- start type NSLinguisticTaggerUnit -->
<h3>New Type Foundation.NSLinguisticTaggerUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLinguisticTaggerUnit {
	<span class='added added-field ' data-is-non-breaking="">Document = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Sentence = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Word = 0,</span>
}
</pre>
</div> <!-- end type NSLinguisticTaggerUnit -->
<div> <!-- start type NSUrlSessionDelayedRequestDisposition -->
<h3>New Type Foundation.NSUrlSessionDelayedRequestDisposition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSUrlSessionDelayedRequestDisposition {
	<span class='added added-field ' data-is-non-breaking="">Cancel = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ContinueLoading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseNewRequest = 1,</span>
}
</pre>
</div> <!-- end type NSUrlSessionDelayedRequestDisposition -->
<div> <!-- start type NSXpcListenerEndpoint -->
<h3>New Type Foundation.NSXpcListenerEndpoint</h3>
<pre class='added' data-is-non-breaking="">
public class NSXpcListenerEndpoint : Foundation.NSObject, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSXpcListenerEndpoint (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSXpcListenerEndpoint (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSXpcListenerEndpoint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSXpcListenerEndpoint -->
<div> <!-- start type RegisterDataRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterDataRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterDataRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterDataRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ItemProviderDataCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (ItemProviderDataCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterDataRepresentationLoadHandler -->
<div> <!-- start type RegisterFileRepresentationCompletionHandler -->
<h3>New Type Foundation.RegisterFileRepresentationCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterFileRepresentationCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterFileRepresentationCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSUrl fileUrl, bool coordinated, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSUrl fileUrl, bool coordinated, NSError error);</span>
}
</pre>
</div> <!-- end type RegisterFileRepresentationCompletionHandler -->
<div> <!-- start type RegisterFileRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterFileRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterFileRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterFileRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (RegisterFileRepresentationCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (RegisterFileRepresentationCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterFileRepresentationLoadHandler -->
<div> <!-- start type RegisterObjectRepresentationCompletionHandler -->
<h3>New Type Foundation.RegisterObjectRepresentationCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterObjectRepresentationCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterObjectRepresentationCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (INSItemProviderWriting object, NSError error, System.AsyncCallback callback, object _object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (INSItemProviderWriting object, NSError error);</span>
}
</pre>
</div> <!-- end type RegisterObjectRepresentationCompletionHandler -->
<div> <!-- start type RegisterObjectRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterObjectRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterObjectRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterObjectRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (RegisterObjectRepresentationCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (RegisterObjectRepresentationCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterObjectRepresentationLoadHandler -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAttitudeAndRotationRate { get; }</span>
</pre>
</div>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameplayKit --> <div> 
<h2>Namespace GameplayKit</h2>
<!-- start type GKAgent3D --> <div>
<h3>Type Changed: GameplayKit.GKAgent3D</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'Rotation3x3' instead.")]
	public virtual OpenTK.Matrix3 Rotation { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix3 Rotation3x3 { get; set; }</span>
</pre>
</div>

</div> <!-- end type GKAgent3D -->
<!-- start type GKDecisionTree --> <div>
<h3>Type Changed: GameplayKit.GKDecisionTree</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKDecisionTree (Foundation.NSUrl url, Foundation.NSError error);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Export (Foundation.NSUrl url, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type GKDecisionTree -->
<!-- start type GKScene --> <div>
<h3>Type Changed: GameplayKit.GKScene</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static GKScene FromFile (string filename, IGKSceneRootNodeType rootNode);</span>
</pre>
</div>

</div> <!-- end type GKScene -->
<div> <!-- start type GKSCNNodeComponent -->
<h3>New Type GameplayKit.GKSCNNodeComponent</h3>
<pre class='added' data-is-non-breaking="">
public class GKSCNNodeComponent : GameplayKit.GKComponent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, IGKAgentDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKSCNNodeComponent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSCNNodeComponent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSCNNodeComponent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSCNNodeComponent (SceneKit.SCNNode node);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSCNNodeComponent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SceneKit.SCNNode Node { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AgentDidUpdate (GKAgent agent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AgentWillUpdate (GKAgent agent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKSCNNodeComponent FromNode (SceneKit.SCNNode node);</span>
}
</pre>
</div> <!-- end type GKSCNNodeComponent -->
<div> <!-- start type SCNNode_GameplayKit -->
<h3>New Type GameplayKit.SCNNode_GameplayKit</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNNode_GameplayKit {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKEntity GetEntity (SceneKit.SCNNode This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetEntity (SceneKit.SCNNode This, GKEntity entity);</span>
}
</pre>
</div> <!-- end type SCNNode_GameplayKit -->

</div> <!-- end namespace GameplayKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestination --> <div>
<h3>Type Changed: ImageIO.CGImageDestination</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAuxiliaryDataInfo (CGImageAuxiliaryDataType auxiliaryImageDataType, CGImageAuxiliaryDataInfo auxiliaryDataInfo);</span>
</pre>
</div>

</div> <!-- end type CGImageDestination -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileContentsDictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Images { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NamedColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Width { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->
<!-- start type CGImageSource --> <div>
<h3>Type Changed: ImageIO.CGImageSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo CopyAuxiliaryDataInfo (uint index, CGImageAuxiliaryDataType auxiliaryImageDataType);</span>
</pre>
</div>

</div> <!-- end type CGImageSource -->
<div> <!-- start type CGImageAuxiliaryDataInfo -->
<h3>New Type ImageIO.CGImageAuxiliaryDataInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGImageAuxiliaryDataInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary DataDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CGImageMetadata Metadata { get; set; }</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataInfo -->
<div> <!-- start type CGImageAuxiliaryDataType -->
<h3>New Type ImageIO.CGImageAuxiliaryDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGImageAuxiliaryDataType {
	<span class='added added-field ' data-is-non-breaking="">Depth = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disparity = 1,</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataType -->
<div> <!-- start type CGImageAuxiliaryDataTypeExtensions -->
<h3>New Type ImageIO.CGImageAuxiliaryDataTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CGImageAuxiliaryDataTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CGImageAuxiliaryDataType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGImageAuxiliaryDataType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataTypeExtensions -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INCallRecordType --> <div>
<h3>Type Changed: Intents.INCallRecordType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Latest = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 5,</span>
</pre>
</div>

</div> <!-- end type INCallRecordType -->
<!-- start type INDateComponentsRange --> <div>
<h3>Type Changed: Intents.INDateComponentsRange</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (EventKit.EKRecurrenceRule recurrenceRule);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSDateComponents startDateComponents, Foundation.NSDateComponents endDateComponents, INRecurrenceRule recurrenceRule);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual EventKit.EKRecurrenceRule EKRecurrenceRule { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRecurrenceRule RecurrenceRule { get; }</span>
</pre>
</div>

</div> <!-- end type INDateComponentsRange -->
<!-- start type INImage --> <div>
<h3>Type Changed: Intents.INImage</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromUrl (Foundation.NSUrl url, double width, double height);</span>
</pre>
</div>

</div> <!-- end type INImage -->
<!-- start type INIntent --> <div>
<h3>Type Changed: Intents.INIntent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string IntentDescription { get; }</span>
</pre>
</div>

</div> <!-- end type INIntent -->
<!-- start type INMessage --> <div>
<h3>Type Changed: Intents.INMessage</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string conversationIdentifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients, INMessageType messageType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string conversationIdentifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients, INSpeakableString groupName, INMessageType messageType);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ConversationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessageType MessageType { get; }</span>
</pre>
</div>

</div> <!-- end type INMessage -->
<!-- start type INMessageAttribute --> <div>
<h3>Type Changed: Intents.INMessageAttribute</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Played = 5,</span>
</pre>
</div>

</div> <!-- end type INMessageAttribute -->
<!-- start type INMessageAttributeOptions --> <div>
<h3>Type Changed: Intents.INMessageAttributeOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Played = 16,</span>
</pre>
</div>

</div> <!-- end type INMessageAttributeOptions -->
<!-- start type INPerson --> <div>
<h3>Type Changed: Intents.INPerson</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IINSpeakable[] AlternativeSpeakableMatches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsMe { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VocabularyIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type INPerson -->
<!-- start type INSearchCallHistoryIntent --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntent</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities, INCallRecordTypeOptions callTypes, Foundation.NSNumber unseen);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities, INCallRecordTypeOptions callTypes, bool unseen);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordTypeOptions CallTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Unseen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakUnseen { get; }</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntent -->
<!-- start type INSearchCallHistoryIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCallTypes (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INCallRecordTypeOptionsResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentHandling_Extensions -->
<!-- start type INSearchCallHistoryIntentResponse --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecord[] CallRecords { get; set; }</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentResponse -->
<!-- start type INSearchCallHistoryIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InProgress = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 7,</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentResponseCode -->
<!-- start type INSearchForMessagesIntent --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (INPerson[] recipients, INPerson[] senders, string[] searchTerms, INMessageAttributeOptions attributes, INDateComponentsRange dateTimeRange, string[] identifiers, string[] notificationIdentifiers, INSpeakableString[] speakableGroupNames);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString[] SpeakableGroupNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SpeakableGroupNamesOperator { get; }</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntent -->
<!-- start type INSearchForMessagesIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpeakableGroupNames (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INSpeakableStringResolutionResult[]&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntentHandling_Extensions -->
<!-- start type INSearchForMessagesIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureMessageTooManyResults = 7,</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntentResponseCode -->
<!-- start type INSendMessageIntent --> <div>
<h3>Type Changed: Intents.INSendMessageIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (INPerson[] recipients, string content, INSpeakableString speakableGroupName, string conversationIdentifier, string serviceName, INPerson sender);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ConversationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString SpeakableGroupName { get; }</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntent -->
<!-- start type INSendMessageIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSendMessageIntentHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSendMessageRecipientResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpeakableGroupName (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntentHandling_Extensions -->
<!-- start type INSendMessageIntentResponse --> <div>
<h3>Type Changed: Intents.INSendMessageIntentResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessage SentMessage { get; set; }</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntentResponse -->
<!-- start type INSpeakableString --> <div>
<h3>Type Changed: Intents.INSpeakableString</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IINSpeakable[] AlternativeSpeakableMatches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VocabularyIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type INSpeakableString -->
<!-- start type INStartAudioCallIntent --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (INCallDestinationType destinationType, INPerson[] contacts);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallDestinationType DestinationType { get; }</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntent -->
<!-- start type INStartAudioCallIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDestinationType (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INCallDestinationTypeResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntentHandling_Extensions -->
<!-- start type INStartAudioCallIntentResponseCode --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureContactNotSupportedByApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoValidNumber = 8,</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntentResponseCode -->
<!-- start type INStartVideoCallIntentResponseCode --> <div>
<h3>Type Changed: Intents.INStartVideoCallIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureContactNotSupportedByApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureInvalidNumber = 8,</span>
</pre>
</div>

</div> <!-- end type INStartVideoCallIntentResponseCode -->
<div> <!-- start type INCallCapability -->
<h3>New Type Intents.INCallCapability</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallCapability {
	<span class='added added-field ' data-is-non-breaking="">AudioCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoCall = 2,</span>
}
</pre>
</div> <!-- end type INCallCapability -->
<div> <!-- start type INCallDestinationType -->
<h3>New Type Intents.INCallDestinationType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallDestinationType {
	<span class='added added-field ' data-is-non-breaking="">Emergency = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Redial = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 3,</span>
}
</pre>
</div> <!-- end type INCallDestinationType -->
<div> <!-- start type INCallDestinationTypeResolutionResult -->
<h3>New Type Intents.INCallDestinationTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallDestinationTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallDestinationTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallDestinationTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult GetConfirmationRequired (INCallDestinationType callDestinationTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult GetSuccess (INCallDestinationType resolvedCallDestinationType);</span>
}
</pre>
</div> <!-- end type INCallDestinationTypeResolutionResult -->
<div> <!-- start type INCallRecord -->
<h3>New Type Intents.INCallRecord</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecord : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCallRecord (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecord (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecord (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCallRecord (string identifier, Foundation.NSDate dateCreated, INPerson caller, INCallRecordType callRecordType, INCallCapability callCapability, Foundation.NSNumber callDuration, Foundation.NSNumber unseen);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallCapability CallCapability { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? CallDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordType CallRecordType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Caller { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Unseen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakCallDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakUnseen { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INCallRecord -->
<div> <!-- start type INCallRecordTypeOptions -->
<h3>New Type Intents.INCallRecordTypeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INCallRecordTypeOptions {
	<span class='added added-field ' data-is-non-breaking="">Latest = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Missed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 16,</span>
}
</pre>
</div> <!-- end type INCallRecordTypeOptions -->
<div> <!-- start type INCallRecordTypeOptionsResolutionResult -->
<h3>New Type Intents.INCallRecordTypeOptionsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecordTypeOptionsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeOptionsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeOptionsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult GetConfirmationRequired (INCallRecordTypeOptions callRecordTypeOptionsToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult GetSuccess (INCallRecordTypeOptions resolvedCallRecordTypeOptions);</span>
}
</pre>
</div> <!-- end type INCallRecordTypeOptionsResolutionResult -->
<div> <!-- start type INMessageType -->
<h3>New Type Intents.INMessageType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INMessageType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DigitalTouch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Handwriting = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaAddressCard = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaAudio = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaCalendar = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaImage = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaLocation = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaPass = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaVideo = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Sticker = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackDisliked = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackEmphasized = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLaughed = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLiked = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLoved = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackQuestioned = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INMessageType -->
<div> <!-- start type INRecurrenceFrequency -->
<h3>New Type Intents.INRecurrenceFrequency</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRecurrenceFrequency {
	<span class='added added-field ' data-is-non-breaking="">Daily = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Hourly = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Minute = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Monthly = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Weekly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Yearly = 6,</span>
}
</pre>
</div> <!-- end type INRecurrenceFrequency -->
<div> <!-- start type INRecurrenceRule -->
<h3>New Type Intents.INRecurrenceRule</h3>
<pre class='added' data-is-non-breaking="">
public class INRecurrenceRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRecurrenceRule (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRecurrenceRule (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRecurrenceRule (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRecurrenceRule (uint interval, INRecurrenceFrequency frequency);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRecurrenceFrequency Frequency { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Interval { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRecurrenceRule -->
<div> <!-- start type INSendMessageRecipientResolutionResult -->
<h3>New Type Intents.INSendMessageRecipientResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageRecipientResolutionResult : Intents.INPersonResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageRecipientResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageRecipientResolutionResult (INPersonResolutionResult personResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageRecipientResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult GetUnsupported (INSendMessageRecipientUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INSendMessageRecipientResolutionResult -->
<div> <!-- start type INSendMessageRecipientUnsupportedReason -->
<h3>New Type Intents.INSendMessageRecipientUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendMessageRecipientUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">MessagingServiceNotEnabledForRecipient = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAccount = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Offline = 2,</span>
}
</pre>
</div> <!-- end type INSendMessageRecipientUnsupportedReason -->
<div> <!-- start type INSpeakable_Extensions -->
<h3>New Type Intents.INSpeakable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSpeakable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IINSpeakable[] GetAlternativeSpeakableMatches (IINSpeakable This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetVocabularyIdentifier (IINSpeakable This);</span>
}
</pre>
</div> <!-- end type INSpeakable_Extensions -->

</div> <!-- end namespace Intents -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InteractionNotAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedReason { get; set; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<!-- start type LAStatus --> <div>
<h3>Type Changed: LocalAuthentication.LAStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BiometryLockout = -8,</span>
	<span class='added added-field ' data-is-non-breaking="">BiometryNotAvailable = -6,</span>
	<span class='added added-field ' data-is-non-breaking="">BiometryNotEnrolled = -7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotInteractive = -1004,</span>
</pre>
</div>

</div> <!-- end type LAStatus -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationView ClusterAnnotationView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ClusteringIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationViewCollisionMode CollisionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float DisplayPriority { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareForDisplay ();</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapType --> <div>
<h3>Type Changed: MapKit.MKMapType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MutedStandard = 5,</span>
</pre>
</div>

</div> <!-- end type MKMapType -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MKCreateClusterAnnotation CreateClusterAnnotation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKAnnotationView DequeueReusableAnnotation (string identifier, IMKAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Register (ObjCRuntime.Class viewClass, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (System.Type viewType, string identifier);</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation CreateClusterAnnotation (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MKClusterAnnotation CreateClusterAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate, Contacts.CNPostalAddress postalAddress);</span>
</pre>
</div>

</div> <!-- end type MKPlacemark -->
<div> <!-- start type MKAnnotationViewCollisionMode -->
<h3>New Type MapKit.MKAnnotationViewCollisionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKAnnotationViewCollisionMode {
	<span class='added added-field ' data-is-non-breaking="">Circle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rectangle = 0,</span>
}
</pre>
</div> <!-- end type MKAnnotationViewCollisionMode -->
<div> <!-- start type MKClusterAnnotation -->
<h3>New Type MapKit.MKClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class MKClusterAnnotation : Foundation.NSObject, Foundation.INSObjectProtocol, IMKAnnotation, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKClusterAnnotation (IMKAnnotation[] memberAnnotations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMKAnnotation[] MemberAnnotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);</span>
}
</pre>
</div> <!-- end type MKClusterAnnotation -->
<div> <!-- start type MKCreateClusterAnnotation -->
<h3>New Type MapKit.MKCreateClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MKCreateClusterAnnotation : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCreateClusterAnnotation (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation[] memberAnnotations, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation Invoke (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
}
</pre>
</div> <!-- end type MKCreateClusterAnnotation -->
<div> <!-- start type MKFeatureDisplayPriority -->
<h3>New Type MapKit.MKFeatureDisplayPriority</h3>
<pre class='added' data-is-non-breaking="">
public static class MKFeatureDisplayPriority {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float Required;</span>
}
</pre>
</div> <!-- end type MKFeatureDisplayPriority -->
<div> <!-- start type MKFeatureVisibility -->
<h3>New Type MapKit.MKFeatureVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKFeatureVisibility {
	<span class='added added-field ' data-is-non-breaking="">Adaptive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type MKFeatureVisibility -->
<div> <!-- start type MKMapViewDefault -->
<h3>New Type MapKit.MKMapViewDefault</h3>
<pre class='added' data-is-non-breaking="">
public static class MKMapViewDefault {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationViewReuseIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClusterAnnotationViewReuseIdentifier { get; }</span>
}
</pre>
</div> <!-- end type MKMapViewDefault -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaLibrary --> <div> 
<h2>Namespace MediaLibrary</h2>
<!-- start type MediaLibraryTypeIdentifierKey --> <div>
<h3>Type Changed: MediaLibrary.MediaLibraryTypeIdentifierKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosAnimatedGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLivePhotosGroupTypeIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhotosLongExposureGroupTypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MediaLibraryTypeIdentifierKey -->

</div> <!-- end namespace MediaLibrary -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPContentItem --> <div>
<h3>Type Changed: MediaPlayer.MPContentItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExplicitContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StreamingContent { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPContentItem -->
<!-- start type MPFeedbackCommand --> <div>
<h3>Type Changed: MediaPlayer.MPFeedbackCommand</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedShortTitle { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPFeedbackCommand -->
<!-- start type MPMediaItem --> <div>
<h3>Type Changed: MediaPlayer.MPMediaItem</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>Foundation.NSObject</span>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (IntPtr handle);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">ObjCRuntime.INativeObject</span>
	<span class='added added-interface ' data-is-non-breaking="">System.IDisposable</span>
	<span class='added added-interface ' data-is-non-breaking="">System.IEquatable&lt;Foundation.NSObject&gt;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPersistentID { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool CanFilterByProperty (Foundation.NSString property);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetObject (Foundation.NSObject key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);</span>
</pre>
</div>

</div> <!-- end type MPMediaItem -->
<!-- start type MPNowPlayingInfo --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate CurrentPlaybackDate { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfo -->
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<!-- start type MPRemoteCommandHandlerStatus --> <div>
<h3>Type Changed: MediaPlayer.MPRemoteCommandHandlerStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DeviceNotFound = 120,</span>
</pre>
</div>

</div> <!-- end type MPRemoteCommandHandlerStatus -->
<div> <!-- start type MPMediaItemEnumerator -->
<h3>New Type MediaPlayer.MPMediaItemEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MPMediaItemEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string property, Foundation.NSObject value, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string property, Foundation.NSObject value, bool stop);</span>
}
</pre>
</div> <!-- end type MPMediaItemEnumerator -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLArgument --> <div>
<h3>Type Changed: Metal.MTLArgument</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArrayLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPointerType BufferPointerType { get; }</span>
</pre>
</div>

</div> <!-- end type MTLArgument -->
<!-- start type MTLArgumentType --> <div>
<h3>Type Changed: Metal.MTLArgumentType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Imageblock = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageblockData = 16,</span>
</pre>
</div>

</div> <!-- end type MTLArgumentType -->
<!-- start type MTLArrayType --> <div>
<h3>Type Changed: Metal.MTLArrayType</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>Metal.MTLType</span>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArgumentIndexStride { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPointerType ElementPointerType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTextureReferenceType ElementTextureReferenceType { get; }</span>
</pre>
</div>

</div> <!-- end type MTLArrayType -->
<!-- start type MTLAttributeFormat --> <div>
<h3>Type Changed: Metal.MTLAttributeFormat</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Char = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">CharNormalized = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">Half = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">Short = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortNormalized = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar4Normalized_Bgra = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">UCharNormalized = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">UShortNormalized = 51,</span>
</pre>
</div>

</div> <!-- end type MTLAttributeFormat -->
<!-- start type MTLBlitCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLBlitCommandEncoder_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Update (IMTLBlitCommandEncoder This, IMTLFence fence);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Wait (IMTLBlitCommandEncoder This, IMTLFence fence);</span>
</pre>
</div>

</div> <!-- end type MTLBlitCommandEncoder_Extensions -->
<!-- start type MTLBuffer_Extensions --> <div>
<h3>Type Changed: Metal.MTLBuffer_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLTexture CreateTexture (IMTLBuffer This, MTLTextureDescriptor descriptor, uint offset, uint bytesPerRow);</span>
</pre>
</div>

</div> <!-- end type MTLBuffer_Extensions -->
<!-- start type MTLCommandBufferError --> <div>
<h3>Type Changed: Metal.MTLCommandBufferError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DeviceRemoved = 11,</span>
</pre>
</div>

</div> <!-- end type MTLCommandBufferError -->
<!-- start type MTLCommandBuffer_Extensions --> <div>
<h3>Type Changed: Metal.MTLCommandBuffer_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void PopDebugGroup (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PushDebugGroup (IMTLCommandBuffer This, string string);</span>
</pre>
</div>

</div> <!-- end type MTLCommandBuffer_Extensions -->
<!-- start type MTLComputeCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLComputeCommandEncoder_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DispatchThreads (IMTLComputeCommandEncoder This, MTLSize threadsPerGrid, MTLSize threadsPerThreadgroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Update (IMTLComputeCommandEncoder This, IMTLFence fence);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeap (IMTLComputeCommandEncoder This, IMTLHeap heap);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeaps (IMTLComputeCommandEncoder This, IMTLHeap[] heaps, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResource (IMTLComputeCommandEncoder This, IMTLResource resource, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResources (IMTLComputeCommandEncoder This, IMTLResource[] resources, uint count, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Wait (IMTLComputeCommandEncoder This, IMTLFence fence);</span>
</pre>
</div>

</div> <!-- end type MTLComputeCommandEncoder_Extensions -->
<!-- start type MTLComputePipelineDescriptor --> <div>
<h3>Type Changed: Metal.MTLComputePipelineDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPipelineBufferDescriptorArray Buffers { get; }</span>
</pre>
</div>

</div> <!-- end type MTLComputePipelineDescriptor -->
<!-- start type MTLDataType --> <div>
<h3>Type Changed: Metal.MTLDataType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Pointer = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">R16Snorm = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">R16Unorm = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">R8Snorm = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">R8Unorm = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">Rg11B10Float = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">Rg16Snorm = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">Rg16Unorm = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">Rg8Snorm = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">Rg8Unorm = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgb10A2Unorm = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgb9E5Float = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba16Snorm = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba16Unorm = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8Snorm = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8Unorm = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8Unorm_sRgb = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">Sampler = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">Texture = 58,</span>
</pre>
</div>

</div> <!-- end type MTLDataType -->
<!-- start type MTLDevice --> <div>
<h3>Type Changed: Metal.MTLDevice</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLDevice[] GetAllDevices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLDevice[] GetAllDevices (Foundation.NSObject observer, MTLDeviceNotificationHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveObserver (Foundation.NSObject observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void TrampolineNotificationHandler (IntPtr block, IntPtr device, IntPtr notifyName);</span>
</pre>
</div>

</div> <!-- end type MTLDevice -->
<!-- start type MTLDevice_Extensions --> <div>
<h3>Type Changed: Metal.MTLDevice_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLArgumentEncoder CreateArgumentEncoder (IMTLDevice This, MTLArgumentDescriptor[] arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLFence CreateFence (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLHeap CreateHeap (IMTLDevice This, MTLHeapDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLLibrary CreateLibrary (IMTLDevice This, Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLTexture CreateTexture (IMTLDevice This, MTLTextureDescriptor descriptor, IOSurface.IOSurface iosurface, uint plane);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLArgumentBuffersTier GetArgumentBuffersSupport (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetCurrentAllocatedSize (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetDefaultSamplePositions (IMTLDevice This, MTLSamplePosition[] positions, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetDefaultSamplePositions (IMTLDevice This, IntPtr positions, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLSizeAndAlign GetHeapBufferSizeAndAlignWithLength (IMTLDevice This, uint length, MTLResourceOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLSizeAndAlign GetHeapTextureSizeAndAlign (IMTLDevice This, MTLTextureDescriptor desc);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetMaxThreadgroupMemoryLength (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetMinimumLinearTextureAlignment (IMTLDevice This, MTLPixelFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetProgrammableSamplePositionsSupported (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetRasterOrderGroupsSupported (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLReadWriteTextureTier GetReadWriteTextureSupport (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetRegistryId (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetRemovable (IMTLDevice This);</span>
</pre>
</div>

</div> <!-- end type MTLDevice_Extensions -->
<!-- start type MTLFeatureSet --> <div>
<h3>Type Changed: Metal.MTLFeatureSet</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily1_v4 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily2_v4 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily3_v3 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily4_v1 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">macOS_GPUFamily1_v1 = 10000,</span>
	<span class='added added-field ' data-is-non-breaking="">macOS_GPUFamily1_v2 = 10001,</span>
	<span class='added added-field ' data-is-non-breaking="">macOS_GPUFamily1_v3 = 10003,</span>
	<span class='added added-field ' data-is-non-breaking="">macOS_ReadWriteTextureTier2 = 10002,</span>
	<span class='added added-field ' data-is-non-breaking="">tvOS_GPUFamily2_v1 = 30003,</span>
</pre>
</div>

</div> <!-- end type MTLFeatureSet -->
<!-- start type MTLFunction_Extensions --> <div>
<h3>Type Changed: Metal.MTLFunction_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLArgumentEncoder CreateArgumentEncoder (IMTLFunction This, uint bufferIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLArgumentEncoder CreateArgumentEncoder (IMTLFunction This, uint bufferIndex, MTLArgument reflection);</span>
</pre>
</div>

</div> <!-- end type MTLFunction_Extensions -->
<!-- start type MTLLanguageVersion --> <div>
<h3>Type Changed: Metal.MTLLanguageVersion</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">v2_0 = 131072,</span>
</pre>
</div>

</div> <!-- end type MTLLanguageVersion -->
<!-- start type MTLParallelRenderCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLParallelRenderCommandEncoder_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetColorStoreActionOptions (IMTLParallelRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions, uint colorAttachmentIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDepthStoreActionOptions (IMTLParallelRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStencilStoreActionOptions (IMTLParallelRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
</pre>
</div>

</div> <!-- end type MTLParallelRenderCommandEncoder_Extensions -->
<!-- start type MTLPixelFormat --> <div>
<h3>Type Changed: Metal.MTLPixelFormat</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BGR10A2Unorm = 94,</span>
</pre>
</div>

</div> <!-- end type MTLPixelFormat -->
<!-- start type MTLRenderCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLRenderCommandEncoder_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetColorStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions, uint colorAttachmentIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDepthStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetScissorRects (IMTLRenderCommandEncoder This, IntPtr scissorRects, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStencilStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetViewports (IMTLRenderCommandEncoder This, IntPtr viewports, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Update (IMTLRenderCommandEncoder This, IMTLFence fence, MTLRenderStages stages);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeap (IMTLRenderCommandEncoder This, IMTLHeap heap);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeaps (IMTLRenderCommandEncoder This, IMTLHeap[] heaps, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResource (IMTLRenderCommandEncoder This, IMTLResource resource, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResources (IMTLRenderCommandEncoder This, IMTLResource[] resources, uint count, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Wait (IMTLRenderCommandEncoder This, IMTLFence fence, MTLRenderStages stages);</span>
</pre>
</div>

</div> <!-- end type MTLRenderCommandEncoder_Extensions -->
<!-- start type MTLRenderPassAttachmentDescriptor --> <div>
<h3>Type Changed: Metal.MTLRenderPassAttachmentDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStoreActionOptions StoreActionOptions { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLRenderPassAttachmentDescriptor -->
<!-- start type MTLRenderPassDescriptor --> <div>
<h3>Type Changed: Metal.MTLRenderPassDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public uint GetSamplePositions (MTLSamplePosition[] positions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetSamplePositions (IntPtr positions, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetSamplePositions (MTLSamplePosition[] positions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSamplePositions (IntPtr positions, uint count);</span>
</pre>
</div>

</div> <!-- end type MTLRenderPassDescriptor -->
<!-- start type MTLRenderPipelineDescriptor --> <div>
<h3>Type Changed: Metal.MTLRenderPipelineDescriptor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPipelineBufferDescriptorArray FragmentBuffers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RasterSampleCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPipelineBufferDescriptorArray VertexBuffers { get; }</span>
</pre>
</div>

</div> <!-- end type MTLRenderPipelineDescriptor -->
<!-- start type MTLResource_Extensions --> <div>
<h3>Type Changed: Metal.MTLResource_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetAllocatedSize (IMTLResource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLHeap GetHeap (IMTLResource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetIsAliasable (IMTLResource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MakeAliasable (IMTLResource This);</span>
</pre>
</div>

</div> <!-- end type MTLResource_Extensions -->
<!-- start type MTLSamplerDescriptor --> <div>
<h3>Type Changed: Metal.MTLSamplerDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportArgumentBuffers { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLSamplerDescriptor -->
<!-- start type MTLStoreAction --> <div>
<h3>Type Changed: Metal.MTLStoreAction</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CustomSampleDepthStore = 5,</span>
</pre>
</div>

</div> <!-- end type MTLStoreAction -->
<!-- start type MTLStructMember --> <div>
<h3>Type Changed: Metal.MTLStructMember</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArgumentIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPointerType PointerType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTextureReferenceType TextureReferenceType { get; }</span>
</pre>
</div>

</div> <!-- end type MTLStructMember -->
<!-- start type MTLStructType --> <div>
<h3>Type Changed: Metal.MTLStructType</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>Metal.MTLType</span>

</div> <!-- end type MTLStructType -->
<!-- start type MTLTexture_Extensions --> <div>
<h3>Type Changed: Metal.MTLTexture_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IOSurface.IOSurface GetIOSurface (IMTLTexture This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetIOSurfacePlane (IMTLTexture This);</span>
</pre>
</div>

</div> <!-- end type MTLTexture_Extensions -->
<!-- start type MTLVertexFormat --> <div>
<h3>Type Changed: Metal.MTLVertexFormat</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Char = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">CharNormalized = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">Half = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">Short = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">ShortNormalized = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar4NormalizedBgra = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">UCharNormalized = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">UShortNormalized = 51,</span>
</pre>
</div>

</div> <!-- end type MTLVertexFormat -->
<div> <!-- start type IMTLArgumentEncoder -->
<h3>New Type Metal.IMTLArgumentEncoder</h3>
<pre class='added' data-is-non-breaking="">
public interface IMTLArgumentEncoder : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Alignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EncodedLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IMTLArgumentEncoder CreateArgumentEncoder (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetConstantData (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetArgumentBuffer (IMTLBuffer argumentBuffer, uint offset);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetArgumentBuffer (IMTLBuffer argumentBuffer, uint startOffset, uint arrayElement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBuffer (IMTLBuffer buffer, uint offset, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBuffers (IMTLBuffer[] buffers, IntPtr offsets, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSamplerState (IMTLSamplerState sampler, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSamplerStates (IMTLSamplerState[] samplers, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTexture (IMTLTexture texture, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTextures (IMTLTexture[] textures, Foundation.NSRange range);</span>
}
</pre>
</div> <!-- end type IMTLArgumentEncoder -->
<div> <!-- start type IMTLCaptureScope -->
<h3>New Type Metal.IMTLCaptureScope</h3>
<pre class='added' data-is-non-breaking="">
public interface IMTLCaptureScope : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLCommandQueue CommandQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginScope ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndScope ();</span>
}
</pre>
</div> <!-- end type IMTLCaptureScope -->
<div> <!-- start type IMTLFence -->
<h3>New Type Metal.IMTLFence</h3>
<pre class='added' data-is-non-breaking="">
public interface IMTLFence : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
}
</pre>
</div> <!-- end type IMTLFence -->
<div> <!-- start type IMTLHeap -->
<h3>New Type Metal.IMTLHeap</h3>
<pre class='added' data-is-non-breaking="">
public interface IMTLHeap : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLCpuCacheMode CpuCacheMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Size { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStorageMode StorageMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint UsedSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IMTLBuffer CreateBuffer (uint length, MTLResourceOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMTLTexture CreateTexture (MTLTextureDescriptor desc);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetMaxAvailableSize (uint alignment);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);</span>
}
</pre>
</div> <!-- end type IMTLHeap -->
<div> <!-- start type IMTLRenderCommandEncoder_Extensions -->
<h3>New Type Metal.IMTLRenderCommandEncoder_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class IMTLRenderCommandEncoder_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void SetScissorRects (IMTLRenderCommandEncoder This, MTLScissorRect[] scissorRects);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetViewports (IMTLRenderCommandEncoder This, MTLViewport[] viewports);</span>
}
</pre>
</div> <!-- end type IMTLRenderCommandEncoder_Extensions -->
<div> <!-- start type MTLArgumentBuffersTier -->
<h3>New Type Metal.MTLArgumentBuffersTier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLArgumentBuffersTier {
	<span class='added added-field ' data-is-non-breaking="">One = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Two = 1,</span>
}
</pre>
</div> <!-- end type MTLArgumentBuffersTier -->
<div> <!-- start type MTLArgumentDescriptor -->
<h3>New Type Metal.MTLArgumentDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLArgumentDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLArgumentDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLArgumentDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLArgumentDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLArgumentAccess Access { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArrayLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ConstantBlockAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Index { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTextureType TextureType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLArgumentDescriptor Create ();</span>
}
</pre>
</div> <!-- end type MTLArgumentDescriptor -->
<div> <!-- start type MTLArgumentEncoder_Extensions -->
<h3>New Type Metal.MTLArgumentEncoder_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLArgumentEncoder_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void SetBuffers (IMTLArgumentEncoder This, IMTLBuffer[] buffers, nint[] offsets, Foundation.NSRange range);</span>
}
</pre>
</div> <!-- end type MTLArgumentEncoder_Extensions -->
<div> <!-- start type MTLCaptureManager -->
<h3>New Type Metal.MTLCaptureManager</h3>
<pre class='added' data-is-non-breaking="">
public class MTLCaptureManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLCaptureManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLCaptureManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLCaptureScope DefaultCaptureScope { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCapturing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MTLCaptureManager Shared { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IMTLCaptureScope CreateNewCaptureScope (IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMTLCaptureScope CreateNewCaptureScope (IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCapture (IMTLCaptureScope captureScope);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCapture (IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCapture (IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopCapture ();</span>
}
</pre>
</div> <!-- end type MTLCaptureManager -->
<div> <!-- start type MTLCaptureScope -->
<h3>New Type Metal.MTLCaptureScope</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MTLCaptureScope : Foundation.NSObject, Foundation.INSObjectProtocol, IMTLCaptureScope, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLCaptureScope ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLCaptureScope (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLCaptureScope (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLCommandQueue CommandQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginScope ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndScope ();</span>
}
</pre>
</div> <!-- end type MTLCaptureScope -->
<div> <!-- start type MTLComputePipelineState_Extensions -->
<h3>New Type Metal.MTLComputePipelineState_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLComputePipelineState_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetLabel (IMTLComputePipelineState This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetStaticThreadgroupMemoryLength (IMTLComputePipelineState This);</span>
}
</pre>
</div> <!-- end type MTLComputePipelineState_Extensions -->
<div> <!-- start type MTLDeviceNotificationHandler -->
<h3>New Type Metal.MTLDeviceNotificationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MTLDeviceNotificationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLDeviceNotificationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IMTLDevice device, Foundation.NSString notifyName, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (IMTLDevice device, Foundation.NSString notifyName);</span>
}
</pre>
</div> <!-- end type MTLDeviceNotificationHandler -->
<div> <!-- start type MTLHeapDescriptor -->
<h3>New Type Metal.MTLHeapDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLHeapDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLHeapDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLHeapDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLHeapDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLCpuCacheMode CpuCacheMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Size { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStorageMode StorageMode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MTLHeapDescriptor -->
<div> <!-- start type MTLHeap_Extensions -->
<h3>New Type Metal.MTLHeap_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLHeap_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static uint GetCurrentAllocatedSize (IMTLHeap This);</span>
}
</pre>
</div> <!-- end type MTLHeap_Extensions -->
<div> <!-- start type MTLMutability -->
<h3>New Type Metal.MTLMutability</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLMutability {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Immutable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Mutable = 1,</span>
}
</pre>
</div> <!-- end type MTLMutability -->
<div> <!-- start type MTLPipelineBufferDescriptor -->
<h3>New Type Metal.MTLPipelineBufferDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLPipelineBufferDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLPipelineBufferDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPipelineBufferDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPipelineBufferDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLMutability Mutability { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MTLPipelineBufferDescriptor -->
<div> <!-- start type MTLPipelineBufferDescriptorArray -->
<h3>New Type Metal.MTLPipelineBufferDescriptorArray</h3>
<pre class='added' data-is-non-breaking="">
public class MTLPipelineBufferDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLPipelineBufferDescriptorArray ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPipelineBufferDescriptorArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPipelineBufferDescriptorArray (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MTLPipelineBufferDescriptor Item { get; set; }</span>
}
</pre>
</div> <!-- end type MTLPipelineBufferDescriptorArray -->
<div> <!-- start type MTLPointerType -->
<h3>New Type Metal.MTLPointerType</h3>
<pre class='added' data-is-non-breaking="">
public class MTLPointerType : Metal.MTLType, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLPointerType ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPointerType (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLPointerType (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLArgumentAccess Access { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Alignment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DataSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLArrayType ElementArrayType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ElementIsArgumentBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStructType ElementStructType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType ElementType { get; }</span>
}
</pre>
</div> <!-- end type MTLPointerType -->
<div> <!-- start type MTLReadWriteTextureTier -->
<h3>New Type Metal.MTLReadWriteTextureTier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLReadWriteTextureTier {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">One = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Two = 2,</span>
}
</pre>
</div> <!-- end type MTLReadWriteTextureTier -->
<div> <!-- start type MTLResourceUsage -->
<h3>New Type Metal.MTLResourceUsage</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MTLResourceUsage {
	<span class='added added-field ' data-is-non-breaking="">Read = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Sample = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Write = 2,</span>
}
</pre>
</div> <!-- end type MTLResourceUsage -->
<div> <!-- start type MTLSamplePosition -->
<h3>New Type Metal.MTLSamplePosition</h3>
<pre class='added' data-is-non-breaking="">
public struct MTLSamplePosition {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLSamplePosition (float x, float y);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
}
</pre>
</div> <!-- end type MTLSamplePosition -->
<div> <!-- start type MTLStoreActionOptions -->
<h3>New Type Metal.MTLStoreActionOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MTLStoreActionOptions {
	<span class='added added-field ' data-is-non-breaking="">CustomSamplePositions = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MTLStoreActionOptions -->
<div> <!-- start type MTLTextureReferenceType -->
<h3>New Type Metal.MTLTextureReferenceType</h3>
<pre class='added' data-is-non-breaking="">
public class MTLTextureReferenceType : Metal.MTLType, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLTextureReferenceType ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLTextureReferenceType (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLTextureReferenceType (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLArgumentAccess Access { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsDepthTexture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType TextureDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTextureType TextureType { get; }</span>
}
</pre>
</div> <!-- end type MTLTextureReferenceType -->
<div> <!-- start type MTLType -->
<h3>New Type Metal.MTLType</h3>
<pre class='added' data-is-non-breaking="">
public class MTLType : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLType ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLType (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLType (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType DataType { get; }</span>
}
</pre>
</div> <!-- end type MTLType -->

</div> <!-- end namespace Metal -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLObjectContainerComponent Animations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLAssetResolver Resolver { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NVector3 UpAxis { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLObject GetObject (string atPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadTextures ();</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->
<!-- start type MDLCamera --> <div>
<h3>Type Changed: ModelIO.MDLCamera</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'ProjectionMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 ProjectionMatrix { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 ProjectionMatrix4x4 { get; }</span>
</pre>
</div>

</div> <!-- end type MDLCamera -->
<!-- start type MDLMaterial --> <div>
<h3>Type Changed: ModelIO.MDLMaterial</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadTextures (IMDLAssetResolver resolver);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResolveTextures (IMDLAssetResolver resolver);</span>
</pre>
</div>

</div> <!-- end type MDLMaterial -->
<!-- start type MDLMaterialProperty --> <div>
<h3>Type Changed: ModelIO.MDLMaterialProperty</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MDLMaterialSemantic, MatrixFloat4x4)' overload instead.")]
	public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.Matrix4 value);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMaterialProperty (string name, MDLMaterialSemantic semantic, OpenTK.NMatrix4 value);</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat4x4' instead.")]
	public virtual OpenTK.Matrix4 Matrix4x4 { get; set; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 MatrixFloat4x4 { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetType (MDLMaterialPropertyType type);</span>
</pre>
</div>

</div> <!-- end type MDLMaterialProperty -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddOrthTanBasis (string textureCoordinateAttributeName, string normalAttributeName, string tangentAttributeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FlipTextureCoordinates (string inTextureCoordinateAttributeNamed);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool MakeVerticesUnique (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLPhotometricLight --> <div>
<h3>Type Changed: ModelIO.MDLPhotometricLight</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTexture GenerateTexture (uint textureSize);</span>
</pre>
</div>

</div> <!-- end type MDLPhotometricLight -->
<!-- start type MDLSkyCubeTexture --> <div>
<h3>Type Changed: ModelIO.MDLSkyCubeTexture</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLSkyCubeTexture (string name, MDLTextureChannelEncoding channelEncoding, OpenTK.Vector2i textureDimensions, float turbidity, float sunElevation, float sunAzimuth, float upperAtmosphereScattering, float groundAlbedo);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual float SunAzimuth { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLSkyCubeTexture -->
<!-- start type MDLStereoscopicCamera --> <div>
<h3>Type Changed: ModelIO.MDLStereoscopicCamera</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'LeftProjectionMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 LeftProjectionMatrix { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'LeftViewMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 LeftViewMatrix { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'RightProjectionMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 RightProjectionMatrix { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'RightViewMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 RightViewMatrix { get; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 LeftProjectionMatrix4x4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 LeftViewMatrix4x4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 RightProjectionMatrix4x4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.NMatrix4 RightViewMatrix4x4 { get; }</span>
</pre>
</div>

</div> <!-- end type MDLStereoscopicCamera -->
<!-- start type MDLTexture --> <div>
<h3>Type Changed: ModelIO.MDLTexture</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGImage GetImageFromTexture (uint level);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WriteToUrl (Foundation.NSUrl url, uint level);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WriteToUrl (Foundation.NSUrl nsurl, string type, uint level);</span>
</pre>
</div>

</div> <!-- end type MDLTexture -->
<!-- start type MDLTextureChannelEncoding --> <div>
<h3>Type Changed: ModelIO.MDLTextureChannelEncoding</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Float16SR = 770,</span>
</pre>
</div>

</div> <!-- end type MDLTextureChannelEncoding -->
<!-- start type MDLTransform --> <div>
<h3>Type Changed: ModelIO.MDLTransform</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(MatrixFloat4x4)' overload instead.")]
	public MDLTransform (OpenTK.Matrix4 matrix);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(MatrixFloat4x4, bool)' overload instead.")]
	public MDLTransform (OpenTK.Matrix4 matrix, bool resetsTransform);</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransform (OpenTK.NMatrix4 matrix);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransform (OpenTK.NMatrix4 matrix, bool resetsTransform);</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'CreateGlobalTransform4x4' instead.")]
	public static OpenTK.Matrix4 CreateGlobalTransform (MDLObject obj, double atTime);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetRotationMatrix4x4' instead.")]
	public virtual OpenTK.Matrix4 GetRotationMatrix (double atTime);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'SetMatrix4x4' instead.")]
	public virtual void SetMatrix (OpenTK.Matrix4 matrix, double time);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.NMatrix4 CreateGlobalTransform4x4 (MDLObject obj, double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.NMatrix4 GetRotationMatrix4x4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetMatrix4x4 (OpenTK.NMatrix4 matrix, double time);</span>
</pre>
</div>

</div> <!-- end type MDLTransform -->
<!-- start type MDLTransformComponent_Extensions --> <div>
<h3>Type Changed: ModelIO.MDLTransformComponent_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.NMatrix4 GetLocalTransform4x4 (IMDLTransformComponent This, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.NMatrix4 GetMatrix4x4 (IMDLTransformComponent self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetLocalTransform4x4 (IMDLTransformComponent This, OpenTK.NMatrix4 transform);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetLocalTransform4x4 (IMDLTransformComponent This, OpenTK.NMatrix4 transform, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetMatrix4x4 (IMDLTransformComponent self, OpenTK.NMatrix4 value);</span>
</pre>
</div>

</div> <!-- end type MDLTransformComponent_Extensions -->
<!-- start type MDLVoxelArray --> <div>
<h3>Type Changed: ModelIO.MDLVoxelArray</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'VoxelIndexExtent2' instead.")]
	public virtual MDLVoxelIndexExtent VoxelIndexExtent { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MDLVoxelIndexExtent2 VoxelIndexExtent2 { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'GetVoxels (MDLVoxelIndexExtent2)' instead.")]
	public virtual Foundation.NSData GetVoxels (MDLVoxelIndexExtent withinExtent);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetVoxels (MDLVoxelIndexExtent2 withinExtent);</span>
</pre>
</div>

</div> <!-- end type MDLVoxelArray -->
<div> <!-- start type IMDLAssetResolver -->
<h3>New Type ModelIO.IMDLAssetResolver</h3>
<pre class='added' data-is-non-breaking="">
public interface IMDLAssetResolver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanResolveAsset (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl ResolveAsset (string name);</span>
}
</pre>
</div> <!-- end type IMDLAssetResolver -->
<div> <!-- start type IMDLJointAnimation -->
<h3>New Type ModelIO.IMDLJointAnimation</h3>
<pre class='added' data-is-non-breaking="">
public interface IMDLJointAnimation : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IMDLJointAnimation -->
<div> <!-- start type IMDLTransformOp -->
<h3>New Type ModelIO.IMDLTransformOp</h3>
<pre class='added' data-is-non-breaking="">
public interface IMDLTransformOp : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type IMDLTransformOp -->
<div> <!-- start type MDLAnimatedMatrix4x4 -->
<h3>New Type ModelIO.MDLAnimatedMatrix4x4</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedMatrix4x4 : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedMatrix4x4 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedMatrix4x4 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedMatrix4x4 (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4Value (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4[] GetNMatrix4Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4dValue (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d[] GetNMatrix4dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NMatrix4[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NMatrix4d[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.NMatrix4 value, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.NMatrix4d value, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedMatrix4x4 -->
<div> <!-- start type MDLAnimatedQuaternionArray -->
<h3>New Type ModelIO.MDLAnimatedQuaternionArray</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedQuaternionArray : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedQuaternionArray ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedQuaternionArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedQuaternionArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedQuaternionArray (uint arrayElementCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ElementCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Quaternion[] GetQuaternionValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Quaternion[] GetQuaternionValues (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Quaterniond[] GetQuaterniondValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Quaterniond[] GetQuaterniondValues (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Quaternion[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Quaterniond[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.Quaternion[] array, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.Quaterniond[] array, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedQuaternionArray -->
<div> <!-- start type MDLAnimatedScalar -->
<h3>New Type ModelIO.MDLAnimatedScalar</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedScalar : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedScalar ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedScalar (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedScalar (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual double GetDouble (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual double[] GetDoubleValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetFloat (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetFloatValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (double[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (float[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (double value, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (float value, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedScalar -->
<div> <!-- start type MDLAnimatedScalarArray -->
<h3>New Type ModelIO.MDLAnimatedScalarArray</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedScalarArray : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedScalarArray ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedScalarArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedScalarArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedScalarArray (uint arrayElementCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ElementCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual double[] GetDoubleValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual double[] GetDoubleValues (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetFloatValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float[] GetFloatValues (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (double[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (float[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (double[] array, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (float[] array, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedScalarArray -->
<div> <!-- start type MDLAnimatedValue -->
<h3>New Type ModelIO.MDLAnimatedValue</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedValueInterpolation Interpolation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAnimated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double[] KeyTimes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double MaximumTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double MinimumTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLDataPrecision Precision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint TimeSampleCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber[] WeakKeyTimes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual double[] GetTimes ();</span>
}
</pre>
</div> <!-- end type MDLAnimatedValue -->
<div> <!-- start type MDLAnimatedValueInterpolation -->
<h3>New Type ModelIO.MDLAnimatedValueInterpolation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLAnimatedValueInterpolation {
	<span class='added added-field ' data-is-non-breaking="">Constant = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 1,</span>
}
</pre>
</div> <!-- end type MDLAnimatedValueInterpolation -->
<div> <!-- start type MDLAnimatedVector2 -->
<h3>New Type ModelIO.MDLAnimatedVector2</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedVector2 : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedVector2 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector2 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector2 (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetVector2Value (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2[] GetVector2Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2d GetVector2dValue (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2d[] GetVector2dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Vector2[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Vector2d[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.Vector2 value, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.Vector2d value, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedVector2 -->
<div> <!-- start type MDLAnimatedVector3 -->
<h3>New Type ModelIO.MDLAnimatedVector3</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedVector3 : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedVector3 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector3 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector3 (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3 GetNVector3Value (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3[] GetNVector3Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3d GetNVector3dValue (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3d[] GetNVector3dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NVector3[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NVector3d[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.NVector3 value, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.NVector3d value, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedVector3 -->
<div> <!-- start type MDLAnimatedVector3Array -->
<h3>New Type ModelIO.MDLAnimatedVector3Array</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedVector3Array : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedVector3Array ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector3Array (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector3Array (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedVector3Array (uint arrayElementCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ElementCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3[] GetNVector3Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3[] GetNVector3Values (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3d[] GetNVector3dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NVector3d[] GetNVector3dValues (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NVector3[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.NVector3d[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.NVector3[] array, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.NVector3d[] array, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedVector3Array -->
<div> <!-- start type MDLAnimatedVector4 -->
<h3>New Type ModelIO.MDLAnimatedVector4</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimatedVector4 : ModelIO.MDLAnimatedValue, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimatedVector4 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector4 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimatedVector4 (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector4 GetVector4Value (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector4[] GetVector4Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector4d GetVector4dValue (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector4d[] GetVector4dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Vector4[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset (OpenTK.Vector4d[] values, double[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.Vector4 value, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (OpenTK.Vector4d value, double time);</span>
}
</pre>
</div> <!-- end type MDLAnimatedVector4 -->
<div> <!-- start type MDLAnimationBindComponent -->
<h3>New Type ModelIO.MDLAnimationBindComponent</h3>
<pre class='added' data-is-non-breaking="">
public class MDLAnimationBindComponent : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, IMDLComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLAnimationBindComponent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimationBindComponent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLAnimationBindComponent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GeometryBindTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLJointAnimation JointAnimation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] JointPaths { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLSkeleton Skeleton { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MDLAnimationBindComponent -->
<div> <!-- start type MDLBundleAssetResolver -->
<h3>New Type ModelIO.MDLBundleAssetResolver</h3>
<pre class='added' data-is-non-breaking="">
public class MDLBundleAssetResolver : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLAssetResolver, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLBundleAssetResolver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLBundleAssetResolver (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLBundleAssetResolver (string path);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Path { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanResolveAsset (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl ResolveAsset (string name);</span>
}
</pre>
</div> <!-- end type MDLBundleAssetResolver -->
<div> <!-- start type MDLDataPrecision -->
<h3>New Type ModelIO.MDLDataPrecision</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLDataPrecision {
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Float = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type MDLDataPrecision -->
<div> <!-- start type MDLMatrix4x4Array -->
<h3>New Type ModelIO.MDLMatrix4x4Array</h3>
<pre class='added' data-is-non-breaking="">
public class MDLMatrix4x4Array : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMatrix4x4Array (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMatrix4x4Array (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMatrix4x4Array (uint arrayElementCount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ElementCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLDataPrecision Precision { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4[] GetNMatrix4Values ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d[] GetNMatrix4dValues ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.NMatrix4[] array);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValues (OpenTK.NMatrix4d[] array);</span>
}
</pre>
</div> <!-- end type MDLMatrix4x4Array -->
<div> <!-- start type MDLPackedJointAnimation -->
<h3>New Type ModelIO.MDLPackedJointAnimation</h3>
<pre class='added' data-is-non-breaking="">
public class MDLPackedJointAnimation : ModelIO.MDLObject, Foundation.INSCopying, Foundation.INSObjectProtocol, IMDLJointAnimation, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLPackedJointAnimation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLPackedJointAnimation (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLPackedJointAnimation (string name, string[] jointPaths);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] JointPaths { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedQuaternionArray Rotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedVector3Array Scales { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedVector3Array Translations { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MDLPackedJointAnimation -->
<div> <!-- start type MDLPathAssetResolver -->
<h3>New Type ModelIO.MDLPathAssetResolver</h3>
<pre class='added' data-is-non-breaking="">
public class MDLPathAssetResolver : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLAssetResolver, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLPathAssetResolver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLPathAssetResolver (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLPathAssetResolver (string path);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Path { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanResolveAsset (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl ResolveAsset (string name);</span>
}
</pre>
</div> <!-- end type MDLPathAssetResolver -->
<div> <!-- start type MDLRelativeAssetResolver -->
<h3>New Type ModelIO.MDLRelativeAssetResolver</h3>
<pre class='added' data-is-non-breaking="">
public class MDLRelativeAssetResolver : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLAssetResolver, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLRelativeAssetResolver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLRelativeAssetResolver (MDLAsset asset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLRelativeAssetResolver (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAsset Asset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanResolveAsset (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl ResolveAsset (string name);</span>
}
</pre>
</div> <!-- end type MDLRelativeAssetResolver -->
<div> <!-- start type MDLSkeleton -->
<h3>New Type ModelIO.MDLSkeleton</h3>
<pre class='added' data-is-non-breaking="">
public class MDLSkeleton : ModelIO.MDLObject, Foundation.INSCopying, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLSkeleton (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLSkeleton (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLSkeleton (string name, string[] jointPaths);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMatrix4x4Array JointBindTransforms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] JointPaths { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MDLSkeleton -->
<div> <!-- start type MDLTransformMatrixOp -->
<h3>New Type ModelIO.MDLTransformMatrixOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformMatrixOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformMatrixOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformMatrixOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformMatrixOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedMatrix4x4 AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformMatrixOp -->
<div> <!-- start type MDLTransformOpRotationOrder -->
<h3>New Type ModelIO.MDLTransformOpRotationOrder</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLTransformOpRotationOrder {
	<span class='added added-field ' data-is-non-breaking="">Xyz = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Xzy = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Yxz = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Yzx = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Zxy = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Zyx = 6,</span>
}
</pre>
</div> <!-- end type MDLTransformOpRotationOrder -->
<div> <!-- start type MDLTransformRotateOp -->
<h3>New Type ModelIO.MDLTransformRotateOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformRotateOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformRotateOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedVector3 AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformRotateOp -->
<div> <!-- start type MDLTransformRotateXOp -->
<h3>New Type ModelIO.MDLTransformRotateXOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformRotateXOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformRotateXOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateXOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateXOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedScalar AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformRotateXOp -->
<div> <!-- start type MDLTransformRotateYOp -->
<h3>New Type ModelIO.MDLTransformRotateYOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformRotateYOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformRotateYOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateYOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateYOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedScalar AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformRotateYOp -->
<div> <!-- start type MDLTransformRotateZOp -->
<h3>New Type ModelIO.MDLTransformRotateZOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformRotateZOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformRotateZOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateZOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformRotateZOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedScalar AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformRotateZOp -->
<div> <!-- start type MDLTransformScaleOp -->
<h3>New Type ModelIO.MDLTransformScaleOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformScaleOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformScaleOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformScaleOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformScaleOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedVector3 AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformScaleOp -->
<div> <!-- start type MDLTransformStack -->
<h3>New Type ModelIO.MDLTransformStack</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformStack : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, IMDLComponent, IMDLTransformComponent, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformStack ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformStack (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformStack (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] KeyTimes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix4 Matrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double MaximumTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double MinimumTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ResetsTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLTransformOp[] TransformOps { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformMatrixOp AddMatrixOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformRotateOp AddRotateOp (string animatedValueName, MDLTransformOpRotationOrder order, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformRotateXOp AddRotateXOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformRotateYOp AddRotateYOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformRotateZOp AddRotateZOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformScaleOp AddScaleOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLTransformTranslateOp AddTranslateOp (string animatedValueName, bool inverse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'CreateGlobalTransform4x4' instead.")]
	public static OpenTK.Matrix4 CreateGlobalTransform (MDLObject obj, double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLAnimatedValue GetAnimatedValue (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Matrix4 GetLocalTransform (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLocalTransform (OpenTK.Matrix4 transform);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLocalTransform (OpenTK.Matrix4 transform, double time);</span>
}
</pre>
</div> <!-- end type MDLTransformStack -->
<div> <!-- start type MDLTransformTranslateOp -->
<h3>New Type ModelIO.MDLTransformTranslateOp</h3>
<pre class='added' data-is-non-breaking="">
public class MDLTransformTranslateOp : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLTransformOp, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransformTranslateOp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformTranslateOp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLTransformTranslateOp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAnimatedVector3 AnimatedValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsInverseOp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 GetNMatrix4 (double atTime);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.NMatrix4d GetNMatrix4d (double atTime);</span>
}
</pre>
</div> <!-- end type MDLTransformTranslateOp -->
<div> <!-- start type MDLVoxelIndexExtent2 -->
<h3>New Type ModelIO.MDLVoxelIndexExtent2</h3>
<pre class='added' data-is-non-breaking="">
public struct MDLVoxelIndexExtent2 {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLVoxelIndexExtent2 (OpenTK.Vector4i minimumExtent, OpenTK.Vector4i maximumExtent);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector4i MaximumExtent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector4i MinimumExtent { get; }</span>
}
</pre>
</div> <!-- end type MDLVoxelIndexExtent2 -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NEVpnManager --> <div>
<h3>Type Changed: NetworkExtension.NEVpnManager</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetAuthorization (Security.Authorization authorization);</span>
</pre>
</div>

</div> <!-- end type NEVpnManager -->
<!-- start type NEVpnProtocolIke2 --> <div>
<h3>Type Changed: NetworkExtension.NEVpnProtocolIke2</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NEVpnIkev2TlsVersion MaximumTlsVersion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NEVpnIkev2TlsVersion MinimumTlsVersion { get; set; }</span>
</pre>
</div>

</div> <!-- end type NEVpnProtocolIke2 -->
<div> <!-- start type NEDnsProxyProviderProtocol -->
<h3>New Type NetworkExtension.NEDnsProxyProviderProtocol</h3>
<pre class='added' data-is-non-breaking="">
public class NEDnsProxyProviderProtocol : NetworkExtension.NEVpnProtocol, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NEDnsProxyProviderProtocol ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NEDnsProxyProviderProtocol (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NEDnsProxyProviderProtocol (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NEDnsProxyProviderProtocol (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProviderBundleIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary ProviderConfiguration { get; set; }</span>
}
</pre>
</div> <!-- end type NEDnsProxyProviderProtocol -->
<div> <!-- start type NEVpnIkev2TlsVersion -->
<h3>New Type NetworkExtension.NEVpnIkev2TlsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NEVpnIkev2TlsVersion {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1_0 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1_1 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1_2 = 3,</span>
}
</pre>
</div> <!-- end type NEVpnIkev2TlsVersion -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.12"</span> <span class='added '>"10.13"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.8.0"</span> <span class='added '>"4.0.0"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string IOSurfaceLibrary = "/System/Library/Frameworks/IOSurface.framework/IOSurface";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string PhotosUILibrary = "/System/Library/Frameworks/PhotosUI.framework/PhotosUI";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNFloat (IntPtr handle, string symbol, nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNInt (IntPtr handle, string symbol, nint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNUInt (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<div> <!-- start type BindAsAttribute -->
<h3>New Type ObjCRuntime.BindAsAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class BindAsAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public BindAsAttribute (System.Type type);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public System.Type OriginalType;</span>
	<span class='added added-field ' data-is-non-breaking="">public System.Type Type;</span>
}
</pre>
</div> <!-- end type BindAsAttribute -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace OpenTK --> <div> 
<h2>Namespace OpenTK</h2>
<div> <!-- start type NMatrix2 -->
<h3>New Type OpenTK.NMatrix2</h3>
<pre class='added' data-is-non-breaking="">
public struct NMatrix2, System.IEquatable&lt;NMatrix2&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix2 (float r0c0, float r0c1, float r1c0, float r1c1);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static NMatrix2 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R0C0;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R0C1;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R1C0;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R1C1;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NMatrix2 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix2 Multiply (NMatrix2 left, NMatrix2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (NMatrix2 left, NMatrix2 right, NMatrix2 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix2 Transpose (NMatrix2 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (NMatrix2 mat, NMatrix2 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NMatrix2 left, NMatrix2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix2 op_Explicit (Matrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix2 op_Explicit (NMatrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NMatrix2 left, NMatrix2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix2 op_Multiply (NMatrix2 left, NMatrix2 right);</span>
}
</pre>
</div> <!-- end type NMatrix2 -->
<div> <!-- start type NMatrix3 -->
<h3>New Type OpenTK.NMatrix3</h3>
<pre class='added' data-is-non-breaking="">
public struct NMatrix3, System.IEquatable&lt;NMatrix3&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix3 (float r0c0, float r0c1, float r0c2, float r1c0, float r1c1, float r1c2, float r2c0, float r2c1, float r2c2);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static NMatrix3 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R0C0;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R0C1;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R0C2;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R1C0;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R1C1;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R1C2;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R2C0;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R2C1;</span>
	<span class='added added-field ' data-is-non-breaking="">public float R2C2;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NMatrix3 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix3 Multiply (NMatrix3 left, NMatrix3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (NMatrix3 left, NMatrix3 right, NMatrix3 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix3 Transpose (NMatrix3 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (NMatrix3 mat, NMatrix3 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NMatrix3 left, NMatrix3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix3 op_Explicit (Matrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix3 op_Explicit (NMatrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NMatrix3 left, NMatrix3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix3 op_Multiply (NMatrix3 left, NMatrix3 right);</span>
}
</pre>
</div> <!-- end type NMatrix3 -->
<div> <!-- start type NMatrix4 -->
<h3>New Type OpenTK.NMatrix4</h3>
<pre class='added' data-is-non-breaking="">
public struct NMatrix4, System.IEquatable&lt;NMatrix4&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix4 (Vector4 row0, Vector4 row1, Vector4 row2, Vector4 row3);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix4 (float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static NMatrix4 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M14;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M24;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M33;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M34;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M41;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M42;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M43;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M44;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Column0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Column1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Column2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Column3 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row3 { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NMatrix4 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4 Multiply (NMatrix4 left, NMatrix4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (NMatrix4 left, NMatrix4 right, NMatrix4 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4 Transpose (NMatrix4 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (NMatrix4 mat, NMatrix4 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NMatrix4 left, NMatrix4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4 op_Explicit (Matrix4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4 op_Explicit (NMatrix4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NMatrix4 left, NMatrix4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4 op_Multiply (NMatrix4 left, NMatrix4 right);</span>
}
</pre>
</div> <!-- end type NMatrix4 -->
<div> <!-- start type NMatrix4d -->
<h3>New Type OpenTK.NMatrix4d</h3>
<pre class='added' data-is-non-breaking="">
public struct NMatrix4d, System.IEquatable&lt;NMatrix4d&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix4d (Vector4d row0, Vector4d row1, Vector4d row2, Vector4d row3);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix4d (double m11, double m12, double m13, double m14, double m21, double m22, double m23, double m24, double m31, double m32, double m33, double m34, double m41, double m42, double m43, double m44);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static NMatrix4d Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M14;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M24;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M33;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M34;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M41;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M42;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M43;</span>
	<span class='added added-field ' data-is-non-breaking="">public double M44;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Column0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Column1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Column2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Column3 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Determinant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Row0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Row1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Row2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4d Row3 { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NMatrix4d other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4d Multiply (NMatrix4d left, NMatrix4d right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (NMatrix4d left, NMatrix4d right, NMatrix4d result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4d Transpose (NMatrix4d mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (NMatrix4d mat, NMatrix4d result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NMatrix4d left, NMatrix4d right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4d op_Explicit (Matrix4d value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Matrix4d op_Explicit (NMatrix4d value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NMatrix4d left, NMatrix4d right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NMatrix4d op_Multiply (NMatrix4d left, NMatrix4d right);</span>
}
</pre>
</div> <!-- end type NMatrix4d -->
<div> <!-- start type NMatrix4x3 -->
<h3>New Type OpenTK.NMatrix4x3</h3>
<pre class='added' data-is-non-breaking="">
public struct NMatrix4x3, System.IEquatable&lt;NMatrix4x3&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NMatrix4x3 (float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M14;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M24;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M33;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M34;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NVector3 Column0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NVector3 Column1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NVector3 Column2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NVector3 Column3 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Vector4 Row2 { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NMatrix4x3 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NMatrix4x3 left, NMatrix4x3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NMatrix4x3 left, NMatrix4x3 right);</span>
}
</pre>
</div> <!-- end type NMatrix4x3 -->
<div> <!-- start type NVector3 -->
<h3>New Type OpenTK.NVector3</h3>
<pre class='added' data-is-non-breaking="">
public struct NVector3, System.IEquatable&lt;NVector3&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NVector3 (float x, float y, float z);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public float X;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Z;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NVector3 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NVector3 left, NVector3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3 op_Explicit (NVector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NVector3 op_Explicit (Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NVector3 left, NVector3 right);</span>
}
</pre>
</div> <!-- end type NVector3 -->
<div> <!-- start type NVector3d -->
<h3>New Type OpenTK.NVector3d</h3>
<pre class='added' data-is-non-breaking="">
public struct NVector3d, System.IEquatable&lt;NVector3d&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NVector3d (double x, double y, double z);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public double X;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Y;</span>
	<span class='added added-field ' data-is-non-breaking="">public double Z;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (NVector3d other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NVector3d left, NVector3d right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Vector3d op_Explicit (NVector3d value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NVector3d op_Explicit (Vector3d value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NVector3d left, NVector3d right);</span>
}
</pre>
</div> <!-- end type NVector3d -->

</div> <!-- end namespace OpenTK -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfAnnotation --> <div>
<h3>Type Changed: PdfKit.PdfAnnotation</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, Foundation.NSString annotationType, Foundation.NSDictionary properties);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAnnotation (CoreGraphics.CGRect bounds, PdfAnnotationKey annotationType, Foundation.NSDictionary properties);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual PdfPage Page { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual string Type { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfAction Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSTextAlignment Alignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsToggleToOff { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary AnnotationKeyValues { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PdfAnnotationKey AnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetCellState ButtonWidgetState { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ButtonWidgetStateString { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Choices { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Comb { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDestination Destination { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle EndLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint EndPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FieldName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSFont Font { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor FontColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Highlighted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfTextAnnotationIconType IconType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPasswordField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ListChoice { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfMarkupType MarkupType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaximumLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Multiline { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Open { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSBezierPath[] Paths { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGPoint[] QuadrilateralPoints { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RadiosInUnison { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfLineStyle StartLineStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint StartPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Values { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType WidgetControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetDefaultStringValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetFieldType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string WidgetStringValue { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddBezierPath (AppKit.NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfLineStyle GetLineStyle (string fromName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetName (PdfLineStyle style);</span>
	<span class='added added-method ' data-is-non-breaking="">public T GetValue&lt;T&gt; (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveBezierPath (AppKit.NSBezierPath path);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void RemoveValue (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveValue (PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (CoreGraphics.CGRect rect, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (CoreGraphics.CGRect rect, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetValue (bool boolean, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (bool boolean, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue (string str, PdfAnnotationKey key);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SetValue&lt;T&gt; (T value, PdfAnnotationKey key);</span>
</pre>
</div>

</div> <!-- end type PdfAnnotation -->
<!-- start type PdfAnnotationButtonWidget --> <div>
<h3>Type Changed: PdfKit.PdfAnnotationButtonWidget</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual bool AllowsToggleToOff { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type PdfAnnotationButtonWidget -->
<!-- start type PdfAnnotationTextWidget --> <div>
<h3>Type Changed: PdfKit.PdfAnnotationTextWidget</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedStringValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsMultiline { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfAnnotationTextWidget -->
<!-- start type PdfBorder --> <div>
<h3>Type Changed: PdfKit.PdfBorder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakBorderKeyValues { get; }</span>
</pre>
</div>

</div> <!-- end type PdfBorder -->
<!-- start type PdfDestination --> <div>
<h3>Type Changed: PdfKit.PdfDestination</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Zoom { get; set; }</span>
</pre>
</div>

</div> <!-- end type PdfDestination -->
<!-- start type PdfDocument --> <div>
<h3>Type Changed: PdfKit.PdfDocument</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCommenting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsContentAccessibility { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentAssembly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsDocumentChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsFormFieldEntry { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidBeginWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageFindNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndPageWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidEndWriteNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidFindMatchNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUnlockNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFDocument Document { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate GetClassForAnnotationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Type PageType { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidBeginDocumentFind;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUnlock;</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Find (string, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection[] Find (string text, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'Find (string, PdfSelection, NSStringCompareOptions)' instead.")]
	public virtual PdfSelection Find (string text, PdfSelection selection, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string, NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string text, nint options);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'FindAsync (string [], NSStringCompareOptions)' instead.")]
	public virtual void FindAsync (string[] text, nint options);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection[] Find (string text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PdfSelection Find (string text, PdfSelection selection, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FindAsync (string text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FindAsync (string[] text, Foundation.NSStringCompareOptions compareOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public PdfDocumentAttributes GetDocumentAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSPrintOperation GetPrintOperation (AppKit.NSPrintInfo printInfo, PdfPrintScalingMode scaleMode, bool doRotate);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetDocumentAttributes (PdfDocumentAttributes attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (Foundation.NSUrl url, PdfDocumentWriteOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Write (string path, PdfDocumentWriteOptions options);</span>
</pre>
</div>

</div> <!-- end type PdfDocument -->
<!-- start type PdfDocumentDelegate --> <div>
<h3>Type Changed: PdfKit.PdfDocumentDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBeginDocumentFind (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnlock (Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForAnnotationType (string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForPage ();</span>
</pre>
</div>

</div> <!-- end type PdfDocumentDelegate -->
<!-- start type PdfDocumentDelegate_Extensions --> <div>
<h3>Type Changed: PdfKit.PdfDocumentDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidBeginDocumentFind (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnlock (IPdfDocumentDelegate This, Foundation.NSNotification notification);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForAnnotationType (IPdfDocumentDelegate This, string annotationType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetClassForPage (IPdfDocumentDelegate This);</span>
</pre>
</div>

</div> <!-- end type PdfDocumentDelegate_Extensions -->
<!-- start type PdfPage --> <div>
<h3>Type Changed: PdfKit.PdfPage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPDFPage Page { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (PdfDisplayBox box, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSImage GetThumbnail (CoreGraphics.CGSize size, PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform GetTransform (PdfDisplayBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TransformContext (CoreGraphics.CGContext context, PdfDisplayBox box);</span>
</pre>
</div>

</div> <!-- end type PdfPage -->
<!-- start type PdfSelection --> <div>
<h3>Type Changed: PdfKit.PdfSelection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExtendSelectionForLineBoundaries ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetNumberOfTextRanges (PdfPage page);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetRange (uint index, PdfPage page);</span>
</pre>
</div>

</div> <!-- end type PdfSelection -->
<!-- start type PdfThumbnailView --> <div>
<h3>Type Changed: PdfKit.PdfThumbnailView</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfThumbnailView (CoreGraphics.CGRect frame);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DocumentEditedNotification { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type PdfThumbnailView -->
<!-- start type PdfView --> <div>
<h3>Type Changed: PdfKit.PdfView</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfView (CoreGraphics.CGRect frame);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSAnimationDelegate</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AcceptsDraggedFiles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfDisplayDirection DisplayDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplaysRtl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfInterpolationQuality InterpolationQuality { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaxScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSEdgeInsets PageBreakMargins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PrintPermissionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScaleFactorForSizeToFit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VisiblePagesChangedNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidEnd (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidReachProgressMark (AppKit.NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidStop (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AnimationShouldStart (AppKit.NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float ComputeAnimationCurve (AppKit.NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPage (PdfPage page, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawPagePost (PdfPage page, CoreGraphics.CGContext context);</span>
</pre>
</div>
<!-- start type PdfView.Notifications --> <div>
<h3>Type Changed: PdfKit.PdfView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePrintPermission (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVisiblePagesChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type PdfView.Notifications -->

</div> <!-- end type PdfView -->
<div> <!-- start type ClassForAnnotationTypeDelegate -->
<h3>New Type PdfKit.ClassForAnnotationTypeDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ClassForAnnotationTypeDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ClassForAnnotationTypeDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string annotationType, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class Invoke (string annotationType);</span>
}
</pre>
</div> <!-- end type ClassForAnnotationTypeDelegate -->
<div> <!-- start type PdfAnnotationHighlightingMode -->
<h3>New Type PdfKit.PdfAnnotationHighlightingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationHighlightingMode {
	<span class='added added-field ' data-is-non-breaking="">Invert = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Outline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Push = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingMode -->
<div> <!-- start type PdfAnnotationHighlightingModeExtensions -->
<h3>New Type PdfKit.PdfAnnotationHighlightingModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationHighlightingModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationHighlightingMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationHighlightingMode GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationHighlightingModeExtensions -->
<div> <!-- start type PdfAnnotationKey -->
<h3>New Type PdfKit.PdfAnnotationKey</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationKey {
	<span class='added added-field ' data-is-non-breaking="">Action = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">AdditionalActions = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceDictionary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AppearanceState = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Border = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BorderStyle = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Color = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Contents = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Date = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DefaultAppearance = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Destination = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Flags = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HighlightingMode = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">IconName = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">Inklist = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InteriorColor = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">LineEndingStyles = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">LinePoints = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Name = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Page = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Parent = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">QuadPoints = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Quadding = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Rect = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtype = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">TextLabel = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetAppearanceDictionary = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBackgroundColor = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetBorderColor = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetCaption = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDefaultValue = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetDownCaption = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldFlags = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetFieldType = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetMaxLen = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetOptions = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRolloverCaption = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetRotation = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetTextLabelUI = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">WidgetValue = 41,</span>
}
</pre>
</div> <!-- end type PdfAnnotationKey -->
<div> <!-- start type PdfAnnotationKeyExtensions -->
<h3>New Type PdfKit.PdfAnnotationKeyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationKeyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationKey self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationKey GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationKeyExtensions -->
<div> <!-- start type PdfAnnotationLineEndingStyle -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationLineEndingStyle {
	<span class='added added-field ' data-is-non-breaking="">Circle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedArrow = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Diamond = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OpenArrow = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 1,</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyle -->
<div> <!-- start type PdfAnnotationLineEndingStyleExtensions -->
<h3>New Type PdfKit.PdfAnnotationLineEndingStyleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationLineEndingStyleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationLineEndingStyle self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationLineEndingStyle GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationLineEndingStyleExtensions -->
<div> <!-- start type PdfAnnotationSubtype -->
<h3>New Type PdfKit.PdfAnnotationSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationSubtype {
	<span class='added added-field ' data-is-non-breaking="">Circle = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FreeText = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Highlight = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Ink = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Line = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Popup = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Square = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Stamp = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">StrikeOut = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Underline = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Widget = 12,</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtype -->
<div> <!-- start type PdfAnnotationSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationSubtypeExtensions -->
<div> <!-- start type PdfAnnotationTextIconType -->
<h3>New Type PdfKit.PdfAnnotationTextIconType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationTextIconType {
	<span class='added added-field ' data-is-non-breaking="">Comment = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Help = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Key = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NewParagraph = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Note = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 5,</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconType -->
<div> <!-- start type PdfAnnotationTextIconTypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationTextIconTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationTextIconTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationTextIconType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationTextIconType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationTextIconTypeExtensions -->
<div> <!-- start type PdfAnnotationWidgetSubtype -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfAnnotationWidgetSubtype {
	<span class='added added-field ' data-is-non-breaking="">Button = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Choice = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Signature = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 3,</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtype -->
<div> <!-- start type PdfAnnotationWidgetSubtypeExtensions -->
<h3>New Type PdfKit.PdfAnnotationWidgetSubtypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAnnotationWidgetSubtypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PdfAnnotationWidgetSubtype self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PdfAnnotationWidgetSubtype GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PdfAnnotationWidgetSubtypeExtensions -->
<div> <!-- start type PdfAppearanceCharacteristics -->
<h3>New Type PdfKit.PdfAppearanceCharacteristics</h3>
<pre class='added' data-is-non-breaking="">
public class PdfAppearanceCharacteristics : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfAppearanceCharacteristics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PdfAppearanceCharacteristics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor BorderColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Caption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PdfWidgetControlType ControlType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DownCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RolloverCaption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakAppearanceCharacteristicsKeyValues { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristics -->
<div> <!-- start type PdfAppearanceCharacteristicsKeys -->
<h3>New Type PdfKit.PdfAppearanceCharacteristicsKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfAppearanceCharacteristicsKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BackgroundColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BorderColorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RolloverCaptionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RotationKey { get; }</span>
}
</pre>
</div> <!-- end type PdfAppearanceCharacteristicsKeys -->
<div> <!-- start type PdfBorderKeys -->
<h3>New Type PdfKit.PdfBorderKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PdfBorderKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DashPatternKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LineWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StyleKey { get; }</span>
}
</pre>
</div> <!-- end type PdfBorderKeys -->
<div> <!-- start type PdfDisplayDirection -->
<h3>New Type PdfKit.PdfDisplayDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfDisplayDirection {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type PdfDisplayDirection -->
<div> <!-- start type PdfDocumentAttributes -->
<h3>New Type PdfKit.PdfDocumentAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentAttributes : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentAttributes (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate CreationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Creator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Keywords { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate ModificationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Producer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subject { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Title { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentAttributes -->
<div> <!-- start type PdfDocumentWriteOptions -->
<h3>New Type PdfKit.PdfDocumentWriteOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PdfDocumentWriteOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PdfDocumentWriteOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string OwnerPassword { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UserPassword { get; set; }</span>
}
</pre>
</div> <!-- end type PdfDocumentWriteOptions -->
<div> <!-- start type PdfInterpolationQuality -->
<h3>New Type PdfKit.PdfInterpolationQuality</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfInterpolationQuality {
	<span class='added added-field ' data-is-non-breaking="">High = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PdfInterpolationQuality -->
<div> <!-- start type PdfWidgetCellState -->
<h3>New Type PdfKit.PdfWidgetCellState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PdfWidgetCellState {
	<span class='added added-field ' data-is-non-breaking="">Mixed = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">On = 1,</span>
}
</pre>
</div> <!-- end type PdfWidgetCellState -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAnimated = 214,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLongExposures = 215,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage DisplaySizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHContentEditingInput -->
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, PHLivePhotoEditingOption options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, PHLivePhotoEditingOption options);</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type IPHPhotoLibraryChangeObserver -->
<h3>New Type Photos.IPHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHPhotoLibraryChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type IPHPhotoLibraryChangeObserver -->
<div> <!-- start type PHAsset -->
<h3>New Type Photos.PHAsset</h3>
<pre class='added' data-is-non-breaking="">
public class PHAsset : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BurstIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LocalIdentifierNotFound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RepresentsBurst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType SourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SyncFailureHidden { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHAsset -->
<div> <!-- start type PHAssetCollection -->
<h3>New Type Photos.PHAssetCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollection : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetCollection ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation ApproximateLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionType AssetCollectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EstimatedAssetCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);</span>
}
</pre>
</div> <!-- end type PHAssetCollection -->
<div> <!-- start type PHAssetImageProgressHandler -->
<h3>New Type Photos.PHAssetImageProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetImageProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetImageProgressHandler -->
<div> <!-- start type PHAssetPlaybackStyle -->
<h3>New Type Photos.PHAssetPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageAnimated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LivePhoto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoLooping = 5,</span>
}
</pre>
</div> <!-- end type PHAssetPlaybackStyle -->
<div> <!-- start type PHAuthorizationStatus -->
<h3>New Type Photos.PHAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type PHAuthorizationStatus -->
<div> <!-- start type PHChange -->
<h3>New Type Photos.PHChange</h3>
<pre class='added' data-is-non-breaking="">
public class PHChange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);</span>
}
</pre>
</div> <!-- end type PHChange -->
<div> <!-- start type PHChangeDetailEnumerator -->
<h3>New Type Photos.PHChangeDetailEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChangeDetailEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (uint fromIndex, uint toIndex);</span>
}
</pre>
</div> <!-- end type PHChangeDetailEnumerator -->
<div> <!-- start type PHCloudIdentifier -->
<h3>New Type Photos.PHCloudIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public class PHCloudIdentifier : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCloudIdentifier (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHCloudIdentifier (string stringValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHCloudIdentifier NotFoundIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHCloudIdentifier -->
<div> <!-- start type PHCollection -->
<h3>New Type Photos.PHCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollection : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainAssets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainCollections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollection -->
<div> <!-- start type PHCollectionList -->
<h3>New Type Photos.PHCollectionList</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionList : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCollectionList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListSubtype CollectionListSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListType CollectionListType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollectionList -->
<div> <!-- start type PHFetchOptions -->
<h3>New Type Photos.PHFetchOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FetchLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAllBurstAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType IncludeAssetSourceTypes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeHiddenAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsIncrementalChangeDetails { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHFetchOptions -->
<div> <!-- start type PHFetchResult -->
<h3>New Type Photos.PHFetchResult</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResult : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LastObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject firstObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSIndexSet idx, Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAt (nint index);</span>
}
</pre>
</div> <!-- end type PHFetchResult -->
<div> <!-- start type PHFetchResultChangeDetails -->
<h3>New Type Photos.PHFetchResultChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResultChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet ChangedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] ChangedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasIncrementalChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasMoves { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet InsertedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] InsertedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet RemovedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] RemovedObjects { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);</span>
}
</pre>
</div> <!-- end type PHFetchResultChangeDetails -->
<div> <!-- start type PHFetchResultEnumerator -->
<h3>New Type Photos.PHFetchResultEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject element, uint elementIndex, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSObject element, uint elementIndex, bool stop);</span>
}
</pre>
</div> <!-- end type PHFetchResultEnumerator -->
<div> <!-- start type PHImageDataHandler -->
<h3>New Type Photos.PHImageDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData data, Foundation.NSString dataUti, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageDataHandler -->
<div> <!-- start type PHImageKeys -->
<h3>New Type Photos.PHImageKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PHImageKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Cancelled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsDegraded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloud { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultRequestID { get; }</span>
}
</pre>
</div> <!-- end type PHImageKeys -->
<div> <!-- start type PHImageManager -->
<h3>New Type Photos.PHImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHImageManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize MaximumSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelImageRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageForAsset (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);</span>
}
</pre>
</div> <!-- end type PHImageManager -->
<div> <!-- start type PHImageRequestOptions -->
<h3>New Type Photos.PHImageRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect NormalizedCropRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Synchronous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHImageRequestOptions -->
<div> <!-- start type PHImageRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHImageRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Opportunistic = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsDeliveryMode -->
<div> <!-- start type PHImageRequestOptionsResizeMode -->
<h3>New Type Photos.PHImageRequestOptionsResizeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	<span class='added added-field ' data-is-non-breaking="">Exact = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsResizeMode -->
<div> <!-- start type PHImageRequestOptionsVersion -->
<h3>New Type Photos.PHImageRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unadjusted = 1,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsVersion -->
<div> <!-- start type PHImageResultHandler -->
<h3>New Type Photos.PHImageResultHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageResultHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AppKit.NSImage result, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AppKit.NSImage result, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageResultHandler -->
<div> <!-- start type PHLivePhotoEditingOption -->
<h3>New Type Photos.PHLivePhotoEditingOption</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingOption : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldRenderAtPlaybackTime { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingOption -->
<div> <!-- start type PHObject -->
<h3>New Type Photos.PHObject</h3>
<pre class='added' data-is-non-breaking="">
public class PHObject : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHObject -->
<div> <!-- start type PHObjectChangeDetails -->
<h3>New Type Photos.PHObjectChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AssetContentChanged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ObjectWasDeleted { get; }</span>
}
</pre>
</div> <!-- end type PHObjectChangeDetails -->
<div> <!-- start type PHPhotoLibrary -->
<h3>New Type Photos.PHPhotoLibrary</h3>
<pre class='added' data-is-non-breaking="">
public class PHPhotoLibrary : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHPhotoLibrary SharedPhotoLibrary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformChanges (System.Action changeHandler, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PerformChangesAndWait (System.Action changeHandler, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestAuthorization (System.Action&lt;PHAuthorizationStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;PHAuthorizationStatus&gt; RequestAuthorizationAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary -->
<div> <!-- start type PHPhotoLibraryChangeObserver -->
<h3>New Type Photos.PHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PHPhotoLibraryChangeObserver : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHPhotoLibraryChangeObserver, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type PHPhotoLibraryChangeObserver -->
<div> <!-- start type PHPhotoLibrary_CloudIdentifiers -->
<h3>New Type Photos.PHPhotoLibrary_CloudIdentifiers</h3>
<pre class='added' data-is-non-breaking="">
public static class PHPhotoLibrary_CloudIdentifiers {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCloudIdentifier[] GetCloudIdentifiers (PHPhotoLibrary This, string[] localIdentifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetLocalIdentifiers (PHPhotoLibrary This, PHCloudIdentifier[] cloudIdentifiers);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary_CloudIdentifiers -->
<div> <!-- start type PHProject -->
<h3>New Type Photos.PHProject</h3>
<pre class='added' data-is-non-breaking="">
public class PHProject : Photos.PHAssetCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProject ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; }</span>
}
</pre>
</div> <!-- end type PHProject -->
<div> <!-- start type PHProjectChangeRequest -->
<h3>New Type Photos.PHProjectChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectChangeRequest (PHProject project);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ProjectExtensionData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetKeyAsset (PHAsset keyAsset);</span>
}
</pre>
</div> <!-- end type PHProjectChangeRequest -->
<div> <!-- start type PHProjectCreationSource -->
<h3>New Type Photos.PHProjectCreationSource</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectCreationSource {
	<span class='added added-field ' data-is-non-breaking="">Album = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Memory = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Project = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectBook = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCalendar = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectCard = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectExtension = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectPrintOrder = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ProjectSlideshow = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserSelection = 1,</span>
}
</pre>
</div> <!-- end type PHProjectCreationSource -->
<div> <!-- start type PHProjectSectionType -->
<h3>New Type Photos.PHProjectSectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectSectionType {
	<span class='added added-field ' data-is-non-breaking="">Auxiliary = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type PHProjectSectionType -->
<div> <!-- start type PHProjectTextElementType -->
<h3>New Type Photos.PHProjectTextElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHProjectTextElementType {
	<span class='added added-field ' data-is-non-breaking="">Body = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title = 1,</span>
}
</pre>
</div> <!-- end type PHProjectTextElementType -->

</div> <!-- end namespace Photos -->
<!-- start namespace QTKit --> <div> 
<h2>Namespace QTKit</h2>
<!-- start type QTCaptureLayer --> <div>
<h3>Type Changed: QTKit.QTCaptureLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTCaptureLayer -->
<!-- start type QTMovieLayer --> <div>
<h3>Type Changed: QTKit.QTMovieLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QTMovieLayer -->

</div> <!-- end namespace QTKit -->
<!-- start namespace QuartzComposer --> <div> 
<h2>Namespace QuartzComposer</h2>
<!-- start type QCCompositionLayer --> <div>
<h3>Type Changed: QuartzComposer.QCCompositionLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type QCCompositionLayer -->

</div> <!-- end namespace QuartzComposer -->
<!-- start namespace SafariServices --> <div> 
<h2>Namespace SafariServices</h2>
<!-- start type SFSafariApplication --> <div>
<h3>Type Changed: SafariServices.SFSafariApplication</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetHostApplication (System.Action&lt;AppKit.NSRunningApplication&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AppKit.NSRunningApplication&gt; GetHostApplicationAsync ();</span>
</pre>
</div>

</div> <!-- end type SFSafariApplication -->
<!-- start type SFSafariToolbarItem --> <div>
<h3>Type Changed: SafariServices.SFSafariToolbarItem</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetLabel (string label);</span>
</pre>
</div>

</div> <!-- end type SFSafariToolbarItem -->
<div> <!-- start type SFSafariServicesVersion -->
<h3>New Type SafariServices.SFSafariServicesVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SFSafariServicesVersion {
	<span class='added added-field ' data-is-non-breaking="">V10_0 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">V10_1 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">V11_0 = 2,</span>
}
</pre>
</div> <!-- end type SFSafariServicesVersion -->

</div> <!-- end namespace SafariServices -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNAnimatable --> <div>
<h3>Type Changed: SceneKit.SCNAnimatable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNAnimatable -->
<!-- start type SCNAnimatable_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNAnimatable_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void AddAnimation (ISCNAnimatable This, SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimationPlayer GetAnimationPlayer (ISCNAnimatable This, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAnimationUsingBlendOutDuration (ISCNAnimatable This, Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNAnimatable_Extensions -->
<!-- start type SCNBlendMode --> <div>
<h3>Type Changed: SceneKit.SCNBlendMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Max = 6,</span>
</pre>
</div>

</div> <!-- end type SCNBlendMode -->
<!-- start type SCNCamera --> <div>
<h3>Type Changed: SceneKit.SCNCamera</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ApertureBladeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FStop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FieldOfView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint FocalBlurSampleCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FocalLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FocusDistance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNCameraProjectionDirection ProjectionDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScreenSpaceAmbientOcclusionBias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScreenSpaceAmbientOcclusionDepthThreshold { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScreenSpaceAmbientOcclusionIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScreenSpaceAmbientOcclusionNormalThreshold { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ScreenSpaceAmbientOcclusionRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat SensorHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsDepthOfField { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNCamera -->
<!-- start type SCNConstraint --> <div>
<h3>Type Changed: SceneKit.SCNConstraint</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Incremental { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNConstraint -->
<!-- start type SCNDebugOptions --> <div>
<h3>Type Changed: SceneKit.SCNDebugOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">RenderAsWireframe = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowCameras = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowConstraints = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowCreases = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowSkeletons = 128,</span>
</pre>
</div>

</div> <!-- end type SCNDebugOptions -->
<!-- start type SCNGeometry --> <div>
<h3>Type Changed: SceneKit.SCNGeometry</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNGeometryTessellator Tessellator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsAdaptiveSubdivision { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNGeometry -->
<!-- start type SCNGeometryElement --> <div>
<h3>Type Changed: SceneKit.SCNGeometryElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumPointScreenSpaceRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinimumPointScreenSpaceRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PointSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange PrimitiveRange { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNGeometryElement -->
<!-- start type SCNHitTest --> <div>
<h3>Type Changed: SceneKit.SCNHitTest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionSearchModeKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTest -->
<!-- start type SCNHitTestOptions --> <div>
<h3>Type Changed: SceneKit.SCNHitTestOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SCNHitTestSearchMode? OptionSearchMode { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTestOptions -->
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->
<!-- start type SCNLight --> <div>
<h3>Type Changed: SceneKit.SCNLight</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyAdjustsShadowProjection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ForcesBackFaceCasters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumShadowDistance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SampleDistributedShadowMaps { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ShadowCascadeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ShadowCascadeSplittingFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData SphericalHarmonicsCoefficients { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNLight -->
<!-- start type SCNLookAtConstraint --> <div>
<h3>Type Changed: SceneKit.SCNLookAtConstraint</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 LocalFront { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 TargetOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldUp { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNLookAtConstraint -->
<!-- start type SCNMaterial --> <div>
<h3>Type Changed: SceneKit.SCNMaterial</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNColorMask ColorBufferWriteMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty Displacement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNFillMode FillMode { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNMaterial -->
<!-- start type SCNMaterialProperty --> <div>
<h3>Type Changed: SceneKit.SCNMaterialProperty</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNColorMask TextureComponents { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNMaterialProperty -->
<!-- start type SCNMorpher --> <div>
<h3>Type Changed: SceneKit.SCNMorpher</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UnifiesNormals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Weights { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetWeight (string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetWeight (nfloat weight, string targetName);</span>
</pre>
</div>

</div> <!-- end type SCNMorpher -->
<!-- start type SCNNode --> <div>
<h3>Type Changed: SceneKit.SCNNode</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual SCNMatrix4 WorldTransform { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNodeFocusBehavior FocusBehavior { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SCNVector3 LocalFront { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SCNVector3 LocalRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SCNVector3 LocalUp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldFront { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNQuaternion WorldOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldPosition { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldUp { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNVector3 ConvertVectorFromNode (SCNVector3 vector, SCNNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNVector3 ConvertVectorToNode (SCNVector3 vector, SCNNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LocalRotate (SCNQuaternion rotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LocalTranslate (SCNVector3 translation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Look (SCNVector3 worldTarget);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Look (SCNVector3 worldTarget, SCNVector3 worldUp, SCNVector3 localFront);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Rotate (SCNQuaternion worldRotation, SCNVector3 worldTarget);</span>
</pre>
</div>

</div> <!-- end type SCNNode -->
<!-- start type SCNParticleSystem --> <div>
<h3>Type Changed: SceneKit.SCNParticleSystem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 OrientationDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ParticleIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ParticleIntensityVariation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNParticleSystem -->
<!-- start type SCNPhysicsContact --> <div>
<h3>Type Changed: SceneKit.SCNPhysicsContact</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat SweepTestFraction { get; }</span>
</pre>
</div>

</div> <!-- end type SCNPhysicsContact -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double time);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNScene --> <div>
<h3>Type Changed: SceneKit.SCNScene</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">GameplayKit.IGKSceneRootNodeType</span>
</pre>
</div>

</div> <!-- end type SCNScene -->
<!-- start type SCNSceneRendererDelegate --> <div>
<h3>Type Changed: SceneKit.SCNSceneRendererDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidApplyConstraints (ISCNSceneRenderer renderer, double atTime);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRendererDelegate -->
<!-- start type SCNSceneRendererDelegate_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNSceneRendererDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidApplyConstraints (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, double atTime);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRendererDelegate_Extensions -->
<!-- start type SCNTechnique --> <div>
<h3>Type Changed: SceneKit.SCNTechnique</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNTechnique -->
<!-- start type SCNTransformConstraint --> <div>
<h3>Type Changed: SceneKit.SCNTransformConstraint</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SCNTransformConstraint CreateOrientationConstraint (bool inWorldSpace, System.Func&lt;SCNNode,SceneKit.SCNQuaternion,SceneKit.SCNQuaternion&gt; transformHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNTransformConstraint CreatePositionConstraint (bool inWorldSpace, System.Func&lt;SCNNode,SceneKit.SCNVector3,SceneKit.SCNVector3&gt; transformHandler);</span>
</pre>
</div>

</div> <!-- end type SCNTransformConstraint -->
<!-- start type SCNTransparencyMode --> <div>
<h3>Type Changed: SceneKit.SCNTransparencyMode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DualLayer = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SingleLayer = 2,</span>
</pre>
</div>

</div> <!-- end type SCNTransparencyMode -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISCNCameraControlConfiguration CameraControlConfiguration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNCameraController DefaultCameraController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RendersContinuously { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNView -->
<div> <!-- start type ISCNAnimationProtocol -->
<h3>New Type SceneKit.ISCNAnimationProtocol</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNAnimationProtocol : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISCNAnimationProtocol -->
<div> <!-- start type ISCNAvoidOccluderConstraintDelegate -->
<h3>New Type SceneKit.ISCNAvoidOccluderConstraintDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNAvoidOccluderConstraintDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISCNAvoidOccluderConstraintDelegate -->
<div> <!-- start type ISCNCameraControlConfiguration -->
<h3>New Type SceneKit.ISCNCameraControlConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNCameraControlConfiguration : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsTranslation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoSwitchToFreeCamera { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FlyModeVelocity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PanSensitivity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RotationSensitivity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TruckSensitivity { get; set; }</span>
}
</pre>
</div> <!-- end type ISCNCameraControlConfiguration -->
<div> <!-- start type ISCNCameraControllerDelegate -->
<h3>New Type SceneKit.ISCNCameraControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNCameraControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISCNCameraControllerDelegate -->
<div> <!-- start type SCNAccelerationConstraint -->
<h3>New Type SceneKit.SCNAccelerationConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNAccelerationConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAccelerationConstraint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAccelerationConstraint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAccelerationConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAccelerationConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Damping { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat DecelerationDistance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumLinearAcceleration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumLinearVelocity { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNAccelerationConstraint Create ();</span>
}
</pre>
</div> <!-- end type SCNAccelerationConstraint -->
<div> <!-- start type SCNAnimation -->
<h3>New Type SceneKit.SCNAnimation</h3>
<pre class='added' data-is-non-breaking="">
public class SCNAnimation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimationProtocol, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAnimation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAnimation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Additive { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNAnimationDidStartHandler AnimationDidStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNAnimationDidStopHandler AnimationDidStop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNAnimationEvent[] AnimationEvents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AppliedOnCompletion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Autoreverses { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double BlendInDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double BlendOutDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Cumulative { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FillsBackward { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FillsForward { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string KeyPath { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RemovedOnCompletion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RepeatCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double StartDelay { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNTimingFunction TimingFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesSceneTimeBase { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimation FromCAAnimation (CoreAnimation.CAAnimation caAnimation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimation FromName (string animationName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimation FromUrl (Foundation.NSUrl animationUrl);</span>
}
</pre>
</div> <!-- end type SCNAnimation -->
<div> <!-- start type SCNAnimationDidStartHandler -->
<h3>New Type SceneKit.SCNAnimationDidStartHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SCNAnimationDidStartHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimationDidStartHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (SCNAnimation animation, SCNAnimatable receiver, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (SCNAnimation animation, SCNAnimatable receiver);</span>
}
</pre>
</div> <!-- end type SCNAnimationDidStartHandler -->
<div> <!-- start type SCNAnimationDidStopHandler -->
<h3>New Type SceneKit.SCNAnimationDidStopHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SCNAnimationDidStopHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimationDidStopHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (SCNAnimation animation, SCNAnimatable receiver, bool completed, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (SCNAnimation animation, SCNAnimatable receiver, bool completed);</span>
}
</pre>
</div> <!-- end type SCNAnimationDidStopHandler -->
<div> <!-- start type SCNAnimationPlayer -->
<h3>New Type SceneKit.SCNAnimationPlayer</h3>
<pre class='added' data-is-non-breaking="">
public class SCNAnimationPlayer : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimationPlayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAnimationPlayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAnimationPlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAnimationPlayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNAnimation Animation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BlendFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Paused { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Speed { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimationPlayer FromAnimation (SCNAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString[] GetAnimationKeys ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAnimationPaused (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PauseAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Play ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllAnimations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimation (Foundation.NSString key, nfloat duration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopWithBlendOutDuration (double seconds);</span>
}
</pre>
</div> <!-- end type SCNAnimationPlayer -->
<div> <!-- start type SCNAvoidOccluderConstraint -->
<h3>New Type SceneKit.SCNAvoidOccluderConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNAvoidOccluderConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAvoidOccluderConstraint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAvoidOccluderConstraint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAvoidOccluderConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAvoidOccluderConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISCNAvoidOccluderConstraintDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OccluderCategoryBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAvoidOccluderConstraint FromTarget (SCNNode target);</span>
}
</pre>
</div> <!-- end type SCNAvoidOccluderConstraint -->
<div> <!-- start type SCNAvoidOccluderConstraintDelegate -->
<h3>New Type SceneKit.SCNAvoidOccluderConstraintDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SCNAvoidOccluderConstraintDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISCNAvoidOccluderConstraintDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNAvoidOccluderConstraintDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAvoidOccluderConstraintDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNAvoidOccluderConstraintDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAvoidOccluder (SCNAvoidOccluderConstraint constraint, SCNNode occluder, SCNNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAvoidOccluder (SCNAvoidOccluderConstraint constraint, SCNNode occluder, SCNNode node);</span>
}
</pre>
</div> <!-- end type SCNAvoidOccluderConstraintDelegate -->
<div> <!-- start type SCNAvoidOccluderConstraintDelegate_Extensions -->
<h3>New Type SceneKit.SCNAvoidOccluderConstraintDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNAvoidOccluderConstraintDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAvoidOccluder (ISCNAvoidOccluderConstraintDelegate This, SCNAvoidOccluderConstraint constraint, SCNNode occluder, SCNNode node);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAvoidOccluder (ISCNAvoidOccluderConstraintDelegate This, SCNAvoidOccluderConstraint constraint, SCNNode occluder, SCNNode node);</span>
}
</pre>
</div> <!-- end type SCNAvoidOccluderConstraintDelegate_Extensions -->
<div> <!-- start type SCNCameraController -->
<h3>New Type SceneKit.SCNCameraController</h3>
<pre class='added' data-is-non-breaking="">
public class SCNCameraController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNCameraController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNCameraController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNCameraController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticTarget { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISCNCameraControllerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InertiaEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float InertiaFriction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InertiaRunning { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNInteractionMode InteractionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumHorizontalAngle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumVerticalAngle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumHorizontalAngle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumVerticalAngle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode PointOfView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 WorldUp { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginInteraction (CoreGraphics.CGPoint location, CoreGraphics.CGSize viewport);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClearRoll ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ContinueInteraction (CoreGraphics.CGPoint location, CoreGraphics.CGSize viewport, nfloat sensitivity);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dolly (float delta, CoreGraphics.CGPoint screenPoint, CoreGraphics.CGSize viewport);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DollyToTarget (float delta);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInteraction (CoreGraphics.CGPoint location, CoreGraphics.CGSize viewport, CoreGraphics.CGPoint velocity);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FrameNodes (SCNNode[] nodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Roll (float delta, CoreGraphics.CGPoint screenPoint, CoreGraphics.CGSize viewport);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RollAroundTarget (float delta);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Rotate (float deltaX, float deltaY);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopInertia ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TranslateInCameraSpace (float deltaX, float deltaY, float deltaZ);</span>
}
</pre>
</div> <!-- end type SCNCameraController -->
<div> <!-- start type SCNCameraControllerDelegate -->
<h3>New Type SceneKit.SCNCameraControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SCNCameraControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISCNCameraControllerDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNCameraControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNCameraControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNCameraControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CameraInertiaDidEnd (SCNCameraController cameraController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CameraInertiaWillStart (SCNCameraController cameraController);</span>
}
</pre>
</div> <!-- end type SCNCameraControllerDelegate -->
<div> <!-- start type SCNCameraControllerDelegate_Extensions -->
<h3>New Type SceneKit.SCNCameraControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNCameraControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CameraInertiaDidEnd (ISCNCameraControllerDelegate This, SCNCameraController cameraController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CameraInertiaWillStart (ISCNCameraControllerDelegate This, SCNCameraController cameraController);</span>
}
</pre>
</div> <!-- end type SCNCameraControllerDelegate_Extensions -->
<div> <!-- start type SCNCameraProjectionDirection -->
<h3>New Type SceneKit.SCNCameraProjectionDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNCameraProjectionDirection {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type SCNCameraProjectionDirection -->
<div> <!-- start type SCNColorMask -->
<h3>New Type SceneKit.SCNColorMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum SCNColorMask {
	<span class='added added-field ' data-is-non-breaking="">All = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Alpha = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Blue = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Green = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Red = 8,</span>
}
</pre>
</div> <!-- end type SCNColorMask -->
<div> <!-- start type SCNDistanceConstraint -->
<h3>New Type SceneKit.SCNDistanceConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNDistanceConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNDistanceConstraint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNDistanceConstraint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNDistanceConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNDistanceConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumDistance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinimumDistance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNDistanceConstraint FromTarget (SCNNode target);</span>
}
</pre>
</div> <!-- end type SCNDistanceConstraint -->
<div> <!-- start type SCNFillMode -->
<h3>New Type SceneKit.SCNFillMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNFillMode {
	<span class='added added-field ' data-is-non-breaking="">Fill = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Lines = 1,</span>
}
</pre>
</div> <!-- end type SCNFillMode -->
<div> <!-- start type SCNGeometryTessellator -->
<h3>New Type SceneKit.SCNGeometryTessellator</h3>
<pre class='added' data-is-non-breaking="">
public class SCNGeometryTessellator : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNGeometryTessellator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNGeometryTessellator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNGeometryTessellator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Adaptive { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat EdgeTessellationFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat InsideTessellationFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumEdgeLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ScreenSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNTessellationSmoothingMode SmoothingMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TessellationFactorScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTessellationPartitionMode TessellationPartitionMode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SCNGeometryTessellator -->
<div> <!-- start type SCNHitTestSearchMode -->
<h3>New Type SceneKit.SCNHitTestSearchMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNHitTestSearchMode {
	<span class='added added-field ' data-is-non-breaking="">All = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Closest = 0,</span>
}
</pre>
</div> <!-- end type SCNHitTestSearchMode -->
<div> <!-- start type SCNInteractionMode -->
<h3>New Type SceneKit.SCNInteractionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNInteractionMode {
	<span class='added added-field ' data-is-non-breaking="">Fly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitAngleMapping = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitArcball = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitCenteredArcball = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitTurntable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Pan = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Truck = 6,</span>
}
</pre>
</div> <!-- end type SCNInteractionMode -->
<div> <!-- start type SCNNodeFocusBehavior -->
<h3>New Type SceneKit.SCNNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SCNNodeFocusBehavior -->
<div> <!-- start type SCNPhysicsConeTwistJoint -->
<h3>New Type SceneKit.SCNPhysicsConeTwistJoint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNPhysicsConeTwistJoint : SceneKit.SCNPhysicsBehavior, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNPhysicsConeTwistJoint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNPhysicsConeTwistJoint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNPhysicsConeTwistJoint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNPhysicsConeTwistJoint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNPhysicsBody BodyA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNPhysicsBody BodyB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMatrix4 FrameA { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMatrix4 FrameB { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumAngularLimit1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumAngularLimit2 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumTwistAngle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNPhysicsConeTwistJoint FromBodies (SCNPhysicsBody bodyA, SCNMatrix4 frameA, SCNPhysicsBody bodyB, SCNMatrix4 frameB);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNPhysicsConeTwistJoint FromBody (SCNPhysicsBody body, SCNMatrix4 frame);</span>
}
</pre>
</div> <!-- end type SCNPhysicsConeTwistJoint -->
<div> <!-- start type SCNReplicatorConstraint -->
<h3>New Type SceneKit.SCNReplicatorConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNReplicatorConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNReplicatorConstraint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNReplicatorConstraint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNReplicatorConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNReplicatorConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNQuaternion OrientationOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 PositionOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReplicatesOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReplicatesPosition { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReplicatesScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 ScaleOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode Target { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNReplicatorConstraint FromTarget (SCNNode target);</span>
}
</pre>
</div> <!-- end type SCNReplicatorConstraint -->
<div> <!-- start type SCNSliderConstraint -->
<h3>New Type SceneKit.SCNSliderConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class SCNSliderConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNSliderConstraint ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNSliderConstraint (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNSliderConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNSliderConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CollisionCategoryBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNVector3 Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Radius { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNSliderConstraint Create ();</span>
}
</pre>
</div> <!-- end type SCNSliderConstraint -->
<div> <!-- start type SCNTessellationSmoothingMode -->
<h3>New Type SceneKit.SCNTessellationSmoothingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNTessellationSmoothingMode {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PNTriangles = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Phong = 2,</span>
}
</pre>
</div> <!-- end type SCNTessellationSmoothingMode -->
<div> <!-- start type SCNTimingFunction -->
<h3>New Type SceneKit.SCNTimingFunction</h3>
<pre class='added' data-is-non-breaking="">
public class SCNTimingFunction : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNTimingFunction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SCNTimingFunction (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNTimingFunction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNTimingFunction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SCNTimingFunction Create (CoreAnimation.CAMediaTimingFunction caTimingFunction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNTimingFunction Create (SCNActionTimingMode timingMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SCNTimingFunction -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

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
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLineBreakMode LineBreakMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLines { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredMaxLayoutWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKLabelNode FromText (Foundation.NSAttributedString attributedText);</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<!-- start type SKScene --> <div>
<h3>Type Changed: SpriteKit.SKScene</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">GameplayKit.IGKSceneRootNodeType</span>
</pre>
</div>

</div> <!-- end type SKScene -->
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
<!-- start type SKUniform --> <div>
<h3>Type Changed: SpriteKit.SKUniform</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat2x2)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix2 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat3x3)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix3 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat4x4)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix4 value);</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, OpenTK.NMatrix2 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, OpenTK.NMatrix3 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, OpenTK.NMatrix4 value);</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat2x2Value' instead.")]
	public virtual OpenTK.Matrix2 FloatMatrix2Value { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat3x3Value' instead.")]
	public virtual OpenTK.Matrix3 FloatMatrix3Value { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat4x4Value' instead.")]
	public virtual OpenTK.Matrix4 FloatMatrix4Value { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix2 MatrixFloat2x2Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix3 MatrixFloat3x3Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix4 MatrixFloat4x4Value { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat2x2)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix2 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat3x3)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix3 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'the '(string, MatrixFloat4x4)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix4 value);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.NMatrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.NMatrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.NMatrix4 value);</span>
</pre>
</div>

</div> <!-- end type SKUniform -->
<div> <!-- start type SKRenderer -->
<h3>New Type SpriteKit.SKRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class SKRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IgnoresSiblingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldCullNonVisibleNodes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsDrawCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsNodeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsPhysics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsQuadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKRenderer FromDevice (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLRenderCommandEncoder renderCommandEncoder, Metal.MTLRenderPassDescriptor renderPassDescriptor, Metal.IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double currentTime);</span>
}
</pre>
</div> <!-- end type SKRenderer -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, AppKit.INSTouchBarProvider, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NVector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace VideoToolbox --> <div> 
<h2>Namespace VideoToolbox</h2>
<!-- start type VTCompressionProperties --> <div>
<h3>Type Changed: VideoToolbox.VTCompressionProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public double? BaseLayerFrameRate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ContentLightLevelInfo { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string EncoderId { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData MasteringDisplayColorVolume { get; set; }</span>
</pre>
</div>

</div> <!-- end type VTCompressionProperties -->
<!-- start type VTCompressionPropertyKey --> <div>
<h3>Type Changed: VideoToolbox.VTCompressionPropertyKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BaseLayerFrameRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContentLightLevelInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EncoderId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MasteringDisplayColorVolume { get; }</span>
</pre>
</div>

</div> <!-- end type VTCompressionPropertyKey -->
<!-- start type VTDecompressionProperties --> <div>
<h3>Type Changed: VideoToolbox.VTDecompressionProperties</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int? TemporalLevelLimit { get; set; }</span>
</pre>
</div>

</div> <!-- end type VTDecompressionProperties -->
<!-- start type VTDecompressionPropertyKey --> <div>
<h3>Type Changed: VideoToolbox.VTDecompressionPropertyKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TemporalLevelLimit { get; }</span>
</pre>
</div>

</div> <!-- end type VTDecompressionPropertyKey -->
<!-- start type VTDecompressionSession --> <div>
<h3>Type Changed: VideoToolbox.VTDecompressionSession</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsHardwareDecodeSupported (CoreMedia.CMVideoCodecType codecType);</span>
</pre>
</div>

</div> <!-- end type VTDecompressionSession -->
<!-- start type VTProfileLevel --> <div>
<h3>Type Changed: VideoToolbox.VTProfileLevel</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HevcMain10AutoLevel = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">HevcMainAutoLevel = 49,</span>
</pre>
</div>

</div> <!-- end type VTProfileLevel -->
<!-- start type VTProfileLevelKeys --> <div>
<h3>Type Changed: VideoToolbox.VTProfileLevelKeys</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Hevc_Main10_AutoLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Hevc_Main_AutoLevel { get; }</span>
</pre>
</div>

</div> <!-- end type VTProfileLevelKeys -->
<!-- start type VTVideoEncoder --> <div>
<h3>Type Changed: VideoToolbox.VTVideoEncoder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static VTSupportedEncoderProperties GetSupportedEncoderProperties (int width, int height, CoreMedia.CMVideoCodecType codecType, Foundation.NSDictionary encoderSpecification);</span>
</pre>
</div>

</div> <!-- end type VTVideoEncoder -->
<div> <!-- start type VTSupportedEncoderProperties -->
<h3>New Type VideoToolbox.VTSupportedEncoderProperties</h3>
<pre class='added' data-is-non-breaking="">
public class VTSupportedEncoderProperties {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTSupportedEncoderProperties ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string EncoderId { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary SupportedProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VTSupportedEncoderProperties -->

</div> <!-- end namespace VideoToolbox -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKErrorCode --> <div>
<h3>Type Changed: WebKit.WKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreCompileFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreLookUpFailed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreRemoveFailed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentRuleListStoreVersionMismatch = 9,</span>
</pre>
</div>

</div> <!-- end type WKErrorCode -->
<!-- start type WKFrameInfo --> <div>
<h3>Type Changed: WebKit.WKFrameInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKWebView WebView { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type WKFrameInfo -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddContentRuleList (WKContentRuleList contentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllContentRuleLists ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (WKContentRuleList contentRuleList);</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebView --> <div>
<h3>Type Changed: WebKit.WKWebView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool HandlesUrlScheme (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot (WKSnapshotConfiguration snapshotConfiguration, System.Action&lt;AppKit.NSImage,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AppKit.NSImage&gt; TakeSnapshotAsync (WKSnapshotConfiguration snapshotConfiguration);</span>
</pre>
</div>

</div> <!-- end type WKWebView -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IWKUrlSchemeHandler GetUrlSchemeHandler (string urlScheme);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetUrlSchemeHandler (IWKUrlSchemeHandler urlSchemeHandler, string urlScheme);</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKHttpCookieStore HttpCookieStore { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<div> <!-- start type IWKHttpCookieStoreObserver -->
<h3>New Type WebKit.IWKHttpCookieStoreObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKHttpCookieStoreObserver : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IWKHttpCookieStoreObserver -->
<div> <!-- start type IWKUrlSchemeHandler -->
<h3>New Type WebKit.IWKUrlSchemeHandler</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeHandler : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopUrlSchemeTask (WKWebView webView, IWKUrlSchemeTask urlSchemeTask);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeHandler -->
<div> <!-- start type IWKUrlSchemeTask -->
<h3>New Type WebKit.IWKUrlSchemeTask</h3>
<pre class='added' data-is-non-breaking="">
public interface IWKUrlSchemeTask : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrlRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFailWithError (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveResponse (Foundation.NSUrlResponse response);</span>
}
</pre>
</div> <!-- end type IWKUrlSchemeTask -->
<div> <!-- start type WKContentRuleList -->
<h3>New Type WebKit.WKContentRuleList</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleList : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type WKContentRuleList -->
<div> <!-- start type WKContentRuleListStore -->
<h3>New Type WebKit.WKContentRuleListStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKContentRuleListStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKContentRuleListStore ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKContentRuleListStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static WKContentRuleListStore DefaultStore { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CompileContentRuleList (string identifier, string encodedContentRuleList, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; CompileContentRuleListAsync (string identifier, string encodedContentRuleList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static WKContentRuleListStore FromUrl (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAvailableContentRuleListIdentifiers (System.Action&lt;System.String[]&gt; callback);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; GetAvailableContentRuleListIdentifiersAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LookUpContentRuleList (string identifier, System.Action&lt;WKContentRuleList,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;WKContentRuleList&gt; LookUpContentRuleListAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveContentRuleList (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveContentRuleListAsync (string identifier);</span>
}
</pre>
</div> <!-- end type WKContentRuleListStore -->
<div> <!-- start type WKHttpCookieStore -->
<h3>New Type WebKit.WKHttpCookieStore</h3>
<pre class='added' data-is-non-breaking="">
public class WKHttpCookieStore : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKHttpCookieStore (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeleteCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DeleteCookieAsync (Foundation.NSHttpCookie cookie);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetAllCookies (System.Action&lt;Foundation.NSHttpCookie[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSHttpCookie[]&gt; GetAllCookiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObserver (IWKHttpCookieStoreObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCookie (Foundation.NSHttpCookie cookie, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetCookieAsync (Foundation.NSHttpCookie cookie);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStore -->
<div> <!-- start type WKHttpCookieStoreObserver_Extensions -->
<h3>New Type WebKit.WKHttpCookieStoreObserver_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class WKHttpCookieStoreObserver_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CookiesDidChangeInCookieStore (IWKHttpCookieStoreObserver This, WKHttpCookieStore cookieStore);</span>
}
</pre>
</div> <!-- end type WKHttpCookieStoreObserver_Extensions -->
<div> <!-- start type WKSnapshotConfiguration -->
<h3>New Type WebKit.WKSnapshotConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class WKSnapshotConfiguration : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKSnapshotConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected WKSnapshotConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SnapshotWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type WKSnapshotConfiguration -->

</div> <!-- end namespace WebKit -->
<!-- start namespace CoreML --> <div> 
<h2>New Namespace CoreML</h2>

<div> <!-- start type IMLFeatureProvider -->
<h3>New Type CoreML.IMLFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLFeatureProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type IMLFeatureProvider -->
<div> <!-- start type MLDictionaryConstraint -->
<h3>New Type CoreML.MLDictionaryConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType KeyType { get; }</span>
}
</pre>
</div> <!-- end type MLDictionaryConstraint -->
<div> <!-- start type MLDictionaryFeatureProvider -->
<h3>New Type CoreML.MLDictionaryFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryFeatureProvider : Foundation.NSObject, IMLFeatureProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; dictionary, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureValue&gt; Dictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLFeatureValue Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type MLDictionaryFeatureProvider -->
<div> <!-- start type MLFeatureDescription -->
<h3>New Type CoreML.MLFeatureDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLDictionaryConstraint DictionaryConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLImageConstraint ImageConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayConstraint MultiArrayConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAllowed (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureDescription -->
<div> <!-- start type MLFeatureType -->
<h3>New Type CoreML.MLFeatureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLFeatureType {
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Int64 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiArray = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 3,</span>
}
</pre>
</div> <!-- end type MLFeatureType -->
<div> <!-- start type MLFeatureValue -->
<h3>New Type CoreML.MLFeatureValue</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; DictionaryValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer ImageBufferValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Int64Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArray MultiArrayValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Undefined { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (MLMultiArray value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (CoreVideo.CVPixelBuffer value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue Create (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; value, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue CreateUndefined (MLFeatureType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureValue -->
<div> <!-- start type MLImageConstraint -->
<h3>New Type CoreML.MLImageConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLImageConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelFormatType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsHigh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsWide { get; }</span>
}
</pre>
</div> <!-- end type MLImageConstraint -->
<div> <!-- start type MLModel -->
<h3>New Type CoreML.MLModel</h3>
<pre class='added' data-is-non-breaking="">
public class MLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLModelDescription ModelDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl CompileModel (Foundation.NSUrl modelUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLModel Create (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, MLPredictionOptions options, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLModel -->
<div> <!-- start type MLModelDescription -->
<h3>New Type CoreML.MLModelDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelDescription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; InputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLModelMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; OutputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedFeatureName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedProbabilitiesName { get; }</span>
}
</pre>
</div> <!-- end type MLModelDescription -->
<div> <!-- start type MLModelError -->
<h3>New Type CoreML.MLModelError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLModelError {
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">IO = 3,</span>
}
</pre>
</div> <!-- end type MLModelError -->
<div> <!-- start type MLModelErrorExtensions -->
<h3>New Type CoreML.MLModelErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLModelErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MLModelError self);</span>
}
</pre>
</div> <!-- end type MLModelErrorExtensions -->
<div> <!-- start type MLModelMetadata -->
<h3>New Type CoreML.MLModelMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelMetadata : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CreatorDefined { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string License { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string VersionString { get; }</span>
}
</pre>
</div> <!-- end type MLModelMetadata -->
<div> <!-- start type MLMultiArray -->
<h3>New Type CoreML.MLMultiArray</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (nint[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSNumber[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, nint[] shape, MLMultiArrayDataType dataType, nint[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr DataPointer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint[] Shape { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint[] Strides { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSNumber GetObject (nint[] indices);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetObject (Foundation.NSNumber obj, nint[] indices);</span>
}
</pre>
</div> <!-- end type MLMultiArray -->
<div> <!-- start type MLMultiArrayConstraint -->
<h3>New Type CoreML.MLMultiArrayConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArrayConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint[] Shape { get; }</span>
}
</pre>
</div> <!-- end type MLMultiArrayConstraint -->
<div> <!-- start type MLMultiArrayDataType -->
<h3>New Type CoreML.MLMultiArrayDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLMultiArrayDataType {
	<span class='added added-field ' data-is-non-breaking="">Double = 65600,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 65568,</span>
	<span class='added added-field ' data-is-non-breaking="">Int32 = 131104,</span>
}
</pre>
</div> <!-- end type MLMultiArrayDataType -->
<div> <!-- start type MLPredictionOptions -->
<h3>New Type CoreML.MLPredictionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class MLPredictionOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLPredictionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
}
</pre>
</div> <!-- end type MLPredictionOptions -->
</div> <!-- end namespace CoreML -->

<!-- start namespace ExternalAccessory --> <div> 
<h2>New Namespace ExternalAccessory</h2>

<div> <!-- start type EAAccessory -->
<h3>New Type ExternalAccessory.EAAccessory</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Connected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ConnectionID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IEAAccessoryDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DockType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FirmwareRevision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string HardwareRevision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ModelNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ProtocolStrings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SerialNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler Disconnected;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type EAAccessory -->
<div> <!-- start type EAAccessoryDelegate -->
<h3>New Type ExternalAccessory.EAAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryDelegate : Foundation.NSObject, IEAAccessoryDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAAccessoryDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Disconnected (EAAccessory accessory);</span>
}
</pre>
</div> <!-- end type EAAccessoryDelegate -->
<div> <!-- start type EAAccessoryDelegate_Extensions -->
<h3>New Type ExternalAccessory.EAAccessoryDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class EAAccessoryDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Disconnected (IEAAccessoryDelegate This, EAAccessory accessory);</span>
}
</pre>
</div> <!-- end type EAAccessoryDelegate_Extensions -->
<div> <!-- start type EAAccessoryEventArgs -->
<h3>New Type ExternalAccessory.EAAccessoryEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryEventArgs : Foundation.NSNotificationEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAAccessoryEventArgs (Foundation.NSNotification notification);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public EAAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EAAccessory Selected { get; }</span>
}
</pre>
</div> <!-- end type EAAccessoryEventArgs -->
<div> <!-- start type EAAccessoryManager -->
<h3>New Type ExternalAccessory.EAAccessoryManager</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual EAAccessory[] ConnectedAccessories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidConnectNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidDisconnectNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static EAAccessoryManager SharedAccessoryManager { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterForLocalNotifications ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterForLocalNotifications ();</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type EAAccessoryManager -->
<div> <!-- start type EABluetoothAccessoryPickerError -->
<h3>New Type ExternalAccessory.EABluetoothAccessoryPickerError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EABluetoothAccessoryPickerError {
	<span class='added added-field ' data-is-non-breaking="">AlreadyConnected = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NotFound = 1,</span>
}
</pre>
</div> <!-- end type EABluetoothAccessoryPickerError -->
<div> <!-- start type EABluetoothAccessoryPickerErrorExtensions -->
<h3>New Type ExternalAccessory.EABluetoothAccessoryPickerErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class EABluetoothAccessoryPickerErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (EABluetoothAccessoryPickerError self);</span>
}
</pre>
</div> <!-- end type EABluetoothAccessoryPickerErrorExtensions -->
<div> <!-- start type EASession -->
<h3>New Type ExternalAccessory.EASession</h3>
<pre class='added' data-is-non-breaking="">
public class EASession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EASession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EASession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EASession (EAAccessory accessory, string protocol);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual EAAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSInputStream InputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSOutputStream OutputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProtocolString { get; }</span>
}
</pre>
</div> <!-- end type EASession -->
<div> <!-- start type IEAAccessoryDelegate -->
<h3>New Type ExternalAccessory.IEAAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IEAAccessoryDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IEAAccessoryDelegate -->
</div> <!-- end namespace ExternalAccessory -->

<!-- start namespace IOSurface --> <div> 
<h2>New Namespace IOSurface</h2>

<div> <!-- start type IOSurface -->
<h3>New Type IOSurface.IOSurface</h3>
<pre class='added' data-is-non-breaking="">
public class IOSurface : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IOSurface ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public IOSurface (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected IOSurface (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public IOSurface (IOSurfaceOptions properties);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected IOSurface (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; AllAttachments { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AllocationSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsPixelSizeCasting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint BytesPerElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ElementHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ElementWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InUse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int LocalUseCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PlaneCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Seed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DecrementUseCount ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetAttachment (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetBaseAddress (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetBytesPerElement (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetBytesPerRow (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetElementHeight (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetElementWidth (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetHeight (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetWidth (uint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void IncrementUseCount ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int Lock (IOSurfaceLockOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public int Lock (IOSurfaceLockOptions options, int seed);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllAttachments ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAttachment (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAttachment (Foundation.NSObject anObject, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public int Unlock (IOSurfaceLockOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public int Unlock (IOSurfaceLockOptions options, int seed);</span>
}
</pre>
</div> <!-- end type IOSurface -->
<div> <!-- start type IOSurfaceLockOptions -->
<h3>New Type IOSurface.IOSurfaceLockOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum IOSurfaceLockOptions {
	<span class='added added-field ' data-is-non-breaking="">AvoidSync = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnly = 1,</span>
}
</pre>
</div> <!-- end type IOSurfaceLockOptions -->
<div> <!-- start type IOSurfaceMemoryMap -->
<h3>New Type IOSurface.IOSurfaceMemoryMap</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum IOSurfaceMemoryMap {
	<span class='added added-field ' data-is-non-breaking="">CopybackCache = 768,</span>
	<span class='added added-field ' data-is-non-breaking="">CopybackInnerCache = 1280,</span>
	<span class='added added-field ' data-is-non-breaking="">DefaultCache = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">InhibitCache = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteCombineCache = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteThruCache = 512,</span>
}
</pre>
</div> <!-- end type IOSurfaceMemoryMap -->
<div> <!-- start type IOSurfaceOptions -->
<h3>New Type IOSurface.IOSurfaceOptions</h3>
<pre class='added' data-is-non-breaking="">
public class IOSurfaceOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public IOSurfaceOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public IOSurfaceOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public nint? AllocSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? BytesPerElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? BytesPerRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IOSurfaceMemoryMap? CacheMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ElementHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ElementWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? PixelFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? PixelSizeCastingAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneBase { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneBytesPerElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneBytesPerRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneElementHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneElementWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary[] PlaneInfo { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? PlaneWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Width { get; set; }</span>
}
</pre>
</div> <!-- end type IOSurfaceOptions -->
<div> <!-- start type IOSurfacePurgeabilityState -->
<h3>New Type IOSurface.IOSurfacePurgeabilityState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum IOSurfacePurgeabilityState {
	<span class='added added-field ' data-is-non-breaking="">Empty = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">KeepCurrent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NonVolatile = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Volatile = 1,</span>
}
</pre>
</div> <!-- end type IOSurfacePurgeabilityState -->
</div> <!-- end namespace IOSurface -->

<!-- start namespace PhotosUI --> <div> 
<h2>New Namespace PhotosUI</h2>

<div> <!-- start type IPHContentEditingController -->
<h3>New Type PhotosUI.IPHContentEditingController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHContentEditingController : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldShowCancelConfirmation { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanHandleAdjustmentData (Photos.PHAdjustmentData adjustmentData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelContentEditing ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishContentEditing (System.Action&lt;Photos.PHContentEditingOutput&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartContentEditing (Photos.PHContentEditingInput contentEditingInput, AppKit.NSImage placeholderImage);</span>
}
</pre>
</div> <!-- end type IPHContentEditingController -->
<div> <!-- start type IPHProjectExtensionController -->
<h3>New Type PhotosUI.IPHProjectExtensionController</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHProjectExtensionController : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginProject (PHProjectExtensionContext extensionContext, PHProjectInfo projectInfo, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishProject (System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeProject (PHProjectExtensionContext extensionContext, System.Action&lt;Foundation.NSError&gt; completion);</span>
}
</pre>
</div> <!-- end type IPHProjectExtensionController -->
<div> <!-- start type PHProjectAssetElement -->
<h3>New Type PhotosUI.PHProjectAssetElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectAssetElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectAssetElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectAssetElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Annotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHCloudIdentifier CloudAssetIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect CropRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectRegionOfInterest[] RegionsOfInterest { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectAssetElement -->
<div> <!-- start type PHProjectElement -->
<h3>New Type PhotosUI.PHProjectElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectElement : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Placement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectElement -->
<div> <!-- start type PHProjectExtensionContext -->
<h3>New Type PhotosUI.PHProjectExtensionContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectExtensionContext : Foundation.NSExtensionContext, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectExtensionContext (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectExtensionContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHPhotoLibrary PhotoLibrary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProject Project { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionContext -->
<div> <!-- start type PHProjectExtensionController_Extensions -->
<h3>New Type PhotosUI.PHProjectExtensionController_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectExtensionController_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHProjectTypeDescription[] GetSupportedProjectTypes (IPHProjectExtensionController This);</span>
}
</pre>
</div> <!-- end type PHProjectExtensionController_Extensions -->
<div> <!-- start type PHProjectInfo -->
<h3>New Type PhotosUI.PHProjectInfo</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectCreationSource CreationSource { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSection[] Sections { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectInfo -->
<div> <!-- start type PHProjectJournalEntryElement -->
<h3>New Type PhotosUI.PHProjectJournalEntryElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectJournalEntryElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectJournalEntryElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectJournalEntryElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectAssetElement AssetElement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Date { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTextElement TextElement { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectJournalEntryElement -->
<div> <!-- start type PHProjectRegionOfInterest -->
<h3>New Type PhotosUI.PHProjectRegionOfInterest</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectRegionOfInterest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectRegionOfInterest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectRegionOfInterest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Weight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectRegionOfInterest -->
<div> <!-- start type PHProjectSection -->
<h3>New Type PhotosUI.PHProjectSection</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSection : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSection (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectSectionContent[] SectionContents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectSectionType SectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSection -->
<div> <!-- start type PHProjectSectionContent -->
<h3>New Type PhotosUI.PHProjectSectionContent</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectSectionContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectSectionContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectSectionContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double AspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHCloudIdentifier[] CloudAssetIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectElement[] Elements { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectSectionContent -->
<div> <!-- start type PHProjectTextElement -->
<h3>New Type PhotosUI.PHProjectTextElement</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTextElement : PhotosUI.PHProjectElement, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTextElement (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTextElement (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHProjectTextElementType TextElementType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTextElement -->
<div> <!-- start type PHProjectType -->
<h3>New Type PhotosUI.PHProjectType</h3>
<pre class='added' data-is-non-breaking="">
public static class PHProjectType {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Undefined { get; }</span>
}
</pre>
</div> <!-- end type PHProjectType -->
<div> <!-- start type PHProjectTypeDescription -->
<h3>New Type PhotosUI.PHProjectTypeDescription</h3>
<pre class='added' data-is-non-breaking="">
public class PHProjectTypeDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHProjectTypeDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHProjectTypeDescription (Foundation.NSString projectType, string localizedTitle, string localizedDescription, AppKit.NSImage image, PHProjectTypeDescription[] subtypeDescriptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ProjectType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProjectTypeDescription[] SubtypeDescriptions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHProjectTypeDescription -->
</div> <!-- end namespace PhotosUI -->

<!-- start namespace Vision --> <div> 
<h2>New Namespace Vision</h2>

<div> <!-- start type IVNFaceObservationAccepting -->
<h3>New Type Vision.IVNFaceObservationAccepting</h3>
<pre class='added' data-is-non-breaking="">
public interface IVNFaceObservationAccepting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type IVNFaceObservationAccepting -->
<div> <!-- start type VNBarcodeObservation -->
<h3>New Type Vision.VNBarcodeObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNBarcodeObservation : Vision.VNRectangleObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor BarcodeDescriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PayloadStringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology Symbology { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakSymbology { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNBarcodeObservation -->
<div> <!-- start type VNBarcodeSymbology -->
<h3>New Type Vision.VNBarcodeSymbology</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNBarcodeSymbology {
	<span class='added added-field ' data-is-non-breaking="">Aztec = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Code128 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39Checksum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAscii = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAsciiChecksum = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93i = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DataMatrix = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean13 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5Checksum = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Itf14 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Pdf417 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">QR = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Upce = 16,</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbology -->
<div> <!-- start type VNBarcodeSymbologyExtensions -->
<h3>New Type Vision.VNBarcodeSymbologyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNBarcodeSymbologyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VNBarcodeSymbology self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (VNBarcodeSymbology[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology[] GetValues (Foundation.NSString[] constants);</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbologyExtensions -->
<div> <!-- start type VNClassificationObservation -->
<h3>New Type Vision.VNClassificationObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNClassificationObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNClassificationObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type VNClassificationObservation -->
<div> <!-- start type VNCoreMLFeatureValueObservation -->
<h3>New Type Vision.VNCoreMLFeatureValueObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLFeatureValueObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLFeatureValueObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreML.MLFeatureValue FeatureValue { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLFeatureValueObservation -->
<div> <!-- start type VNCoreMLModel -->
<h3>New Type Vision.VNCoreMLModel</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNCoreMLModel FromMLModel (CoreML.MLModel model, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNCoreMLModel -->
<div> <!-- start type VNCoreMLRequest -->
<h3>New Type Vision.VNCoreMLRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNImageCropAndScaleOption ImageCropAndScaleOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNCoreMLModel Model { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLRequest -->
<div> <!-- start type VNDetectBarcodesRequest -->
<h3>New Type Vision.VNDetectBarcodesRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNDetectBarcodesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectBarcodesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static VNBarcodeSymbology[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology[] Symbologies { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected static Foundation.NSString[] WeakSupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString[] WeakSymbologies { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectBarcodesRequest -->
<div> <!-- start type VNDetectFaceLandmarksRequest -->
<h3>New Type Vision.VNDetectFaceLandmarksRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceLandmarksRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVNFaceObservationAccepting {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceLandmarksRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceLandmarksRequest -->
<div> <!-- start type VNDetectFaceRectanglesRequest -->
<h3>New Type Vision.VNDetectFaceRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceRectanglesRequest -->
<div> <!-- start type VNDetectHorizonRequest -->
<h3>New Type Vision.VNDetectHorizonRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectHorizonRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectHorizonRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectHorizonRequest -->
<div> <!-- start type VNDetectRectanglesRequest -->
<h3>New Type Vision.VNDetectRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumObservations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumConfidence { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float QuadratureTolerance { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectRectanglesRequest -->
<div> <!-- start type VNDetectTextRectanglesRequest -->
<h3>New Type Vision.VNDetectTextRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectTextRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectTextRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportCharacterBoxes { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectTextRectanglesRequest -->
<div> <!-- start type VNDetectedObjectObservation -->
<h3>New Type Vision.VNDetectedObjectObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectedObjectObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectedObjectObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BoundingBox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNDetectedObjectObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNDetectedObjectObservation -->
<div> <!-- start type VNErrorCode -->
<h3>New Type Vision.VNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">IOError = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidImage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModel = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOperation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOption = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingOption = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationFailed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBoundsError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfMemory = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestCancelled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownError = 11,</span>
}
</pre>
</div> <!-- end type VNErrorCode -->
<div> <!-- start type VNErrorCodeExtensions -->
<h3>New Type Vision.VNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VNErrorCode self);</span>
}
</pre>
</div> <!-- end type VNErrorCodeExtensions -->
<div> <!-- start type VNFaceLandmarkRegion -->
<h3>New Type Vision.VNFaceLandmarkRegion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarkRegion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PointCount { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion -->
<div> <!-- start type VNFaceLandmarkRegion2D -->
<h3>New Type Vision.VNFaceLandmarkRegion2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarkRegion2D : Vision.VNFaceLandmarkRegion, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] NormalizedPoints { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] GetPointsInImage (CoreGraphics.CGSize imageSize);</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion2D -->
<div> <!-- start type VNFaceLandmarks -->
<h3>New Type Vision.VNFaceLandmarks</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarks : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks -->
<div> <!-- start type VNFaceLandmarks2D -->
<h3>New Type Vision.VNFaceLandmarks2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarks2D : Vision.VNFaceLandmarks, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D AllPoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D FaceContour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D InnerLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftPupil { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D MedianLine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D Nose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D NoseCrest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D OuterLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightPupil { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks2D -->
<div> <!-- start type VNFaceObservation -->
<h3>New Type Vision.VNFaceObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNFaceObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarks2D Landmarks { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNFaceObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNFaceObservation -->
<div> <!-- start type VNHomographicImageRegistrationRequest -->
<h3>New Type Vision.VNHomographicImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNHomographicImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNHomographicImageRegistrationRequest -->
<div> <!-- start type VNHorizonObservation -->
<h3>New Type Vision.VNHorizonObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNHorizonObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHorizonObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Angle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
}
</pre>
</div> <!-- end type VNHorizonObservation -->
<div> <!-- start type VNImageAlignmentObservation -->
<h3>New Type Vision.VNImageAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageAlignmentObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageAlignmentObservation -->
<div> <!-- start type VNImageBasedRequest -->
<h3>New Type Vision.VNImageBasedRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageBasedRequest : Vision.VNRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageBasedRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect RegionOfInterest { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageBasedRequest -->
<div> <!-- start type VNImageCropAndScaleOption -->
<h3>New Type Vision.VNImageCropAndScaleOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNImageCropAndScaleOption {
	<span class='added added-field ' data-is-non-breaking="">CenterCrop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFill = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFit = 1,</span>
}
</pre>
</div> <!-- end type VNImageCropAndScaleOption -->
<div> <!-- start type VNImageHomographicAlignmentObservation -->
<h3>New Type Vision.VNImageHomographicAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageHomographicAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageHomographicAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.NMatrix3 WarpTransform { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageHomographicAlignmentObservation -->
<div> <!-- start type VNImageOptions -->
<h3>New Type Vision.VNImageOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreImage.CIContext CIContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary WeakProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageOptions -->
<div> <!-- start type VNImageRegistrationRequest -->
<h3>New Type Vision.VNImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageRegistrationRequest : Vision.VNTargetedImageRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageRegistrationRequest -->
<div> <!-- start type VNImageRequestHandler -->
<h3>New Type Vision.VNImageRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNImageRequestHandler -->
<div> <!-- start type VNImageTranslationAlignmentObservation -->
<h3>New Type Vision.VNImageTranslationAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageTranslationAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageTranslationAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AlignmentTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageTranslationAlignmentObservation -->
<div> <!-- start type VNObservation -->
<h3>New Type Vision.VNObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNObservation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type VNObservation -->
<div> <!-- start type VNPixelBufferObservation -->
<h3>New Type Vision.VNPixelBufferObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNPixelBufferObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNPixelBufferObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
}
</pre>
</div> <!-- end type VNPixelBufferObservation -->
<div> <!-- start type VNRectangleObservation -->
<h3>New Type Vision.VNRectangleObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNRectangleObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRectangleObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNRectangleObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNRectangleObservation -->
<div> <!-- start type VNRequest -->
<h3>New Type Vision.VNRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestCompletionHandler CompletionHandler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreferBackgroundProcessing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice PreferredMetalContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual T[] GetResults&lt;T&gt; ();</span>
}
</pre>
</div> <!-- end type VNRequest -->
<div> <!-- start type VNRequestCompletionHandler -->
<h3>New Type Vision.VNRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate VNRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (VNRequest request, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (VNRequest request, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNRequestCompletionHandler -->
<div> <!-- start type VNRequestTrackingLevel -->
<h3>New Type Vision.VNRequestTrackingLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNRequestTrackingLevel {
	<span class='added added-field ' data-is-non-breaking="">Accurate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
}
</pre>
</div> <!-- end type VNRequestTrackingLevel -->
<div> <!-- start type VNSequenceRequestHandler -->
<h3>New Type Vision.VNSequenceRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNSequenceRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNSequenceRequestHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNSequenceRequestHandler -->
<div> <!-- start type VNTargetedImageRequest -->
<h3>New Type Vision.VNTargetedImageRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTargetedImageRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTargetedImageRequest -->
<div> <!-- start type VNTextObservation -->
<h3>New Type Vision.VNTextObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNTextObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTextObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRectangleObservation[] CharacterBoxes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNTextObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNTextObservation -->
<div> <!-- start type VNTrackObjectRequest -->
<h3>New Type Vision.VNTrackObjectRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackObjectRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackObjectRequest -->
<div> <!-- start type VNTrackRectangleRequest -->
<h3>New Type Vision.VNTrackRectangleRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackRectangleRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackRectangleRequest -->
<div> <!-- start type VNTrackingRequest -->
<h3>New Type Vision.VNTrackingRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTrackingRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackingRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNDetectedObjectObservation InputObservation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LastFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestTrackingLevel TrackingLevel { get; set; }</span>
}
</pre>
</div> <!-- end type VNTrackingRequest -->
<div> <!-- start type VNTranslationalImageRegistrationRequest -->
<h3>New Type Vision.VNTranslationalImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTranslationalImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTranslationalImageRegistrationRequest -->
<div> <!-- start type VNUtils -->
<h3>New Type Vision.VNUtils</h3>
<pre class='added' data-is-non-breaking="">
public static class VNUtils {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGRect NormalizedIdentityRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (CoreGraphics.CGPoint normalizedPoint, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetImageRect (CoreGraphics.CGRect normalizedRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetNormalizedFaceBoundingBoxPoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetNormalizedRect (CoreGraphics.CGRect imageRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsIdentityRect (CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type VNUtils -->
</div> <!-- end namespace Vision -->

</div>
