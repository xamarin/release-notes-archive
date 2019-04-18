---
id: 8E4C6EDD-EC2E-449C-99D9-C4FB870332F0
title: "watchOS 11.4.0 11.6.1"
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
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactFormatter --> <div>
<h3>Type Changed: Contacts.CNContactFormatter</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CNContactFormatter -->

</div> <!-- end namespace Contacts -->
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

</div> <!-- end namespace CoreML -->
<!-- start namespace HealthKit --> <div> 
<h2>Namespace HealthKit</h2>
<!-- start type HKMetadata --> <div>
<h3>Type Changed: HealthKit.HKMetadata</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public HKQuantity AlpineSlopeGrade { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKQuantity AverageSpeed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKQuantity ElevationAscended { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKQuantity ElevationDescended { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HKQuantity MaximumSpeed { get; set; }</span>
</pre>
</div>

</div> <!-- end type HKMetadata -->
<!-- start type HKMetadataKey --> <div>
<h3>Type Changed: HealthKit.HKMetadataKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlpineSlopeGrade { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AverageSpeed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ElevationAscended { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ElevationDescended { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaximumSpeed { get; }</span>
</pre>
</div>

</div> <!-- end type HKMetadataKey -->
<!-- start type HKQuantityTypeIdentifierKey --> <div>
<h3>Type Changed: HealthKit.HKQuantityTypeIdentifierKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DistanceDownhillSnowSports { get; }</span>
</pre>
</div>

</div> <!-- end type HKQuantityTypeIdentifierKey -->

</div> <!-- end namespace HealthKit -->
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
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INSearchForNotebookItemsIntent --> <div>
<h3>Type Changed: Intents.INSearchForNotebookItemsIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntent (INSpeakableString title, string content, INNotebookItemType itemType, INTaskStatus status, CoreLocation.CLPlacemark location, INLocationSearchType locationSearchType, INDateComponentsRange dateTime, INDateSearchType dateSearchType, string notebookItemIdentifier);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string NotebookItemIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type INSearchForNotebookItemsIntent -->

</div> <!-- end namespace Intents -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"4.1"</span> <span class='added '>"4.2"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"11.4.0"</span> <span class='added '>"11.6.1"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKPaymentNetwork --> <div>
<h3>Type Changed: PassKit.PKPaymentNetwork</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CartesBancaires { get; }</span>
</pre>
</div>

</div> <!-- end type PKPaymentNetwork -->

</div> <!-- end namespace PassKit -->
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
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKExtension --> <div>
<h3>Type Changed: WatchKit.WKExtension</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Autorotated { get; }</span>
</pre>
</div>

</div> <!-- end type WKExtension -->

</div> <!-- end namespace WatchKit -->
</div>



   


 <hr>
