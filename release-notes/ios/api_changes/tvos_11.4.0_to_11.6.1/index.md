---
id: 071B2B49-32DC-40F5-A9C4-970ADE0D0609
title: "tvOS 11.4.0 to 11.6.1"
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
<!-- start type AVAsset --> <div>
<h3>Type Changed: AVFoundation.AVAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVDisplayCriteria PreferredDisplayCriteria { get; }</span>
</pre>
</div>

</div> <!-- end type AVAsset -->
<!-- start type AVAssetResourceLoadingContentInformationRequest --> <div>
<h3>Type Changed: AVFoundation.AVAssetResourceLoadingContentInformationRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AllowedContentTypes { get; }</span>
</pre>
</div>

</div> <!-- end type AVAssetResourceLoadingContentInformationRequest -->
<!-- start type AVContentKeyRequest --> <div>
<h3>Type Changed: AVFoundation.AVContentKeyRequest</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("This API is not available on this platform.")]
	public virtual void RespondByRequestingPersistableContentKeyRequest ();</span>
</div></pre>

</div> <!-- end type AVContentKeyRequest -->
<!-- start type AVError --> <div>
<h3>Type Changed: AVFoundation.AVError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ContentIsUnavailable = -11863,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentNotUpdated = -11866,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatUnsupported = -11864,</span>
	<span class='added added-field ' data-is-non-breaking="">MalformedDepth = -11865,</span>
	<span class='added added-field ' data-is-non-breaking="">NoCompatibleAlternatesForExternalDisplay = -11868,</span>
	<span class='added added-field ' data-is-non-breaking="">NoLongerPlayable = -11867,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSourceTrack = -11869,</span>
</pre>
</div>

</div> <!-- end type AVError -->
<!-- start type AVPlayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static AVPlayerHdrMode AvailableHdrModes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AvailableHdrModesDidChangeNotification { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayer -->
<!-- start type AVSampleBufferAudioRenderer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferAudioRenderer</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("This API is not available on this platform.")]
	public virtual string AudioOutputDeviceUniqueId { get; set; }</span>
</div></pre>

</div> <!-- end type AVSampleBufferAudioRenderer -->
<div> <!-- start type AVDisplayCriteria -->
<h3>New Type AVFoundation.AVDisplayCriteria</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVDisplayCriteria : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDisplayCriteria ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDisplayCriteria (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDisplayCriteria (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type AVDisplayCriteria -->
<div> <!-- start type AVPlayerHdrMode -->
<h3>New Type AVFoundation.AVPlayerHdrMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum AVPlayerHdrMode {
	<span class='added added-field ' data-is-non-breaking="">DolbyVision = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Hdr10 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Hlg = 1,</span>
}
</pre>
</div> <!-- end type AVPlayerHdrMode -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AppliesPreferredDisplayCriteriaAutomatically { get; set; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewController -->
<div> <!-- start type AVDisplayManager -->
<h3>New Type AVKit.AVDisplayManager</h3>
<pre class='added' data-is-non-breaking="">
public class AVDisplayManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDisplayManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVDisplayManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool DisplayModeSwitchInProgress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVDisplayCriteria PreferredDisplayCriteria { get; set; }</span>
}
</pre>
</div> <!-- end type AVDisplayManager -->
<div> <!-- start type UIWindow_AVAdditions -->
<h3>New Type AVKit.UIWindow_AVAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIWindow_AVAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVDisplayManager GetAVDisplayManager (UIKit.UIWindow This);</span>
}
</pre>
</div> <!-- end type UIWindow_AVAdditions -->

</div> <!-- end namespace AVKit -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumDrawableCount { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBCentralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManager</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionStartDelayKey { get; }</span>
</pre>
</div>

</div> <!-- end type CBCentralManager -->

</div> <!-- end namespace CoreBluetooth -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIAreaMaximum --> <div>
<h3>Type Changed: CoreImage.CIAreaMaximum</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMaximum (string name);</span>
</pre>
</div>

</div> <!-- end type CIAreaMaximum -->
<!-- start type CIFilterInputKey --> <div>
<h3>Type Changed: CoreImage.CIFilterInputKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DepthImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisparityImage { get; }</span>
</pre>
</div>

</div> <!-- end type CIFilterInputKey -->
<!-- start type CIImageInitializationOptions --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? ApplyOrientationProperty { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDepth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AuxiliaryDisparity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NearestSampling { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIImageInitializationOptions -->
<!-- start type CIImageInitializationOptionsWithMetadata --> <div>
<h3>Type Changed: CoreImage.CIImageInitializationOptionsWithMetadata</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
</pre>

</div> <!-- end type CIImageInitializationOptionsWithMetadata -->
<!-- start type CIMotionBlur --> <div>
<h3>Type Changed: CoreImage.CIMotionBlur</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>CoreImage.CIFilter</span> <span class='added '>CoreImage.CILinearBlur</span>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public float Radius { get; set; }</span>
</pre>

</div> <!-- end type CIMotionBlur -->
<!-- start type CIVector --> <div>
<h3>Type Changed: CoreImage.CIVector</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIVector (nfloat[] values, nint count);</span>
</pre>
</div>

</div> <!-- end type CIVector -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIAreaMaximum, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Extent { get; set; }</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSAttributedString Text { get; set; }</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIBarcodeDescriptor BarcodeDescriptor { get; set; }</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float AspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float B { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float C { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Scale { get; set; }</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithBlueMask -->
<div> <!-- start type CIBlendWithRedMask -->
<h3>New Type CoreImage.CIBlendWithRedMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithRedMask : CoreImage.CIBlendWithMask, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithRedMask -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : CoreImage.CILinearBlur, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float RingAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float RingSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Softness { get; set; }</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube0Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Cube1Data { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float CubeDimension { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage MaskImage { get; set; }</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CurvesData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector CurvesDomain { get; set; }</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Aperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVFoundation.AVCameraCalibrationData CalibrationData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector ChinPositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage DisparityImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector FocusRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector LeftEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float LumaNoiseScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector NosePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector RightEyePositions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthDisparityConverter -->
<h3>New Type CoreImage.CIDepthDisparityConverter</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIDepthDisparityConverter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthDisparityConverter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthDisparityConverter (string name);</span>
}
</pre>
</div> <!-- end type CIDepthDisparityConverter -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : CoreImage.CIDepthDisparityConverter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float LumaSigma { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIImage SmallImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float SpatialSigma { get; set; }</span>
}
</pre>
</div> <!-- end type CIEdgePreserveUpsampleFilter -->
<div> <!-- start type CIImageGenerator -->
<h3>New Type CoreImage.CIImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageGenerator (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float ScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type CIImageGenerator -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIImage Image2 { get; set; }</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CILinearBlur -->
<h3>New Type CoreImage.CILinearBlur</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CILinearBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILinearBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILinearBlur (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CILinearBlur -->
<div> <!-- start type CIMorphology -->
<h3>New Type CoreImage.CIMorphology</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIMorphology : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphology (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphology (string name);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
}
</pre>
</div> <!-- end type CIMorphology -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : CoreImage.CIMorphology, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : CoreImage.CIImageGenerator, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FontName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float FontSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Text { get; set; }</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreML --> <div> 
<h2>Namespace CoreML</h2>
<!-- start type MLModelError --> <div>
<h3>Type Changed: CoreML.MLModelError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CustomLayer = 4,</span>
</pre>
</div>

</div> <!-- end type MLModelError -->
<div> <!-- start type IMLCustomLayer -->
<h3>New Type CoreML.IMLCustomLayer</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLCustomLayer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EvaluateOnCpu (MLMultiArray[] inputs, MLMultiArray[] outputs, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSArray[] GetOutputShapes (Foundation.NSArray[] inputShapes, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetWeightData (Foundation.NSData[] weights, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IMLCustomLayer -->
<div> <!-- start type MLCustomLayer_Extensions -->
<h3>New Type CoreML.MLCustomLayer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLCustomLayer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Encode (IMLCustomLayer This, Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture[] inputs, Metal.IMTLTexture[] outputs, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLCustomLayer_Extensions -->

</div> <!-- end namespace CoreML -->
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessoryCategory --> <div>
<h3>Type Changed: HomeKit.HMAccessoryCategory</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakCategoryType { get; }</span>
</pre>
</div>

</div> <!-- end type HMAccessoryCategory -->
<!-- start type HMAccessoryCategoryType --> <div>
<h3>Type Changed: HomeKit.HMAccessoryCategoryType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Faucet = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowerHead = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Sprinkler = 23,</span>
</pre>
</div>

</div> <!-- end type HMAccessoryCategoryType -->
<!-- start type HMCharacteristic --> <div>
<h3>Type Changed: HomeKit.HMCharacteristic</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakCharacteristicType { get; }</span>
</pre>
</div>

</div> <!-- end type HMCharacteristic -->
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InUse = 117,</span>
	<span class='added added-field ' data-is-non-breaking="">IsConfigured = 121,</span>
	<span class='added added-field ' data-is-non-breaking="">ProgramMode = 116,</span>
	<span class='added added-field ' data-is-non-breaking="">RemainingDuration = 119,</span>
	<span class='added added-field ' data-is-non-breaking="">SetDuration = 118,</span>
	<span class='added added-field ' data-is-non-breaking="">ValveType = 120,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMError --> <div>
<h3>Type Changed: HomeKit.HMError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnexpectedError = -1,</span>
</pre>
</div>

</div> <!-- end type HMError -->
<!-- start type HMHome --> <div>
<h3>Type Changed: HomeKit.HMHome</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual HMService[] GetServices (Foundation.NSString[] serviceTypes);</span>
</pre>
</div>

</div> <!-- end type HMHome -->
<!-- start type HMHomeAccessControl --> <div>
<h3>Type Changed: HomeKit.HMHomeAccessControl</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>HomeKit.HMAccessControl</span>

</div> <!-- end type HMHomeAccessControl -->
<!-- start type HMMutableSignificantTimeEvent --> <div>
<h3>Type Changed: HomeKit.HMMutableSignificantTimeEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSString WeakSignificantEvent { get; set; }</span>
</pre>
</div>

</div> <!-- end type HMMutableSignificantTimeEvent -->
<!-- start type HMService --> <div>
<h3>Type Changed: HomeKit.HMService</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakServiceType { get; }</span>
</pre>
</div>

</div> <!-- end type HMService -->
<!-- start type HMServiceType --> <div>
<h3>Type Changed: HomeKit.HMServiceType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Faucet = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">IrrigationSystem = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">Valve = 41,</span>
</pre>
</div>

</div> <!-- end type HMServiceType -->
<!-- start type HMSignificantTimeEvent --> <div>
<h3>Type Changed: HomeKit.HMSignificantTimeEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString WeakSignificantEvent { get; set; }</span>
</pre>
</div>

</div> <!-- end type HMSignificantTimeEvent -->
<div> <!-- start type HMAccessControl -->
<h3>New Type HomeKit.HMAccessControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessControl : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMAccessControl -->
<div> <!-- start type HMCharacteristicValueConfigurationState -->
<h3>New Type HomeKit.HMCharacteristicValueConfigurationState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueConfigurationState {
	<span class='added added-field ' data-is-non-breaking="">Configured = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConfigured = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueConfigurationState -->
<div> <!-- start type HMCharacteristicValueProgramMode -->
<h3>New Type HomeKit.HMCharacteristicValueProgramMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueProgramMode {
	<span class='added added-field ' data-is-non-breaking="">NotScheduled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScheduleOverriddenToManual = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Scheduled = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueProgramMode -->
<div> <!-- start type HMCharacteristicValueUsageState -->
<h3>New Type HomeKit.HMCharacteristicValueUsageState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueUsageState {
	<span class='added added-field ' data-is-non-breaking="">InUse = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotInUse = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueUsageState -->
<div> <!-- start type HMCharacteristicValueValveType -->
<h3>New Type HomeKit.HMCharacteristicValueValveType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueValveType {
	<span class='added added-field ' data-is-non-breaking="">GenericValve = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Irrigation = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowerHead = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WaterFaucet = 3,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueValveType -->

</div> <!-- end namespace HomeKit -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<!-- start type MPSBinaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
</pre>
</div>

</div> <!-- end type MPSBinaryImageKernel -->
<!-- start type MPSCnnConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolution</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelHeight { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelWidth { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint StrideInPixelsX { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint StrideInPixelsY { get; }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage, MPSCnnConvolutionState state);</span>
</pre>
</div>

</div> <!-- end type MPSCnnConvolution -->
<!-- start type MPSCnnConvolutionDescriptor --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SupportsSecureCoding { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor CreateCnnConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBatchNormalizationParameters (float[] mean, float[] variance, float[] gamma, float[] beta, float epsilon);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData A);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB);</span>
</pre>
</div>

</div> <!-- end type MPSCnnConvolutionDescriptor -->
<!-- start type MPSCnnCrossChannelNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSCnnCrossChannelNormalization -->
<!-- start type MPSCnnFullyConnected --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
</pre>
</div>

</div> <!-- end type MPSCnnFullyConnected -->
<!-- start type MPSCnnKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage);</span>
</pre>
</div>

</div> <!-- end type MPSCnnKernel -->
<!-- start type MPSCnnLocalContrastNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelHeight { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelWidth { get; }
</div></pre>

</div> <!-- end type MPSCnnLocalContrastNormalization -->
<!-- start type MPSCnnNeuron --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuron</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuron -->
<!-- start type MPSCnnPooling --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPooling</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelHeight { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelWidth { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint StrideInPixelsX { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint StrideInPixelsY { get; }
</div></pre>

</div> <!-- end type MPSCnnPooling -->
<!-- start type MPSCnnPoolingAverage --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ZeroPadSizeY { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingAverage -->
<!-- start type MPSCnnPoolingMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingMax -->
<!-- start type MPSCnnSpatialNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelHeight { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>virtual</span> <span class='added '>override</span> uint KernelWidth { get; }
</div></pre>

</div> <!-- end type MPSCnnSpatialNormalization -->
<!-- start type MPSDataType --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSDataType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Float16 = 268435472,</span>
	<span class='added added-field ' data-is-non-breaking="">NormalizedBit = 1073741824,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm1 = 1073741825,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1073741832,</span>
</pre>
</div>

</div> <!-- end type MPSDataType -->
<!-- start type MPSImage --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImage</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint imageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteBytes (IntPtr dataBytes, MPSDataLayout dataLayout, uint bytesPerRow, Metal.MTLRegion region, MPSImageReadWriteParams featureChannelInfo, uint imageIndex);</span>
</pre>
</div>

</div> <!-- end type MPSImage -->
<!-- start type MPSImageAreaMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMax -->
<!-- start type MPSImageBox --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageBox</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageBox -->
<!-- start type MPSImageConversion --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConversion</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageConversion -->
<!-- start type MPSImageConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageConvolution -->
<!-- start type MPSImageDilate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageDilate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageDilate -->
<!-- start type MPSImageErode --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageErode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageErode -->
<!-- start type MPSImageGaussianBlur --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianBlur -->
<!-- start type MPSImageGaussianPyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianPyramid -->
<!-- start type MPSImageHistogram --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogram</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector4 MinPixelThresholdValue { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Please use 'GetHistogramSize' instead.")]
	public virtual uint HistogramSizeForSourceFormat (Metal.MTLPixelFormat sourceFormat);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetHistogramSize (Metal.MTLPixelFormat sourceFormat);</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogram -->
<!-- start type MPSImageHistogramEqualization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramEqualization -->
<!-- start type MPSImageHistogramSpecification --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramSpecification -->
<!-- start type MPSImageIntegral --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegral</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegral -->
<!-- start type MPSImageIntegralOfSquares --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegralOfSquares -->
<!-- start type MPSImageLanczosScale --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLanczosScale</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform? ScaleTransform { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPSImageLanczosScale -->
<!-- start type MPSImageLaplacian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLaplacian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageLaplacian -->
<!-- start type MPSImageMedian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageMedian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageMedian -->
<!-- start type MPSImagePyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImagePyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImagePyramid -->
<!-- start type MPSImageSobel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageSobel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageSobel -->
<!-- start type MPSImageThresholdBinary --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinary -->
<!-- start type MPSImageThresholdBinaryInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinaryInverse -->
<!-- start type MPSImageThresholdToZero --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZero -->
<!-- start type MPSImageThresholdToZeroInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZeroInverse -->
<!-- start type MPSImageThresholdTruncate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdTruncate -->
<!-- start type MPSImageTranspose --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTranspose</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSImageTranspose -->
<!-- start type MPSKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>

</div> <!-- end type MPSKernel -->
<!-- start type MPSKernelOptions --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSKernelOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Verbose = 16,</span>
</pre>
</div>

</div> <!-- end type MPSKernelOptions -->
<!-- start type MPSMatrix --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrix</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
</pre>
</div>

</div> <!-- end type MPSMatrix -->
<!-- start type MPSMatrixDescriptor --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrixDescriptor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Matrices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MatrixBytes { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Please use 'GetRowBytesFromColumns' instead.")]
	public static uint GetRowBytes (uint columns, MPSDataType dataType);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor GetMatrixDescriptor (uint rows, uint columns, uint matrices, uint rowBytes, uint matrixBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesForColumns (uint columns, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytesFromColumns (uint columns, MPSDataType dataType);</span>
</pre>
</div>

</div> <!-- end type MPSMatrixDescriptor -->
<!-- start type MPSMatrixMultiplication --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, uint resultRows, uint resultColumns, uint interiorColumns);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPSMatrixMultiplication -->
<!-- start type MPSUnaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
</pre>
</div>

</div> <!-- end type MPSUnaryImageKernel -->
<div> <!-- start type IMPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.IMPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSCnnConvolutionDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type IMPSCnnConvolutionDataSource -->
<div> <!-- start type IMPSDeviceProvider -->
<h3>New Type MetalPerformanceShaders.IMPSDeviceProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSDeviceProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLDevice GetMTLDevice ();</span>
}
</pre>
</div> <!-- end type IMPSDeviceProvider -->
<div> <!-- start type IMPSHandle -->
<h3>New Type MetalPerformanceShaders.IMPSHandle</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSHandle : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
}
</pre>
</div> <!-- end type IMPSHandle -->
<div> <!-- start type IMPSImageAllocator -->
<h3>New Type MetalPerformanceShaders.IMPSImageAllocator</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageAllocator : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetImage (Metal.IMTLCommandBuffer cmdBuf, MPSImageDescriptor descriptor, MPSKernel kernel);</span>
}
</pre>
</div> <!-- end type IMPSImageAllocator -->
<div> <!-- start type IMPSImageSizeEncodingState -->
<h3>New Type MetalPerformanceShaders.IMPSImageSizeEncodingState</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageSizeEncodingState : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type IMPSImageSizeEncodingState -->
<div> <!-- start type IMPSImageTransformProvider -->
<h3>New Type MetalPerformanceShaders.IMPSImageTransformProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSImageTransformProvider : Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSScaleTransform GetTransform (MPSImage image, IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type IMPSImageTransformProvider -->
<div> <!-- start type IMPSNNPadding -->
<h3>New Type MetalPerformanceShaders.IMPSNNPadding</h3>
<pre class='added' data-is-non-breaking="">
public interface IMPSNNPadding : Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
}
</pre>
</div> <!-- end type IMPSNNPadding -->
<div> <!-- start type MPSCnnBinaryConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolution (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolution -->
<div> <!-- start type MPSCnnBinaryConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseBetaScaling = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionFlags -->
<div> <!-- start type MPSCnnBinaryConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryConvolutionNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionNode -->
<div> <!-- start type MPSCnnBinaryConvolutionType -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryConvolutionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnBinaryConvolutionType {
	<span class='added added-field ' data-is-non-breaking="">And = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">BinaryWeights = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Xnor = 1,</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryConvolutionType -->
<div> <!-- start type MPSCnnBinaryFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnected : MetalPerformanceShaders.MPSCnnBinaryConvolution, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnected (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource convolutionData, float[] outputBiasTerms, float[] outputScaleTerms, float[] inputBiasTerms, float[] inputScaleTerms, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnected -->
<div> <!-- start type MPSCnnBinaryFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryFullyConnectedNode : MetalPerformanceShaders.MPSCnnBinaryConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnBinaryFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights, float scaleValue, MPSCnnBinaryConvolutionType type, MPSCnnBinaryConvolutionFlags flags);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryFullyConnectedNode -->
<div> <!-- start type MPSCnnBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBackwards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding Padding { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode PrimaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset PrimaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PrimaryStrideInPixelsY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode SecondaryEdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SecondaryOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SecondaryStrideInPixelsY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage primaryImage, MPSImage secondaryImage, MPSImage destinationImage);</span>
}
</pre>
</div> <!-- end type MPSCnnBinaryKernel -->
<div> <!-- start type MPSCnnConvolutionDataSource -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnConvolutionDataSource : Foundation.NSObject, Foundation.INSObjectProtocol, IMPSCnnConvolutionDataSource, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDataSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BiasTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionDescriptor Descriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Load { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Weights { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetLookupTableForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRangesForUInt8Kernel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Purge ();</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource -->
<div> <!-- start type MPSCnnConvolutionDataSource_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDataSource_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSCnnConvolutionDataSource_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetLookupTableForUInt8Kernel (IMPSCnnConvolutionDataSource This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr GetRangesForUInt8Kernel (IMPSCnnConvolutionDataSource This);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDataSource_Extensions -->
<div> <!-- start type MPSCnnConvolutionNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnConvolutionStateNode ConvolutionState { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionNode -->
<div> <!-- start type MPSCnnConvolutionState -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, IMPSImageSizeEncodingState, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset SourceOffset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionState -->
<div> <!-- start type MPSCnnConvolutionStateNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionStateNode : MetalPerformanceShaders.MPSNNStateNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionStateNode -->
<div> <!-- start type MPSCnnConvolutionTranspose -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTranspose</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTranspose : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTranspose (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTranspose (Metal.IMTLDevice device, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint KernelOffsetY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSCnnConvolutionState convolutionState);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTranspose -->
<div> <!-- start type MPSCnnConvolutionTransposeNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionTransposeNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionTransposeNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionTransposeNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionTransposeNode (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionTransposeNode Create (MPSNNImageNode sourceNode, MPSCnnConvolutionStateNode convolutionState, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionTransposeNode -->
<div> <!-- start type MPSCnnCrossChannelNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSizeInFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnCrossChannelNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalizationNode -->
<div> <!-- start type MPSCnnDepthWiseConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnDepthWiseConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDepthWiseConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDepthWiseConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ChannelMultiplier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDepthWiseConvolutionDescriptor -->
<div> <!-- start type MPSCnnDilatedPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint dilationRateX, uint dilationRateY, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMax -->
<div> <!-- start type MPSCnnDilatedPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnDilatedPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnDilatedPoolingMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnDilatedPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnDilatedPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY, uint dilationRateX, uint dilationRateY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DilationRateY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnDilatedPoolingMaxNode Create (MPSNNImageNode sourceNode, uint size, uint stride, uint dilationRate);</span>
}
</pre>
</div> <!-- end type MPSCnnDilatedPoolingMaxNode -->
<div> <!-- start type MPSCnnFullyConnectedNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnectedNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnectedNode : MetalPerformanceShaders.MPSCnnConvolutionNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnectedNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnectedNode (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnFullyConnectedNode Create (MPSNNImageNode sourceNode, IMPSCnnConvolutionDataSource weights);</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnectedNode -->
<div> <!-- start type MPSCnnLocalContrastNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLocalContrastNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalizationNode -->
<div> <!-- start type MPSCnnLogSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnLogSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMaxNode -->
<div> <!-- start type MPSCnnNeuronAbsoluteNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsoluteNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsoluteNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsoluteNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsoluteNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronAbsoluteNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsoluteNode -->
<div> <!-- start type MPSCnnNeuronElu -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronElu</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronElu : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronElu (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronElu (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronElu -->
<div> <!-- start type MPSCnnNeuronEluNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronEluNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronEluNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronEluNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronEluNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronEluNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronEluNode -->
<div> <!-- start type MPSCnnNeuronHardSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoid (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoid -->
<div> <!-- start type MPSCnnNeuronHardSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronHardSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronHardSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronHardSigmoidNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronHardSigmoidNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronHardSigmoidNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronHardSigmoidNode -->
<div> <!-- start type MPSCnnNeuronLinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinearNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinearNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronLinearNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinearNode -->
<div> <!-- start type MPSCnnNeuronNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float C { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronNode -->
<div> <!-- start type MPSCnnNeuronPReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLU (Metal.IMTLDevice device, float[] a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLU -->
<div> <!-- start type MPSCnnNeuronPReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronPReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronPReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronPReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronPReLUNode (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronPReLUNode Create (MPSNNImageNode sourceNode, Foundation.NSData aData);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronPReLUNode -->
<div> <!-- start type MPSCnnNeuronReLUNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLUNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLUNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLUNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLUNode (MPSNNImageNode sourceNode, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLUNode Create (MPSNNImageNode sourceNode, float a);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLUNode -->
<div> <!-- start type MPSCnnNeuronReLun -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLun</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLun : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLun (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLun (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLun -->
<div> <!-- start type MPSCnnNeuronReLunNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLunNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLunNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLunNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLunNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronReLunNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLunNode -->
<div> <!-- start type MPSCnnNeuronSigmoidNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoidNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoidNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoidNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoidNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSigmoidNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoidNode -->
<div> <!-- start type MPSCnnNeuronSoftPlus -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlus</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlus : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlus (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlus (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlus -->
<div> <!-- start type MPSCnnNeuronSoftPlusNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftPlusNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftPlusNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftPlusNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftPlusNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftPlusNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftPlusNode -->
<div> <!-- start type MPSCnnNeuronSoftSign -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSign</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSign : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSign (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSign (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSign -->
<div> <!-- start type MPSCnnNeuronSoftSignNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSoftSignNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSoftSignNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSoftSignNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSoftSignNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronSoftSignNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSoftSignNode -->
<div> <!-- start type MPSCnnNeuronTanHNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanHNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanHNode : MetalPerformanceShaders.MPSCnnNeuronNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanHNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanHNode (MPSNNImageNode sourceNode, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNeuronTanHNode Create (MPSNNImageNode sourceNode, float a, float b);</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanHNode -->
<div> <!-- start type MPSCnnNeuronType -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSCnnNeuronType {
	<span class='added added-field ' data-is-non-breaking="">Absolute = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Elu = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HardSigmoid = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Linear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PReLU = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLU = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReLun = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Sigmoid = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftPlus = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftSign = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TanH = 5,</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronType -->
<div> <!-- start type MPSCnnNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNormalizationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNormalizationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnNormalizationNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnNormalizationNode -->
<div> <!-- start type MPSCnnPoolingAverageNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverageNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverageNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverageNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverageNode -->
<div> <!-- start type MPSCnnPoolingL2Norm -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2Norm</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2Norm : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2Norm (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2Norm (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2Norm -->
<div> <!-- start type MPSCnnPoolingL2NormNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingL2NormNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingL2NormNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingL2NormNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingL2NormNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingL2NormNode -->
<div> <!-- start type MPSCnnPoolingMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMaxNode : MetalPerformanceShaders.MPSCnnPoolingNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMaxNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMaxNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMaxNode -->
<div> <!-- start type MPSCnnPoolingNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint size, uint stride);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingNode (MPSNNImageNode sourceNode, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnPoolingNode Create (MPSNNImageNode sourceNode, uint size, uint stride);</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingNode -->
<div> <!-- start type MPSCnnSoftMaxNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMaxNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMaxNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMaxNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMaxNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSoftMaxNode Create (MPSNNImageNode sourceNode);</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMaxNode -->
<div> <!-- start type MPSCnnSpatialNormalizationNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalizationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalizationNode : MetalPerformanceShaders.MPSCnnNormalizationNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalizationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalizationNode (MPSNNImageNode sourceNode, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnSpatialNormalizationNode Create (MPSNNImageNode sourceNode, uint kernelSize);</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalizationNode -->
<div> <!-- start type MPSCnnSubPixelConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnSubPixelConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSubPixelConvolutionDescriptor : MetalPerformanceShaders.MPSCnnConvolutionDescriptor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSubPixelConvolutionDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSubPixelConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SubPixelScaleFactor { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnSubPixelConvolutionDescriptor -->
<div> <!-- start type MPSCnnUpsampling -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsampling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsampling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsampling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsampling (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsampling -->
<div> <!-- start type MPSCnnUpsamplingBilinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinear : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinear (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinear -->
<div> <!-- start type MPSCnnUpsamplingBilinearNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingBilinearNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingBilinearNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingBilinearNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingBilinearNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingBilinearNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingBilinearNode -->
<div> <!-- start type MPSCnnUpsamplingNearest -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearest</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearest : MetalPerformanceShaders.MPSCnnUpsampling, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearest (Metal.IMTLDevice device, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearest -->
<div> <!-- start type MPSCnnUpsamplingNearestNode -->
<h3>New Type MetalPerformanceShaders.MPSCnnUpsamplingNearestNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnUpsamplingNearestNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnUpsamplingNearestNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnUpsamplingNearestNode (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ScaleFactorY { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnUpsamplingNearestNode Create (MPSNNImageNode sourceNode, uint integerScaleFactorX, uint integerScaleFactorY);</span>
}
</pre>
</div> <!-- end type MPSCnnUpsamplingNearestNode -->
<div> <!-- start type MPSDataLayout -->
<h3>New Type MetalPerformanceShaders.MPSDataLayout</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataLayout {
	<span class='added added-field ' data-is-non-breaking="">FeatureChannelsPerHeightPerWidth = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HeightPerWidthPerFeatureChannels = 0,</span>
}
</pre>
</div> <!-- end type MPSDataLayout -->
<div> <!-- start type MPSGRUDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSGRUDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSGRUDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSGRUDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSGRUDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipOutputGates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float GatePnormValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputGateWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSGRUDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSGRUDescriptor -->
<div> <!-- start type MPSImageAdd -->
<h3>New Type MetalPerformanceShaders.MPSImageAdd</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageAdd : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAdd (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageAdd (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageAdd -->
<div> <!-- start type MPSImageArithmetic -->
<h3>New Type MetalPerformanceShaders.MPSImageArithmetic</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageArithmetic : MetalPerformanceShaders.MPSBinaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageArithmetic (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageArithmetic (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float PrimaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize PrimaryStrideInPixels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float SecondaryScale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLSize SecondaryStrideInPixels { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageArithmetic -->
<div> <!-- start type MPSImageBilinearScale -->
<h3>New Type MetalPerformanceShaders.MPSImageBilinearScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageBilinearScale : MetalPerformanceShaders.MPSImageScale, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageBilinearScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBilinearScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageBilinearScale -->
<div> <!-- start type MPSImageCopyToMatrix -->
<h3>New Type MetalPerformanceShaders.MPSImageCopyToMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageCopyToMatrix : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageCopyToMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageCopyToMatrix (Metal.IMTLDevice device, MPSDataLayout dataLayout);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataLayout DataLayout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationMatrixBatchIndex { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin DestinationMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSMatrix destinationMatrix);</span>
}
</pre>
</div> <!-- end type MPSImageCopyToMatrix -->
<div> <!-- start type MPSImageDivide -->
<h3>New Type MetalPerformanceShaders.MPSImageDivide</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDivide : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDivide (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDivide (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageDivide -->
<div> <!-- start type MPSImageFindKeypoints -->
<h3>New Type MetalPerformanceShaders.MPSImageFindKeypoints</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageFindKeypoints : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageFindKeypoints (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageFindKeypoints (Metal.IMTLDevice device, MPSImageKeypointRangeInfo info);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageKeypointRangeInfo KeypointRangeInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, Metal.IMTLTexture source, Metal.MTLRegion regions, uint numberOfRegions, Metal.IMTLBuffer keypointCountBuffer, uint keypointCountBufferOffset, Metal.IMTLBuffer keypointDataBuffer, uint keypointDataBufferOffset);</span>
}
</pre>
</div> <!-- end type MPSImageFindKeypoints -->
<div> <!-- start type MPSImageKeypointRangeInfo -->
<h3>New Type MetalPerformanceShaders.MPSImageKeypointRangeInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageKeypointRangeInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint MaximumKeypoints;</span>
	<span class='added added-field ' data-is-non-breaking="">public float MinimumThresholdValue;</span>
}
</pre>
</div> <!-- end type MPSImageKeypointRangeInfo -->
<div> <!-- start type MPSImageMultiply -->
<h3>New Type MetalPerformanceShaders.MPSImageMultiply</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageMultiply : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMultiply (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageMultiply (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageMultiply -->
<div> <!-- start type MPSImageReadWriteParams -->
<h3>New Type MetalPerformanceShaders.MPSImageReadWriteParams</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSImageReadWriteParams {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint FeatureChannelOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint NumberOfFeatureChannelsToReadWrite;</span>
}
</pre>
</div> <!-- end type MPSImageReadWriteParams -->
<div> <!-- start type MPSImageScale -->
<h3>New Type MetalPerformanceShaders.MPSImageScale</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageScale : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageScale (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageScale (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSScaleTransform ScaleTransform { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageScale -->
<div> <!-- start type MPSImageStatisticsMean -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMean</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMean : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMean (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMean (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMean -->
<div> <!-- start type MPSImageStatisticsMeanAndVariance -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMeanAndVariance</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMeanAndVariance : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMeanAndVariance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMeanAndVariance (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMeanAndVariance -->
<div> <!-- start type MPSImageStatisticsMinAndMax -->
<h3>New Type MetalPerformanceShaders.MPSImageStatisticsMinAndMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageStatisticsMinAndMax : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageStatisticsMinAndMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageStatisticsMinAndMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRectSource { get; set; }</span>
}
</pre>
</div> <!-- end type MPSImageStatisticsMinAndMax -->
<div> <!-- start type MPSImageSubtract -->
<h3>New Type MetalPerformanceShaders.MPSImageSubtract</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageSubtract : MetalPerformanceShaders.MPSImageArithmetic, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSubtract (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageSubtract (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageSubtract -->
<div> <!-- start type MPSLSTMDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSLSTMDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSLSTMDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSLSTMDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSLSTMDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreMemoryWeightsDiagonal { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource CellGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamA { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamB { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float CellToOutputNeuronParamC { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType CellToOutputNeuronType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource ForgetGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputGateRecurrentWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateInputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateMemoryWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource OutputGateRecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSLSTMDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSLSTMDescriptor -->
<div> <!-- start type MPSMatrixBinaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixBinaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixBinaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixBinaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixBinaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin PrimarySourceMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SecondarySourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixBinaryKernel -->
<div> <!-- start type MPSMatrixCopy -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopy</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopy : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopy (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopy (Metal.IMTLDevice device, uint copyRows, uint copyColumns, bool areSourcesTransposed, bool areDestinationsTransposed);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreDestinationsTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AreSourcesTransposed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyColumns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint CopyRows { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer cmdBuf, MPSMatrixCopyDescriptor copyDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixCopyDescriptor copyDescriptor, MPSVector rowPermuteIndices, uint rowPermuteOffset, MPSVector columnPermuteIndices, uint columnPermuteOffset);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopy -->
<div> <!-- start type MPSMatrixCopyDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixCopyDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixCopyDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (Metal.IMTLDevice device, uint count);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixCopyDescriptor (MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSVector offsets, uint byteOffset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixCopyDescriptor Create (MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCopyOperation (uint index, MPSMatrix sourceMatrix, MPSMatrix destinationMatrix, MPSMatrixCopyOffsets offsets);</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyDescriptor -->
<div> <!-- start type MPSMatrixCopyOffsets -->
<h3>New Type MetalPerformanceShaders.MPSMatrixCopyOffsets</h3>
<pre class='added' data-is-non-breaking="">
public struct MPSMatrixCopyOffsets {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint DestinationRowOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceColumnOffset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint SourceRowOffset;</span>
}
</pre>
</div> <!-- end type MPSMatrixCopyOffsets -->
<div> <!-- start type MPSMatrixDecompositionCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionCholesky : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionCholesky (Metal.IMTLDevice device, bool lower, uint order);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionCholesky -->
<div> <!-- start type MPSMatrixDecompositionLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDecompositionLU : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDecompositionLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixDecompositionLU (Metal.IMTLDevice device, uint rows, uint columns);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix resultMatrix, MPSMatrix pivotIndices, Metal.IMTLBuffer status);</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionLU -->
<div> <!-- start type MPSMatrixDecompositionStatus -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDecompositionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSMatrixDecompositionStatus {
	<span class='added added-field ' data-is-non-breaking="">Failure = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPositiveDefinite = -3,</span>
	<span class='added added-field ' data-is-non-breaking="">Singular = -2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type MPSMatrixDecompositionStatus -->
<div> <!-- start type MPSMatrixFindTopK -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFindTopK</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFindTopK : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFindTopK (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFindTopK (Metal.IMTLDevice device, uint numberOfTopKValues);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint IndexOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfTopKValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFindTopK Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultIndexMatrix, MPSMatrix resultValueMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixFindTopK -->
<div> <!-- start type MPSMatrixFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSMatrixFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixFullyConnected : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixFullyConnected (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceOutputFeatureChannels { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixFullyConnected Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix weightMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixFullyConnected -->
<div> <!-- start type MPSMatrixLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixLogSoftMax : MetalPerformanceShaders.MPSMatrixSoftMax, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixLogSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixLogSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrixLogSoftMax -->
<div> <!-- start type MPSMatrixNeuron -->
<h3>New Type MetalPerformanceShaders.MPSMatrixNeuron</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixNeuron : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixNeuron (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixNeuron (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceInputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceNumberOfFeatureVectors { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixNeuron Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector biasVector, MPSMatrix resultMatrix);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronToPReLU (Foundation.NSData parametersA);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixNeuron -->
<div> <!-- start type MPSMatrixSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSoftMax : MetalPerformanceShaders.MPSMatrixUnaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSoftMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSoftMax (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint SourceRows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrixSoftMax Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSoftMax -->
<div> <!-- start type MPSMatrixSolveCholesky -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveCholesky</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveCholesky : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveCholesky (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveCholesky (Metal.IMTLDevice device, bool upper, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveCholesky -->
<div> <!-- start type MPSMatrixSolveLU -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveLU : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveLU (Metal.IMTLDevice device, bool transpose, uint order, uint numberOfRightHandSides);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix pivotIndices, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveLU -->
<div> <!-- start type MPSMatrixSolveTriangular -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSolveTriangular</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSolveTriangular : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSolveTriangular (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSolveTriangular (Metal.IMTLDevice device, bool right, bool upper, bool transpose, bool unit, uint order, uint numberOfRightHandSides, double alpha);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix sourceMatrix, MPSMatrix rightHandSideMatrix, MPSMatrix solutionMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixSolveTriangular -->
<div> <!-- start type MPSMatrixSum -->
<h3>New Type MetalPerformanceShaders.MPSMatrixSum</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixSum : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixSum (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixSum (Metal.IMTLDevice device, uint count, uint rows, uint columns, bool transpose);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterA { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterB { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float NeuronParameterC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuronType NeuronType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Transpose { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer buffer, MPSMatrix[] sourceMatrices, MPSMatrix resultMatrix, MPSVector scaleVector, MPSVector offsetVector, MPSVector biasVector, uint startIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeuronType (MPSCnnNeuronType neuronType, float parameterA, float parameterB, float parameterC);</span>
}
</pre>
</div> <!-- end type MPSMatrixSum -->
<div> <!-- start type MPSMatrixUnaryKernel -->
<h3>New Type MetalPerformanceShaders.MPSMatrixUnaryKernel</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixUnaryKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixUnaryKernel (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixUnaryKernel (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BatchStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin SourceMatrixOrigin { get; set; }</span>
}
</pre>
</div> <!-- end type MPSMatrixUnaryKernel -->
<div> <!-- start type MPSMatrixVectorMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixVectorMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixVectorMultiplication : MetalPerformanceShaders.MPSMatrixBinaryKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixVectorMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, uint rows, uint columns);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixVectorMultiplication (Metal.IMTLDevice device, bool transpose, uint rows, uint columns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix inputMatrix, MPSVector inputVector, MPSVector resultVector);</span>
}
</pre>
</div> <!-- end type MPSMatrixVectorMultiplication -->
<div> <!-- start type MPSNNAdditionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNAdditionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNAdditionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNAdditionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNAdditionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNAdditionNode -->
<div> <!-- start type MPSNNBilinearScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBilinearScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBilinearScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBilinearScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBilinearScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNBilinearScaleNode -->
<div> <!-- start type MPSNNBinaryArithmeticNode -->
<h3>New Type MetalPerformanceShaders.MPSNNBinaryArithmeticNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNBinaryArithmeticNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNBinaryArithmeticNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNBinaryArithmeticNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNBinaryArithmeticNode Create (MPSNNImageNode left, MPSNNImageNode right);</span>
}
</pre>
</div> <!-- end type MPSNNBinaryArithmeticNode -->
<div> <!-- start type MPSNNConcatenationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNConcatenationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNConcatenationNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNConcatenationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNConcatenationNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNConcatenationNode Create (MPSNNImageNode[] sourceNodes);</span>
}
</pre>
</div> <!-- end type MPSNNConcatenationNode -->
<div> <!-- start type MPSNNDefaultPadding -->
<h3>New Type MetalPerformanceShaders.MPSNNDefaultPadding</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDefaultPadding : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IMPSNNPadding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDefaultPadding (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDefaultPadding (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNPaddingMethod PaddingMethod { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding Create (MPSNNPaddingMethod method);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNDefaultPadding CreatePaddingForTensorflowAveragePooling ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImageDescriptor GetDestinationImageDescriptor (MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetLabel ();</span>
}
</pre>
</div> <!-- end type MPSNNDefaultPadding -->
<div> <!-- start type MPSNNDivisionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNDivisionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNDivisionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNDivisionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNDivisionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNDivisionNode -->
<div> <!-- start type MPSNNFilterNode -->
<h3>New Type MetalPerformanceShaders.MPSNNFilterNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNFilterNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNFilterNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSNNPadding PaddingPolicy { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNImageNode ResultImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode ResultState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSNNStateNode[] ResultStates { get; }</span>
}
</pre>
</div> <!-- end type MPSNNFilterNode -->
<div> <!-- start type MPSNNGraph -->
<h3>New Type MetalPerformanceShaders.MPSNNGraph</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNGraph : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNGraph (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNGraph (Metal.IMTLDevice device, MPSNNImageNode resultImage);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator DestinationImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] IntermediateImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsOutputStateTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle ResultHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] ResultStateHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceImageHandles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle[] SourceStateHandles { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSState[] sourceStates, Foundation.NSMutableArray&lt;MPSImage&gt; intermediateImages, Foundation.NSMutableArray&lt;MPSState&gt; destinationStates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage Execute (MPSImage[] sourceImages, System.Action&lt;MPSImage,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPSImage&gt; ExecuteAsync (MPSImage[] sourceImages, MPSImage result);</span>
}
</pre>
</div> <!-- end type MPSNNGraph -->
<div> <!-- start type MPSNNImageNode -->
<h3>New Type MetalPerformanceShaders.MPSNNImageNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNImageNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNImageNode (IMPSHandle handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNImageNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExportFromGraph { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat Format { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSImageAllocator ImageAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode Create (IMPSHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNImageNode GetExportedNode (IMPSHandle handle);</span>
}
</pre>
</div> <!-- end type MPSNNImageNode -->
<div> <!-- start type MPSNNLanczosScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNLanczosScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNLanczosScaleNode : MetalPerformanceShaders.MPSNNScaleNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNLanczosScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNLanczosScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNLanczosScaleNode -->
<div> <!-- start type MPSNNMultiplicationNode -->
<h3>New Type MetalPerformanceShaders.MPSNNMultiplicationNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNMultiplicationNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNMultiplicationNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNMultiplicationNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNMultiplicationNode -->
<div> <!-- start type MPSNNPaddingMethod -->
<h3>New Type MetalPerformanceShaders.MPSNNPaddingMethod</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSNNPaddingMethod {
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomLeft = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToBottomRight = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopLeft = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AddRemainderToTopRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignBottomRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignCentered = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignReserved = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AlignTopLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Custom = 16384,</span>
	<span class='added added-field ' data-is-non-breaking="">ExcludeEdges = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeFull = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeMask = 2032,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeReserved = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeSame = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SizeValidOnly = 0,</span>
}
</pre>
</div> <!-- end type MPSNNPaddingMethod -->
<div> <!-- start type MPSNNPadding_Extensions -->
<h3>New Type MetalPerformanceShaders.MPSNNPadding_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPSNNPadding_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetDestinationImageDescriptor (IMPSNNPadding This, MPSImage[] sourceImages, MPSState[] sourceStates, MPSKernel kernel, MPSImageDescriptor inDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetLabel (IMPSNNPadding This);</span>
}
</pre>
</div> <!-- end type MPSNNPadding_Extensions -->
<div> <!-- start type MPSNNScaleNode -->
<h3>New Type MetalPerformanceShaders.MPSNNScaleNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNScaleNode : MetalPerformanceShaders.MPSNNFilterNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNScaleNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNScaleNode (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, Metal.MTLSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSNNScaleNode Create (MPSNNImageNode sourceNode, IMPSImageTransformProvider transformProvider, Metal.MTLSize size);</span>
}
</pre>
</div> <!-- end type MPSNNScaleNode -->
<div> <!-- start type MPSNNStateNode -->
<h3>New Type MetalPerformanceShaders.MPSNNStateNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNStateNode : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNStateNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSHandle MPSHandle { get; set; }</span>
}
</pre>
</div> <!-- end type MPSNNStateNode -->
<div> <!-- start type MPSNNSubtractionNode -->
<h3>New Type MetalPerformanceShaders.MPSNNSubtractionNode</h3>
<pre class='added' data-is-non-breaking="">
public class MPSNNSubtractionNode : MetalPerformanceShaders.MPSNNBinaryArithmeticNode, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode[] sourceNodes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSNNSubtractionNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSNNSubtractionNode (MPSNNImageNode left, MPSNNImageNode right);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSNNSubtractionNode -->
<div> <!-- start type MPSRnnBidirectionalCombineMode -->
<h3>New Type MetalPerformanceShaders.MPSRnnBidirectionalCombineMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnBidirectionalCombineMode {
	<span class='added added-field ' data-is-non-breaking="">Add = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Concatenate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnBidirectionalCombineMode -->
<div> <!-- start type MPSRnnDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnSequenceDirection LayerSequenceDirection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseFloat32Weights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UseLayerInputUnitTransformMode { get; set; }</span>
}
</pre>
</div> <!-- end type MPSRnnDescriptor -->
<div> <!-- start type MPSRnnImageInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnImageInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnImageInferenceLayer : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnImageInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnImageInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnImageInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceSequence, MPSImage[] destinationForwardImages, MPSImage[] destinationBackwardImages);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSImage[] sourceImages, MPSImage[] destinationImages, MPSRnnRecurrentImageState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentImageState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnImageInferenceLayer -->
<div> <!-- start type MPSRnnMatrixInferenceLayer -->
<h3>New Type MetalPerformanceShaders.MPSRnnMatrixInferenceLayer</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnMatrixInferenceLayer : MetalPerformanceShaders.MPSKernel, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnMatrixInferenceLayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Foundation.NSCoder aDecoder, Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor rnnDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnMatrixInferenceLayer (Metal.IMTLDevice device, MPSRnnDescriptor[] rnnDescriptors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSRnnBidirectionalCombineMode BidirectionalCombineMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsRecurrentOutputTemporary { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfLayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool StoreAllIntermediateStates { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRnnMatrixInferenceLayer Copy (Foundation.NSZone zone, Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeBidirectionalSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceSequence, MPSMatrix[] destinationForwardMatrices, MPSMatrix[] destinationBackwardMatrices);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeSequence (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix[] sourceMatrices, MPSMatrix[] destinationMatrices, MPSRnnRecurrentMatrixState recurrentInputState, Foundation.NSMutableArray&lt;MPSRnnRecurrentMatrixState&gt; recurrentOutputStates);</span>
}
</pre>
</div> <!-- end type MPSRnnMatrixInferenceLayer -->
<div> <!-- start type MPSRnnRecurrentImageState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentImageState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentImageState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentImageState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetMemoryCellImage (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSImage GetRecurrentOutputImage (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentImageState -->
<div> <!-- start type MPSRnnRecurrentMatrixState -->
<h3>New Type MetalPerformanceShaders.MPSRnnRecurrentMatrixState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnRecurrentMatrixState : MetalPerformanceShaders.MPSState, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnRecurrentMatrixState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetMemoryCellMatrix (uint layerIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSMatrix GetRecurrentOutputMatrix (uint layerIndex);</span>
}
</pre>
</div> <!-- end type MPSRnnRecurrentMatrixState -->
<div> <!-- start type MPSRnnSequenceDirection -->
<h3>New Type MetalPerformanceShaders.MPSRnnSequenceDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSRnnSequenceDirection {
	<span class='added added-field ' data-is-non-breaking="">Backward = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Forward = 0,</span>
}
</pre>
</div> <!-- end type MPSRnnSequenceDirection -->
<div> <!-- start type MPSRnnSingleGateDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSRnnSingleGateDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSRnnSingleGateDescriptor : MetalPerformanceShaders.MPSRnnDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPSRnnSingleGateDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSRnnSingleGateDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource InputWeights { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMPSCnnConvolutionDataSource RecurrentWeights { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSRnnSingleGateDescriptor Create (uint inputFeatureChannels, uint outputFeatureChannels);</span>
}
</pre>
</div> <!-- end type MPSRnnSingleGateDescriptor -->
<div> <!-- start type MPSState -->
<h3>New Type MetalPerformanceShaders.MPSState</h3>
<pre class='added' data-is-non-breaking="">
public class MPSState : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSState (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsTemporary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
}
</pre>
</div> <!-- end type MPSState -->
<div> <!-- start type MPSTemporaryMatrix -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryMatrix : MetalPerformanceShaders.MPSMatrix, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryMatrix (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryMatrix Create (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor matrixDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSMatrixDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryMatrix -->
<div> <!-- start type MPSTemporaryVector -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryVector : MetalPerformanceShaders.MPSVector, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryVector (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryVector Create (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSVectorDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryVector -->
<div> <!-- start type MPSVector -->
<h3>New Type MetalPerformanceShaders.MPSVector</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVector : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVector (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSVector (Metal.IMTLBuffer buffer, MPSVectorDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
}
</pre>
</div> <!-- end type MPSVector -->
<div> <!-- start type MPSVectorDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSVectorDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSVectorDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSVectorDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Length { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VectorBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Vectors { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSVectorDescriptor Create (uint length, uint vectors, uint vectorBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetVectorBytes (uint length, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSVectorDescriptor -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"11.1"</span> <span class='added '>"11.2"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.4.0"</span> <span class='added '>"11.6.1"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace ReplayKit --> <div> 
<h2>Namespace ReplayKit</h2>
<!-- start type RPRecordingError --> <div>
<h3>Type Changed: ReplayKit.RPRecordingError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailedApplicationConnectionInterrupted = -5815,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedApplicationConnectionInvalid = -5814,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedMediaServicesFailure = -5817,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedNoMatchingApplicationContext = -5816,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoMixingFailure = -5818,</span>
</pre>
</div>

</div> <!-- end type RPRecordingError -->

</div> <!-- end namespace ReplayKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecCertificate --> <div>
<h3>Type Changed: Security.SecCertificate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetSerialNumber (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type SecCertificate -->
<!-- start type SecKeyAlgorithm --> <div>
<h3>Type Changed: Security.SecKeyAlgorithm</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha224AesGcm = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha256AesGcm = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha384AesGcm = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionCofactorVariableIvx963Sha512AesGcm = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha224AesGcm = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha256AesGcm = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha384AesGcm = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">EciesEncryptionStandardVariableIvx963Sha512AesGcm = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha1 = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha224 = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha256 = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha384 = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureDigestPssSha512 = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha1 = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha224 = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha256 = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha384 = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">RsaSignatureMessagePssSha512 = 67,</span>
</pre>
</div>

</div> <!-- end type SecKeyAlgorithm -->
<!-- start type SecRecord --> <div>
<h3>Type Changed: Security.SecRecord</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool PersistentReference { get; set; }</span>
</pre>
</div>

</div> <!-- end type SecRecord -->
<!-- start type SecStatusCode --> <div>
<h3>Type Changed: Security.SecStatusCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MissingEntitlement = -34018,</span>
</pre>
</div>

</div> <!-- end type SecStatusCode -->
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 = 52393,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 = 52392,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->
<!-- start type SslContext --> <div>
<h3>Type Changed: Security.SslContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetAlpnProtocols ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetAlpnProtocols (int error);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetAlpnProtocols (string[] protocols);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetError (SecStatusCode status);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetOcspResponse (Foundation.NSData response);</span>
	<span class='added added-method ' data-is-non-breaking="">public int SetSessionTickets (bool enabled);</span>
</pre>
</div>

</div> <!-- end type SslContext -->
<!-- start type SslProtocol --> <div>
<h3>Type Changed: Security.SslProtocol</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Tls_1_3 = 10,</span>
</pre>
</div>

</div> <!-- end type SslProtocol -->
<!-- start type SslSessionOption --> <div>
<h3>Type Changed: Security.SslSessionOption</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">EnableSessionTickets = 9,</span>
</pre>
</div>

</div> <!-- end type SslSessionOption -->

</div> <!-- end namespace Security -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKProduct --> <div>
<h3>Type Changed: StoreKit.SKProduct</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscount IntroductoryPrice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
</pre>
</div>

</div> <!-- end type SKProduct -->
<div> <!-- start type SKProductDiscount -->
<h3>New Type StoreKit.SKProductDiscount</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductDiscount : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductDiscount ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductDiscount (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfPeriods { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductDiscountPaymentMode PaymentMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Price { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSLocale PriceLocale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductSubscriptionPeriod SubscriptionPeriod { get; }</span>
}
</pre>
</div> <!-- end type SKProductDiscount -->
<div> <!-- start type SKProductDiscountPaymentMode -->
<h3>New Type StoreKit.SKProductDiscountPaymentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductDiscountPaymentMode {
	<span class='added added-field ' data-is-non-breaking="">FreeTrial = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PayAsYouGo = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PayUpFront = 1,</span>
}
</pre>
</div> <!-- end type SKProductDiscountPaymentMode -->
<div> <!-- start type SKProductPeriodUnit -->
<h3>New Type StoreKit.SKProductPeriodUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductPeriodUnit {
	<span class='added added-field ' data-is-non-breaking="">Day = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Month = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Week = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Year = 3,</span>
}
</pre>
</div> <!-- end type SKProductPeriodUnit -->
<div> <!-- start type SKProductSubscriptionPeriod -->
<h3>New Type StoreKit.SKProductSubscriptionPeriod</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductSubscriptionPeriod : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKProductSubscriptionPeriod ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductSubscriptionPeriod (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfUnits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKProductPeriodUnit Unit { get; }</span>
}
</pre>
</div> <!-- end type SKProductSubscriptionPeriod -->

</div> <!-- end namespace StoreKit -->
</div>



   


 <hr>
