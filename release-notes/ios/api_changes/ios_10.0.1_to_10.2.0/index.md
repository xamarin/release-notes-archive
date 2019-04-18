---
id: D48A8A59-7F1A-4D60-B36F-4EF67567DCCB
title: "iOS 10.0.1 to 10.2.0"
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
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
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

</div> <!-- end namespace HomeKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPErrorCode --> <div>
<h3>Type Changed: MediaPlayer.MPErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 6,</span>
</pre>
</div>

</div> <!-- end type MPErrorCode -->
<!-- start type MPMusicPlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareToPlay (System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PrepareToPlayAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetQueue (MPMusicPlayerQueueDescriptor descriptor);</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerController -->
<div> <!-- start type MPMusicPlayerMediaItemQueueDescriptor -->
<h3>New Type MediaPlayer.MPMusicPlayerMediaItemQueueDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerMediaItemQueueDescriptor : MediaPlayer.MPMusicPlayerQueueDescriptor, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerMediaItemQueueDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerMediaItemQueueDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerMediaItemQueueDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerMediaItemQueueDescriptor (MPMediaItemCollection itemCollection);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerMediaItemQueueDescriptor (MPMediaQuery query);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerMediaItemQueueDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMediaItemCollection ItemCollection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMediaQuery Query { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMediaItem StartItem { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetEndTime (double endTime, MPMediaItem mediaItem);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetStartTime (double startTime, MPMediaItem mediaItem);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerMediaItemQueueDescriptor -->
<div> <!-- start type MPMusicPlayerQueueDescriptor -->
<h3>New Type MediaPlayer.MPMusicPlayerQueueDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerQueueDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerQueueDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerQueueDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerQueueDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerQueueDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerQueueDescriptor -->
<div> <!-- start type MPMusicPlayerStoreQueueDescriptor -->
<h3>New Type MediaPlayer.MPMusicPlayerStoreQueueDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerStoreQueueDescriptor : MediaPlayer.MPMusicPlayerQueueDescriptor, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerStoreQueueDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerStoreQueueDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerStoreQueueDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerStoreQueueDescriptor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerStoreQueueDescriptor (string[] storeIDs);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StartItemID { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] StoreIDs { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetEndTime (double endTime, string storeID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetStartTime (double startTime, string storeID);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerStoreQueueDescriptor -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.0"</span> <span class='added '>"10.1"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.0.0"</span> <span class='added '>"10.2.0"</span>;
</div></pre>

</div> <!-- end type Constants -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKAddPaymentPassRequestConfiguration --> <div>
<h3>Type Changed: PassKit.PKAddPaymentPassRequestConfiguration</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PKLabeledValue[] CardDetails { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RequiresFelicaSecureElement { get; set; }</span>
</pre>
</div>

</div> <!-- end type PKAddPaymentPassRequestConfiguration -->
<!-- start type PKPassLibrary --> <div>
<h3>Type Changed: PassKit.PKPassLibrary</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanAddFelicaPass { get; }</span>
</pre>
</div>

</div> <!-- end type PKPassLibrary -->
<!-- start type PKPaymentNetwork --> <div>
<h3>Type Changed: PassKit.PKPaymentNetwork</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Jcb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Suica { get; }</span>
</pre>
</div>

</div> <!-- end type PKPaymentNetwork -->
<div> <!-- start type PKLabeledValue -->
<h3>New Type PassKit.PKLabeledValue</h3>
<pre class='added' data-is-non-breaking="">
public class PKLabeledValue : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKLabeledValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKLabeledValue (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKLabeledValue (string label, string value);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Value { get; }</span>
}
</pre>
</div> <!-- end type PKLabeledValue -->
<div> <!-- start type PKSuicaPassProperties -->
<h3>New Type PassKit.PKSuicaPassProperties</h3>
<pre class='added' data-is-non-breaking="">
public class PKSuicaPassProperties : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PKSuicaPassProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKSuicaPassProperties (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKSuicaPassProperties (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Blacklisted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool GreenCarTicketUsed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InShinkansenStation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InStation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber TransitBalance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransitBalanceCurrencyCode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PKSuicaPassProperties GetPassProperties (PKPass pass);</span>
}
</pre>
</div> <!-- end type PKSuicaPassProperties -->

</div> <!-- end namespace PassKit -->
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
<div> <!-- start type ISKCloudServiceSetupViewControllerDelegate -->
<h3>New Type StoreKit.ISKCloudServiceSetupViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISKCloudServiceSetupViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISKCloudServiceSetupViewControllerDelegate -->
<div> <!-- start type SKCloudServiceSetupAction -->
<h3>New Type StoreKit.SKCloudServiceSetupAction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKCloudServiceSetupAction {
	<span class='added added-field ' data-is-non-breaking="">Subscribe = 0,</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupAction -->
<div> <!-- start type SKCloudServiceSetupActionExtensions -->
<h3>New Type StoreKit.SKCloudServiceSetupActionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKCloudServiceSetupActionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SKCloudServiceSetupAction self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKCloudServiceSetupAction GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupActionExtensions -->
<div> <!-- start type SKCloudServiceSetupOptions -->
<h3>New Type StoreKit.SKCloudServiceSetupOptions</h3>
<pre class='added' data-is-non-breaking="">
public class SKCloudServiceSetupOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKCloudServiceSetupOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKCloudServiceSetupOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public SKCloudServiceSetupAction? Action { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? ITunesItemIdentifier { get; set; }</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupOptions -->
<div> <!-- start type SKCloudServiceSetupViewController -->
<h3>New Type StoreKit.SKCloudServiceSetupViewController</h3>
<pre class='added' data-is-non-breaking="">
public class SKCloudServiceSetupViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKCloudServiceSetupViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKCloudServiceSetupViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKCloudServiceSetupViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKCloudServiceSetupViewController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISKCloudServiceSetupViewControllerDelegate Delegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Load (Foundation.NSDictionary options, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Load (SKCloudServiceSetupOptions options, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; LoadAsync (Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; LoadAsync (SKCloudServiceSetupOptions options);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupViewController -->
<div> <!-- start type SKCloudServiceSetupViewControllerDelegate -->
<h3>New Type StoreKit.SKCloudServiceSetupViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SKCloudServiceSetupViewControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISKCloudServiceSetupViewControllerDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKCloudServiceSetupViewControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKCloudServiceSetupViewControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKCloudServiceSetupViewControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDismiss (SKCloudServiceSetupViewController cloudServiceSetupViewController);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupViewControllerDelegate -->
<div> <!-- start type SKCloudServiceSetupViewControllerDelegate_Extensions -->
<h3>New Type StoreKit.SKCloudServiceSetupViewControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKCloudServiceSetupViewControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidDismiss (ISKCloudServiceSetupViewControllerDelegate This, SKCloudServiceSetupViewController cloudServiceSetupViewController);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupViewControllerDelegate_Extensions -->

</div> <!-- end namespace StoreKit -->
</div>



   


 <hr>
