---
id: D3A087AC-56F4-4D8C-AAB9-842ECB58F0D4
title: "watchOS 10.2.1 to 10.3.0"
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
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.2.1"</span> <span class='added '>"10.3.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKPassLibrary --> <div>
<h3>Type Changed: PassKit.PKPassLibrary</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanAddFelicaPass { get; }</span>
</pre>
</div>

</div> <!-- end type PKPassLibrary -->

</div> <!-- end namespace PassKit -->
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
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKInterfaceController --> <div>
<h3>Type Changed: WatchKit.WKInterfaceController</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void HandleAction (string identifier, UserNotifications.UNNotification notification);</span>
</pre>

</div> <!-- end type WKInterfaceController -->

</div> <!-- end namespace WatchKit -->
</div>



   


 <hr>
