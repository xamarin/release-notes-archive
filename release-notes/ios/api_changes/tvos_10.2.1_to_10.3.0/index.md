---
id: DE15EFF2-60C2-4918-A99B-68A5307CDCE9
title: "tvOS 10.2.1 to 10.3.0"
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
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime OverallDurationHint { get; }</span>
</pre>
</div>

</div> <!-- end type AVAsset -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<div> <!-- start type AVKitMetadataIdentifier -->
<h3>New Type AVKit.AVKitMetadataIdentifier</h3>
<pre class='added' data-is-non-breaking="">
public static class AVKitMetadataIdentifier {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExternalContentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExternalUserProfileIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackProgress { get; }</span>
}
</pre>
</div> <!-- end type AVKitMetadataIdentifier -->

</div> <!-- end namespace AVKit -->
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessoryCategoryType --> <div>
<h3>Type Changed: HomeKit.HMAccessoryCategoryType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AirConditioner = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">AirDehumidifier = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">AirHeater = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">AirHumidifier = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">AirPurifier = 18,</span>
</pre>
</div>

</div> <!-- end type HMAccessoryCategoryType -->
<!-- start type HMCameraSnapshotControlDelegate --> <div>
<h3>Type Changed: HomeKit.HMCameraSnapshotControlDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateMostRecentSnapshot (HMCameraSnapshotControl cameraSnapshotControl);</span>
</pre>
</div>

</div> <!-- end type HMCameraSnapshotControlDelegate -->
<!-- start type HMCameraSnapshotControlDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMCameraSnapshotControlDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateMostRecentSnapshot (IHMCameraSnapshotControlDelegate This, HMCameraSnapshotControl cameraSnapshotControl);</span>
</pre>
</div>

</div> <!-- end type HMCameraSnapshotControlDelegate_Extensions -->
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("This value does not exist anymore and will always return null")]
	HeatingCoolingStatus = 12,</span>
</div></pre>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Active = 85,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentAirPurifierState = 86,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentFanState = 88,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentHeaterCoolerState = 89,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentHumidifierDehumidifierState = 90,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentSlatState = 91,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentTilt = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">DehumidifierThreshold = 110,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterChangeIndication = 93,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterLifeLevel = 94,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterResetChangeIndication = 95,</span>
	<span class='added added-field ' data-is-non-breaking="">HumidifierThreshold = 111,</span>
	<span class='added added-field ' data-is-non-breaking="">LockPhysicalControls = 96,</span>
	<span class='added added-field ' data-is-non-breaking="">NitrogenDioxideDensity = 105,</span>
	<span class='added added-field ' data-is-non-breaking="">OzoneDensity = 104,</span>
	<span class='added added-field ' data-is-non-breaking="">PM10Density = 108,</span>
	<span class='added added-field ' data-is-non-breaking="">PM2_5Density = 107,</span>
	<span class='added added-field ' data-is-non-breaking="">SecuritySystemAlarmType = 112,</span>
	<span class='added added-field ' data-is-non-breaking="">SlatType = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">SulphurDioxideDensity = 106,</span>
	<span class='added added-field ' data-is-non-breaking="">SwingMode = 97,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetAirPurifierState = 87,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetFanState = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetHeaterCoolerState = 98,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetHumidifierDehumidifierState = 99,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetTilt = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">VolatileOrganicCompoundDensity = 109,</span>
	<span class='added added-field ' data-is-non-breaking="">WaterLevel = 92,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMCharacteristicValueChargingState --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicValueChargingState</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">NotChargeable = 2,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicValueChargingState -->
<!-- start type HMError --> <div>
<h3>Type Changed: HomeKit.HMError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IncompatibleNetwork = 90,</span>
</pre>
</div>

</div> <!-- end type HMError -->
<!-- start type HMServiceType --> <div>
<h3>Type Changed: HomeKit.HMServiceType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AirPurifier = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">FilterMaintenance = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">HeaterCooler = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">HumidifierDehumidifier = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">Slats = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">VentilationFan = 34,</span>
</pre>
</div>

</div> <!-- end type HMServiceType -->
<div> <!-- start type HMAccessoryCategoryTypeExtensions -->
<h3>New Type HomeKit.HMAccessoryCategoryTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMAccessoryCategoryTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMAccessoryCategoryType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMAccessoryCategoryType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMAccessoryCategoryTypeExtensions -->
<div> <!-- start type HMCharacteristicTypeExtensions -->
<h3>New Type HomeKit.HMCharacteristicTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMCharacteristicTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMCharacteristicType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCharacteristicType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMCharacteristicTypeExtensions -->
<div> <!-- start type HMCharacteristicValueActivationState -->
<h3>New Type HomeKit.HMCharacteristicValueActivationState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueActivationState {
	<span class='added added-field ' data-is-non-breaking="">Active = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueActivationState -->
<div> <!-- start type HMCharacteristicValueCurrentAirPurifierState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentAirPurifierState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentAirPurifierState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Idle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentAirPurifierState -->
<div> <!-- start type HMCharacteristicValueCurrentFanState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentFanState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentFanState {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Idle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentFanState -->
<div> <!-- start type HMCharacteristicValueCurrentHeaterCoolerState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentHeaterCoolerState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentHeaterCoolerState {
	<span class='added added-field ' data-is-non-breaking="">Cooling = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Heating = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Idle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentHeaterCoolerState -->
<div> <!-- start type HMCharacteristicValueCurrentHumidifierDehumidifierState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentHumidifierDehumidifierState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentHumidifierDehumidifierState {
	<span class='added added-field ' data-is-non-breaking="">Dehumidifying = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Humidifying = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Idle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentHumidifierDehumidifierState -->
<div> <!-- start type HMCharacteristicValueCurrentSlatState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentSlatState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentSlatState {
	<span class='added added-field ' data-is-non-breaking="">Jammed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Oscillating = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stationary = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentSlatState -->
<div> <!-- start type HMCharacteristicValueFilterChange -->
<h3>New Type HomeKit.HMCharacteristicValueFilterChange</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueFilterChange {
	<span class='added added-field ' data-is-non-breaking="">Needed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotNeeded = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueFilterChange -->
<div> <!-- start type HMCharacteristicValueLockPhysicalControlsState -->
<h3>New Type HomeKit.HMCharacteristicValueLockPhysicalControlsState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueLockPhysicalControlsState {
	<span class='added added-field ' data-is-non-breaking="">Locked = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotLocked = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueLockPhysicalControlsState -->
<div> <!-- start type HMCharacteristicValueSlatType -->
<h3>New Type HomeKit.HMCharacteristicValueSlatType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueSlatType {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueSlatType -->
<div> <!-- start type HMCharacteristicValueSwingMode -->
<h3>New Type HomeKit.HMCharacteristicValueSwingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueSwingMode {
	<span class='added added-field ' data-is-non-breaking="">Disabled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Enabled = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueSwingMode -->
<div> <!-- start type HMCharacteristicValueTargetAirPurifierState -->
<h3>New Type HomeKit.HMCharacteristicValueTargetAirPurifierState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTargetAirPurifierState {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Manual = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTargetAirPurifierState -->
<div> <!-- start type HMCharacteristicValueTargetFanState -->
<h3>New Type HomeKit.HMCharacteristicValueTargetFanState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTargetFanState {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Manual = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTargetFanState -->
<div> <!-- start type HMCharacteristicValueTargetHeaterCoolerState -->
<h3>New Type HomeKit.HMCharacteristicValueTargetHeaterCoolerState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTargetHeaterCoolerState {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Cool = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Heat = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTargetHeaterCoolerState -->
<div> <!-- start type HMCharacteristicValueTargetHumidifierDehumidifierState -->
<h3>New Type HomeKit.HMCharacteristicValueTargetHumidifierDehumidifierState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTargetHumidifierDehumidifierState {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Dehumidify = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Humidify = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTargetHumidifierDehumidifierState -->
<div> <!-- start type HMServiceTypeExtensions -->
<h3>New Type HomeKit.HMServiceTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMServiceTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMServiceType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMServiceType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMServiceTypeExtensions -->

</div> <!-- end namespace HomeKit -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLMaterial --> <div>
<h3>Type Changed: ModelIO.MDLMaterial</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLMaterialProperty[] GetProperties (MDLMaterialSemantic semantic);</span>
</pre>
</div>

</div> <!-- end type MDLMaterial -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual IMDLMeshBuffer[] VertexBuffers { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCapsule (float height, OpenTK.Vector2 radii, uint radialSegments, uint verticalSegments, uint hemisphereSegments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateIcosahedron (float radius, bool inwardNormals, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLNoiseTexture --> <div>
<h3>Type Changed: ModelIO.MDLNoiseTexture</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public MDLNoiseTexture (float <span class='removed removed-inline '>smoothness</span> <span class='added '>input</span>, string name, OpenTK.Vector2i textureDimensions, MDLTextureChannelEncoding channelEncoding)
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
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateChildObjects (ObjCRuntime.Class objectClass, MDLObject root, MDLObjectHandler handler, ref bool stop);</span>
</pre>
</div>

</div> <!-- end type MDLObject -->
<!-- start type MDLSubmesh --> <div>
<h3>Type Changed: ModelIO.MDLSubmesh</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual MDLSubmeshTopology Topology { get; <span class='added '>set;</span> }
</div></pre>

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
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MDLObject mdlObject, ref bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (MDLObject mdlObject, ref bool stop);</span>
}
</pre>
</div> <!-- end type MDLObjectHandler -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.0"</span> <span class='added '>"10.1"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.2.1"</span> <span class='added '>"10.3.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumDepthEffect = 212,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->
<!-- start type PHAssetMediaSubtype --> <div>
<h3>Type Changed: Photos.PHAssetMediaSubtype</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PhotoDepthEffect = 16,</span>
</pre>
</div>

</div> <!-- end type PHAssetMediaSubtype -->

</div> <!-- end namespace Photos -->
<!-- start namespace ReplayKit --> <div> 
<h2>Namespace ReplayKit</h2>
<!-- start type RPBroadcastSampleHandler --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastSampleHandler</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishBroadcast (Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type RPBroadcastSampleHandler -->

</div> <!-- end namespace ReplayKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslSessionConfig --> <div>
<h3>Type Changed: Security.SslSessionConfig</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ThreeDesFallback = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Tls1ThreeDesFallback = 11,</span>
</pre>
</div>

</div> <!-- end type SslSessionConfig -->

</div> <!-- end namespace Security -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIScreenOverscanCompensation --> <div>
<h3>Type Changed: UIKit.UIScreenOverscanCompensation</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use UIScreenOverscanCompensation.None instead")]
	InsetApplicationFrame = 2,</span>
</div></pre>

</div> <!-- end type UIScreenOverscanCompensation -->

</div> <!-- end namespace UIKit -->
<!-- start namespace VideoSubscriberAccount --> <div> 
<h2>Namespace VideoSubscriberAccount</h2>
<!-- start type VSAccountMetadata --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountMetadata</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual VSAccountProviderResponse AccountProviderResponse { get; }</span>
</pre>
</div>

</div> <!-- end type VSAccountMetadata -->
<!-- start type VSAccountMetadataRequest --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountMetadataRequest</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public VSAccountProviderAuthenticationScheme[] SupportedAuthenticationSchemes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString[] SupportedAuthenticationSchemesString { get; set; }</span>
</pre>
</div>

</div> <!-- end type VSAccountMetadataRequest -->
<!-- start type VSErrorInfo --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSErrorInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string AccountProviderResponse { get; }</span>
</pre>
</div>

</div> <!-- end type VSErrorInfo -->
<div> <!-- start type VSAccountProviderAuthenticationScheme -->
<h3>New Type VideoSubscriberAccount.VSAccountProviderAuthenticationScheme</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VSAccountProviderAuthenticationScheme {
	<span class='added added-field ' data-is-non-breaking="">Saml = 0,</span>
}
</pre>
</div> <!-- end type VSAccountProviderAuthenticationScheme -->
<div> <!-- start type VSAccountProviderAuthenticationSchemeExtensions -->
<h3>New Type VideoSubscriberAccount.VSAccountProviderAuthenticationSchemeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VSAccountProviderAuthenticationSchemeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VSAccountProviderAuthenticationScheme self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (VSAccountProviderAuthenticationScheme[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VSAccountProviderAuthenticationScheme GetValue (Foundation.NSString constant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VSAccountProviderAuthenticationScheme[] GetValues (Foundation.NSString[] constants);</span>
}
</pre>
</div> <!-- end type VSAccountProviderAuthenticationSchemeExtensions -->
<div> <!-- start type VSAccountProviderResponse -->
<h3>New Type VideoSubscriberAccount.VSAccountProviderResponse</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountProviderResponse : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountProviderResponse ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountProviderResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountProviderResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public VSAccountProviderAuthenticationScheme AuthenticationScheme { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString AuthenticationSchemeString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Body { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Status { get; }</span>
}
</pre>
</div> <!-- end type VSAccountProviderResponse -->

</div> <!-- end namespace VideoSubscriberAccount -->
</div>



   


 <hr>
