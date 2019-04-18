---
id: FE7B7823-DAFF-4F6A-96E4-82BE374D9944
title: "iOS 11.6.1 to 11.6.99"
---

# API diff

 [Xamarin.iOS.dll](#diff/xi/Xamarin.iOS/Xamarin.iOS.html)

   


   


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
</script><h1 id='diff/xi/Xamarin.iOS/Xamarin.iOS.html'>Xamarin.iOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace ARKit --> <div> 
<h2>Namespace ARKit</h2>
<!-- start type ARAnchor --> <div>
<h3>Type Changed: ARKit.ARAnchor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ARAnchor (Foundation.NSCoder coder);</span>
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

</div> <!-- end type ARAnchor -->
<!-- start type ARConfiguration --> <div>
<h3>Type Changed: ARKit.ARConfiguration</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static ARVideoFormat[] SupportedVideoFormats { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARVideoFormat VideoFormat { get; set; }</span>
</pre>
</div>

</div> <!-- end type ARConfiguration -->
<!-- start type ARFaceAnchor --> <div>
<h3>Type Changed: ARKit.ARFaceAnchor</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Constructor marked as unavailable.")]
	public ARFaceAnchor ();</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ARFaceAnchor (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type ARFaceAnchor -->
<!-- start type ARFaceGeometry --> <div>
<h3>Type Changed: ARKit.ARFaceGeometry</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ARFaceGeometry (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetTextureCoordinates' method instead.")]
	public virtual OpenTK.Vector2 TextureCoordinates { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetTriangleIndices' method instead.")]
	public virtual short TriangleIndices { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use the 'GetVertices' method instead.")]
	public virtual OpenTK.NVector3 Vertices { get; }</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawVertices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.Vector2[] GetTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public short[] GetTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.NVector3[] GetVertices ();</span>
</pre>
</div>

</div> <!-- end type ARFaceGeometry -->
<!-- start type ARHitTestResultType --> <div>
<h3>Type Changed: ARKit.ARHitTestResultType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExistingPlaneUsingGeometry = 32,</span>
</pre>
</div>

</div> <!-- end type ARHitTestResultType -->
<!-- start type AROrientationTrackingConfiguration --> <div>
<h3>Type Changed: ARKit.AROrientationTrackingConfiguration</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoFocusEnabled { get; set; }</span>
</pre>
</div>

</div> <!-- end type AROrientationTrackingConfiguration -->
<!-- start type ARPlaneAnchor --> <div>
<h3>Type Changed: ARKit.ARPlaneAnchor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ARPlaneAnchor (Foundation.NSCoder coder);</span>
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
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARPlaneGeometry Geometry { get; }</span>
</pre>
</div>

</div> <!-- end type ARPlaneAnchor -->
<!-- start type ARPlaneAnchorAlignment --> <div>
<h3>Type Changed: ARKit.ARPlaneAnchorAlignment</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Vertical = 1,</span>
</pre>
</div>

</div> <!-- end type ARPlaneAnchorAlignment -->
<!-- start type ARPlaneDetection --> <div>
<h3>Type Changed: ARKit.ARPlaneDetection</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Vertical = 2,</span>
</pre>
</div>

</div> <!-- end type ARPlaneDetection -->
<!-- start type ARPointCloud --> <div>
<h3>Type Changed: ARKit.ARPointCloud</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ARPointCloud (Foundation.NSCoder coder);</span>
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

</div> <!-- end type ARPointCloud -->
<!-- start type ARSCNFaceGeometry --> <div>
<h3>Type Changed: ARKit.ARSCNFaceGeometry</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'Create' static constructor instead.")]
	public static ARSCNFaceGeometry CreateFaceGeometry (Metal.IMTLDevice device);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the 'Create' static constructor instead.")]
	public static ARSCNFaceGeometry CreateFaceGeometry (Metal.IMTLDevice device, bool fillMesh);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNFaceGeometry Create (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNFaceGeometry Create (Metal.IMTLDevice device, bool fillMesh);</span>
</pre>
</div>

</div> <!-- end type ARSCNFaceGeometry -->
<!-- start type ARSCNViewDelegate --> <div>
<h3>Type Changed: ARKit.ARSCNViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAttemptRelocalization (ARSession session);</span>
</pre>
</div>

</div> <!-- end type ARSCNViewDelegate -->
<!-- start type ARSKViewDelegate --> <div>
<h3>Type Changed: ARKit.ARSKViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAttemptRelocalization (ARSession session);</span>
</pre>
</div>

</div> <!-- end type ARSKViewDelegate -->
<!-- start type ARSession --> <div>
<h3>Type Changed: ARKit.ARSession</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetWorldOrigin (OpenTK.NMatrix4 relativeTransform);</span>
</pre>
</div>

</div> <!-- end type ARSession -->
<!-- start type ARSessionDelegate --> <div>
<h3>Type Changed: ARKit.ARSessionDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAttemptRelocalization (ARSession session);</span>
</pre>
</div>

</div> <!-- end type ARSessionDelegate -->
<!-- start type ARSessionObserver_Extensions --> <div>
<h3>Type Changed: ARKit.ARSessionObserver_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAttemptRelocalization (IARSessionObserver This, ARSession session);</span>
</pre>
</div>

</div> <!-- end type ARSessionObserver_Extensions -->
<!-- start type ARTrackingStateReason --> <div>
<h3>Type Changed: ARKit.ARTrackingStateReason</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Relocalizing = 4,</span>
</pre>
</div>

</div> <!-- end type ARTrackingStateReason -->
<!-- start type ARWorldTrackingConfiguration --> <div>
<h3>Type Changed: ARKit.ARWorldTrackingConfiguration</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutoFocusEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;ARReferenceImage&gt; DetectionImages { get; set; }</span>
</pre>
</div>

</div> <!-- end type ARWorldTrackingConfiguration -->
<div> <!-- start type ARImageAnchor -->
<h3>New Type ARKit.ARImageAnchor</h3>
<pre class='added' data-is-non-breaking="">
public class ARImageAnchor : ARKit.ARAnchor, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARImageAnchor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARImageAnchor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARImageAnchor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ARReferenceImage ReferenceImage { get; }</span>
}
</pre>
</div> <!-- end type ARImageAnchor -->
<div> <!-- start type ARPlaneGeometry -->
<h3>New Type ARKit.ARPlaneGeometry</h3>
<pre class='added' data-is-non-breaking="">
public class ARPlaneGeometry : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARPlaneGeometry (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPlaneGeometry (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARPlaneGeometry (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BoundaryVertexCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint TextureCoordinateCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint TriangleCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint VertexCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.NVector3[] GetBoundaryVertices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawBoundaryVertices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IntPtr GetRawVertices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.Vector2[] GetTextureCoordinates ();</span>
	<span class='added added-method ' data-is-non-breaking="">public short[] GetTriangleIndices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public OpenTK.NVector3[] GetVertices ();</span>
}
</pre>
</div> <!-- end type ARPlaneGeometry -->
<div> <!-- start type ARReferenceImage -->
<h3>New Type ARKit.ARReferenceImage</h3>
<pre class='added' data-is-non-breaking="">
public class ARReferenceImage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARReferenceImage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARReferenceImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARReferenceImage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ARReferenceImage (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, nfloat physicalWidth);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ARReferenceImage (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, nfloat physicalWidth);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize PhysicalSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSSet&lt;ARReferenceImage&gt; GetReferenceImagesInGroup (string name, Foundation.NSBundle bundle);</span>
}
</pre>
</div> <!-- end type ARReferenceImage -->
<div> <!-- start type ARSCNPlaneGeometry -->
<h3>New Type ARKit.ARSCNPlaneGeometry</h3>
<pre class='added' data-is-non-breaking="">
public class ARSCNPlaneGeometry : SceneKit.SCNGeometry, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, SceneKit.ISCNAnimatable, SceneKit.ISCNBoundingVolume, SceneKit.ISCNShadable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ARSCNPlaneGeometry (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNPlaneGeometry (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARSCNPlaneGeometry (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ARSCNPlaneGeometry Create (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (ARPlaneGeometry planeGeometry);</span>
}
</pre>
</div> <!-- end type ARSCNPlaneGeometry -->
<div> <!-- start type ARVideoFormat -->
<h3>New Type ARKit.ARVideoFormat</h3>
<pre class='added' data-is-non-breaking="">
public class ARVideoFormat : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected ARVideoFormat (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ARVideoFormat (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint FramesPerSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize ImageResolution { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type ARVideoFormat -->

</div> <!-- end namespace ARKit -->
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
<!-- start type HMHome --> <div>
<h3>Type Changed: HomeKit.HMHome</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAndSetupAccessories (HMAccessorySetupPayload payload, System.Action&lt;HMAccessory[],Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;HMAccessory[]&gt; AddAndSetupAccessoriesAsync (HMAccessorySetupPayload payload);</span>
</pre>
</div>

</div> <!-- end type HMHome -->
<div> <!-- start type HMAccessorySetupPayload -->
<h3>New Type HomeKit.HMAccessorySetupPayload</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessorySetupPayload : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessorySetupPayload (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessorySetupPayload (Foundation.NSUrl setupPayloadUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessorySetupPayload (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMAccessorySetupPayload -->

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
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenExrDictionary { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INSpatialEventTrigger --> <div>
<h3>Type Changed: Intents.INSpatialEventTrigger</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpatialEventTrigger (Foundation.NSCoder coder);</span>
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

</div> <!-- end type INSpatialEventTrigger -->
<!-- start type INSpeakableString --> <div>
<h3>Type Changed: Intents.INSpeakableString</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (Foundation.NSCoder coder);</span>
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

</div> <!-- end type INSpeakableString -->

</div> <!-- end namespace Intents -->
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
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKSuicaPassProperties --> <div>
<h3>Type Changed: PassKit.PKSuicaPassProperties</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>PassKit.PKTransitPassProperties</span>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool BalanceAllowedForCommute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LowBalanceGateNotificationEnabled { get; }</span>
</pre>
</div>

</div> <!-- end type PKSuicaPassProperties -->
<div> <!-- start type PKTransitPassProperties -->
<h3>New Type PassKit.PKTransitPassProperties</h3>
<pre class='added' data-is-non-breaking="">
public class PKTransitPassProperties : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKTransitPassProperties (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKTransitPassProperties (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Blacklisted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ExpirationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InStation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber TransitBalance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransitBalanceCurrencyCode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PKTransitPassProperties GetPassProperties (PKPass pass);</span>
}
</pre>
</div> <!-- end type PKTransitPassProperties -->

</div> <!-- end namespace PassKit -->
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
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKPreferences --> <div>
<h3>Type Changed: WebKit.WKPreferences</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKPreferences -->
<!-- start type WKProcessPool --> <div>
<h3>Type Changed: WebKit.WKProcessPool</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKProcessPool -->
<!-- start type WKUserContentController --> <div>
<h3>Type Changed: WebKit.WKUserContentController</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKUserContentController -->
<!-- start type WKWebViewConfiguration --> <div>
<h3>Type Changed: WebKit.WKWebViewConfiguration</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebViewConfiguration -->
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->
<!-- start type WKWebsiteDataType --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FetchCache { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceWorkerRegistrations { get; }</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataType -->

</div> <!-- end namespace WebKit -->
<!-- start namespace iAd --> <div> 
<h2>Namespace iAd</h2>
<!-- start type ADClientError --> <div>
<h3>Type Changed: iAd.ADClientError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CorruptResponse = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingData = 2,</span>
</pre>
</div>

</div> <!-- end type ADClientError -->

</div> <!-- end namespace iAd -->
</div>



   


 <hr>
