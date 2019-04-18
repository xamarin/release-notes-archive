---
id: 46774C17-F8E3-4C7F-B097-00D5EACA71C9
title: "watchOS 11.2.0 to 11.3.0"
---

# API diff

 [Xamarin.WatchOS.dll](#diff/xi/Xamarin.WatchOS/Xamarin.WatchOS.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.WatchOS/Xamarin.WatchOS.html'>Xamarin.WatchOS.dll</h1>

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

</div> <!-- end namespace AVFoundation -->
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

</div> <!-- end namespace CoreVideo -->
<!-- start namespace HealthKit --> <div> 
<h2>Namespace HealthKit</h2>
<!-- start type HKDeletedObject --> <div>
<h3>Type Changed: HealthKit.HKDeletedObject</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public HKMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary WeakMetadata { get; }</span>
</pre>
</div>

</div> <!-- end type HKDeletedObject -->
<!-- start type HKMetadata --> <div>
<h3>Type Changed: HealthKit.HKMetadata</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public HKBloodGlucoseMealTime? BloodGlucoseMealTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKHeartRateMotionContext? HeartRateMotionContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKInsulinDeliveryReason? InsulinDeliveryReason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string SyncIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? SyncVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKVO2MaxTestType? VO2MaxTestType { get; }</span>
</pre>
</div>

</div> <!-- end type HKMetadata -->
<!-- start type HKMetadataKey --> <div>
<h3>Type Changed: HealthKit.HKMetadataKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BloodGlucoseMealTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HeartRateMotionContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString InsulinDeliveryReason { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SyncIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SyncVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VO2MaxTestType { get; }</span>
</pre>
</div>

</div> <!-- end type HKMetadataKey -->
<!-- start type HKObjectType --> <div>
<h3>Type Changed: HealthKit.HKObjectType</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static HKSeriesType GetSeriesType (string identifier);</span>
</pre>
</div>

</div> <!-- end type HKObjectType -->
<!-- start type HKPredicateKeyPath --> <div>
<h3>Type Changed: HealthKit.HKPredicateKeyPath</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TotalFlightsClimbed { get; }</span>
</pre>
</div>

</div> <!-- end type HKPredicateKeyPath -->
<!-- start type HKQuantityTypeIdentifier --> <div>
<h3>Type Changed: HealthKit.HKQuantityTypeIdentifier</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">VO2Max = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">WaistCircumference = 73,</span>
</pre>
</div>

</div> <!-- end type HKQuantityTypeIdentifier -->
<!-- start type HKQuantityTypeIdentifierKey --> <div>
<h3>Type Changed: HealthKit.HKQuantityTypeIdentifierKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HeartRateVariabilitySdnn { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString InsulinDelivery { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestingHeartRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VO2Max { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WaistCircumference { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WalkingHeartRateAverage { get; }</span>
</pre>
</div>

</div> <!-- end type HKQuantityTypeIdentifierKey -->
<!-- start type HKQuery --> <div>
<h3>Type Changed: HealthKit.HKQuery</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate GetPredicateForTotalFlightsClimbed (Foundation.NSPredicateOperatorType operatorType, HKQuantity totalFlightsClimbed);</span>
</pre>
</div>

</div> <!-- end type HKQuery -->
<!-- start type HKSourceRevision --> <div>
<h3>Type Changed: HealthKit.HKSourceRevision</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public HKSourceRevision (HKSource source, string version, string productType, Foundation.NSOperatingSystemVersion operatingSystemVersion);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSOperatingSystemVersion OperatingSystemVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProductType { get; }</span>
</pre>
</div>

</div> <!-- end type HKSourceRevision -->
<!-- start type HKUnit --> <div>
<h3>Type Changed: HealthKit.HKUnit</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static HKUnit InternationalUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static HKUnit LargeCalorie { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static HKUnit SmallCalorie { get; }</span>
</pre>
</div>

</div> <!-- end type HKUnit -->
<!-- start type HKWorkout --> <div>
<h3>Type Changed: HealthKit.HKWorkout</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SortIdentifierTotalFlightsClimbed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HKQuantity TotalFlightsClimbed { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static HKWorkout CreateFlightsClimbedWorkout (HKWorkoutActivityType workoutActivityType, Foundation.NSDate startDate, Foundation.NSDate endDate, HKWorkoutEvent[] workoutEvents, HKQuantity totalEnergyBurned, HKQuantity totalDistance, HKQuantity totalFlightsClimbed, HKDevice device, Foundation.NSDictionary metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HKWorkout CreateFlightsClimbedWorkout (HKWorkoutActivityType workoutActivityType, Foundation.NSDate startDate, Foundation.NSDate endDate, HKWorkoutEvent[] workoutEvents, HKQuantity totalEnergyBurned, HKQuantity totalDistance, HKQuantity totalFlightsClimbed, HKDevice device, HKMetadata metadata);</span>
</pre>
</div>

</div> <!-- end type HKWorkout -->
<!-- start type HKWorkoutActivityType --> <div>
<h3>Type Changed: HealthKit.HKWorkoutActivityType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandCycling = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">MixedCardio = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">TaiChi = 72,</span>
</pre>
</div>

</div> <!-- end type HKWorkoutActivityType -->
<!-- start type HKWorkoutEvent --> <div>
<h3>Type Changed: HealthKit.HKWorkoutEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateInterval DateInterval { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static HKWorkoutEvent Create (HKWorkoutEventType type, Foundation.NSDateInterval dateInterval, Foundation.NSDictionary metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HKWorkoutEvent Create (HKWorkoutEventType type, Foundation.NSDateInterval dateInterval, HKMetadata metadata);</span>
</pre>
</div>

</div> <!-- end type HKWorkoutEvent -->
<!-- start type HKWorkoutEventType --> <div>
<h3>Type Changed: HealthKit.HKWorkoutEventType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PauseOrResumeRequest = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Segment = 7,</span>
</pre>
</div>

</div> <!-- end type HKWorkoutEventType -->
<div> <!-- start type HKBloodGlucoseMealTime -->
<h3>New Type HealthKit.HKBloodGlucoseMealTime</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HKBloodGlucoseMealTime {
	<span class='added added-field ' data-is-non-breaking="">Ostprandial = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Reprandial = 1,</span>
}
</pre>
</div> <!-- end type HKBloodGlucoseMealTime -->
<div> <!-- start type HKHeartRateMotionContext -->
<h3>New Type HealthKit.HKHeartRateMotionContext</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HKHeartRateMotionContext {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotSet = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sedentary = 1,</span>
}
</pre>
</div> <!-- end type HKHeartRateMotionContext -->
<div> <!-- start type HKInsulinDeliveryReason -->
<h3>New Type HealthKit.HKInsulinDeliveryReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HKInsulinDeliveryReason {
	<span class='added added-field ' data-is-non-breaking="">Asal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Olus = 2,</span>
}
</pre>
</div> <!-- end type HKInsulinDeliveryReason -->
<div> <!-- start type HKSeriesBuilder -->
<h3>New Type HealthKit.HKSeriesBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class HKSeriesBuilder : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKSeriesBuilder (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesBuilder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesBuilder (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Discard ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type HKSeriesBuilder -->
<div> <!-- start type HKSeriesSample -->
<h3>New Type HealthKit.HKSeriesSample</h3>
<pre class='added' data-is-non-breaking="">
public class HKSeriesSample : HealthKit.HKSample, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKSeriesSample (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesSample (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesSample (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HKSeriesSample -->
<div> <!-- start type HKSeriesType -->
<h3>New Type HealthKit.HKSeriesType</h3>
<pre class='added' data-is-non-breaking="">
public class HKSeriesType : HealthKit.HKSampleType, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKSeriesType (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesType (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKSeriesType (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static HKSeriesType WorkoutRouteType { get; }</span>
}
</pre>
</div> <!-- end type HKSeriesType -->
<div> <!-- start type HKSourceRevisionInfo -->
<h3>New Type HealthKit.HKSourceRevisionInfo</h3>
<pre class='added' data-is-non-breaking="">
public static class HKSourceRevisionInfo {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnyProductType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnyVersion { get; }</span>
}
</pre>
</div> <!-- end type HKSourceRevisionInfo -->
<div> <!-- start type HKVO2MaxTestType -->
<h3>New Type HealthKit.HKVO2MaxTestType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HKVO2MaxTestType {
	<span class='added added-field ' data-is-non-breaking="">MaxExercise = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PredictionNonExercise = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">PredictionSubMaxExercise = 2,</span>
}
</pre>
</div> <!-- end type HKVO2MaxTestType -->
<div> <!-- start type HKWorkoutRoute -->
<h3>New Type HealthKit.HKWorkoutRoute</h3>
<pre class='added' data-is-non-breaking="">
public class HKWorkoutRoute : HealthKit.HKSeriesSample, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRoute (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRoute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRoute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HKWorkoutRoute -->
<div> <!-- start type HKWorkoutRouteBuilder -->
<h3>New Type HealthKit.HKWorkoutRouteBuilder</h3>
<pre class='added' data-is-non-breaking="">
public class HKWorkoutRouteBuilder : HealthKit.HKSeriesBuilder, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRouteBuilder (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRouteBuilder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRouteBuilder (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRouteBuilder (HKHealthStore healthStore, HKDevice device);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected virtual void FinishRoute (HKWorkout workout, Foundation.NSDictionary metadata, System.Action&lt;HKWorkoutRoute,Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FinishRoute (HKWorkout workout, HKMetadata metadata, System.Action&lt;HKWorkoutRoute,Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual System.Threading.Tasks.Task&lt;HKWorkoutRoute&gt; FinishRouteAsync (HKWorkout workout, Foundation.NSDictionary metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;HKWorkoutRoute&gt; FinishRouteAsync (HKWorkout workout, HKMetadata metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertRouteData (CoreLocation.CLLocation[] routeData, System.Action&lt;System.Boolean,Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; InsertRouteDataAsync (CoreLocation.CLLocation[] routeData);</span>
}
</pre>
</div> <!-- end type HKWorkoutRouteBuilder -->
<div> <!-- start type HKWorkoutRouteBuilderDataHandler -->
<h3>New Type HealthKit.HKWorkoutRouteBuilderDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate HKWorkoutRouteBuilderDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRouteBuilderDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (HKWorkoutRouteQuery query, CoreLocation.CLLocation[] routeData, bool done, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (HKWorkoutRouteQuery query, CoreLocation.CLLocation[] routeData, bool done, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type HKWorkoutRouteBuilderDataHandler -->
<div> <!-- start type HKWorkoutRouteQuery -->
<h3>New Type HealthKit.HKWorkoutRouteQuery</h3>
<pre class='added' data-is-non-breaking="">
public class HKWorkoutRouteQuery : HealthKit.HKQuery, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRouteQuery ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRouteQuery (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HKWorkoutRouteQuery (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HKWorkoutRouteQuery (HKWorkoutRoute workoutRoute, HKWorkoutRouteBuilderDataHandler dataHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HKWorkoutRouteQuery -->

</div> <!-- end namespace HealthKit -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INRequestPaymentIntentResponseCode --> <div>
<h3>Type Changed: Intents.INRequestPaymentIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureTermsAndConditionsAcceptanceRequired = 12,</span>
</pre>
</div>

</div> <!-- end type INRequestPaymentIntentResponseCode -->
<!-- start type INRequestPaymentPayerUnsupportedReason --> <div>
<h3>Type Changed: Intents.INRequestPaymentPayerUnsupportedReason</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NoValidHandle = 3,</span>
</pre>
</div>

</div> <!-- end type INRequestPaymentPayerUnsupportedReason -->
<!-- start type INSendPaymentIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSendPaymentIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureTermsAndConditionsAcceptanceRequired = 13,</span>
</pre>
</div>

</div> <!-- end type INSendPaymentIntentResponseCode -->
<!-- start type INSendPaymentPayeeUnsupportedReason --> <div>
<h3>Type Changed: Intents.INSendPaymentPayeeUnsupportedReason</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NoValidHandle = 4,</span>
</pre>
</div>

</div> <!-- end type INSendPaymentPayeeUnsupportedReason -->

</div> <!-- end namespace Intents -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"4.0"</span> <span class='added '>"4.1"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.2.0"</span> <span class='added '>"11.3.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
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
</div>



   


 <hr>
