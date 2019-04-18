---
id: E48878BD-17C7-4824-A185-D6D085CB21FC
title: "tvOS 11.2.0 to 11.3.0"
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
<!-- start type AVDepthData --> <div>
<h3>Type Changed: AVFoundation.AVDepthData</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVDepthDataQuality DepthDataQuality { get; }</span>
</pre>
</div>

</div> <!-- end type AVDepthData -->
<!-- start type AVMutableVideoComposition --> <div>
<h3>Type Changed: AVFoundation.AVMutableVideoComposition</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual int SourceTrackIdForFrameTiming { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVMutableVideoComposition -->
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
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
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
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">SceneKit.ISCNAnimationProtocol</span>
</pre>
</div>

</div> <!-- end type CATransition -->

</div> <!-- end namespace CoreAnimation -->
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
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
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
<!-- start type CVMetalTextureCache --> <div>
<h3>Type Changed: CoreVideo.CVMetalTextureCache</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CVMetalTextureCache (Metal.IMTLDevice metalDevice, CVMetalTextureAttributes textureAttributes);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CVMetalTextureCache FromDevice (Metal.IMTLDevice metalDevice, CVMetalTextureAttributes textureAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVMetalTextureCache FromDevice (Metal.IMTLDevice metalDevice, CVMetalTextureAttributes textureAttributes, CVReturn creationErr);</span>
</pre>
</div>

</div> <!-- end type CVMetalTextureCache -->
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
<!-- start namespace GameplayKit --> <div> 
<h2>Namespace GameplayKit</h2>
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
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfo --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDate CurrentPlaybackDate { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfo -->

</div> <!-- end namespace MediaPlayer -->
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

</div> <!-- end namespace ModelIO -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"11.0"</span> <span class='added '>"11.1"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.2.0"</span> <span class='added '>"11.3.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace ReplayKit --> <div> 
<h2>Namespace ReplayKit</h2>
<!-- start type RPBroadcastSampleHandler --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastSampleHandler</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VideoSampleOrientationKey { get; }</span>
</pre>
</div>

</div> <!-- end type RPBroadcastSampleHandler -->

</div> <!-- end namespace ReplayKit -->
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
<!-- start type SCNAnimationPlayer --> <div>
<h3>Type Changed: SceneKit.SCNAnimationPlayer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNAnimationPlayer -->
<!-- start type SCNCamera --> <div>
<h3>Type Changed: SceneKit.SCNCamera</h3>
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
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimation (SCNAnimationPlayer player, Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SCNAnimationPlayer GetAnimationPlayer (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAnimationUsingBlendOutDuration (Foundation.NSString key, nfloat blendOutDuration);</span>
</pre>
</div>

</div> <!-- end type SCNConstraint -->
<!-- start type SCNGeometry --> <div>
<h3>Type Changed: SceneKit.SCNGeometry</h3>
<div>
<p>Added property:</p>
<pre>
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
<!-- start type SCNMaterial --> <div>
<h3>Type Changed: SceneKit.SCNMaterial</h3>
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
<!-- start type SCNScene --> <div>
<h3>Type Changed: SceneKit.SCNScene</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">GameplayKit.IGKSceneRootNodeType</span>
</pre>
</div>

</div> <!-- end type SCNScene -->
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
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RendersContinuously { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNView -->
<div> <!-- start type ISCNAvoidOccluderConstraintDelegate -->
<h3>New Type SceneKit.ISCNAvoidOccluderConstraintDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNAvoidOccluderConstraintDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISCNAvoidOccluderConstraintDelegate -->
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

</div> <!-- end namespace SceneKit -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKScene --> <div>
<h3>Type Changed: SpriteKit.SKScene</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">GameplayKit.IGKSceneRootNodeType</span>
</pre>
</div>

</div> <!-- end type SKScene -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIContentSizeCategoryExtensions --> <div>
<h3>Type Changed: UIKit.UIContentSizeCategoryExtensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSComparisonResult Compare (UIContentSizeCategory category1, UIContentSizeCategory category2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsAccessibilityCategory (UIContentSizeCategory self);</span>
</pre>
</div>

</div> <!-- end type UIContentSizeCategoryExtensions -->
<!-- start type UIInputViewController --> <div>
<h3>Type Changed: UIKit.UIInputViewController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasDictationKey { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIInputViewController -->

</div> <!-- end namespace UIKit -->
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
</div>



   


 <hr>
