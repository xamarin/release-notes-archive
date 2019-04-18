---
id: 15041C6B-54FA-4CD3-87BA-F43C1E964B43
title: "Mac 2.10 to 3.0"
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
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime OverallDurationHint { get; }</span>
</pre>
</div>

</div> <!-- end type AVAsset -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAssetExportSession (AVAsset asset, AVAssetExportSessionPreset preset);</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
<!-- start type AVAudioChannelLayout --> <div>
<h3>Type Changed: AVFoundation.AVAudioChannelLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created")]
	public AVAudioChannelLayout ();</span>
</div></pre>

</div> <!-- end type AVAudioChannelLayout -->
<!-- start type AVAudioConnectionPoint --> <div>
<h3>Type Changed: AVFoundation.AVAudioConnectionPoint</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created")]
	public AVAudioConnectionPoint ();</span>
</div></pre>

</div> <!-- end type AVAudioConnectionPoint -->
<!-- start type AVAudioConverterPrimeInfo --> <div>
<h3>Type Changed: AVFoundation.AVAudioConverterPrimeInfo</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioConverterPrimeInfo (uint leadingFrames, uint trailingFrames);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVAudioConverterPrimeInfo other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVAudioConverterPrimeInfo left, AVAudioConverterPrimeInfo right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVAudioConverterPrimeInfo left, AVAudioConverterPrimeInfo right);</span>
</pre>
</div>

</div> <!-- end type AVAudioConverterPrimeInfo -->
<!-- start type AVAudioFormat --> <div>
<h3>Type Changed: AVFoundation.AVAudioFormat</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData MagicCookie { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVAudioFormat -->
<!-- start type AVAudioPlayer --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioFormat Format { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetVolume (float volume, double duration);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayer -->
<!-- start type AVAudioRecorder --> <div>
<h3>Type Changed: AVFoundation.AVAudioRecorder</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVAudioRecorder Create (Foundation.NSUrl url, AVAudioFormat format, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type AVAudioRecorder -->
<!-- start type AVAudioSessionCategoryOptions --> <div>
<h3>Type Changed: AVFoundation.AVAudioSessionCategoryOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AllowAirPlay = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowBluetoothA2DP = 32,</span>
</pre>
</div>

</div> <!-- end type AVAudioSessionCategoryOptions -->
<!-- start type AVAudioSettings --> <div>
<h3>Type Changed: AVFoundation.AVAudioSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AVSampleRateConverterAlgorithm_MinimumPhase { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioSettings -->
<!-- start type AVBeatRange --> <div>
<h3>Type Changed: AVFoundation.AVBeatRange</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVBeatRange other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVBeatRange left, AVBeatRange right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVBeatRange left, AVBeatRange right);</span>
</pre>
</div>

</div> <!-- end type AVBeatRange -->
<!-- start type AVCaptureConnection --> <div>
<h3>Type Changed: AVFoundation.AVCaptureConnection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureConnection FromInputPort (AVCaptureInputPort port, AVCaptureVideoPreviewLayer layer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureConnection FromInputPorts (AVCaptureInputPort[] ports, AVCaptureOutput output);</span>
</pre>
</div>

</div> <!-- end type AVCaptureConnection -->
<!-- start type AVCaptureDevice --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetDefaultDevice(AVMediaTypes)")]
	public static AVCaptureDevice DefaultDeviceWithMediaType (string mediaType);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureDevice GetDefaultDevice (AVMediaTypes mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVCaptureDevice GetDefaultDevice (Foundation.NSString mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool HasMediaType (AVMediaTypes mediaType);</span>
</pre>
</div>

</div> <!-- end type AVCaptureDevice -->
<!-- start type AVCaptureWhiteBalanceChromaticityValues --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceChromaticityValues</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceChromaticityValues other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceChromaticityValues left, AVCaptureWhiteBalanceChromaticityValues right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceChromaticityValues left, AVCaptureWhiteBalanceChromaticityValues right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceChromaticityValues -->
<!-- start type AVCaptureWhiteBalanceGains --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceGains</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceGains other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceGains left, AVCaptureWhiteBalanceGains right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceGains left, AVCaptureWhiteBalanceGains right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceGains -->
<!-- start type AVCaptureWhiteBalanceTemperatureAndTintValues --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceTemperatureAndTintValues other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceTemperatureAndTintValues left, AVCaptureWhiteBalanceTemperatureAndTintValues right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceTemperatureAndTintValues left, AVCaptureWhiteBalanceTemperatureAndTintValues right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceTemperatureAndTintValues -->
<!-- start type AVError --> <div>
<h3>Type Changed: AVFoundation.AVError</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	ApplicationIsNotAuthorizedToUseDevice = <span class='removed removed-inline removed-breaking-inline'>11852</span> <span class='added '>-11852</span>
</div><div data-is-breaking="">	MaximumStillImageCaptureRequestsExceeded = <span class='removed removed-inline removed-breaking-inline'>11830</span> <span class='added '>-11830</span>
</div></pre>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">OperationNotAllowed = -11862,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedOutputSettings = -11861,</span>
</pre>
</div>

</div> <!-- end type AVError -->
<!-- start type AVMediaCharacteristic --> <div>
<h3>Type Changed: AVFoundation.AVMediaCharacteristic</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UsesWideGamutColorSpace { get; }</span>
</pre>
</div>

</div> <!-- end type AVMediaCharacteristic -->
<!-- start type AVMetadata --> <div>
<h3>Type Changed: AVFoundation.AVMetadata</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ID3MetadataKeyInvolvedPeopleList_v24 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsoUserDataKeyDate { get; }</span>
</pre>
</div>

</div> <!-- end type AVMetadata -->
<!-- start type AVMetadataIdentifiers --> <div>
<h3>Type Changed: AVFoundation.AVMetadataIdentifiers</h3>
<!-- start type AVMetadataIdentifiers.Iso --> <div>
<h3>Type Changed: AVFoundation.AVMetadataIdentifiers.Iso</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserDataDate { get; }</span>
</pre>
</div>

</div> <!-- end type AVMetadataIdentifiers.Iso -->

</div> <!-- end type AVMetadataIdentifiers -->
<!-- start type AVMutableVideoComposition --> <div>
<h3>Type Changed: AVFoundation.AVMutableVideoComposition</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorPrimaries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorTransferFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorYCbCrMatrix { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVMutableVideoComposition -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyWaitsToMinimizeStalling { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ReasonForWaitingToPlay { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVPlayerTimeControlStatus TimeControlStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WaitingToMinimizeStallsReason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WaitingWhileEvaluatingBufferingRateReason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WaitingWithNoItemToPlayReason { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PlayImmediatelyAtRate (float rate);</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->
<!-- start type AVPlayerItem --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double PreferredForwardBufferDuration { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItem -->
<!-- start type AVPlayerItemAccessLogEvent --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemAccessLogEvent</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double AverageAudioBitrate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double AverageVideoBitrate { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemAccessLogEvent -->
<!-- start type AVPlayerItemVideoOutput --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemVideoOutput</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVPlayerItemVideoOutput (AVPlayerItemVideoOutputSettings settings);</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemVideoOutput -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FailedToDecodeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FailedToDecodeNotificationErrorKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVUrlAsset --> <div>
<h3>Type Changed: AVFoundation.AVUrlAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAssetCache Cache { get; }</span>
</pre>
</div>

</div> <!-- end type AVUrlAsset -->
<!-- start type AVVideo --> <div>
<h3>Type Changed: AVFoundation.AVVideo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AppleProRes422 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AppleProRes4444 { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideo -->
<!-- start type AVVideoCompositing --> <div>
<h3>Type Changed: AVFoundation.AVVideoCompositing</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsWideColorSourceFrames { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoCompositing -->
<!-- start type AVVideoCompositing_Extensions --> <div>
<h3>Type Changed: AVFoundation.AVVideoCompositing_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetSupportsWideColorSourceFrames (IAVVideoCompositing This);</span>
</pre>
</div>

</div> <!-- end type AVVideoCompositing_Extensions -->
<!-- start type AVVideoComposition --> <div>
<h3>Type Changed: AVFoundation.AVVideoComposition</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorPrimaries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorTransferFunction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ColorYCbCrMatrix { get; }</span>
</pre>
</div>

</div> <!-- end type AVVideoComposition -->
<div> <!-- start type AVAssetCache -->
<h3>New Type AVFoundation.AVAssetCache</h3>
<pre class='added' data-is-non-breaking="">
public class AVAssetCache : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAssetCache (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAssetCache (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPlayableOffline { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AVMediaSelectionOption[] GetMediaSelectionOptions (AVMediaSelectionGroup mediaSelectionGroup);</span>
}
</pre>
</div> <!-- end type AVAssetCache -->
<div> <!-- start type AVAssetExportSessionPreset -->
<h3>New Type AVFoundation.AVAssetExportSessionPreset</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAssetExportSessionPreset {
	<span class='added added-field ' data-is-non-breaking="">AppleM4A = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HighestQuality = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LowQuality = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumQuality = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Passthrough = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset1280x720 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset1920x1080 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset3840x2160 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset640x480 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Preset960x540 = 4,</span>
}
</pre>
</div> <!-- end type AVAssetExportSessionPreset -->
<div> <!-- start type AVAssetExportSessionPresetExtensions -->
<h3>New Type AVFoundation.AVAssetExportSessionPresetExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAssetExportSessionPresetExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVAssetExportSessionPreset self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVAssetExportSessionPreset GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVAssetExportSessionPresetExtensions -->
<div> <!-- start type AVCleanApertureProperties -->
<h3>New Type AVFoundation.AVCleanApertureProperties</h3>
<pre class='added' data-is-non-breaking="">
public class AVCleanApertureProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVCleanApertureProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVCleanApertureProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber HorizontalOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber VerticalOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Width { get; set; }</span>
}
</pre>
</div> <!-- end type AVCleanApertureProperties -->
<div> <!-- start type AVColorProperties -->
<h3>New Type AVFoundation.AVColorProperties</h3>
<pre class='added' data-is-non-breaking="">
public class AVColorProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVColorProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVColorProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString AVVideoColorPrimaries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString AVVideoTransferFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString AVVideoYCbCrMatrix { get; }</span>
}
</pre>
</div> <!-- end type AVColorProperties -->
<div> <!-- start type AVCompressionProperties -->
<h3>New Type AVFoundation.AVCompressionProperties</h3>
<pre class='added' data-is-non-breaking="">
public class AVCompressionProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVCompressionProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVCompressionProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AVCleanApertureProperties CleanAperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVPixelAspectRatioProperties PixelAspectRatio { get; set; }</span>
}
</pre>
</div> <!-- end type AVCompressionProperties -->
<div> <!-- start type AVMediaTypes -->
<h3>New Type AVFoundation.AVMediaTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMediaTypes {
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ClosedCaption = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Metadata = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">MetadataObject = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Muxed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Subtitle = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Timecode = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedMetadata = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 0,</span>
}
</pre>
</div> <!-- end type AVMediaTypes -->
<div> <!-- start type AVMediaTypesExtensions -->
<h3>New Type AVFoundation.AVMediaTypesExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVMediaTypesExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVMediaTypes self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVMediaTypes GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVMediaTypesExtensions -->
<div> <!-- start type AVMusicTrackLoopCount -->
<h3>New Type AVFoundation.AVMusicTrackLoopCount</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMusicTrackLoopCount {
	<span class='added added-field ' data-is-non-breaking="">Forever = -1,</span>
}
</pre>
</div> <!-- end type AVMusicTrackLoopCount -->
<div> <!-- start type AVPixelAspectRatioProperties -->
<h3>New Type AVFoundation.AVPixelAspectRatioProperties</h3>
<pre class='added' data-is-non-breaking="">
public class AVPixelAspectRatioProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVPixelAspectRatioProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVPixelAspectRatioProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber PixelAspectRatioHorizontalSpacing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber PixelAspectRatioVerticalSpacing { get; set; }</span>
}
</pre>
</div> <!-- end type AVPixelAspectRatioProperties -->
<div> <!-- start type AVPlayerItemVideoOutputSettings -->
<h3>New Type AVFoundation.AVPlayerItemVideoOutputSettings</h3>
<pre class='added' data-is-non-breaking="">
public class AVPlayerItemVideoOutputSettings : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVPlayerItemVideoOutputSettings ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVPlayerItemVideoOutputSettings (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString Codec { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVColorProperties ColorProperties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVCompressionProperties CompressionProperties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString ScalingMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Width { get; set; }</span>
}
</pre>
</div> <!-- end type AVPlayerItemVideoOutputSettings -->
<div> <!-- start type AVPlayerLooper -->
<h3>New Type AVFoundation.AVPlayerLooper</h3>
<pre class='added' data-is-non-breaking="">
public class AVPlayerLooper : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPlayerLooper (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPlayerLooper (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVPlayerLooper (AVQueuePlayer player, AVPlayerItem itemToLoop, CoreMedia.CMTimeRange loopRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint LoopCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LoopingEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVPlayerItem[] LoopingPlayerItems { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVPlayerLooperStatus Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisableLooping ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVPlayerLooper FromPlayer (AVQueuePlayer player, AVPlayerItem itemToLoop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVPlayerLooper FromPlayer (AVQueuePlayer player, AVPlayerItem itemToLoop, CoreMedia.CMTimeRange loopRange);</span>
}
</pre>
</div> <!-- end type AVPlayerLooper -->
<div> <!-- start type AVPlayerLooperStatus -->
<h3>New Type AVFoundation.AVPlayerLooperStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVPlayerLooperStatus {
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type AVPlayerLooperStatus -->
<div> <!-- start type AVPlayerTimeControlStatus -->
<h3>New Type AVFoundation.AVPlayerTimeControlStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVPlayerTimeControlStatus {
	<span class='added added-field ' data-is-non-breaking="">Paused = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Playing = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WaitingToPlayAtSpecifiedRate = 1,</span>
}
</pre>
</div> <!-- end type AVPlayerTimeControlStatus -->
<div> <!-- start type AVVideoColorPrimaries -->
<h3>New Type AVFoundation.AVVideoColorPrimaries</h3>
<pre class='added' data-is-non-breaking="">
public static class AVVideoColorPrimaries {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Ebu_3213 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Itu_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Smpte_C { get; }</span>
}
</pre>
</div> <!-- end type AVVideoColorPrimaries -->
<div> <!-- start type AVVideoTransferFunction -->
<h3>New Type AVFoundation.AVVideoTransferFunction</h3>
<pre class='added' data-is-non-breaking="">
public static class AVVideoTransferFunction {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AVVideoTransferFunction_Itu_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AVVideoTransferFunction_Smpte_240M_1995 { get; }</span>
}
</pre>
</div> <!-- end type AVVideoTransferFunction -->
<div> <!-- start type AVVideoYCbCrMatrix -->
<h3>New Type AVFoundation.AVVideoYCbCrMatrix</h3>
<pre class='added' data-is-non-breaking="">
public static class AVVideoYCbCrMatrix {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Itu_R_601_4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Itu_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Smpte_240M_1995 { get; }</span>
}
</pre>
</div> <!-- end type AVVideoYCbCrMatrix -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerView --> <div>
<h3>Type Changed: AVKit.AVPlayerView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type AVPlayerView -->

</div> <!-- end namespace AVKit -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACErrorCode --> <div>
<h3>Type Changed: Accounts.ACErrorCode</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use MissingTransportMessageId")]
	MissingMessageID = 21,</span>
</div></pre>

</div> <!-- end type ACErrorCode -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AppKit --> <div> 
<h2>Namespace AppKit</h2>
<!-- start type NSAccessibilityAttributes --> <div>
<h3>Type Changed: AppKit.NSAccessibilityAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RequiredAttribute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextAlignmentAttribute { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityAttributes -->
<!-- start type NSAccessibilityElement --> <div>
<h3>Type Changed: AppKit.NSAccessibilityElement</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityElement -->
<!-- start type NSAccessibilityRoles --> <div>
<h3>Type Changed: AppKit.NSAccessibilityRoles</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MenuBarItemRole { get; }</span>
</pre>
</div>

</div> <!-- end type NSAccessibilityRoles -->
<!-- start type NSApplication --> <div>
<h3>Type Changed: AppKit.NSApplication</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;NSApplicationUserAcceptedCloudKitShareEventArgs&gt; UserDidAcceptCloudKitShare;</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateWindows (NSWindowListOptions options, NSApplicationEnumerateWindowsHandler block);</span>
</pre>
</div>

</div> <!-- end type NSApplication -->
<!-- start type NSApplicationDelegate --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UserDidAcceptCloudKitShare (NSApplication application, CloudKit.CKShareMetadata metadata);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate -->
<!-- start type NSApplicationDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSApplicationDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void UserDidAcceptCloudKitShare (INSApplicationDelegate This, NSApplication application, CloudKit.CKShareMetadata metadata);</span>
</pre>
</div>

</div> <!-- end type NSApplicationDelegate_Extensions -->
<!-- start type NSBox --> <div>
<h3>Type Changed: AppKit.NSBox</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSBox -->
<!-- start type NSBrowser --> <div>
<h3>Type Changed: AppKit.NSBrowser</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSBrowser -->
<!-- start type NSBrowserCell --> <div>
<h3>Type Changed: AppKit.NSBrowserCell</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSBrowserCell (NSImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSBrowserCell (string str);</span>
</pre>
</div>

</div> <!-- end type NSBrowserCell -->
<!-- start type NSButton --> <div>
<h3>Type Changed: AppKit.NSButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor BezelColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ImageHugsTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImageScale ImageScaling { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSButton CreateButton (NSImage image, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSButton CreateButton (string title, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSButton CreateButton (string title, NSImage image, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSButton CreateCheckbox (string title, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSButton CreateRadioButton (string title, System.Action action);</span>
</pre>
</div>

</div> <!-- end type NSButton -->
<!-- start type NSCell --> <div>
<h3>Type Changed: AppKit.NSCell</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSCell -->
<!-- start type NSCellImagePosition --> <div>
<h3>Type Changed: AppKit.NSCellImagePosition</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ImageLeading = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageTrailing = 8,</span>
</pre>
</div>

</div> <!-- end type NSCellImagePosition -->
<!-- start type NSClickGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSClickGestureRecognizer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfTouchesRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSClickGestureRecognizer -->
<!-- start type NSClipView --> <div>
<h3>Type Changed: AppKit.NSClipView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSClipView -->
<!-- start type NSCollectionView --> <div>
<h3>Type Changed: AppKit.NSCollectionView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool BackgroundViewScrollsWithContent { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleSectionCollapse (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSCollectionView -->
<!-- start type NSCollectionViewFlowLayout --> <div>
<h3>Type Changed: AppKit.NSCollectionViewFlowLayout</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SectionFootersPinToVisibleBounds { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SectionHeadersPinToVisibleBounds { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CollapseSectionAtIndex (uint sectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExpandSectionAtIndex (uint sectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SectionAtIndexIsCollapsed (uint sectionIndex);</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewFlowLayout -->
<!-- start type NSCollectionViewItem --> <div>
<h3>Type Changed: AppKit.NSCollectionViewItem</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSCollectionViewItem -->
<!-- start type NSColor --> <div>
<h3>Type Changed: AppKit.NSColor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColor ScrubberTexturedBackgroundColor { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromColor (NSColorSpace space, nfloat hue, nfloat saturation, nfloat brightness, nfloat alpha);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColor FromDisplayP3 (nfloat red, nfloat green, nfloat blue, nfloat alpha);</span>
</pre>
</div>

</div> <!-- end type NSColor -->
<!-- start type NSColorList --> <div>
<h3>Type Changed: AppKit.NSColorList</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WriteToUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSColorList -->
<!-- start type NSColorPanel --> <div>
<h3>Type Changed: AppKit.NSColorPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSColorPanel -->
<!-- start type NSColorSpace --> <div>
<h3>Type Changed: AppKit.NSColorSpace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSColorSpace DisplayP3ColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColorSpace ExtendedGenericGamma22GrayColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSColorSpace ExtendedSRgbColorSpace { get; }</span>
</pre>
</div>

</div> <!-- end type NSColorSpace -->
<!-- start type NSColorWell --> <div>
<h3>Type Changed: AppKit.NSColorWell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSColorWell -->
<!-- start type NSComboBox --> <div>
<h3>Type Changed: AppKit.NSComboBox</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSComboBox -->
<!-- start type NSCompositingOperation --> <div>
<h3>Type Changed: AppKit.NSCompositingOperation</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Color = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorBurn = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorDodge = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Darken = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Difference = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Exclusion = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">HardLight = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Hue = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Lighten = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Luminosity = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">Multiply = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Overlay = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Saturation = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Screen = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftLight = 21,</span>
</pre>
</div>

</div> <!-- end type NSCompositingOperation -->
<!-- start type NSControl --> <div>
<h3>Type Changed: AppKit.NSControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSControl -->
<!-- start type NSDatePicker --> <div>
<h3>Type Changed: AppKit.NSDatePicker</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSDatePicker -->
<!-- start type NSDocument --> <div>
<h3>Type Changed: AppKit.NSDocument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBrowsingVersions { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopBrowsingVersions (System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StopBrowsingVersionsAsync ();</span>
</pre>
</div>

</div> <!-- end type NSDocument -->
<!-- start type NSDrawer --> <div>
<h3>Type Changed: AppKit.NSDrawer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDrawer -->
<!-- start type NSEvent --> <div>
<h3>Type Changed: AppKit.NSEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSTouch&gt; AllTouches { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouch[] GetCoalescedTouches (NSTouch touch);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSTouch&gt; GetTouches (NSView view);</span>
</pre>
</div>

</div> <!-- end type NSEvent -->
<!-- start type NSEventMask --> <div>
<h3>Type Changed: AppKit.NSEventMask</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DirectTouch = 137438953472,</span>
</pre>
</div>

</div> <!-- end type NSEventMask -->
<!-- start type NSEventType --> <div>
<h3>Type Changed: AppKit.NSEventType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DirectTouch = 37,</span>
</pre>
</div>

</div> <!-- end type NSEventType -->
<!-- start type NSFontPanel --> <div>
<h3>Type Changed: AppKit.NSFontPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSFontPanel -->
<!-- start type NSForm --> <div>
<h3>Type Changed: AppKit.NSForm</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSForm -->
<!-- start type NSGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSGestureRecognizer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public NSTouchEvent ShouldReceiveTouch { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TouchesBegan (NSEvent touchEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TouchesCancelled (NSEvent touchEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TouchesEnded (NSEvent touchEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TouchesMoved (NSEvent touchEvent);</span>
</pre>
</div>

</div> <!-- end type NSGestureRecognizer -->
<!-- start type NSGestureRecognizerDelegate --> <div>
<h3>Type Changed: AppKit.NSGestureRecognizerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldReceiveTouch (NSGestureRecognizer gestureRecognizer, NSTouch touch);</span>
</pre>
</div>

</div> <!-- end type NSGestureRecognizerDelegate -->
<!-- start type NSGestureRecognizerDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSGestureRecognizerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldReceiveTouch (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSTouch touch);</span>
</pre>
</div>

</div> <!-- end type NSGestureRecognizerDelegate_Extensions -->
<!-- start type NSImageName --> <div>
<h3>Type Changed: AppKit.NSImageName</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TouchBarAddDetailTemplate = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAddTemplate = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAlarmTemplate = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioInputMuteTemplate = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioInputTemplate = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioOutputMuteTemplate = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioOutputVolumeHighTemplate = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioOutputVolumeLowTemplate = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioOutputVolumeMediumTemplate = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarAudioOutputVolumeOffTemplate = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarBookmarksTemplate = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarColorPickerFill = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarColorPickerFont = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarColorPickerStroke = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarCommunicationAudioTemplate = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarCommunicationVideoTemplate = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarComposeTemplate = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarDeleteTemplate = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarDownloadTemplate = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarEnterFullScreenTemplate = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarExitFullScreenTemplate = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarFastForwardTemplate = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarFolderCopyToTemplate = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarFolderMoveToTemplate = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarFolderTemplate = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarGetInfoTemplate = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarGoBackTemplate = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarGoDownTemplate = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarGoForwardTemplate = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarGoUpTemplate = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarHistoryTemplate = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarIconViewTemplate = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarListViewTemplate = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarMailTemplate = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarNewFolderTemplate = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarNewMessageTemplate = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarOpenInBrowserTemplate = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarPauseTemplate = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarPlayPauseTemplate = 79,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarPlayTemplate = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarPlayheadTemplate = 78,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarQuickLookTemplate = 81,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRecordStartTemplate = 82,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRecordStopTemplate = 83,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRefreshTemplate = 84,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRewindTemplate = 85,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRotateLeftTemplate = 86,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarRotateRightTemplate = 87,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSearchTemplate = 88,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarShareTemplate = 89,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSidebarTemplate = 90,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipAhead15SecondsTemplate = 91,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipAhead30SecondsTemplate = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipAheadTemplate = 93,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipBack15SecondsTemplate = 94,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipBack30SecondsTemplate = 95,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipBackTemplate = 96,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipToEndTemplate = 97,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSkipToStartTemplate = 98,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarSlideshowTemplate = 99,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTagIconTemplate = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextBoldTemplate = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextBoxTemplate = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextCenterAlignTemplate = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextItalicTemplate = 104,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextJustifiedAlignTemplate = 105,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextLeftAlignTemplate = 106,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextListTemplate = 107,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextRightAlignTemplate = 108,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextStrikethroughTemplate = 109,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarTextUnderlineTemplate = 110,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarUserAddTemplate = 111,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarUserGroupTemplate = 112,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarUserTemplate = 113,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarVolumeDownTemplate = 114,</span>
	<span class='added added-field ' data-is-non-breaking="">TouchBarVolumeUpTemplate = 115,</span>
</pre>
</div>

</div> <!-- end type NSImageName -->
<!-- start type NSImageRep --> <div>
<h3>Type Changed: AppKit.NSImageRep</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImageLayoutDirection LayoutDirection { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSImageRep -->
<!-- start type NSImageView --> <div>
<h3>Type Changed: AppKit.NSImageView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSImageView FromImage (NSImage image);</span>
</pre>
</div>

</div> <!-- end type NSImageView -->
<!-- start type NSLayoutAnchor`1 --> <div>
<h3>Type Changed: AppKit.NSLayoutAnchor`1</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSLayoutAnchor`1 (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NSLayoutAnchor`1 -->
<!-- start type NSLayoutConstraint --> <div>
<h3>Type Changed: AppKit.NSLayoutConstraint</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLayoutAnchor&lt;Foundation.NSObject&gt; FirstAnchor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSLayoutAnchor&lt;Foundation.NSObject&gt; SecondAnchor { get; }</span>
</pre>
</div>

</div> <!-- end type NSLayoutConstraint -->
<!-- start type NSLayoutDimension --> <div>
<h3>Type Changed: AppKit.NSLayoutDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSLayoutDimension (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>

</div> <!-- end type NSLayoutDimension -->
<!-- start type NSLayoutGuide --> <div>
<h3>Type Changed: AppKit.NSLayoutGuide</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAmbiguousLayout { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSLayoutConstraint[] GetConstraintsAffectingLayout (NSLayoutConstraintOrientation orientation);</span>
</pre>
</div>

</div> <!-- end type NSLayoutGuide -->
<!-- start type NSLayoutXAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutXAxisAnchor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSLayoutXAxisAnchor (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>

</div> <!-- end type NSLayoutXAxisAnchor -->
<!-- start type NSLayoutYAxisAnchor --> <div>
<h3>Type Changed: AppKit.NSLayoutYAxisAnchor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSLayoutYAxisAnchor (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>

</div> <!-- end type NSLayoutYAxisAnchor -->
<!-- start type NSLevelIndicator --> <div>
<h3>Type Changed: AppKit.NSLevelIndicator</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSLevelIndicator -->
<!-- start type NSMatrix --> <div>
<h3>Type Changed: AppKit.NSMatrix</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSMatrix -->
<!-- start type NSMenu --> <div>
<h3>Type Changed: AppKit.NSMenu</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAccessibility</span>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceItemIdentification</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AccessibilityActivationPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] AccessibilityAllowedValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityAlternateUIVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityApplicationFocusedUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCancelButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityClearButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCloseButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityColumnCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityColumnIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnTitles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCriticalValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDecrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDefaultButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityDisclosed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityDisclosureLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityDocument { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEdited { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityExpanded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityExtrasMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityFilename { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFocused { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFocusedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrameInParentSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFrontmost { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFullScreenButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityGrowArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHandles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHeader { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHelp { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityHidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHorizontalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHorizontalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityHorizontalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityIncrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityInsertionPointLineNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLabelUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float AccessibilityLabelValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLinkedUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMain { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMainWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerGroupUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityMarkerTypeDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityMarkerUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMaxValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinimizeButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMinimized { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityModal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityNextContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityNumberOfCharacters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityOrderedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityOrientation AccessibilityOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityOverflowButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityParent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityPlaceholderValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityPreviousContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityProtectedContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityProxy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRoleDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityRowCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRowHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityRowIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityRulerMarkerType AccessibilityRulerMarkerType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilitySelected { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySelectedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySelectedTextRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSValue[] AccessibilitySelectedTextRanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityServesAsTitleForUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySharedCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedFocusElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedTextUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityShownMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilitySortDirection AccessibilitySortDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySplitters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySubrole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityTabs { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTitleUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityToolbarButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTopLevelUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl AccessibilityUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityValueDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityVerticalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityVerticalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityVerticalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityVisibleCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWarningValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityWindows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityZoomButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AccessibilityAddChildElement (NSAccessibilityElement childElement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformCancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformConfirm ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDecrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDelete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformIncrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPick ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPress ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformRaise ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowAlternateUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowDefaultUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowMenu ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject CreateElement (Foundation.NSString role, CoreGraphics.CGRect frame, Foundation.NSString label, Foundation.NSObject parent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAccessibilityAttributedString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetAccessibilityCellForColumn (nint column, nint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetAccessibilityFrame (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityLayoutForScreen (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityLayoutForScreen (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetAccessibilityLine (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRangeForLine (nint line);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetAccessibilityRtf (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityScreenForLayout (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityScreenForLayout (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetAccessibilityString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityStyleRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAccessibilitySelectorAllowed (ObjCRuntime.Selector selector);</span>
</pre>
</div>

</div> <!-- end type NSMenu -->
<!-- start type NSMenuItem --> <div>
<h3>Type Changed: AppKit.NSMenuItem</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAccessibility</span>
	<span class='added added-interface ' data-is-non-breaking="">INSUserInterfaceItemIdentification</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AccessibilityActivationPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] AccessibilityAllowedValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityAlternateUIVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityApplicationFocusedUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCancelButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityClearButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCloseButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityColumnCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityColumnIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnTitles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCriticalValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDecrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDefaultButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityDisclosed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityDisclosureLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityDocument { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEdited { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityExpanded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityExtrasMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityFilename { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFocused { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFocusedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrameInParentSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFrontmost { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFullScreenButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityGrowArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHandles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHeader { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHelp { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityHidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHorizontalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHorizontalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityHorizontalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityIncrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityInsertionPointLineNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLabelUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float AccessibilityLabelValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLinkedUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMain { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMainWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerGroupUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityMarkerTypeDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityMarkerUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMaxValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinimizeButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMinimized { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityModal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityNextContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityNumberOfCharacters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityOrderedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityOrientation AccessibilityOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityOverflowButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityParent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityPlaceholderValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityPreviousContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityProtectedContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityProxy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRoleDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityRowCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRowHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityRowIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityRulerMarkerType AccessibilityRulerMarkerType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilitySelected { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySelectedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySelectedTextRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSValue[] AccessibilitySelectedTextRanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityServesAsTitleForUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySharedCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedFocusElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedTextUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityShownMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilitySortDirection AccessibilitySortDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySplitters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySubrole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityTabs { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTitleUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityToolbarButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTopLevelUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl AccessibilityUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityValueDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityVerticalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityVerticalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityVerticalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityVisibleCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWarningValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityWindows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityZoomButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AccessibilityAddChildElement (NSAccessibilityElement childElement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformCancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformConfirm ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDecrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDelete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformIncrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPick ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPress ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformRaise ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowAlternateUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowDefaultUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowMenu ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject CreateElement (Foundation.NSString role, CoreGraphics.CGRect frame, Foundation.NSString label, Foundation.NSObject parent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAccessibilityAttributedString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetAccessibilityCellForColumn (nint column, nint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetAccessibilityFrame (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityLayoutForScreen (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityLayoutForScreen (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetAccessibilityLine (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRangeForLine (nint line);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetAccessibilityRtf (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityScreenForLayout (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityScreenForLayout (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetAccessibilityString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityStyleRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAccessibilitySelectorAllowed (ObjCRuntime.Selector selector);</span>
</pre>
</div>

</div> <!-- end type NSMenuItem -->
<!-- start type NSMenuView --> <div>
<h3>Type Changed: AppKit.NSMenuView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSMenuView -->
<!-- start type NSMutableFontCollection --> <div>
<h3>Type Changed: AppKit.NSMutableFontCollection</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("macOS 10.12 does not allow creation via this constructor")]
	public NSMutableFontCollection ();</span>
</div></pre>

</div> <!-- end type NSMutableFontCollection -->
<!-- start type NSOpenGLPixelFormat --> <div>
<h3>Type Changed: AppKit.NSOpenGLPixelFormat</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSOpenGLPixelFormat (uint[] attribs);</span>
</pre>
</div>

</div> <!-- end type NSOpenGLPixelFormat -->
<!-- start type NSOpenGLView --> <div>
<h3>Type Changed: AppKit.NSOpenGLView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSOpenGLView -->
<!-- start type NSOpenPanel --> <div>
<h3>Type Changed: AppKit.NSOpenPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSOpenPanel -->
<!-- start type NSOutlineView --> <div>
<h3>Type Changed: AppKit.NSOutlineView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StronglyReferencesItems { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSOutlineView -->
<!-- start type NSPageController --> <div>
<h3>Type Changed: AppKit.NSPageController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSPageController -->
<!-- start type NSPanGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSPanGestureRecognizer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfTouchesRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPanGestureRecognizer -->
<!-- start type NSPanel --> <div>
<h3>Type Changed: AppKit.NSPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSPanel -->
<!-- start type NSPasteboard --> <div>
<h3>Type Changed: AppKit.NSPasteboard</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint PrepareForNewContents (NSPasteboardContentsOptions options);</span>
</pre>
</div>

</div> <!-- end type NSPasteboard -->
<!-- start type NSPathControl --> <div>
<h3>Type Changed: AppKit.NSPathControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSPathControl -->
<!-- start type NSPopUpButton --> <div>
<h3>Type Changed: AppKit.NSPopUpButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSPopUpButton -->
<!-- start type NSPopover --> <div>
<h3>Type Changed: AppKit.NSPopover</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPopover -->
<!-- start type NSPredicateEditor --> <div>
<h3>Type Changed: AppKit.NSPredicateEditor</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSPredicateEditor -->
<!-- start type NSPressGestureRecognizer --> <div>
<h3>Type Changed: AppKit.NSPressGestureRecognizer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfTouchesRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPressGestureRecognizer -->
<!-- start type NSProgressIndicator --> <div>
<h3>Type Changed: AppKit.NSProgressIndicator</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSProgressIndicator -->
<!-- start type NSRemoteNotificationType --> <div>
<h3>Type Changed: AppKit.NSRemoteNotificationType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Alert = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Sound = 2,</span>
</pre>
</div>

</div> <!-- end type NSRemoteNotificationType -->
<!-- start type NSRemoteOpenPanel --> <div>
<h3>Type Changed: AppKit.NSRemoteOpenPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSRemoteOpenPanel -->
<!-- start type NSRemoteSavePanel --> <div>
<h3>Type Changed: AppKit.NSRemoteSavePanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSRemoteSavePanel -->
<!-- start type NSResponder --> <div>
<h3>Type Changed: AppKit.NSResponder</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTouchBar TouchBar { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetNewWindowForTab (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PresentError (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PresentError (Foundation.NSError error, NSWindow window, Foundation.NSObject delegate, ObjCRuntime.Selector didPresentSelector, IntPtr contextInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSError WillPresentError (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSResponder -->
<!-- start type NSRuleEditor --> <div>
<h3>Type Changed: AppKit.NSRuleEditor</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSRuleEditor -->
<!-- start type NSRulerView --> <div>
<h3>Type Changed: AppKit.NSRulerView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSRulerView -->
<!-- start type NSSavePanel --> <div>
<h3>Type Changed: AppKit.NSSavePanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSSavePanel -->
<!-- start type NSScreen --> <div>
<h3>Type Changed: AppKit.NSScreen</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanRepresentDisplayGamut (NSDisplayGamut displayGamut);</span>
</pre>
</div>

</div> <!-- end type NSScreen -->
<!-- start type NSScrollView --> <div>
<h3>Type Changed: AppKit.NSScrollView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSScrollView -->
<!-- start type NSScroller --> <div>
<h3>Type Changed: AppKit.NSScroller</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSScroller -->
<!-- start type NSSearchField --> <div>
<h3>Type Changed: AppKit.NSSearchField</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSSearchField -->
<!-- start type NSSearchFieldDelegate --> <div>
<h3>Type Changed: AppKit.NSSearchFieldDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] GetCandidates (NSTextField textField, NSTextView textView, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] GetTextCheckingResults (NSTextField textField, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSelectCandidate (NSTextField textField, NSTextView textView, uint index);</span>
</pre>
</div>

</div> <!-- end type NSSearchFieldDelegate -->
<!-- start type NSSecureTextField --> <div>
<h3>Type Changed: AppKit.NSSecureTextField</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSSecureTextField -->
<!-- start type NSSegmentedControl --> <div>
<h3>Type Changed: AppKit.NSSegmentedControl</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor SelectedSegmentBezelColor { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSSegmentedControl FromImages (NSImage[] images, NSSegmentSwitchTracking trackingMode, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSSegmentedControl FromLabels (string[] labels, NSSegmentSwitchTracking trackingMode, System.Action action);</span>
</pre>
</div>

</div> <!-- end type NSSegmentedControl -->
<!-- start type NSSharingService --> <div>
<h3>Type Changed: AppKit.NSSharingService</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public NSSharingServiceAnchoringViewForSharingService CreateAnchoringView { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSSharingService -->
<!-- start type NSSharingServiceDelegate --> <div>
<h3>Type Changed: AppKit.NSSharingServiceDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSView CreateAnchoringView (NSSharingService sharingService, CoreGraphics.CGRect positioningRect, NSRectEdge preferredEdge);</span>
</pre>
</div>

</div> <!-- end type NSSharingServiceDelegate -->
<!-- start type NSSharingServiceDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSSharingServiceDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSView CreateAnchoringView (INSSharingServiceDelegate This, NSSharingService sharingService, CoreGraphics.CGRect positioningRect, NSRectEdge preferredEdge);</span>
</pre>
</div>

</div> <!-- end type NSSharingServiceDelegate_Extensions -->
<!-- start type NSSharingServiceName --> <div>
<h3>Type Changed: AppKit.NSSharingServiceName</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CloudSharing = 15,</span>
</pre>
</div>

</div> <!-- end type NSSharingServiceName -->
<!-- start type NSSlider --> <div>
<h3>Type Changed: AppKit.NSSlider</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual nint IsVertical { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor TrackFillColor { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSSlider FromTarget (System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSSlider FromValue (double value, double minValue, double maxValue, System.Action action);</span>
</pre>
</div>

</div> <!-- end type NSSlider -->
<!-- start type NSSliderCell --> <div>
<h3>Type Changed: AppKit.NSSliderCell</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual nint IsVertical { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type NSSliderCell -->
<!-- start type NSSpellChecker --> <div>
<h3>Type Changed: AppKit.NSSpellChecker</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidChangeAutomaticCapitalizationNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidChangeAutomaticPeriodSubstitutionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidChangeAutomaticTextCompletionNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsAutomaticCapitalizationEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsAutomaticPeriodSubstitutionEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsAutomaticTextCompletionEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TextCheckingSelectedRangeKey { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DeletesAutospace (string precedingString, string followingString, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PreventsAutocorrectionBefore (string aString, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint RequestCandidates (Foundation.NSRange selectedRange, string stringToCheck, ulong checkingTypes, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, nint tag, System.Action&lt;System.nint,Foundation.NSTextCheckingResult[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSSpellCheckerCanidates&gt; RequestCandidatesAsync (Foundation.NSRange selectedRange, string stringToCheck, ulong checkingTypes, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, nint tag);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSSpellCheckerCanidates&gt; RequestCandidatesAsync (Foundation.NSRange selectedRange, string stringToCheck, ulong checkingTypes, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, nint tag, nint result);</span>
</pre>
</div>
<!-- start type NSSpellChecker.Notifications --> <div>
<h3>Type Changed: AppKit.NSSpellChecker.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticCapitalization (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticPeriodSubstitution (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeAutomaticTextCompletion (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSSpellChecker.Notifications -->

</div> <!-- end type NSSpellChecker -->
<!-- start type NSSplitView --> <div>
<h3>Type Changed: AppKit.NSSplitView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSSplitView -->
<!-- start type NSSplitViewController --> <div>
<h3>Type Changed: AppKit.NSSplitViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSSplitViewController -->
<!-- start type NSStackView --> <div>
<h3>Type Changed: AppKit.NSStackView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSStackView -->
<!-- start type NSStatusBarButton --> <div>
<h3>Type Changed: AppKit.NSStatusBarButton</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSStatusBarButton -->
<!-- start type NSStatusItem --> <div>
<h3>Type Changed: AppKit.NSStatusItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AutosaveName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSStatusItemBehavior Behavior { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Visible { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSStatusItem -->
<!-- start type NSStepper --> <div>
<h3>Type Changed: AppKit.NSStepper</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSStepper -->
<!-- start type NSTabView --> <div>
<h3>Type Changed: AppKit.NSTabView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTabViewBorderType BorderType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTabPosition TabPosition { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTabView -->
<!-- start type NSTabViewController --> <div>
<h3>Type Changed: AppKit.NSTabViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSTabViewController -->
<!-- start type NSTableCellView --> <div>
<h3>Type Changed: AppKit.NSTableCellView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSTableCellView -->
<!-- start type NSTableHeaderView --> <div>
<h3>Type Changed: AppKit.NSTableHeaderView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSTableHeaderView -->
<!-- start type NSTableRowView --> <div>
<h3>Type Changed: AppKit.NSTableRowView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSTableRowView -->
<!-- start type NSTableView --> <div>
<h3>Type Changed: AppKit.NSTableView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection UserInterfaceLayoutDirection { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableView -->
<!-- start type NSTableViewRowAction --> <div>
<h3>Type Changed: AppKit.NSTableViewRowAction</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage Image { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTableViewRowAction -->
<!-- start type NSText --> <div>
<h3>Type Changed: AppKit.NSText</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSText -->
<!-- start type NSTextField --> <div>
<h3>Type Changed: AppKit.NSTextField</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public NSTextFieldGetCandidates GetCandidates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextFieldTextCheckingResults GetTextCheckingResults { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextFieldSelectCandidate ShouldSelectCandidate { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextField CreateLabel (Foundation.NSAttributedString attributedStringValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextField CreateLabel (string stringValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextField CreateTextField (string stringValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTextField CreateWrappingLabel (string stringValue);</span>
</pre>
</div>

</div> <!-- end type NSTextField -->
<!-- start type NSTextFieldDelegate --> <div>
<h3>Type Changed: AppKit.NSTextFieldDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] GetCandidates (NSTextField textField, NSTextView textView, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] GetTextCheckingResults (NSTextField textField, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSelectCandidate (NSTextField textField, NSTextView textView, uint index);</span>
</pre>
</div>

</div> <!-- end type NSTextFieldDelegate -->
<!-- start type NSTextFieldDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSTextFieldDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject[] GetCandidates (INSTextFieldDelegate This, NSTextField textField, NSTextView textView, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSTextCheckingResult[] GetTextCheckingResults (INSTextFieldDelegate This, NSTextField textField, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldSelectCandidate (INSTextFieldDelegate This, NSTextField textField, NSTextView textView, uint index);</span>
</pre>
</div>

</div> <!-- end type NSTextFieldDelegate_Extensions -->
<!-- start type NSTextInputContext --> <div>
<h3>Type Changed: AppKit.NSTextInputContext</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextInputContext (INSTextInputClient client);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AcceptsGlyphInfo { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AllowedInputSourceLocales { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSTextInputClient Client { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] KeyboardInputSources { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SelectedKeyboardInputSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSTextInputContext -->
<!-- start type NSTextTab --> <div>
<h3>Type Changed: AppKit.NSTextTab</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSTextTab -->
<!-- start type NSTextTableBlock --> <div>
<h3>Type Changed: AppKit.NSTextTableBlock</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("macOS 10.12 does not allow creation via this constructor")]
	public NSTextTableBlock ();</span>
</div></pre>

</div> <!-- end type NSTextTableBlock -->
<!-- start type NSTextView --> <div>
<h3>Type Changed: AppKit.NSTextView</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSCandidateListTouchBarItemDelegate</span>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarDelegate</span>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCharacterPickerTouchBarItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticTextCompletionEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSCandidateListTouchBarItem CandidateListTouchBarItem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextViewGetCandidates GetCandidates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextViewTextCheckingResults GetTextCheckingCandidates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextViewSelectCandidate ShouldSelectCandidates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTextViewUpdateTouchBarItemIdentifiers ShouldUpdateTouchBarItemIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool StronglyReferencesTextStorage { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginSelectingCandidate (NSCandidateListTouchBarItem anItem, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ChangeSelectionFromCandidate (NSCandidateListTouchBarItem anItem, nint previousIndex, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ChangedCandidateListVisibility (NSCandidateListTouchBarItem anItem, bool isVisible);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSelectingCandidate (NSCandidateListTouchBarItem anItem, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouchBarItem MakeItem (NSTouchBar touchBar, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleAutomaticTextCompletion (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateCandidates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateTextTouchBarItems ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateTouchBarItemIdentifiers ();</span>
</pre>
</div>

</div> <!-- end type NSTextView -->
<!-- start type NSTextViewDelegate --> <div>
<h3>Type Changed: AppKit.NSTextViewDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] GetCandidates (NSTextView textView, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] GetTextCheckingCandidates (NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldSelectCandidates (NSTextView textView, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] ShouldUpdateTouchBarItemIdentifiers (NSTextView textView, string[] identifiers);</span>
</pre>
</div>

</div> <!-- end type NSTextViewDelegate -->
<!-- start type NSTextViewDelegate_Extensions --> <div>
<h3>Type Changed: AppKit.NSTextViewDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject[] GetCandidates (INSTextViewDelegate This, NSTextView textView, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSTextCheckingResult[] GetTextCheckingCandidates (INSTextViewDelegate This, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldSelectCandidates (INSTextViewDelegate This, NSTextView textView, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] ShouldUpdateTouchBarItemIdentifiers (INSTextViewDelegate This, NSTextView textView, string[] identifiers);</span>
</pre>
</div>

</div> <!-- end type NSTextViewDelegate_Extensions -->
<!-- start type NSTickMarkPosition --> <div>
<h3>Type Changed: AppKit.NSTickMarkPosition</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 3,</span>
</pre>
</div>

</div> <!-- end type NSTickMarkPosition -->
<!-- start type NSTitlebarAccessoryViewController --> <div>
<h3>Type Changed: AppKit.NSTitlebarAccessoryViewController</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSAnimationDelegate</span>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Animations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Animator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsHidden { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidEnd (NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidReachProgressMark (NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AnimationDidStop (NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject AnimationFor (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AnimationShouldStart (NSAnimation animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float ComputeAnimationCurve (NSAnimation animation, float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject DefaultAnimationFor (Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type NSTitlebarAccessoryViewController -->
<!-- start type NSTokenField --> <div>
<h3>Type Changed: AppKit.NSTokenField</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSTokenField -->
<!-- start type NSToolbar --> <div>
<h3>Type Changed: AppKit.NSToolbar</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSToolbarCloudSharingItemIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NSToolbarToggleSidebarItemIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type NSToolbar -->
<!-- start type NSView --> <div>
<h3>Type Changed: AppKit.NSView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSView -->
<!-- start type NSViewController --> <div>
<h3>Type Changed: AppKit.NSViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSViewController -->
<!-- start type NSVisualEffectMaterial --> <div>
<h3>Type Changed: AppKit.NSVisualEffectMaterial</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MediumLight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Menu = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Popover = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Selection = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Sidebar = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">UltraDark = 9,</span>
</pre>
</div>

</div> <!-- end type NSVisualEffectMaterial -->
<!-- start type NSVisualEffectView --> <div>
<h3>Type Changed: AppKit.NSVisualEffectView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Emphasized { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSVisualEffectView -->
<!-- start type NSWindow --> <div>
<h3>Type Changed: AppKit.NSWindow</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static bool DisableReleasedWhenClosedInConstructor;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool AllowsAutomaticWindowTabbing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindow[] TabbedWindows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TabbingIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSWindowTabbingMode TabbingMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSWindowUserTabbingPreference UserTabbingPreference { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserInterfaceLayoutDirection WindowTitlebarLayoutDirection { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddTabbedWindow (NSWindow window, NSWindowOrderingMode ordered);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanRepresentDisplayGamut (NSDisplayGamut displayGamut);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MergeAllWindows (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveTabToNewWindow (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SelectNextTab (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SelectPreviousTab (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToggleTabBar (Foundation.NSObject sender);</span>
</pre>
</div>

</div> <!-- end type NSWindow -->
<!-- start type NSWindowCollectionBehavior --> <div>
<h3>Type Changed: AppKit.NSWindowCollectionBehavior</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FullScreenNone = 512,</span>
</pre>
</div>

</div> <!-- end type NSWindowCollectionBehavior -->
<!-- start type NSWindowController --> <div>
<h3>Type Changed: AppKit.NSWindowController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NSWindowController -->
<!-- start type NSWorkspace --> <div>
<h3>Type Changed: AppKit.NSWorkspace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityDisplayShouldInvertColors { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityDisplayShouldReduceMotion { get; }</span>
</pre>
</div>

</div> <!-- end type NSWorkspace -->
<div> <!-- start type AttributedStringForCandidateHandler -->
<h3>New Type AppKit.AttributedStringForCandidateHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AttributedStringForCandidateHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AttributedStringForCandidateHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject candidate, nint index, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString Invoke (Foundation.NSObject candidate, nint index);</span>
}
</pre>
</div> <!-- end type AttributedStringForCandidateHandler -->
<div> <!-- start type INSCandidateListTouchBarItemDelegate -->
<h3>New Type AppKit.INSCandidateListTouchBarItemDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCandidateListTouchBarItemDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSCandidateListTouchBarItemDelegate -->
<div> <!-- start type INSCloudSharingServiceDelegate -->
<h3>New Type AppKit.INSCloudSharingServiceDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCloudSharingServiceDelegate : INSSharingServiceDelegate, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSCloudSharingServiceDelegate -->
<div> <!-- start type INSCloudSharingValidation -->
<h3>New Type AppKit.INSCloudSharingValidation</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCloudSharingValidation : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CloudKit.CKShare GetCloudShare (INSValidatedUserInterfaceItem item);</span>
}
</pre>
</div> <!-- end type INSCloudSharingValidation -->
<div> <!-- start type INSCollectionViewSectionHeaderView -->
<h3>New Type AppKit.INSCollectionViewSectionHeaderView</h3>
<pre class='added' data-is-non-breaking="">
public interface INSCollectionViewSectionHeaderView : INSCollectionViewElement, INSUserInterfaceItemIdentification, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSCollectionViewSectionHeaderView -->
<div> <!-- start type INSFilePromiseProviderDelegate -->
<h3>New Type AppKit.INSFilePromiseProviderDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFilePromiseProviderDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetFileNameForDestination (NSFilePromiseProvider filePromiseProvider, string fileType);</span>
}
</pre>
</div> <!-- end type INSFilePromiseProviderDelegate -->
<div> <!-- start type INSMenuValidation -->
<h3>New Type AppKit.INSMenuValidation</h3>
<pre class='added' data-is-non-breaking="">
public interface INSMenuValidation : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateMenuItem (NSMenuItem menuItem);</span>
}
</pre>
</div> <!-- end type INSMenuValidation -->
<div> <!-- start type INSScrubberDataSource -->
<h3>New Type AppKit.INSScrubberDataSource</h3>
<pre class='added' data-is-non-breaking="">
public interface INSScrubberDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetNumberOfItems (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberItemView GetViewForItem (NSScrubber scrubber, nint index);</span>
}
</pre>
</div> <!-- end type INSScrubberDataSource -->
<div> <!-- start type INSScrubberDelegate -->
<h3>New Type AppKit.INSScrubberDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSScrubberDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSScrubberDelegate -->
<div> <!-- start type INSScrubberFlowLayoutDelegate -->
<h3>New Type AppKit.INSScrubberFlowLayoutDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSScrubberFlowLayoutDelegate : INSScrubberDelegate, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSScrubberFlowLayoutDelegate -->
<div> <!-- start type INSSharingServicePickerTouchBarItemDelegate -->
<h3>New Type AppKit.INSSharingServicePickerTouchBarItemDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSSharingServicePickerTouchBarItemDelegate : INSSharingServicePickerDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual INSPasteboardWriting[] ItemsForSharingServicePickerTouchBarItem (NSSharingServicePickerTouchBarItem pickerTouchBarItem);</span>
}
</pre>
</div> <!-- end type INSSharingServicePickerTouchBarItemDelegate -->
<div> <!-- start type INSToolTipOwner -->
<h3>New Type AppKit.INSToolTipOwner</h3>
<pre class='added' data-is-non-breaking="">
public interface INSToolTipOwner : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetStringForToolTip (NSView view, nint tag, CoreGraphics.CGPoint point, IntPtr data);</span>
}
</pre>
</div> <!-- end type INSToolTipOwner -->
<div> <!-- start type INSTouchBarDelegate -->
<h3>New Type AppKit.INSTouchBarDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface INSTouchBarDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSTouchBarDelegate -->
<div> <!-- start type INSTouchBarProvider -->
<h3>New Type AppKit.INSTouchBarProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface INSTouchBarProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTouchBar TouchBar { get; }</span>
}
</pre>
</div> <!-- end type INSTouchBarProvider -->
<div> <!-- start type INSUserInterfaceValidations -->
<h3>New Type AppKit.INSUserInterfaceValidations</h3>
<pre class='added' data-is-non-breaking="">
public interface INSUserInterfaceValidations : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ValidateUserInterfaceItem (INSValidatedUserInterfaceItem item);</span>
}
</pre>
</div> <!-- end type INSUserInterfaceValidations -->
<div> <!-- start type INSValidatedUserInterfaceItem -->
<h3>New Type AppKit.INSValidatedUserInterfaceItem</h3>
<pre class='added' data-is-non-breaking="">
public interface INSValidatedUserInterfaceItem : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Action { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Tag { get; }</span>
}
</pre>
</div> <!-- end type INSValidatedUserInterfaceItem -->
<div> <!-- start type NSAccessibility_Extensions -->
<h3>New Type AppKit.NSAccessibility_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSAccessibility_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool GetAccessibilityRequired (INSAccessibility This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityRequired (INSAccessibility This, bool value);</span>
}
</pre>
</div> <!-- end type NSAccessibility_Extensions -->
<div> <!-- start type NSApplicationEnumerateWindowsHandler -->
<h3>New Type AppKit.NSApplicationEnumerateWindowsHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSApplicationEnumerateWindowsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationEnumerateWindowsHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSWindow window, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSWindow window, bool stop);</span>
}
</pre>
</div> <!-- end type NSApplicationEnumerateWindowsHandler -->
<div> <!-- start type NSApplicationUserAcceptedCloudKitShareEventArgs -->
<h3>New Type AppKit.NSApplicationUserAcceptedCloudKitShareEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class NSApplicationUserAcceptedCloudKitShareEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSApplicationUserAcceptedCloudKitShareEventArgs (CloudKit.CKShareMetadata metadata);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CloudKit.CKShareMetadata Metadata { get; set; }</span>
}
</pre>
</div> <!-- end type NSApplicationUserAcceptedCloudKitShareEventArgs -->
<div> <!-- start type NSApplication_NSTouchBarCustomization -->
<h3>New Type AppKit.NSApplication_NSTouchBarCustomization</h3>
<pre class='added' data-is-non-breaking="">
public static class NSApplication_NSTouchBarCustomization {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool GetAutomaticCustomizeTouchBarMenuItemEnabled (NSApplication This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAutomaticCustomizeTouchBarMenuItemEnabled (NSApplication This, bool enabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ToggleTouchBarCustomizationPalette (NSApplication This, Foundation.NSObject sender);</span>
}
</pre>
</div> <!-- end type NSApplication_NSTouchBarCustomization -->
<div> <!-- start type NSCandidateListTouchBarItem -->
<h3>New Type AppKit.NSCandidateListTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSCandidateListTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSCandidateListTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCandidateListTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCandidateListTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSCandidateListTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCollapsing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsTextInputContextCandidates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AttributedStringForCandidateHandler AttributedStringForCandidate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CandidateListVisible { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] Candidates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSTextInputClient Client { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Collapsed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSCandidateListTouchBarItemDelegate Delegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCandidates (Foundation.NSObject[] candidates, Foundation.NSRange selectedRange, string originalString);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateWithInsertionPointVisibility (bool isVisible);</span>
}
</pre>
</div> <!-- end type NSCandidateListTouchBarItem -->
<div> <!-- start type NSCandidateListTouchBarItemDelegate -->
<h3>New Type AppKit.NSCandidateListTouchBarItemDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSCandidateListTouchBarItemDelegate : Foundation.NSObject, INSCandidateListTouchBarItemDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSCandidateListTouchBarItemDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCandidateListTouchBarItemDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCandidateListTouchBarItemDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginSelectingCandidate (NSCandidateListTouchBarItem anItem, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ChangeSelectionFromCandidate (NSCandidateListTouchBarItem anItem, nint previousIndex, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ChangedCandidateListVisibility (NSCandidateListTouchBarItem anItem, bool isVisible);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndSelectingCandidate (NSCandidateListTouchBarItem anItem, nint index);</span>
}
</pre>
</div> <!-- end type NSCandidateListTouchBarItemDelegate -->
<div> <!-- start type NSCandidateListTouchBarItemDelegate_Extensions -->
<h3>New Type AppKit.NSCandidateListTouchBarItemDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCandidateListTouchBarItemDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void BeginSelectingCandidate (INSCandidateListTouchBarItemDelegate This, NSCandidateListTouchBarItem anItem, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ChangeSelectionFromCandidate (INSCandidateListTouchBarItemDelegate This, NSCandidateListTouchBarItem anItem, nint previousIndex, nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ChangedCandidateListVisibility (INSCandidateListTouchBarItemDelegate This, NSCandidateListTouchBarItem anItem, bool isVisible);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EndSelectingCandidate (INSCandidateListTouchBarItemDelegate This, NSCandidateListTouchBarItem anItem, nint index);</span>
}
</pre>
</div> <!-- end type NSCandidateListTouchBarItemDelegate_Extensions -->
<div> <!-- start type NSCloudKitSharingServiceOptions -->
<h3>New Type AppKit.NSCloudKitSharingServiceOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSCloudKitSharingServiceOptions {
	<span class='added added-field ' data-is-non-breaking="">AllowPrivate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowPublic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowReadOnly = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowReadWrite = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Standard = 0,</span>
}
</pre>
</div> <!-- end type NSCloudKitSharingServiceOptions -->
<div> <!-- start type NSCloudSharingServiceDelegate -->
<h3>New Type AppKit.NSCloudSharingServiceDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSCloudSharingServiceDelegate : AppKit.NSSharingServiceDelegate, INSCloudSharingServiceDelegate, INSSharingServiceDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSCloudSharingServiceDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCloudSharingServiceDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCloudSharingServiceDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Completed (NSSharingService sharingService, Foundation.NSObject[] items, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSCloudKitSharingServiceOptions Options (NSSharingService cloudKitSharingService, Foundation.NSItemProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Saved (NSSharingService sharingService, CloudKit.CKShare share);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stopped (NSSharingService sharingService, CloudKit.CKShare share);</span>
}
</pre>
</div> <!-- end type NSCloudSharingServiceDelegate -->
<div> <!-- start type NSCloudSharingServiceDelegate_Extensions -->
<h3>New Type AppKit.NSCloudSharingServiceDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCloudSharingServiceDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Completed (INSCloudSharingServiceDelegate This, NSSharingService sharingService, Foundation.NSObject[] items, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSCloudKitSharingServiceOptions Options (INSCloudSharingServiceDelegate This, NSSharingService cloudKitSharingService, Foundation.NSItemProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Saved (INSCloudSharingServiceDelegate This, NSSharingService sharingService, CloudKit.CKShare share);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Stopped (INSCloudSharingServiceDelegate This, NSSharingService sharingService, CloudKit.CKShare share);</span>
}
</pre>
</div> <!-- end type NSCloudSharingServiceDelegate_Extensions -->
<div> <!-- start type NSCollectionViewSectionHeaderView_Extensions -->
<h3>New Type AppKit.NSCollectionViewSectionHeaderView_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSCollectionViewSectionHeaderView_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSButton GetSectionCollapseButton (INSCollectionViewSectionHeaderView This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSectionCollapseButton (INSCollectionViewSectionHeaderView This, NSButton value);</span>
}
</pre>
</div> <!-- end type NSCollectionViewSectionHeaderView_Extensions -->
<div> <!-- start type NSColorPickerTouchBarItem -->
<h3>New Type AppKit.NSColorPickerTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSColorPickerTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSColorPickerTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSColorPickerTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSColorPickerTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSColorPickerTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor Color { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColorList ColorList { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsAlpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler Activated;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSColorPickerTouchBarItem CreateColorPicker (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColorPickerTouchBarItem CreateColorPicker (string identifier, NSImage image);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColorPickerTouchBarItem CreateStrokeColorPicker (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSColorPickerTouchBarItem CreateTextColorPicker (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSColorPickerTouchBarItem -->
<div> <!-- start type NSCustomTouchBarItem -->
<h3>New Type AppKit.NSCustomTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSCustomTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSCustomTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCustomTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSCustomTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSCustomTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView View { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSViewController ViewController { get; set; }</span>
}
</pre>
</div> <!-- end type NSCustomTouchBarItem -->
<div> <!-- start type NSDisplayGamut -->
<h3>New Type AppKit.NSDisplayGamut</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSDisplayGamut {
	<span class='added added-field ' data-is-non-breaking="">P3 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Srgb = 1,</span>
}
</pre>
</div> <!-- end type NSDisplayGamut -->
<div> <!-- start type NSFilePromiseProvider -->
<h3>New Type AppKit.NSFilePromiseProvider</h3>
<pre class='added' data-is-non-breaking="">
public class NSFilePromiseProvider : Foundation.NSObject, INSPasteboardWriting, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFilePromiseProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFilePromiseProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFilePromiseProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFilePromiseProvider (string fileType, INSFilePromiseProviderDelegate delegate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSFilePromiseProviderDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FileType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject UserInfo { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetPasteboardPropertyListForType (string type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);</span>
}
</pre>
</div> <!-- end type NSFilePromiseProvider -->
<div> <!-- start type NSFilePromiseProviderDelegate_Extensions -->
<h3>New Type AppKit.NSFilePromiseProviderDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFilePromiseProviderDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSOperationQueue GetOperationQueue (INSFilePromiseProviderDelegate This, NSFilePromiseProvider filePromiseProvider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WritePromiseToUrl (INSFilePromiseProviderDelegate This, NSFilePromiseProvider filePromiseProvider, Foundation.NSUrl url, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type NSFilePromiseProviderDelegate_Extensions -->
<div> <!-- start type NSFilePromiseReceiver -->
<h3>New Type AppKit.NSFilePromiseReceiver</h3>
<pre class='added' data-is-non-breaking="">
public class NSFilePromiseReceiver : Foundation.NSObject, INSPasteboardReading, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFilePromiseReceiver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFilePromiseReceiver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFilePromiseReceiver (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] FileNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] FileTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableDraggedTypes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("No longer an OS X API - it will never be called")]
	public virtual Foundation.NSObject InitWithPasteboardPropertyList (Foundation.NSObject propertyList, string type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReceivePromisedFiles (Foundation.NSUrl destinationDir, Foundation.NSDictionary options, Foundation.NSOperationQueue operationQueue, System.Action&lt;Foundation.NSUrl,Foundation.NSError&gt; reader);</span>
}
</pre>
</div> <!-- end type NSFilePromiseReceiver -->
<div> <!-- start type NSGestureRecognizer_NSTouchBar -->
<h3>New Type AppKit.NSGestureRecognizer_NSTouchBar</h3>
<pre class='added' data-is-non-breaking="">
public static class NSGestureRecognizer_NSTouchBar {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchTypeMask GetAllowedTouchTypes (NSGestureRecognizer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAllowedTouchTypes (NSGestureRecognizer This, NSTouchTypeMask types);</span>
}
</pre>
</div> <!-- end type NSGestureRecognizer_NSTouchBar -->
<div> <!-- start type NSGridCell -->
<h3>New Type AppKit.NSGridCell</h3>
<pre class='added' data-is-non-breaking="">
public class NSGridCell : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridCell (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridCell (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridCell (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridColumn Column { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView ContentView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLayoutConstraint[] CustomPlacementConstraints { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSView EmptyContentView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridRow Row { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridRowAlignment RowAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSGridCell -->
<div> <!-- start type NSGridCellPlacement -->
<h3>New Type AppKit.NSGridCellPlacement</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSGridCellPlacement {
	<span class='added added-field ' data-is-non-breaking="">Bottom = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Center = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Fill = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Inherited = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Leading = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Top = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 3,</span>
}
</pre>
</div> <!-- end type NSGridCellPlacement -->
<div> <!-- start type NSGridColumn -->
<h3>New Type AppKit.NSGridColumn</h3>
<pre class='added' data-is-non-breaking="">
public class NSGridColumn : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridColumn (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridColumn (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridColumn (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nint CellCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridView GridView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat LeadingPadding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TrailingPadding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement X { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridCell GetCell (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MergeCells (Foundation.NSRange range);</span>
}
</pre>
</div> <!-- end type NSGridColumn -->
<div> <!-- start type NSGridRow -->
<h3>New Type AppKit.NSGridRow</h3>
<pre class='added' data-is-non-breaking="">
public class NSGridRow : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridRow (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridRow (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridRow (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BottomPadding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint CellCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridView GridView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridRowAlignment RowAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TopPadding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridCell GetCell (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MergeCells (Foundation.NSRange range);</span>
}
</pre>
</div> <!-- end type NSGridRow -->
<div> <!-- start type NSGridRowAlignment -->
<h3>New Type AppKit.NSGridRowAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSGridRowAlignment {
	<span class='added added-field ' data-is-non-breaking="">FirstBaseline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Inherited = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">LastBaseline = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 1,</span>
}
</pre>
</div> <!-- end type NSGridRowAlignment -->
<div> <!-- start type NSGridView -->
<h3>New Type AppKit.NSGridView</h3>
<pre class='added' data-is-non-breaking="">
public class NSGridView : AppKit.NSView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridView (CoreGraphics.CGRect frameRect);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSGridView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGridView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ColumnCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColumnSpacing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridRowAlignment RowAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint RowCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RowSpacing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static nfloat SizeForContent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSGridCellPlacement Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridColumn AddColumn (NSView[] views);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridRow AddRow (NSView[] views);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGridView Create (NSView[] rows);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSGridView Create (nint columnCount, nint rowCount);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridCell GetCell (NSView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridCell GetCell (nint columnIndex, nint rowIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridColumn GetColumn (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetIndex (NSGridColumn column);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetIndex (NSGridRow row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridRow GetRow (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridColumn InsertColumn (nint index, NSView[] views);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGridRow InsertRow (nint index, NSView[] views);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MergeCells (Foundation.NSRange hRange, Foundation.NSRange vRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveColumn (nint fromIndex, nint toIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveRow (nint fromIndex, nint toIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveColumn (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveRow (nint index);</span>
}
</pre>
</div> <!-- end type NSGridView -->
<div> <!-- start type NSGroupTouchBarItem -->
<h3>New Type AppKit.NSGroupTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSGroupTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSGroupTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGroupTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSGroupTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSGroupTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTouchBar GroupTouchBar { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSGroupTouchBarItem CreateGroupItem (string identifier, NSTouchBarItem[] items);</span>
}
</pre>
</div> <!-- end type NSGroupTouchBarItem -->
<div> <!-- start type NSImageHint -->
<h3>New Type AppKit.NSImageHint</h3>
<pre class='added' data-is-non-breaking="">
public static class NSImageHint {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Ctm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Interpolation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserInterfaceLayoutDirection { get; }</span>
}
</pre>
</div> <!-- end type NSImageHint -->
<div> <!-- start type NSImageLayoutDirection -->
<h3>New Type AppKit.NSImageLayoutDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSImageLayoutDirection {
	<span class='added added-field ' data-is-non-breaking="">LeftToRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RightToLeft = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = -1,</span>
}
</pre>
</div> <!-- end type NSImageLayoutDirection -->
<div> <!-- start type NSImageNameExtensions -->
<h3>New Type AppKit.NSImageNameExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSImageNameExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSImageName self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSImageName GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSImageNameExtensions -->
<div> <!-- start type NSOpenGLLayer -->
<h3>New Type AppKit.NSOpenGLLayer</h3>
<pre class='added' data-is-non-breaking="">
public class NSOpenGLLayer : CoreAnimation.CAOpenGLLayer, CoreAnimation.ICAMediaTiming, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSOpenGLLayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSOpenGLLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSOpenGLLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSOpenGLLayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSOpenGLContext OpenGLContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSOpenGLPixelFormat OpenGLPixelFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView View { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanDraw (NSOpenGLContext context, NSOpenGLPixelFormat pixelFormat, double t, CoreVideo.CVTimeStamp ts);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Draw (NSOpenGLContext context, NSOpenGLPixelFormat pixelFormat, double t, CoreVideo.CVTimeStamp ts);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSOpenGLContext GetOpenGLContext (NSOpenGLPixelFormat pixelFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSOpenGLPixelFormat GetOpenGLPixelFormat (uint mask);</span>
}
</pre>
</div> <!-- end type NSOpenGLLayer -->
<div> <!-- start type NSPasteboardContentsOptions -->
<h3>New Type AppKit.NSPasteboardContentsOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPasteboardContentsOptions {
	<span class='added added-field ' data-is-non-breaking="">CurrentHostOnly = 1,</span>
}
</pre>
</div> <!-- end type NSPasteboardContentsOptions -->
<div> <!-- start type NSPopoverTouchBarItem -->
<h3>New Type AppKit.NSPopoverTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSPopoverTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPopoverTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPopoverTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPopoverTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPopoverTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView CollapsedRepresentation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage CollapsedRepresentationImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CollapsedRepresentationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTouchBar PopoverTouchBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTouchBar PressAndHoldTouchBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsCloseButton { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DismissPopover (Foundation.NSObject sender);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSGestureRecognizer MakeStandardActivatePopoverGestureRecognizer ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShowPopover (Foundation.NSObject sender);</span>
}
</pre>
</div> <!-- end type NSPopoverTouchBarItem -->
<div> <!-- start type NSResponder_NSTouchBarProvider -->
<h3>New Type AppKit.NSResponder_NSTouchBarProvider</h3>
<pre class='added' data-is-non-breaking="">
public static class NSResponder_NSTouchBarProvider {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchBar GetTouchBar (NSResponder This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchBar MakeTouchBar (NSResponder This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetTouchBar (NSResponder This, NSTouchBar bar);</span>
}
</pre>
</div> <!-- end type NSResponder_NSTouchBarProvider -->
<div> <!-- start type NSScrubber -->
<h3>New Type AppKit.NSScrubber</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubber : AppKit.NSView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubber ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubber (CoreGraphics.CGRect frameRect);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubber (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubber (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubber (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView BackgroundView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Continuous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSScrubberDataSource DataSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSScrubberDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FloatsSelectionViews { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint HighlightedIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubberAlignment ItemAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubberMode Mode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfItems { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubberLayout ScrubberLayout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SelectedIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubberSelectionStyle SelectionBackgroundStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubberSelectionStyle SelectionOverlayStyle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsAdditionalContentIndicators { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsArrowButtons { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberItemView GetItemViewForItem (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertItems (Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberItemView MakeItem (string itemIdentifier, Foundation.NSObject owner);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveItem (nint oldIndex, nint newIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformSequentialBatchUpdates (System.Action updateHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterClass (ObjCRuntime.Class itemViewClass, string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterNib (NSNib nib, string itemIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReloadData ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReloadItems (Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveItems (Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScrollItem (nint index, NSScrubberAlignment alignment);</span>
}
</pre>
</div> <!-- end type NSScrubber -->
<div> <!-- start type NSScrubberAlignment -->
<h3>New Type AppKit.NSScrubberAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSScrubberAlignment {
	<span class='added added-field ' data-is-non-breaking="">Center = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Leading = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 2,</span>
}
</pre>
</div> <!-- end type NSScrubberAlignment -->
<div> <!-- start type NSScrubberArrangedView -->
<h3>New Type AppKit.NSScrubberArrangedView</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberArrangedView : AppKit.NSView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberArrangedView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberArrangedView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberArrangedView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberArrangedView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Highlighted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Selected { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ApplyLayoutAttributes (NSScrubberLayoutAttributes layoutAttributes);</span>
}
</pre>
</div> <!-- end type NSScrubberArrangedView -->
<div> <!-- start type NSScrubberDataSource -->
<h3>New Type AppKit.NSScrubberDataSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSScrubberDataSource : Foundation.NSObject, INSScrubberDataSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberDataSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberDataSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberDataSource (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetNumberOfItems (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberItemView GetViewForItem (NSScrubber scrubber, nint index);</span>
}
</pre>
</div> <!-- end type NSScrubberDataSource -->
<div> <!-- start type NSScrubberDelegate -->
<h3>New Type AppKit.NSScrubberDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberDelegate : Foundation.NSObject, INSScrubberDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBeginInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidCancelInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeVisible (NSScrubber scrubber, Foundation.NSRange visibleRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidHighlightItem (NSScrubber scrubber, nint highlightedIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectItem (NSScrubber scrubber, nint selectedIndex);</span>
}
</pre>
</div> <!-- end type NSScrubberDelegate -->
<div> <!-- start type NSScrubberDelegate_Extensions -->
<h3>New Type AppKit.NSScrubberDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSScrubberDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidBeginInteracting (INSScrubberDelegate This, NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidCancelInteracting (INSScrubberDelegate This, NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeVisible (INSScrubberDelegate This, NSScrubber scrubber, Foundation.NSRange visibleRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinishInteracting (INSScrubberDelegate This, NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidHighlightItem (INSScrubberDelegate This, NSScrubber scrubber, nint highlightedIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectItem (INSScrubberDelegate This, NSScrubber scrubber, nint selectedIndex);</span>
}
</pre>
</div> <!-- end type NSScrubberDelegate_Extensions -->
<div> <!-- start type NSScrubberFlowLayout -->
<h3>New Type AppKit.NSScrubberFlowLayout</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberFlowLayout : AppKit.NSScrubberLayout, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberFlowLayout ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberFlowLayout (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberFlowLayout (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberFlowLayout (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize ItemSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ItemSpacing { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvalidateLayoutForItems (Foundation.NSIndexSet invalidItemIndexes);</span>
}
</pre>
</div> <!-- end type NSScrubberFlowLayout -->
<div> <!-- start type NSScrubberFlowLayoutDelegate -->
<h3>New Type AppKit.NSScrubberFlowLayoutDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberFlowLayoutDelegate : Foundation.NSObject, INSScrubberDelegate, INSScrubberFlowLayoutDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberFlowLayoutDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberFlowLayoutDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberFlowLayoutDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidBeginInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidCancelInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeVisible (NSScrubber scrubber, Foundation.NSRange visibleRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishInteracting (NSScrubber scrubber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidHighlightItem (NSScrubber scrubber, nint highlightedIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectItem (NSScrubber scrubber, nint selectedIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Layout (NSScrubber scrubber, NSScrubberFlowLayout layout, nint itemIndex);</span>
}
</pre>
</div> <!-- end type NSScrubberFlowLayoutDelegate -->
<div> <!-- start type NSScrubberFlowLayoutDelegate_Extensions -->
<h3>New Type AppKit.NSScrubberFlowLayoutDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSScrubberFlowLayoutDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGSize Layout (INSScrubberFlowLayoutDelegate This, NSScrubber scrubber, NSScrubberFlowLayout layout, nint itemIndex);</span>
}
</pre>
</div> <!-- end type NSScrubberFlowLayoutDelegate_Extensions -->
<div> <!-- start type NSScrubberImageItemView -->
<h3>New Type AppKit.NSScrubberImageItemView</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberImageItemView : AppKit.NSScrubberItemView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberImageItemView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberImageItemView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberImageItemView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberImageItemView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage Image { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImageAlignment ImageAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImageView ImageView { get; }</span>
}
</pre>
</div> <!-- end type NSScrubberImageItemView -->
<div> <!-- start type NSScrubberItemView -->
<h3>New Type AppKit.NSScrubberItemView</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberItemView : AppKit.NSScrubberArrangedView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberItemView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberItemView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberItemView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberItemView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type NSScrubberItemView -->
<div> <!-- start type NSScrubberLayout -->
<h3>New Type AppKit.NSScrubberLayout</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberLayout : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberLayout ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberLayout (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberLayout (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberLayout (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyMirrorsInRightToLeftLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ObjCRuntime.Class LayoutAttributesClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSScrubber Scrubber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize ScrubberContentSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect VisibleRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvalidateLayout ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberLayoutAttributes LayoutAttributesForItem (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSScrubberLayoutAttributes&gt; LayoutAttributesForItems (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareLayout ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInvalidateLayoutForChangeFromVisibleRect (CoreGraphics.CGRect fromVisibleRect, CoreGraphics.CGRect toVisibleRect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInvalidateLayoutForHighlightChange ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInvalidateLayoutForSelectionChange ();</span>
}
</pre>
</div> <!-- end type NSScrubberLayout -->
<div> <!-- start type NSScrubberLayoutAttributes -->
<h3>New Type AppKit.NSScrubberLayoutAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberLayoutAttributes : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberLayoutAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberLayoutAttributes (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberLayoutAttributes (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Frame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint ItemIndex { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSScrubberLayoutAttributes CreateLayoutAttributes (nint index);</span>
}
</pre>
</div> <!-- end type NSScrubberLayoutAttributes -->
<div> <!-- start type NSScrubberMode -->
<h3>New Type AppKit.NSScrubberMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSScrubberMode {
	<span class='added added-field ' data-is-non-breaking="">Fixed = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Free = 1,</span>
}
</pre>
</div> <!-- end type NSScrubberMode -->
<div> <!-- start type NSScrubberProportionalLayout -->
<h3>New Type AppKit.NSScrubberProportionalLayout</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberProportionalLayout : AppKit.NSScrubberLayout, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberProportionalLayout ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberProportionalLayout (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberProportionalLayout (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberProportionalLayout (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberProportionalLayout (nint numberOfVisibleItems);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfVisibleItems { get; set; }</span>
}
</pre>
</div> <!-- end type NSScrubberProportionalLayout -->
<div> <!-- start type NSScrubberSelectionStyle -->
<h3>New Type AppKit.NSScrubberSelectionStyle</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberSelectionStyle : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberSelectionStyle ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberSelectionStyle (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberSelectionStyle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberSelectionStyle (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSScrubberSelectionStyle OutlineOverlayStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSScrubberSelectionStyle RoundedBackgroundStyle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSScrubberSelectionView MakeSelectionView ();</span>
}
</pre>
</div> <!-- end type NSScrubberSelectionStyle -->
<div> <!-- start type NSScrubberSelectionView -->
<h3>New Type AppKit.NSScrubberSelectionView</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberSelectionView : AppKit.NSScrubberArrangedView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberSelectionView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberSelectionView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberSelectionView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberSelectionView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type NSScrubberSelectionView -->
<div> <!-- start type NSScrubberTextItemView -->
<h3>New Type AppKit.NSScrubberTextItemView</h3>
<pre class='added' data-is-non-breaking="">
public class NSScrubberTextItemView : AppKit.NSScrubberItemView, INSAccessibility, INSAccessibilityElementProtocol, INSAppearanceCustomization, INSDraggingDestination, INSTouchBarProvider, INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberTextItemView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSScrubberTextItemView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberTextItemView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSScrubberTextItemView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTextField TextField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
}
</pre>
</div> <!-- end type NSScrubberTextItemView -->
<div> <!-- start type NSSharingServiceAnchoringViewForSharingService -->
<h3>New Type AppKit.NSSharingServiceAnchoringViewForSharingService</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSSharingServiceAnchoringViewForSharingService : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSharingServiceAnchoringViewForSharingService (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSSharingService sharingService, CoreGraphics.CGRect positioningRect, NSRectEdge preferredEdge, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSView EndInvoke (CoreGraphics.CGRect positioningRect, NSRectEdge preferredEdge, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSView Invoke (NSSharingService sharingService, CoreGraphics.CGRect positioningRect, NSRectEdge preferredEdge);</span>
}
</pre>
</div> <!-- end type NSSharingServiceAnchoringViewForSharingService -->
<div> <!-- start type NSSharingServicePickerTouchBarItem -->
<h3>New Type AppKit.NSSharingServicePickerTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSSharingServicePickerTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSharingServicePickerTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSharingServicePickerTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSharingServicePickerTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSSharingServicePickerTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual NSImage ButtonImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ButtonTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSSharingServicePickerTouchBarItemDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSSharingServicePickerTouchBarItem -->
<div> <!-- start type NSSharingServicePickerTouchBarItemDelegate -->
<h3>New Type AppKit.NSSharingServicePickerTouchBarItemDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSSharingServicePickerTouchBarItemDelegate : Foundation.NSObject, INSSharingServicePickerDelegate, INSSharingServicePickerTouchBarItemDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSharingServicePickerTouchBarItemDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSharingServicePickerTouchBarItemDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSharingServicePickerTouchBarItemDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual INSSharingServiceDelegate DelegateForSharingService (NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChooseSharingService (NSSharingServicePicker sharingServicePicker, NSSharingService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual INSPasteboardWriting[] ItemsForSharingServicePickerTouchBarItem (NSSharingServicePickerTouchBarItem pickerTouchBarItem);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSSharingService[] SharingServicesForItems (NSSharingServicePicker sharingServicePicker, Foundation.NSObject[] items, NSSharingService[] proposedServices);</span>
}
</pre>
</div> <!-- end type NSSharingServicePickerTouchBarItemDelegate -->
<div> <!-- start type NSSliderAccessory -->
<h3>New Type AppKit.NSSliderAccessory</h3>
<pre class='added' data-is-non-breaking="">
public class NSSliderAccessory : Foundation.NSObject, INSAccessibility, INSAccessibilityElementProtocol, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSliderAccessory (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderAccessory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderAccessory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AccessibilityActivationPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] AccessibilityAllowedValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityAlternateUIVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityApplicationFocusedUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCancelButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityClearButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCloseButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityColumnCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityColumnIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumnTitles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityCriticalValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDecrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDefaultButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityDisclosed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityDisclosedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityDisclosureLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityDocument { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEdited { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityExpanded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityExtrasMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityFilename { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFocused { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFocusedWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityFrontmost { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityFullScreenButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityGrowArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityHandles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHeader { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHelp { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityHidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityHorizontalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityHorizontalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityHorizontalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityIncrementButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityInsertionPointLineNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLabelUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float AccessibilityLabelValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityLinkedUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMain { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMainWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerGroupUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityMarkerTypeDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityMarkerUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMarkerValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMaxValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMenuBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityMinimizeButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityMinimized { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityModal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityNextContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityNumberOfCharacters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityOrderedByRow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityOrientation AccessibilityOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityOverflowButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityParent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityPlaceholderValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityPreviousContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityProtectedContent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityProxy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilityRequired { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityRoleDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint AccessibilityRowCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRowHeaderUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityRowIndexRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityRulerMarkerType AccessibilityRulerMarkerType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilitySearchMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AccessibilitySelected { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySelectedRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySelectedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySelectedTextRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSValue[] AccessibilitySelectedTextRanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityServesAsTitleForUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilitySharedCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedFocusElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySharedTextUIElements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityShownMenu { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilitySortDirection AccessibilitySortDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilitySplitters { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilitySubrole { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityTabs { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTitleUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityToolbarButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityTopLevelUIElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl AccessibilityUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityValueDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityVerticalScrollBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccessibilityVerticalUnitDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAccessibilityUnits AccessibilityVerticalUnits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleCells { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange AccessibilityVisibleCharacterRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleChildren { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityVisibleRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWarningValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityWindow { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject[] AccessibilityWindows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject AccessibilityZoomButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSliderAccessoryBehavior Behavior { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double DefaultWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double WidthWide { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformCancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformConfirm ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDecrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformDelete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformIncrement ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPick ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformPress ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformRaise ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowAlternateUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowDefaultUI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool AccessibilityPerformShowMenu ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSSliderAccessory CreateAccessory (NSImage image);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSAttributedString GetAccessibilityAttributedString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetAccessibilityCellForColumn (nint column, nint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetAccessibilityFrame (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityLayoutForScreen (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityLayoutForScreen (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetAccessibilityLine (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityRangeForLine (nint line);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetAccessibilityRtf (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetAccessibilityScreenForLayout (CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGSize GetAccessibilityScreenForLayout (CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetAccessibilityString (Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSRange GetAccessibilityStyleRange (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAccessibilitySelectorAllowed (ObjCRuntime.Selector selector);</span>
}
</pre>
</div> <!-- end type NSSliderAccessory -->
<div> <!-- start type NSSliderAccessoryBehavior -->
<h3>New Type AppKit.NSSliderAccessoryBehavior</h3>
<pre class='added' data-is-non-breaking="">
public class NSSliderAccessoryBehavior : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSliderAccessoryBehavior ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSSliderAccessoryBehavior (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderAccessoryBehavior (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderAccessoryBehavior (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSSliderAccessoryBehavior AutomaticBehavior { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSSliderAccessoryBehavior ValueResetBehavior { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSSliderAccessoryBehavior ValueStepBehavior { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSSliderAccessoryBehavior CreateBehavior (System.Action&lt;NSSliderAccessory&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSSliderAccessoryBehavior CreateBehavior (Foundation.NSObject target, ObjCRuntime.Selector action);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleAction (NSSliderAccessory sender);</span>
}
</pre>
</div> <!-- end type NSSliderAccessoryBehavior -->
<div> <!-- start type NSSliderTouchBarItem -->
<h3>New Type AppKit.NSSliderTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSSliderTouchBarItem : AppKit.NSTouchBarItem, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSliderTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSSliderTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSSliderTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Selector Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSliderAccessory MaximumValueAccessory { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSliderAccessory MinimumValueAccessory { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSSlider Slider { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Target { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ValueAccessoryWidth { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler Activated;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type NSSliderTouchBarItem -->
<div> <!-- start type NSSpellCheckerCanidates -->
<h3>New Type AppKit.NSSpellCheckerCanidates</h3>
<pre class='added' data-is-non-breaking="">
public class NSSpellCheckerCanidates {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSSpellCheckerCanidates (nint arg1, Foundation.NSTextCheckingResult[] arg2);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public nint Arg1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSTextCheckingResult[] Arg2 { get; set; }</span>
}
</pre>
</div> <!-- end type NSSpellCheckerCanidates -->
<div> <!-- start type NSStatusItemBehavior -->
<h3>New Type AppKit.NSStatusItemBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSStatusItemBehavior {
	<span class='added added-field ' data-is-non-breaking="">RemovalAllowed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TerminationOnRemoval = 4,</span>
}
</pre>
</div> <!-- end type NSStatusItemBehavior -->
<div> <!-- start type NSTabPosition -->
<h3>New Type AppKit.NSTabPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTabPosition {
	<span class='added added-field ' data-is-non-breaking="">Bottom = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Top = 1,</span>
}
</pre>
</div> <!-- end type NSTabPosition -->
<div> <!-- start type NSTabViewBorderType -->
<h3>New Type AppKit.NSTabViewBorderType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTabViewBorderType {
	<span class='added added-field ' data-is-non-breaking="">Bezel = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Line = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type NSTabViewBorderType -->
<div> <!-- start type NSTextFieldGetCandidates -->
<h3>New Type AppKit.NSTextFieldGetCandidates</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextFieldGetCandidates : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextFieldGetCandidates (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextField textField, NSTextView textView, Foundation.NSRange selectedRange, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] Invoke (NSTextField textField, NSTextView textView, Foundation.NSRange selectedRange);</span>
}
</pre>
</div> <!-- end type NSTextFieldGetCandidates -->
<div> <!-- start type NSTextFieldSelectCandidate -->
<h3>New Type AppKit.NSTextFieldSelectCandidate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextFieldSelectCandidate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextFieldSelectCandidate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextField textField, NSTextView textView, uint index, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (NSTextField textField, NSTextView textView, uint index);</span>
}
</pre>
</div> <!-- end type NSTextFieldSelectCandidate -->
<div> <!-- start type NSTextFieldTextCheckingResults -->
<h3>New Type AppKit.NSTextFieldTextCheckingResults</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextFieldTextCheckingResults : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextFieldTextCheckingResults (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextField textField, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] Invoke (NSTextField textField, NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
}
</pre>
</div> <!-- end type NSTextFieldTextCheckingResults -->
<div> <!-- start type NSTextField_NSTouchBar -->
<h3>New Type AppKit.NSTextField_NSTouchBar</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTextField_NSTouchBar {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool GetAllowsCharacterPickerTouchBarItem (NSTextField This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetAutomaticTextCompletionEnabled (NSTextField This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAllowsCharacterPickerTouchBarItem (NSTextField This, bool allows);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAutomaticTextCompletionEnabled (NSTextField This, bool enabled);</span>
}
</pre>
</div> <!-- end type NSTextField_NSTouchBar -->
<div> <!-- start type NSTextViewGetCandidates -->
<h3>New Type AppKit.NSTextViewGetCandidates</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextViewGetCandidates : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextViewGetCandidates (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextView textView, Foundation.NSRange selectedRange, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] Invoke (NSTextView textView, Foundation.NSRange selectedRange);</span>
}
</pre>
</div> <!-- end type NSTextViewGetCandidates -->
<div> <!-- start type NSTextViewSelectCandidate -->
<h3>New Type AppKit.NSTextViewSelectCandidate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextViewSelectCandidate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextViewSelectCandidate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextView textView, uint index, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (NSTextView textView, uint index);</span>
}
</pre>
</div> <!-- end type NSTextViewSelectCandidate -->
<div> <!-- start type NSTextViewTextCheckingResults -->
<h3>New Type AppKit.NSTextViewTextCheckingResults</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextViewTextCheckingResults : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextViewTextCheckingResults (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSTextCheckingResult[] Invoke (NSTextView textView, Foundation.NSTextCheckingResult[] candidates, Foundation.NSRange selectedRange);</span>
}
</pre>
</div> <!-- end type NSTextViewTextCheckingResults -->
<div> <!-- start type NSTextViewUpdateTouchBarItemIdentifiers -->
<h3>New Type AppKit.NSTextViewUpdateTouchBarItemIdentifiers</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTextViewUpdateTouchBarItemIdentifiers : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTextViewUpdateTouchBarItemIdentifiers (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTextView textView, string[] identifiers, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] Invoke (NSTextView textView, string[] identifiers);</span>
}
</pre>
</div> <!-- end type NSTextViewUpdateTouchBarItemIdentifiers -->
<div> <!-- start type NSTouchBar -->
<h3>New Type AppKit.NSTouchBar</h3>
<pre class='added' data-is-non-breaking="">
public class NSTouchBar : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBar ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBar (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBar (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBar (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] CustomizationAllowedItemIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] CustomizationRequiredItemIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] DefaultItemIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSTouchBarDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSTouchBarMakeItem MakeItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PrincipalItemIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSTouchBarItem&gt; TemplateItems { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Visible { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouchBarItem GetItemForIdentifier (string identifier);</span>
}
</pre>
</div> <!-- end type NSTouchBar -->
<div> <!-- start type NSTouchBarDelegate -->
<h3>New Type AppKit.NSTouchBarDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class NSTouchBarDelegate : Foundation.NSObject, INSTouchBarDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBarDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBarDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBarDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouchBarItem MakeItem (NSTouchBar touchBar, string identifier);</span>
}
</pre>
</div> <!-- end type NSTouchBarDelegate -->
<div> <!-- start type NSTouchBarDelegate_Extensions -->
<h3>New Type AppKit.NSTouchBarDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTouchBarDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchBarItem MakeItem (INSTouchBarDelegate This, NSTouchBar touchBar, string identifier);</span>
}
</pre>
</div> <!-- end type NSTouchBarDelegate_Extensions -->
<div> <!-- start type NSTouchBarItem -->
<h3>New Type AppKit.NSTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public class NSTouchBarItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBarItem (NSTouchBarItemIdentifier identifier);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBarItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSTouchBarItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBarItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomizationLabel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSView View { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSViewController ViewController { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float VisibilityPriority { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Visible { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSTouchBarItem -->
<div> <!-- start type NSTouchBarItemIdentifier -->
<h3>New Type AppKit.NSTouchBarItemIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTouchBarItemIdentifier {
	<span class='added added-field ' data-is-non-breaking="">CharacterPicker = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FixedSpaceLarge = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FixedSpaceSmall = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">FlexibleSpace = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">OtherItemsProxy = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">TextAlignment = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TextColorPicker = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TextFormat = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">TextList = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TextStyle = 6,</span>
}
</pre>
</div> <!-- end type NSTouchBarItemIdentifier -->
<div> <!-- start type NSTouchBarItemIdentifierExtensions -->
<h3>New Type AppKit.NSTouchBarItemIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTouchBarItemIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (NSTouchBarItemIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchBarItemIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type NSTouchBarItemIdentifierExtensions -->
<div> <!-- start type NSTouchBarMakeItem -->
<h3>New Type AppKit.NSTouchBarMakeItem</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTouchBarMakeItem : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchBarMakeItem (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSTouchBar touchBar, string identifier, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouchBarItem EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSTouchBarItem Invoke (NSTouchBar touchBar, string identifier);</span>
}
</pre>
</div> <!-- end type NSTouchBarMakeItem -->
<div> <!-- start type NSTouchEvent -->
<h3>New Type AppKit.NSTouchEvent</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSTouchEvent : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSTouchEvent (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, NSTouch touch, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (NSGestureRecognizer gestureRecognizer, NSTouch touch);</span>
}
</pre>
</div> <!-- end type NSTouchEvent -->
<div> <!-- start type NSTouchType -->
<h3>New Type AppKit.NSTouchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSTouchType {
	<span class='added added-field ' data-is-non-breaking="">Direct = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Indirect = 1,</span>
}
</pre>
</div> <!-- end type NSTouchType -->
<div> <!-- start type NSTouchTypeMask -->
<h3>New Type AppKit.NSTouchTypeMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSTouchTypeMask {
	<span class='added added-field ' data-is-non-breaking="">Direct = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Indirect = 2,</span>
}
</pre>
</div> <!-- end type NSTouchTypeMask -->
<div> <!-- start type NSTouch_NSTouchBar -->
<h3>New Type AppKit.NSTouch_NSTouchBar</h3>
<pre class='added' data-is-non-breaking="">
public static class NSTouch_NSTouchBar {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetLocation (NSTouch This, NSView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetPreviousLocation (NSTouch This, NSView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchType GetTouchType (NSTouch This);</span>
}
</pre>
</div> <!-- end type NSTouch_NSTouchBar -->
<div> <!-- start type NSView_NSCandidateListTouchBarItem -->
<h3>New Type AppKit.NSView_NSCandidateListTouchBarItem</h3>
<pre class='added' data-is-non-breaking="">
public static class NSView_NSCandidateListTouchBarItem {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSCandidateListTouchBarItem GetCandidateListTouchBarItem (NSView This);</span>
}
</pre>
</div> <!-- end type NSView_NSCandidateListTouchBarItem -->
<div> <!-- start type NSView_NSTouchBar -->
<h3>New Type AppKit.NSView_NSTouchBar</h3>
<pre class='added' data-is-non-breaking="">
public static class NSView_NSTouchBar {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSTouchTypeMask GetAllowedTouchTypes (NSView This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAllowedTouchTypes (NSView This, NSTouchTypeMask touchTypes);</span>
}
</pre>
</div> <!-- end type NSView_NSTouchBar -->
<div> <!-- start type NSWindowListOptions -->
<h3>New Type AppKit.NSWindowListOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSWindowListOptions {
	<span class='added added-field ' data-is-non-breaking="">OrderedFrontToBack = 1,</span>
}
</pre>
</div> <!-- end type NSWindowListOptions -->
<div> <!-- start type NSWindowTabbingMode -->
<h3>New Type AppKit.NSWindowTabbingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSWindowTabbingMode {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disallowed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Preferred = 1,</span>
}
</pre>
</div> <!-- end type NSWindowTabbingMode -->
<div> <!-- start type NSWindowUserTabbingPreference -->
<h3>New Type AppKit.NSWindowUserTabbingPreference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSWindowUserTabbingPreference {
	<span class='added added-field ' data-is-non-breaking="">Always = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InFullScreen = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Manual = 0,</span>
}
</pre>
</div> <!-- end type NSWindowUserTabbingPreference -->

</div> <!-- end namespace AppKit -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioQueueStatus --> <div>
<h3>Type Changed: AudioToolbox.AudioQueueStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CannotStartYet = -66665,</span>
</pre>
</div>

</div> <!-- end type AudioQueueStatus -->
<!-- start type AudioServicesError --> <div>
<h3>Type Changed: AudioToolbox.AudioServicesError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SystemSoundExceededMaximumDurationError = -1502,</span>
</pre>
</div>

</div> <!-- end type AudioServicesError -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] ChannelMap { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsMpe { get; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUParameter --> <div>
<h3>Type Changed: AudioUnit.AUParameter</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator, ulong hostTime, AUParameterAutomationEventType eventType);</span>
</pre>
</div>

</div> <!-- end type AUParameter -->
<!-- start type AUParameterNode --> <div>
<h3>Type Changed: AudioUnit.AUParameterNode</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken GetToken (AUParameterAutomationObserver observer);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<!-- start type AUParameterObserverToken --> <div>
<h3>Type Changed: AudioUnit.AUParameterObserverToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AUParameterObserverToken (IntPtr observerToken);</span>
</pre>
</div>

</div> <!-- end type AUParameterObserverToken -->
<!-- start type AudioComponentStatus --> <div>
<h3>Type Changed: AudioUnit.AudioComponentStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">RenderTimeout = -66745,</span>
</pre>
</div>

</div> <!-- end type AudioComponentStatus -->
<!-- start type AudioUnitPropertyIDType --> <div>
<h3>Type Changed: AudioUnit.AudioUnitPropertyIDType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InputAnchorTimeStamp = 3016,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportsMpe = 58,</span>
</pre>
</div>

</div> <!-- end type AudioUnitPropertyIDType -->
<div> <!-- start type AUParameterAutomationEvent -->
<h3>New Type AudioUnit.AUParameterAutomationEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AUParameterAutomationEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ulong Address;</span>
	<span class='added added-field ' data-is-non-breaking="">public AUParameterAutomationEventType EventType;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong HostTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
}
</pre>
</div> <!-- end type AUParameterAutomationEvent -->
<div> <!-- start type AUParameterAutomationEventType -->
<h3>New Type AudioUnit.AUParameterAutomationEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AUParameterAutomationEventType {
	<span class='added added-field ' data-is-non-breaking="">Release = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Touch = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Value = 0,</span>
}
</pre>
</div> <!-- end type AUParameterAutomationEventType -->
<div> <!-- start type AUParameterAutomationObserver -->
<h3>New Type AudioUnit.AUParameterAutomationObserver</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUParameterAutomationObserver : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUParameterAutomationObserver (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ulong address, float value, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (ulong address, float value);</span>
}
</pre>
</div> <!-- end type AUParameterAutomationObserver -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKContainer --> <div>
<h3>Type Changed: CloudKit.CKContainer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CurrentUserDefaultName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabase SharedCloudDatabase { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AcceptShareMetadata (CKShareMetadata metadata, System.Action&lt;CKShare,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShare&gt; AcceptShareMetadataAsync (CKShareMetadata metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverAllIdentities (System.Action&lt;CKUserIdentity[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity[]&gt; DiscoverAllIdentitiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentity (CKRecordID userRecordID, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityAsync (CKRecordID userRecordID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentityWithEmailAddress (string email, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityWithEmailAddressAsync (string email);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentityWithPhoneNumber (string phoneNumber, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityWithPhoneNumberAsync (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareMetadata (Foundation.NSUrl url, System.Action&lt;CKShareMetadata,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareMetadata&gt; FetchShareMetadataAsync (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipant (CKRecordID userRecordID, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantAsync (CKRecordID userRecordID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipantWithEmailAddress (string emailAddress, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantWithEmailAddressAsync (string emailAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipantWithPhoneNumber (string phoneNumber, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantWithPhoneNumberAsync (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CKDatabase GetDatabase (CKDatabaseScope databaseScope);</span>
</pre>
</div>

</div> <!-- end type CKContainer -->
<!-- start type CKDatabase --> <div>
<h3>Type Changed: CloudKit.CKDatabase</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKDatabase -->
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: CloudKit.CKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AlreadyShared = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedAccountRestricted = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">ParticipantMayNeedVerification = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">ReferenceViolation = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">TooManyParticipants = 29,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->
<!-- start type CKNotificationID --> <div>
<h3>Type Changed: CloudKit.CKNotificationID</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This type is not meant to be created by user code")]
	public CKNotificationID ();</span>
</div></pre>

</div> <!-- end type CKNotificationID -->
<!-- start type CKNotificationType --> <div>
<h3>Type Changed: CloudKit.CKNotificationType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Database = 4,</span>
</pre>
</div>

</div> <!-- end type CKNotificationType -->
<!-- start type CKOperation --> <div>
<h3>Type Changed: CloudKit.CKOperation</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForRequest { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForResource { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKOperation -->
<!-- start type CKQueryNotification --> <div>
<h3>Type Changed: CloudKit.CKQueryNotification</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKQueryNotification -->
<!-- start type CKRecord --> <div>
<h3>Type Changed: CloudKit.CKRecord</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKReference Parent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ParentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKReference Share { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ShareKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeShare { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetParent (CKRecord parentRecord);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetParent (CKRecordID parentRecordID);</span>
</pre>
</div>

</div> <!-- end type CKRecord -->
<!-- start type CKRecordZoneCapabilities --> <div>
<h3>Type Changed: CloudKit.CKRecordZoneCapabilities</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Sharing = 4,</span>
</pre>
</div>

</div> <!-- end type CKRecordZoneCapabilities -->
<!-- start type CKRecordZoneNotification --> <div>
<h3>Type Changed: CloudKit.CKRecordZoneNotification</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKRecordZoneNotification -->
<!-- start type CKSubscriptionType --> <div>
<h3>Type Changed: CloudKit.CKSubscriptionType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Database = 3,</span>
</pre>
</div>

</div> <!-- end type CKSubscriptionType -->
<div> <!-- start type CKAcceptPerShareCompletionHandler -->
<h3>New Type CloudKit.CKAcceptPerShareCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKAcceptPerShareCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptPerShareCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKShareMetadata shareMetadata, CKShare acceptedShare, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKShareMetadata shareMetadata, CKShare acceptedShare, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CKAcceptPerShareCompletionHandler -->
<div> <!-- start type CKAcceptSharesOperation -->
<h3>New Type CloudKit.CKAcceptSharesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKAcceptSharesOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptSharesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptSharesOperation (CKShareMetadata[] shareMetadatas);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKAcceptSharesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKAcceptSharesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; AcceptSharesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKAcceptPerShareCompletionHandler PerShareCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareMetadata[] ShareMetadatas { get; set; }</span>
}
</pre>
</div> <!-- end type CKAcceptSharesOperation -->
<div> <!-- start type CKDatabaseNotification -->
<h3>New Type CloudKit.CKDatabaseNotification</h3>
<pre class='added' data-is-non-breaking="">
public class CKDatabaseNotification : CloudKit.CKNotification, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseNotification (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseNotification (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseNotification (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
}
</pre>
</div> <!-- end type CKDatabaseNotification -->
<div> <!-- start type CKDatabaseScope -->
<h3>New Type CloudKit.CKDatabaseScope</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKDatabaseScope {
	<span class='added added-field ' data-is-non-breaking="">Private = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Public = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Shared = 3,</span>
}
</pre>
</div> <!-- end type CKDatabaseScope -->
<div> <!-- start type CKDatabaseSubscription -->
<h3>New Type CloudKit.CKDatabaseSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKDatabaseSubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseSubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseSubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseSubscription (string subscriptionID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKDatabaseSubscription -->
<div> <!-- start type CKDiscoverAllUserIdentitiesOperation -->
<h3>New Type CloudKit.CKDiscoverAllUserIdentitiesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKDiscoverAllUserIdentitiesOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDiscoverAllUserIdentitiesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverAllUserIdentitiesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverAllUserIdentitiesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; Completed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKUserIdentity&gt; Discovered { get; set; }</span>
}
</pre>
</div> <!-- end type CKDiscoverAllUserIdentitiesOperation -->
<div> <!-- start type CKDiscoverUserIdentitiesOperation -->
<h3>New Type CloudKit.CKDiscoverUserIdentitiesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKDiscoverUserIdentitiesOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDiscoverUserIdentitiesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKDiscoverUserIdentitiesOperation (CKUserIdentityLookupInfo[] userIdentityLookupInfos);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverUserIdentitiesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverUserIdentitiesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; Completed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKUserIdentity,CloudKit.CKUserIdentityLookupInfo&gt; Discovered { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo[] UserIdentityLookupInfos { get; set; }</span>
}
</pre>
</div> <!-- end type CKDiscoverUserIdentitiesOperation -->
<div> <!-- start type CKFetchDatabaseChangesCompletionHandler -->
<h3>New Type CloudKit.CKFetchDatabaseChangesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchDatabaseChangesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKServerChangeToken serverChangeToken, bool moreComing, Foundation.NSError operationError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKServerChangeToken serverChangeToken, bool moreComing, Foundation.NSError operationError);</span>
}
</pre>
</div> <!-- end type CKFetchDatabaseChangesCompletionHandler -->
<div> <!-- start type CKFetchDatabaseChangesOperation -->
<h3>New Type CloudKit.CKFetchDatabaseChangesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchDatabaseChangesOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesOperation (CKServerChangeToken previousServerChangeToken);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchDatabaseChangesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchDatabaseChangesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKServerChangeToken&gt; ChangeTokenUpdated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecordZoneID&gt; Changed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchDatabaseChangesCompletionHandler ChangesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FetchAllChanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ResultsLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecordZoneID&gt; WasDeleted { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchDatabaseChangesOperation -->
<div> <!-- start type CKFetchPerShareMetadataHandler -->
<h3>New Type CloudKit.CKFetchPerShareMetadataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchPerShareMetadataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchPerShareMetadataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSUrl shareURL, CKShareMetadata shareMetadata, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSUrl shareURL, CKShareMetadata shareMetadata, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CKFetchPerShareMetadataHandler -->
<div> <!-- start type CKFetchRecordZoneChangesFetchCompletedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesFetchCompletedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesFetchCompletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesFetchCompletedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, bool moreComing, Foundation.NSError recordZoneError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, bool moreComing, Foundation.NSError recordZoneError);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesFetchCompletedHandler -->
<div> <!-- start type CKFetchRecordZoneChangesOperation -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchRecordZoneChangesOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOperation (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOperation (CKRecordZoneID[] recordZoneIDs, Foundation.NSDictionary&lt;CKRecordZoneID,CloudKit.CKFetchRecordZoneChangesOptions&gt; optionsByRecordZoneID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; ChangesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FetchAllChanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesFetchCompletedHandler FetchCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;CKRecordZoneID,CloudKit.CKFetchRecordZoneChangesOptions&gt; OptionsByRecordZoneID { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecord&gt; RecordChanged { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesWithIDWasDeletedHandler RecordWithIDWasDeleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesTokensUpdatedHandler RecordZoneChangeTokensUpdated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID[] RecordZoneIDs { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesOperation -->
<div> <!-- start type CKFetchRecordZoneChangesOptions -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchRecordZoneChangesOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] DesiredKeys { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ResultsLimit { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesOptions -->
<div> <!-- start type CKFetchRecordZoneChangesTokensUpdatedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesTokensUpdatedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesTokensUpdatedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesTokensUpdatedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesTokensUpdatedHandler -->
<div> <!-- start type CKFetchRecordZoneChangesWithIDWasDeletedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesWithIDWasDeletedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesWithIDWasDeletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesWithIDWasDeletedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordID recordID, Foundation.NSString recordType, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordID recordID, Foundation.NSString recordType);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesWithIDWasDeletedHandler -->
<div> <!-- start type CKFetchShareMetadataOperation -->
<h3>New Type CloudKit.CKFetchShareMetadataOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchShareMetadataOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareMetadataOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareMetadataOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareMetadataOperation (Foundation.NSUrl[] shareUrls);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareMetadataOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; FetchShareMetadataCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchPerShareMetadataHandler PerShareMetadata { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] RootRecordDesiredKeys { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl[] ShareUrls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldFetchRootRecord { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchShareMetadataOperation -->
<div> <!-- start type CKFetchShareParticipantsOperation -->
<h3>New Type CloudKit.CKFetchShareParticipantsOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchShareParticipantsOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareParticipantsOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareParticipantsOperation (CKUserIdentityLookupInfo[] userIdentityLookupInfos);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareParticipantsOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareParticipantsOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; Completed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKShareParticipant&gt; Fetched { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo[] UserIdentityLookupInfos { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchShareParticipantsOperation -->
<div> <!-- start type CKFetchWebAuthTokenOperation -->
<h3>New Type CloudKit.CKFetchWebAuthTokenOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchWebAuthTokenOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchWebAuthTokenOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchWebAuthTokenOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchWebAuthTokenOperation (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchWebAuthTokenOperation (string token);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string ApiToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchWebAuthTokenOperationHandler Completed { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchWebAuthTokenOperation -->
<div> <!-- start type CKFetchWebAuthTokenOperationHandler -->
<h3>New Type CloudKit.CKFetchWebAuthTokenOperationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchWebAuthTokenOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchWebAuthTokenOperationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string webAuthToken, Foundation.NSError operationError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string webAuthToken, Foundation.NSError operationError);</span>
}
</pre>
</div> <!-- end type CKFetchWebAuthTokenOperationHandler -->
<div> <!-- start type CKQuerySubscription -->
<h3>New Type CloudKit.CKQuerySubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKQuerySubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKQuerySubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKQuerySubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (string recordType, Foundation.NSPredicate predicate, CKQuerySubscriptionOptions querySubscriptionOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (string recordType, Foundation.NSPredicate predicate, string subscriptionID, CKQuerySubscriptionOptions querySubscriptionOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKQuerySubscriptionOptions SubscriptionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID ZoneID { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKQuerySubscription -->
<div> <!-- start type CKQuerySubscriptionOptions -->
<h3>New Type CloudKit.CKQuerySubscriptionOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKQuerySubscriptionOptions {
	<span class='added added-field ' data-is-non-breaking="">FiresOnce = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordCreation = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordDeletion = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordUpdate = 2,</span>
}
</pre>
</div> <!-- end type CKQuerySubscriptionOptions -->
<div> <!-- start type CKRecordZoneSubscription -->
<h3>New Type CloudKit.CKRecordZoneSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKRecordZoneSubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (CKRecordZoneID zoneID);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKRecordZoneSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKRecordZoneSubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (CKRecordZoneID zoneID, string subscriptionID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID ZoneID { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKRecordZoneSubscription -->
<div> <!-- start type CKShare -->
<h3>New Type CloudKit.CKShare</h3>
<pre class='added' data-is-non-breaking="">
public class CKShare : CloudKit.CKRecord, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (CKRecord rootRecord);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShare (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShare (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (CKRecord rootRecord, CKRecordID shareID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant CurrentUser { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant Owner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant[] Participants { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission PublicPermission { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (CKShareParticipant participant);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (CKShareParticipant participant);</span>
}
</pre>
</div> <!-- end type CKShare -->
<div> <!-- start type CKShareKeys -->
<h3>New Type CloudKit.CKShareKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class CKShareKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImageData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Type { get; }</span>
}
</pre>
</div> <!-- end type CKShareKeys -->
<div> <!-- start type CKShareMetadata -->
<h3>New Type CloudKit.CKShareMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class CKShareMetadata : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareMetadata (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareMetadata (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareMetadata (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContainerIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentity OwnerIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission Permission { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecord RootRecord { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID RootRecordID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShare Share { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantAcceptanceStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKShareMetadata -->
<div> <!-- start type CKShareParticipant -->
<h3>New Type CloudKit.CKShareParticipant</h3>
<pre class='added' data-is-non-breaking="">
public class CKShareParticipant : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareParticipant (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareParticipant (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareParticipant (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantAcceptanceStatus AcceptanceStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission Permission { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantType Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentity UserIdentity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKShareParticipant -->
<div> <!-- start type CKShareParticipantAcceptanceStatus -->
<h3>New Type CloudKit.CKShareParticipantAcceptanceStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantAcceptanceStatus {
	<span class='added added-field ' data-is-non-breaking="">Accepted = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Pending = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Removed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantAcceptanceStatus -->
<div> <!-- start type CKShareParticipantPermission -->
<h3>New Type CloudKit.CKShareParticipantPermission</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantPermission {
	<span class='added added-field ' data-is-non-breaking="">None = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnly = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWrite = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantPermission -->
<div> <!-- start type CKShareParticipantType -->
<h3>New Type CloudKit.CKShareParticipantType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantType {
	<span class='added added-field ' data-is-non-breaking="">Owner = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PrivateUser = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">PublicUser = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantType -->
<div> <!-- start type CKUserIdentity -->
<h3>New Type CloudKit.CKUserIdentity</h3>
<pre class='added' data-is-non-breaking="">
public class CKUserIdentity : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentity (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasICloudAccount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo LookupInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPersonNameComponents NameComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID UserRecordID { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKUserIdentity -->
<div> <!-- start type CKUserIdentityLookupInfo -->
<h3>New Type CloudKit.CKUserIdentityLookupInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CKUserIdentityLookupInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentityLookupInfo (CKRecordID userRecordID);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentityLookupInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentityLookupInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentityLookupInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EmailAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PhoneNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID UserRecordID { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo FromEmail (string email);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo FromPhoneNumber (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfos (CKRecordID[] recordIDs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfosWithEmails (string[] emails);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfosWithPhoneNumbers (string[] phoneNumbers);</span>
}
</pre>
</div> <!-- end type CKUserIdentityLookupInfo -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContact --> <div>
<h3>Type Changed: Contacts.CNContact</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ImageDataAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PhoneticOrganizationName { get; }</span>
</pre>
</div>

</div> <!-- end type CNContact -->
<!-- start type CNContactFetchRequest --> <div>
<h3>Type Changed: Contacts.CNContactFetchRequest</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CNContactFetchRequest (Foundation.NSCoder coder);</span>
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

</div> <!-- end type CNContactFetchRequest -->
<!-- start type CNContactKey --> <div>
<h3>Type Changed: Contacts.CNContactKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageDataAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhoneticOrganizationName { get; }</span>
</pre>
</div>

</div> <!-- end type CNContactKey -->
<!-- start type CNMutableContact --> <div>
<h3>Type Changed: Contacts.CNMutableContact</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PhoneticOrganizationName { get; set; }</span>
</pre>
</div>

</div> <!-- end type CNMutableContact -->

</div> <!-- end namespace Contacts -->
<!-- start namespace ContactsUI --> <div> 
<h2>Namespace ContactsUI</h2>
<!-- start type CNContactViewController --> <div>
<h3>Type Changed: ContactsUI.CNContactViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type CNContactViewController -->

</div> <!-- end namespace ContactsUI -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnimationDiscrete { get; }</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SimpleAttractor { get; }</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CAContentsFormat ContentsFormat { get; set; }</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CALayerDelegate --> <div>
<h3>Type Changed: CoreAnimation.CALayerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillDrawLayer (CALayer layer);</span>
</pre>
</div>

</div> <!-- end type CALayerDelegate -->
<!-- start type CALayerDelegate_Extensions --> <div>
<h3>Type Changed: CoreAnimation.CALayerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void WillDrawLayer (ICALayerDelegate This, CALayer layer);</span>
</pre>
</div>

</div> <!-- end type CALayerDelegate_Extensions -->
<!-- start type CATransform3D --> <div>
<h3>Type Changed: CoreAnimation.CATransform3D</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use Invert() as the argument to this method is unused.")]
	public CATransform3D Invert (CATransform3D t);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CATransform3D Invert ();</span>
</pre>
</div>

</div> <!-- end type CATransform3D -->
<div> <!-- start type CAContentsFormat -->
<h3>New Type CoreAnimation.CAContentsFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CAContentsFormat {
	<span class='added added-field ' data-is-non-breaking="">Gray8Uint = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba16Float = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8Uint = 1,</span>
}
</pre>
</div> <!-- end type CAContentsFormat -->
<div> <!-- start type CAContentsFormatExtensions -->
<h3>New Type CoreAnimation.CAContentsFormatExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CAContentsFormatExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CAContentsFormat self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CAContentsFormat GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CAContentsFormatExtensions -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreAudioKit --> <div> 
<h2>Namespace CoreAudioKit</h2>
<!-- start type AUViewController --> <div>
<h3>Type Changed: CoreAudioKit.AUViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type AUViewController -->

</div> <!-- end namespace CoreAudioKit -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBPeripheral --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheral</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetMaximumWriteValueLength (CBCharacteristicWriteType type);</span>
</pre>
</div>

</div> <!-- end type CBPeripheral -->
<!-- start type CBPeripheralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManager</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManager ();</span>
</pre>
</div>

</div> <!-- end type CBPeripheralManager -->
<!-- start type CBUUID --> <div>
<h3>Type Changed: CoreBluetooth.CBUUID</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicValidRangeString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Uuid { get; }</span>
</pre>
</div>

</div> <!-- end type CBUUID -->
<div> <!-- start type CBManagerState -->
<h3>New Type CoreBluetooth.CBManagerState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBManagerState {
	<span class='added added-field ' data-is-non-breaking="">PoweredOff = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PoweredOn = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Resetting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unauthorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 2,</span>
}
</pre>
</div> <!-- end type CBManagerState -->

</div> <!-- end namespace CoreBluetooth -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSEntityMappingType --> <div>
<h3>Type Changed: CoreData.NSEntityMappingType</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	Copy = <span class='removed removed-inline removed-breaking-inline'>5</span> <span class='added '>4</span>
</div><div data-is-breaking="">	Transform = <span class='removed removed-inline removed-breaking-inline'>6</span> <span class='added '>5</span>
</div></pre>

</div> <!-- end type NSEntityMappingType -->
<!-- start type NSFetchRequest --> <div>
<h3>Type Changed: CoreData.NSFetchRequest</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual INSFetchRequestResult[] Execute (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSFetchRequest -->
<!-- start type NSIncrementalStore --> <div>
<h3>Type Changed: CoreData.NSIncrementalStore</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public Foundation.NSObject IdentifierForNewStoreAtURL (Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>storeURL</span> <span class='added '>storeUrl</span>)
</div></pre>

</div> <!-- end type NSIncrementalStore -->
<!-- start type NSManagedObject --> <div>
<h3>Type Changed: CoreData.NSManagedObject</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSManagedObject (NSManagedObjectContext moc);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool ContextShouldIgnoreUnModeledPropertyChanges { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AwakeFromSnapshotEvents (NSSnapshotEventType flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSFetchRequest CreateFetchRequest ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSEntityDescription GetEntityDescription ();</span>
</pre>
</div>

</div> <!-- end type NSManagedObject -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyMergesChangesFromParent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSQueryGenerationToken QueryGenerationToken { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetQueryGenerationFromToken (NSQueryGenerationToken generation, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSManagedObjectID --> <div>
<h3>Type Changed: CoreData.NSManagedObjectID</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectID -->
<!-- start type NSMergePolicy --> <div>
<h3>Type Changed: CoreData.NSMergePolicy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy ErrorPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy MergeByPropertyObjectTrumpPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy MergeByPropertyStoreTrumpPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy OverwritePolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy RollbackPolicy { get; }</span>
</pre>
</div>

</div> <!-- end type NSMergePolicy -->
<!-- start type NSMigrationManager --> <div>
<h3>Type Changed: CoreData.NSMigrationManager</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual bool MigrateStoreFromUrl (Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>sourceURL</span> <span class='added '>sourceUrl</span>, string sStoreType, Foundation.NSDictionary sOptions, NSMappingModel mappings, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>dURL</span> <span class='added '>dUrl</span>, string dStoreType, Foundation.NSDictionary dOptions, out Foundation.NSError error)
</div></pre>

</div> <!-- end type NSMigrationManager -->
<!-- start type NSPersistentStore --> <div>
<h3>Type Changed: CoreData.NSPersistentStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool LoadMetadata (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStore -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual NSPersistentStore AddPersistentStoreWithType (Foundation.NSString storeType, string configuration, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>storeURL</span> <span class='added '>storeUrl</span>, Foundation.NSDictionary options, out Foundation.NSError error)
</div><div data-is-breaking="">	public virtual NSPersistentStore MigratePersistentStore (NSPersistentStore store, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>URL</span> <span class='added '>url</span>, Foundation.NSDictionary options, Foundation.NSString storeType, out Foundation.NSError error)
</div><div data-is-breaking="">	public virtual NSPersistentStore PersistentStoreForUrl (Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>URL</span> <span class='added '>url</span>)
</div><div data-is-breaking="">	public virtual bool ReplacePersistentStore (Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>destinationURL</span> <span class='added '>destinationUrl</span>, Foundation.NSDictionary destinationOptions, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>sourceURL</span> <span class='added '>sourceUrl</span>, Foundation.NSDictionary sourceOptions, string storeType, out Foundation.NSError error)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddPersistentStore (NSPersistentStoreDescription storeDescription, System.Action&lt;NSPersistentStoreDescription,Foundation.NSError&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSPersistentStoreDescription&gt; AddPersistentStoreAsync (NSPersistentStoreDescription storeDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; GetMetadata (string storeType, Foundation.NSUrl url, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool SetMetadata (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; metadata, string storeType, Foundation.NSUrl url, Foundation.NSDictionary options, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<div> <!-- start type INSFetchRequestResult -->
<h3>New Type CoreData.INSFetchRequestResult</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFetchRequestResult : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSFetchRequestResult -->
<div> <!-- start type MigrationErrorType -->
<h3>New Type CoreData.MigrationErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MigrationErrorType {
	<span class='added added-field ' data-is-non-breaking="">EntityMigrationPolicy = 134170,</span>
	<span class='added added-field ' data-is-non-breaking="">ExternalRecordImport = 134200,</span>
	<span class='added added-field ' data-is-non-breaking="">InferredMappingModel = 134190,</span>
	<span class='added added-field ' data-is-non-breaking="">Migration = 134110,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationCancelled = 134120,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationManagerDestinationStore = 134160,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationManagerSourceStore = 134150,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationMissingMappingModel = 134140,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationMissingSourceModel = 134130,</span>
}
</pre>
</div> <!-- end type MigrationErrorType -->
<div> <!-- start type NSPersistentContainer -->
<h3>New Type CoreData.NSPersistentContainer</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentContainer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentContainer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentContainer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentContainer (string name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentContainer (string name, NSManagedObjectModel model);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSUrl DefaultDirectoryUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectModel ManagedObjectModel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectContext NewBackgroundContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentStoreCoordinator PersistentStoreCoordinator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentStoreDescription[] PersistentStoreDescriptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectContext ViewContext { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentContainer GetPersistentContainer (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentContainer GetPersistentContainer (string name, NSManagedObjectModel model);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadPersistentStores (System.Action&lt;NSPersistentStoreDescription,Foundation.NSError&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSPersistentStoreDescription&gt; LoadPersistentStoresAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (System.Action&lt;NSManagedObjectContext&gt; block);</span>
}
</pre>
</div> <!-- end type NSPersistentContainer -->
<div> <!-- start type NSPersistentStoreDescription -->
<h3>New Type CoreData.NSPersistentStoreDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentStoreDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentStoreDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentStoreDescription (Foundation.NSUrl url);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentStoreDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Configuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; Options { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldAddStoreAsynchronously { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldInferMappingModelAutomatically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldMigrateStoreAutomatically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; SqlitePragmas { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Timeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentStoreDescription GetPersistentStoreDescription (Foundation.NSUrl Url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetOption (Foundation.NSObject option, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (Foundation.NSObject value, string name);</span>
}
</pre>
</div> <!-- end type NSPersistentStoreDescription -->
<div> <!-- start type NSQueryGenerationToken -->
<h3>New Type CoreData.NSQueryGenerationToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSQueryGenerationToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSQueryGenerationToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSQueryGenerationToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSQueryGenerationToken CurrentToken { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSQueryGenerationToken -->
<div> <!-- start type ObjectGraphManagementErrorType -->
<h3>New Type CoreData.ObjectGraphManagementErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ObjectGraphManagementErrorType {
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectContextLocking = 132000,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectExternalRelationship = 133010,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectMerge = 133020,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectReferentialIntegrity = 133000,</span>
	<span class='added added-field ' data-is-non-breaking="">PersistentStoreCoordinatorLocking = 132010,</span>
}
</pre>
</div> <!-- end type ObjectGraphManagementErrorType -->
<div> <!-- start type PersistentStoreErrorType -->
<h3>New Type CoreData.PersistentStoreErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PersistentStoreErrorType {
	<span class='added added-field ' data-is-non-breaking="">IncompatibleSchema = 134020,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleVersionHash = 134100,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompleteSave = 134040,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidType = 134000,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 134080,</span>
	<span class='added added-field ' data-is-non-breaking="">Operation = 134070,</span>
	<span class='added added-field ' data-is-non-breaking="">Save = 134030,</span>
	<span class='added added-field ' data-is-non-breaking="">SaveConflicts = 134050,</span>
	<span class='added added-field ' data-is-non-breaking="">Timeout = 134090,</span>
	<span class='added added-field ' data-is-non-breaking="">TypeMismatch = 134010,</span>
}
</pre>
</div> <!-- end type PersistentStoreErrorType -->
<div> <!-- start type UserInfo -->
<h3>New Type CoreData.UserInfo</h3>
<pre class='added' data-is-non-breaking="">
public class UserInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UserInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UserInfo (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NSPersistentStore[] AffectedStoresForError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError[] DetailedErrors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString KeyForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSManagedObject ObjectForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSMergeConflict[] PersistentStoreSaveConflicts { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSPredicate PredicateForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSValue ValueForValidationError { get; set; }</span>
}
</pre>
</div> <!-- end type UserInfo -->
<div> <!-- start type UserInfoKeys -->
<h3>New Type CoreData.UserInfoKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class UserInfoKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AffectedStoresForErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DetailedErrorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ObjectForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PersistentStoreSaveConflictsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PredicateForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueForValidationErrorKey { get; }</span>
}
</pre>
</div> <!-- end type UserInfoKeys -->
<div> <!-- start type ValidationErrorType -->
<h3>New Type CoreData.ValidationErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ValidationErrorType {
	<span class='added added-field ' data-is-non-breaking="">DateTooLate = 1630,</span>
	<span class='added added-field ' data-is-non-breaking="">DateTooSoon = 1640,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDate = 1650,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectValidation = 1550,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingMandatoryProperty = 1570,</span>
	<span class='added added-field ' data-is-non-breaking="">MultipleErrors = 1560,</span>
	<span class='added added-field ' data-is-non-breaking="">NumberTooLarge = 1610,</span>
	<span class='added added-field ' data-is-non-breaking="">NumberTooSmall = 1620,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipDeniedDelete = 1600,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipExceedsMaximumCount = 1590,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipLacksMinimumCount = 1580,</span>
	<span class='added added-field ' data-is-non-breaking="">StringPatternMatching = 1680,</span>
	<span class='added added-field ' data-is-non-breaking="">StringTooLong = 1660,</span>
	<span class='added added-field ' data-is-non-breaking="">StringTooShort = 1670,</span>
}
</pre>
</div> <!-- end type ValidationErrorType -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGColorSpace --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsWideGamutRgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsOutput { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetIccData ();</span>
</pre>
</div>

</div> <!-- end type CGColorSpace -->
<!-- start type CGColorSpaceNames --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpaceNames</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedLinearGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedLinearSrgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedSrgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LinearGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LinearSrgb { get; }</span>
</pre>
</div>

</div> <!-- end type CGColorSpaceNames -->
<div> <!-- start type CGColorConversionInfo -->
<h3>New Type CoreGraphics.CGColorConversionInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGColorConversionInfo : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (CGColorConversionOptions options, GColorConversionInfoTriple[] triples);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (CGColorSpace src, CGColorSpace dst);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (Foundation.NSDictionary options, GColorConversionInfoTriple[] triples);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~CGColorConversionInfo ();</span>
}
</pre>
</div> <!-- end type CGColorConversionInfo -->
<div> <!-- start type CGColorConversionInfoTransformType -->
<h3>New Type CoreGraphics.CGColorConversionInfoTransformType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGColorConversionInfoTransformType {
	<span class='added added-field ' data-is-non-breaking="">ApplySpace = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FromSpace = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ToSpace = 1,</span>
}
</pre>
</div> <!-- end type CGColorConversionInfoTransformType -->
<div> <!-- start type CGColorConversionOptions -->
<h3>New Type CoreGraphics.CGColorConversionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CGColorConversionOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? BlackPointCompensation { get; set; }</span>
}
</pre>
</div> <!-- end type CGColorConversionOptions -->
<div> <!-- start type GColorConversionInfoTriple -->
<h3>New Type CoreGraphics.GColorConversionInfoTriple</h3>
<pre class='added' data-is-non-breaking="">
public struct GColorConversionInfoTriple {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CGColorRenderingIntent Intent;</span>
	<span class='added added-field ' data-is-non-breaking="">public CGColorSpace Space;</span>
	<span class='added added-field ' data-is-non-breaking="">public CGColorConversionInfoTransformType Transform;</span>
}
</pre>
</div> <!-- end type GColorConversionInfoTriple -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIColor --> <div>
<h3>Type Changed: CoreImage.CIColor</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColor (nfloat red, nfloat green, nfloat blue, CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColor (nfloat red, nfloat green, nfloat blue, nfloat alpha, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor BlackColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor BlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor ClearColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor CyanColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor GrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor GreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor MagentaColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor RedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor WhiteColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor YellowColor { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIColor FromRgb (nfloat red, nfloat green, nfloat blue, CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIColor FromRgba (nfloat red, nfloat green, nfloat blue, nfloat alpha, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIColor -->
<!-- start type CIContext --> <div>
<h3>Type Changed: CoreImage.CIContext</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIContext (CIContextOptions options);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat WorkingFormat { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGImage CreateCGImage (CIImage image, CoreGraphics.CGRect fromRect, CIFormat format, CoreGraphics.CGColorSpace colorSpace, bool deferred);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CIImage image, CoreVideo.CVPixelBuffer buffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CIImage image, CoreVideo.CVPixelBuffer buffer, CoreGraphics.CGRect rectangle, CoreGraphics.CGColorSpace cs);</span>
</pre>
</div>

</div> <!-- end type CIContext -->
<!-- start type CIContextOptions --> <div>
<h3>Type Changed: CoreImage.CIContextOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? CacheIntermediates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? OutputPremultiplied { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIContextOptions -->
<!-- start type CIDetectorOptions --> <div>
<h3>Type Changed: CoreImage.CIDetectorOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int? MaxFeatureCount { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIDetectorOptions -->
<!-- start type CIFilter --> <div>
<h3>Type Changed: CoreImage.CIFilter</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSData data, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSData data, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSUrl url, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSUrl url, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary properties, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary properties, Foundation.NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type CIFilter -->
<!-- start type CIFilterGenerator --> <div>
<h3>Type Changed: CoreImage.CIFilterGenerator</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICIFilterConstructor</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIFilter FilterWithName (string name);</span>
</pre>
</div>

</div> <!-- end type CIFilterGenerator -->
<!-- start type CIImage --> <div>
<h3>Type Changed: CoreImage.CIImage</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (CoreVideo.CVPixelBuffer buffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (CoreVideo.CVPixelBuffer buffer, CIImageInitializationOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImage (CoreVideo.CVPixelBuffer buffer, Foundation.NSDictionary dict);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGImage CGImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGColorSpace ColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByApplyingGaussianBlur (double sigma);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByClamping (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByColorMatchingColorSpaceToWorkingSpace (CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByColorMatchingWorkingSpaceToColorSpace (CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByPremultiplyingAlpha ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateBySettingAlphaOne (CoreGraphics.CGRect extent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateBySettingProperties (Foundation.NSDictionary properties);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByUnpremultiplyingAlpha ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGRect GetRegionOfInterest (CIImage im, CoreGraphics.CGRect r);</span>
</pre>
</div>

</div> <!-- end type CIImage -->
<!-- start type CIVector --> <div>
<h3>Type Changed: CoreImage.CIVector</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AffineTransform { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint Point { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Rectangle { get; }</span>
</pre>
</div>

</div> <!-- end type CIVector -->
<div> <!-- start type CIClamp -->
<h3>New Type CoreImage.CIClamp</h3>
<pre class='added' data-is-non-breaking="">
public class CIClamp : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIClamp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIClamp (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIClamp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIClamp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Extent { get; set; }</span>
}
</pre>
</div> <!-- end type CIClamp -->
<div> <!-- start type CIContext_ImageRepresentation -->
<h3>New Type CoreImage.CIContext_ImageRepresentation</h3>
<pre class='added' data-is-non-breaking="">
public static class CIContext_ImageRepresentation {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetJpegRepresentation (CIContext This, CIImage image, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetTiffRepresentation (CIContext This, CIImage image, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteJpegRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteTiffRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIContext_ImageRepresentation -->
<div> <!-- start type CIHueSaturationValueGradient -->
<h3>New Type CoreImage.CIHueSaturationValueGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIHueSaturationValueGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIHueSaturationValueGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIHueSaturationValueGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIHueSaturationValueGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIHueSaturationValueGradient (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Dither { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Softness { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Value { get; set; }</span>
}
</pre>
</div> <!-- end type CIHueSaturationValueGradient -->
<div> <!-- start type CIImageProcessorKernel -->
<h3>New Type CoreImage.CIImageProcessorKernel</h3>
<pre class='added' data-is-non-breaking="">
public class CIImageProcessorKernel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageProcessorKernel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageProcessorKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageProcessorKernel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIFormat OutputFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SynchronizeInputs { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIImage Apply (CoreGraphics.CGRect extent, CIImage[] inputs, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; args, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFormat GetFormat (int input);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetRegionOfInterest (int input, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; arguments, CoreGraphics.CGRect outputRect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Process (ICIImageProcessorInput[] inputs, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; arguments, ICIImageProcessorOutput output, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIImageProcessorKernel -->
<div> <!-- start type CINinePartStretched -->
<h3>New Type CoreImage.CINinePartStretched</h3>
<pre class='added' data-is-non-breaking="">
public class CINinePartStretched : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartStretched ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartStretched (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartStretched (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartStretched (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector GrowAmount { get; set; }</span>
}
</pre>
</div> <!-- end type CINinePartStretched -->
<div> <!-- start type CINinePartTiled -->
<h3>New Type CoreImage.CINinePartTiled</h3>
<pre class='added' data-is-non-breaking="">
public class CINinePartTiled : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartTiled ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartTiled (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartTiled (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartTiled (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FlipYTiles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector GrowAmount { get; set; }</span>
}
</pre>
</div> <!-- end type CINinePartTiled -->
<div> <!-- start type CIQRCodeFeature -->
<h3>New Type CoreImage.CIQRCodeFeature</h3>
<pre class='added' data-is-non-breaking="">
public class CIQRCodeFeature : CoreImage.CIFeature, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIQRCodeFeature (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIQRCodeFeature (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string MessageString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
}
</pre>
</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIRawFilterOptions -->
<h3>New Type CoreImage.CIRawFilterOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CIRawFilterOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIRawFilterOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRawFilterOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSSet ActiveKeys { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AllowDraftMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? BaselineExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? Boost { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? BoostShadowAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ColorNoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? DisableGamutMap { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableChromaticNoiseTracking { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableSharpening { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableVendorLensCorrection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IgnoreImageOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ImageOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIFilter LinearSpaceFilter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? LuminanceNoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralChromaticityX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralChromaticityY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector NeutralLocation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralTemperature { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralTint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionContrastAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionDetailAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionSharpnessAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector OutputNativeSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? ScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary[] SupportedDecoderVersions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Version { get; set; }</span>
}
</pre>
</div> <!-- end type CIRawFilterOptions -->
<div> <!-- start type CITextFeature -->
<h3>New Type CoreImage.CITextFeature</h3>
<pre class='added' data-is-non-breaking="">
public class CITextFeature : CoreImage.CIFeature, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextFeature ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextFeature (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextFeature (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFeature[] SubFeatures { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
}
</pre>
</div> <!-- end type CITextFeature -->
<div> <!-- start type CIThermal -->
<h3>New Type CoreImage.CIThermal</h3>
<pre class='added' data-is-non-breaking="">
public class CIThermal : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIThermal ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIThermal (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIThermal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIThermal (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIThermal -->
<div> <!-- start type CIXRay -->
<h3>New Type CoreImage.CIXRay</h3>
<pre class='added' data-is-non-breaking="">
public class CIXRay : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIXRay ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIXRay (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIXRay (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIXRay (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIXRay -->
<div> <!-- start type ICIImageProcessorInput -->
<h3>New Type CoreImage.ICIImageProcessorInput</h3>
<pre class='added' data-is-non-breaking="">
public interface ICIImageProcessorInput : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture MetalTexture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Region { get; }</span>
}
</pre>
</div> <!-- end type ICIImageProcessorInput -->
<div> <!-- start type ICIImageProcessorOutput -->
<h3>New Type CoreImage.ICIImageProcessorOutput</h3>
<pre class='added' data-is-non-breaking="">
public interface ICIImageProcessorOutput : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLCommandBuffer MetalCommandBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture MetalTexture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Region { get; }</span>
}
</pre>
</div> <!-- end type ICIImageProcessorOutput -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLHeading --> <div>
<h3>Type Changed: CoreLocation.CLHeading</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the Description property from NSObject")]
	public virtual string Description ();</span>
</div></pre>

</div> <!-- end type CLHeading -->
<!-- start type CLLocation --> <div>
<h3>Type Changed: CoreLocation.CLLocation</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the Description property from NSObject")]
	public virtual string Description ();</span>
</div></pre>

</div> <!-- end type CLLocation -->
<!-- start type CLLocationManager --> <div>
<h3>Type Changed: CoreLocation.CLLocationManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool DeferredLocationUpdatesAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool HeadingAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double MaximumRegionMonitoringDistance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet MonitoredRegions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Purpose { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool RegionMonitoringAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool RegionMonitoringEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SignificantLocationChangeMonitoringAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CLAuthorizationStatus Status { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CLRegionStateDeterminedEventArgs&gt; DidDetermineState;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; DidStartMonitoringForRegion;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CLRegionErrorEventArgs&gt; MonitoringFailed;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; RegionEntered;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CLRegionEventArgs&gt; RegionLeft;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsMonitoringAvailable (ObjCRuntime.Class regionClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestState (CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartMonitoring (CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartMonitoringSignificantLocationChanges ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopMonitoring (CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopMonitoringSignificantLocationChanges ();</span>
</pre>
</div>

</div> <!-- end type CLLocationManager -->
<!-- start type CLLocationManagerDelegate --> <div>
<h3>Type Changed: CoreLocation.CLLocationManagerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDetermineState (CLLocationManager manager, CLRegionState state, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStartMonitoringForRegion (CLLocationManager manager, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MonitoringFailed (CLLocationManager manager, CLRegion region, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegionEntered (CLLocationManager manager, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegionLeft (CLLocationManager manager, CLRegion region);</span>
</pre>
</div>

</div> <!-- end type CLLocationManagerDelegate -->
<!-- start type CLLocationManagerDelegate_Extensions --> <div>
<h3>Type Changed: CoreLocation.CLLocationManagerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidDetermineState (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegionState state, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStartMonitoringForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MonitoringFailed (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RegionEntered (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RegionLeft (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);</span>
</pre>
</div>

</div> <!-- end type CLLocationManagerDelegate_Extensions -->
<div> <!-- start type CLCircularRegion -->
<h3>New Type CoreLocation.CLCircularRegion</h3>
<pre class='added' data-is-non-breaking="">
public class CLCircularRegion : CoreLocation.CLRegion, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLCircularRegion (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CLCircularRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CLCircularRegion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CLCircularRegion (CLLocationCoordinate2D center, double radius, string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CLLocationCoordinate2D Center { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Radius { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ContainsCoordinate (CLLocationCoordinate2D coordinate);</span>
}
</pre>
</div> <!-- end type CLCircularRegion -->
<div> <!-- start type CLGeocodeCompletionHandler -->
<h3>New Type CoreLocation.CLGeocodeCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CLGeocodeCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLGeocodeCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CLPlacemark[] placemarks, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CLPlacemark[] placemarks, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CLGeocodeCompletionHandler -->
<div> <!-- start type CLGeocoder -->
<h3>New Type CoreLocation.CLGeocoder</h3>
<pre class='added' data-is-non-breaking="">
public class CLGeocoder : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLGeocoder ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CLGeocoder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CLGeocoder (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Geocoding { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelGeocode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (Foundation.NSDictionary addressDictionary, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (Foundation.NSDictionary addressDictionary);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location);</span>
}
</pre>
</div> <!-- end type CLGeocoder -->
<div> <!-- start type CLRegionErrorEventArgs -->
<h3>New Type CoreLocation.CLRegionErrorEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CLRegionErrorEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLRegionErrorEventArgs (CLRegion region, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CLRegion Region { get; set; }</span>
}
</pre>
</div> <!-- end type CLRegionErrorEventArgs -->
<div> <!-- start type CLRegionEventArgs -->
<h3>New Type CoreLocation.CLRegionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CLRegionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLRegionEventArgs (CLRegion region);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CLRegion Region { get; set; }</span>
}
</pre>
</div> <!-- end type CLRegionEventArgs -->
<div> <!-- start type CLRegionStateDeterminedEventArgs -->
<h3>New Type CoreLocation.CLRegionStateDeterminedEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CLRegionStateDeterminedEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CLRegionStateDeterminedEventArgs (CLRegionState state, CLRegion region);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CLRegion Region { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CLRegionState State { get; set; }</span>
}
</pre>
</div> <!-- end type CLRegionStateDeterminedEventArgs -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreText --> <div> 
<h2>Namespace CoreText</h2>
<!-- start type CTStringAttributeKey --> <div>
<h3>Type Changed: CoreText.CTStringAttributeKey</h3>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BackgroundColor;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString HorizontalInVerticalForms;</span>
</pre>
</div>

</div> <!-- end type CTStringAttributeKey -->
<!-- start type CTStringAttributes --> <div>
<h3>Type Changed: CoreText.CTStringAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? HorizontalInVerticalForms { get; set; }</span>
</pre>
</div>

</div> <!-- end type CTStringAttributes -->

</div> <!-- end namespace CoreText -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVImageBuffer --> <div>
<h3>Type Changed: CoreVideo.CVImageBuffer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_428_1 { get; }</span>
</pre>
</div>

</div> <!-- end type CVImageBuffer -->
<!-- start type CVPixelBufferPool --> <div>
<h3>Type Changed: CoreVideo.CVPixelBufferPool</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_428_1 { get; }</span>
</pre>
</div>

</div> <!-- end type CVPixelBufferPool -->
<!-- start type CVPixelFormatType --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CV14BayerBggr = 1650943796,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerGbrg = 1734505012,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerGrbg = 1735549492,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerRggb = 1919379252,</span>
	<span class='added added-field ' data-is-non-breaking="">CV30RgbLePackedWideGamut = 1999843442,</span>
</pre>
</div>

</div> <!-- end type CVPixelFormatType -->
<!-- start type CVReturn --> <div>
<h3>Type Changed: CoreVideo.CVReturn</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Retry = -6692,</span>
</pre>
</div>

</div> <!-- end type CVReturn -->
<div> <!-- start type CVPlanarPixelBufferInfo_YCbCrBiPlanar -->
<h3>New Type CoreVideo.CVPlanarPixelBufferInfo_YCbCrBiPlanar</h3>
<pre class='added' data-is-non-breaking="">
public struct CVPlanarPixelBufferInfo_YCbCrBiPlanar {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoCbCr;</span>
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoY;</span>
}
</pre>
</div> <!-- end type CVPlanarPixelBufferInfo_YCbCrBiPlanar -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace CoreWlan --> <div> 
<h2>Namespace CoreWlan</h2>
<div> <!-- start type CWEventDelegate -->
<h3>New Type CoreWlan.CWEventDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class CWEventDelegate : Foundation.NSObject, ICWEventDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CWEventDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CWEventDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CWEventDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BssidDidChangeForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClientConnectionInterrupted ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClientConnectionInvalidated ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CountryCodeDidChangeForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LinkDidChangeForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LinkQualityDidChangeForWiFi (string interfaceName, int rssi, double transmitRate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ModeDidChangeForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PowerStateDidChangeForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScanCacheUpdatedForWiFi (string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SsidDidChangeForWiFi (string interfaceName);</span>
}
</pre>
</div> <!-- end type CWEventDelegate -->
<div> <!-- start type CWEventDelegate_Extensions -->
<h3>New Type CoreWlan.CWEventDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CWEventDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void BssidDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ClientConnectionInterrupted (ICWEventDelegate This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ClientConnectionInvalidated (ICWEventDelegate This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CountryCodeDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LinkDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LinkQualityDidChangeForWiFi (ICWEventDelegate This, string interfaceName, int rssi, double transmitRate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ModeDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PowerStateDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ScanCacheUpdatedForWiFi (ICWEventDelegate This, string interfaceName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SsidDidChangeForWiFi (ICWEventDelegate This, string interfaceName);</span>
}
</pre>
</div> <!-- end type CWEventDelegate_Extensions -->
<div> <!-- start type CWEventType -->
<h3>New Type CoreWlan.CWEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CWEventType {
	<span class='added added-field ' data-is-non-breaking="">BssidDidChange = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">CountryCodeDidChange = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">LinkDidChange = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">LinkQualityDidChange = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ModeDidChange = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PowerDidChange = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RangingReportEvent = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ScanCacheUpdated = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SsidDidChange = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 9223372036854775807,</span>
	<span class='added added-field ' data-is-non-breaking="">VirtualInterfaceStateChanged = 9,</span>
}
</pre>
</div> <!-- end type CWEventType -->
<div> <!-- start type CWWiFiClient -->
<h3>New Type CoreWlan.CWWiFiClient</h3>
<pre class='added' data-is-non-breaking="">
public class CWWiFiClient : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CWWiFiClient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CWWiFiClient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CWWiFiClient (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ICWEventDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string[] InterfaceNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CWInterface[] Interfaces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CWInterface MainInterface { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CWWiFiClient SharedWiFiClient { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CWInterface FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool StartMonitoringEvent (CWEventType type, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool StopMonitoringAllEvents (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool StopMonitoringEvent (CWEventType type, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CWWiFiClient -->
<div> <!-- start type ICWEventDelegate -->
<h3>New Type CoreWlan.ICWEventDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ICWEventDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ICWEventDelegate -->

</div> <!-- end namespace CoreWlan -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type DictionaryContainer --> <div>
<h3>Type Changed: Foundation.DictionaryContainer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGPoint? GetCGPointValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGRect? GetCGRectValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGSize? GetCGSizeValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreMedia.CMTime? GetCMTimeValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGPointValue (NSString key, CoreGraphics.CGPoint? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGRectValue (NSString key, CoreGraphics.CGRect? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGSizeValue (NSString key, CoreGraphics.CGSize? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCMTimeValue (NSString key, CoreMedia.CMTime? value);</span>
</pre>
</div>

</div> <!-- end type DictionaryContainer -->
<!-- start type NSArray --> <div>
<h3>Type Changed: Foundation.NSArray</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static T[] EnumsFromHandle&lt;T&gt; (IntPtr handle);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSCharacterSet --> <div>
<h3>Type Changed: Foundation.NSCharacterSet</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSCharacterSet -->
<!-- start type NSCocoaError --> <div>
<h3>Type Changed: Foundation.NSCocoaError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CloudSharingConflictError = 5123,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingErrorMaximum = 5375,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingErrorMinimum = 5120,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingNetworkFailureError = 5120,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingNoPermissionError = 5124,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingOtherError = 5375,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingQuotaExceededError = 5121,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingTooManyParticipantsError = 5122,</span>
</pre>
</div>

</div> <!-- end type NSCocoaError -->
<!-- start type NSCoder --> <div>
<h3>Type Changed: Foundation.NSCoder</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDecodingFailurePolicy DecodingFailurePolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSError Error { get; }</span>
</pre>
</div>

</div> <!-- end type NSCoder -->
<!-- start type NSDateComponentsFormatterUnitsStyle --> <div>
<h3>Type Changed: Foundation.NSDateComponentsFormatterUnitsStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Brief = 5,</span>
</pre>
</div>

</div> <!-- end type NSDateComponentsFormatterUnitsStyle -->
<!-- start type NSDateIntervalFormatter --> <div>
<h3>Type Changed: Foundation.NSDateIntervalFormatter</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSDateInterval dateInterval);</span>
</pre>
</div>

</div> <!-- end type NSDateIntervalFormatter -->
<!-- start type NSFileHandle --> <div>
<h3>Type Changed: Foundation.NSFileHandle</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AcceptConnectionInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ReadInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ReadToEndOfFileInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void WaitForDataInBackground (NSRunLoopMode[] notifyRunLoopModes);</span>
</pre>
</div>

</div> <!-- end type NSFileHandle -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterCloudKitShare (System.Action&lt;CloudKitRegistrationPreparationHandler&gt; preparationHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterCloudKitShare (CloudKit.CKShare share, CloudKit.CKContainer container);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CloudKitRegistrationPreparationHandler&gt; RegisterCloudKitShareAsync ();</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSKeyedArchiver --> <div>
<h3>Type Changed: Foundation.NSKeyedArchiver</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSKeyedArchiver ();</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSData EncodedData { get; }</span>
</pre>
</div>

</div> <!-- end type NSKeyedArchiver -->
<!-- start type NSLocale --> <div>
<h3>Type Changed: Foundation.NSLocale</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CalendarIdentifier { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetLocalizedCalendarIdentifier (string calendarIdentifier);</span>
</pre>
</div>

</div> <!-- end type NSLocale -->
<!-- start type NSMetadataItem --> <div>
<h3>Type Changed: Foundation.NSMetadataItem</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMetadataItem (NSUrl url);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public NSString ContentType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSString[] ContentTypeTree { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSString UbiquitousItemContainerDisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UbiquitousItemDownloadRequested { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UbiquitousItemIsExternalDocument { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSUrl UbiquitousItemUrlInLocalContainer { get; }</span>
</pre>
</div>

</div> <!-- end type NSMetadataItem -->
<!-- start type NSMutableCharacterSet --> <div>
<h3>Type Changed: Foundation.NSMutableCharacterSet</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSMutableCharacterSet -->
<!-- start type NSNetService --> <div>
<h3>Type Changed: Foundation.NSNetService</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSNetService -->
<!-- start type NSNetServiceBrowser --> <div>
<h3>Type Changed: Foundation.NSNetServiceBrowser</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSNetServiceBrowser -->
<!-- start type NSPersonNameComponentsFormatter --> <div>
<h3>Type Changed: Foundation.NSPersonNameComponentsFormatter</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSPersonNameComponents GetComponents (string string);</span>
</pre>
</div>

</div> <!-- end type NSPersonNameComponentsFormatter -->
<!-- start type NSPort --> <div>
<h3>Type Changed: Foundation.NSPort</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveFromRunLoop (NSRunLoop runLoop, NSRunLoopMode runLoopMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScheduleInRunLoop (NSRunLoop runLoop, NSRunLoopMode runLoopMode);</span>
</pre>
</div>

</div> <!-- end type NSPort -->
<!-- start type NSRunLoop --> <div>
<h3>Type Changed: Foundation.NSRunLoop</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public bool RunUntil (NSRunLoopMode <span class='removed removed-inline removed-breaking-inline'>mode</span> <span class='added '>runLoopMode</span>, NSDate limitDate)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (System.Action block);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Perform (NSRunLoopMode[] modes, System.Action block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (NSString[] modes, System.Action block);</span>
</pre>
</div>

</div> <!-- end type NSRunLoop -->
<!-- start type NSStream --> <div>
<h3>Type Changed: Foundation.NSStream</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString NetworkServiceTypeCallSignaling { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected virtual NSObject GetProperty (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode mode);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual bool SetProperty (NSObject property, NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode mode);</span>
</pre>
</div>

</div> <!-- end type NSStream -->
<!-- start type NSTimer --> <div>
<h3>Type Changed: Foundation.NSTimer</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTimer (NSDate date, double seconds, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSTimer CreateScheduledTimer (double interval, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTimer CreateTimer (double interval, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
</pre>
</div>

</div> <!-- end type NSTimer -->
<!-- start type NSUrlConnection --> <div>
<h3>Type Changed: Foundation.NSUrlConnection</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Schedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Unschedule (NSRunLoop aRunLoop, NSRunLoopMode forMode);</span>
</pre>
</div>

</div> <!-- end type NSUrlConnection -->
<!-- start type NSUrlRequestNetworkServiceType --> <div>
<h3>Type Changed: Foundation.NSUrlRequestNetworkServiceType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CallSignaling = 11,</span>
</pre>
</div>

</div> <!-- end type NSUrlRequestNetworkServiceType -->
<!-- start type NSUrlSessionHandler --> <div>
<h3>Type Changed: Foundation.NSUrlSessionHandler</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionHandler -->
<!-- start type NSUrlSessionTaskDelegate --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishCollectingMetrics (NSUrlSession session, NSUrlSessionTask task, NSUrlSessionTaskMetrics metrics);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate -->
<!-- start type NSUrlSessionTaskDelegate_Extensions --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinishCollectingMetrics (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlSessionTaskMetrics metrics);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate_Extensions -->
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set an activity type")]
	public NSUserActivity ();</span>
</div></pre>

</div> <!-- end type NSUserActivity -->
<!-- start type NSUserNotification --> <div>
<h3>Type Changed: Foundation.NSUserNotification</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserNotificationAction[] AdditionalActions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUserNotificationAction AdditionalActivationAction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSImage ContentImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasReplyButton { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAttributedString Response { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ResponsePlaceholder { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUserNotification -->
<div> <!-- start type CloudKitRegistrationPreparationHandler -->
<h3>New Type Foundation.CloudKitRegistrationPreparationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CloudKitRegistrationPreparationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CloudKitRegistrationPreparationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CloudKit.CKShare share, CloudKit.CKContainer container, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CloudKit.CKShare share, CloudKit.CKContainer container, NSError error);</span>
}
</pre>
</div> <!-- end type CloudKitRegistrationPreparationHandler -->
<div> <!-- start type NSDateInterval -->
<h3>New Type Foundation.NSDateInterval</h3>
<pre class='added' data-is-non-breaking="">
public class NSDateInterval : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDateInterval (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDateInterval (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSDate startDate, NSDate endDate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSDate startDate, double duration);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSComparisonResult Compare (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ContainsDate (NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDateInterval GetIntersection (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqualTo (NSDateInterval dateInterval);</span>
}
</pre>
</div> <!-- end type NSDateInterval -->
<div> <!-- start type NSDecodingFailurePolicy -->
<h3>New Type Foundation.NSDecodingFailurePolicy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSDecodingFailurePolicy {
	<span class='added added-field ' data-is-non-breaking="">RaiseException = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SetErrorAndReturn = 1,</span>
}
</pre>
</div> <!-- end type NSDecodingFailurePolicy -->
<div> <!-- start type NSDimension -->
<h3>New Type Foundation.NSDimension</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSDimension : Foundation.NSUnit, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDimension (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDimension (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDimension (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDimension (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUnitConverter Converter { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSDimension -->
<div> <!-- start type NSFileManager_NSUserInformation -->
<h3>New Type Foundation.NSFileManager_NSUserInformation</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileManager_NSUserInformation {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl GetHomeDirectory (NSFileManager This, string userName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl GetHomeDirectoryForCurrentUser (NSFileManager This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl GetTemporaryDirectory (NSFileManager This);</span>
}
</pre>
</div> <!-- end type NSFileManager_NSUserInformation -->
<div> <!-- start type NSIso8601DateFormatOptions -->
<h3>New Type Foundation.NSIso8601DateFormatOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSIso8601DateFormatOptions {
	<span class='added added-field ' data-is-non-breaking="">ColonSeparatorInTime = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">ColonSeparatorInTimeZone = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">DashSeparatorInDate = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Day = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">FullDate = 275,</span>
	<span class='added added-field ' data-is-non-breaking="">FullTime = 1632,</span>
	<span class='added added-field ' data-is-non-breaking="">InternetDateTime = 1907,</span>
	<span class='added added-field ' data-is-non-breaking="">Month = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SpaceBetweenDateAndTime = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Time = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">TimeZone = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">WeekOfYear = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Year = 1,</span>
}
</pre>
</div> <!-- end type NSIso8601DateFormatOptions -->
<div> <!-- start type NSIso8601DateFormatter -->
<h3>New Type Foundation.NSIso8601DateFormatter</h3>
<pre class='added' data-is-non-breaking="">
public class NSIso8601DateFormatter : Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSIso8601DateFormatter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSIso8601DateFormatter (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSIso8601DateFormatter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSIso8601DateFormatter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSIso8601DateFormatOptions FormatOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTimeZone TimeZone { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string Format (NSDate date, NSTimeZone timeZone, NSIso8601DateFormatOptions formatOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDate ToDate (string string);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSDate date);</span>
}
</pre>
</div> <!-- end type NSIso8601DateFormatter -->
<div> <!-- start type NSItemDownloadingStatusExtensions -->
<h3>New Type Foundation.NSItemDownloadingStatusExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemDownloadingStatusExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSItemDownloadingStatus self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSItemDownloadingStatus GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSItemDownloadingStatusExtensions -->
<div> <!-- start type NSMeasurementFormatter -->
<h3>New Type Foundation.NSMeasurementFormatter</h3>
<pre class='added' data-is-non-breaking="">
public class NSMeasurementFormatter : Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurementFormatter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurementFormatter (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurementFormatter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurementFormatter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLocale Locale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSNumberFormatter NumberFormatter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMeasurementFormatterUnitOptions UnitOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFormattingUnitStyle UnitStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (Foundation.NSMeasurement&lt;NSUnit&gt; measurement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSUnit unit);</span>
}
</pre>
</div> <!-- end type NSMeasurementFormatter -->
<div> <!-- start type NSMeasurementFormatterUnitOptions -->
<h3>New Type Foundation.NSMeasurementFormatterUnitOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSMeasurementFormatterUnitOptions {
	<span class='added added-field ' data-is-non-breaking="">NaturalScale = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ProvidedUnit = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TemperatureWithoutUnit = 4,</span>
}
</pre>
</div> <!-- end type NSMeasurementFormatterUnitOptions -->
<div> <!-- start type NSMeasurement`1 -->
<h3>New Type Foundation.NSMeasurement`1</h3>
<pre class='added' data-is-non-breaking="">
public class NSMeasurement`1 : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurement`1 (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurement`1 (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurement`1 (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurement`1 (double doubleValue, NSUnit unit);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUnit Unit { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanBeConvertedTo (NSUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementByAdding (Foundation.NSMeasurement&lt;UnitType&gt; measurement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementByConverting (NSUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementBySubtracting (Foundation.NSMeasurement&lt;UnitType&gt; measurement);</span>
}
</pre>
</div> <!-- end type NSMeasurement`1 -->
<div> <!-- start type NSProcessInfo_NSUserInformation -->
<h3>New Type Foundation.NSProcessInfo_NSUserInformation</h3>
<pre class='added' data-is-non-breaking="">
public static class NSProcessInfo_NSUserInformation {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static string GetFullUserName (NSProcessInfo This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetUserName (NSProcessInfo This);</span>
}
</pre>
</div> <!-- end type NSProcessInfo_NSUserInformation -->
<div> <!-- start type NSRunLoopModeExtensions -->
<h3>New Type Foundation.NSRunLoopModeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSRunLoopModeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSRunLoopMode self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSString[] GetConstants (NSRunLoopMode[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSRunLoopMode GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSRunLoopModeExtensions -->
<div> <!-- start type NSUnit -->
<h3>New Type Foundation.NSUnit</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnit : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnit (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnit (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit (string symbol);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Symbol { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnit -->
<div> <!-- start type NSUnitAcceleration -->
<h3>New Type Foundation.NSUnitAcceleration</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitAcceleration : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAcceleration (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAcceleration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAcceleration Gravity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAcceleration MetersPerSecondSquared { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitAcceleration -->
<div> <!-- start type NSUnitAngle -->
<h3>New Type Foundation.NSUnitAngle</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitAngle : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAngle (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAngle (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle ArcMinutes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle ArcSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Degrees { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Gradians { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Radians { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Revolutions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitAngle -->
<div> <!-- start type NSUnitArea -->
<h3>New Type Foundation.NSUnitArea</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitArea : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitArea (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitArea (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Acres { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Ares { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Hectares { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareCentimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareInches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareKilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMegameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMicrometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMillimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareNanometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareYards { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitArea -->
<div> <!-- start type NSUnitConcentrationMass -->
<h3>New Type Foundation.NSUnitConcentrationMass</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConcentrationMass : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConcentrationMass (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConcentrationMass (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitConcentrationMass GramsPerLiter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitConcentrationMass MilligramsPerDeciliter { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUnitConcentrationMass GetMillimolesPerLiter (double gramsPerMole);</span>
}
</pre>
</div> <!-- end type NSUnitConcentrationMass -->
<div> <!-- start type NSUnitConverter -->
<h3>New Type Foundation.NSUnitConverter</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConverter : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual double GetBaseUnitValue (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual double GetValue (double baseUnitValue);</span>
}
</pre>
</div> <!-- end type NSUnitConverter -->
<div> <!-- start type NSUnitConverterLinear -->
<h3>New Type Foundation.NSUnitConverterLinear</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConverterLinear : Foundation.NSUnitConverter, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverterLinear (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (double coefficient);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverterLinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (double coefficient, double constant);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Coefficient { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Constant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitConverterLinear -->
<div> <!-- start type NSUnitDispersion -->
<h3>New Type Foundation.NSUnitDispersion</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitDispersion : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDispersion (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDispersion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDispersion PartsPerMillion { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitDispersion -->
<div> <!-- start type NSUnitDuration -->
<h3>New Type Foundation.NSUnitDuration</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitDuration : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDuration (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDuration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Hours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Minutes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Seconds { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitDuration -->
<div> <!-- start type NSUnitElectricCharge -->
<h3>New Type Foundation.NSUnitElectricCharge</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricCharge : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCharge (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCharge (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge AmpereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge Coulombs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge KiloampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MegaampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MicroampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MilliampereHours { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricCharge -->
<div> <!-- start type NSUnitElectricCurrent -->
<h3>New Type Foundation.NSUnitElectricCurrent</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricCurrent : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCurrent (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCurrent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Amperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Kiloamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Megaamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Microamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Milliamperes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricCurrent -->
<div> <!-- start type NSUnitElectricPotentialDifference -->
<h3>New Type Foundation.NSUnitElectricPotentialDifference</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricPotentialDifference : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricPotentialDifference (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricPotentialDifference (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Kilovolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Megavolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Microvolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Millivolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Volts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricPotentialDifference -->
<div> <!-- start type NSUnitElectricResistance -->
<h3>New Type Foundation.NSUnitElectricResistance</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricResistance : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricResistance (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricResistance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Kiloohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Megaohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Microohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Milliohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Ohms { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricResistance -->
<div> <!-- start type NSUnitEnergy -->
<h3>New Type Foundation.NSUnitEnergy</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitEnergy : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitEnergy (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitEnergy (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Calories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Joules { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Kilocalories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Kilojoules { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy KilowattHours { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitEnergy -->
<div> <!-- start type NSUnitFrequency -->
<h3>New Type Foundation.NSUnitFrequency</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitFrequency : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFrequency (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFrequency (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Gigahertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Hertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Kilohertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Megahertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Microhertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Millihertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Nanohertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Terahertz { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitFrequency -->
<div> <!-- start type NSUnitFuelEfficiency -->
<h3>New Type Foundation.NSUnitFuelEfficiency</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitFuelEfficiency : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFuelEfficiency (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFuelEfficiency (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency LitersPer100Kilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency MilesPerGallon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency MilesPerImperialGallon { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitFuelEfficiency -->
<div> <!-- start type NSUnitIlluminance -->
<h3>New Type Foundation.NSUnitIlluminance</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitIlluminance : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitIlluminance (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitIlluminance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitIlluminance Lux { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitIlluminance -->
<div> <!-- start type NSUnitLength -->
<h3>New Type Foundation.NSUnitLength</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitLength : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitLength (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitLength (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength AstronomicalUnits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Centimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Decameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Decimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Fathoms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Feet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Furlongs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Hectometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Inches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Kilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Lightyears { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Megameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Meters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Micrometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Miles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Millimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Nanometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength NauticalMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Parsecs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Picometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength ScandinavianMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Yards { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitLength -->
<div> <!-- start type NSUnitMass -->
<h3>New Type Foundation.NSUnitMass</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitMass : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitMass (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitMass (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Carats { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Centigrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Decigrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Grams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Kilograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass MetricTons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Micrograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Milligrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Nanograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Ounces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass OuncesTroy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Picograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Pounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass ShortTons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Slugs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Stones { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitMass -->
<div> <!-- start type NSUnitPower -->
<h3>New Type Foundation.NSUnitPower</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitPower : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPower (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPower (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Femtowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Gigawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Horsepower { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Kilowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Megawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Microwatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Milliwatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Nanowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Picowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Terawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Watts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitPower -->
<div> <!-- start type NSUnitPressure -->
<h3>New Type Foundation.NSUnitPressure</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitPressure : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPressure (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPressure (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Bars { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Gigapascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Hectopascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure InchesOfMercury { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Kilopascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Megapascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Millibars { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure MillimetersOfMercury { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure NewtonsPerMetersSquared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure PoundsForcePerSquareInch { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitPressure -->
<div> <!-- start type NSUnitSpeed -->
<h3>New Type Foundation.NSUnitSpeed</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitSpeed : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitSpeed (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitSpeed (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed KilometersPerHour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed Knots { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed MetersPerSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed MilesPerHour { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitSpeed -->
<div> <!-- start type NSUnitTemperature -->
<h3>New Type Foundation.NSUnitTemperature</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitTemperature : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitTemperature (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitTemperature (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitTemperature (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitTemperature (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Celsius { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Fahrenheit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Kelvin { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitTemperature -->
<div> <!-- start type NSUnitVolume -->
<h3>New Type Foundation.NSUnitVolume</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitVolume : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitVolume (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitVolume (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume AcreFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Bushels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Centiliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicCentimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicDecimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicInches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicKilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMillimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicYards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Cups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Deciliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume FluidOunces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Gallons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialFluidOunces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialGallons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialPints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialQuarts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialTablespoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialTeaspoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Kiloliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Liters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Megaliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume MetricCups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Milliliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Pints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Quarts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Tablespoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Teaspoons { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitVolume -->
<div> <!-- start type NSUrlSessionTaskMetrics -->
<h3>New Type Foundation.NSUrlSessionTaskMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class NSUrlSessionTaskMetrics : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionTaskMetrics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskMetrics (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskMetrics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RedirectCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDateInterval TaskInterval { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlSessionTaskTransactionMetrics[] TransactionMetrics { get; }</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskMetrics -->
<div> <!-- start type NSUrlSessionTaskMetricsResourceFetchType -->
<h3>New Type Foundation.NSUrlSessionTaskMetricsResourceFetchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSUrlSessionTaskMetricsResourceFetchType {
	<span class='added added-field ' data-is-non-breaking="">LocalCache = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkLoad = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerPush = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskMetricsResourceFetchType -->
<div> <!-- start type NSUrlSessionTaskTransactionMetrics -->
<h3>New Type Foundation.NSUrlSessionTaskTransactionMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class NSUrlSessionTaskTransactionMetrics : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionTaskTransactionMetrics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskTransactionMetrics (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskTransactionMetrics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ConnectEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ConnectStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate DomainLookupEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate DomainLookupStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate FetchStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string NetworkProtocolName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ProxyConnection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlRequest Request { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate RequestEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate RequestStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlSessionTaskMetricsResourceFetchType ResourceFetchType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlResponse Response { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ResponseEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ResponseStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReusedConnection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate SecureConnectionEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate SecureConnectionStartDate { get; }</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskTransactionMetrics -->
<div> <!-- start type NSUserNotificationAction -->
<h3>New Type Foundation.NSUserNotificationAction</h3>
<pre class='added' data-is-non-breaking="">
public class NSUserNotificationAction : Foundation.NSObject, INSCopying, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUserNotificationAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserNotificationAction (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUserNotificationAction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUserNotificationAction GetAction (string identifier, string title);</span>
}
</pre>
</div> <!-- end type NSUserNotificationAction -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GLKit --> <div> 
<h2>Namespace GLKit</h2>
<!-- start type GLKTextureInfo --> <div>
<h3>Type Changed: GLKit.GLKTextureInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArrayLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Depth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MimapLevelCount { get; }</span>
</pre>
</div>

</div> <!-- end type GLKTextureInfo -->
<!-- start type GLKTextureLoader --> <div>
<h3>Type Changed: GLKit.GLKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginTextureLoad (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, CoreFoundation.DispatchQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GLKTextureInfo FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type GLKTextureLoader -->
<!-- start type GLKTextureLoaderError --> <div>
<h3>Type Changed: GLKit.GLKTextureLoaderError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnsupportedTextureTarget = 19,</span>
</pre>
</div>

</div> <!-- end type GLKTextureLoaderError -->

</div> <!-- end namespace GLKit -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKAchievementViewController --> <div>
<h3>Type Changed: GameKit.GKAchievementViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKAchievementViewController -->
<!-- start type GKDialogController --> <div>
<h3>Type Changed: GameKit.GKDialogController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKDialogController -->
<!-- start type GKError --> <div>
<h3>Type Changed: GameKit.GKError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">GameSessionRequestInvalid = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">MatchNotConnected = 28,</span>
</pre>
</div>

</div> <!-- end type GKError -->
<!-- start type GKFriendRequestComposeViewController --> <div>
<h3>Type Changed: GameKit.GKFriendRequestComposeViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKFriendRequestComposeViewController -->
<!-- start type GKGameCenterViewController --> <div>
<h3>Type Changed: GameKit.GKGameCenterViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKGameCenterViewController -->
<!-- start type GKLeaderboard --> <div>
<h3>Type Changed: GameKit.GKLeaderboard</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadImage (GKImageLoadedHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AppKit.NSImage&gt; LoadImageAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLeaderboard -->
<!-- start type GKLeaderboardViewController --> <div>
<h3>Type Changed: GameKit.GKLeaderboardViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKLeaderboardViewController -->
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadRecentPlayers (System.Action&lt;GKPlayer[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKPlayer[]&gt; LoadRecentPlayersAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKMatch --> <div>
<h3>Type Changed: GameKit.GKMatch</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ChooseBestHostPlayer (System.Action&lt;string&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;string&gt; ChooseBestHostPlayerAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Rematch (System.Action&lt;GKMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; RematchAsync ();</span>
</pre>
</div>

</div> <!-- end type GKMatch -->
<!-- start type GKMatchRequest --> <div>
<h3>Type Changed: GameKit.GKMatchRequest</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint DefaultNumberOfPlayers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string InviteMessage { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetMaxPlayersAllowed (GKMatchType matchType);</span>
</pre>
</div>

</div> <!-- end type GKMatchRequest -->
<!-- start type GKMatchmaker --> <div>
<h3>Type Changed: GameKit.GKMatchmaker</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelInvite (string playerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishMatchmaking (GKMatch match);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Match (GKInvite invite, System.Action&lt;GKMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; MatchAsync (GKInvite invite);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartBrowsingForNearbyPlayers (System.Action&lt;System.String,System.Boolean&gt; reachableHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopBrowsingForNearbyPlayers ();</span>
</pre>
</div>

</div> <!-- end type GKMatchmaker -->
<!-- start type GKMatchmakerViewController --> <div>
<h3>Type Changed: GameKit.GKMatchmakerViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DefaultInvitationMessage { get; set; }</span>
</pre>
</div>

</div> <!-- end type GKMatchmakerViewController -->
<!-- start type GKNotificationBanner --> <div>
<h3>Type Changed: GameKit.GKNotificationBanner</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Show (string title, string message, double durationSeconds, System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ShowAsync (string title, string message, double durationSeconds);</span>
</pre>
</div>

</div> <!-- end type GKNotificationBanner -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: GameKit.GKPlayer</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>GameKit.GKBasePlayer</span>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
</pre>
</div>

</div> <!-- end type GKPlayer -->
<!-- start type GKScore --> <div>
<h3>Type Changed: GameKit.GKScore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKScore (string identifier, string playerID);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LeaderboardIdentifier { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ReportScores (GKScore[] scores, GKChallenge[] challenges, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ReportScoresAsync (GKScore[] scores, GKChallenge[] challenges);</span>
</pre>
</div>

</div> <!-- end type GKScore -->
<!-- start type GKTurnBasedEventHandlerDelegate --> <div>
<h3>Type Changed: GameKit.GKTurnBasedEventHandlerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleTurnEvent (GKTurnBasedMatch match, bool activated);</span>
</pre>
</div>

</div> <!-- end type GKTurnBasedEventHandlerDelegate -->
<!-- start type GKTurnBasedEventHandlerDelegate_Extensions --> <div>
<h3>Type Changed: GameKit.GKTurnBasedEventHandlerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void HandleTurnEvent (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match, bool activated);</span>
</pre>
</div>

</div> <!-- end type GKTurnBasedEventHandlerDelegate_Extensions -->
<!-- start type GKTurnBasedMatch --> <div>
<h3>Type Changed: GameKit.GKTurnBasedMatch</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKTurnBasedExchange[] ActiveExchanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKTurnBasedExchange[] CompletedExchanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double DefaultTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ExchangeMaxInitiatedExchangesPerPlayer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKTurnBasedExchange[] Exchanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ExhangeDataMaximumSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MatchDataMaximumSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static double NoTimeout { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AcceptInvite (System.Action&lt;GKTurnBasedMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; AcceptInviteAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeclineInvite (System.Action&lt;GKTurnBasedMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; DeclineInviteAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndMatchInTurn (Foundation.NSData matchData, GKScore[] scores, GKAchievement[] achievements, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task EndMatchInTurnAsync (Foundation.NSData matchData, GKScore[] scores, GKAchievement[] achievements);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndTurn (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, Foundation.NSData matchData, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task EndTurnAsync (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, Foundation.NSData matchData);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadMatch (string matchId, System.Action&lt;GKTurnBasedMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; LoadMatchAsync (string matchId);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, Foundation.NSData matchData, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, Foundation.NSData matchData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Rematch (System.Action&lt;GKTurnBasedMatch,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; RematchAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveCurrentTurn (Foundation.NSData matchData, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SaveCurrentTurnAsync (Foundation.NSData matchData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveMergedMatchData (Foundation.NSData matchData, GKTurnBasedExchange[] exchanges, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SaveMergedMatchDataAsync (Foundation.NSData matchData, GKTurnBasedExchange[] exchanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendExchange (GKTurnBasedParticipant[] participants, Foundation.NSData data, string localizableMessage, Foundation.NSObject[] arguments, double timeout, System.Action&lt;GKTurnBasedExchange,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKTurnBasedExchange&gt; SendExchangeAsync (GKTurnBasedParticipant[] participants, Foundation.NSData data, string localizableMessage, Foundation.NSObject[] arguments, double timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendReminder (GKTurnBasedParticipant[] participants, string localizableMessage, Foundation.NSObject[] arguments, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendReminderAsync (GKTurnBasedParticipant[] participants, string localizableMessage, Foundation.NSObject[] arguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetMessage (string localizableMessage, Foundation.NSObject[] arguments);</span>
</pre>
</div>

</div> <!-- end type GKTurnBasedMatch -->
<!-- start type GKTurnBasedMatchmakerViewController --> <div>
<h3>Type Changed: GameKit.GKTurnBasedMatchmakerViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type GKTurnBasedMatchmakerViewController -->
<!-- start type GKTurnBasedParticipant --> <div>
<h3>Type Changed: GameKit.GKTurnBasedParticipant</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate TimeoutDate { get; }</span>
</pre>
</div>

</div> <!-- end type GKTurnBasedParticipant -->
<div> <!-- start type GKBasePlayer -->
<h3>New Type GameKit.GKBasePlayer</h3>
<pre class='added' data-is-non-breaking="">
public class GKBasePlayer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKBasePlayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBasePlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBasePlayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PlayerID { get; }</span>
}
</pre>
</div> <!-- end type GKBasePlayer -->
<div> <!-- start type GKCloudPlayer -->
<h3>New Type GameKit.GKCloudPlayer</h3>
<pre class='added' data-is-non-breaking="">
public class GKCloudPlayer : GameKit.GKBasePlayer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKCloudPlayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCloudPlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCloudPlayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void GetCurrentSignedInPlayer (string containerName, System.Action&lt;GKCloudPlayer,Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type GKCloudPlayer -->
<div> <!-- start type GKConnectionState -->
<h3>New Type GameKit.GKConnectionState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKConnectionState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConnected = 0,</span>
}
</pre>
</div> <!-- end type GKConnectionState -->
<div> <!-- start type GKGameSession -->
<h3>New Type GameKit.GKGameSession</h3>
<pre class='added' data-is-non-breaking="">
public class GKGameSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSession ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer[] BadgedPlayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate LastModifiedDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer LastModifiedPlayer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaxNumberOfConnectedPlayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer Owner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer[] Players { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddEventListener (IGKGameSessionEventListener listener);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClearBadge (GKCloudPlayer[] players, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ClearBadgeAsync (GKCloudPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CreateSession (string containerName, string title, nint maxPlayers, System.Action&lt;GKGameSession,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession&gt; CreateSessionAsync (string containerName, string title, nint maxPlayers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKCloudPlayer[] GetPlayers (GKConnectionState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetShareUrl (System.Action&lt;Foundation.NSUrl,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSUrl&gt; GetShareUrlAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadData (System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadSession (string identifier, System.Action&lt;GKGameSession,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession&gt; LoadSessionAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadSessions (string containerName, System.Action&lt;GKGameSession[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession[]&gt; LoadSessionsAsync (string containerName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveEventListener (IGKGameSessionEventListener listener);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveSession (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task RemoveSessionAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveData (Foundation.NSData data, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; SaveDataAsync (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendData (Foundation.NSData data, GKTransportType transport, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendDataAsync (Foundation.NSData data, GKTransportType transport);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendMessage (string key, string[] arguments, Foundation.NSData data, GKCloudPlayer[] players, bool badgePlayers, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendMessageAsync (string key, string[] arguments, Foundation.NSData data, GKCloudPlayer[] players, bool badgePlayers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConnectionState (GKConnectionState state, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetConnectionStateAsync (GKConnectionState state);</span>
}
</pre>
</div> <!-- end type GKGameSession -->
<div> <!-- start type GKGameSessionErrorCode -->
<h3>New Type GameKit.GKGameSessionErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKGameSessionErrorCode {
	<span class='added added-field ' data-is-non-breaking="">BadContainer = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudDriveDisabled = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudQuotaExceeded = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionCancelledByUser = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSession = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkFailure = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAuthenticated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNoRecipients = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNotConnected = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNotReachable = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">SendRateLimitReached = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionConflict = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionHasMaxConnectedPlayers = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionNotShared = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 1,</span>
}
</pre>
</div> <!-- end type GKGameSessionErrorCode -->
<div> <!-- start type GKGameSessionErrorCodeExtensions -->
<h3>New Type GameKit.GKGameSessionErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class GKGameSessionErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (GKGameSessionErrorCode self);</span>
}
</pre>
</div> <!-- end type GKGameSessionErrorCodeExtensions -->
<div> <!-- start type GKGameSessionEventListener_Extensions -->
<h3>New Type GameKit.GKGameSessionEventListener_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class GKGameSessionEventListener_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddPlayer (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeConnectionState (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player, GKConnectionState newState);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidReceiveData (IGKGameSessionEventListener This, GKGameSession session, Foundation.NSData data, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidReceiveMessage (IGKGameSessionEventListener This, GKGameSession session, string message, Foundation.NSData data, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemovePlayer (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSaveData (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player, Foundation.NSData data);</span>
}
</pre>
</div> <!-- end type GKGameSessionEventListener_Extensions -->
<div> <!-- start type GKLeaderboardSet -->
<h3>New Type GameKit.GKLeaderboardSet</h3>
<pre class='added' data-is-non-breaking="">
public class GKLeaderboardSet : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKLeaderboardSet ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKLeaderboardSet (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKLeaderboardSet (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKLeaderboardSet (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GroupIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadLeaderboardSets (GKLeaderboardSetsHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKLeaderboardSet[]&gt; LoadLeaderboardSetsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadLeaderboards (GKLeaderboardsHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKLeaderboard[]&gt; LoadLeaderboardsAsync ();</span>
}
</pre>
</div> <!-- end type GKLeaderboardSet -->
<div> <!-- start type GKLeaderboardSetsHandler -->
<h3>New Type GameKit.GKLeaderboardSetsHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GKLeaderboardSetsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKLeaderboardSetsHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (GKLeaderboardSet[] leaderboardSets, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (GKLeaderboardSet[] leaderboardSets, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GKLeaderboardSetsHandler -->
<div> <!-- start type GKLeaderboardsHandler -->
<h3>New Type GameKit.GKLeaderboardsHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate GKLeaderboardsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKLeaderboardsHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (GKLeaderboard[] leaderboards, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (GKLeaderboard[] leaderboards, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GKLeaderboardsHandler -->
<div> <!-- start type GKPeerConnectionState -->
<h3>New Type GameKit.GKPeerConnectionState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKPeerConnectionState {
	<span class='added added-field ' data-is-non-breaking="">Available = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Connected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connecting = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnected = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unavailable = 1,</span>
}
</pre>
</div> <!-- end type GKPeerConnectionState -->
<div> <!-- start type GKSendDataMode -->
<h3>New Type GameKit.GKSendDataMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKSendDataMode {
	<span class='added added-field ' data-is-non-breaking="">Reliable = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unreliable = 1,</span>
}
</pre>
</div> <!-- end type GKSendDataMode -->
<div> <!-- start type GKSessionMode -->
<h3>New Type GameKit.GKSessionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKSessionMode {
	<span class='added added-field ' data-is-non-breaking="">Client = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Peer = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Server = 0,</span>
}
</pre>
</div> <!-- end type GKSessionMode -->
<div> <!-- start type GKTransportType -->
<h3>New Type GameKit.GKTransportType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKTransportType {
	<span class='added added-field ' data-is-non-breaking="">Reliable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unreliable = 0,</span>
}
</pre>
</div> <!-- end type GKTransportType -->
<div> <!-- start type IGKGameSessionEventListener -->
<h3>New Type GameKit.IGKGameSessionEventListener</h3>
<pre class='added' data-is-non-breaking="">
public interface IGKGameSessionEventListener : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IGKGameSessionEventListener -->

</div> <!-- end namespace GameKit -->
<!-- start namespace GameplayKit --> <div> 
<h2>Namespace GameplayKit</h2>
<!-- start type GKAgent --> <div>
<h3>Type Changed: GameplayKit.GKAgent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual float Speed { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKAgent -->
<!-- start type GKAgent2D --> <div>
<h3>Type Changed: GameplayKit.GKAgent2D</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent2D (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKAgent2D -->
<!-- start type GKBehavior --> <div>
<h3>Type Changed: GameplayKit.GKBehavior</h3>
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

</div> <!-- end type GKBehavior -->
<!-- start type GKComponent --> <div>
<h3>Type Changed: GameplayKit.GKComponent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKComponent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddToEntity ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillRemoveFromEntity ();</span>
</pre>
</div>

</div> <!-- end type GKComponent -->
<!-- start type GKComponentSystem`1 --> <div>
<h3>Type Changed: GameplayKit.GKComponentSystem`1</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForGenericArgument (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Type GetTypeForGenericArgument (uint index);</span>
</pre>
</div>

</div> <!-- end type GKComponentSystem`1 -->
<!-- start type GKEntity --> <div>
<h3>Type Changed: GameplayKit.GKEntity</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKEntity (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKEntity -->
<!-- start type GKGraph --> <div>
<h3>Type Changed: GameplayKit.GKGraph</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraph (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKGraph -->
<!-- start type GKGraphNode --> <div>
<h3>Type Changed: GameplayKit.GKGraphNode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKGraphNode -->
<!-- start type GKGraphNode2D --> <div>
<h3>Type Changed: GameplayKit.GKGraphNode2D</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode2D (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKGraphNode2D -->
<!-- start type GKGridGraph --> <div>
<h3>Type Changed: GameplayKit.GKGridGraph</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraph (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraph (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed, ObjCRuntime.Class aClass);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraph (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed, System.Type nodeType);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static GKGridGraph FromGridStartingAt (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed, ObjCRuntime.Class aClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKGridGraph FromGridStartingAt (OpenTK.Vector2i position, int width, int height, bool diagonalsAllowed, System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForGenericArgument (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public NodeType GetNodeAt&lt;NodeType&gt; (OpenTK.Vector2i position);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Type GetTypeForGenericArgument (uint index);</span>
</pre>
</div>

</div> <!-- end type GKGridGraph -->
<!-- start type GKGridGraphNode --> <div>
<h3>Type Changed: GameplayKit.GKGridGraphNode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraphNode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKGridGraphNode -->
<!-- start type GKMinMaxStrategist --> <div>
<h3>Type Changed: GameplayKit.GKMinMaxStrategist</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IGKStrategist</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();</span>
</pre>
</div>

</div> <!-- end type GKMinMaxStrategist -->
<!-- start type GKObstacleGraph --> <div>
<h3>Type Changed: GameplayKit.GKObstacleGraph</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKObstacleGraph (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForGenericArgument (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Type GetTypeForGenericArgument (uint index);</span>
</pre>
</div>

</div> <!-- end type GKObstacleGraph -->
<!-- start type GKPath --> <div>
<h3>Type Changed: GameplayKit.GKPath</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKPath (GKGraphNode[] nodes, float radius);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKPath (OpenTK.Vector3[] points, float radius, bool cyclical);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static GKPath FromGraphNodes (GKGraphNode[] nodes, float radius);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKPath FromPoints (OpenTK.Vector3[] points, float radius, bool cyclical);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetVector2Point (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector3 GetVector3Point (uint index);</span>
</pre>
</div>

</div> <!-- end type GKPath -->
<!-- start type GKPolygonObstacle --> <div>
<h3>Type Changed: GameplayKit.GKPolygonObstacle</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKPolygonObstacle (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKPolygonObstacle -->
<!-- start type GKState --> <div>
<h3>Type Changed: GameplayKit.GKState</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>

</div> <!-- end type GKState -->
<!-- start type GKStateMachine --> <div>
<h3>Type Changed: GameplayKit.GKStateMachine</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual void Update (double <span class='removed removed-inline removed-breaking-inline'>seconds</span> <span class='added '>deltaTimeInSeconds</span>)
</div></pre>

</div> <!-- end type GKStateMachine -->
<div> <!-- start type GKAgent3D -->
<h3>New Type GameplayKit.GKAgent3D</h3>
<pre class='added' data-is-non-breaking="">
public class GKAgent3D : GameplayKit.GKAgent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent3D ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent3D (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKAgent3D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKAgent3D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Position { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RightHanded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Velocity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double deltaTimeInSeconds);</span>
}
</pre>
</div> <!-- end type GKAgent3D -->
<div> <!-- start type GKBillowNoiseSource -->
<h3>New Type GameplayKit.GKBillowNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKBillowNoiseSource : GameplayKit.GKCoherentNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBillowNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBillowNoiseSource (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKBillowNoiseSource (double frequency, nint octaveCount, double persistence, double lacunarity, int seed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Persistence { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKBillowNoiseSource Create (double frequency, nint octaveCount, double persistence, double lacunarity, int seed);</span>
}
</pre>
</div> <!-- end type GKBillowNoiseSource -->
<div> <!-- start type GKBox -->
<h3>New Type GameplayKit.GKBox</h3>
<pre class='added' data-is-non-breaking="">
public struct GKBox {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector3 Max;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector3 Min;</span>
}
</pre>
</div> <!-- end type GKBox -->
<div> <!-- start type GKCheckerboardNoiseSource -->
<h3>New Type GameplayKit.GKCheckerboardNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKCheckerboardNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCheckerboardNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKCheckerboardNoiseSource (double squareSize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCheckerboardNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double SquareSize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKCheckerboardNoiseSource Create (double squareSize);</span>
}
</pre>
</div> <!-- end type GKCheckerboardNoiseSource -->
<div> <!-- start type GKCoherentNoiseSource -->
<h3>New Type GameplayKit.GKCoherentNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class GKCoherentNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCoherentNoiseSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCoherentNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCoherentNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Frequency { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Lacunarity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint OctaveCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Seed { get; set; }</span>
}
</pre>
</div> <!-- end type GKCoherentNoiseSource -->
<div> <!-- start type GKCompositeBehavior -->
<h3>New Type GameplayKit.GKCompositeBehavior</h3>
<pre class='added' data-is-non-breaking="">
public class GKCompositeBehavior : GameplayKit.GKBehavior, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKCompositeBehavior ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCompositeBehavior (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCompositeBehavior (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nint BehaviorCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public GKBehavior Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKCompositeBehavior FromBehaviors (GKBehavior[] behaviors);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKCompositeBehavior FromBehaviors (GKBehavior[] behaviors, Foundation.NSNumber[] weights);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetWeight (GKBehavior behavior);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllBehaviors ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveBehavior (GKBehavior behavior);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetWeight (float weight, GKBehavior behavior);</span>
}
</pre>
</div> <!-- end type GKCompositeBehavior -->
<div> <!-- start type GKConstantNoiseSource -->
<h3>New Type GameplayKit.GKConstantNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKConstantNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKConstantNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKConstantNoiseSource (double value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKConstantNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Value { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKConstantNoiseSource Create (double value);</span>
}
</pre>
</div> <!-- end type GKConstantNoiseSource -->
<div> <!-- start type GKCylindersNoiseSource -->
<h3>New Type GameplayKit.GKCylindersNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKCylindersNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCylindersNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKCylindersNoiseSource (double frequency);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCylindersNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Frequency { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKCylindersNoiseSource Create (double frequency);</span>
}
</pre>
</div> <!-- end type GKCylindersNoiseSource -->
<div> <!-- start type GKDecisionNode -->
<h3>New Type GameplayKit.GKDecisionNode</h3>
<pre class='added' data-is-non-breaking="">
public class GKDecisionNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKDecisionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKDecisionNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual GKDecisionNode CreateBranch (Foundation.NSNumber value, Foundation.NSObject attribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKDecisionNode CreateBranch (Foundation.NSPredicate predicate, Foundation.NSObject attribute);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKDecisionNode CreateBranch (nint weight, Foundation.NSObject attribute);</span>
}
</pre>
</div> <!-- end type GKDecisionNode -->
<div> <!-- start type GKDecisionTree -->
<h3>New Type GameplayKit.GKDecisionTree</h3>
<pre class='added' data-is-non-breaking="">
public class GKDecisionTree : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKDecisionTree (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKDecisionTree (Foundation.NSObject attribute);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKDecisionTree (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKDecisionTree (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKDecisionTree (Foundation.NSArray&lt;Foundation.NSObject&gt;[] examples, Foundation.NSObject[] actions, Foundation.NSObject[] attributes);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKRandomSource RandomSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKDecisionNode RootNode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject FindAction (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSObject&gt; answers);</span>
}
</pre>
</div> <!-- end type GKDecisionTree -->
<div> <!-- start type GKGraphNode3D -->
<h3>New Type GameplayKit.GKGraphNode3D</h3>
<pre class='added' data-is-non-breaking="">
public class GKGraphNode3D : GameplayKit.GKGraphNode, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode3D (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGraphNode3D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode3D (OpenTK.Vector3 point);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGraphNode3D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Position { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKGraphNode3D FromPoint (OpenTK.Vector3 point);</span>
}
</pre>
</div> <!-- end type GKGraphNode3D -->
<div> <!-- start type GKMeshGraphTriangulationMode -->
<h3>New Type GameplayKit.GKMeshGraphTriangulationMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum GKMeshGraphTriangulationMode {
	<span class='added added-field ' data-is-non-breaking="">Centers = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">EdgeMidpoints = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertices = 1,</span>
}
</pre>
</div> <!-- end type GKMeshGraphTriangulationMode -->
<div> <!-- start type GKMeshGraph`1 -->
<h3>New Type GameplayKit.GKMeshGraph`1</h3>
<pre class='added' data-is-non-breaking="">
public class GKMeshGraph`1 : GameplayKit.GKGraph, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKMeshGraph`1 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKMeshGraph`1 (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKMeshGraph`1 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKMeshGraph`1 (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKMeshGraph`1 (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKMeshGraph`1 (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max, ObjCRuntime.Class nodeClass);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKMeshGraph`1 (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max, System.Type nodeType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float BufferRadius { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKPolygonObstacle[] Obstacles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint TriangleCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKMeshGraphTriangulationMode TriangulationMode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddObstacles (GKPolygonObstacle[] obstacles);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConnectNodeUsingObstacles (NodeType node);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKMeshGraph&lt;NodeType&gt; FromBufferRadius (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKMeshGraph&lt;NodeType&gt; FromBufferRadius (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max, ObjCRuntime.Class nodeClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKMeshGraph&lt;NodeType&gt; FromBufferRadius (float bufferRadius, OpenTK.Vector2 min, OpenTK.Vector2 max, System.Type nodeType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetClassForGenericArgument (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKTriangle GetTriangle (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Type GetTypeForGenericArgument (uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveObstacles (GKPolygonObstacle[] obstacles);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Triangulate ();</span>
}
</pre>
</div> <!-- end type GKMeshGraph`1 -->
<div> <!-- start type GKMonteCarloStrategist -->
<h3>New Type GameplayKit.GKMonteCarloStrategist</h3>
<pre class='added' data-is-non-breaking="">
public class GKMonteCarloStrategist : Foundation.NSObject, Foundation.INSObjectProtocol, IGKStrategist, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKMonteCarloStrategist ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKMonteCarloStrategist (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKMonteCarloStrategist (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Budget { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ExplorationParameter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IGKGameModel GameModel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IGKRandom RandomSource { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IGKGameModelUpdate GetBestMoveForActivePlayer ();</span>
}
</pre>
</div> <!-- end type GKMonteCarloStrategist -->
<div> <!-- start type GKNoise -->
<h3>New Type GameplayKit.GKNoise</h3>
<pre class='added' data-is-non-breaking="">
public class GKNoise : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoise ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoise (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoise (GKNoiseSource noiseSource);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoise (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoise (GKNoiseSource noiseSource, Foundation.NSDictionary&lt;Foundation.NSNumber,AppKit.NSColor&gt; gradientColors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSNumber,AppKit.NSColor&gt; GradientColors { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ApplyAbsoluteValue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ApplyTurbulence (double frequency, double power, int roughness, int seed);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Clamp (double lowerBound, double upperBound);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisplaceX (GKNoise xDisplacementNoise, GKNoise yDisplacementNoise, GKNoise zDisplacementNoise);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKNoise FromComponentNoises (GKNoise[] noises, GKNoise selectionNoise);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKNoise FromComponentNoises (GKNoise[] noises, GKNoise selectionNoise, Foundation.NSNumber[] componentBoundaries, Foundation.NSNumber[] blendDistances);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKNoise FromNoiseSource (GKNoiseSource noiseSource);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKNoise FromNoiseSource (GKNoiseSource noiseSource, Foundation.NSDictionary&lt;Foundation.NSNumber,AppKit.NSColor&gt; gradientColors);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetMaximum (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetMinimum (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetValue (OpenTK.Vector2 position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invert ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Move (OpenTK.Vector3d delta);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Multiply (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RaiseToPower (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RaiseToPower (double power);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemapValuesToCurve (Foundation.NSDictionary&lt;Foundation.NSNumber,Foundation.NSNumber&gt; controlPoints);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemapValuesToTerraces (Foundation.NSNumber[] peakInputValues, bool inverted);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Rotate (OpenTK.Vector3d radians);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Scale (OpenTK.Vector3d factor);</span>
}
</pre>
</div> <!-- end type GKNoise -->
<div> <!-- start type GKNoiseMap -->
<h3>New Type GameplayKit.GKNoiseMap</h3>
<pre class='added' data-is-non-breaking="">
public class GKNoiseMap : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoiseMap ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoiseMap (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoiseMap (GKNoise noise);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoiseMap (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKNoiseMap (GKNoise noise, OpenTK.Vector2d size, OpenTK.Vector2d origin, OpenTK.Vector2i sampleCount, bool seamless);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2d Origin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2i SampleCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Seamless { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2d Size { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKNoiseMap FromNoise (GKNoise noise);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKNoiseMap FromNoise (GKNoise noise, OpenTK.Vector2d size, OpenTK.Vector2d origin, OpenTK.Vector2i sampleCount, bool seamless);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetInterpolatedValue (OpenTK.Vector2 position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float GetValue (OpenTK.Vector2i position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (float value, OpenTK.Vector2i position);</span>
}
</pre>
</div> <!-- end type GKNoiseMap -->
<div> <!-- start type GKNoiseSource -->
<h3>New Type GameplayKit.GKNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class GKNoiseSource : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type GKNoiseSource -->
<div> <!-- start type GKObstacleGraph`1 -->
<h3>New Type GameplayKit.GKObstacleGraph`1</h3>
<pre class='added' data-is-non-breaking="">
public class GKObstacleGraph`1 : GameplayKit.GKObstacleGraph, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKObstacleGraph`1 (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKObstacleGraph`1 (GKPolygonObstacle[] obstacles, float bufferRadius);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKObstacleGraph&lt;NodeType&gt; FromObstacles (GKPolygonObstacle[] obstacles, float bufferRadius);</span>
	<span class='added added-method ' data-is-non-breaking="">public NodeType[] GetNodes (GKPolygonObstacle obstacle);</span>
}
</pre>
</div> <!-- end type GKObstacleGraph`1 -->
<div> <!-- start type GKOctreeNode -->
<h3>New Type GameplayKit.GKOctreeNode</h3>
<pre class='added' data-is-non-breaking="">
public class GKOctreeNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKOctreeNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKOctreeNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual GKBox Box { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type GKOctreeNode -->
<div> <!-- start type GKOctree`1 -->
<h3>New Type GameplayKit.GKOctree`1</h3>
<pre class='added' data-is-non-breaking="">
public class GKOctree`1 : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKOctree`1 ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKOctree`1 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKOctree`1 (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKOctree`1 (GKBox box, float minCellSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual GKOctreeNode AddElement (ElementType element, GKBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKOctreeNode AddElement (ElementType element, OpenTK.Vector3 point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKOctree&lt;ElementType&gt; FromBoundingBox (GKBox box, float minCellSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ElementType[] GetElements (GKBox box);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ElementType[] GetElements (OpenTK.Vector3 point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool RemoveElement (ElementType element);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool RemoveElement (ElementType element, GKOctreeNode node);</span>
}
</pre>
</div> <!-- end type GKOctree`1 -->
<div> <!-- start type GKPerlinNoiseSource -->
<h3>New Type GameplayKit.GKPerlinNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKPerlinNoiseSource : GameplayKit.GKCoherentNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKPerlinNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKPerlinNoiseSource (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKPerlinNoiseSource (double frequency, nint octaveCount, double persistence, double lacunarity, int seed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Persistence { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKPerlinNoiseSource Create (double frequency, nint octaveCount, double persistence, double lacunarity, int seed);</span>
}
</pre>
</div> <!-- end type GKPerlinNoiseSource -->
<div> <!-- start type GKQuad -->
<h3>New Type GameplayKit.GKQuad</h3>
<pre class='added' data-is-non-breaking="">
public struct GKQuad {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector2 Max;</span>
	<span class='added added-field ' data-is-non-breaking="">public OpenTK.Vector2 Min;</span>
}
</pre>
</div> <!-- end type GKQuad -->
<div> <!-- start type GKQuadTree -->
<h3>New Type GameplayKit.GKQuadTree</h3>
<pre class='added' data-is-non-breaking="">
public class GKQuadTree : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKQuadTree (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKQuadTree (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKQuadTree (GKQuad quad, float minCellSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual GKQuadTreeNode AddElement (Foundation.NSObject element, GKQuad quad);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKQuadTreeNode AddElement (Foundation.NSObject element, OpenTK.Vector2 point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKQuadTree FromBoundingQuad (GKQuad quad, float minCellSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] GetElements (GKQuad quad);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] GetElements (OpenTK.Vector2 point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool RemoveElement (Foundation.NSObject element);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool RemoveElement (Foundation.NSObject data, GKQuadTreeNode node);</span>
}
</pre>
</div> <!-- end type GKQuadTree -->
<div> <!-- start type GKQuadTreeNode -->
<h3>New Type GameplayKit.GKQuadTreeNode</h3>
<pre class='added' data-is-non-breaking="">
public class GKQuadTreeNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKQuadTreeNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKQuadTreeNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKQuad Quad { get; }</span>
}
</pre>
</div> <!-- end type GKQuadTreeNode -->
<div> <!-- start type GKRTreeSplitStrategy -->
<h3>New Type GameplayKit.GKRTreeSplitStrategy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKRTreeSplitStrategy {
	<span class='added added-field ' data-is-non-breaking="">Halve = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Quadratic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReduceOverlap = 3,</span>
}
</pre>
</div> <!-- end type GKRTreeSplitStrategy -->
<div> <!-- start type GKRTree`1 -->
<h3>New Type GameplayKit.GKRTree`1</h3>
<pre class='added' data-is-non-breaking="">
public class GKRTree`1 : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKRTree`1 (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKRTree`1 (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKRTree`1 (uint maxNumberOfChildren);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint QueryReserve { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddElement (ElementType element, OpenTK.Vector2 boundingRectMin, OpenTK.Vector2 boundingRectMax, GKRTreeSplitStrategy splitStrategy);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKRTree&lt;ElementType&gt; FromMaxNumberOfChildren (uint maxNumberOfChildren);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ElementType[] GetElements (OpenTK.Vector2 rectMin, OpenTK.Vector2 rectMax);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveElement (ElementType element, OpenTK.Vector2 boundingRectMin, OpenTK.Vector2 boundingRectMax);</span>
}
</pre>
</div> <!-- end type GKRTree`1 -->
<div> <!-- start type GKRidgedNoiseSource -->
<h3>New Type GameplayKit.GKRidgedNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKRidgedNoiseSource : GameplayKit.GKCoherentNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKRidgedNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKRidgedNoiseSource (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKRidgedNoiseSource (double frequency, nint octaveCount, double lacunarity, int seed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKRidgedNoiseSource Create (double frequency, nint octaveCount, double lacunarity, int seed);</span>
}
</pre>
</div> <!-- end type GKRidgedNoiseSource -->
<div> <!-- start type GKSKNodeComponent -->
<h3>New Type GameplayKit.GKSKNodeComponent</h3>
<pre class='added' data-is-non-breaking="">
public class GKSKNodeComponent : GameplayKit.GKComponent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, IGKAgentDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKSKNodeComponent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSKNodeComponent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSKNodeComponent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSKNodeComponent (SpriteKit.SKNode node);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSKNodeComponent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SpriteKit.SKNode Node { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AgentDidUpdate (GKAgent agent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AgentWillUpdate (GKAgent agent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKSKNodeComponent FromNode (SpriteKit.SKNode node);</span>
}
</pre>
</div> <!-- end type GKSKNodeComponent -->
<div> <!-- start type GKScene -->
<h3>New Type GameplayKit.GKScene</h3>
<pre class='added' data-is-non-breaking="">
public class GKScene : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKScene ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKScene (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKScene (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKScene (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKEntity[] Entities { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,GameplayKit.GKGraph&gt; Graphs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IGKSceneRootNodeType RootNode { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddEntity (GKEntity entity);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddGraph (GKGraph graph, string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GKScene FromFile (string filename);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveEntity (GKEntity entity);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveGraph (string name);</span>
}
</pre>
</div> <!-- end type GKScene -->
<div> <!-- start type GKSphereObstacle -->
<h3>New Type GameplayKit.GKSphereObstacle</h3>
<pre class='added' data-is-non-breaking="">
public class GKSphereObstacle : GameplayKit.GKObstacle, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSphereObstacle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSphereObstacle (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSphereObstacle (float radius);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 Position { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Radius { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKSphereObstacle FromRadius (float radius);</span>
}
</pre>
</div> <!-- end type GKSphereObstacle -->
<div> <!-- start type GKSpheresNoiseSource -->
<h3>New Type GameplayKit.GKSpheresNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKSpheresNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSpheresNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKSpheresNoiseSource (double frequency);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKSpheresNoiseSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Frequency { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKSpheresNoiseSource Create (double frequency);</span>
}
</pre>
</div> <!-- end type GKSpheresNoiseSource -->
<div> <!-- start type GKTriangle -->
<h3>New Type GameplayKit.GKTriangle</h3>
<pre class='added' data-is-non-breaking="">
public struct GKTriangle {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public OpenTK.Vector3[] Points { get; set; }</span>
}
</pre>
</div> <!-- end type GKTriangle -->
<div> <!-- start type GKVoronoiNoiseSource -->
<h3>New Type GameplayKit.GKVoronoiNoiseSource</h3>
<pre class='added' data-is-non-breaking="">
public class GKVoronoiNoiseSource : GameplayKit.GKNoiseSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKVoronoiNoiseSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKVoronoiNoiseSource (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKVoronoiNoiseSource (double frequency, double displacement, bool distanceEnabled, int seed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Displacement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DistanceEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Frequency { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual int Seed { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKVoronoiNoiseSource Create (double frequency, double displacement, bool distanceEnabled, int seed);</span>
}
</pre>
</div> <!-- end type GKVoronoiNoiseSource -->
<div> <!-- start type IGKSceneRootNodeType -->
<h3>New Type GameplayKit.IGKSceneRootNodeType</h3>
<pre class='added' data-is-non-breaking="">
public interface IGKSceneRootNodeType : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IGKSceneRootNodeType -->
<div> <!-- start type NSArray_GameplayKit -->
<h3>New Type GameplayKit.NSArray_GameplayKit</h3>
<pre class='added' data-is-non-breaking="">
public static class NSArray_GameplayKit {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static T[] GetShuffledArray&lt;T&gt; (Foundation.NSArray This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static T[] GetShuffledArray&lt;T&gt; (Foundation.NSArray This, GKRandomSource randomSource);</span>
}
</pre>
</div> <!-- end type NSArray_GameplayKit -->
<div> <!-- start type SKNode_GameplayKit -->
<h3>New Type GameplayKit.SKNode_GameplayKit</h3>
<pre class='added' data-is-non-breaking="">
public static class SKNode_GameplayKit {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static GKEntity GetEntity (SpriteKit.SKNode This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetEntity (SpriteKit.SKNode This, GKEntity entity);</span>
}
</pre>
</div> <!-- end type SKNode_GameplayKit -->

</div> <!-- end namespace GameplayKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestinationOptions --> <div>
<h3>Type Changed: ImageIO.CGImageDestinationOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? OptimizeColorForSharing { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGImageDestinationOptions -->
<!-- start type CGImageDestinationOptionsKeys --> <div>
<h3>Type Changed: ImageIO.CGImageDestinationOptionsKeys</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptimizeColorForSharing { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageDestinationOptionsKeys -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGAsShotNeutral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGAsShotWhiteXY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineExposure { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineNoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineSharpness { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBlackLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCalibrationIlluminant1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCalibrationIlluminant2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibration1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibration2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibrationSignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGColorMatrix1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGColorMatrix2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGFixVignetteRadial { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGNoiseProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGPrivateData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGProfileCalibrationSignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWarpFisheye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWarpRectilinear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWhiteLevel { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace ImageKit --> <div> 
<h2>Namespace ImageKit</h2>
<!-- start type IKCameraDeviceView --> <div>
<h3>Type Changed: ImageKit.IKCameraDeviceView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKCameraDeviceView -->
<!-- start type IKDeviceBrowserView --> <div>
<h3>Type Changed: ImageKit.IKDeviceBrowserView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKDeviceBrowserView -->
<!-- start type IKFilterBrowserPanel --> <div>
<h3>Type Changed: ImageKit.IKFilterBrowserPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKFilterBrowserPanel -->
<!-- start type IKFilterBrowserView --> <div>
<h3>Type Changed: ImageKit.IKFilterBrowserView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKFilterBrowserView -->
<!-- start type IKFilterUIView --> <div>
<h3>Type Changed: ImageKit.IKFilterUIView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKFilterUIView -->
<!-- start type IKImageBrowserView --> <div>
<h3>Type Changed: ImageKit.IKImageBrowserView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKImageBrowserView -->
<!-- start type IKImageEditPanel --> <div>
<h3>Type Changed: ImageKit.IKImageEditPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKImageEditPanel -->
<!-- start type IKImageView --> <div>
<h3>Type Changed: ImageKit.IKImageView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKImageView -->
<!-- start type IKPictureTaker --> <div>
<h3>Type Changed: ImageKit.IKPictureTaker</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKPictureTaker -->
<!-- start type IKScannerDeviceView --> <div>
<h3>Type Changed: ImageKit.IKScannerDeviceView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type IKScannerDeviceView -->

</div> <!-- end namespace ImageKit -->
<!-- start namespace LocalAuthentication --> <div> 
<h2>Namespace LocalAuthentication</h2>
<!-- start type LAAccessControlOperation --> <div>
<h3>Type Changed: LocalAuthentication.LAAccessControlOperation</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UseKeyDecrypt = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UseKeyKeyExchange = 5,</span>
</pre>
</div>

</div> <!-- end type LAAccessControlOperation -->
<!-- start type LAContext --> <div>
<h3>Type Changed: LocalAuthentication.LAContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedCancelTitle { get; set; }</span>
</pre>
</div>

</div> <!-- end type LAContext -->
<div> <!-- start type LAStatusExtensions -->
<h3>New Type LocalAuthentication.LAStatusExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class LAStatusExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (LAStatus self);</span>
}
</pre>
</div> <!-- end type LAStatusExtensions -->

</div> <!-- end namespace LocalAuthentication -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKDirectionsMode --> <div>
<h3>Type Changed: MapKit.MKDirectionsMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Default = 3,</span>
</pre>
</div>

</div> <!-- end type MKDirectionsMode -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKPinAnnotationView --> <div>
<h3>Type Changed: MapKit.MKPinAnnotationView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type MKPinAnnotationView -->
<div> <!-- start type NSUserActivity_MKMapItem -->
<h3>New Type MapKit.NSUserActivity_MKMapItem</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_MKMapItem {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKMapItem GetMapItem (Foundation.NSUserActivity This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetMapItem (Foundation.NSUserActivity This, MKMapItem item);</span>
}
</pre>
</div> <!-- end type NSUserActivity_MKMapItem -->

</div> <!-- end namespace MapKit -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLArgument --> <div>
<h3>Type Changed: Metal.MTLArgument</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsDepthTexture { get; }</span>
</pre>
</div>

</div> <!-- end type MTLArgument -->
<!-- start type MTLCommandBufferError --> <div>
<h3>Type Changed: Metal.MTLCommandBufferError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Memoryless = 10,</span>
</pre>
</div>

</div> <!-- end type MTLCommandBufferError -->
<!-- start type MTLComputeCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLComputeCommandEncoder_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStage (IMTLComputeCommandEncoder This, MTLRegion region);</span>
</pre>
</div>

</div> <!-- end type MTLComputeCommandEncoder_Extensions -->
<!-- start type MTLComputePipelineDescriptor --> <div>
<h3>Type Changed: Metal.MTLComputePipelineDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStageInputOutputDescriptor StageInputDescriptor { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLComputePipelineDescriptor -->
<!-- start type MTLDevice_Extensions --> <div>
<h3>Type Changed: Metal.MTLDevice_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLLibrary CreateLibrary (IMTLDevice This, Foundation.NSBundle bundle, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetRecommendedMaxWorkingSetSize (IMTLDevice This);</span>
</pre>
</div>

</div> <!-- end type MTLDevice_Extensions -->
<!-- start type MTLFeatureSet --> <div>
<h3>Type Changed: Metal.MTLFeatureSet</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">OSX_GPUFamily1_v2 = 10001,</span>
	<span class='added added-field ' data-is-non-breaking="">OSX_ReadWriteTextureTier2 = 10002,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily1_v3 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily2_v3 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">iOS_GPUFamily3_v2 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">tvOS_GPUFamily1_v2 = 30001,</span>
</pre>
</div>

</div> <!-- end type MTLFeatureSet -->
<!-- start type MTLLanguageVersion --> <div>
<h3>Type Changed: Metal.MTLLanguageVersion</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">v1_2 = 65538,</span>
</pre>
</div>

</div> <!-- end type MTLLanguageVersion -->
<!-- start type MTLLibraryError --> <div>
<h3>Type Changed: Metal.MTLLibraryError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FileNotFound = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FunctionNotFound = 5,</span>
</pre>
</div>

</div> <!-- end type MTLLibraryError -->
<!-- start type MTLPixelFormat --> <div>
<h3>Type Changed: Metal.MTLPixelFormat</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">X24_Stencil8 = 262,</span>
	<span class='added added-field ' data-is-non-breaking="">X32_Stencil8 = 261,</span>
</pre>
</div>

</div> <!-- end type MTLPixelFormat -->
<!-- start type MTLRenderCommandEncoder_Extensions --> <div>
<h3>Type Changed: Metal.MTLRenderCommandEncoder_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DrawIndexedPatches (IMTLRenderCommandEncoder This, uint numberOfPatchControlPoints, IMTLBuffer patchIndexBuffer, uint patchIndexBufferOffset, IMTLBuffer controlPointIndexBuffer, uint controlPointIndexBufferOffset, IMTLBuffer indirectBuffer, uint indirectBufferOffset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DrawIndexedPatches (IMTLRenderCommandEncoder This, uint numberOfPatchControlPoints, uint patchStart, uint patchCount, IMTLBuffer patchIndexBuffer, uint patchIndexBufferOffset, IMTLBuffer controlPointIndexBuffer, uint controlPointIndexBufferOffset, uint instanceCount, uint baseInstance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DrawPatches (IMTLRenderCommandEncoder This, uint numberOfPatchControlPoints, IMTLBuffer patchIndexBuffer, uint patchIndexBufferOffset, IMTLBuffer indirectBuffer, uint indirectBufferOffset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DrawPatches (IMTLRenderCommandEncoder This, uint numberOfPatchControlPoints, uint patchStart, uint patchCount, IMTLBuffer patchIndexBuffer, uint patchIndexBufferOffset, uint instanceCount, uint baseInstance);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetColorStoreAction (IMTLRenderCommandEncoder This, MTLStoreAction storeAction, uint colorAttachmentIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDepthStoreAction (IMTLRenderCommandEncoder This, MTLStoreAction storeAction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStencilStoreAction (IMTLRenderCommandEncoder This, MTLStoreAction storeAction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetTessellationFactorBuffer (IMTLRenderCommandEncoder This, IMTLBuffer buffer, uint offset, uint instanceStride);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetTessellationFactorScale (IMTLRenderCommandEncoder This, float scale);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void TextureBarrier (IMTLRenderCommandEncoder This);</span>
</pre>
</div>

</div> <!-- end type MTLRenderCommandEncoder_Extensions -->
<!-- start type MTLRenderPassDescriptor --> <div>
<h3>Type Changed: Metal.MTLRenderPassDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RenderTargetArrayLength { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLRenderPassDescriptor -->
<!-- start type MTLRenderPipelineDescriptor --> <div>
<h3>Type Changed: Metal.MTLRenderPipelineDescriptor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLPrimitiveTopologyClass InputPrimitiveTopology { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsTessellationFactorScaleEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaxTessellationFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTessellationControlPointIndexType TessellationControlPointIndexType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTessellationFactorFormat TessellationFactorFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTessellationFactorStepFunction TessellationFactorStepFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLWinding TessellationOutputWindingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLTessellationPartitionMode TessellationPartitionMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLRenderPipelineDescriptor -->
<!-- start type MTLResourceOptions --> <div>
<h3>Type Changed: Metal.MTLResourceOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HazardTrackingModeUntracked = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">StorageModeMemoryless = 48,</span>
</pre>
</div>

</div> <!-- end type MTLResourceOptions -->
<!-- start type MTLSamplerAddressMode --> <div>
<h3>Type Changed: Metal.MTLSamplerAddressMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClampToBorderColor = 5,</span>
</pre>
</div>

</div> <!-- end type MTLSamplerAddressMode -->
<!-- start type MTLSamplerDescriptor --> <div>
<h3>Type Changed: Metal.MTLSamplerDescriptor</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLSamplerBorderColor BorderColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTLSamplerDescriptor -->
<!-- start type MTLStorageMode --> <div>
<h3>Type Changed: Metal.MTLStorageMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Memoryless = 3,</span>
</pre>
</div>

</div> <!-- end type MTLStorageMode -->
<!-- start type MTLStoreAction --> <div>
<h3>Type Changed: Metal.MTLStoreAction</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">StoreAndMultisampleResolve = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 4,</span>
</pre>
</div>

</div> <!-- end type MTLStoreAction -->
<!-- start type MTLVertexAttribute --> <div>
<h3>Type Changed: Metal.MTLVertexAttribute</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PatchControlPointData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PatchData { get; }</span>
</pre>
</div>

</div> <!-- end type MTLVertexAttribute -->
<!-- start type MTLVertexDescriptor --> <div>
<h3>Type Changed: Metal.MTLVertexDescriptor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MTLVertexDescriptor FromModelIO (ModelIO.MDLVertexDescriptor descriptor, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MTLVertexDescriptor -->
<!-- start type MTLVertexStepFunction --> <div>
<h3>Type Changed: Metal.MTLVertexStepFunction</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PerPatch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">PerPatchControlPoint = 4,</span>
</pre>
</div>

</div> <!-- end type MTLVertexStepFunction -->
<div> <!-- start type MTLAttribute -->
<h3>New Type Metal.MTLAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class MTLAttribute : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttribute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttribute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Active { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint AttributeIndex { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType AttributeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPatchControlPointData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsPatchData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
}
</pre>
</div> <!-- end type MTLAttribute -->
<div> <!-- start type MTLAttributeDescriptor -->
<h3>New Type Metal.MTLAttributeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLAttributeDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLAttributeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttributeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttributeDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BufferIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLAttributeFormat Format { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Offset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MTLAttributeDescriptor -->
<div> <!-- start type MTLAttributeDescriptorArray -->
<h3>New Type Metal.MTLAttributeDescriptorArray</h3>
<pre class='added' data-is-non-breaking="">
public class MTLAttributeDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLAttributeDescriptorArray ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttributeDescriptorArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLAttributeDescriptorArray (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MTLAttributeDescriptor Item { get; set; }</span>
}
</pre>
</div> <!-- end type MTLAttributeDescriptorArray -->
<div> <!-- start type MTLAttributeFormat -->
<h3>New Type Metal.MTLAttributeFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLAttributeFormat {
	<span class='added added-field ' data-is-non-breaking="">Char2 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Char2Normalized = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Char3 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Char3Normalized = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Char4 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Char4Normalized = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Float = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">Float2 = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">Float3 = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">Float4 = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">Half2 = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Half3 = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Half4 = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">Int = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Int1010102Normalized = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">Int2 = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">Int3 = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">Int4 = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Short2 = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Short2Normalized = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">Short3 = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Short3Normalized = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Short4 = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Short4Normalized = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar2 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar2Normalized = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar3 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar3Normalized = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar4 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">UChar4Normalized = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt1010102Normalized = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt2 = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt3 = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt4 = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort2 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort2Normalized = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort3 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort3Normalized = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort4 = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">UShort4Normalized = 21,</span>
}
</pre>
</div> <!-- end type MTLAttributeFormat -->
<div> <!-- start type MTLBufferLayoutDescriptor -->
<h3>New Type Metal.MTLBufferLayoutDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLBufferLayoutDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLBufferLayoutDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLBufferLayoutDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLBufferLayoutDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLStepFunction StepFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StepRate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Stride { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type MTLBufferLayoutDescriptor -->
<div> <!-- start type MTLBufferLayoutDescriptorArray -->
<h3>New Type Metal.MTLBufferLayoutDescriptorArray</h3>
<pre class='added' data-is-non-breaking="">
public class MTLBufferLayoutDescriptorArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLBufferLayoutDescriptorArray ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLBufferLayoutDescriptorArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLBufferLayoutDescriptorArray (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MTLBufferLayoutDescriptor Item { get; set; }</span>
}
</pre>
</div> <!-- end type MTLBufferLayoutDescriptorArray -->
<div> <!-- start type MTLBuffer_Extensions -->
<h3>New Type Metal.MTLBuffer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLBuffer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddDebugMarker (IMTLBuffer This, string marker, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAllDebugMarkers (IMTLBuffer This);</span>
}
</pre>
</div> <!-- end type MTLBuffer_Extensions -->
<div> <!-- start type MTLDrawPatchIndirectArguments -->
<h3>New Type Metal.MTLDrawPatchIndirectArguments</h3>
<pre class='added' data-is-non-breaking="">
public struct MTLDrawPatchIndirectArguments {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLDrawPatchIndirectArguments (uint pathCount, uint instanceCount, uint patchStart, uint baseInstance);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint BaseInstance;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint InstanceCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint PatchCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint PatchStart;</span>
}
</pre>
</div> <!-- end type MTLDrawPatchIndirectArguments -->
<div> <!-- start type MTLFunctionConstant -->
<h3>New Type Metal.MTLFunctionConstant</h3>
<pre class='added' data-is-non-breaking="">
public class MTLFunctionConstant : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLFunctionConstant ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLFunctionConstant (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLFunctionConstant (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Index { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLDataType Type { get; }</span>
}
</pre>
</div> <!-- end type MTLFunctionConstant -->
<div> <!-- start type MTLFunctionConstantValues -->
<h3>New Type Metal.MTLFunctionConstantValues</h3>
<pre class='added' data-is-non-breaking="">
public class MTLFunctionConstantValues : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLFunctionConstantValues (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLFunctionConstantValues (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConstantValue (IntPtr value, MTLDataType type, string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConstantValue (IntPtr value, MTLDataType type, uint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConstantValues (IntPtr values, MTLDataType type, Foundation.NSRange range);</span>
}
</pre>
</div> <!-- end type MTLFunctionConstantValues -->
<div> <!-- start type MTLFunction_Extensions -->
<h3>New Type Metal.MTLFunction_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLFunction_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;Foundation.NSString,Metal.MTLFunctionConstant&gt; GetFunctionConstants (IMTLFunction This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetLabel (IMTLFunction This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetPatchControlPointCount (IMTLFunction This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLPatchType GetPatchType (IMTLFunction This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLAttribute[] GetStageInputAttributes (IMTLFunction This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetLabel (IMTLFunction This, string value);</span>
}
</pre>
</div> <!-- end type MTLFunction_Extensions -->
<div> <!-- start type MTLLibrary_Extensions -->
<h3>New Type Metal.MTLLibrary_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLLibrary_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CreateFunction (IMTLLibrary This, string name, MTLFunctionConstantValues constantValues, System.Action&lt;IMTLFunction,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IMTLFunction CreateFunction (IMTLLibrary This, string name, MTLFunctionConstantValues constantValues, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MTLLibrary_Extensions -->
<div> <!-- start type MTLParallelRenderCommandEncoder_Extensions -->
<h3>New Type Metal.MTLParallelRenderCommandEncoder_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLParallelRenderCommandEncoder_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void SetColorStoreAction (IMTLParallelRenderCommandEncoder This, MTLStoreAction storeAction, uint colorAttachmentIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetDepthStoreAction (IMTLParallelRenderCommandEncoder This, MTLStoreAction storeAction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetStencilStoreAction (IMTLParallelRenderCommandEncoder This, MTLStoreAction storeAction);</span>
}
</pre>
</div> <!-- end type MTLParallelRenderCommandEncoder_Extensions -->
<div> <!-- start type MTLPatchType -->
<h3>New Type Metal.MTLPatchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLPatchType {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Quad = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Triangle = 1,</span>
}
</pre>
</div> <!-- end type MTLPatchType -->
<div> <!-- start type MTLPrimitiveTopologyClass -->
<h3>New Type Metal.MTLPrimitiveTopologyClass</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLPrimitiveTopologyClass {
	<span class='added added-field ' data-is-non-breaking="">Line = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Point = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Triangle = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type MTLPrimitiveTopologyClass -->
<div> <!-- start type MTLQuadTessellationFactorsHalf -->
<h3>New Type Metal.MTLQuadTessellationFactorsHalf</h3>
<pre class='added' data-is-non-breaking="">
public struct MTLQuadTessellationFactorsHalf {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLQuadTessellationFactorsHalf (ushort[] edgeTessellationFactor, ushort[] insideTessellationFactor);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ushort[] EdgeTessellationFactor;</span>
	<span class='added added-field ' data-is-non-breaking="">public ushort[] InsideTessellationFactor;</span>
}
</pre>
</div> <!-- end type MTLQuadTessellationFactorsHalf -->
<div> <!-- start type MTLRenderStages -->
<h3>New Type Metal.MTLRenderStages</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLRenderStages {
	<span class='added added-field ' data-is-non-breaking="">Fragment = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertex = 1,</span>
}
</pre>
</div> <!-- end type MTLRenderStages -->
<div> <!-- start type MTLSamplerBorderColor -->
<h3>New Type Metal.MTLSamplerBorderColor</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLSamplerBorderColor {
	<span class='added added-field ' data-is-non-breaking="">OpaqueBlack = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">OpaqueWhite = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TransparentBlack = 0,</span>
}
</pre>
</div> <!-- end type MTLSamplerBorderColor -->
<div> <!-- start type MTLSizeAndAlign -->
<h3>New Type Metal.MTLSizeAndAlign</h3>
<pre class='added' data-is-non-breaking="">
public struct MTLSizeAndAlign {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLSizeAndAlign (uint size, uint align);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint Align;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Size;</span>
}
</pre>
</div> <!-- end type MTLSizeAndAlign -->
<div> <!-- start type MTLStageInputOutputDescriptor -->
<h3>New Type Metal.MTLStageInputOutputDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MTLStageInputOutputDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLStageInputOutputDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLStageInputOutputDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MTLStageInputOutputDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLAttributeDescriptorArray Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexBufferIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLIndexType IndexType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MTLBufferLayoutDescriptorArray Layouts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTLStageInputOutputDescriptor Create ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reset ();</span>
}
</pre>
</div> <!-- end type MTLStageInputOutputDescriptor -->
<div> <!-- start type MTLStepFunction -->
<h3>New Type Metal.MTLStepFunction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLStepFunction {
	<span class='added added-field ' data-is-non-breaking="">Constant = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PerInstance = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PerPatch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">PerPatchControlPoint = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PerVertex = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreadPositionInGridX = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreadPositionInGridXIndexed = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreadPositionInGridY = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreadPositionInGridYIndexed = 8,</span>
}
</pre>
</div> <!-- end type MTLStepFunction -->
<div> <!-- start type MTLTessellationControlPointIndexType -->
<h3>New Type Metal.MTLTessellationControlPointIndexType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLTessellationControlPointIndexType {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt16 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt32 = 2,</span>
}
</pre>
</div> <!-- end type MTLTessellationControlPointIndexType -->
<div> <!-- start type MTLTessellationFactorFormat -->
<h3>New Type Metal.MTLTessellationFactorFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLTessellationFactorFormat {
	<span class='added added-field ' data-is-non-breaking="">Half = 0,</span>
}
</pre>
</div> <!-- end type MTLTessellationFactorFormat -->
<div> <!-- start type MTLTessellationFactorStepFunction -->
<h3>New Type Metal.MTLTessellationFactorStepFunction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLTessellationFactorStepFunction {
	<span class='added added-field ' data-is-non-breaking="">Constant = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PerInstance = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PerPatch = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PerPatchAndPerInstance = 3,</span>
}
</pre>
</div> <!-- end type MTLTessellationFactorStepFunction -->
<div> <!-- start type MTLTessellationPartitionMode -->
<h3>New Type Metal.MTLTessellationPartitionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTLTessellationPartitionMode {
	<span class='added added-field ' data-is-non-breaking="">FractionalEven = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FractionalOdd = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Integer = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Pow2 = 0,</span>
}
</pre>
</div> <!-- end type MTLTessellationPartitionMode -->
<div> <!-- start type MTLTriangleTessellationFactorsHalf -->
<h3>New Type Metal.MTLTriangleTessellationFactorsHalf</h3>
<pre class='added' data-is-non-breaking="">
public struct MTLTriangleTessellationFactorsHalf {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTLTriangleTessellationFactorsHalf (ushort[] edgeTessellationFactor, ushort insideTessellationFactor);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ushort[] EdgeTessellationFactor;</span>
	<span class='added added-field ' data-is-non-breaking="">public ushort InsideTessellationFactor;</span>
}
</pre>
</div> <!-- end type MTLTriangleTessellationFactorsHalf -->

</div> <!-- end namespace Metal -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKMeshBuffer --> <div>
<h3>Type Changed: MetalKit.MTKMeshBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ModelIO.IMDLNamed</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTKMeshBuffer -->
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromNames (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromNames (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromTexture (ModelIO.MDLTexture texture, Foundation.NSDictionary options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture FromTexture (ModelIO.MDLTexture texture, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromTexture (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture FromTexture (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromUrls (Foundation.NSUrl[] urls, Foundation.NSDictionary options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture[] FromUrls (Foundation.NSUrl[] urls, Foundation.NSDictionary options, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromUrls (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture[] FromUrls (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->
<!-- start type MTKTextureLoaderOptions --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoaderOptions</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public bool? AllocateMipmaps { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public bool? Srgb { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MTKTextureLoaderCubeLayout? CubeLayout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? GenerateMipmaps { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MTKTextureLoaderOrigin? Origin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Metal.MTLStorageMode? TextureStorageMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoaderOptions -->
<!-- start type MTKView --> <div>
<h3>Type Changed: MetalKit.MTKView</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
	<span class='added added-interface ' data-is-non-breaking="">CoreAnimation.ICALayerDelegate</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ActionForLayer (CoreAnimation.CALayer layer, string eventKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisplayLayer (CoreAnimation.CALayer layer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawLayer (CoreAnimation.CALayer layer, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LayoutSublayersOfLayer (CoreAnimation.CALayer layer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillDrawLayer (CoreAnimation.CALayer layer);</span>
</pre>
</div>

</div> <!-- end type MTKView -->
<div> <!-- start type MTKTextureLoaderArrayCallback -->
<h3>New Type MetalKit.MTKTextureLoaderArrayCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MTKTextureLoaderArrayCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTKTextureLoaderArrayCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Metal.IMTLTexture[] textures, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Metal.IMTLTexture[] textures, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderArrayCallback -->
<div> <!-- start type MTKTextureLoaderCubeLayout -->
<h3>New Type MetalKit.MTKTextureLoaderCubeLayout</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTKTextureLoaderCubeLayout {
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderCubeLayout -->
<div> <!-- start type MTKTextureLoaderCubeLayoutExtensions -->
<h3>New Type MetalKit.MTKTextureLoaderCubeLayoutExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTKTextureLoaderCubeLayoutExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (MTKTextureLoaderCubeLayout self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTKTextureLoaderCubeLayout GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderCubeLayoutExtensions -->
<div> <!-- start type MTKTextureLoaderOrigin -->
<h3>New Type MetalKit.MTKTextureLoaderOrigin</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTKTextureLoaderOrigin {
	<span class='added added-field ' data-is-non-breaking="">BottomLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FlippedVertically = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeft = 0,</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderOrigin -->
<div> <!-- start type MTKTextureLoaderOriginExtensions -->
<h3>New Type MetalKit.MTKTextureLoaderOriginExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTKTextureLoaderOriginExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (MTKTextureLoaderOrigin self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTKTextureLoaderOrigin GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderOriginExtensions -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace MobileCoreServices --> <div> 
<h2>Namespace MobileCoreServices</h2>
<!-- start type UTType --> <div>
<h3>Type Changed: MobileCoreServices.UTType</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UniversalSceneDescription { get; }</span>
</pre>
</div>

</div> <!-- end type UTType -->

</div> <!-- end namespace MobileCoreServices -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLObjectContainerComponent Masters { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLAsset FromScene (SceneKit.SCNScene scene, IMDLMeshBufferAllocator bufferAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLObject[] GetChildObjects (ObjCRuntime.Class objectClass);</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->
<!-- start type MDLCamera --> <div>
<h3>Type Changed: ModelIO.MDLCamera</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLCameraProjection Projection { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLCamera -->
<!-- start type MDLLight --> <div>
<h3>Type Changed: ModelIO.MDLLight</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString ColorSpace { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLLight -->
<!-- start type MDLMaterial --> <div>
<h3>Type Changed: ModelIO.MDLMaterial</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialFace MaterialFace { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLMaterialProperty[] GetProperties (MDLMaterialSemantic semantic);</span>
</pre>
</div>

</div> <!-- end type MDLMaterial -->
<!-- start type MDLMaterialProperty --> <div>
<h3>Type Changed: ModelIO.MDLMaterialProperty</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Luminance { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type MDLMaterialProperty -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMesh (IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual Foundation.NSMutableArray&lt;MDLSubmesh&gt; Submeshes { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual IMDLMeshBuffer[] VertexBuffers { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual uint VertexCount { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLMeshBufferAllocator Allocator { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAttribute (string name, MDLVertexFormat format, string type, Foundation.NSData data, nint stride);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAttribute (string name, MDLVertexFormat format, string type, Foundation.NSData data, nint stride, double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddUnwrappedTextureCoordinates (string textureCoordinateAttributeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCapsule (OpenTK.Vector3 dimensions, OpenTK.Vector2i segments, MDLGeometryType geometryType, bool inwardNormals, int hemisphereSegments, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCapsule (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, uint hemisphereSegments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCone (OpenTK.Vector3 dimensions, OpenTK.Vector2i segments, MDLGeometryType geometryType, bool inwardNormals, bool cap, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateHemisphere (OpenTK.Vector3 dimensions, OpenTK.Vector2i segments, MDLGeometryType geometryType, bool inwardNormals, bool cap, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateIcosahedron (float radius, bool inwardNormals, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateSphere (OpenTK.Vector3 dimensions, OpenTK.Vector2i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateSubdividedMesh (MDLMesh mesh, int submeshIndex, uint subdivisionLevels, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh FromGeometry (SceneKit.SCNGeometry geometry, IMDLMeshBufferAllocator bufferAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLVertexAttributeData GetVertexAttributeData (string attributeName, MDLVertexFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAttribute (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReplaceAttribute (string name, MDLVertexAttributeData newData);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateAttribute (string name, MDLVertexAttributeData newData);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLNoiseTexture --> <div>
<h3>Type Changed: ModelIO.MDLNoiseTexture</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-breaking="">	public MDLNoiseTexture (float <span class='removed removed-inline removed-breaking-inline'>smoothness</span> <span class='added '>input</span>, string name, OpenTK.Vector2i textureDimensions, MDLTextureChannelEncoding channelEncoding)
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLNoiseTexture (float input, string name, OpenTK.Vector2i textureDimensions, MDLTextureChannelEncoding channelEncoding, MDLNoiseTextureType type);</span>
</pre>
</div>

</div> <!-- end type MDLNoiseTexture -->
<!-- start type MDLObject --> <div>
<h3>Type Changed: ModelIO.MDLObject</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLObject Instance { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Path { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateChildObjects (ObjCRuntime.Class objectClass, MDLObject root, MDLObjectHandler handler, bool stop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLObject FromNode (SceneKit.SCNNode node, IMDLMeshBufferAllocator bufferAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLObject GetObject (string path);</span>
</pre>
</div>

</div> <!-- end type MDLObject -->
<!-- start type MDLSubmesh --> <div>
<h3>Type Changed: ModelIO.MDLSubmesh</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual MDLSubmeshTopology Topology { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLSubmesh FromGeometryElement (SceneKit.SCNGeometryElement element, IMDLMeshBufferAllocator bufferAllocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMDLMeshBuffer GetIndexBuffer (MDLIndexBitDepth indexType);</span>
</pre>
</div>

</div> <!-- end type MDLSubmesh -->
<!-- start type MDLSubmeshTopology --> <div>
<h3>Type Changed: ModelIO.MDLSubmeshTopology</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLSubmeshTopology (MDLSubmesh submesh);</span>
</pre>
</div>

</div> <!-- end type MDLSubmeshTopology -->
<!-- start type MDLTexture --> <div>
<h3>Type Changed: ModelIO.MDLTexture</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasAlphaValues { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLTexture -->
<!-- start type MDLTransform --> <div>
<h3>Type Changed: ModelIO.MDLTransform</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransform (IMDLTransformComponent component, bool resetsTransform);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLTransform (OpenTK.Matrix4 matrix, bool resetsTransform);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] KeyTimes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ResetsTransform { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type MDLTransform -->
<!-- start type MDLTransformComponent_Extensions --> <div>
<h3>Type Changed: ModelIO.MDLTransformComponent_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSNumber[] GetKeyTimes (IMDLTransformComponent This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool GetResetsTransform (IMDLTransformComponent This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetResetsTransform (IMDLTransformComponent This, bool value);</span>
</pre>
</div>

</div> <!-- end type MDLTransformComponent_Extensions -->
<!-- start type MDLVertexAttribute --> <div>
<h3>Type Changed: ModelIO.MDLVertexAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Time { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLVertexAttribute -->
<!-- start type MDLVertexBufferLayout --> <div>
<h3>Type Changed: ModelIO.MDLVertexBufferLayout</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLVertexBufferLayout (uint stride);</span>
</pre>
</div>

</div> <!-- end type MDLVertexBufferLayout -->
<!-- start type MDLVertexDescriptor --> <div>
<h3>Type Changed: ModelIO.MDLVertexDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLVertexDescriptor FromMetal (Metal.MTLVertexDescriptor descriptor, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAttribute (string name);</span>
</pre>
</div>

</div> <!-- end type MDLVertexDescriptor -->
<!-- start type MDLVoxelArray --> <div>
<h3>Type Changed: ModelIO.MDLVoxelArray</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLVoxelArray (MDLAsset asset, int divisions, float patchRadius);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsValidSignedShellField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ShellFieldExteriorThickness { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float ShellFieldInteriorThickness { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConvertToSignedShellField ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLMesh GetCoarseMesh ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLMesh GetCoarseMeshUsingAllocator (IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetVoxels (MDLMesh mesh, int divisions, float patchRadius);</span>
</pre>
</div>

</div> <!-- end type MDLVoxelArray -->
<div> <!-- start type IMDLLightProbeIrradianceDataSource -->
<h3>New Type ModelIO.IMDLLightProbeIrradianceDataSource</h3>
<pre class='added' data-is-non-breaking="">
public interface IMDLLightProbeIrradianceDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAxisAlignedBoundingBox BoundingBox { get; set; }</span>
}
</pre>
</div> <!-- end type IMDLLightProbeIrradianceDataSource -->
<div> <!-- start type MDLCameraProjection -->
<h3>New Type ModelIO.MDLCameraProjection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLCameraProjection {
	<span class='added added-field ' data-is-non-breaking="">Orthographic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Perspective = 0,</span>
}
</pre>
</div> <!-- end type MDLCameraProjection -->
<div> <!-- start type MDLLightProbeIrradianceDataSource -->
<h3>New Type ModelIO.MDLLightProbeIrradianceDataSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MDLLightProbeIrradianceDataSource : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLLightProbeIrradianceDataSource, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLLightProbeIrradianceDataSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLLightProbeIrradianceDataSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLLightProbeIrradianceDataSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLAxisAlignedBoundingBox BoundingBox { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SphericalHarmonicsLevel { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetSphericalHarmonicsCoefficients (OpenTK.Vector3 position);</span>
}
</pre>
</div> <!-- end type MDLLightProbeIrradianceDataSource -->
<div> <!-- start type MDLLightProbeIrradianceDataSource_Extensions -->
<h3>New Type ModelIO.MDLLightProbeIrradianceDataSource_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MDLLightProbeIrradianceDataSource_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetSphericalHarmonicsCoefficients (IMDLLightProbeIrradianceDataSource This, OpenTK.Vector3 position);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetSphericalHarmonicsLevel (IMDLLightProbeIrradianceDataSource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSphericalHarmonicsLevel (IMDLLightProbeIrradianceDataSource This, uint value);</span>
}
</pre>
</div> <!-- end type MDLLightProbeIrradianceDataSource_Extensions -->
<div> <!-- start type MDLMaterialFace -->
<h3>New Type ModelIO.MDLMaterialFace</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLMaterialFace {
	<span class='added added-field ' data-is-non-breaking="">Back = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DoubleSided = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Front = 0,</span>
}
</pre>
</div> <!-- end type MDLMaterialFace -->
<div> <!-- start type MDLMaterialPropertyConnection -->
<h3>New Type ModelIO.MDLMaterialPropertyConnection</h3>
<pre class='added' data-is-non-breaking="">
public class MDLMaterialPropertyConnection : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyConnection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyConnection (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMaterialPropertyConnection (MDLMaterialProperty output, MDLMaterialProperty input);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialProperty Input { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialProperty Output { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type MDLMaterialPropertyConnection -->
<div> <!-- start type MDLMaterialPropertyGraph -->
<h3>New Type ModelIO.MDLMaterialPropertyGraph</h3>
<pre class='added' data-is-non-breaking="">
public class MDLMaterialPropertyGraph : ModelIO.MDLMaterialPropertyNode, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyGraph (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyGraph (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMaterialPropertyGraph (MDLMaterialPropertyNode[] nodes, MDLMaterialPropertyConnection[] connections);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialPropertyConnection[] Connections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialPropertyNode[] Nodes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Evaluate ();</span>
}
</pre>
</div> <!-- end type MDLMaterialPropertyGraph -->
<div> <!-- start type MDLMaterialPropertyNode -->
<h3>New Type ModelIO.MDLMaterialPropertyNode</h3>
<pre class='added' data-is-non-breaking="">
public class MDLMaterialPropertyNode : Foundation.NSObject, Foundation.INSObjectProtocol, IMDLNamed, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MDLMaterialPropertyNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MDLMaterialPropertyNode (MDLMaterialProperty[] inputs, MDLMaterialProperty[] outputs, System.Action&lt;MDLMaterialPropertyNode&gt; function);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;MDLMaterialPropertyNode&gt; EvaluationFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialProperty[] Inputs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MDLMaterialProperty[] Outputs { get; }</span>
}
</pre>
</div> <!-- end type MDLMaterialPropertyNode -->
<div> <!-- start type MDLNoiseTextureType -->
<h3>New Type ModelIO.MDLNoiseTextureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLNoiseTextureType {
	<span class='added added-field ' data-is-non-breaking="">Cellular = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Vector = 0,</span>
}
</pre>
</div> <!-- end type MDLNoiseTextureType -->
<div> <!-- start type MDLObjectHandler -->
<h3>New Type ModelIO.MDLObjectHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MDLObjectHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MDLObjectHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MDLObject mdlObject, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (MDLObject mdlObject, bool stop);</span>
}
</pre>
</div> <!-- end type MDLObjectHandler -->
<div> <!-- start type MDLProbePlacement -->
<h3>New Type ModelIO.MDLProbePlacement</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MDLProbePlacement {
	<span class='added added-field ' data-is-non-breaking="">IrradianceDistribution = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UniformGrid = 0,</span>
}
</pre>
</div> <!-- end type MDLProbePlacement -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace MultipeerConnectivity --> <div> 
<h2>Namespace MultipeerConnectivity</h2>
<!-- start type MCBrowserViewController --> <div>
<h3>Type Changed: MultipeerConnectivity.MCBrowserViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type MCBrowserViewController -->
<!-- start type MCSession --> <div>
<h3>Type Changed: MultipeerConnectivity.MCSession</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; NearbyConnectionDataForPeerAsync (MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendResourceAsync (Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendResourceAsync (Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, Foundation.NSProgress result);</span>
</pre>
</div>

</div> <!-- end type MCSession -->

</div> <!-- end namespace MultipeerConnectivity -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NEFlowMetaData --> <div>
<h3>Type Changed: NetworkExtension.NEFlowMetaData</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NEFlowMetaData (Foundation.NSCoder coder);</span>
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
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NEFlowMetaData -->
<!-- start type NEPacketTunnelFlow --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelFlow</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadPacketObjects (System.Action&lt;NEPacket[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NEPacket[]&gt; ReadPacketObjectsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WritePacketObjects (NEPacket[] packets);</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelFlow -->
<!-- start type NEPacketTunnelNetworkSettings --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelNetworkSettings</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This constructor does not create a valid instance of the type")]
	public NEPacketTunnelNetworkSettings ();</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacketTunnelNetworkSettings (string address);</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelNetworkSettings -->
<!-- start type NEPacketTunnelProvider --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelProvider</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacketTunnelProvider ();</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelProvider -->
<!-- start type NEProvider --> <div>
<h3>Type Changed: NetworkExtension.NEProvider</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisplayMessage (string message, System.Action&lt;bool&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type NEProvider -->
<!-- start type NETunnelProviderManager --> <div>
<h3>Type Changed: NetworkExtension.NETunnelProviderManager</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NETunnelProviderManager ();</span>
</pre>
</div>

</div> <!-- end type NETunnelProviderManager -->
<!-- start type NEVpnConnection --> <div>
<h3>Type Changed: NetworkExtension.NEVpnConnection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NEVpnManager Manager { get; }</span>
</pre>
</div>

</div> <!-- end type NEVpnConnection -->
<!-- start type NEVpnIke2DiffieHellman --> <div>
<h3>Type Changed: NetworkExtension.NEVpnIke2DiffieHellman</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
</pre>
</div>

</div> <!-- end type NEVpnIke2DiffieHellman -->
<!-- start type NWBonjourServiceEndpoint --> <div>
<h3>Type Changed: NetworkExtension.NWBonjourServiceEndpoint</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NWBonjourServiceEndpoint (Foundation.NSCoder coder);</span>
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

</div> <!-- end type NWBonjourServiceEndpoint -->
<!-- start type NWEndpoint --> <div>
<h3>Type Changed: NetworkExtension.NWEndpoint</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected NWEndpoint (Foundation.NSCoder coder);</span>
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
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type NWEndpoint -->
<!-- start type NWHostEndpoint --> <div>
<h3>Type Changed: NetworkExtension.NWHostEndpoint</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NWHostEndpoint (Foundation.NSCoder coder);</span>
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

</div> <!-- end type NWHostEndpoint -->
<div> <!-- start type NEAppProxyFlowErrorExtensions -->
<h3>New Type NetworkExtension.NEAppProxyFlowErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NEAppProxyFlowErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NEAppProxyFlowError self);</span>
}
</pre>
</div> <!-- end type NEAppProxyFlowErrorExtensions -->
<div> <!-- start type NEFilterManagerErrorExtensions -->
<h3>New Type NetworkExtension.NEFilterManagerErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NEFilterManagerErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NEFilterManagerError self);</span>
}
</pre>
</div> <!-- end type NEFilterManagerErrorExtensions -->
<div> <!-- start type NEPacket -->
<h3>New Type NetworkExtension.NEPacket</h3>
<pre class='added' data-is-non-breaking="">
public class NEPacket : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacket ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacket (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NEPacket (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NEPacket (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacket (Foundation.NSData data, byte protocolFamily);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NEFlowMetaData Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual byte ProtocolFamily { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NEPacket -->
<div> <!-- start type NETunnelProviderErrorExtensions -->
<h3>New Type NetworkExtension.NETunnelProviderErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NETunnelProviderErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NETunnelProviderError self);</span>
}
</pre>
</div> <!-- end type NETunnelProviderErrorExtensions -->
<div> <!-- start type NEVpnErrorExtensions -->
<h3>New Type NetworkExtension.NEVpnErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NEVpnErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (NEVpnError self);</span>
}
</pre>
</div> <!-- end type NEVpnErrorExtensions -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace NotificationCenter --> <div> 
<h2>Namespace NotificationCenter</h2>
<!-- start type NCWidgetListViewController --> <div>
<h3>Type Changed: NotificationCenter.NCWidgetListViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NCWidgetListViewController -->
<!-- start type NCWidgetSearchViewController --> <div>
<h3>Type Changed: NotificationCenter.NCWidgetSearchViewController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type NCWidgetSearchViewController -->

</div> <!-- end namespace NotificationCenter -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.11"</span> <span class='added '>"10.12"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"2.10.0"</span> <span class='added '>"3.0.0"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string IntentsLibrary = "/System/Library/Frameworks/Intents.framework/Intents";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MediaPlayerLibrary = "/System/Library/Frameworks/MediaPlayer.framework/MediaPlayer";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string PhotosLibrary = "/System/Library/Frameworks/Photos.framework/Photos";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string SafariServicesLibrary = "/System/Library/Frameworks/SafariServices.framework/SafariServices";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type LinkWithAttribute --> <div>
<h3>Type Changed: ObjCRuntime.LinkWithAttribute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public LinkWithAttribute ();</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public DlsymOption Dlsym { get; set; }</span>
</pre>
</div>

</div> <!-- end type LinkWithAttribute -->
<!-- start type Platform --> <div>
<h3>Type Changed: ObjCRuntime.Platform</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Mac_10_12 = 2827943906639872,</span>
</pre>
</div>

</div> <!-- end type Platform -->
<div> <!-- start type DlsymOption -->
<h3>New Type ObjCRuntime.DlsymOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DlsymOption {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disabled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Required = 1,</span>
}
</pre>
</div> <!-- end type DlsymOption -->
<div> <!-- start type UserDelegateTypeAttribute -->
<h3>New Type ObjCRuntime.UserDelegateTypeAttribute</h3>
<pre class='added' data-is-non-breaking="">
public sealed class UserDelegateTypeAttribute : System.Attribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UserDelegateTypeAttribute (System.Type userDelegateType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Type UserDelegateType { get; }</span>
}
</pre>
</div> <!-- end type UserDelegateTypeAttribute -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PdfKit --> <div> 
<h2>Namespace PdfKit</h2>
<!-- start type PdfThumbnailView --> <div>
<h3>Type Changed: PdfKit.PdfThumbnailView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type PdfThumbnailView -->
<!-- start type PdfView --> <div>
<h3>Type Changed: PdfKit.PdfView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type PdfView -->

</div> <!-- end namespace PdfKit -->
<!-- start namespace QTKit --> <div> 
<h2>Namespace QTKit</h2>
<!-- start type QTCaptureView --> <div>
<h3>Type Changed: QTKit.QTCaptureView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type QTCaptureView -->
<!-- start type QTMovieView --> <div>
<h3>Type Changed: QTKit.QTMovieView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type QTMovieView -->

</div> <!-- end namespace QTKit -->
<!-- start namespace QuickLookUI --> <div> 
<h2>Namespace QuickLookUI</h2>
<!-- start type QLPreviewPanel --> <div>
<h3>Type Changed: QuickLookUI.QLPreviewPanel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type QLPreviewPanel -->

</div> <!-- end namespace QuickLookUI -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNAnimatable --> <div>
<h3>Type Changed: SceneKit.SCNAnimatable</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNAnimatable -->
<!-- start type SCNCamera --> <div>
<h3>Type Changed: SceneKit.SCNCamera</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat AverageGray { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomBlurRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomThreshold { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorFringeIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorFringeStrength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty ColorGrading { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Contrast { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureAdaptationBrighteningSpeedFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureAdaptationDarkeningSpeedFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinimumExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MotionBlurIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Saturation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat VignettingIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat VignettingPower { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsExposureAdaptation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsHdr { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat WhitePoint { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNCamera -->
<!-- start type SCNConstraint --> <div>
<h3>Type Changed: SceneKit.SCNConstraint</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNConstraint -->
<!-- start type SCNFloor --> <div>
<h3>Type Changed: SceneKit.SCNFloor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Length { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReflectionCategoryBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNFloor -->
<!-- start type SCNGeometry --> <div>
<h3>Type Changed: SceneKit.SCNGeometry</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNGeometry -->
<!-- start type SCNGeometryPrimitiveType --> <div>
<h3>Type Changed: SceneKit.SCNGeometryPrimitiveType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Polygon = 4,</span>
</pre>
</div>

</div> <!-- end type SCNGeometryPrimitiveType -->
<!-- start type SCNGeometrySourceSemantic --> <div>
<h3>Type Changed: SceneKit.SCNGeometrySourceSemantic</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Tangent { get; }</span>
</pre>
</div>

</div> <!-- end type SCNGeometrySourceSemantic -->
<!-- start type SCNHitTest --> <div>
<h3>Type Changed: SceneKit.SCNHitTest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionCategoryBitMaskKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTest -->
<!-- start type SCNHitTestResult --> <div>
<h3>Type Changed: SceneKit.SCNHitTestResult</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode BoneNode { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTestResult -->
<!-- start type SCNLight --> <div>
<h3>Type Changed: SceneKit.SCNLight</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl IesProfileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Intensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Temperature { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNLight -->
<!-- start type SCNLightType --> <div>
<h3>Type Changed: SceneKit.SCNLightType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Ies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Probe { get; }</span>
</pre>
</div>

</div> <!-- end type SCNLightType -->
<!-- start type SCNLightingModel --> <div>
<h3>Type Changed: SceneKit.SCNLightingModel</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhysicallyBased { get; }</span>
</pre>
</div>

</div> <!-- end type SCNLightingModel -->
<!-- start type SCNLookAtConstraint --> <div>
<h3>Type Changed: SceneKit.SCNLookAtConstraint</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual SCNNode Target { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type SCNLookAtConstraint -->
<!-- start type SCNMaterial --> <div>
<h3>Type Changed: SceneKit.SCNMaterial</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty Metalness { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty Roughness { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMaterial -->
<!-- start type SCNMaterialProperty --> <div>
<h3>Type Changed: SceneKit.SCNMaterialProperty</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMaterialProperty -->
<!-- start type SCNMorpher --> <div>
<h3>Type Changed: SceneKit.SCNMorpher</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMorpher -->
<!-- start type SCNNode --> <div>
<h3>Type Changed: SceneKit.SCNNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMovabilityHint MovabilityHint { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload that takes a SCNNodeHandler instead")]
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateChildNodes (SCNNodeHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateHierarchy (SCNNodeHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNNode -->
<!-- start type SCNParticleProperty --> <div>
<h3>Type Changed: SceneKit.SCNParticleProperty</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContactNormal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContactPoint { get; }</span>
</pre>
</div>

</div> <!-- end type SCNParticleProperty -->
<!-- start type SCNParticleSystem --> <div>
<h3>Type Changed: SceneKit.SCNParticleSystem</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNParticleSystem -->
<!-- start type SCNPhysicsShapeOptionsKeys --> <div>
<h3>Type Changed: SceneKit.SCNPhysicsShapeOptionsKeys</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollisionMargin { get; }</span>
</pre>
</div>

</div> <!-- end type SCNPhysicsShapeOptionsKeys -->
<!-- start type SCNProgramDelegate --> <div>
<h3>Type Changed: SceneKit.SCNProgramDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool BindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsProgramOpaque (SCNProgram program);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnbindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);</span>
</pre>
</div>

</div> <!-- end type SCNProgramDelegate -->
<!-- start type SCNProgramDelegate_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNProgramDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);</span>
</pre>
</div>

</div> <!-- end type SCNProgramDelegate_Extensions -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SCNRenderer FromContext (OpenGL.CGLContext context, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSImage GetSnapshot (double time, CoreGraphics.CGSize size, SCNAntialiasingMode antialiasingMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SCNNode[] lightProbes, double time);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNScene --> <div>
<h3>Type Changed: SceneKit.SCNScene</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty LightingEnvironment { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ISCNSceneExportDelegate overload instead")]
	public virtual bool WriteToUrl (Foundation.NSUrl url, Foundation.NSDictionary options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ISCNSceneExportDelegate overload instead")]
	public virtual bool WriteToUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> bool WriteToUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WriteToUrl (Foundation.NSUrl url, Foundation.NSDictionary options, ISCNSceneExportDelegate aDelegate, SCNSceneExportProgressHandler exportProgressHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool WriteToUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, ISCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);</span>
</pre>
</div>

</div> <!-- end type SCNScene -->
<!-- start type SCNSceneExportDelegate --> <div>
<h3>Type Changed: SceneKit.SCNSceneExportDelegate</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public virtual Foundation.NSUrl WriteImage (AppKit.NSImage image, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>documentURL</span> <span class='added '>documentUrl</span>, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>originalImageURL</span> <span class='added '>originalImageUrl</span>)
</div></pre>

</div> <!-- end type SCNSceneExportDelegate -->
<!-- start type SCNSceneExportDelegate_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNSceneExportDelegate_Extensions</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public Foundation.NSUrl WriteImage (this ISCNSceneExportDelegate This, AppKit.NSImage image, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>documentURL</span> <span class='added '>documentUrl</span>, Foundation.NSUrl <span class='removed removed-inline removed-breaking-inline'>originalImageURL</span> <span class='added '>originalImageUrl</span>)
</div></pre>

</div> <!-- end type SCNSceneExportDelegate_Extensions -->
<!-- start type SCNSceneLoadingOptions --> <div>
<h3>Type Changed: SceneKit.SCNSceneLoadingOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? PreserveOriginalTopology { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneLoadingOptions -->
<!-- start type SCNSceneSourceLoading --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceLoading</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionPreserveOriginalTopology { get; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneSourceLoading -->
<!-- start type SCNSceneSourceProperties --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetAuthorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetAuthoringToolKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetUnitMeterKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetUnitNameKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneSourceProperties -->
<!-- start type SCNTechnique --> <div>
<h3>Type Changed: SceneKit.SCNTechnique</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNTechnique -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PreferredFramesPerSecond { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNView -->
<div> <!-- start type SCNAnimatable_Extensions -->
<h3>New Type SceneKit.SCNAnimatable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNAnimatable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void SetSpeed (ISCNAnimatable This, nfloat speed, Foundation.NSString key);</span>
}
</pre>
</div> <!-- end type SCNAnimatable_Extensions -->
<div> <!-- start type SCNMovabilityHint -->
<h3>New Type SceneKit.SCNMovabilityHint</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNMovabilityHint {
	<span class='added added-field ' data-is-non-breaking="">Fixed = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Movable = 1,</span>
}
</pre>
</div> <!-- end type SCNMovabilityHint -->
<div> <!-- start type SCNNodeHandler -->
<h3>New Type SceneKit.SCNNodeHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SCNNodeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNNodeHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (SCNNode node, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (SCNNode node, bool stop);</span>
}
</pre>
</div> <!-- end type SCNNodeHandler -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecKey --> <div>
<h3>Type Changed: Security.SecKey</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SecKey Create (Foundation.NSData keyData, Foundation.NSDictionary parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKey Create (Foundation.NSData keyData, SecKeyType keyType, SecKeyClass keyClass, int keySizeInBits, Foundation.NSDictionary parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData CreateDecryptedData (SecKeyAlgorithm algorithm, Foundation.NSData ciphertext, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData CreateEncryptedData (SecKeyAlgorithm algorithm, Foundation.NSData plaintext, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKey CreateRandomKey (Foundation.NSDictionary parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKey CreateRandomKey (SecKeyType keyType, int keySizeInBits, Foundation.NSDictionary parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData CreateSignature (SecKeyAlgorithm algorithm, Foundation.NSData dataToSign, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary GetAttributes ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetExternalRepresentation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetExternalRepresentation (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetKeyExchangeResult (SecKeyAlgorithm algorithm, SecKey publicKey, Foundation.NSDictionary parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetKeyExchangeResult (SecKeyAlgorithm algorithm, SecKey publicKey, SecKeyKeyExchangeParameter parameters, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public SecKey GetPublicKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IsAlgorithmSupported (SecKeyOperationType operation, SecKeyAlgorithm algorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool VerifySignature (SecKeyAlgorithm algorithm, Foundation.NSData signedData, Foundation.NSData signature, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type SecKey -->
<!-- start type SecKeyType --> <div>
<h3>Type Changed: Security.SecKeyType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ECSecPrimeRandom = 2,</span>
</pre>
</div>

</div> <!-- end type SecKeyType -->
<!-- start type SecPolicyIdentifier --> <div>
<h3>Type Changed: Security.SecPolicyIdentifier</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApplePassbookSigning { get; }</span>
</pre>
</div>

</div> <!-- end type SecPolicyIdentifier -->
<!-- start type SecPolicyPropertyKey --> <div>
<h3>Type Changed: Security.SecPolicyPropertyKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TeamIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type SecPolicyPropertyKey -->
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecCertificate certificate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecIdentity identity);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecRecord (SecKey key);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public LocalAuthentication.LAContext AuthenticationContext { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public SecCertificate GetCertificate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SecIdentity GetIdentity ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SecKey GetKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (SecCertificate cert);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetIdentity (SecIdentity identity);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetKey (SecKey key);</span>
</pre>
</div>

</div> <!-- end type SecRecord -->
<!-- start type SecTrustResultKey --> <div>
<h3>Type Changed: Security.SecTrustResultKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CertificateTransparency { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CertificateTransparencyWhiteList { get; }</span>
</pre>
</div>

</div> <!-- end type SecTrustResultKey -->
<!-- start type SslContext --> <div>
<h3>Type Changed: Security.SslContext</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("SetSessionStrengthPolicy is not available anymore.")]
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public string GetRequestedPeerName ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int ReHandshake ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetSessionConfig (Foundation.NSString config);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetSessionConfig (SslSessionConfig config);</span>
</pre>
</div>

</div> <!-- end type SslContext -->
<!-- start type SslSessionOption --> <div>
<h3>Type Changed: Security.SslSessionOption</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AllowRenegotiation = 8,</span>
</pre>
</div>

</div> <!-- end type SslSessionOption -->
<div> <!-- start type SecKeyAlgorithm -->
<h3>New Type Security.SecKeyAlgorithm</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SecKeyAlgorithm {
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactor = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactorX963Sha1 = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactorX963Sha224 = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactorX963Sha256 = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactorX963Sha384 = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeCofactorX963Sha512 = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandard = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandardX963Sha1 = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandardX963Sha224 = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandardX963Sha256 = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandardX963Sha384 = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdhKeyExchangeStandardX963Sha512 = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962Sha1 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962Sha224 = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962Sha256 = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962Sha384 = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureDigestX962Sha512 = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureMessageX962Sha1 = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureMessageX962Sha224 = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureMessageX962Sha256 = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureMessageX962Sha384 = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureMessageX962Sha512 = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">EcdsaSignatureRfc4754 = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorX963Sha1AesGcm = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorX963Sha224AesGcm = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorX963Sha256AesGcm = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorX963Sha384AesGcm = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorX963Sha512AesGcm = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardX963Sha1AesGcm = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardX963Sha224AesGcm = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardX963Sha256AesGcm = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardX963Sha384AesGcm = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardX963Sha512AesGcm = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha1 = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha1AesCgm = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha224 = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha224AesGcm = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha256 = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha256AesGcm = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha384 = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha384AesGcm = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha512 = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionOaepSha512AesGcm = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionPkcs1 = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaEncryptionRaw = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Raw = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Sha1 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Sha224 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Sha256 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Sha384 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPkcs1v15Sha512 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePkcs1v15Sha1 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePkcs1v15Sha224 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePkcs1v15Sha256 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePkcs1v15Sha384 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePkcs1v15Sha512 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureRaw = 0,</span>
}
</pre>
</div> <!-- end type SecKeyAlgorithm -->
<div> <!-- start type SecKeyAlgorithmExtensions -->
<h3>New Type Security.SecKeyAlgorithmExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecKeyAlgorithmExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SecKeyAlgorithm self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKeyAlgorithm GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SecKeyAlgorithmExtensions -->
<div> <!-- start type SecKeyClassExtensions -->
<h3>New Type Security.SecKeyClassExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecKeyClassExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SecKeyClass self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKeyClass GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SecKeyClassExtensions -->
<div> <!-- start type SecKeyKeyExchangeParameter -->
<h3>New Type Security.SecKeyKeyExchangeParameter</h3>
<pre class='added' data-is-non-breaking="">
public class SecKeyKeyExchangeParameter : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SecKeyKeyExchangeParameter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SecKeyKeyExchangeParameter (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int? RequestedSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData SharedInfo { get; set; }</span>
}
</pre>
</div> <!-- end type SecKeyKeyExchangeParameter -->
<div> <!-- start type SecKeyOperationType -->
<h3>New Type Security.SecKeyOperationType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SecKeyOperationType {
	<span class='added added-field ' data-is-non-breaking="">Decrypt = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Encrypt = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyExchange = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Sign = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Verify = 1,</span>
}
</pre>
</div> <!-- end type SecKeyOperationType -->
<div> <!-- start type SecKeyTypeExtensions -->
<h3>New Type Security.SecKeyTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SecKeyTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SecKeyType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecKeyType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SecKeyTypeExtensions -->
<div> <!-- start type SslSessionConfig -->
<h3>New Type Security.SslSessionConfig</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SslSessionConfig {
	<span class='added added-field ' data-is-non-breaking="">Anonymous = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Ats1 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Ats1NoPfs = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Legacy = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LegacyDhe = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">RC4Fallback = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Standard = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreeDesFallback = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1Fallback = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1RC4Fallback = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1ThreeDesFallback = 11,</span>
}
</pre>
</div> <!-- end type SslSessionConfig -->
<div> <!-- start type SslSessionConfigExtensions -->
<h3>New Type Security.SslSessionConfigExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SslSessionConfigExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SslSessionConfig self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SslSessionConfig GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SslSessionConfigExtensions -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SK3DNode --> <div>
<h3>Type Changed: SpriteKit.SK3DNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SK3DNode -->
<!-- start type SKAction --> <div>
<h3>Type Changed: SpriteKit.SKAction</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction Animate (SKWarpGeometry[] warps, Foundation.NSNumber[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction Animate (SKWarpGeometry[] warps, Foundation.NSNumber[] times, bool restore);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction ScaleTo (CoreGraphics.CGSize size, double sec);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction WarpTo (SKWarpGeometry warp, double duration);</span>
</pre>
</div>

</div> <!-- end type SKAction -->
<!-- start type SKAudioNode --> <div>
<h3>Type Changed: SpriteKit.SKAudioNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKAudioNode -->
<!-- start type SKCameraNode --> <div>
<h3>Type Changed: SpriteKit.SKCameraNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKCameraNode -->
<!-- start type SKCropNode --> <div>
<h3>Type Changed: SpriteKit.SKCropNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKCropNode -->
<!-- start type SKEffectNode --> <div>
<h3>Type Changed: SpriteKit.SKEffectNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type SKEffectNode -->
<!-- start type SKEmitterNode --> <div>
<h3>Type Changed: SpriteKit.SKEmitterNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKEmitterNode -->
<!-- start type SKFieldNode --> <div>
<h3>Type Changed: SpriteKit.SKFieldNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKFieldNode -->
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<!-- start type SKLightNode --> <div>
<h3>Type Changed: SpriteKit.SKLightNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKLightNode -->
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKPolygonObstacle[] GetObstaclesFromNodeBounds (SKNode[] nodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKPolygonObstacle[] GetObstaclesFromNodePhysicsBodies (SKNode[] nodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GameplayKit.GKPolygonObstacle[] GetObstaclesFromSpriteTextures (SKNode[] sprites, float accuracy);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKReferenceNode --> <div>
<h3>Type Changed: SpriteKit.SKReferenceNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKReferenceNode -->
<!-- start type SKScene --> <div>
<h3>Type Changed: SpriteKit.SKScene</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SceneDidLoad ();</span>
</pre>
</div>

</div> <!-- end type SKScene -->
<!-- start type SKShader --> <div>
<h3>Type Changed: SpriteKit.SKShader</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKAttribute[] Attributes { get; set; }</span>
</pre>
</div>

</div> <!-- end type SKShader -->
<!-- start type SKShapeNode --> <div>
<h3>Type Changed: SpriteKit.SKShapeNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKShapeNode -->
<!-- start type SKSpriteNode --> <div>
<h3>Type Changed: SpriteKit.SKSpriteNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScaleTo (CoreGraphics.CGSize size);</span>
</pre>
</div>

</div> <!-- end type SKSpriteNode -->
<!-- start type SKTexture --> <div>
<h3>Type Changed: SpriteKit.SKTexture</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKTexture FromNoiseMap (GameplayKit.GKNoiseMap noiseMap);</span>
</pre>
</div>

</div> <!-- end type SKTexture -->
<!-- start type SKVideoNode --> <div>
<h3>Type Changed: SpriteKit.SKVideoNode</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type SKVideoNode -->
<!-- start type SKView --> <div>
<h3>Type Changed: SpriteKit.SKView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISKViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PreferredFramesPerSecond { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type SKView -->
<div> <!-- start type ISKViewDelegate -->
<h3>New Type SpriteKit.ISKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISKViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISKViewDelegate -->
<div> <!-- start type ISKWarpable -->
<h3>New Type SpriteKit.ISKWarpable</h3>
<pre class='added' data-is-non-breaking="">
public interface ISKWarpable : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
}
</pre>
</div> <!-- end type ISKWarpable -->
<div> <!-- start type SKAttribute -->
<h3>New Type SpriteKit.SKAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class SKAttribute : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttribute (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttribute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttribute (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttribute (string name, SKAttributeType type);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKAttributeType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKAttribute Create (string name, SKAttributeType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKAttribute -->
<div> <!-- start type SKAttributeType -->
<h3>New Type SpriteKit.SKAttributeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKAttributeType {
	<span class='added added-field ' data-is-non-breaking="">Float = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HalfFloat = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat2 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat3 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat4 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat4 = 8,</span>
}
</pre>
</div> <!-- end type SKAttributeType -->
<div> <!-- start type SKAttributeValue -->
<h3>New Type SpriteKit.SKAttributeValue</h3>
<pre class='added' data-is-non-breaking="">
public class SKAttributeValue : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttributeValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttributeValue (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttributeValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttributeValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float FloatValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2 VectorFloat2Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 VectorFloat3Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector4 VectorFloat4Value { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (float value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKAttributeValue -->
<div> <!-- start type SKTileAdjacencyMask -->
<h3>New Type SpriteKit.SKTileAdjacencyMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileAdjacencyMask {
	<span class='added added-field ' data-is-non-breaking="">All = 255,</span>
	<span class='added added-field ' data-is-non-breaking="">Down = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">DownEdge = 199,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatAll = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatDown = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatLowerLeft = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatLowerRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUp = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUpperLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyAll = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLowerLeft = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLowerRight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyUpperLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyUpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">LeftEdge = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeftCorner = 253,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeftEdge = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRightCorner = 127,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRightEdge = 193,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RightEdge = 241,</span>
	<span class='added added-field ' data-is-non-breaking="">Up = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UpEdge = 124,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeft = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeftCorner = 247,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeftEdge = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRightCorner = 223,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRightEdge = 112,</span>
}
</pre>
</div> <!-- end type SKTileAdjacencyMask -->
<div> <!-- start type SKTileDefinition -->
<h3>New Type SpriteKit.SKTileDefinition</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileDefinition : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileDefinition (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileDefinition (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture, CoreGraphics.CGSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture, SKTexture normalTexture, CoreGraphics.CGSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture[] textures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture[] textures, SKTexture[] normalTextures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipHorizontally { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipVertically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTexture[] NormalTextures { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PlacementWeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileDefinitionRotation Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTexture[] Textures { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TimePerFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSMutableDictionary UserData { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture, CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture, SKTexture normalTexture, CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture[] textures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture[] textures, SKTexture[] normalTextures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileDefinition -->
<div> <!-- start type SKTileDefinitionRotation -->
<h3>New Type SpriteKit.SKTileDefinitionRotation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileDefinitionRotation {
	<span class='added added-field ' data-is-non-breaking="">Angle0 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle180 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle270 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle90 = 1,</span>
}
</pre>
</div> <!-- end type SKTileDefinitionRotation -->
<div> <!-- start type SKTileGroup -->
<h3>New Type SpriteKit.SKTileGroup</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileGroup : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (SKTileDefinition tileDefinition);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (SKTileGroupRule[] rules);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroupRule[] Rules { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup Create (SKTileDefinition tileDefinition);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup Create (SKTileGroupRule[] rules);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup CreateEmpty ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileGroup -->
<div> <!-- start type SKTileGroupRule -->
<h3>New Type SpriteKit.SKTileGroupRule</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileGroupRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroupRule (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroupRule (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule (SKTileAdjacencyMask adjacency, SKTileDefinition[] tileDefinitions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileAdjacencyMask Adjacency { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileDefinition[] TileDefinitions { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroupRule Create (SKTileAdjacencyMask adjacency, SKTileDefinition[] tileDefinitions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileGroupRule -->
<div> <!-- start type SKTileMapNode -->
<h3>New Type SpriteKit.SKTileMapNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileMapNode : SpriteKit.SKNode, AppKit.INSTouchBarProvider, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileMapNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileMapNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup tileGroup);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup[] tileGroupLayout);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKBlendMode BlendMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AppKit.NSColor Color { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorBlendFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EnableAutomapping { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint LightingBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize MapSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKShader Shader { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileSet TileSet { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize TileSize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup tileGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup[] tileGroupLayout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Fill (SKTileGroup tileGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode[] FromTileSet (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, GameplayKit.GKNoiseMap noiseMap, Foundation.NSNumber[] thresholds);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetCenterOfTile (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetTileColumnIndex (CoreGraphics.CGPoint position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKTileDefinition GetTileDefinition (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKTileGroup GetTileGroup (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetTileRowIndex (CoreGraphics.CGPoint position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTileGroup (SKTileGroup tileGroup, uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTileGroup (SKTileGroup tileGroup, SKTileDefinition tileDefinition, uint column, uint row);</span>
}
</pre>
</div> <!-- end type SKTileMapNode -->
<div> <!-- start type SKTileSet -->
<h3>New Type SpriteKit.SKTileSet</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileSet : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileSet (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (SKTileGroup[] tileGroups);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileSet (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (SKTileGroup[] tileGroups, SKTileSetType tileSetType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroup DefaultTileGroup { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize DefaultTileSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroup[] TileGroups { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileSetType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet Create (SKTileGroup[] tileGroups);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet Create (SKTileGroup[] tileGroups, SKTileSetType tileSetType);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet FromUrl (Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type SKTileSet -->
<div> <!-- start type SKTileSetType -->
<h3>New Type SpriteKit.SKTileSetType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileSetType {
	<span class='added added-field ' data-is-non-breaking="">Grid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">HexagonalFlat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HexagonalPointy = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Isometric = 1,</span>
}
</pre>
</div> <!-- end type SKTileSetType -->
<div> <!-- start type SKViewDelegate -->
<h3>New Type SpriteKit.SKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SKViewDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISKViewDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRender (SKView view, double time);</span>
}
</pre>
</div> <!-- end type SKViewDelegate -->
<div> <!-- start type SKViewDelegate_Extensions -->
<h3>New Type SpriteKit.SKViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldRender (ISKViewDelegate This, SKView view, double time);</span>
}
</pre>
</div> <!-- end type SKViewDelegate_Extensions -->
<div> <!-- start type SKWarpGeometry -->
<h3>New Type SpriteKit.SKWarpGeometry</h3>
<pre class='added' data-is-non-breaking="">
public class SKWarpGeometry : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometry ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometry (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometry (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometry (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKWarpGeometry -->
<div> <!-- start type SKWarpGeometryGrid -->
<h3>New Type SpriteKit.SKWarpGeometryGrid</h3>
<pre class='added' data-is-non-breaking="">
public class SKWarpGeometryGrid : SpriteKit.SKWarpGeometry, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometryGrid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometryGrid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometryGrid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometryGrid (nint cols, nint rows, OpenTK.Vector2[] sourcePositions, OpenTK.Vector2[] destPositions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfRows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint VertexCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid Create (nint cols, nint rows);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid Create (nint cols, nint rows, OpenTK.Vector2[] sourcePositions, OpenTK.Vector2[] destPositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetDestPosition (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid GetGrid ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SKWarpGeometryGrid GetGridByReplacingDestPositions (OpenTK.Vector2[] destPositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public SKWarpGeometryGrid GetGridByReplacingSourcePositions (OpenTK.Vector2[] sourcePositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetSourcePosition (nint index);</span>
}
</pre>
</div> <!-- end type SKWarpGeometryGrid -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceCapability --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceCapability</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MusicCatalogSubscriptionEligible = 2,</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceCapability -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace VideoToolbox --> <div> 
<h2>Namespace VideoToolbox</h2>
<!-- start type VTStatus --> <div>
<h3>Type Changed: VideoToolbox.VTStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorCorrectionImageRotationFailed = -12219,</span>
</pre>
</div>

</div> <!-- end type VTStatus -->

</div> <!-- end namespace VideoToolbox -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKPreferences --> <div>
<h3>Type Changed: WebKit.WKPreferences</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WKPreferences (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type WKPreferences -->
<!-- start type WKProcessPool --> <div>
<h3>Type Changed: WebKit.WKProcessPool</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WKProcessPool (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type WKProcessPool -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WKUserContentController (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebView --> <div>
<h3>Type Changed: WebKit.WKWebView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Security.SecTrust ServerTrust { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebView -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WKWebViewConfiguration (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKAudiovisualMediaTypes MediaTypesRequiringUserActionForPlayback { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WKWebsiteDataStore (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WebFrame --> <div>
<h3>Type Changed: WebKit.WebFrame</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual JavaScriptCore.JSContext JavaScriptContext { get; }</span>
</pre>
</div>

</div> <!-- end type WebFrame -->
<!-- start type WebFrameLoadDelegate --> <div>
<h3>Type Changed: WebKit.WebFrameLoadDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidCreateJavaScriptContext (WebView webView, JavaScriptCore.JSContext context, WebFrame frame);</span>
</pre>
</div>

</div> <!-- end type WebFrameLoadDelegate -->
<!-- start type WebFrameLoadDelegate_Extensions --> <div>
<h3>Type Changed: WebKit.WebFrameLoadDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidCreateJavaScriptContext (IWebFrameLoadDelegate This, WebView webView, JavaScriptCore.JSContext context, WebFrame frame);</span>
</pre>
</div>

</div> <!-- end type WebFrameLoadDelegate_Extensions -->
<!-- start type WebFrameView --> <div>
<h3>Type Changed: WebKit.WebFrameView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>

</div> <!-- end type WebFrameView -->
<!-- start type WebScriptObject --> <div>
<h3>Type Changed: WebKit.WebScriptObject</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual JavaScriptCore.JSValue JSValue { get; }</span>
</pre>
</div>

</div> <!-- end type WebScriptObject -->
<!-- start type WebView --> <div>
<h3>Type Changed: WebKit.WebView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">AppKit.INSTouchBarProvider</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;WebFrameJavaScriptContextEventArgs&gt; DidCreateJavaScriptContext;</span>
</pre>
</div>

</div> <!-- end type WebView -->
<div> <!-- start type WKAudiovisualMediaTypes -->
<h3>New Type WebKit.WKAudiovisualMediaTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum WKAudiovisualMediaTypes {
	<span class='added added-field ' data-is-non-breaking="">All = 18446744073709551615,</span>
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type WKAudiovisualMediaTypes -->
<div> <!-- start type WebFrameJavaScriptContextEventArgs -->
<h3>New Type WebKit.WebFrameJavaScriptContextEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class WebFrameJavaScriptContextEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public WebFrameJavaScriptContextEventArgs (JavaScriptCore.JSContext context, WebFrame frame);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public JavaScriptCore.JSContext Context { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public WebFrame Frame { get; set; }</span>
}
</pre>
</div> <!-- end type WebFrameJavaScriptContextEventArgs -->

</div> <!-- end namespace WebKit -->
<!-- start namespace Intents --> <div> 
<h2>New Namespace Intents</h2>

<div> <!-- start type IINCallsDomainHandling -->
<h3>New Type Intents.IINCallsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCallsDomainHandling : IINSearchCallHistoryIntentHandling, IINStartAudioCallIntentHandling, IINStartVideoCallIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINCallsDomainHandling -->
<div> <!-- start type IINSearchCallHistoryIntentHandling -->
<h3>New Type Intents.IINSearchCallHistoryIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchCallHistoryIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchCallHistory (INSearchCallHistoryIntent intent, System.Action&lt;INSearchCallHistoryIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchCallHistoryIntentHandling -->
<div> <!-- start type IINSearchForMessagesIntentHandling -->
<h3>New Type Intents.IINSearchForMessagesIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForMessagesIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchForMessages (INSearchForMessagesIntent intent, System.Action&lt;INSearchForMessagesIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchForMessagesIntentHandling -->
<div> <!-- start type IINSendMessageIntentHandling -->
<h3>New Type Intents.IINSendMessageIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSendMessageIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSendMessage (INSendMessageIntent intent, System.Action&lt;INSendMessageIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSendMessageIntentHandling -->
<div> <!-- start type IINSpeakable -->
<h3>New Type Intents.IINSpeakable</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSpeakable : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
}
</pre>
</div> <!-- end type IINSpeakable -->
<div> <!-- start type IINStartAudioCallIntentHandling -->
<h3>New Type Intents.IINStartAudioCallIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINStartAudioCallIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleStartAudioCall (INStartAudioCallIntent intent, System.Action&lt;INStartAudioCallIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINStartAudioCallIntentHandling -->
<div> <!-- start type IINStartVideoCallIntentHandling -->
<h3>New Type Intents.IINStartVideoCallIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINStartVideoCallIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleStartVideoCall (INStartVideoCallIntent intent, System.Action&lt;INStartVideoCallIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINStartVideoCallIntentHandling -->
<div> <!-- start type INCallCapabilityOptions -->
<h3>New Type Intents.INCallCapabilityOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INCallCapabilityOptions {
	<span class='added added-field ' data-is-non-breaking="">AudioCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoCall = 2,</span>
}
</pre>
</div> <!-- end type INCallCapabilityOptions -->
<div> <!-- start type INCallRecordType -->
<h3>New Type Intents.INCallRecordType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallRecordType {
	<span class='added added-field ' data-is-non-breaking="">Missed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INCallRecordType -->
<div> <!-- start type INCallRecordTypeResolutionResult -->
<h3>New Type Intents.INCallRecordTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecordTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult GetConfirmationRequired (INCallRecordType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult GetSuccess (INCallRecordType resolvedValue);</span>
}
</pre>
</div> <!-- end type INCallRecordTypeResolutionResult -->
<div> <!-- start type INConditionalOperator -->
<h3>New Type Intents.INConditionalOperator</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INConditionalOperator {
	<span class='added added-field ' data-is-non-breaking="">All = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 2,</span>
}
</pre>
</div> <!-- end type INConditionalOperator -->
<div> <!-- start type INDateComponentsRange -->
<h3>New Type Intents.INDateComponentsRange</h3>
<pre class='added' data-is-non-breaking="">
public class INDateComponentsRange : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRange (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSDateComponents startDateComponents, Foundation.NSDateComponents endDateComponents);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents EndDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents StartDateComponents { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INDateComponentsRange -->
<div> <!-- start type INDateComponentsRangeResolutionResult -->
<h3>New Type Intents.INDateComponentsRangeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INDateComponentsRangeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRangeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRangeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetConfirmationRequired (INDateComponentsRange dateComponentsRangeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetDisambiguation (INDateComponentsRange[] dateComponentsRangesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetSuccess (INDateComponentsRange resolvedDateComponentsRange);</span>
}
</pre>
</div> <!-- end type INDateComponentsRangeResolutionResult -->
<div> <!-- start type INImage -->
<h3>New Type Intents.INImage</h3>
<pre class='added' data-is-non-breaking="">
public class INImage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INImage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromData (Foundation.NSData imageData);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromUrl (Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type INImage -->
<div> <!-- start type INIntent -->
<h3>New Type Intents.INIntent</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString IdentifierString { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INIntent -->
<div> <!-- start type INIntentErrorCode -->
<h3>New Type Intents.INIntentErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentErrorCode {
	<span class='added added-field ' data-is-non-breaking="">DeletingAllInteractions = 1902,</span>
	<span class='added added-field ' data-is-non-breaking="">DeletingInteractionWithGroupIdentifier = 1904,</span>
	<span class='added added-field ' data-is-non-breaking="">DeletingInteractionWithIdentifiers = 1903,</span>
	<span class='added added-field ' data-is-non-breaking="">DonatingInteraction = 1901,</span>
	<span class='added added-field ' data-is-non-breaking="">IntentSupportedByMultipleExtension = 2001,</span>
	<span class='added added-field ' data-is-non-breaking="">InteractionOperationNotSupported = 1900,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIntentName = 2004,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidUserVocabularyFileLocation = 4000,</span>
	<span class='added added-field ' data-is-non-breaking="">NoHandlerProvidedForIntent = 2003,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestTimedOut = 3001,</span>
	<span class='added added-field ' data-is-non-breaking="">RestrictedIntentsNotSupportedByExtension = 2002,</span>
}
</pre>
</div> <!-- end type INIntentErrorCode -->
<div> <!-- start type INIntentErrorCodeExtensions -->
<h3>New Type Intents.INIntentErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INIntentErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (INIntentErrorCode self);</span>
}
</pre>
</div> <!-- end type INIntentErrorCodeExtensions -->
<div> <!-- start type INIntentHandlingStatus -->
<h3>New Type Intents.INIntentHandlingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentHandlingStatus {
	<span class='added added-field ' data-is-non-breaking="">DeferredToApplication = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INIntentHandlingStatus -->
<div> <!-- start type INIntentIdentifier -->
<h3>New Type Intents.INIntentIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentIdentifier {
	<span class='added added-field ' data-is-non-breaking="">CancelWorkout = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">EndWorkout = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">GetRideStatus = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ListRideOptions = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">PauseWorkout = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestPayment = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestRide = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ResumeWorkout = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">SaveProfileInCar = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchCallHistory = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchForMessages = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchForPhotos = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">SendMessage = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">SendPayment = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">SetAudioSourceInCar = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SetClimateSettingsInCar = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SetDefrosterSettingsInCar = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">SetMessageAttribute = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">SetProfileInCar = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SetRadioStation = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">SetSeatSettingsInCar = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">StartAudioCall = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">StartPhotoPlayback = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">StartVideoCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StartWorkout = 9,</span>
}
</pre>
</div> <!-- end type INIntentIdentifier -->
<div> <!-- start type INIntentResolutionResult -->
<h3>New Type Intents.INIntentResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntentResolutionResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult Unsupported { get; }</span>
}
</pre>
</div> <!-- end type INIntentResolutionResult -->
<div> <!-- start type INIntentResolutionResult`1 -->
<h3>New Type Intents.INIntentResolutionResult`1</h3>
<pre class='added' data-is-non-breaking="">
public sealed class INIntentResolutionResult`1 : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
}
</pre>
</div> <!-- end type INIntentResolutionResult`1 -->
<div> <!-- start type INIntentResponse -->
<h3>New Type Intents.INIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntentResponse : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity UserActivity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INIntentResponse -->
<div> <!-- start type INInteraction -->
<h3>New Type Intents.INInteraction</h3>
<pre class='added' data-is-non-breaking="">
public class INInteraction : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INInteraction (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INInteraction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INInteraction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INInteraction (INIntent intent, INIntentResponse response);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateInterval DateInterval { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INInteractionDirection Direction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GroupIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntent Intent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntentHandlingStatus IntentHandlingStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntentResponse IntentResponse { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteAllInteractions (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteAllInteractionsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteGroupedInteractions (string groupIdentifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteGroupedInteractionsAsync (string groupIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteInteractions (string[] identifiers, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteInteractionsAsync (string[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DonateInteraction (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DonateInteractionAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INInteraction -->
<div> <!-- start type INInteractionDirection -->
<h3>New Type Intents.INInteractionDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INInteractionDirection {
	<span class='added added-field ' data-is-non-breaking="">Incoming = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INInteractionDirection -->
<div> <!-- start type INMessage -->
<h3>New Type Intents.INMessage</h3>
<pre class='added' data-is-non-breaking="">
public class INMessage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate DateSent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Sender { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INMessage -->
<div> <!-- start type INMessageAttribute -->
<h3>New Type Intents.INMessageAttribute</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INMessageAttribute {
	<span class='added added-field ' data-is-non-breaking="">Flagged = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unflagged = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unread = 2,</span>
}
</pre>
</div> <!-- end type INMessageAttribute -->
<div> <!-- start type INMessageAttributeOptions -->
<h3>New Type Intents.INMessageAttributeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INMessageAttributeOptions {
	<span class='added added-field ' data-is-non-breaking="">Flagged = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unflagged = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Unread = 2,</span>
}
</pre>
</div> <!-- end type INMessageAttributeOptions -->
<div> <!-- start type INMessageAttributeOptionsResolutionResult -->
<h3>New Type Intents.INMessageAttributeOptionsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INMessageAttributeOptionsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeOptionsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeOptionsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult GetConfirmationRequired (INMessageAttributeOptions valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult GetSuccess (INMessageAttributeOptions resolvedValue);</span>
}
</pre>
</div> <!-- end type INMessageAttributeOptionsResolutionResult -->
<div> <!-- start type INMessageAttributeResolutionResult -->
<h3>New Type Intents.INMessageAttributeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INMessageAttributeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeResolutionResult GetConfirmationRequired (INMessageAttribute valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeResolutionResult GetSuccess (INMessageAttribute resolvedValue);</span>
}
</pre>
</div> <!-- end type INMessageAttributeResolutionResult -->
<div> <!-- start type INPerson -->
<h3>New Type Intents.INPerson</h3>
<pre class='added' data-is-non-breaking="">
public class INPerson : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IINSpeakable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPerson (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPerson (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (INPersonHandle personHandle, Foundation.NSPersonNameComponents nameComponents, string displayName, INImage image, string contactIdentifier, string customIdentifier);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (INPersonHandle personHandle, Foundation.NSPersonNameComponents nameComponents, string displayName, INImage image, string contactIdentifier, string customIdentifier, INPersonHandle[] aliases, INPersonSuggestionType suggestionType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandle[] Aliases { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContactIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPersonNameComponents NameComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandle PersonHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public INPersonRelationship Relationship { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonSuggestionType SuggestionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakRelationship { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPerson -->
<div> <!-- start type INPersonHandle -->
<h3>New Type Intents.INPersonHandle</h3>
<pre class='added' data-is-non-breaking="">
public class INPersonHandle : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (string value, INPersonHandleType type);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (string value, INPersonHandleType type, Foundation.NSString stringLabel);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (string value, INPersonHandleType type, INPersonHandleLabel label);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public INPersonHandleLabel Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandleType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakLabel { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPersonHandle -->
<div> <!-- start type INPersonHandleLabel -->
<h3>New Type Intents.INPersonHandleLabel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonHandleLabel {
	<span class='added added-field ' data-is-non-breaking="">Home = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeFax = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Main = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Mobile = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Other = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Pager = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Work = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WorkFax = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">iPhone = 3,</span>
}
</pre>
</div> <!-- end type INPersonHandleLabel -->
<div> <!-- start type INPersonHandleLabelExtensions -->
<h3>New Type Intents.INPersonHandleLabelExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPersonHandleLabelExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INPersonHandleLabel self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonHandleLabel GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INPersonHandleLabelExtensions -->
<div> <!-- start type INPersonHandleType -->
<h3>New Type Intents.INPersonHandleType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonHandleType {
	<span class='added added-field ' data-is-non-breaking="">EmailAddress = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PhoneNumber = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INPersonHandleType -->
<div> <!-- start type INPersonRelationship -->
<h3>New Type Intents.INPersonRelationship</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonRelationship {
	<span class='added added-field ' data-is-non-breaking="">Assistant = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Brother = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Child = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Father = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Friend = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Manager = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Mother = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Parent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Partner = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Sister = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Spouse = 8,</span>
}
</pre>
</div> <!-- end type INPersonRelationship -->
<div> <!-- start type INPersonRelationshipExtensions -->
<h3>New Type Intents.INPersonRelationshipExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPersonRelationshipExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INPersonRelationship self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonRelationship GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INPersonRelationshipExtensions -->
<div> <!-- start type INPersonResolutionResult -->
<h3>New Type Intents.INPersonResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPersonResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetConfirmationRequired (INPerson personToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetDisambiguation (INPerson[] peopleToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetSuccess (INPerson resolvedPerson);</span>
}
</pre>
</div> <!-- end type INPersonResolutionResult -->
<div> <!-- start type INPersonSuggestionType -->
<h3>New Type Intents.INPersonSuggestionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonSuggestionType {
	<span class='added added-field ' data-is-non-breaking="">InstantMessageAddress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SocialProfile = 1,</span>
}
</pre>
</div> <!-- end type INPersonSuggestionType -->
<div> <!-- start type INPlacemarkResolutionResult -->
<h3>New Type Intents.INPlacemarkResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPlacemarkResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPlacemarkResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPlacemarkResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetConfirmationRequired (CoreLocation.CLPlacemark placemarkToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetDisambiguation (CoreLocation.CLPlacemark[] placemarksToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetSuccess (CoreLocation.CLPlacemark resolvedPlacemark);</span>
}
</pre>
</div> <!-- end type INPlacemarkResolutionResult -->
<div> <!-- start type INSearchCallHistoryIntent -->
<h3>New Type Intents.INSearchCallHistoryIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchCallHistoryIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INCallRecordType callType, INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallCapabilityOptions CallCapabilities { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordType CallType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Recipient { get; }</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntent -->
<div> <!-- start type INSearchCallHistoryIntentHandling_Extensions -->
<h3>New Type Intents.INSearchCallHistoryIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchCallHistoryIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearchCallHistory (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INSearchCallHistoryIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCallType (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INCallRecordTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateCreated (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipient (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INPersonResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentHandling_Extensions -->
<div> <!-- start type INSearchCallHistoryIntentResponse -->
<h3>New Type Intents.INSearchCallHistoryIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchCallHistoryIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntentResponse (INSearchCallHistoryIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchCallHistoryIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentResponse -->
<div> <!-- start type INSearchCallHistoryIntentResponseCode -->
<h3>New Type Intents.INSearchCallHistoryIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchCallHistoryIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentResponseCode -->
<div> <!-- start type INSearchForMessagesIntent -->
<h3>New Type Intents.INSearchForMessagesIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForMessagesIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (INPerson[] recipients, INPerson[] senders, string[] searchTerms, INMessageAttributeOptions attributes, INDateComponentsRange dateTimeRange, string[] identifiers, string[] notificationIdentifiers, string[] groupNames);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessageAttributeOptions Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateTimeRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] GroupNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator GroupNamesOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Identifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator IdentifiersOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] NotificationIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator NotificationIdentifiersOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator RecipientsOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SearchTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SearchTermsOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Senders { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SendersOperator { get; }</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntent -->
<div> <!-- start type INSearchForMessagesIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForMessagesIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForMessagesIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearchForMessages (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INSearchForMessagesIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAttributes (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INMessageAttributeOptionsResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateTimeRange (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupNames (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INStringResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSenders (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentHandling_Extensions -->
<div> <!-- start type INSearchForMessagesIntentResponse -->
<h3>New Type Intents.INSearchForMessagesIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForMessagesIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntentResponse (INSearchForMessagesIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForMessagesIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessage[] Messages { get; set; }</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentResponse -->
<div> <!-- start type INSearchForMessagesIntentResponseCode -->
<h3>New Type Intents.INSearchForMessagesIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForMessagesIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentResponseCode -->
<div> <!-- start type INSendMessageIntent -->
<h3>New Type Intents.INSendMessageIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (INPerson[] recipients, string content, string groupName, string serviceName, INPerson sender);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Sender { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ServiceName { get; }</span>
}
</pre>
</div> <!-- end type INSendMessageIntent -->
<div> <!-- start type INSendMessageIntentHandling_Extensions -->
<h3>New Type Intents.INSendMessageIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSendMessageIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSendMessage (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSendMessageIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContent (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupName (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INSendMessageIntentHandling_Extensions -->
<div> <!-- start type INSendMessageIntentResponse -->
<h3>New Type Intents.INSendMessageIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntentResponse (INSendMessageIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSendMessageIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSendMessageIntentResponse -->
<div> <!-- start type INSendMessageIntentResponseCode -->
<h3>New Type Intents.INSendMessageIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendMessageIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSendMessageIntentResponseCode -->
<div> <!-- start type INSetMessageAttributeIntentResponseCode -->
<h3>New Type Intents.INSetMessageAttributeIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSetMessageAttributeIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageAttributeNotSet = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageNotFound = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSetMessageAttributeIntentResponseCode -->
<div> <!-- start type INSpeakableString -->
<h3>New Type Intents.INSpeakableString</h3>
<pre class='added' data-is-non-breaking="">
public class INSpeakableString : Foundation.NSObject, Foundation.INSObjectProtocol, IINSpeakable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableString (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableString (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (string spokenPhrase);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (string identifier, string spokenPhrase, string pronunciationHint);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
}
</pre>
</div> <!-- end type INSpeakableString -->
<div> <!-- start type INSpeakableStringResolutionResult -->
<h3>New Type Intents.INSpeakableStringResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSpeakableStringResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableStringResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableStringResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetConfirmationRequired (INSpeakableString stringToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetDisambiguation (INSpeakableString[] stringsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetSuccess (INSpeakableString resolvedString);</span>
}
</pre>
</div> <!-- end type INSpeakableStringResolutionResult -->
<div> <!-- start type INStartAudioCallIntent -->
<h3>New Type Intents.INStartAudioCallIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INStartAudioCallIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (INPerson[] contacts);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Contacts { get; }</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntent -->
<div> <!-- start type INStartAudioCallIntentHandling_Extensions -->
<h3>New Type Intents.INStartAudioCallIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INStartAudioCallIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmStartAudioCall (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INStartAudioCallIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContacts (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentHandling_Extensions -->
<div> <!-- start type INStartAudioCallIntentResponse -->
<h3>New Type Intents.INStartAudioCallIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INStartAudioCallIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntentResponse (INStartAudioCallIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INStartAudioCallIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentResponse -->
<div> <!-- start type INStartAudioCallIntentResponseCode -->
<h3>New Type Intents.INStartAudioCallIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INStartAudioCallIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCallingServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentResponseCode -->
<div> <!-- start type INStartVideoCallIntent -->
<h3>New Type Intents.INStartVideoCallIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INStartVideoCallIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartVideoCallIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartVideoCallIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartVideoCallIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartVideoCallIntent (INPerson[] contacts);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartVideoCallIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Contacts { get; }</span>
}
</pre>
</div> <!-- end type INStartVideoCallIntent -->
<div> <!-- start type INStartVideoCallIntentHandling_Extensions -->
<h3>New Type Intents.INStartVideoCallIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INStartVideoCallIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmStartVideoCall (IINStartVideoCallIntentHandling This, INStartVideoCallIntent intent, System.Action&lt;INStartVideoCallIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContacts (IINStartVideoCallIntentHandling This, INStartVideoCallIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INStartVideoCallIntentHandling_Extensions -->
<div> <!-- start type INStartVideoCallIntentResponse -->
<h3>New Type Intents.INStartVideoCallIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INStartVideoCallIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartVideoCallIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartVideoCallIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartVideoCallIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartVideoCallIntentResponse (INStartVideoCallIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INStartVideoCallIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INStartVideoCallIntentResponse -->
<div> <!-- start type INStartVideoCallIntentResponseCode -->
<h3>New Type Intents.INStartVideoCallIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INStartVideoCallIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCallingServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INStartVideoCallIntentResponseCode -->
<div> <!-- start type INStringResolutionResult -->
<h3>New Type Intents.INStringResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INStringResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INStringResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStringResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetConfirmationRequired (string stringToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetDisambiguation (string[] stringsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetSuccess (string resolvedString);</span>
}
</pre>
</div> <!-- end type INStringResolutionResult -->
<div> <!-- start type NSUserActivity_IntentsAdditions -->
<h3>New Type Intents.NSUserActivity_IntentsAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_IntentsAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INInteraction GetInteraction (Foundation.NSUserActivity This);</span>
}
</pre>
</div> <!-- end type NSUserActivity_IntentsAdditions -->
</div> <!-- end namespace Intents -->

<!-- start namespace MediaPlayer --> <div> 
<h2>New Namespace MediaPlayer</h2>

<div> <!-- start type MPChangeLanguageOptionCommandEvent -->
<h3>New Type MediaPlayer.MPChangeLanguageOptionCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeLanguageOptionCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeLanguageOptionCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeLanguageOptionCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPNowPlayingInfoLanguageOption LanguageOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeLanguageOptionSetting Setting { get; }</span>
}
</pre>
</div> <!-- end type MPChangeLanguageOptionCommandEvent -->
<div> <!-- start type MPChangeLanguageOptionSetting -->
<h3>New Type MediaPlayer.MPChangeLanguageOptionSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPChangeLanguageOptionSetting {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NowPlayingItemOnly = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Permanent = 2,</span>
}
</pre>
</div> <!-- end type MPChangeLanguageOptionSetting -->
<div> <!-- start type MPChangePlaybackPositionCommand -->
<h3>New Type MediaPlayer.MPChangePlaybackPositionCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangePlaybackPositionCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackPositionCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackPositionCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPChangePlaybackPositionCommand -->
<div> <!-- start type MPChangePlaybackPositionCommandEvent -->
<h3>New Type MediaPlayer.MPChangePlaybackPositionCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangePlaybackPositionCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackPositionCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackPositionCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double PositionTime { get; }</span>
}
</pre>
</div> <!-- end type MPChangePlaybackPositionCommandEvent -->
<div> <!-- start type MPChangePlaybackRateCommand -->
<h3>New Type MediaPlayer.MPChangePlaybackRateCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangePlaybackRateCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackRateCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackRateCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] SupportedPlaybackRates { get; set; }</span>
}
</pre>
</div> <!-- end type MPChangePlaybackRateCommand -->
<div> <!-- start type MPChangePlaybackRateCommandEvent -->
<h3>New Type MediaPlayer.MPChangePlaybackRateCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangePlaybackRateCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackRateCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangePlaybackRateCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PlaybackRate { get; }</span>
}
</pre>
</div> <!-- end type MPChangePlaybackRateCommandEvent -->
<div> <!-- start type MPChangeRepeatModeCommand -->
<h3>New Type MediaPlayer.MPChangeRepeatModeCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeRepeatModeCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRepeatType CurrentRepeatType { get; set; }</span>
}
</pre>
</div> <!-- end type MPChangeRepeatModeCommand -->
<div> <!-- start type MPChangeRepeatModeCommandEvent -->
<h3>New Type MediaPlayer.MPChangeRepeatModeCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeRepeatModeCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreservesRepeatMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRepeatType RepeatType { get; }</span>
}
</pre>
</div> <!-- end type MPChangeRepeatModeCommandEvent -->
<div> <!-- start type MPChangeShuffleModeCommand -->
<h3>New Type MediaPlayer.MPChangeShuffleModeCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeShuffleModeCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPShuffleType CurrentShuffleType { get; set; }</span>
}
</pre>
</div> <!-- end type MPChangeShuffleModeCommand -->
<div> <!-- start type MPChangeShuffleModeCommandEvent -->
<h3>New Type MediaPlayer.MPChangeShuffleModeCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeShuffleModeCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreservesShuffleMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPShuffleType ShuffleType { get; }</span>
}
</pre>
</div> <!-- end type MPChangeShuffleModeCommandEvent -->
<div> <!-- start type MPContentItem -->
<h3>New Type MediaPlayer.MPContentItem</h3>
<pre class='added' data-is-non-breaking="">
public class MPContentItem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPContentItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPContentItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPContentItem (string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMediaItemArtwork Artwork { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Container { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Playable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PlaybackProgress { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
}
</pre>
</div> <!-- end type MPContentItem -->
<div> <!-- start type MPFeedbackCommand -->
<h3>New Type MediaPlayer.MPFeedbackCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPFeedbackCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPFeedbackCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPFeedbackCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Active { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; set; }</span>
}
</pre>
</div> <!-- end type MPFeedbackCommand -->
<div> <!-- start type MPFeedbackCommandEvent -->
<h3>New Type MediaPlayer.MPFeedbackCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPFeedbackCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPFeedbackCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPFeedbackCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Negative { get; }</span>
}
</pre>
</div> <!-- end type MPFeedbackCommandEvent -->
<div> <!-- start type MPLanguageOptionCharacteristics -->
<h3>New Type MediaPlayer.MPLanguageOptionCharacteristics</h3>
<pre class='added' data-is-non-breaking="">
public static class MPLanguageOptionCharacteristics {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContainsOnlyForcedSubtitles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DescribesMusicAndSound { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DescribesVideo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DubbedTranslation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EasyToRead { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsAuxiliaryContent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsMainProgramContent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LanguageTranslation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TranscribesSpokenDialog { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VoiceOverTranslation { get; }</span>
}
</pre>
</div> <!-- end type MPLanguageOptionCharacteristics -->
<div> <!-- start type MPMediaItemArtwork -->
<h3>New Type MediaPlayer.MPMediaItemArtwork</h3>
<pre class='added' data-is-non-breaking="">
public class MPMediaItemArtwork : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItemArtwork (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItemArtwork (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemArtwork (CoreGraphics.CGSize boundsSize, System.Func&lt;CoreGraphics.CGSize,AppKit.NSImage&gt; requestHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AppKit.NSImage ImageWithSize (CoreGraphics.CGSize size);</span>
}
</pre>
</div> <!-- end type MPMediaItemArtwork -->
<div> <!-- start type MPNowPlayingInfoCenter -->
<h3>New Type MediaPlayer.MPNowPlayingInfoCenter</h3>
<pre class='added' data-is-non-breaking="">
public class MPNowPlayingInfoCenter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoCenter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoCenter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MPNowPlayingInfoCenter DefaultCenter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPNowPlayingPlaybackState PlaybackState { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyCollectionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyExternalContentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyExternalUserProfileIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyIsLiveStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyMediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPlaybackProgress { get; }</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoCenter -->
<div> <!-- start type MPNowPlayingInfoLanguageOption -->
<h3>New Type MediaPlayer.MPNowPlayingInfoLanguageOption</h3>
<pre class='added' data-is-non-breaking="">
public class MPNowPlayingInfoLanguageOption : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoLanguageOption (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoLanguageOption (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOption (MPNowPlayingInfoLanguageOptionType languageOptionType, string languageTag, Foundation.NSString[] languageOptionCharacteristics, string displayName, string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAutomaticAudibleLanguageOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAutomaticLegibleLanguageOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString[] LanguageOptionCharacteristics { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPNowPlayingInfoLanguageOptionType LanguageOptionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LanguageTag { get; }</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoLanguageOption -->
<div> <!-- start type MPNowPlayingInfoLanguageOptionGroup -->
<h3>New Type MediaPlayer.MPNowPlayingInfoLanguageOptionGroup</h3>
<pre class='added' data-is-non-breaking="">
public class MPNowPlayingInfoLanguageOptionGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoLanguageOptionGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPNowPlayingInfoLanguageOptionGroup (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOptionGroup (MPNowPlayingInfoLanguageOption[] languageOptions, MPNowPlayingInfoLanguageOption defaultLanguageOption, bool allowEmptySelection);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowEmptySelection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPNowPlayingInfoLanguageOption DefaultLanguageOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPNowPlayingInfoLanguageOption[] LanguageOptions { get; }</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoLanguageOptionGroup -->
<div> <!-- start type MPNowPlayingInfoLanguageOptionType -->
<h3>New Type MediaPlayer.MPNowPlayingInfoLanguageOptionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPNowPlayingInfoLanguageOptionType {
	<span class='added added-field ' data-is-non-breaking="">Audible = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Legible = 1,</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoLanguageOptionType -->
<div> <!-- start type MPNowPlayingInfoMediaType -->
<h3>New Type MediaPlayer.MPNowPlayingInfoMediaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPNowPlayingInfoMediaType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoMediaType -->
<div> <!-- start type MPNowPlayingPlaybackState -->
<h3>New Type MediaPlayer.MPNowPlayingPlaybackState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPNowPlayingPlaybackState {
	<span class='added added-field ' data-is-non-breaking="">Interrupted = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Paused = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Playing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type MPNowPlayingPlaybackState -->
<div> <!-- start type MPRatingCommand -->
<h3>New Type MediaPlayer.MPRatingCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPRatingCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRatingCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRatingCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumRating { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumRating { get; set; }</span>
}
</pre>
</div> <!-- end type MPRatingCommand -->
<div> <!-- start type MPRatingCommandEvent -->
<h3>New Type MediaPlayer.MPRatingCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPRatingCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRatingCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRatingCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Rating { get; }</span>
}
</pre>
</div> <!-- end type MPRatingCommandEvent -->
<div> <!-- start type MPRemoteCommand -->
<h3>New Type MediaPlayer.MPRemoteCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPRemoteCommand : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject AddTarget (System.Func&lt;MPRemoteCommandEvent,MediaPlayer.MPRemoteCommandHandlerStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddTarget (Foundation.NSObject target, ObjCRuntime.Selector action);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveTarget (Foundation.NSObject target);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveTarget (Foundation.NSObject target, ObjCRuntime.Selector action);</span>
}
</pre>
</div> <!-- end type MPRemoteCommand -->
<div> <!-- start type MPRemoteCommandCenter -->
<h3>New Type MediaPlayer.MPRemoteCommandCenter</h3>
<pre class='added' data-is-non-breaking="">
public class MPRemoteCommandCenter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommandCenter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommandCenter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPFeedbackCommand BookmarkCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangePlaybackPositionCommand ChangePlaybackPositionCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangePlaybackRateCommand ChangePlaybackRateCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeRepeatModeCommand ChangeRepeatModeCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeShuffleModeCommand ChangeShuffleModeCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand DisableLanguageOptionCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPFeedbackCommand DislikeCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand EnableLanguageOptionCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPFeedbackCommand LikeCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand NextTrackCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand PauseCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand PlayCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand PreviousTrackCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRatingCommand RatingCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand SeekBackwardCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand SeekForwardCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MPRemoteCommandCenter Shared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSkipIntervalCommand SkipBackwardCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSkipIntervalCommand SkipForwardCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand StopCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand TogglePlayPauseCommand { get; }</span>
}
</pre>
</div> <!-- end type MPRemoteCommandCenter -->
<div> <!-- start type MPRemoteCommandEvent -->
<h3>New Type MediaPlayer.MPRemoteCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPRemoteCommandEvent : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPRemoteCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRemoteCommand Command { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Timestamp { get; }</span>
}
</pre>
</div> <!-- end type MPRemoteCommandEvent -->
<div> <!-- start type MPRemoteCommandHandlerStatus -->
<h3>New Type MediaPlayer.MPRemoteCommandHandlerStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPRemoteCommandHandlerStatus {
	<span class='added added-field ' data-is-non-breaking="">CommandFailed = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">NoActionableNowPlayingItem = 110,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSuchContent = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type MPRemoteCommandHandlerStatus -->
<div> <!-- start type MPRepeatType -->
<h3>New Type MediaPlayer.MPRepeatType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPRepeatType {
	<span class='added added-field ' data-is-non-breaking="">All = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">One = 1,</span>
}
</pre>
</div> <!-- end type MPRepeatType -->
<div> <!-- start type MPSeekCommandEvent -->
<h3>New Type MediaPlayer.MPSeekCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPSeekCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSeekCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSeekCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSeekCommandEventType Type { get; }</span>
}
</pre>
</div> <!-- end type MPSeekCommandEvent -->
<div> <!-- start type MPSeekCommandEventType -->
<h3>New Type MediaPlayer.MPSeekCommandEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSeekCommandEventType {
	<span class='added added-field ' data-is-non-breaking="">BeginSeeking = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">EndSeeking = 1,</span>
}
</pre>
</div> <!-- end type MPSeekCommandEventType -->
<div> <!-- start type MPShuffleType -->
<h3>New Type MediaPlayer.MPShuffleType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPShuffleType {
	<span class='added added-field ' data-is-non-breaking="">Collections = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Items = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
}
</pre>
</div> <!-- end type MPShuffleType -->
<div> <!-- start type MPSkipIntervalCommand -->
<h3>New Type MediaPlayer.MPSkipIntervalCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPSkipIntervalCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSkipIntervalCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSkipIntervalCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double[] PreferredIntervals { get; set; }</span>
}
</pre>
</div> <!-- end type MPSkipIntervalCommand -->
<div> <!-- start type MPSkipIntervalCommandEvent -->
<h3>New Type MediaPlayer.MPSkipIntervalCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPSkipIntervalCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSkipIntervalCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSkipIntervalCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Interval { get; }</span>
}
</pre>
</div> <!-- end type MPSkipIntervalCommandEvent -->
</div> <!-- end namespace MediaPlayer -->

<!-- start namespace Photos --> <div> 
<h2>New Namespace Photos</h2>

<div> <!-- start type IPHLivePhotoFrame -->
<h3>New Type Photos.IPHLivePhotoFrame</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHLivePhotoFrame : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RenderScale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Time { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameType Type { get; }</span>
}
</pre>
</div> <!-- end type IPHLivePhotoFrame -->
<div> <!-- start type PHAdjustmentData -->
<h3>New Type Photos.PHAdjustmentData</h3>
<pre class='added' data-is-non-breaking="">
public class PHAdjustmentData : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAdjustmentData (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAdjustmentData (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData (string formatIdentifier, string formatVersion, Foundation.NSData data);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FormatIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FormatVersion { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHAdjustmentData -->
<div> <!-- start type PHAssetBurstSelectionType -->
<h3>New Type Photos.PHAssetBurstSelectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PHAssetBurstSelectionType {
	<span class='added added-field ' data-is-non-breaking="">AutoPick = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserPick = 2,</span>
}
</pre>
</div> <!-- end type PHAssetBurstSelectionType -->
<div> <!-- start type PHAssetCollectionSubtype -->
<h3>New Type Photos.PHAssetCollectionSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetCollectionSubtype {
	<span class='added added-field ' data-is-non-breaking="">AlbumCloudShared = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumImported = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumMyPhotoStream = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumRegular = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedAlbum = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedEvent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedFaces = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 9223372036854775807,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAllHidden = 205,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumBursts = 207,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumDepthEffect = 212,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumFavorites = 203,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumGeneric = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumPanoramas = 201,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumRecentlyAdded = 206,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumScreenshots = 211,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumSelfPortraits = 210,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumSlomoVideos = 208,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumTimelapses = 204,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumUserLibrary = 209,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumVideos = 202,</span>
}
</pre>
</div> <!-- end type PHAssetCollectionSubtype -->
<div> <!-- start type PHAssetCollectionType -->
<h3>New Type Photos.PHAssetCollectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetCollectionType {
	<span class='added added-field ' data-is-non-breaking="">Album = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbum = 2,</span>
}
</pre>
</div> <!-- end type PHAssetCollectionType -->
<div> <!-- start type PHAssetEditOperation -->
<h3>New Type Photos.PHAssetEditOperation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetEditOperation {
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Delete = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Properties = 3,</span>
}
</pre>
</div> <!-- end type PHAssetEditOperation -->
<div> <!-- start type PHAssetMediaSubtype -->
<h3>New Type Photos.PHAssetMediaSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PHAssetMediaSubtype {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoDepthEffect = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoHDR = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoLive = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoPanorama = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Screenshot = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoHighFrameRate = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoStreamed = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoTimelapse = 262144,</span>
}
</pre>
</div> <!-- end type PHAssetMediaSubtype -->
<div> <!-- start type PHAssetMediaType -->
<h3>New Type Photos.PHAssetMediaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetMediaType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type PHAssetMediaType -->
<div> <!-- start type PHAssetResourceType -->
<h3>New Type Photos.PHAssetResourceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetResourceType {
	<span class='added added-field ' data-is-non-breaking="">AdjustmentBasePhoto = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AdjustmentData = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">AlternatePhoto = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Audio = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FullSizePhoto = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FullSizeVideo = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">PairedVideo = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Photo = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type PHAssetResourceType -->
<div> <!-- start type PHAssetSourceType -->
<h3>New Type Photos.PHAssetSourceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetSourceType {
	<span class='added added-field ' data-is-non-breaking="">CloudShared = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserLibrary = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">iTunesSynced = 4,</span>
}
</pre>
</div> <!-- end type PHAssetSourceType -->
<div> <!-- start type PHCollectionEditOperation -->
<h3>New Type Photos.PHCollectionEditOperation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionEditOperation {
	<span class='added added-field ' data-is-non-breaking="">AddContent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">CreateContent = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Delete = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DeleteContent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RearrangeContent = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">RemoveContent = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rename = 7,</span>
}
</pre>
</div> <!-- end type PHCollectionEditOperation -->
<div> <!-- start type PHCollectionListSubtype -->
<h3>New Type Photos.PHCollectionListSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionListSubtype {
	<span class='added added-field ' data-is-non-breaking="">Any = 9223372036854775807,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentListCluster = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentListYear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RegularFolder = 100,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Incorrect value (exists in PHAssetCollectionSubtype)")]
	SmartAlbumScreenshots = 211,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Incorrect value (exists in PHAssetCollectionSubtype)")]
	SmartAlbumSelfPortraits = 210,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolderEvents = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolderFaces = 201,</span>
}
</pre>
</div> <!-- end type PHCollectionListSubtype -->
<div> <!-- start type PHCollectionListType -->
<h3>New Type Photos.PHCollectionListType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionListType {
	<span class='added added-field ' data-is-non-breaking="">Folder = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentList = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolder = 3,</span>
}
</pre>
</div> <!-- end type PHCollectionListType -->
<div> <!-- start type PHContentEditingInput -->
<h3>New Type Photos.PHContentEditingInput</h3>
<pre class='added' data-is-non-breaking="">
public class PHContentEditingInput : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingInput ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInput (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInput (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAdjustmentData AdjustmentData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVAsset AudiovisualAsset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVAsset AvAsset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImageOrientation FullSizeImageOrientation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl FullSizeImageUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhoto LivePhoto { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string UniformTypeIdentifier { get; }</span>
}
</pre>
</div> <!-- end type PHContentEditingInput -->
<div> <!-- start type PHContentEditingOutput -->
<h3>New Type Photos.PHContentEditingOutput</h3>
<pre class='added' data-is-non-breaking="">
public class PHContentEditingOutput : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingOutput (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput (PHContentEditingInput contentEditingInput);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingOutput (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAdjustmentData AdjustmentData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl RenderedContentUrl { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHContentEditingOutput -->
<div> <!-- start type PHImageContentMode -->
<h3>New Type Photos.PHImageContentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageContentMode {
	<span class='added added-field ' data-is-non-breaking="">AspectFill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">AspectFit = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
}
</pre>
</div> <!-- end type PHImageContentMode -->
<div> <!-- start type PHLivePhoto -->
<h3>New Type Photos.PHLivePhoto</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhoto : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhoto (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhoto (IntPtr handle);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int RequestIdInvalid;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhoto -->
<div> <!-- start type PHLivePhotoEditingContext -->
<h3>New Type Photos.PHLivePhotoEditingContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingContext : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoEditingContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingContext (PHContentEditingInput livePhotoInput);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoEditingContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float AudioVolume { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameProcessingBlock FrameProcessor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImage FullSizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ImageIO.CGImagePropertyOrientation Orientation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime PhotoTime { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Cancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveLivePhoto (PHContentEditingOutput output, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type PHLivePhotoFrameProcessingBlock -->
<h3>New Type Photos.PHLivePhotoFrameProcessingBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHLivePhotoFrameProcessingBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoFrameProcessingBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IPHLivePhotoFrame frame, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage Invoke (IPHLivePhotoFrame frame, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameProcessingBlock -->
<div> <!-- start type PHLivePhotoFrameType -->
<h3>New Type Photos.PHLivePhotoFrameType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHLivePhotoFrameType {
	<span class='added added-field ' data-is-non-breaking="">Photo = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 1,</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameType -->
</div> <!-- end namespace Photos -->

<!-- start namespace SafariServices --> <div> 
<h2>New Namespace SafariServices</h2>

<div> <!-- start type ISFSafariExtensionHandling -->
<h3>New Type SafariServices.ISFSafariExtensionHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface ISFSafariExtensionHandling : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISFSafariExtensionHandling -->
<div> <!-- start type SFContentBlockerManager -->
<h3>New Type SafariServices.SFContentBlockerManager</h3>
<pre class='added' data-is-non-breaking="">
public class SFContentBlockerManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFContentBlockerManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFContentBlockerManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFContentBlockerManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void GetStateOfContentBlocker (string identifier, System.Action&lt;SFContentBlockerState,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SFContentBlockerState&gt; GetStateOfContentBlockerAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ReloadContentBlocker (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task ReloadContentBlockerAsync (string identifier);</span>
}
</pre>
</div> <!-- end type SFContentBlockerManager -->
<div> <!-- start type SFContentBlockerState -->
<h3>New Type SafariServices.SFContentBlockerState</h3>
<pre class='added' data-is-non-breaking="">
public class SFContentBlockerState : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFContentBlockerState ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFContentBlockerState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFContentBlockerState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; }</span>
}
</pre>
</div> <!-- end type SFContentBlockerState -->
<div> <!-- start type SFErrorCode -->
<h3>New Type SafariServices.SFErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SFErrorCode {
	<span class='added added-field ' data-is-non-breaking="">LoadingInterrupted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAttachmentFound = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NoExtensionFound = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
}
</pre>
</div> <!-- end type SFErrorCode -->
<div> <!-- start type SFErrorCodeExtensions -->
<h3>New Type SafariServices.SFErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SFErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (SFErrorCode self);</span>
}
</pre>
</div> <!-- end type SFErrorCodeExtensions -->
<div> <!-- start type SFSafariApplication -->
<h3>New Type SafariServices.SFSafariApplication</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariApplication : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariApplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariApplication (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void GetActiveWindow (System.Action&lt;SFSafariWindow&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SFSafariWindow&gt; GetActiveWindowAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void OpenWindow (Foundation.NSUrl url, System.Action&lt;SFSafariWindow&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SFSafariWindow&gt; OpenWindowAsync (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetToolbarItemsNeedUpdate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ShowPreferencesForExtension (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type SFSafariApplication -->
<div> <!-- start type SFSafariExtensionHandler -->
<h3>New Type SafariServices.SFSafariExtensionHandler</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariExtensionHandler : Foundation.NSObject, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISFSafariExtensionHandling, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariExtensionHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariExtensionHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariExtensionHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SFSafariExtensionViewController PopoverViewController { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginRequestWithExtensionContext (Foundation.NSExtensionContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ContextMenuItemSelected (string command, SFSafariPage page, Foundation.NSDictionary userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MessageReceived (string messageName, SFSafariPage page, Foundation.NSDictionary userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PopoverDidClose (SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PopoverWillShow (SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ToolbarItemClicked (SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ValidateToolbarItem (SFSafariWindow window, System.Action&lt;System.Boolean,Foundation.NSString&gt; validationHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFValidationResult&gt; ValidateToolbarItemAsync (SFSafariWindow window);</span>
}
</pre>
</div> <!-- end type SFSafariExtensionHandler -->
<div> <!-- start type SFSafariExtensionHandling_Extensions -->
<h3>New Type SafariServices.SFSafariExtensionHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SFSafariExtensionHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ContextMenuItemSelected (ISFSafariExtensionHandling This, string command, SFSafariPage page, Foundation.NSDictionary userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SFSafariExtensionViewController GetPopoverViewController (ISFSafariExtensionHandling This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MessageReceived (ISFSafariExtensionHandling This, string messageName, SFSafariPage page, Foundation.NSDictionary userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PopoverDidClose (ISFSafariExtensionHandling This, SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PopoverWillShow (ISFSafariExtensionHandling This, SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ToolbarItemClicked (ISFSafariExtensionHandling This, SFSafariWindow window);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ValidateToolbarItem (ISFSafariExtensionHandling This, SFSafariWindow window, System.Action&lt;System.Boolean,Foundation.NSString&gt; validationHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;SFValidationResult&gt; ValidateToolbarItemAsync (ISFSafariExtensionHandling This, SFSafariWindow window);</span>
}
</pre>
</div> <!-- end type SFSafariExtensionHandling_Extensions -->
<div> <!-- start type SFSafariExtensionViewController -->
<h3>New Type SafariServices.SFSafariExtensionViewController</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariExtensionViewController : AppKit.NSViewController, AppKit.INSSeguePerforming, AppKit.INSTouchBarProvider, AppKit.INSUserInterfaceItemIdentification, Foundation.INSCoding, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariExtensionViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariExtensionViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariExtensionViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariExtensionViewController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type SFSafariExtensionViewController -->
<div> <!-- start type SFSafariPage -->
<h3>New Type SafariServices.SFSafariPage</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariPage : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariPage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariPage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DispatchMessageToScript (string messageName, Foundation.NSDictionary userInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetPageProperties (System.Action&lt;SFSafariPageProperties&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariPageProperties&gt; GetPagePropertiesAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Reload ();</span>
}
</pre>
</div> <!-- end type SFSafariPage -->
<div> <!-- start type SFSafariPageProperties -->
<h3>New Type SafariServices.SFSafariPageProperties</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariPageProperties : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFSafariPageProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariPageProperties (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariPageProperties (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Active { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesPrivateBrowsing { get; }</span>
}
</pre>
</div> <!-- end type SFSafariPageProperties -->
<div> <!-- start type SFSafariTab -->
<h3>New Type SafariServices.SFSafariTab</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariTab : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariTab (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariTab (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Activate (System.Action completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ActivateAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetActivePage (System.Action&lt;SFSafariPage&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariPage&gt; GetActivePageAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetPages (System.Action&lt;SFSafariPage[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariPage[]&gt; GetPagesAsync ();</span>
}
</pre>
</div> <!-- end type SFSafariTab -->
<div> <!-- start type SFSafariToolbarItem -->
<h3>New Type SafariServices.SFSafariToolbarItem</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariToolbarItem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariToolbarItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariToolbarItem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetEnabled (bool enabled, string badgeText);</span>
}
</pre>
</div> <!-- end type SFSafariToolbarItem -->
<div> <!-- start type SFSafariWindow -->
<h3>New Type SafariServices.SFSafariWindow</h3>
<pre class='added' data-is-non-breaking="">
public class SFSafariWindow : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariWindow (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SFSafariWindow (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetActiveTab (System.Action&lt;SFSafariTab&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariTab&gt; GetActiveTabAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetToolbarItem (System.Action&lt;SFSafariToolbarItem&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariToolbarItem&gt; GetToolbarItemAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenTab (Foundation.NSUrl url, bool activateTab, System.Action&lt;SFSafariTab&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SFSafariTab&gt; OpenTabAsync (Foundation.NSUrl url, bool activateTab);</span>
}
</pre>
</div> <!-- end type SFSafariWindow -->
<div> <!-- start type SFValidationResult -->
<h3>New Type SafariServices.SFValidationResult</h3>
<pre class='added' data-is-non-breaking="">
public class SFValidationResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SFValidationResult (bool arg1, Foundation.NSString arg2);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool Arg1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString Arg2 { get; set; }</span>
}
</pre>
</div> <!-- end type SFValidationResult -->
</div> <!-- end namespace SafariServices -->

</div>
