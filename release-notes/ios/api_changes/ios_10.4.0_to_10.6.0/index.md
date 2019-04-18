---
id: EDAC53CF-868F-49BF-97E8-EE77A910864E
title: "iOS 10.4.0 to 10.6.0"
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
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAssetDownloadOptions --> <div>
<h3>Type Changed: AVFoundation.AVAssetDownloadOptions</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public AVMediaSelection MediaSelection { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public Foundation.NSNumber MinimumRequiredMediaBitrate { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type AVAssetDownloadOptions -->
<!-- start type AVAssetExportSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetExportSession</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAssetExportSession (AVAsset asset, AVAssetExportSessionPreset preset);</span>
</pre>
</div>

</div> <!-- end type AVAssetExportSession -->
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
<!-- start type AVCaptureVideoPreviewLayer --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoPreviewLayer</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVCaptureVideoPreviewLayer (AVCaptureSession session, AVCaptureVideoPreviewLayer.InitMode mode);</span>
</pre>
</div>

</div> <!-- end type AVCaptureVideoPreviewLayer -->
<!-- start type AVPlayerItemAccessLogEvent --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItemAccessLogEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double IndicatedAverageBitrate { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerItemAccessLogEvent -->
<!-- start type AVUrlAsset --> <div>
<h3>Type Changed: AVFoundation.AVUrlAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MayRequireContentKeysForMediaDataProcessing { get; }</span>
</pre>
</div>

</div> <!-- end type AVUrlAsset -->
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
<div> <!-- start type AVContentKeyRequest -->
<h3>New Type AVFoundation.AVContentKeyRequest</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeyRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanProvidePersistableContentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData InitializationData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProtocolVersions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVContentKeyRequestStatus Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void MakeStreamingContentKeyRequestData (Foundation.NSData appIdentifier, Foundation.NSData contentIdentifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; MakeStreamingContentKeyRequestDataAsync (Foundation.NSData appIdentifier, Foundation.NSData contentIdentifier, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Process (AVContentKeyResponse keyResponse);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Process (Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RespondByRequestingPersistableContentKeyRequest ();</span>
}
</pre>
</div> <!-- end type AVContentKeyRequest -->
<div> <!-- start type AVContentKeyRequestRetryReason -->
<h3>New Type AVFoundation.AVContentKeyRequestRetryReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeyRequestRetryReason {
	<span class='added added-field ' data-is-non-breaking="">ReceivedObsoleteContentKey = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReceivedResponseWithExpiredLease = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedOut = 0,</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestRetryReason -->
<div> <!-- start type AVContentKeyRequestRetryReasonExtensions -->
<h3>New Type AVFoundation.AVContentKeyRequestRetryReasonExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeyRequestRetryReasonExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVContentKeyRequestRetryReason self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeyRequestRetryReason GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestRetryReasonExtensions -->
<div> <!-- start type AVContentKeyRequestStatus -->
<h3>New Type AVFoundation.AVContentKeyRequestStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeyRequestStatus {
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Renewed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Requesting = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Retried = 3,</span>
}
</pre>
</div> <!-- end type AVContentKeyRequestStatus -->
<div> <!-- start type AVContentKeyRequest_AVContentKeyRequestRenewal -->
<h3>New Type AVFoundation.AVContentKeyRequest_AVContentKeyRequestRenewal</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeyRequest_AVContentKeyRequestRenewal {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool GetRenewsExpiringResponseData (AVContentKeyRequest This);</span>
}
</pre>
</div> <!-- end type AVContentKeyRequest_AVContentKeyRequestRenewal -->
<div> <!-- start type AVContentKeyResponse -->
<h3>New Type AVFoundation.AVContentKeyResponse</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeyResponse : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeyResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeyResponse Create (Foundation.NSData fairPlayStreamingKeyResponseData);</span>
}
</pre>
</div> <!-- end type AVContentKeyResponse -->
<div> <!-- start type AVContentKeySession -->
<h3>New Type AVFoundation.AVContentKeySession</h3>
<pre class='added' data-is-non-breaking="">
public class AVContentKeySession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData ContentProtectionSessionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVContentKeySessionDelegate Delegate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreFoundation.DispatchQueue DelegateQueue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVContentKeySystem KeySystem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString KeySystemConstant { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl StorageUrl { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySession Create (AVContentKeySystem keySystem, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySession Create (Foundation.NSString keySystem, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Expire ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary[] GetPendingExpiredSessionReports (Foundation.NSData appIdentifier, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ProcessContentKeyRequest (Foundation.NSObject identifier, Foundation.NSData initializationData, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemovePendingExpiredSessionReports (Foundation.NSDictionary[] expiredSessionReports, Foundation.NSData appIdentifier, Foundation.NSUrl storageUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RenewExpiringResponseData (AVContentKeyRequest contentKeyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDelegate (IAVContentKeySessionDelegate newDelegate, CoreFoundation.DispatchQueue delegateQueue);</span>
}
</pre>
</div> <!-- end type AVContentKeySession -->
<div> <!-- start type AVContentKeySessionDelegate -->
<h3>New Type AVFoundation.AVContentKeySessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class AVContentKeySessionDelegate : Foundation.NSObject, IAVContentKeySessionDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVContentKeySessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChange (AVContentKeySession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFail (AVContentKeySession session, AVContentKeyRequest keyRequest, Foundation.NSError err);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvidePersistableContentKeyRequest (AVContentKeySession session, AVPersistableContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideRenewingContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRetryContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest, string retryReason);</span>
}
</pre>
</div> <!-- end type AVContentKeySessionDelegate -->
<div> <!-- start type AVContentKeySessionDelegate_Extensions -->
<h3>New Type AVFoundation.AVContentKeySessionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySessionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidChange (IAVContentKeySessionDelegate This, AVContentKeySession session);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFail (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest, Foundation.NSError err);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidProvidePersistableContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVPersistableContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidProvideRenewingContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldRetryContentKeyRequest (IAVContentKeySessionDelegate This, AVContentKeySession session, AVContentKeyRequest keyRequest, string retryReason);</span>
}
</pre>
</div> <!-- end type AVContentKeySessionDelegate_Extensions -->
<div> <!-- start type AVContentKeySession_AVContentKeyRecipients -->
<h3>New Type AVFoundation.AVContentKeySession_AVContentKeyRecipients</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySession_AVContentKeyRecipients {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Add (AVContentKeySession This, IAVContentKeyRecipient recipient);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IAVContentKeyRecipient[] GetContentKeyRecipients (AVContentKeySession This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Remove (AVContentKeySession This, IAVContentKeyRecipient recipient);</span>
}
</pre>
</div> <!-- end type AVContentKeySession_AVContentKeyRecipients -->
<div> <!-- start type AVContentKeySystem -->
<h3>New Type AVFoundation.AVContentKeySystem</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVContentKeySystem {
	<span class='added added-field ' data-is-non-breaking="">FairPlayStreaming = 0,</span>
}
</pre>
</div> <!-- end type AVContentKeySystem -->
<div> <!-- start type AVContentKeySystemExtensions -->
<h3>New Type AVFoundation.AVContentKeySystemExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVContentKeySystemExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVContentKeySystem self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVContentKeySystem GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVContentKeySystemExtensions -->
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
<div> <!-- start type AVPersistableContentKeyRequest -->
<h3>New Type AVFoundation.AVPersistableContentKeyRequest</h3>
<pre class='added' data-is-non-breaking="">
public class AVPersistableContentKeyRequest : AVFoundation.AVContentKeyRequest, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPersistableContentKeyRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVPersistableContentKeyRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData GetPersistableContentKey (Foundation.NSData keyVendorResponse, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, Foundation.NSError outError);</span>
}
</pre>
</div> <!-- end type AVPersistableContentKeyRequest -->
<div> <!-- start type IAVContentKeyRecipient -->
<h3>New Type AVFoundation.IAVContentKeyRecipient</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVContentKeyRecipient : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MayRequireContentKeysForMediaDataProcessing { get; }</span>
}
</pre>
</div> <!-- end type IAVContentKeyRecipient -->
<div> <!-- start type IAVContentKeySessionDelegate -->
<h3>New Type AVFoundation.IAVContentKeySessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVContentKeySessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidProvideContentKeyRequest (AVContentKeySession session, AVContentKeyRequest keyRequest);</span>
}
</pre>
</div> <!-- end type IAVContentKeySessionDelegate -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace CallKit --> <div> 
<h2>Namespace CallKit</h2>
<!-- start type CXErrorCodeCallDirectoryManagerError --> <div>
<h3>Type Changed: CallKit.CXErrorCodeCallDirectoryManagerError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CurrentlyLoading = 7,</span>
</pre>
</div>

</div> <!-- end type CXErrorCodeCallDirectoryManagerError -->

</div> <!-- end namespace CallKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNMutablePostalAddress --> <div>
<h3>Type Changed: Contacts.CNMutablePostalAddress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubAdministrativeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubLocality { get; set; }</span>
</pre>
</div>

</div> <!-- end type CNMutablePostalAddress -->
<!-- start type CNPostalAddress --> <div>
<h3>Type Changed: Contacts.CNPostalAddress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubAdministrativeArea { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SubLocality { get; }</span>
</pre>
</div>

</div> <!-- end type CNPostalAddress -->
<!-- start type CNPostalAddressKey --> <div>
<h3>Type Changed: Contacts.CNPostalAddressKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SubAdministrativeArea { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SubLocality { get; }</span>
</pre>
</div>

</div> <!-- end type CNPostalAddressKey -->

</div> <!-- end namespace Contacts -->
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
<!-- start type CADisplayLink --> <div>
<h3>Type Changed: CoreAnimation.CADisplayLink</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveFromRunLoop (Foundation.NSRunLoop runloop, Foundation.NSRunLoopMode mode);</span>
</pre>
</div>

</div> <!-- end type CADisplayLink -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreFoundation --> <div> 
<h2>Namespace CoreFoundation</h2>
<!-- start type CFNetworkErrors --> <div>
<h3>Type Changed: CoreFoundation.CFNetworkErrors</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FileOutsideSafeArea = -1104,</span>
</pre>
</div>

</div> <!-- end type CFNetworkErrors -->

</div> <!-- end namespace CoreFoundation -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImage --> <div>
<h3>Type Changed: CoreImage.CIImage</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGColorSpace ColorSpace { get; }</span>
</pre>
</div>

</div> <!-- end type CIImage -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVPixelFormatType --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Argb2101010LEPacked = 1815162994,</span>
</pre>
</div>

</div> <!-- end type CVPixelFormatType -->
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
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSCalendar --> <div>
<h3>Type Changed: Foundation.NSCalendar</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a NSCalendarOptions parameter")]
	public NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a NSCalendarOptions parameter")]
	public NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);</span>
</div></pre>

</div> <!-- end type NSCalendar -->
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
<!-- start type NSMetadataItem --> <div>
<h3>Type Changed: Foundation.NSMetadataItem</h3>
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
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void Perform (NSRunLoopMode[] modes, System.Action block);</span>
</pre>
</div>

</div> <!-- end type NSRunLoop -->
<!-- start type NSStream --> <div>
<h3>Type Changed: Foundation.NSStream</h3>
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
<!-- start type NSUrlError --> <div>
<h3>Type Changed: Foundation.NSUrlError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FileOutsideSafeArea = -1104,</span>
</pre>
</div>

</div> <!-- end type NSUrlError -->
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

</div> <!-- end namespace Foundation -->
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LabelIndex = 114,</span>
	<span class='added added-field ' data-is-non-breaking="">LabelNamespace = 113,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMCharacteristicValueContactState --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicValueContactState</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	Detected = <span class='removed removed-inline removed-breaking-inline'>1</span> <span class='added '>0</span>
</div><div data-is-breaking="">	None = <span class='removed removed-inline removed-breaking-inline'>0</span> <span class='added '>1</span>
</div></pre>

</div> <!-- end type HMCharacteristicValueContactState -->
<!-- start type HMServiceType --> <div>
<h3>Type Changed: HomeKit.HMServiceType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Label = 39,</span>
</pre>
</div>

</div> <!-- end type HMServiceType -->
<div> <!-- start type HMCharacteristicValueInputEvent -->
<h3>New Type HomeKit.HMCharacteristicValueInputEvent</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueInputEvent {
	<span class='added added-field ' data-is-non-breaking="">DoublePress = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">LongPress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SinglePress = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueInputEvent -->
<div> <!-- start type HMCharacteristicValueLabelNamespace -->
<h3>New Type HomeKit.HMCharacteristicValueLabelNamespace</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueLabelNamespace {
	<span class='added added-field ' data-is-non-breaking="">Dot = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Numeral = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueLabelNamespace -->

</div> <!-- end namespace HomeKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExifSubsecTimeOriginal { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type IINPaymentsDomainHandling --> <div>
<h3>Type Changed: Intents.IINPaymentsDomainHandling</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface breaking' data-is-breaking="">IINPayBillIntentHandling</span>
	<span class='added added-interface breaking' data-is-breaking="">IINSearchForBillsIntentHandling</span>
</pre>
</div>

</div> <!-- end type IINPaymentsDomainHandling -->
<!-- start type INCarDefroster --> <div>
<h3>Type Changed: Intents.INCarDefroster</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">All = 3,</span>
</pre>
</div>

</div> <!-- end type INCarDefroster -->
<!-- start type INCarSeat --> <div>
<h3>Type Changed: Intents.INCarSeat</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">All = 12,</span>
</pre>
</div>

</div> <!-- end type INCarSeat -->
<!-- start type INIntentErrorCode --> <div>
<h3>Type Changed: Intents.INIntentErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExtensionBringUpFailed = 5001,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtensionLaunchingTimeout = 5000,</span>
</pre>
</div>

</div> <!-- end type INIntentErrorCode -->
<!-- start type INPaymentStatus --> <div>
<h3>Type Changed: Intents.INPaymentStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Unpaid = 5,</span>
</pre>
</div>

</div> <!-- end type INPaymentStatus -->
<!-- start type INPerson --> <div>
<h3>Type Changed: Intents.INPerson</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] SiriMatches { get; }</span>
</pre>
</div>

</div> <!-- end type INPerson -->
<!-- start type INPreferences --> <div>
<h3>Type Changed: Intents.INPreferences</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public INPreferences ();</span>
</pre>

</div> <!-- end type INPreferences -->
<!-- start type INRequestRideIntent --> <div>
<h3>Type Changed: Intents.INRequestRideIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntent (CoreLocation.CLPlacemark pickupLocation, CoreLocation.CLPlacemark dropOffLocation, INSpeakableString rideOptionName, Foundation.NSNumber partySize, INPaymentMethod paymentMethod, INDateComponentsRange scheduledPickupTime);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange ScheduledPickupTime { get; }</span>
</pre>
</div>

</div> <!-- end type INRequestRideIntent -->
<!-- start type INRequestRideIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INRequestRideIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveScheduledPickupTime (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INRequestRideIntentHandling_Extensions -->
<!-- start type INRideStatus --> <div>
<h3>Type Changed: Intents.INRideStatus</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange ScheduledPickupTime { get; set; }</span>
</pre>
</div>

</div> <!-- end type INRideStatus -->
<!-- start type INVocabularyStringType --> <div>
<h3>Type Changed: Intents.INVocabularyStringType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CarName = 301,</span>
	<span class='added added-field ' data-is-non-breaking="">PaymentsAccountNickname = 401,</span>
	<span class='added added-field ' data-is-non-breaking="">PaymentsOrganizationName = 400,</span>
</pre>
</div>

</div> <!-- end type INVocabularyStringType -->
<div> <!-- start type IINActivateCarSignalIntentHandling -->
<h3>New Type Intents.IINActivateCarSignalIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINActivateCarSignalIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleActivateCarSignal (INActivateCarSignalIntent intent, System.Action&lt;INActivateCarSignalIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINActivateCarSignalIntentHandling -->
<div> <!-- start type IINCarCommandsDomainHandling -->
<h3>New Type Intents.IINCarCommandsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCarCommandsDomainHandling : IINActivateCarSignalIntentHandling, IINGetCarLockStatusIntentHandling, IINGetCarPowerLevelStatusIntentHandling, IINSetCarLockStatusIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINCarCommandsDomainHandling -->
<div> <!-- start type IINGetCarLockStatusIntentHandling -->
<h3>New Type Intents.IINGetCarLockStatusIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINGetCarLockStatusIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleGetCarLockStatus (INGetCarLockStatusIntent intent, System.Action&lt;INGetCarLockStatusIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINGetCarLockStatusIntentHandling -->
<div> <!-- start type IINGetCarPowerLevelStatusIntentHandling -->
<h3>New Type Intents.IINGetCarPowerLevelStatusIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINGetCarPowerLevelStatusIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleGetCarPowerLevelStatus (INGetCarPowerLevelStatusIntent intent, System.Action&lt;INGetCarPowerLevelStatusIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINGetCarPowerLevelStatusIntentHandling -->
<div> <!-- start type IINPayBillIntentHandling -->
<h3>New Type Intents.IINPayBillIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINPayBillIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINPayBillIntentHandling -->
<div> <!-- start type IINSearchForBillsIntentHandling -->
<h3>New Type Intents.IINSearchForBillsIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForBillsIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINSearchForBillsIntentHandling -->
<div> <!-- start type IINSetCarLockStatusIntentHandling -->
<h3>New Type Intents.IINSetCarLockStatusIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSetCarLockStatusIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSetCarLockStatus (INSetCarLockStatusIntent intent, System.Action&lt;INSetCarLockStatusIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSetCarLockStatusIntentHandling -->
<div> <!-- start type INAccountType -->
<h3>New Type Intents.INAccountType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INAccountType {
	<span class='added added-field ' data-is-non-breaking="">Checking = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Credit = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Debit = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Investment = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Mortgage = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Prepaid = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Saving = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INAccountType -->
<div> <!-- start type INActivateCarSignalIntent -->
<h3>New Type Intents.INActivateCarSignalIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INActivateCarSignalIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INActivateCarSignalIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INActivateCarSignalIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INActivateCarSignalIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INActivateCarSignalIntent (INSpeakableString carName, INCarSignalOptions signals);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString CarName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCarSignalOptions Signals { get; }</span>
}
</pre>
</div> <!-- end type INActivateCarSignalIntent -->
<div> <!-- start type INActivateCarSignalIntentHandling_Extensions -->
<h3>New Type Intents.INActivateCarSignalIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INActivateCarSignalIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmActivateCarSignal (IINActivateCarSignalIntentHandling This, INActivateCarSignalIntent intent, System.Action&lt;INActivateCarSignalIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCarName (IINActivateCarSignalIntentHandling This, INActivateCarSignalIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSignals (IINActivateCarSignalIntentHandling This, INActivateCarSignalIntent intent, System.Action&lt;INCarSignalOptionsResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INActivateCarSignalIntentHandling_Extensions -->
<div> <!-- start type INActivateCarSignalIntentResponse -->
<h3>New Type Intents.INActivateCarSignalIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INActivateCarSignalIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INActivateCarSignalIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INActivateCarSignalIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INActivateCarSignalIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INActivateCarSignalIntentResponse (INActivateCarSignalIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INActivateCarSignalIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCarSignalOptions Signals { get; set; }</span>
}
</pre>
</div> <!-- end type INActivateCarSignalIntentResponse -->
<div> <!-- start type INActivateCarSignalIntentResponseCode -->
<h3>New Type Intents.INActivateCarSignalIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INActivateCarSignalIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INActivateCarSignalIntentResponseCode -->
<div> <!-- start type INAmountType -->
<h3>New Type Intents.INAmountType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INAmountType {
	<span class='added added-field ' data-is-non-breaking="">AmountDue = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentBalance = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">MinimumDue = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INAmountType -->
<div> <!-- start type INBillDetails -->
<h3>New Type Intents.INBillDetails</h3>
<pre class='added' data-is-non-breaking="">
public class INBillDetails : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INBillDetails (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillDetails (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INBillDetails (INBillType billType, INPaymentStatus paymentStatus, INBillPayee billPayee, INCurrencyAmount amountDue, INCurrencyAmount minimumDue, INCurrencyAmount lateFee, Foundation.NSDateComponents dueDate, Foundation.NSDateComponents paymentDate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount AmountDue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillPayee BillPayee { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillType BillType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents DueDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount LateFee { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount MinimumDue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents PaymentDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentStatus PaymentStatus { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INBillDetails -->
<div> <!-- start type INBillPayee -->
<h3>New Type Intents.INBillPayee</h3>
<pre class='added' data-is-non-breaking="">
public class INBillPayee : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INBillPayee (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillPayee (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillPayee (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INBillPayee (INSpeakableString nickname, string accountNumber, INSpeakableString organizationName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccountNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Nickname { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString OrganizationName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INBillPayee -->
<div> <!-- start type INBillPayeeResolutionResult -->
<h3>New Type Intents.INBillPayeeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INBillPayeeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillPayeeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillPayeeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillPayeeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillPayeeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillPayeeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INBillPayeeResolutionResult GetConfirmationRequired (INBillPayee billPayeeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INBillPayeeResolutionResult GetDisambiguation (INBillPayee[] billPayeesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INBillPayeeResolutionResult GetSuccess (INBillPayee resolvedBillPayee);</span>
}
</pre>
</div> <!-- end type INBillPayeeResolutionResult -->
<div> <!-- start type INBillType -->
<h3>New Type Intents.INBillType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INBillType {
	<span class='added added-field ' data-is-non-breaking="">AutoInsurance = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Cable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CarLease = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">CarLoan = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">CreditCard = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Electricity = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">GarbageAndRecycling = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Gas = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HealthInsurance = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeInsurance = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Internet = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">LifeInsurance = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Mortgage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">MusicStreaming = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Phone = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Rent = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Sewer = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">StudentLoan = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">TrafficTicket = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Tuition = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Utilities = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">Water = 22,</span>
}
</pre>
</div> <!-- end type INBillType -->
<div> <!-- start type INBillTypeResolutionResult -->
<h3>New Type Intents.INBillTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INBillTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBillTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBillTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INBillTypeResolutionResult GetConfirmationRequired (INBillType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INBillTypeResolutionResult GetSuccess (INBillType resolvedValue);</span>
}
</pre>
</div> <!-- end type INBillTypeResolutionResult -->
<div> <!-- start type INCarSignalOptions -->
<h3>New Type Intents.INCarSignalOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INCarSignalOptions {
	<span class='added added-field ' data-is-non-breaking="">Audible = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type INCarSignalOptions -->
<div> <!-- start type INCarSignalOptionsResolutionResult -->
<h3>New Type Intents.INCarSignalOptionsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCarSignalOptionsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarSignalOptionsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarSignalOptionsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSignalOptionsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSignalOptionsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSignalOptionsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCarSignalOptionsResolutionResult GetConfirmationRequired (INCarSignalOptions valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCarSignalOptionsResolutionResult GetSuccess (INCarSignalOptions resolvedValue);</span>
}
</pre>
</div> <!-- end type INCarSignalOptionsResolutionResult -->
<div> <!-- start type INGetCarLockStatusIntent -->
<h3>New Type Intents.INGetCarLockStatusIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INGetCarLockStatusIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarLockStatusIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarLockStatusIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarLockStatusIntent (INSpeakableString carName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarLockStatusIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString CarName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type INGetCarLockStatusIntent -->
<div> <!-- start type INGetCarLockStatusIntentHandling_Extensions -->
<h3>New Type Intents.INGetCarLockStatusIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INGetCarLockStatusIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmGetCarLockStatus (IINGetCarLockStatusIntentHandling This, INGetCarLockStatusIntent intent, System.Action&lt;INGetCarLockStatusIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCarName (IINGetCarLockStatusIntentHandling This, INGetCarLockStatusIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INGetCarLockStatusIntentHandling_Extensions -->
<div> <!-- start type INGetCarLockStatusIntentResponse -->
<h3>New Type Intents.INGetCarLockStatusIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INGetCarLockStatusIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarLockStatusIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarLockStatusIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarLockStatusIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarLockStatusIntentResponse (INGetCarLockStatusIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INGetCarLockStatusIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Locked { get; }</span>
}
</pre>
</div> <!-- end type INGetCarLockStatusIntentResponse -->
<div> <!-- start type INGetCarLockStatusIntentResponseCode -->
<h3>New Type Intents.INGetCarLockStatusIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetCarLockStatusIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INGetCarLockStatusIntentResponseCode -->
<div> <!-- start type INGetCarPowerLevelStatusIntent -->
<h3>New Type Intents.INGetCarPowerLevelStatusIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INGetCarPowerLevelStatusIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarPowerLevelStatusIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarPowerLevelStatusIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarPowerLevelStatusIntent (INSpeakableString carName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarPowerLevelStatusIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString CarName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type INGetCarPowerLevelStatusIntent -->
<div> <!-- start type INGetCarPowerLevelStatusIntentHandling_Extensions -->
<h3>New Type Intents.INGetCarPowerLevelStatusIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INGetCarPowerLevelStatusIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmGetCarPowerLevelStatus (IINGetCarPowerLevelStatusIntentHandling This, INGetCarPowerLevelStatusIntent intent, System.Action&lt;INGetCarPowerLevelStatusIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCarName (IINGetCarPowerLevelStatusIntentHandling This, INGetCarPowerLevelStatusIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INGetCarPowerLevelStatusIntentHandling_Extensions -->
<div> <!-- start type INGetCarPowerLevelStatusIntentResponse -->
<h3>New Type Intents.INGetCarPowerLevelStatusIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INGetCarPowerLevelStatusIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarPowerLevelStatusIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarPowerLevelStatusIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetCarPowerLevelStatusIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetCarPowerLevelStatusIntentResponse (INGetCarPowerLevelStatusIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float? ChargePercentRemaining { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INGetCarPowerLevelStatusIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;Foundation.NSUnitLength&gt; DistanceRemaining { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? FuelPercentRemaining { get; }</span>
}
</pre>
</div> <!-- end type INGetCarPowerLevelStatusIntentResponse -->
<div> <!-- start type INGetCarPowerLevelStatusIntentResponseCode -->
<h3>New Type Intents.INGetCarPowerLevelStatusIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetCarPowerLevelStatusIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INGetCarPowerLevelStatusIntentResponseCode -->
<div> <!-- start type INPayBillIntent -->
<h3>New Type Intents.INPayBillIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INPayBillIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPayBillIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPayBillIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPayBillIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPayBillIntent (INBillPayee billPayee, INPaymentAccount fromAccount, INPaymentAmount transactionAmount, INDateComponentsRange transactionScheduledDate, string transactionNote, INBillType billType, INDateComponentsRange dueDate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillPayee BillPayee { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillType BillType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DueDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount FromAccount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAmount TransactionAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionNote { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange TransactionScheduledDate { get; }</span>
}
</pre>
</div> <!-- end type INPayBillIntent -->
<div> <!-- start type INPayBillIntentHandling_Extensions -->
<h3>New Type Intents.INPayBillIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPayBillIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmPayBill (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INPayBillIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void HandlePayBill (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INPayBillIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveBillPayee (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INBillPayeeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveBillType (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INBillTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDueDate (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveFromAccount (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INPaymentAccountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionAmount (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INPaymentAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionNote (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionScheduledDate (IINPayBillIntentHandling This, INPayBillIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INPayBillIntentHandling_Extensions -->
<div> <!-- start type INPayBillIntentResponse -->
<h3>New Type Intents.INPayBillIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INPayBillIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPayBillIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPayBillIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPayBillIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPayBillIntentResponse (INPayBillIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillDetails BillDetails { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPayBillIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount FromAccount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAmount TransactionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange TransactionScheduledDate { get; set; }</span>
}
</pre>
</div> <!-- end type INPayBillIntentResponse -->
<div> <!-- start type INPayBillIntentResponseCode -->
<h3>New Type Intents.INPayBillIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPayBillIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCredentialsUnverified = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureInsufficientFunds = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INPayBillIntentResponseCode -->
<div> <!-- start type INPaymentAccount -->
<h3>New Type Intents.INPaymentAccount</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentAccount : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentAccount (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAccount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAccount (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentAccount (INSpeakableString nickname, string accountNumber, INAccountType accountType, INSpeakableString organizationName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccountNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INAccountType AccountType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Nickname { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString OrganizationName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPaymentAccount -->
<div> <!-- start type INPaymentAccountResolutionResult -->
<h3>New Type Intents.INPaymentAccountResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentAccountResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAccountResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAccountResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAccountResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAccountResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAccountResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAccountResolutionResult GetConfirmationRequired (INPaymentAccount paymentAccountToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAccountResolutionResult GetDisambiguation (INPaymentAccount[] paymentAccountsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAccountResolutionResult GetSuccess (INPaymentAccount resolvedPaymentAccount);</span>
}
</pre>
</div> <!-- end type INPaymentAccountResolutionResult -->
<div> <!-- start type INPaymentAmount -->
<h3>New Type Intents.INPaymentAmount</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentAmount : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentAmount (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAmount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAmount (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentAmount (INAmountType amountType, INCurrencyAmount amount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount Amount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INAmountType AmountType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPaymentAmount -->
<div> <!-- start type INPaymentAmountResolutionResult -->
<h3>New Type Intents.INPaymentAmountResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentAmountResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAmountResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentAmountResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAmountResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAmountResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentAmountResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAmountResolutionResult GetConfirmationRequired (INPaymentAmount paymentAmountToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAmountResolutionResult GetDisambiguation (INPaymentAmount[] paymentAmountsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentAmountResolutionResult GetSuccess (INPaymentAmount resolvedPaymentAmount);</span>
}
</pre>
</div> <!-- end type INPaymentAmountResolutionResult -->
<div> <!-- start type INPaymentStatusResolutionResult -->
<h3>New Type Intents.INPaymentStatusResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentStatusResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentStatusResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentStatusResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentStatusResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentStatusResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentStatusResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentStatusResolutionResult GetConfirmationRequired (INPaymentStatus valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPaymentStatusResolutionResult GetSuccess (INPaymentStatus resolvedValue);</span>
}
</pre>
</div> <!-- end type INPaymentStatusResolutionResult -->
<div> <!-- start type INSearchForBillsIntent -->
<h3>New Type Intents.INSearchForBillsIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForBillsIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForBillsIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForBillsIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForBillsIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForBillsIntent (INBillPayee billPayee, INDateComponentsRange paymentDateRange, INBillType billType, INPaymentStatus status, INDateComponentsRange dueDateRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillPayee BillPayee { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillType BillType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DueDateRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange PaymentDateRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentStatus Status { get; }</span>
}
</pre>
</div> <!-- end type INSearchForBillsIntent -->
<div> <!-- start type INSearchForBillsIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForBillsIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForBillsIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearch (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INSearchForBillsIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void HandleSearch (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INSearchForBillsIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveBillPayee (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INBillPayeeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveBillType (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INBillTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDueDateRange (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePaymentDateRange (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveStatus (IINSearchForBillsIntentHandling This, INSearchForBillsIntent intent, System.Action&lt;INPaymentStatusResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForBillsIntentHandling_Extensions -->
<div> <!-- start type INSearchForBillsIntentResponse -->
<h3>New Type Intents.INSearchForBillsIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForBillsIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForBillsIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForBillsIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForBillsIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForBillsIntentResponse (INSearchForBillsIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INBillDetails[] Bills { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForBillsIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSearchForBillsIntentResponse -->
<div> <!-- start type INSearchForBillsIntentResponseCode -->
<h3>New Type Intents.INSearchForBillsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForBillsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureBillNotFound = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCredentialsUnverified = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForBillsIntentResponseCode -->
<div> <!-- start type INSetCarLockStatusIntent -->
<h3>New Type Intents.INSetCarLockStatusIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSetCarLockStatusIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSetCarLockStatusIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (Foundation.NSNumber locked, INSpeakableString carName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSetCarLockStatusIntent (bool? locked, INSpeakableString carName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString CarName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Locked { get; }</span>
}
</pre>
</div> <!-- end type INSetCarLockStatusIntent -->
<div> <!-- start type INSetCarLockStatusIntentHandling_Extensions -->
<h3>New Type Intents.INSetCarLockStatusIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSetCarLockStatusIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSetCarLockStatus (IINSetCarLockStatusIntentHandling This, INSetCarLockStatusIntent intent, System.Action&lt;INSetCarLockStatusIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCarName (IINSetCarLockStatusIntentHandling This, INSetCarLockStatusIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveLocked (IINSetCarLockStatusIntentHandling This, INSetCarLockStatusIntent intent, System.Action&lt;INBooleanResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSetCarLockStatusIntentHandling_Extensions -->
<div> <!-- start type INSetCarLockStatusIntentResponse -->
<h3>New Type Intents.INSetCarLockStatusIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSetCarLockStatusIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSetCarLockStatusIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSetCarLockStatusIntentResponse (INSetCarLockStatusIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSetCarLockStatusIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSetCarLockStatusIntentResponse -->
<div> <!-- start type INSetCarLockStatusIntentResponseCode -->
<h3>New Type Intents.INSetCarLockStatusIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSetCarLockStatusIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSetCarLockStatusIntentResponseCode -->

</div> <!-- end namespace Intents -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPErrorCode --> <div>
<h3>Type Changed: MediaPlayer.MPErrorCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">RequestTimedOut = 7,</span>
</pre>
</div>

</div> <!-- end type MPErrorCode -->
<!-- start type MPMediaItem --> <div>
<h3>Type Changed: MediaPlayer.MPMediaItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString PlaybackStoreID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackStoreIDProperty { get; }</span>
</pre>
</div>

</div> <!-- end type MPMediaItem -->
<!-- start type MPMusicPlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static MPMusicPlayerApplicationController ApplicationQueuePlayer { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Append (MPMusicPlayerQueueDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Prepend (MPMusicPlayerQueueDescriptor descriptor);</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerController -->
<!-- start type MPNowPlayingInfo --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfo</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl AssetUrl { get; set; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfo -->
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyAssetUrl { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<div> <!-- start type MPMusicPlayerApplicationController -->
<h3>New Type MediaPlayer.MPMusicPlayerApplicationController</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerApplicationController : MediaPlayer.MPMusicPlayerController, Foundation.INSObjectProtocol, IMPMediaPlayback, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerApplicationController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerApplicationController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerApplicationController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (System.Action&lt;MPMusicPlayerControllerMutableQueue&gt; queueTransaction, System.Action&lt;MPMusicPlayerControllerQueue,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MPMusicPlayerControllerQueue&gt; PerformAsync (System.Action&lt;MPMusicPlayerControllerMutableQueue&gt; queueTransaction);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerApplicationController -->
<div> <!-- start type MPMusicPlayerControllerMutableQueue -->
<h3>New Type MediaPlayer.MPMusicPlayerControllerMutableQueue</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerControllerMutableQueue : MediaPlayer.MPMusicPlayerControllerQueue, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMusicPlayerControllerMutableQueue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerControllerMutableQueue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerControllerMutableQueue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertAfter (MPMusicPlayerQueueDescriptor queueDescriptor, MPMediaItem item);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveItem (MPMediaItem item);</span>
}
</pre>
</div> <!-- end type MPMusicPlayerControllerMutableQueue -->
<div> <!-- start type MPMusicPlayerControllerQueue -->
<h3>New Type MediaPlayer.MPMusicPlayerControllerQueue</h3>
<pre class='added' data-is-non-breaking="">
public class MPMusicPlayerControllerQueue : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerControllerQueue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMusicPlayerControllerQueue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidChangeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPMediaItem[] Items { get; }</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type MPMusicPlayerControllerQueue -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLDrawable --> <div>
<h3>Type Changed: Metal.MTLDrawable</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DrawableID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double PresentedTime { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddPresentedHandler (System.Action&lt;IMTLDrawable&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PresentAfter (double duration);</span>
</pre>
</div>

</div> <!-- end type MTLDrawable -->
<div> <!-- start type MTLCommandBuffer_Extensions -->
<h3>New Type Metal.MTLCommandBuffer_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLCommandBuffer_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static double GetGpuEndTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetGpuStartTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetKernelEndTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetKernelStartTime (IMTLCommandBuffer This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PresentDrawableAfter (IMTLCommandBuffer This, IMTLDrawable drawable, double duration);</span>
}
</pre>
</div> <!-- end type MTLCommandBuffer_Extensions -->
<div> <!-- start type MTLDrawable_Extensions -->
<h3>New Type Metal.MTLDrawable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTLDrawable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddPresentedHandler (IMTLDrawable This, System.Action&lt;IMTLDrawable&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetDrawableID (IMTLDrawable This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetPresentedTime (IMTLDrawable This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PresentAfter (IMTLDrawable This, double duration);</span>
}
</pre>
</div> <!-- end type MTLDrawable_Extensions -->

</div> <!-- end namespace Metal -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLComponent[] Components { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMDLComponent GetComponent (ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLLightProbe[] PlaceLightProbes (float density, MDLProbePlacement type, MDLLightProbeIrradianceDataSource dataSource);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetComponent (IMDLComponent component, ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetComponent (IMDLComponent component, System.Type type);</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 vector, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator, MDLMesh.MDLMeshVectorType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateCylinder (OpenTK.Vector3 extent, OpenTK.Vector2i segments, bool inwardNormals, bool topCap, bool bottomCap, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateIcosahedron (OpenTK.Vector3 extent, bool inwardNormals, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreatePlane (OpenTK.Vector3 extent, OpenTK.Vector2i segments, MDLGeometryType geometryType, IMDLMeshBufferAllocator allocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLObject --> <div>
<h3>Type Changed: ModelIO.MDLObject</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMDLComponent[] Components { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use GetComponent (Type type)")]
	public virtual IMDLComponent IsComponentConforming (ObjCRuntime.Protocol protocol);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (ObjCRuntime.Protocol protocol);</span>
	<span class='added added-method ' data-is-non-breaking="">public IMDLComponent GetComponent (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetComponent (IMDLComponent component, System.Type type);</span>
</pre>
</div>

</div> <!-- end type MDLObject -->
<!-- start type MDLObjectContainer --> <div>
<h3>Type Changed: ModelIO.MDLObjectContainer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Count { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MDLObject GetObject (uint index);</span>
</pre>
</div>

</div> <!-- end type MDLObjectContainer -->
<!-- start type MDLTransform --> <div>
<h3>Type Changed: ModelIO.MDLTransform</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetMatrix (OpenTK.Matrix4 matrix, double time);</span>
</pre>
</div>

</div> <!-- end type MDLTransform -->
<!-- start type MDLVertexAttributeData --> <div>
<h3>Type Changed: ModelIO.MDLVertexAttributeData</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BufferSize { get; set; }</span>
</pre>
</div>

</div> <!-- end type MDLVertexAttributeData -->
<div> <!-- start type MDLObjectContainerComponent_Extensions -->
<h3>New Type ModelIO.MDLObjectContainerComponent_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MDLObjectContainerComponent_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static uint GetCount (IMDLObjectContainerComponent This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MDLObject GetObject (IMDLObjectContainerComponent This, uint index);</span>
}
</pre>
</div> <!-- end type MDLObjectContainerComponent_Extensions -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace MultipeerConnectivity --> <div> 
<h2>Namespace MultipeerConnectivity</h2>
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
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.2"</span> <span class='added '>"10.3"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.3.1"</span> <span class='added '>"10.6.0"</span>;
</div></pre>

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
<!-- start type Protocol --> <div>
<h3>Type Changed: ObjCRuntime.Protocol</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public Protocol (System.Type type);</span>
</pre>
</div>

</div> <!-- end type Protocol -->
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

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace OpenGLES --> <div> 
<h2>Namespace OpenGLES</h2>
<!-- start type EAGLContext --> <div>
<h3>Type Changed: OpenGLES.EAGLContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PresentRenderBuffer (uint target, double presentationTime, EAGLContext.PresentationMode mode);</span>
</pre>
</div>

</div> <!-- end type EAGLContext -->

</div> <!-- end namespace OpenGLES -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKPaymentNetwork --> <div>
<h3>Type Changed: PassKit.PKPaymentNetwork</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CarteBancaire { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IDCredit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString QuicPay { get; }</span>
</pre>
</div>

</div> <!-- end type PKPaymentNetwork -->

</div> <!-- end namespace PassKit -->
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLivePhotos = 213,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->

</div> <!-- end namespace Photos -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SCNRenderer FromContext (OpenGLES.EAGLContext context, Foundation.NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SecCertificate --> <div>
<h3>Type Changed: Security.SecCertificate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public string GetCommonName ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetEmailAddresses ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetNormalizedIssuerSequence ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetNormalizedSubjectSequence ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SecKey GetPublicKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetSerialNumber ();</span>
</pre>
</div>

</div> <!-- end type SecCertificate -->
<!-- start type SecPadding --> <div>
<h3>Type Changed: Security.SecPadding</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Hash algorithm is deprecated")]
	PKCS1MD2 = 32768,</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Hash algorithm is deprecated")]
	PKCS1MD5 = 32769,</span>
</div></pre>

</div> <!-- end type SecPadding -->
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
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public LocalAuthentication.LAContext AuthenticationContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsExtractable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsSensitive { get; set; }</span>
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
<!-- start type SecStatusCode --> <div>
<h3>Type Changed: Security.SecStatusCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ACLAddFailed = -67698,</span>
	<span class='added added-field ' data-is-non-breaking="">ACLChangeFailed = -67699,</span>
	<span class='added added-field ' data-is-non-breaking="">ACLDeleteFailed = -67696,</span>
	<span class='added added-field ' data-is-non-breaking="">ACLNotSimple = -25240,</span>
	<span class='added added-field ' data-is-non-breaking="">ACLReplaceFailed = -67697,</span>
	<span class='added added-field ' data-is-non-breaking="">AddinLoadFailed = -67711,</span>
	<span class='added added-field ' data-is-non-breaking="">AddinUnloadFailed = -67714,</span>
	<span class='added added-field ' data-is-non-breaking="">AlgorithmMismatch = -67730,</span>
	<span class='added added-field ' data-is-non-breaking="">AlreadyLoggedIn = -67814,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleAddAppACLSubject = -67589,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleInvalidKeyEndDate = -67593,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleInvalidKeyStartDate = -67592,</span>
	<span class='added added-field ' data-is-non-breaking="">ApplePublicKeyIncomplete = -67590,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleSSLv2Rollback = -67595,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleSignatureMismatch = -67591,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachHandleBusy = -67728,</span>
	<span class='added added-field ' data-is-non-breaking="">AttributeNotInContext = -67720,</span>
	<span class='added added-field ' data-is-non-breaking="">BlockSizeMismatch = -67810,</span>
	<span class='added added-field ' data-is-non-breaking="">BufferTooSmall = -25301,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLAlreadySigned = -67684,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLBadURI = -67617,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLExpired = -67613,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLNotFound = -67615,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLNotTrusted = -67620,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLNotValidYet = -67614,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLPolicyFailed = -67621,</span>
	<span class='added added-field ' data-is-non-breaking="">CRLServerDown = -67616,</span>
	<span class='added added-field ' data-is-non-breaking="">CallbackFailed = -67695,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateCannotOperate = -67817,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateExpired = -67818,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateNotValidYet = -67819,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateRevoked = -67820,</span>
	<span class='added added-field ' data-is-non-breaking="">CertificateSuspended = -67821,</span>
	<span class='added added-field ' data-is-non-breaking="">CodeSigningBadCertChainLength = -67647,</span>
	<span class='added added-field ' data-is-non-breaking="">CodeSigningBadPathLengthConstraint = -67649,</span>
	<span class='added added-field ' data-is-non-breaking="">CodeSigningDevelopment = -67651,</span>
	<span class='added added-field ' data-is-non-breaking="">CodeSigningNoBasicConstraints = -67648,</span>
	<span class='added added-field ' data-is-non-breaking="">CodeSigningNoExtendedKeyUsage = -67650,</span>
	<span class='added added-field ' data-is-non-breaking="">ConversionError = -67594,</span>
	<span class='added added-field ' data-is-non-breaking="">CoreFoundationUnknown = -4960,</span>
	<span class='added added-field ' data-is-non-breaking="">CreateChainFailed = -25318,</span>
	<span class='added added-field ' data-is-non-breaking="">DataNotAvailable = -25316,</span>
	<span class='added added-field ' data-is-non-breaking="">DataNotModifiable = -25317,</span>
	<span class='added added-field ' data-is-non-breaking="">DataTooLarge = -25302,</span>
	<span class='added added-field ' data-is-non-breaking="">DatabaseLocked = -67869,</span>
	<span class='added added-field ' data-is-non-breaking="">DatastoreIsOpen = -67870,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceError = -67727,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceFailed = -67588,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceReset = -67587,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceVerifyFailed = -67812,</span>
	<span class='added added-field ' data-is-non-breaking="">DiskFull = -34,</span>
	<span class='added added-field ' data-is-non-breaking="">DuplicateCallback = -25297,</span>
	<span class='added added-field ' data-is-non-breaking="">EMMLoadFailed = -67709,</span>
	<span class='added added-field ' data-is-non-breaking="">EMMUnloadFailed = -67710,</span>
	<span class='added added-field ' data-is-non-breaking="">EndOfData = -67634,</span>
	<span class='added added-field ' data-is-non-breaking="">EventNotificationCallbackNotFound = -67723,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtendedKeyUsageNotCritical = -67881,</span>
	<span class='added added-field ' data-is-non-breaking="">FieldSpecifiedMultiple = -67866,</span>
	<span class='added added-field ' data-is-non-breaking="">FileTooBig = -67597,</span>
	<span class='added added-field ' data-is-non-breaking="">FunctionFailed = -67677,</span>
	<span class='added added-field ' data-is-non-breaking="">FunctionIntegrityFail = -67670,</span>
	<span class='added added-field ' data-is-non-breaking="">HostNameMismatch = -67602,</span>
	<span class='added added-field ' data-is-non-breaking="">IDPFailure = -67622,</span>
	<span class='added added-field ' data-is-non-breaking="">InDarkWake = -25320,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleDatabaseBlob = -67600,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleFieldFormat = -67867,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleKeyBlob = -67601,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleVersion = -67704,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompleteCertRevocationCheck = -67635,</span>
	<span class='added added-field ' data-is-non-breaking="">InputLengthError = -67724,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientClientID = -67586,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientCredentials = -67822,</span>
	<span class='added added-field ' data-is-non-breaking="">InteractionRequired = -25315,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = -67671,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidACL = -67702,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAccessCredentials = -67700,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAccessRequest = -67876,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAction = -67823,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAddinFunctionTable = -67716,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAlgorithm = -67747,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAlgorithmParms = -67770,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeAccessCredentials = -67796,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeBase = -67788,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeBlockSize = -67764,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeDLDBHandle = -67794,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeEffectiveBits = -67778,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeEndDate = -67782,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeInitVector = -67750,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeIterationCount = -67792,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeKey = -67748,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeKeyLength = -67762,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeKeyType = -67774,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeLabel = -67772,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeMode = -67776,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeOutputSize = -67766,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributePadding = -67754,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributePassphrase = -67760,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributePrime = -67786,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributePrivateKeyFormat = -67800,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributePublicKeyFormat = -67798,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeRandom = -67756,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeRounds = -67768,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeSalt = -67752,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeSeed = -67758,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeStartDate = -67780,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeSubprime = -67790,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeSymmetricKeyFormat = -67802,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeVersion = -67784,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeWrappedKeyFormat = -67804,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAuthority = -67824,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAuthorityKeyID = -67606,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidBaseACLs = -67851,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidBundleInfo = -67857,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRL = -67830,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLAuthority = -67827,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLEncoding = -67828,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLGroup = -67816,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLIndex = -67858,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCRLType = -67829,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCallback = -25298,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCertAuthority = -67826,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCertificateGroup = -67691,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidCertificateRef = -67690,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidContext = -67746,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDBList = -67681,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDBLocation = -67875,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidData = -67673,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDatabaseBlob = -67598,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDigestAlgorithm = -67815,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidEncoding = -67853,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidExtendedKeyUsage = -67609,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormType = -67831,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidGUID = -67679,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidHandle = -67680,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidHandleUsage = -67668,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidID = -67832,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIDLinkage = -67610,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIdentifier = -67833,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIndex = -67834,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIndexInfo = -67877,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidInputVector = -67744,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidItemRef = -25304,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyAttributeMask = -67738,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyBlob = -67599,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyFormat = -67742,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyHierarchy = -67713,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyLabel = -67740,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyRef = -67712,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyUsageForPolicy = -67608,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidKeyUsageMask = -67736,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidLoginName = -67813,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModifyMode = -67879,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidName = -67689,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidNetworkAddress = -67683,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidNewOwner = -67878,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidNumberOfFields = -67685,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOutputVector = -67745,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOwnerEdit = -25244,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPVC = -67708,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidParsingModule = -67868,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPassthroughID = -67682,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPasswordRef = -25261,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPointer = -67675,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPolicyIdentifiers = -67835,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPrefsDomain = -25319,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidQuery = -67693,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidReason = -67837,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidRecord = -67701,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidRequestInputs = -67838,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidRequestor = -67855,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidResponseVector = -67839,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidRoot = -67612,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSampleValue = -67703,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidScope = -67706,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSearchRef = -25305,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidServiceMask = -67717,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSignature = -67688,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidStopOnPolicy = -67840,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSubServiceID = -67719,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSubjectKeyID = -67607,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSubjectName = -67655,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTimeString = -67836,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTrustSetting = -25242,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTrustSettings = -25262,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTuple = -67841,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTupleCredentials = -67852,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidTupleGroup = -67850,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidValidityPeriod = -67854,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidValue = -67694,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyBlobTypeIncorrect = -67732,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyHeaderInconsistent = -67733,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyIsSensitive = -25258,</span>
	<span class='added added-field ' data-is-non-breaking="">KeySizeNotAllowed = -25311,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyUsageIncorrect = -67731,</span>
	<span class='added added-field ' data-is-non-breaking="">LibraryReferenceNotFound = -67715,</span>
	<span class='added added-field ' data-is-non-breaking="">MDSError = -67674,</span>
	<span class='added added-field ' data-is-non-breaking="">MemoryError = -67672,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAlgorithmParms = -67771,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeAccessCredentials = -67797,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeBase = -67789,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeBlockSize = -67765,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeDLDBHandle = -67795,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeEffectiveBits = -67779,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeEndDate = -67783,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeInitVector = -67751,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeIterationCount = -67793,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeKey = -67749,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeKeyLength = -67763,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeKeyType = -67775,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeLabel = -67773,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeMode = -67777,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeOutputSize = -67767,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributePadding = -67755,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributePassphrase = -67761,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributePrime = -67787,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributePrivateKeyFormat = -67801,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributePublicKeyFormat = -67799,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeRandom = -67757,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeRounds = -67769,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeSalt = -67753,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeSeed = -67759,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeStartDate = -67781,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeSubprime = -67791,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeSymmetricKeyFormat = -67803,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeVersion = -67785,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingAttributeWrappedKeyFormat = -67805,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingRequiredExtension = -67880,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingValue = -67871,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeCSRVerifyFailure = -67665,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeFailedConsistencyCheck = -67666,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeNoRequestPending = -67664,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeRequestAlreadyPending = -67663,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeRequestQueued = -67657,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeRequestRedirected = -67658,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeServerAlreadyExists = -67661,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeServerError = -67659,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeServerNotAvailable = -67660,</span>
	<span class='added added-field ' data-is-non-breaking="">MobileMeServerServiceErr = -67662,</span>
	<span class='added added-field ' data-is-non-breaking="">ModuleManagerInitializeFailed = -67721,</span>
	<span class='added added-field ' data-is-non-breaking="">ModuleManagerNotFound = -67722,</span>
	<span class='added added-field ' data-is-non-breaking="">ModuleManifestVerifyFailed = -67678,</span>
	<span class='added added-field ' data-is-non-breaking="">ModuleNotLoaded = -67718,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiplePrivateKeys = -25259,</span>
	<span class='added added-field ' data-is-non-breaking="">MultipleValuesUnsupported = -67842,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkFailure = -67636,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAccessForItem = -25243,</span>
	<span class='added added-field ' data-is-non-breaking="">NoBasicConstraints = -67604,</span>
	<span class='added added-field ' data-is-non-breaking="">NoBasicConstraintsCA = -67605,</span>
	<span class='added added-field ' data-is-non-breaking="">NoCertificateModule = -25313,</span>
	<span class='added added-field ' data-is-non-breaking="">NoDefaultAuthority = -67844,</span>
	<span class='added added-field ' data-is-non-breaking="">NoDefaultKeychain = -25307,</span>
	<span class='added added-field ' data-is-non-breaking="">NoFieldValues = -67859,</span>
	<span class='added added-field ' data-is-non-breaking="">NoPolicyModule = -25314,</span>
	<span class='added added-field ' data-is-non-breaking="">NoStorageModule = -25312,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSuchAttribute = -25303,</span>
	<span class='added added-field ' data-is-non-breaking="">NoSuchClass = -25306,</span>
	<span class='added added-field ' data-is-non-breaking="">NoTrustSettings = -25263,</span>
	<span class='added added-field ' data-is-non-breaking="">NotInitialized = -67667,</span>
	<span class='added added-field ' data-is-non-breaking="">NotLoggedIn = -67729,</span>
	<span class='added added-field ' data-is-non-breaking="">NotSigner = -26267,</span>
	<span class='added added-field ' data-is-non-breaking="">NotTrusted = -67843,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPBadRequest = -67631,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPBadResponse = -67630,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPNoSigner = -67640,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPNotTrustedToAnchor = -67637,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponderInternalError = -67642,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponderMalformedReq = -67641,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponderSignatureRequired = -67644,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponderTryLater = -67643,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponderUnauthorized = -67645,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPResponseNonceMismatch = -67646,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPSignatureError = -67639,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPStatusUnrecognized = -67633,</span>
	<span class='added added-field ' data-is-non-breaking="">OCSPUnavailable = -67632,</span>
	<span class='added added-field ' data-is-non-breaking="">OutputLengthError = -67725,</span>
	<span class='added added-field ' data-is-non-breaking="">PVCAlreadyConfigured = -67707,</span>
	<span class='added added-field ' data-is-non-breaking="">PVCReferentNotFound = -67669,</span>
	<span class='added added-field ' data-is-non-breaking="">PassphraseRequired = -25260,</span>
	<span class='added added-field ' data-is-non-breaking="">PathLengthConstraintExceeded = -67611,</span>
	<span class='added added-field ' data-is-non-breaking="">Pkcs12VerifyFailure = -25264,</span>
	<span class='added added-field ' data-is-non-breaking="">PolicyNotFound = -25241,</span>
	<span class='added added-field ' data-is-non-breaking="">PrivilegeNotGranted = -67705,</span>
	<span class='added added-field ' data-is-non-breaking="">PrivilegeNotSupported = -67726,</span>
	<span class='added added-field ' data-is-non-breaking="">PublicKeyInconsistent = -67811,</span>
	<span class='added added-field ' data-is-non-breaking="">QuerySizeUnknown = -67809,</span>
	<span class='added added-field ' data-is-non-breaking="">QuotaExceeded = -67596,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnlyAttribute = -25309,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordModified = -67638,</span>
	<span class='added added-field ' data-is-non-breaking="">RejectedForm = -67845,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestDescriptor = -67856,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestLost = -67846,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestRejected = -67847,</span>
	<span class='added added-field ' data-is-non-breaking="">ResourceSignBadCertChainLength = -67652,</span>
	<span class='added added-field ' data-is-non-breaking="">ResourceSignBadExtKeyUsage = -67653,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMEBadExtendedKeyUsage = -67624,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMEBadKeyUsage = -67625,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMEEmailAddressesNotFound = -67623,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMEKeyUsageNotCritical = -67626,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMENoEmailAddress = -67627,</span>
	<span class='added added-field ' data-is-non-breaking="">SMIMESubjAltNameNotCritical = -67628,</span>
	<span class='added added-field ' data-is-non-breaking="">SSLBadExtendedKeyUsage = -67629,</span>
	<span class='added added-field ' data-is-non-breaking="">SelfCheckFailed = -67676,</span>
	<span class='added added-field ' data-is-non-breaking="">ServiceNotAvailable = -67585,</span>
	<span class='added added-field ' data-is-non-breaking="">SigningTimeMissing = -67894,</span>
	<span class='added added-field ' data-is-non-breaking="">StagedOperationInProgress = -67806,</span>
	<span class='added added-field ' data-is-non-breaking="">StagedOperationNotStarted = -67807,</span>
	<span class='added added-field ' data-is-non-breaking="">TagNotFound = -67692,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampAddInfoNotAvailable = -67892,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampBadAlg = -67886,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampBadDataFormat = -67888,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampBadRequest = -67887,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampInvalid = -67883,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampMissing = -67882,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampNotTrusted = -67884,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampRejection = -67895,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampRevocationNotification = -67898,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampRevocationWarning = -67897,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampServiceNotAvailable = -67885,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampSystemFailure = -67893,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampTimeNotAvailable = -67889,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampUnacceptedExtension = -67891,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampUnacceptedPolicy = -67890,</span>
	<span class='added added-field ' data-is-non-breaking="">TimestampWaiting = -67896,</span>
	<span class='added added-field ' data-is-non-breaking="">TrustNotAvailable = -25245,</span>
	<span class='added added-field ' data-is-non-breaking="">TrustSettingDeny = -67654,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownCRLExtension = -67619,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownCertExtension = -67618,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownCriticalExtensionFlag = -67603,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownFormat = -25257,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownQualifiedCertStatement = -67656,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownTag = -67687,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedAddressType = -67848,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedFieldFormat = -67860,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedFormat = -25256,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedIndexInfo = -67861,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedKeyAttributeMask = -67739,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedKeyFormat = -67734,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedKeyLabel = -67741,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedKeySize = -67735,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedKeyUsageMask = -67737,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedLocality = -67862,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedNumAttributes = -67863,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedNumIndexes = -67864,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedNumRecordTypes = -67865,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedNumSelectionPreds = -67873,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedOperator = -67874,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedQueryLimits = -67872,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedService = -67849,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedVectorOfBuffers = -67743,</span>
	<span class='added added-field ' data-is-non-breaking="">VerificationFailure = -67686,</span>
	<span class='added added-field ' data-is-non-breaking="">VerifyActionFailed = -67825,</span>
	<span class='added added-field ' data-is-non-breaking="">WritePermissions = -61,</span>
	<span class='added added-field ' data-is-non-breaking="">WrongSecVersion = -25310,</span>
</pre>
</div>

</div> <!-- end type SecStatusCode -->

</div> <!-- end namespace Security -->
<!-- start namespace Social --> <div> 
<h2>Namespace Social</h2>
<!-- start type SLComposeServiceViewController --> <div>
<h3>Type Changed: Social.SLComposeServiceViewController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithTextAttachment (UIKit.UITextView textView, UIKit.NSTextAttachment textAttachment, Foundation.NSRange characterRange, UIKit.UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithUrl (UIKit.UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UIKit.UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type SLComposeServiceViewController -->

</div> <!-- end namespace Social -->
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
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKNode Create (string filename);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (SKNode node);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKShapeNode --> <div>
<h3>Type Changed: SpriteKit.SKShapeNode</h3>
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

</div> <!-- end type SKShapeNode -->
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
<!-- start type SKTileMapNode --> <div>
<h3>Type Changed: SpriteKit.SKTileMapNode</h3>
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

</div> <!-- end type SKTileMapNode -->
<!-- start type SKUniform --> <div>
<h3>Type Changed: SpriteKit.SKUniform</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Matrix4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, OpenTK.Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, SKTexture texture);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, float value);</span>
</pre>
</div>

</div> <!-- end type SKUniform -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestPersonalizationToken (string clientToken, System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestPersonalizationTokenAsync (string clientToken);</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceController -->
<!-- start type SKCloudServiceSetupOptions --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceSetupOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string AffiliateToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CampaignToken { get; set; }</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceSetupOptions -->
<!-- start type SKError --> <div>
<h3>Type Changed: StoreKit.SKError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Revoked = 8,</span>
</pre>
</div>

</div> <!-- end type SKError -->
<div> <!-- start type SKStoreReviewController -->
<h3>New Type StoreKit.SKStoreReviewController</h3>
<pre class='added' data-is-non-breaking="">
public class SKStoreReviewController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKStoreReviewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKStoreReviewController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void RequestReview ();</span>
}
</pre>
</div> <!-- end type SKStoreReviewController -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AlternateIconName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsAlternateIcons { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetAlternateIconName (string alternateIconName, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetAlternateIconNameAsync (string alternateIconName);</span>
</pre>
</div>

</div> <!-- end type UIApplication -->
<!-- start type UICollectionViewController --> <div>
<h3>Type Changed: UIKit.UICollectionViewController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetIndexPath (UICollectionView collectionView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetIndexTitles (UICollectionView collectionView);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewController -->
<!-- start type UICollectionViewDataSource --> <div>
<h3>Type Changed: UIKit.UICollectionViewDataSource</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetIndexPath (UICollectionView collectionView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetIndexTitles (UICollectionView collectionView);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewDataSource -->
<!-- start type UICollectionViewDataSource_Extensions --> <div>
<h3>Type Changed: UIKit.UICollectionViewDataSource_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSIndexPath GetIndexPath (IUICollectionViewDataSource This, UICollectionView collectionView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetIndexTitles (IUICollectionViewDataSource This, UICollectionView collectionView);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewDataSource_Extensions -->
<!-- start type UICollectionViewSource --> <div>
<h3>Type Changed: UIKit.UICollectionViewSource</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetIndexPath (UICollectionView collectionView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetIndexTitles (UICollectionView collectionView);</span>
</pre>
</div>

</div> <!-- end type UICollectionViewSource -->
<!-- start type UIFont --> <div>
<h3>Type Changed: UIKit.UIFont</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (UIFontTextStyle uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFont -->
<!-- start type UIFontDescriptor --> <div>
<h3>Type Changed: UIKit.UIFontDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (UIFontTextStyle uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFontDescriptor -->
<!-- start type UIScreen --> <div>
<h3>Type Changed: UIKit.UIScreen</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaximumFramesPerSecond { get; }</span>
</pre>
</div>

</div> <!-- end type UIScreen -->
<!-- start type UIScrollView --> <div>
<h3>Type Changed: UIKit.UIScrollView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIScrollViewIndexDisplayMode IndexDisplayMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIScrollView -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;UITextFieldEditingEndedEventArgs&gt; EndedWithReason;</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextFieldDelegate --> <div>
<h3>Type Changed: UIKit.UITextFieldDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EditingEnded (UITextField textField, UITextFieldDidEndEditingReason reason);</span>
</pre>
</div>

</div> <!-- end type UITextFieldDelegate -->
<!-- start type UITextFieldDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITextFieldDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void EditingEnded (IUITextFieldDelegate This, UITextField textField, UITextFieldDidEndEditingReason reason);</span>
</pre>
</div>

</div> <!-- end type UITextFieldDelegate_Extensions -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public UITextViewDelegateShouldInteractTextDelegate AllowTextAttachmentInteraction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public UITextViewDelegateShouldInteractUrlDelegate AllowUrlInteraction { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UITextViewDelegate --> <div>
<h3>Type Changed: UIKit.UITextViewDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithTextAttachment (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldInteractWithUrl (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type UITextViewDelegate -->
<!-- start type UITextViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UITextViewDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldInteractWithTextAttachment (IUITextViewDelegate This, UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldInteractWithUrl (IUITextViewDelegate This, UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
</pre>
</div>

</div> <!-- end type UITextViewDelegate_Extensions -->
<!-- start type UIViewAnimationOptions --> <div>
<h3>Type Changed: UIKit.UIViewAnimationOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">PreferredFramesPerSecond30 = 117440512,</span>
	<span class='added added-field ' data-is-non-breaking="">PreferredFramesPerSecond60 = 50331648,</span>
	<span class='added added-field ' data-is-non-breaking="">PreferredFramesPerSecondDefault = 0,</span>
</pre>
</div>

</div> <!-- end type UIViewAnimationOptions -->
<div> <!-- start type UIFontTextStyle -->
<h3>New Type UIKit.UIFontTextStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIFontTextStyle {
	<span class='added added-field ' data-is-non-breaking="">Body = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Callout = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Caption1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Caption2 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Footnote = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Headline = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Subheadline = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Title1 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Title2 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Title3 = 8,</span>
}
</pre>
</div> <!-- end type UIFontTextStyle -->
<div> <!-- start type UIFontTextStyleExtensions -->
<h3>New Type UIKit.UIFontTextStyleExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIFontTextStyleExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (UIFontTextStyle self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontTextStyle GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type UIFontTextStyleExtensions -->
<div> <!-- start type UIScrollViewIndexDisplayMode -->
<h3>New Type UIKit.UIScrollViewIndexDisplayMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIScrollViewIndexDisplayMode {
	<span class='added added-field ' data-is-non-breaking="">AlwaysHidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
}
</pre>
</div> <!-- end type UIScrollViewIndexDisplayMode -->
<div> <!-- start type UITextFieldEditingEndedEventArgs -->
<h3>New Type UIKit.UITextFieldEditingEndedEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class UITextFieldEditingEndedEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextFieldEditingEndedEventArgs (UITextFieldDidEndEditingReason reason);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public UITextFieldDidEndEditingReason Reason { get; set; }</span>
}
</pre>
</div> <!-- end type UITextFieldEditingEndedEventArgs -->
<div> <!-- start type UITextViewDelegateShouldInteractTextDelegate -->
<h3>New Type UIKit.UITextViewDelegateShouldInteractTextDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UITextViewDelegateShouldInteractTextDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextViewDelegateShouldInteractTextDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UITextView textView, NSTextAttachment textAttachment, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
}
</pre>
</div> <!-- end type UITextViewDelegateShouldInteractTextDelegate -->
<div> <!-- start type UITextViewDelegateShouldInteractUrlDelegate -->
<h3>New Type UIKit.UITextViewDelegateShouldInteractUrlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UITextViewDelegateShouldInteractUrlDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UITextViewDelegateShouldInteractUrlDelegate (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (UITextView textView, Foundation.NSUrl url, Foundation.NSRange characterRange, UITextItemInteraction interaction);</span>
}
</pre>
</div> <!-- end type UITextViewDelegateShouldInteractUrlDelegate -->

</div> <!-- end namespace UIKit -->
<!-- start namespace VideoToolbox --> <div> 
<h2>Namespace VideoToolbox</h2>
<!-- start type VTPixelTransferProperties --> <div>
<h3>Type Changed: VideoToolbox.VTPixelTransferProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public VTColorPrimaries DestinationColorPrimaries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTTransferFunction DestinationTransferFunction { get; set; }</span>
</pre>
</div>

</div> <!-- end type VTPixelTransferProperties -->

</div> <!-- end namespace VideoToolbox -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKInterfaceDevice --> <div>
<h3>Type Changed: WatchKit.WKInterfaceDevice</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use PreferredContentSizeCategoryString instead.")]
	public UIKit.UIContentSizeCategory PreferredContentSizeCategory { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string PreferredContentSizeCategoryString { get; }</span>
</pre>
</div>

</div> <!-- end type WKInterfaceDevice -->

</div> <!-- end namespace WatchKit -->
<!-- start namespace iAd --> <div> 
<h2>Namespace iAd</h2>
<!-- start type ADError --> <div>
<h3>Type Changed: iAd.ADError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AdAssetLoadPending = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">AdResponseValidateFailure = 9,</span>
</pre>
</div>

</div> <!-- end type ADError -->

</div> <!-- end namespace iAd -->
</div>



   


 <hr>
