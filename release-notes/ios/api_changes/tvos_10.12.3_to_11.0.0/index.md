---
id: 46057298-C195-405B-851E-8FE3EA0E69EF
title: "tvOS 10.12.3 to 11.0.0"
---

# API diff

 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


 [MonoTouch.Dialog-1.dll](#diff/xi/Xamarin.TVOS/MonoTouch.Dialog-1.html)

   


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
<!-- start type AVAssetDownloadTask --> <div>
<h3>Type Changed: AVFoundation.AVAssetDownloadTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type AVAssetDownloadTask -->
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
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoShutdownEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InManualRenderingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioInputNode InputNode { get; }</span>
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
<!-- start type AVAudioSession --> <div>
<h3>Type Changed: AVFoundation.AVAudioSession</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioSessionRouteSharingPolicy RouteSharingPolicy { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetCategory (string category, string mode, AVAudioSessionRouteSharingPolicy policy, AVAudioSessionCategoryOptions options, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AVAudioSession -->
<!-- start type AVAudioSettings --> <div>
<h3>Type Changed: AVFoundation.AVAudioSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileTypeKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioSettings -->
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeySpaceAudioFile { get; }</span>
</pre>
</div>

</div> <!-- end type AVMetadata -->
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

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVKitMetadataIdentifier --> <div>
<h3>Type Changed: AVKit.AVKitMetadataIdentifier</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type AVKitMetadataIdentifier -->
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIViewController CustomInfoViewController { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeInfoViews { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeTransportBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILayoutGuide UnobscuredContentGuide { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewController -->
<!-- start type AVPlayerViewControllerDelegate --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldDismiss (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillTransitionToVisibilityOfTransportBar (AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate -->
<!-- start type AVPlayerViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldDismiss (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillTransitionToVisibilityOfTransportBar (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate_Extensions -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor ActiveTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVRoutePickerViewButtonStyle RoutePickerButtonStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class AVRoutePickerViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonStyle -->
<h3>New Type AVKit.AVRoutePickerViewButtonStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonStyle {
	<span class='added added-field ' data-is-non-breaking="">Custom = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Plain = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">System = 0,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonStyle -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : Foundation.NSObject, IAVRoutePickerViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVPlayerViewControllerAnimationCoordinator -->
<h3>New Type AVKit.IAVPlayerViewControllerAnimationCoordinator</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVPlayerViewControllerAnimationCoordinator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedAnimations (System.Action animations, System.Action&lt;bool&gt; completion);</span>
}
</pre>
</div> <!-- end type IAVPlayerViewControllerAnimationCoordinator -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
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
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsRunning (AUAudioUnit This);</span>
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
<!-- start type CKNotificationInfo --> <div>
<h3>Type Changed: CloudKit.CKNotificationInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CollapseIdKey { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldSendMutableContent { get; set; }</span>
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
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAEAGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEAGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEAGLLayer -->
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
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsNextDrawableTimeout { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
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
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
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
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
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
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBError --> <div>
<h3>Type Changed: CoreBluetooth.CBError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnknownDevice = 12,</span>
</pre>
</div>

</div> <!-- end type CBError -->
<!-- start type CBPeripheral --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheral</h3>
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
<!-- start type CBUUID --> <div>
<h3>Type Changed: CoreBluetooth.CBUUID</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString L2CapPsmCharacteristicString { get; }</span>
</pre>
</div>

</div> <!-- end type CBUUID -->
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
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
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
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVDepthData DepthData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatL16 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatL8 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLA16 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLA8 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLAf { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLAh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLf { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatLh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int FormatRGBA16 { get; }</span>
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
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
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
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->

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

</div> <!-- end namespace CoreMedia -->
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

</div> <!-- end namespace CoreVideo -->
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
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadObject (ObjCRuntime.Class aClass, System.Action&lt;INSItemProviderReading,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (ObjCRuntime.Class aClass);</span>
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
<!-- start type NSProcessInfo --> <div>
<h3>Type Changed: Foundation.NSProcessInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSProcessInfoThermalState ThermalState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString ThermalStateDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type NSProcessInfo.Notifications --> <div>
<h3>Type Changed: Foundation.NSProcessInfo.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveThermalStateDidChange (System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveThermalStateDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSProcessInfo.Notifications -->

</div> <!-- end type NSProcessInfo -->
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
<!-- start type NSValue --> <div>
<h3>Type Changed: Foundation.NSValue</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.NSDirectionalEdgeInsets DirectionalEdgeInsetsValue { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSValue FromDirectionalEdgeInsets (UIKit.NSDirectionalEdgeInsets insets);</span>
</pre>
</div>

</div> <!-- end type NSValue -->
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
<div> <!-- start type NSProcessInfoThermalState -->
<h3>New Type Foundation.NSProcessInfoThermalState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSProcessInfoThermalState {
	<span class='added added-field ' data-is-non-breaking="">Critical = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Fair = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Nominal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Serious = 2,</span>
}
</pre>
</div> <!-- end type NSProcessInfoThermalState -->
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
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaterniond Attitude { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAttitudeAndRotationRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3d RotationRate { get; }</span>
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

</div> <!-- end namespace GameplayKit -->
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessory --> <div>
<h3>Type Changed: HomeKit.HMAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FirmwareVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Model { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessoryProfile[] Profiles { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidAddProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidRemoveProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryFirmwareVersionEventArgs&gt; DidUpdateFirmwareVersion;</span>
</pre>
</div>

</div> <!-- end type HMAccessory -->
<!-- start type HMAccessoryDelegate --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFirmwareVersion (HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate -->
<!-- start type HMAccessoryDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateFirmwareVersion (IHMAccessoryDelegate This, HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate_Extensions -->
<!-- start type HMCharacteristicEvent --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicEvent</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSMutableCopying</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual HMCharacteristic Characteristic { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual Foundation.INSCopying TriggerValue { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicEvent -->
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorTemperature = 115,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMError --> <div>
<h3>Type Changed: HomeKit.HMError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IncompatibleHomeHub = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">NoHomeHub = 91,</span>
</pre>
</div>

</div> <!-- end type HMError -->
<!-- start type HMEvent --> <div>
<h3>Type Changed: HomeKit.HMEvent</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSupported (HMHome home);</span>
</pre>
</div>

</div> <!-- end type HMEvent -->
<!-- start type HMEventTrigger --> <div>
<h3>Type Changed: HomeKit.HMEventTrigger</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEvent[] EndEvents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExecuteOnce { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents[] Recurrences { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEventTriggerActivationState TriggerActivationState { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTrigger (HMPresenceEvent presenceEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringAfterSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBeforeSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenDates (Foundation.NSDateComponents firstDateComponents, Foundation.NSDateComponents secondDateComponents);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenSignificantEvent (HMSignificantTimeEvent firstSignificantEvent, HMSignificantTimeEvent secondSignificantEvent);</span>
</pre>
</div>

</div> <!-- end type HMEventTrigger -->
<!-- start type HMHome --> <div>
<h3>Type Changed: HomeKit.HMHome</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMHomeHubState HomeHubState { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateAccessControlForCurrentUser;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeHubStateEventArgs&gt; DidUpdateHomeHubState;</span>
</pre>
</div>

</div> <!-- end type HMHome -->
<!-- start type HMHomeDelegate --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateAccessControlForCurrentUser (HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateHomeHubState (HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate -->
<!-- start type HMHomeDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateAccessControlForCurrentUser (IHMHomeDelegate This, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateHomeHubState (IHMHomeDelegate This, HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate_Extensions -->
<!-- start type HMLocationEvent --> <div>
<h3>Type Changed: HomeKit.HMLocationEvent</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSMutableCopying</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual CoreLocation.CLRegion Region { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type HMLocationEvent -->
<div> <!-- start type HMAccessoryFirmwareVersionEventArgs -->
<h3>New Type HomeKit.HMAccessoryFirmwareVersionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryFirmwareVersionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryFirmwareVersionEventArgs (string firmwareVersion);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FirmwareVersion { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryFirmwareVersionEventArgs -->
<div> <!-- start type HMAccessoryProfileEventArgs -->
<h3>New Type HomeKit.HMAccessoryProfileEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryProfileEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryProfileEventArgs (HMAccessoryProfile profile);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessoryProfile Profile { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryProfileEventArgs -->
<div> <!-- start type HMCalendarEvent -->
<h3>New Type HomeKit.HMCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCalendarEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents FireDateComponents { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCalendarEvent -->
<div> <!-- start type HMCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicThresholdRangeEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMNumberRange ThresholdRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMDurationEvent -->
<h3>New Type HomeKit.HMDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMDurationEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMDurationEvent -->
<div> <!-- start type HMEventTriggerActivationState -->
<h3>New Type HomeKit.HMEventTriggerActivationState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMEventTriggerActivationState {
	<span class='added added-field ' data-is-non-breaking="">Disabled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoCompatibleHomeHub = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoHomeHub = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoLocationServicesAuthorization = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Enabled = 4,</span>
}
</pre>
</div> <!-- end type HMEventTriggerActivationState -->
<div> <!-- start type HMHomeHubState -->
<h3>New Type HomeKit.HMHomeHubState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMHomeHubState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAvailable = 0,</span>
}
</pre>
</div> <!-- end type HMHomeHubState -->
<div> <!-- start type HMHomeHubStateEventArgs -->
<h3>New Type HomeKit.HMHomeHubStateEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeHubStateEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeHubStateEventArgs (HMHomeHubState homeHubState);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMHomeHubState HomeHubState { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeHubStateEventArgs -->
<div> <!-- start type HMMutableCalendarEvent -->
<h3>New Type HomeKit.HMMutableCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCalendarEvent : HomeKit.HMCalendarEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents FireDateComponents { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCalendarEvent -->
<div> <!-- start type HMMutableCharacteristicEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicEvent : HomeKit.HMCharacteristicEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicEvent (HMCharacteristic characteristic, Foundation.INSCopying triggerValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.INSCopying TriggerValue { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicEvent -->
<div> <!-- start type HMMutableCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicThresholdRangeEvent : HomeKit.HMCharacteristicThresholdRangeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override HMNumberRange ThresholdRange { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMMutableDurationEvent -->
<h3>New Type HomeKit.HMMutableDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableDurationEvent : HomeKit.HMDurationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override double Duration { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableDurationEvent -->
<div> <!-- start type HMMutableLocationEvent -->
<h3>New Type HomeKit.HMMutableLocationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableLocationEvent : HomeKit.HMLocationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableLocationEvent (CoreLocation.CLRegion region);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CoreLocation.CLRegion Region { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableLocationEvent -->
<div> <!-- start type HMMutablePresenceEvent -->
<h3>New Type HomeKit.HMMutablePresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutablePresenceEvent : HomeKit.HMPresenceEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventType PresenceEventType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventUserType PresenceUserType { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutablePresenceEvent -->
<div> <!-- start type HMMutableSignificantTimeEvent -->
<h3>New Type HomeKit.HMMutableSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableSignificantTimeEvent : HomeKit.HMSignificantTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableSignificantTimeEvent -->
<div> <!-- start type HMNumberRange -->
<h3>New Type HomeKit.HMNumberRange</h3>
<pre class='added' data-is-non-breaking="">
public class HMNumberRange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Max { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Min { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMax (Foundation.NSNumber maxValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMin (Foundation.NSNumber minValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromRange (Foundation.NSNumber minValue, Foundation.NSNumber maxValue);</span>
}
</pre>
</div> <!-- end type HMNumberRange -->
<div> <!-- start type HMPresenceEvent -->
<h3>New Type HomeKit.HMPresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMPresenceEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMPresenceEvent (HMPresenceEventType presenceEventType, HMPresenceEventUserType presenceUserType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventType PresenceEventType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventUserType PresenceUserType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMPresenceEvent -->
<div> <!-- start type HMPresenceEventType -->
<h3>New Type HomeKit.HMPresenceEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMPresenceEventType {
	<span class='added added-field ' data-is-non-breaking="">AtHome = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">EveryEntry = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">EveryExit = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FirstEntry = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LastExit = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAtHome = 4,</span>
}
</pre>
</div> <!-- end type HMPresenceEventType -->
<div> <!-- start type HMPresenceEventUserType -->
<h3>New Type HomeKit.HMPresenceEventUserType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMPresenceEventUserType {
	<span class='added added-field ' data-is-non-breaking="">CurrentUser = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CustomUsers = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeUsers = 2,</span>
}
</pre>
</div> <!-- end type HMPresenceEventUserType -->
<div> <!-- start type HMSignificantEventExtensions -->
<h3>New Type HomeKit.HMSignificantEventExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMSignificantEventExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMSignificantEvent self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMSignificantEvent GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMSignificantEventExtensions -->
<div> <!-- start type HMSignificantTimeEvent -->
<h3>New Type HomeKit.HMSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMSignificantTimeEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMSignificantTimeEvent -->
<div> <!-- start type HMTimeEvent -->
<h3>New Type HomeKit.HMTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMTimeEvent : HomeKit.HMEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMTimeEvent -->

</div> <!-- end namespace HomeKit -->
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
<div> <!-- start type MKMarkerAnnotationView -->
<h3>New Type MapKit.MKMarkerAnnotationView</h3>
<pre class='added' data-is-non-breaking="">
public class MKMarkerAnnotationView : MapKit.MKAnnotationView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (IMKAnnotation annotation, string reuseIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AnimatesWhenAdded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility SubtitleVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility TitleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKMarkerAnnotationViewAppearance : MapKit.MKAnnotationView+MKAnnotationViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	}
}
</pre>
</div> <!-- end type MKMarkerAnnotationView -->
<div> <!-- start type MKScaleView -->
<h3>New Type MapKit.MKScaleView</h3>
<pre class='added' data-is-non-breaking="">
public class MKScaleView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKScaleView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKScaleViewAlignment LegendAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKMapView MapView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility ScaleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView FromMapView (MKMapView mapView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKScaleViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type MKScaleView -->
<div> <!-- start type MKScaleViewAlignment -->
<h3>New Type MapKit.MKScaleViewAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKScaleViewAlignment {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type MKScaleViewAlignment -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfo NowPlaying { get; set; }</span>
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
<div> <!-- start type MPMediaItem -->
<h3>New Type MediaPlayer.MPMediaItem</h3>
<pre class='added' data-is-non-breaking="">
public class MPMediaItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (IntPtr handle);</span>
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
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
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
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPersistentID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RatingProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReleaseDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SkipCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserGroupingProperty { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanFilterByProperty (Foundation.NSString property);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetObject (Foundation.NSObject key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);</span>
}
</pre>
</div> <!-- end type MPMediaItem -->
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
<div> <!-- start type NSUserActivity_MediaPlayerAdditions -->
<h3>New Type MediaPlayer.NSUserActivity_MediaPlayerAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_MediaPlayerAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetExternalMediaContentIdentifier (Foundation.NSUserActivity This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetExternalMediaContentIdentifier (Foundation.NSUserActivity This, Foundation.NSString identifier);</span>
}
</pre>
</div> <!-- end type NSUserActivity_MediaPlayerAdditions -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLArgument --> <div>
<h3>Type Changed: Metal.MTLArgument</h3>
<div>
<p>Added property:</p>
<pre>
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
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeap (IMTLComputeCommandEncoder This, IMTLHeap heap);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeaps (IMTLComputeCommandEncoder This, IMTLHeap[] heaps, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResource (IMTLComputeCommandEncoder This, IMTLResource resource, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResources (IMTLComputeCommandEncoder This, IMTLResource[] resources, uint count, MTLResourceUsage usage);</span>
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
<!-- start type MTLDevice_Extensions --> <div>
<h3>Type Changed: Metal.MTLDevice_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLArgumentEncoder CreateArgumentEncoder (IMTLDevice This, MTLArgumentDescriptor[] arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLLibrary CreateLibrary (IMTLDevice This, Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLTexture CreateTexture (IMTLDevice This, MTLTextureDescriptor descriptor, IOSurface.IOSurface iosurface, uint plane);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLArgumentBuffersTier GetArgumentBuffersSupport (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetCurrentAllocatedSize (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetDefaultSamplePositions (IMTLDevice This, MTLSamplePosition[] positions, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void GetDefaultSamplePositions (IMTLDevice This, IntPtr positions, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetMaxThreadgroupMemoryLength (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetMinimumLinearTextureAlignment (IMTLDevice This, MTLPixelFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetProgrammableSamplePositionsSupported (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetRasterOrderGroupsSupported (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLReadWriteTextureTier GetReadWriteTextureSupport (IMTLDevice This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetRegistryId (IMTLDevice This);</span>
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
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public void SetDepthClipMode (<span class='added '>this </span>IMTLRenderCommandEncoder This, MTLDepthClipMode depthClipMode)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetColorStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions, uint colorAttachmentIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDepthStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStencilStoreActionOptions (IMTLRenderCommandEncoder This, MTLStoreActionOptions storeActionOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeap (IMTLRenderCommandEncoder This, IMTLHeap heap);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseHeaps (IMTLRenderCommandEncoder This, IMTLHeap[] heaps, uint count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResource (IMTLRenderCommandEncoder This, IMTLResource resource, MTLResourceUsage usage);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UseResources (IMTLRenderCommandEncoder This, IMTLResource[] resources, uint count, MTLResourceUsage usage);</span>
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
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetAllocatedSize (IMTLResource This);</span>
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
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<!-- start type MPSBinaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSBinaryImageKernel -->
<!-- start type MPSCnnConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnConvolution -->
<!-- start type MPSCnnConvolutionDescriptor --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionDescriptor (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSCnnConvolutionDescriptor -->
<!-- start type MPSCnnCrossChannelNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnCrossChannelNormalization -->
<!-- start type MPSCnnFullyConnected --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnFullyConnected -->
<!-- start type MPSCnnKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnKernel -->
<!-- start type MPSCnnLocalContrastNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLocalContrastNormalization -->
<!-- start type MPSCnnLogSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLogSoftMax -->
<!-- start type MPSCnnNeuron --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuron</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuron -->
<!-- start type MPSCnnNeuronAbsolute --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronAbsolute -->
<!-- start type MPSCnnNeuronLinear --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronLinear -->
<!-- start type MPSCnnNeuronReLU --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronReLU -->
<!-- start type MPSCnnNeuronSigmoid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronSigmoid -->
<!-- start type MPSCnnNeuronTanH --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronTanH -->
<!-- start type MPSCnnPooling --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPooling</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPooling -->
<!-- start type MPSCnnPoolingAverage --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingAverage -->
<!-- start type MPSCnnPoolingMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingMax -->
<!-- start type MPSCnnSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSoftMax -->
<!-- start type MPSCnnSpatialNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSpatialNormalization -->
<!-- start type MPSImageAreaMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMax -->
<!-- start type MPSImageAreaMin --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMin</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMin -->
<!-- start type MPSImageBox --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageBox</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageBox -->
<!-- start type MPSImageConversion --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConversion</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConversion -->
<!-- start type MPSImageConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConvolution -->
<!-- start type MPSImageDilate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageDilate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageDilate -->
<!-- start type MPSImageErode --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageErode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageErode -->
<!-- start type MPSImageGaussianBlur --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianBlur -->
<!-- start type MPSImageGaussianPyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianPyramid -->
<!-- start type MPSImageHistogram --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogram</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogram -->
<!-- start type MPSImageHistogramEqualization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramEqualization -->
<!-- start type MPSImageHistogramSpecification --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramSpecification -->
<!-- start type MPSImageIntegral --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegral</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegral -->
<!-- start type MPSImageIntegralOfSquares --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegralOfSquares -->
<!-- start type MPSImageLanczosScale --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLanczosScale</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLanczosScale -->
<!-- start type MPSImageLaplacian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLaplacian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLaplacian -->
<!-- start type MPSImageMedian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageMedian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageMedian -->
<!-- start type MPSImagePyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImagePyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImagePyramid -->
<!-- start type MPSImageSobel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageSobel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageSobel -->
<!-- start type MPSImageTent --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTent -->
<!-- start type MPSImageThresholdBinary --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinary -->
<!-- start type MPSImageThresholdBinaryInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinaryInverse -->
<!-- start type MPSImageThresholdToZero --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZero -->
<!-- start type MPSImageThresholdToZeroInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZeroInverse -->
<!-- start type MPSImageThresholdTruncate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdTruncate -->
<!-- start type MPSImageTranspose --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTranspose</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTranspose -->
<!-- start type MPSKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSKernel -->
<!-- start type MPSMatrixMultiplication --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSMatrixMultiplication -->
<!-- start type MPSUnaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSUnaryImageKernel -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
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

</div> <!-- end type MDLMaterialProperty -->
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
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.2"</span> <span class='added '>"11.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.12.0"</span> <span class='added '>"11.0.0"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string DeviceCheckLibrary = "/System/Library/Frameworks/DeviceCheck.framework/DeviceCheck";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string IOSurfaceLibrary = "/System/Library/Frameworks/IOSurface.framework/IOSurface";</span>
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

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace OpenGLES --> <div> 
<h2>Namespace OpenGLES</h2>
<!-- start type EAGLContext --> <div>
<h3>Type Changed: OpenGLES.EAGLContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool TexImage (IOSurface.IOSurface ioSurface, uint target, uint internalFormat, uint width, uint height, uint format, uint type, uint plane);</span>
</pre>
</div>

</div> <!-- end type EAGLContext -->

</div> <!-- end namespace OpenGLES -->
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
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAsset --> <div>
<h3>Type Changed: Photos.PHAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHAsset -->
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
<p>Added property:</p>
<pre>
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

</div> <!-- end namespace Photos -->
<!-- start namespace ReplayKit --> <div> 
<h2>Namespace ReplayKit</h2>
<!-- start type NSExtensionContext_RPBroadcastExtension --> <div>
<h3>Type Changed: ReplayKit.NSExtensionContext_RPBroadcastExtension</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void CompleteRequest (Foundation.NSExtensionContext This, Foundation.NSUrl broadcastURL, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.INSCoding&gt; setupInfo);</span>
</pre>
</div>

</div> <!-- end type NSExtensionContext_RPBroadcastExtension -->
<!-- start type RPBroadcastControllerDelegate --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastControllerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateBroadcastUrl (RPBroadcastController broadcastController, Foundation.NSUrl broadcastUrl);</span>
</pre>
</div>

</div> <!-- end type RPBroadcastControllerDelegate -->
<!-- start type RPBroadcastControllerDelegate_Extensions --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastControllerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateBroadcastUrl (IRPBroadcastControllerDelegate This, RPBroadcastController broadcastController, Foundation.NSUrl broadcastUrl);</span>
</pre>
</div>

</div> <!-- end type RPBroadcastControllerDelegate_Extensions -->
<!-- start type RPRecordingError --> <div>
<h3>Type Changed: ReplayKit.RPRecordingError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ActivePhoneCall = -5811,</span>
	<span class='added added-field ' data-is-non-breaking="">CarPlay = -5813,</span>
	<span class='added added-field ' data-is-non-breaking="">Entitlements = -5810,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedToSave = -5812,</span>
</pre>
</div>

</div> <!-- end type RPRecordingError -->
<!-- start type RPScreenRecorder --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCapture (System.Action&lt;CoreMedia.CMSampleBuffer,ReplayKit.RPSampleBufferType,Foundation.NSError&gt; captureHandler, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StartCaptureAsync (System.Action&lt;CoreMedia.CMSampleBuffer,ReplayKit.RPSampleBufferType,Foundation.NSError&gt; captureHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopCapture (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StopCaptureAsync ();</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorder -->
<!-- start type RPScreenRecorderDelegate --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorderDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStopRecording (RPScreenRecorder screenRecorder, RPPreviewViewController previewViewController, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorderDelegate -->
<!-- start type RPScreenRecorderDelegate_Extensions --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorderDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStopRecording (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder, RPPreviewViewController previewViewController, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorderDelegate_Extensions -->

</div> <!-- end namespace ReplayKit -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
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

</div> <!-- end type SCNMaterial -->
<!-- start type SCNNode --> <div>
<h3>Type Changed: SceneKit.SCNNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanBecomeFocused { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.IUIFocusEnvironment[] PreferredFocusEnvironments { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIView PreferredFocusedView { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFocus (UIKit.UIFocusUpdateContext context, UIKit.UIFocusAnimationCoordinator coordinator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIKit.UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeedsFocusUpdate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldUpdateFocus (UIKit.UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateFocusIfNeeded ();</span>
</pre>
</div>

</div> <!-- end type SCNNode -->
<!-- start type SCNReferenceNode --> <div>
<h3>Type Changed: SceneKit.SCNReferenceNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SCNReferenceNode -->
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
<!-- start type SCNSceneSourceLoading --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceLoading</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ConvertToYUpKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ConvertUnitsToMetersKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneSourceLoading -->
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
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SCNAnimationPlayer FromAnimation (SCNAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString[] GetAnimationKeys ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAnimationPaused (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PauseAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Play ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllAnimations ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimation (Foundation.NSString key, nfloat duration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeAnimation (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopWithBlendOutDuration (double seconds);</span>
}
</pre>
</div> <!-- end type SCNAnimationPlayer -->
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
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILineBreakMode LineBreakMode { get; set; }</span>
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
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKNodeFocusBehavior FocusBehavior { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIKit.UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
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
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->
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
public class SKTransformNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem {
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
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StorefrontCountryCodeDidChangeNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestStorefrontCountryCode (System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestStorefrontCountryCodeAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestUserToken (string developerToken, System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestUserTokenAsync (string developerToken);</span>
</pre>
</div>
<!-- start type SKCloudServiceController.Notifications --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceController.Notifications -->

</div> <!-- end type SKCloudServiceController -->
<!-- start type SKPaymentTransactionObserver --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAddStorePayment (SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver -->
<!-- start type SKPaymentTransactionObserver_Extensions --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAddStorePayment (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver_Extensions -->
<!-- start type SKStoreProductParameterKey --> <div>
<h3>Type Changed: StoreKit.SKStoreProductParameterKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProductIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type SKStoreProductParameterKey -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifier -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKCloudServiceSetupMessageIdentifier {
	<span class='added added-field ' data-is-non-breaking="">AddMusic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connect = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Join = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PlayMusic = 3,</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifier -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifierExtensions -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKCloudServiceSetupMessageIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SKCloudServiceSetupMessageIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKCloudServiceSetupMessageIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifierExtensions -->
<div> <!-- start type SKProductStorePromotionController -->
<h3>New Type StoreKit.SKProductStorePromotionController</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductStorePromotionController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SKProductStorePromotionController Default { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionOrder (System.Action&lt;SKProduct[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProduct[]&gt; FetchStorePromotionOrderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionVisibility (SKProduct product, System.Action&lt;SKProductStorePromotionVisibility,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProductStorePromotionVisibility&gt; FetchStorePromotionVisibilityAsync (SKProduct product);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProduct[] storePromotionOrder, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProductStorePromotionVisibility promotionVisibility, SKProduct product, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProduct[] storePromotionOrder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProductStorePromotionVisibility promotionVisibility, SKProduct product);</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionController -->
<div> <!-- start type SKProductStorePromotionVisibility -->
<h3>New Type StoreKit.SKProductStorePromotionVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductStorePromotionVisibility {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hide = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Show = 1,</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionVisibility -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace TVMLKit --> <div> 
<h2>Namespace TVMLKit</h2>
<!-- start type TVElementAlignment --> <div>
<h3>Type Changed: TVMLKit.TVElementAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type TVElementAlignment -->
<!-- start type TVElementPosition --> <div>
<h3>Type Changed: TVMLKit.TVElementPosition</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BottomLeading = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomTrailing = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Leading = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeading = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">TopTrailing = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 13,</span>
</pre>
</div>

</div> <!-- end type TVElementPosition -->

</div> <!-- end namespace TVMLKit -->
<!-- start namespace TVServices --> <div> 
<h2>Namespace TVServices</h2>
<!-- start type TVContentItem --> <div>
<h3>Type Changed: TVServices.TVContentItem</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetImageUrl (TVContentItemImageTrait traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetImageUrl (Foundation.NSUrl aUrl, TVContentItemImageTrait traits);</span>
</pre>
</div>

</div> <!-- end type TVContentItem -->
<div> <!-- start type TVContentItemImageTrait -->
<h3>New Type TVServices.TVContentItemImageTrait</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum TVContentItemImageTrait {
	<span class='added added-field ' data-is-non-breaking="">ScreenScale1x = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">ScreenScale2x = 8192,</span>
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleDark = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleLight = 256,</span>
}
</pre>
</div> <!-- end type TVContentItemImageTrait -->

</div> <!-- end namespace TVServices -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSCoder_UIGeometryKeyedCoding --> <div>
<h3>Type Changed: UIKit.NSCoder_UIGeometryKeyedCoding</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSDirectionalEdgeInsets DecodeDirectionalEdgeInsets (Foundation.NSCoder This, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Encode (Foundation.NSCoder This, NSDirectionalEdgeInsets directionalEdgeInsets, string forKey);</span>
</pre>
</div>

</div> <!-- end type NSCoder_UIGeometryKeyedCoding -->
<!-- start type NSLayoutFormatOptions --> <div>
<h3>Type Changed: UIKit.NSLayoutFormatOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SpacingBaselineToBaseline = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingEdgeToEdge = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingMask = 524288,</span>
</pre>
</div>

</div> <!-- end type NSLayoutFormatOptions -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: UIKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintEqualToSystemSpacingAfterAnchor (NSLayoutXAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToSystemSpacingAfterAnchor (NSLayoutXAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintLessThanOrEqualToSystemSpacingAfterAnchor (NSLayoutXAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension CreateAnchorWithOffset (NSLayoutXAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: UIKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintEqualToSystemSpacingBelowAnchor (NSLayoutYAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintGreaterThanOrEqualToSystemSpacingBelowAnchor (NSLayoutYAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint ConstraintLessThanOrEqualToSystemSpacingBelowAnchor (NSLayoutYAxisAnchor anchor, nfloat multiplier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutDimension CreateAnchorWithOffset (NSLayoutYAxisAnchor otherAnchor);</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSTextAttachment --> <div>
<h3>Type Changed: UIKit.NSTextAttachment</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIAccessibilityContentSizeCategoryImageAdjusting</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsImageSizeForAccessibilityContentSizeCategory { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTextAttachment -->
<!-- start type UIAccessibilityContainer_Extensions --> <div>
<h3>Type Changed: UIKit.UIAccessibilityContainer_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIAccessibilityContainerType GetAccessibilityContainerType (IUIAccessibilityContainer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityContainerType (IUIAccessibilityContainer This, UIAccessibilityContainerType value);</span>
</pre>
</div>

</div> <!-- end type UIAccessibilityContainer_Extensions -->
<!-- start type UIAccessibilityCustomAction --> <div>
<h3>Type Changed: UIKit.UIAccessibilityCustomAction</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomAction (Foundation.NSAttributedString attributedName, Foundation.NSObject target, ObjCRuntime.Selector selector);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedName { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIAccessibilityCustomAction -->
<!-- start type UIAccessibilityCustomRotor --> <div>
<h3>Type Changed: UIKit.UIAccessibilityCustomRotor</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotor (Foundation.NSAttributedString attributedName, UIAccessibilityCustomRotorSearch itemSearchBlock);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotor (UIAccessibilityCustomSystemRotorType type, UIAccessibilityCustomRotorSearch itemSearchBlock);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIAccessibilityCustomSystemRotorType SystemRotorType { get; }</span>
</pre>
</div>

</div> <!-- end type UIAccessibilityCustomRotor -->
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static double BackgroundFetchIntervalMinimum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double BackgroundFetchIntervalNever { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIBackgroundRefreshStatus BackgroundRefreshStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BackgroundRefreshStatusDidChangeNotification { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetMinimumBackgroundFetchInterval (double minimumBackgroundFetchInterval);</span>
</pre>
</div>
<!-- start type UIApplication.Notifications --> <div>
<h3>Type Changed: UIKit.UIApplication.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIApplication.Notifications -->

</div> <!-- end type UIApplication -->
<!-- start type UIApplicationDelegate --> <div>
<h3>Type Changed: UIKit.UIApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformFetch (UIApplication application, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type UIApplicationDelegate -->
<!-- start type UIApplicationDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void PerformFetch (IUIApplicationDelegate This, UIApplication application, System.Action&lt;UIBackgroundFetchResult&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type UIApplicationDelegate_Extensions -->
<!-- start type UIBarItem --> <div>
<h3>Type Changed: UIKit.UIBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedHint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIImage LargeContentSizeImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets LargeContentSizeImageInsets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeIpaNotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeQueueAnnouncement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeCustom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeHeadingLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VoiceOverStatusDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type UIBarItem.Notifications --> <div>
<h3>Type Changed: UIKit.UIBarItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIBarItem.Notifications -->

</div> <!-- end type UIBarItem -->
<!-- start type UIBezierPath --> <div>
<h3>Type Changed: UIKit.UIBezierPath</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type UIBezierPath -->
<!-- start type UIButton --> <div>
<h3>Type Changed: UIKit.UIButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIAccessibilityContentSizeCategoryImageAdjusting</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsImageSizeForAccessibilityContentSizeCategory { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIButton -->
<!-- start type UIButtonType --> <div>
<h3>Type Changed: UIKit.UIButtonType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Plain = 6,</span>
</pre>
</div>

</div> <!-- end type UIButtonType -->
<!-- start type UICollectionView --> <div>
<h3>Type Changed: UIKit.UICollectionView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UICollectionView -->
<!-- start type UICollectionViewFlowLayout --> <div>
<h3>Type Changed: UIKit.UICollectionViewFlowLayout</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICollectionViewFlowLayoutSectionInsetReference SectionInsetReference { get; set; }</span>
</pre>
</div>

</div> <!-- end type UICollectionViewFlowLayout -->
<!-- start type UICollectionViewFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UICollectionViewFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UICollectionViewFocusUpdateContext ();</span>
</div></pre>

</div> <!-- end type UICollectionViewFocusUpdateContext -->
<!-- start type UICollectionViewLayout --> <div>
<h3>Type Changed: UIKit.UICollectionViewLayout</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIUserInterfaceLayoutDirection DevelopmentLayoutDirection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipsHorizontallyInOppositeLayoutDirection { get; }</span>
</pre>
</div>

</div> <!-- end type UICollectionViewLayout -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name, Foundation.NSBundle inBundle, UITraitCollection compatibleWithTraitCollection);</span>
</pre>
</div>

</div> <!-- end type UIColor -->
<!-- start type UIControl --> <div>
<h3>Type Changed: UIKit.UIControl</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIControlContentHorizontalAlignment EffectiveContentHorizontalAlignment { get; }</span>
</pre>
</div>

</div> <!-- end type UIControl -->
<!-- start type UIControlContentHorizontalAlignment --> <div>
<h3>Type Changed: UIKit.UIControlContentHorizontalAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type UIControlContentHorizontalAlignment -->
<!-- start type UIFocusAnimationCoordinator --> <div>
<h3>Type Changed: UIKit.UIFocusAnimationCoordinator</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedFocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedFocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedUnfocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedUnfocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
</pre>
</div>

</div> <!-- end type UIFocusAnimationCoordinator -->
<!-- start type UIFocusEnvironment_Extensions --> <div>
<h3>Type Changed: UIKit.UIFocusEnvironment_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetSoundIdentifier (IUIFocusEnvironment This, UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type UIFocusEnvironment_Extensions -->
<!-- start type UIFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UIFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UIFocusUpdateContext ();</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnimationCoordinatorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUpdateNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Key { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovementDidFailNotification { get; }</span>
</pre>
</div>

</div> <!-- end type UIFocusUpdateContext -->
<!-- start type UIFontTextStyle --> <div>
<h3>Type Changed: UIKit.UIFontTextStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LargeTitle = 10,</span>
</pre>
</div>

</div> <!-- end type UIFontTextStyle -->
<!-- start type UIGestureRecognizer --> <div>
<h3>Type Changed: UIKit.UIGestureRecognizer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIGestureRecognizer -->
<!-- start type UIGraphicsImageRendererFormat --> <div>
<h3>Type Changed: UIKit.UIGraphicsImageRendererFormat</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIGraphicsImageRendererFormat GetFormat (UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIGraphicsImageRendererFormat -->
<!-- start type UIGraphicsRendererFormat --> <div>
<h3>Type Changed: UIKit.UIGraphicsRendererFormat</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static UIGraphicsRendererFormat PreferredFormat { get; }</span>
</pre>
</div>

</div> <!-- end type UIGraphicsRendererFormat -->
<!-- start type UIImage --> <div>
<h3>Type Changed: UIKit.UIImage</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedHint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeIpaNotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeQueueAnnouncement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeCustom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeHeadingLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VoiceOverStatusDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type UIImage.Notifications --> <div>
<h3>Type Changed: UIKit.UIImage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIImage.Notifications -->

</div> <!-- end type UIImage -->
<!-- start type UIImageView --> <div>
<h3>Type Changed: UIKit.UIImageView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIAccessibilityContentSizeCategoryImageAdjusting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsImageSizeForAccessibilityContentSizeCategory { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MasksFocusEffectToContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView OverlayContentView { get; }</span>
</pre>
</div>

</div> <!-- end type UIImageView -->
<!-- start type UIInputViewController --> <div>
<h3>Type Changed: UIKit.UIInputViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasFullAccess { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NeedsInputModeSwitchKey { get; }</span>
</pre>
</div>

</div> <!-- end type UIInputViewController -->
<!-- start type UIModalPresentationStyle --> <div>
<h3>Type Changed: UIKit.UIModalPresentationStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BlurOverFullScreen = 8,</span>
</pre>
</div>

</div> <!-- end type UIModalPresentationStyle -->
<!-- start type UIPresentationController --> <div>
<h3>Type Changed: UIKit.UIPresentationController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type UIPresentationController -->
<!-- start type UIScreen --> <div>
<h3>Type Changed: UIKit.UIScreen</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Captured { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CapturedDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type UIScreen.Notifications --> <div>
<h3>Type Changed: UIKit.UIScreen.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCapturedDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCapturedDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIScreen.Notifications -->

</div> <!-- end type UIScreen -->
<!-- start type UIScrollView --> <div>
<h3>Type Changed: UIKit.UIScrollView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets AdjustedContentInset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIScrollViewContentInsetAdjustmentBehavior ContentInsetAdjustmentBehavior { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide ContentLayoutGuide { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide FrameLayoutGuide { get; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidChangeAdjustedContentInset;</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AdjustedContentInsetDidChange ();</span>
</pre>
</div>

</div> <!-- end type UIScrollView -->
<!-- start type UIScrollViewAccessibilityDelegate --> <div>
<h3>Type Changed: UIKit.UIScrollViewAccessibilityDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAccessibilityAttributedScrollStatus (UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewAccessibilityDelegate -->
<!-- start type UIScrollViewAccessibilityDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIScrollViewAccessibilityDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSAttributedString GetAccessibilityAttributedScrollStatus (IUIScrollViewAccessibilityDelegate This, UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewAccessibilityDelegate_Extensions -->
<!-- start type UIScrollViewDelegate --> <div>
<h3>Type Changed: UIKit.UIScrollViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeAdjustedContentInset (UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewDelegate -->
<!-- start type UIScrollViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIScrollViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeAdjustedContentInset (IUIScrollViewDelegate This, UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewDelegate_Extensions -->
<!-- start type UISearchBar --> <div>
<h3>Type Changed: UIKit.UISearchBar</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISearchBar -->
<!-- start type UISplitViewController --> <div>
<h3>Type Changed: UIKit.UISplitViewController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISplitViewControllerPrimaryEdge PrimaryEdge { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISplitViewController -->
<!-- start type UIStackView --> <div>
<h3>Type Changed: UIKit.UIStackView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetCustomSpacing (UIView arrangedSubview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCustomSpacing (nfloat spacing, UIView arrangedSubview);</span>
</pre>
</div>

</div> <!-- end type UIStackView -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InsetsContentViewsToSafeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITableViewSeparatorInsetReference SeparatorInsetReference { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformBatchUpdates (System.Action updates, System.Action&lt;bool&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PerformBatchUpdatesAsync (System.Action updates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UITableView -->
<!-- start type UITextContentType --> <div>
<h3>Type Changed: UIKit.UITextContentType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Password { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Username { get; }</span>
</pre>
</div>

</div> <!-- end type UITextContentType -->
<!-- start type UITextDocumentProxy --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid DocumentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SelectedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy -->
<!-- start type UITextDocumentProxy_Extensions --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUuid GetDocumentIdentifier (IUITextDocumentProxy This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetSelectedText (IUITextDocumentProxy This);</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy_Extensions -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextInputTraits_Extensions --> <div>
<h3>Type Changed: UIKit.UITextInputTraits_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartDashesType GetSmartDashesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartInsertDeleteType GetSmartInsertDeleteType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartQuotesType GetSmartQuotesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartDashesType (IUITextInputTraits This, UITextSmartDashesType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartInsertDeleteType (IUITextInputTraits This, UITextSmartInsertDeleteType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartQuotesType (IUITextInputTraits This, UITextSmartQuotesType value);</span>
</pre>
</div>

</div> <!-- end type UITextInputTraits_Extensions -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedHint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AccessibilityAttributedValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityIgnoresInvertColors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDirectionalEdgeInsets DirectionalLayoutMargins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InsetsLayoutMarginsFromSafeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets SafeAreaInsets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide SafeAreaLayoutGuide { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeIpaNotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SpeechAttributeQueueAnnouncement { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeCustom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAttributeHeadingLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VoiceOverStatusDidChangeNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SafeAreaInsetsDidChange ();</span>
</pre>
</div>
<!-- start type UIView.Notifications --> <div>
<h3>Type Changed: UIKit.UIView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIView.Notifications -->

</div> <!-- end type UIView -->
<!-- start type UIViewController --> <div>
<h3>Type Changed: UIKit.UIViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets AdditionalSafeAreaInsets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIViewController ChildViewControllerForUserInterfaceStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIUserInterfaceStyle PreferredUserInterfaceStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDirectionalEdgeInsets SystemMinimumLayoutMargins { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ViewRespectsSystemMinimumLayoutMargins { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeedsUserInterfaceAppearanceUpdate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ViewLayoutMarginsDidChange ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ViewSafeAreaInsetsDidChange ();</span>
</pre>
</div>

</div> <!-- end type UIViewController -->
<!-- start type UIViewPropertyAnimator --> <div>
<h3>Type Changed: UIKit.UIViewPropertyAnimator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PausesOnCompletion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ScrubsLinearly { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIViewPropertyAnimator -->
<div> <!-- start type IUIAccessibilityContainerDataTable -->
<h3>New Type UIKit.IUIAccessibilityContainerDataTable</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIAccessibilityContainerDataTable : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint AccessibilityColumnCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint AccessibilityRowCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIAccessibilityContainerDataTableCell GetAccessibilityDataTableCellElement (uint row, uint column);</span>
}
</pre>
</div> <!-- end type IUIAccessibilityContainerDataTable -->
<div> <!-- start type IUIAccessibilityContainerDataTableCell -->
<h3>New Type UIKit.IUIAccessibilityContainerDataTableCell</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIAccessibilityContainerDataTableCell : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityColumnRange ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRowRange ();</span>
}
</pre>
</div> <!-- end type IUIAccessibilityContainerDataTableCell -->
<div> <!-- start type IUIAccessibilityContentSizeCategoryImageAdjusting -->
<h3>New Type UIKit.IUIAccessibilityContentSizeCategoryImageAdjusting</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIAccessibilityContentSizeCategoryImageAdjusting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsImageSizeForAccessibilityContentSizeCategory { get; set; }</span>
}
</pre>
</div> <!-- end type IUIAccessibilityContentSizeCategoryImageAdjusting -->
<div> <!-- start type IUIDataSourceTranslating -->
<h3>New Type UIKit.IUIDataSourceTranslating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDataSourceTranslating : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
}
</pre>
</div> <!-- end type IUIDataSourceTranslating -->
<div> <!-- start type IUIFocusAnimationContext -->
<h3>New Type UIKit.IUIFocusAnimationContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusAnimationContext : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
}
</pre>
</div> <!-- end type IUIFocusAnimationContext -->
<div> <!-- start type IUIFocusDebuggerOutput -->
<h3>New Type UIKit.IUIFocusDebuggerOutput</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusDebuggerOutput : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUIFocusDebuggerOutput -->
<div> <!-- start type NSDirectionalEdgeInsets -->
<h3>New Type UIKit.NSDirectionalEdgeInsets</h3>
<pre class='added' data-is-non-breaking="">
public struct NSDirectionalEdgeInsets {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSDirectionalEdgeInsets (nfloat top, nfloat leading, nfloat bottom, nfloat trailing);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public nfloat Bottom;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Leading;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Top;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Trailing;</span>
	<span class='added added-field ' data-is-non-breaking="">public static NSDirectionalEdgeInsets Zero;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (NSDirectionalEdgeInsets other);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSDirectionalEdgeInsets FromString (string s);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NSDirectionalEdgeInsets insets1, NSDirectionalEdgeInsets insets2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NSDirectionalEdgeInsets insets1, NSDirectionalEdgeInsets insets2);</span>
}
</pre>
</div> <!-- end type NSDirectionalEdgeInsets -->
<div> <!-- start type UIAccessibilityContainerDataTable -->
<h3>New Type UIKit.UIAccessibilityContainerDataTable</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UIAccessibilityContainerDataTable : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIAccessibilityContainerDataTable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityContainerDataTable ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityContainerDataTable (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityContainerDataTable (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint AccessibilityColumnCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint AccessibilityRowCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIAccessibilityContainerDataTableCell GetAccessibilityDataTableCellElement (uint row, uint column);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIAccessibilityContainerDataTableCell[] GetAccessibilityHeaderElementsForColumn (uint column);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IUIAccessibilityContainerDataTableCell[] GetAccessibilityHeaderElementsForRow (uint row);</span>
}
</pre>
</div> <!-- end type UIAccessibilityContainerDataTable -->
<div> <!-- start type UIAccessibilityContainerDataTable_Extensions -->
<h3>New Type UIKit.UIAccessibilityContainerDataTable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIAccessibilityContainerDataTable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IUIAccessibilityContainerDataTableCell[] GetAccessibilityHeaderElementsForColumn (IUIAccessibilityContainerDataTable This, uint column);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IUIAccessibilityContainerDataTableCell[] GetAccessibilityHeaderElementsForRow (IUIAccessibilityContainerDataTable This, uint row);</span>
}
</pre>
</div> <!-- end type UIAccessibilityContainerDataTable_Extensions -->
<div> <!-- start type UIAccessibilityContainerType -->
<h3>New Type UIKit.UIAccessibilityContainerType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityContainerType {
	<span class='added added-field ' data-is-non-breaking="">DataTable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIAccessibilityContainerType -->
<div> <!-- start type UIAccessibilityCustomSystemRotorType -->
<h3>New Type UIKit.UIAccessibilityCustomSystemRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityCustomSystemRotorType {
	<span class='added added-field ' data-is-non-breaking="">BoldText = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 2,</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomSystemRotorType -->
<div> <!-- start type UIAccessibilityReadingContent_Extensions -->
<h3>New Type UIKit.UIAccessibilityReadingContent_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIAccessibilityReadingContent_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSAttributedString GetAccessibilityAttributedContent (IUIAccessibilityReadingContent This, nint lineNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSAttributedString GetAccessibilityAttributedPageContent (IUIAccessibilityReadingContent This);</span>
}
</pre>
</div> <!-- end type UIAccessibilityReadingContent_Extensions -->
<div> <!-- start type UIBackgroundRefreshStatus -->
<h3>New Type UIKit.UIBackgroundRefreshStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIBackgroundRefreshStatus {
	<span class='added added-field ' data-is-non-breaking="">Available = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 0,</span>
}
</pre>
</div> <!-- end type UIBackgroundRefreshStatus -->
<div> <!-- start type UICollectionViewFlowLayoutSectionInsetReference -->
<h3>New Type UIKit.UICollectionViewFlowLayoutSectionInsetReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UICollectionViewFlowLayoutSectionInsetReference {
	<span class='added added-field ' data-is-non-breaking="">ContentInset = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">LayoutMargins = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SafeArea = 1,</span>
}
</pre>
</div> <!-- end type UICollectionViewFlowLayoutSectionInsetReference -->
<div> <!-- start type UIFocusDebugger -->
<h3>New Type UIKit.UIFocusDebugger</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusDebugger : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIFocusDebugger ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Help { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput CheckFocusability (IUIFocusItem item);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput SimulateFocusUpdateRequest (IUIFocusEnvironment environment);</span>
}
</pre>
</div> <!-- end type UIFocusDebugger -->
<div> <!-- start type UIFocusSoundIdentifier -->
<h3>New Type UIKit.UIFocusSoundIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIFocusSoundIdentifier {
	<span class='added added-field ' data-is-non-breaking="">Default = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIFocusSoundIdentifier -->
<div> <!-- start type UIFocusSoundIdentifierExtensions -->
<h3>New Type UIKit.UIFocusSoundIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIFocusSoundIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (UIFocusSoundIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFocusSoundIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type UIFocusSoundIdentifierExtensions -->
<div> <!-- start type UIFocusSystem -->
<h3>New Type UIKit.UIFocusSystem</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusSystem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Contains (IUIFocusEnvironment environment, IUIFocusEnvironment otherEnvironment);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RegisterUrl (Foundation.NSUrl soundFileUrl, Foundation.NSString identifier);</span>
}
</pre>
</div> <!-- end type UIFocusSystem -->
<div> <!-- start type UIFontMetrics -->
<h3>New Type UIKit.UIFontMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class UIFontMetrics : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFontMetrics (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFontMetrics (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIFontMetrics (string textStyle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static UIFontMetrics DefaultMetrics { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIFontMetrics GetMetrics (string textStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font, nfloat maximumPointSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font, UITraitCollection traitCollection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font, nfloat maximumPointSize, UITraitCollection traitCollection);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetScaledValue (nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetScaledValue (nfloat value, UITraitCollection traitCollection);</span>
}
</pre>
</div> <!-- end type UIFontMetrics -->
<div> <!-- start type UINavigationItemLargeTitleDisplayMode -->
<h3>New Type UIKit.UINavigationItemLargeTitleDisplayMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UINavigationItemLargeTitleDisplayMode {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Never = 2,</span>
}
</pre>
</div> <!-- end type UINavigationItemLargeTitleDisplayMode -->
<div> <!-- start type UIScrollViewContentInsetAdjustmentBehavior -->
<h3>New Type UIKit.UIScrollViewContentInsetAdjustmentBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIScrollViewContentInsetAdjustmentBehavior {
	<span class='added added-field ' data-is-non-breaking="">Always = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Never = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScrollableAxes = 1,</span>
}
</pre>
</div> <!-- end type UIScrollViewContentInsetAdjustmentBehavior -->
<div> <!-- start type UISplitViewControllerPrimaryEdge -->
<h3>New Type UIKit.UISplitViewControllerPrimaryEdge</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UISplitViewControllerPrimaryEdge {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type UISplitViewControllerPrimaryEdge -->
<div> <!-- start type UITableViewSeparatorInsetReference -->
<h3>New Type UIKit.UITableViewSeparatorInsetReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITableViewSeparatorInsetReference {
	<span class='added added-field ' data-is-non-breaking="">AutomaticInsets = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CellEdges = 0,</span>
}
</pre>
</div> <!-- end type UITableViewSeparatorInsetReference -->
<div> <!-- start type UITextSmartDashesType -->
<h3>New Type UIKit.UITextSmartDashesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartDashesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartDashesType -->
<div> <!-- start type UITextSmartInsertDeleteType -->
<h3>New Type UIKit.UITextSmartInsertDeleteType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartInsertDeleteType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartInsertDeleteType -->
<div> <!-- start type UITextSmartQuotesType -->
<h3>New Type UIKit.UITextSmartQuotesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartQuotesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartQuotesType -->

</div> <!-- end namespace UIKit -->
<!-- start namespace VideoSubscriberAccount --> <div> 
<h2>Namespace VideoSubscriberAccount</h2>
<!-- start type VSAccountManagerDelegate --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountManagerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAuthenticateAccountProvider (VSAccountManager accountManager, string accountProviderIdentifier);</span>
</pre>
</div>

</div> <!-- end type VSAccountManagerDelegate -->
<!-- start type VSAccountMetadataRequest --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountMetadataRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] FeaturedAccountProviderIdentifiers { get; set; }</span>
</pre>
</div>

</div> <!-- end type VSAccountMetadataRequest -->
<div> <!-- start type VSAccountManagerDelegate_Extensions -->
<h3>New Type VideoSubscriberAccount.VSAccountManagerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VSAccountManagerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAuthenticateAccountProvider (IVSAccountManagerDelegate This, VSAccountManager accountManager, string accountProviderIdentifier);</span>
}
</pre>
</div> <!-- end type VSAccountManagerDelegate_Extensions -->
<div> <!-- start type VSSubscription -->
<h3>New Type VideoSubscriberAccount.VSSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class VSSubscription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSSubscription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VSSubscriptionAccessLevel AccessLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ExpirationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] TierIdentifiers { get; set; }</span>
}
</pre>
</div> <!-- end type VSSubscription -->
<div> <!-- start type VSSubscriptionAccessLevel -->
<h3>New Type VideoSubscriberAccount.VSSubscriptionAccessLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VSSubscriptionAccessLevel {
	<span class='added added-field ' data-is-non-breaking="">FreeWithAccount = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Paid = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type VSSubscriptionAccessLevel -->
<div> <!-- start type VSSubscriptionRegistrationCenter -->
<h3>New Type VideoSubscriberAccount.VSSubscriptionRegistrationCenter</h3>
<pre class='added' data-is-non-breaking="">
public class VSSubscriptionRegistrationCenter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscriptionRegistrationCenter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscriptionRegistrationCenter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static VSSubscriptionRegistrationCenter Default { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCurrentSubscription (VSSubscription currentSubscription);</span>
}
</pre>
</div> <!-- end type VSSubscriptionRegistrationCenter -->

</div> <!-- end namespace VideoSubscriberAccount -->
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

<!-- start namespace DeviceCheck --> <div> 
<h2>New Namespace DeviceCheck</h2>

<div> <!-- start type DCDevice -->
<h3>New Type DeviceCheck.DCDevice</h3>
<pre class='added' data-is-non-breaking="">
public class DCDevice : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DCDevice CurrentDevice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Supported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void GenerateToken (DCDeviceGenerateTokenCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; GenerateTokenAsync ();</span>
}
</pre>
</div> <!-- end type DCDevice -->
<div> <!-- start type DCDeviceGenerateTokenCompletionHandler -->
<h3>New Type DeviceCheck.DCDeviceGenerateTokenCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DCDeviceGenerateTokenCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DCDeviceGenerateTokenCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData token, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData token, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DCDeviceGenerateTokenCompletionHandler -->
<div> <!-- start type DCError -->
<h3>New Type DeviceCheck.DCError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DCError {
	<span class='added added-field ' data-is-non-breaking="">FeatureUnsupported = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownSystemFailure = 0,</span>
}
</pre>
</div> <!-- end type DCError -->
<div> <!-- start type DCErrorExtensions -->
<h3>New Type DeviceCheck.DCErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class DCErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (DCError self);</span>
}
</pre>
</div> <!-- end type DCErrorExtensions -->
</div> <!-- end namespace DeviceCheck -->

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
	<span class='added added-method ' data-is-non-breaking="">public int SetPurgeable (IOSurfacePurgeabilityState newState);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetPurgeable (IOSurfacePurgeabilityState newState, IOSurfacePurgeabilityState oldState);</span>
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

<!-- start namespace WebKit --> <div> 
<h2>New Namespace WebKit</h2>

<div> <!-- start type WKWebView -->
<h3>New Type WebKit.WKWebView</h3>
<pre class='added' data-is-non-breaking="">
public class WKWebView {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WKWebView ();</span>
}
</pre>
</div> <!-- end type WKWebView -->
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
</script><h1 id='diff/xi/Xamarin.TVOS/MonoTouch.Dialog-1.html'>MonoTouch.Dialog-1.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.Dialog --> <div> 
<h2>Namespace MonoTouch.Dialog</h2>
<!-- start type GlassButton --> <div>
<h3>Type Changed: MonoTouch.Dialog.GlassButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIAccessibilityContentSizeCategoryImageAdjusting</span>
</pre>
</div>

</div> <!-- end type GlassButton -->

</div> <!-- end namespace MonoTouch.Dialog -->
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
