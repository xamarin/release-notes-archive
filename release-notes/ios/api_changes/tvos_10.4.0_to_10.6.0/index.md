---
id: 1EBC25E0-E819-4EBD-8DEE-83148C70F782
title: "tvOS 10.4.0 to 10.6.0"
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
<div> <!-- start type AVQueuedSampleBufferRenderingStatus -->
<h3>New Type AVFoundation.AVQueuedSampleBufferRenderingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVQueuedSampleBufferRenderingStatus {
	<span class='added added-field ' data-is-non-breaking="">Failed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rendering = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type AVQueuedSampleBufferRenderingStatus -->
<div> <!-- start type AVSampleBufferDisplayLayer -->
<h3>New Type AVFoundation.AVSampleBufferDisplayLayer</h3>
<pre class='added' data-is-non-breaking="">
public class AVSampleBufferDisplayLayer : CoreAnimation.CALayer, CoreAnimation.ICAMediaTiming, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferDisplayLayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVSampleBufferDisplayLayer (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferDisplayLayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVSampleBufferDisplayLayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTimebase ControlTimebase { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FailedToDecodeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FailedToDecodeNotificationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReadyForMoreMediaData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVQueuedSampleBufferRenderingStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VideoGravity { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnqueueSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FlushAndRemoveImage ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestMediaDataWhenReadyOnQueue (CoreFoundation.DispatchQueue queue, System.Action enqueuer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopRequestingMediaData ();</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFailedToDecode (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type AVSampleBufferDisplayLayer -->
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
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyAssetUrl { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->

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
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.1"</span> <span class='added '>"10.2"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.3.1"</span> <span class='added '>"10.6.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";</span>
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
<!-- start type SKError --> <div>
<h3>Type Changed: StoreKit.SKError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Revoked = 8,</span>
</pre>
</div>

</div> <!-- end type SKError -->

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
<!-- start type UITableViewController --> <div>
<h3>Type Changed: UIKit.UITableViewController</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint SectionFor (UITableView tableView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
</pre>
</div>

</div> <!-- end type UITableViewController -->
<!-- start type UITableViewDataSource --> <div>
<h3>Type Changed: UIKit.UITableViewDataSource</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint SectionFor (UITableView tableView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
</pre>
</div>

</div> <!-- end type UITableViewDataSource -->
<!-- start type UITableViewDataSource_Extensions --> <div>
<h3>Type Changed: UIKit.UITableViewDataSource_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static nint SectionFor (IUITableViewDataSource This, UITableView tableView, string title, nint atIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] SectionIndexTitles (IUITableViewDataSource This, UITableView tableView);</span>
</pre>
</div>

</div> <!-- end type UITableViewDataSource_Extensions -->
<!-- start type UITableViewSource --> <div>
<h3>Type Changed: UIKit.UITableViewSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] SectionIndexTitles (UITableView tableView);</span>
</pre>
</div>

</div> <!-- end type UITableViewSource -->
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
<div> <!-- start type UILocalizedIndexedCollation -->
<h3>New Type UIKit.UILocalizedIndexedCollation</h3>
<pre class='added' data-is-non-breaking="">
public class UILocalizedIndexedCollation : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UILocalizedIndexedCollation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UILocalizedIndexedCollation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UILocalizedIndexedCollation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SectionIndexTitles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SectionTitles { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UILocalizedIndexedCollation CurrentCollation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetSectionForObject (Foundation.NSObject obj, ObjCRuntime.Selector collationStringSelector);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetSectionForSectionIndexTitle (nint indexTitleIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject[] SortedArrayFromArraycollationStringSelector (Foundation.NSObject[] array, ObjCRuntime.Selector collationStringSelector);</span>
}
</pre>
</div> <!-- end type UILocalizedIndexedCollation -->
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
<h2>New Namespace VideoToolbox</h2>

<div> <!-- start type VTColorPrimaries -->
<h3>New Type VideoToolbox.VTColorPrimaries</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTColorPrimaries {
	<span class='added added-field ' data-is-non-breaking="">Ebu3213 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR7092 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">P22 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SmpteC = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTColorPrimaries -->
<div> <!-- start type VTCompressionProperties -->
<h3>New Type VideoToolbox.VTCompressionProperties</h3>
<pre class='added' data-is-non-breaking="">
public class VTCompressionProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTCompressionProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTCompressionProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? AllowFrameReordering { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AllowTemporalCompression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AspectRatio16x9 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? AverageBitRate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary CleanAperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTColorPrimaries ColorPrimaries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.List&lt;VTDataRateLimit&gt; DataRateLimits { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreMedia.CMPixelFormat? Depth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ExpectedDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ExpectedFrameRate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTFieldCount? FieldCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTFieldDetail FieldDetail { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTH264EntropyMode H264EntropyMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ICCProfile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? MaxFrameDelayCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? MaxH264SliceBytes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? MaxKeyFrameInterval { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? MaxKeyFrameIntervalDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? MoreFramesAfterEnd { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? MoreFramesBeforeStart { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTMultiPassStorage MultiPassStorage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? NumberOfPendingFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary PixelAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? PixelBufferPoolIsShared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary PixelTransferProperties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTProfileLevel ProfileLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? ProgressiveScan { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? Quality { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? RealTime { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? SourceFrameCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTTransferFunction TransferFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? UsingHardwareAcceleratedVideoEncoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary VideoEncoderPixelBufferAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTYCbCrMatrix YCbCrMatrix { get; set; }</span>
}
</pre>
</div> <!-- end type VTCompressionProperties -->
<div> <!-- start type VTCompressionPropertyKey -->
<h3>New Type VideoToolbox.VTCompressionPropertyKey</h3>
<pre class='added' data-is-non-breaking="">
public static class VTCompressionPropertyKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AllowFrameReordering { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AllowTemporalCompression { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AspectRatio16x9 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AverageBitRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanAperture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataRateLimits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Depth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExpectedDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExpectedFrameRate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetail { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264EntropyMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ICCProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaxFrameDelayCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaxH264SliceBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaxKeyFrameInterval { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaxKeyFrameIntervalDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MoreFramesAfterEnd { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MoreFramesBeforeStart { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MultiPassStorage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NumberOfPendingFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelBufferPoolIsShared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelTransferProperties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProfileLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProgressiveScan { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Quality { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RealTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SourceFrameCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString VideoEncoderPixelBufferAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix { get; }</span>
}
</pre>
</div> <!-- end type VTCompressionPropertyKey -->
<div> <!-- start type VTCompressionSession -->
<h3>New Type VideoToolbox.VTCompressionSession</h3>
<pre class='added' data-is-non-breaking="">
public class VTCompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VTCompressionSession (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public VTStatus BeginPass (VTCompressionSessionOptionFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus CompleteFrames (CoreMedia.CMTime completeUntilPresentationTimeStamp);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VTCompressionSession Create (int width, int height, CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, CoreVideo.CVPixelBufferAttributes sourceImageBufferAttributes);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This overload requires that the provided compressionOutputCallback manually CFRetain the passed CMSampleBuffer, use Create(int,int,CMVideoCodecType,VTCompressionOutputCallback,VTVideoEncoderSpecification,CVPixelBufferAttributes) variant instead which does not have that requirement.")]
	public static VTCompressionSession Create (int width, int height, CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, Foundation.NSDictionary sourceImageBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus EncodeFrame (CoreVideo.CVImageBuffer imageBuffer, CoreMedia.CMTime presentationTimestampe, CoreMedia.CMTime duration, Foundation.NSDictionary frameProperties, IntPtr sourceFrame, VTEncodeInfoFlags infoFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus EndPass (bool furtherPassesRequested);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus EndPassAsFinal ();</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreVideo.CVPixelBufferPool GetPixelBufferPool ();</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus GetTimeRangesForNextPass (CoreMedia.CMTimeRange[] timeRanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus PrepareToEncodeFrames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus SetCompressionProperties (VTCompressionProperties options);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~VTCompressionSession ();</span>

	// inner types
	public sealed delegate VTCompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public VTCompressionSession (object object, IntPtr method);</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer, System.AsyncCallback callback, object object);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer);</span>
	}
}
</pre>
</div> <!-- end type VTCompressionSession -->
<div> <!-- start type VTCompressionSessionOptionFlags -->
<h3>New Type VideoToolbox.VTCompressionSessionOptionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	<span class='added added-field ' data-is-non-breaking="">BeginFinalPass = 1,</span>
}
</pre>
</div> <!-- end type VTCompressionSessionOptionFlags -->
<div> <!-- start type VTDataRateLimit -->
<h3>New Type VideoToolbox.VTDataRateLimit</h3>
<pre class='added' data-is-non-breaking="">
public struct VTDataRateLimit {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTDataRateLimit (uint numberOfBytes, double seconds);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public uint NumberOfBytes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double Seconds { get; set; }</span>
}
</pre>
</div> <!-- end type VTDataRateLimit -->
<div> <!-- start type VTDecodeFrameFlags -->
<h3>New Type VideoToolbox.VTDecodeFrameFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum VTDecodeFrameFlags {
	<span class='added added-field ' data-is-non-breaking="">DoNotOutputFrame = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">EnableAsynchronousDecompression = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">EnableTemporalProcessing = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">OneTimeRealTimePlayback = 4,</span>
}
</pre>
</div> <!-- end type VTDecodeFrameFlags -->
<div> <!-- start type VTDecodeInfoFlags -->
<h3>New Type VideoToolbox.VTDecodeInfoFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	<span class='added added-field ' data-is-non-breaking="">Asynchronous = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FrameDropped = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageBufferModifiable = 4,</span>
}
</pre>
</div> <!-- end type VTDecodeInfoFlags -->
<div> <!-- start type VTDecompressionProperties -->
<h3>New Type VideoToolbox.VTDecompressionProperties</h3>
<pre class='added' data-is-non-breaking="">
public class VTDecompressionProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTDecompressionProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTDecompressionProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ContentHasInterframeDependencies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTDeinterlaceMode DeinterlaceMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTFieldMode FieldMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? NumberOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTOnlyTheseFrames OnlyTheseFrames { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? OutputPoolRequestedMinimumBufferCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreVideo.CVPixelBufferPool PixelBufferPool { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? PixelBufferPoolIsShared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreMedia.CMPixelFormat[] PixelFormatsWithReducedResolutionSupport { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary PixelTransferProperties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTPixelTransferProperties PixelTransferSettings { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? RealTime { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? ReducedCoefficientDecode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? ReducedFrameDelivery { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTDecompressionResolutionOptions ReducedResolutionDecode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary[] SuggestedQualityOfServiceTiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByPerformance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByQuality { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? ThreadCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? UsingHardwareAcceleratedVideoDecoder { get; }</span>
}
</pre>
</div> <!-- end type VTDecompressionProperties -->
<div> <!-- start type VTDecompressionPropertyKey -->
<h3>New Type VideoToolbox.VTDecompressionPropertyKey</h3>
<pre class='added' data-is-non-breaking="">
public static class VTDecompressionPropertyKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContentHasInterframeDependencies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DeinterlaceMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DeinterlaceMode_Temporal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DeinterlaceMode_VerticalFilter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode_BothFields { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode_BottomFieldOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode_DeinterlaceFields { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode_SingleField { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldMode_TopFieldOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NumberOfFramesBeingDecoded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OnlyTheseFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OnlyTheseFrames_AllFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OnlyTheseFrames_IFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OnlyTheseFrames_KeyFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelBufferPool { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelBufferPoolIsShared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelTransferProperties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RealTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReducedCoefficientDecode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReducedFrameDelivery { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReducedResolutionDecode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SuggestedQualityOfServiceTiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThreadCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }</span>
}
</pre>
</div> <!-- end type VTDecompressionPropertyKey -->
<div> <!-- start type VTDecompressionResolutionKeys -->
<h3>New Type VideoToolbox.VTDecompressionResolutionKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTDecompressionResolutionKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Width { get; }</span>
}
</pre>
</div> <!-- end type VTDecompressionResolutionKeys -->
<div> <!-- start type VTDecompressionResolutionOptions -->
<h3>New Type VideoToolbox.VTDecompressionResolutionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VTDecompressionResolutionOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTDecompressionResolutionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTDecompressionResolutionOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float? Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? Width { get; set; }</span>
}
</pre>
</div> <!-- end type VTDecompressionResolutionOptions -->
<div> <!-- start type VTDecompressionSession -->
<h3>New Type VideoToolbox.VTDecompressionSession</h3>
<pre class='added' data-is-non-breaking="">
public class VTDecompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VTDecompressionSession (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public VTStatus CanAcceptFormatDescriptor (CoreMedia.CMFormatDescription newDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus CopyBlackPixelBuffer (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, CoreVideo.CVPixelBufferAttributes destinationImageBufferAttributes);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("This overload requires that the provided compressionOutputCallback manually CFRetain the passed CMSampleBuffer, use Create(VTDecompressionOutputCallback,CMVideoFormatDescription,VTVideoDecoderSpecification,CVPixelBufferAttributes) variant instead which does not have that requirement.")]
	public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, Foundation.NSDictionary destinationImageBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus DecodeFrame (CoreMedia.CMSampleBuffer sampleBuffer, VTDecodeFrameFlags decodeFlags, IntPtr sourceFrame, VTDecodeInfoFlags infoFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus FinishDelayedFrames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus SetDecompressionProperties (VTDecompressionProperties options);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus WaitForAsynchronousFrames ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~VTDecompressionSession ();</span>

	// inner types
	public sealed delegate VTDecompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">public VTDecompressionSession (object object, IntPtr method);</span>
		// methods
		<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration, System.AsyncCallback callback, object object);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
		<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration);</span>
	}
}
</pre>
</div> <!-- end type VTDecompressionSession -->
<div> <!-- start type VTDeinterlaceMode -->
<h3>New Type VideoToolbox.VTDeinterlaceMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTDeinterlaceMode {
	<span class='added added-field ' data-is-non-breaking="">Temporal = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VerticalFilter = 1,</span>
}
</pre>
</div> <!-- end type VTDeinterlaceMode -->
<div> <!-- start type VTDownsamplingMode -->
<h3>New Type VideoToolbox.VTDownsamplingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTDownsamplingMode {
	<span class='added added-field ' data-is-non-breaking="">Average = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Decimate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTDownsamplingMode -->
<div> <!-- start type VTEncodeFrameOptionKey -->
<h3>New Type VideoToolbox.VTEncodeFrameOptionKey</h3>
<pre class='added' data-is-non-breaking="">
public static class VTEncodeFrameOptionKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ForceKeyFrame { get; }</span>
}
</pre>
</div> <!-- end type VTEncodeFrameOptionKey -->
<div> <!-- start type VTEncodeFrameOptions -->
<h3>New Type VideoToolbox.VTEncodeFrameOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VTEncodeFrameOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTEncodeFrameOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTEncodeFrameOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ForceKeyFrame { get; set; }</span>
}
</pre>
</div> <!-- end type VTEncodeFrameOptions -->
<div> <!-- start type VTEncodeInfoFlags -->
<h3>New Type VideoToolbox.VTEncodeInfoFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	<span class='added added-field ' data-is-non-breaking="">Asynchronous = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FrameDropped = 2,</span>
}
</pre>
</div> <!-- end type VTEncodeInfoFlags -->
<div> <!-- start type VTFieldCount -->
<h3>New Type VideoToolbox.VTFieldCount</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTFieldCount {
	<span class='added added-field ' data-is-non-breaking="">Interlaced = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Progressive = 1,</span>
}
</pre>
</div> <!-- end type VTFieldCount -->
<div> <!-- start type VTFieldDetail -->
<h3>New Type VideoToolbox.VTFieldDetail</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTFieldDetail {
	<span class='added added-field ' data-is-non-breaking="">SpatialFirstLineEarly = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SpatialFirstLineLate = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">TemporalBottomFirst = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TemporalTopFirst = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTFieldDetail -->
<div> <!-- start type VTFieldMode -->
<h3>New Type VideoToolbox.VTFieldMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTFieldMode {
	<span class='added added-field ' data-is-non-breaking="">BothFields = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomFieldOnly = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">DeinterlaceFields = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">SingleField = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">TopFieldOnly = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTFieldMode -->
<div> <!-- start type VTFrameSilo -->
<h3>New Type VideoToolbox.VTFrameSilo</h3>
<pre class='added' data-is-non-breaking="">
public class VTFrameSilo : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VTFrameSilo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public VTStatus AddSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VTFrameSilo Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus ForEach (System.Func&lt;CoreMedia.CMSampleBuffer,VideoToolbox.VTStatus&gt; callback, CoreMedia.CMTimeRange? range);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus GetProgressOfCurrentPass (float progress);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus SetTimeRangesForNextPass (CoreMedia.CMTimeRange[] ranges);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~VTFrameSilo ();</span>
}
</pre>
</div> <!-- end type VTFrameSilo -->
<div> <!-- start type VTH264EntropyMode -->
<h3>New Type VideoToolbox.VTH264EntropyMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTH264EntropyMode {
	<span class='added added-field ' data-is-non-breaking="">Cabac = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Cavlc = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTH264EntropyMode -->
<div> <!-- start type VTH264EntropyModeKeys -->
<h3>New Type VideoToolbox.VTH264EntropyModeKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTH264EntropyModeKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CABAC { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CAVLC { get; }</span>
}
</pre>
</div> <!-- end type VTH264EntropyModeKeys -->
<div> <!-- start type VTMultiPassStorage -->
<h3>New Type VideoToolbox.VTMultiPassStorage</h3>
<pre class='added' data-is-non-breaking="">
public class VTMultiPassStorage : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VTMultiPassStorage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public VTStatus Close ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static VTMultiPassStorage Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VTMultiPassStorage Create (VTMultiPassStorageCreationOptions options, Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~VTMultiPassStorage ();</span>
}
</pre>
</div> <!-- end type VTMultiPassStorage -->
<div> <!-- start type VTMultiPassStorageCreationOptionKeys -->
<h3>New Type VideoToolbox.VTMultiPassStorageCreationOptionKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTMultiPassStorageCreationOptionKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DoNotDelete { get; }</span>
}
</pre>
</div> <!-- end type VTMultiPassStorageCreationOptionKeys -->
<div> <!-- start type VTMultiPassStorageCreationOptions -->
<h3>New Type VideoToolbox.VTMultiPassStorageCreationOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VTMultiPassStorageCreationOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTMultiPassStorageCreationOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTMultiPassStorageCreationOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? DoNotDelete { get; set; }</span>
}
</pre>
</div> <!-- end type VTMultiPassStorageCreationOptions -->
<div> <!-- start type VTOnlyTheseFrames -->
<h3>New Type VideoToolbox.VTOnlyTheseFrames</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTOnlyTheseFrames {
	<span class='added added-field ' data-is-non-breaking="">AllFrames = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">IFrames = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">KeyFrames = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NonDroppableFrames = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTOnlyTheseFrames -->
<div> <!-- start type VTPixelTransferProperties -->
<h3>New Type VideoToolbox.VTPixelTransferProperties</h3>
<pre class='added' data-is-non-breaking="">
public class VTPixelTransferProperties : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTPixelTransferProperties ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTPixelTransferProperties (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AVFoundation.AVVideoCleanApertureSettings DestinationCleanAperture { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTColorPrimaries DestinationColorPrimaries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData DestinationICCProfile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AVFoundation.AVVideoPixelAspectRatioSettings DestinationPixelAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTTransferFunction DestinationTransferFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTYCbCrMatrix DestinationYCbCrMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTDownsamplingMode DownsamplingMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTScalingMode ScalingMode { get; set; }</span>
}
</pre>
</div> <!-- end type VTPixelTransferProperties -->
<div> <!-- start type VTPixelTransferPropertyKeys -->
<h3>New Type VideoToolbox.VTPixelTransferPropertyKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTPixelTransferPropertyKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationCleanAperture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationColorPrimaries { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationICCProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationPixelAspectRatio { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationTransferFunction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DestinationYCbCrMatrix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownsamplingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownsamplingMode_Average { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DownsamplingMode_Decimate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScalingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScalingMode_CropSourceToCleanAperture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScalingMode_Letterbox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScalingMode_Normal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScalingMode_Trim { get; }</span>
}
</pre>
</div> <!-- end type VTPixelTransferPropertyKeys -->
<div> <!-- start type VTProfileLevel -->
<h3>New Type VideoToolbox.VTProfileLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTProfileLevel {
	<span class='added added-field ' data-is-non-breaking="">H263Profile0Level10 = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">H263Profile0Level45 = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">H263Profile3Level45 = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline13 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline30 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline31 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline32 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline40 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline41 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline42 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline50 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline51 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Baseline52 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">H264BaselineAutoLevel = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Extended50 = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">H264ExtendedAutoLevel = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High30 = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High31 = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High32 = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High40 = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High41 = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High42 = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High50 = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High51 = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">H264High52 = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">H264HighAutoLevel = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main30 = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main31 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main32 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main40 = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main41 = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main42 = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main50 = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main51 = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">H264Main52 = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">H264MainAutoLevel = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VAdvancedSimpleL0 = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VAdvancedSimpleL1 = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VAdvancedSimpleL2 = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VAdvancedSimpleL3 = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VAdvancedSimpleL4 = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VMainL2 = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VMainL3 = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VMainL4 = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VSimpleL0 = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VSimpleL1 = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VSimpleL2 = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">MP4VSimpleL3 = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTProfileLevel -->
<div> <!-- start type VTProfileLevelKeys -->
<h3>New Type VideoToolbox.VTProfileLevelKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTProfileLevelKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H263_Profile0_Level10 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H263_Profile0_Level45 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H263_Profile3_Level45 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_1_3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_3_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_3_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_3_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_4_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_4_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_4_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_5_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_5_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_5_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Baseline_AutoLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Extended_5_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Extended_AutoLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_3_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_3_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_3_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_4_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_4_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_4_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_5_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_5_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_5_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_High_AutoLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_3_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_3_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_3_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_4_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_4_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_4_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_5_0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_5_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_5_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString H264_Main_AutoLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_AdvancedSimple_L0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_AdvancedSimple_L1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_AdvancedSimple_L2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_AdvancedSimple_L3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_AdvancedSimple_L4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Main_L2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Main_L3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Main_L4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Simple_L0 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Simple_L1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Simple_L2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MP4V_Simple_L3 { get; }</span>
}
</pre>
</div> <!-- end type VTProfileLevelKeys -->
<div> <!-- start type VTPropertyKeys -->
<h3>New Type VideoToolbox.VTPropertyKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTPropertyKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DocumentationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReadWriteStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ShouldBeSerialized { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SupportedValueListKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SupportedValueMaximumKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SupportedValueMinimumKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Type { get; }</span>
}
</pre>
</div> <!-- end type VTPropertyKeys -->
<div> <!-- start type VTPropertyOptions -->
<h3>New Type VideoToolbox.VTPropertyOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VTPropertyOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTPropertyOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTPropertyOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString Documentation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTReadWriteStatus ReadWriteStatus { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldBeSerialized { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber[] SupportedValueList { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber SupportedValueMaximum { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber SupportedValueMinimum { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VTPropertyType Type { get; set; }</span>
}
</pre>
</div> <!-- end type VTPropertyOptions -->
<div> <!-- start type VTPropertyReadWriteStatusKeys -->
<h3>New Type VideoToolbox.VTPropertyReadWriteStatusKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTPropertyReadWriteStatusKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReadWrite { get; }</span>
}
</pre>
</div> <!-- end type VTPropertyReadWriteStatusKeys -->
<div> <!-- start type VTPropertyType -->
<h3>New Type VideoToolbox.VTPropertyType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTPropertyType {
	<span class='added added-field ' data-is-non-breaking="">Boolean = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Enumeration = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Number = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTPropertyType -->
<div> <!-- start type VTPropertyTypeKeys -->
<h3>New Type VideoToolbox.VTPropertyTypeKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTPropertyTypeKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Boolean { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Enumeration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Number { get; }</span>
}
</pre>
</div> <!-- end type VTPropertyTypeKeys -->
<div> <!-- start type VTReadWriteStatus -->
<h3>New Type VideoToolbox.VTReadWriteStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTReadWriteStatus {
	<span class='added added-field ' data-is-non-breaking="">ReadOnly = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWrite = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTReadWriteStatus -->
<div> <!-- start type VTScalingMode -->
<h3>New Type VideoToolbox.VTScalingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTScalingMode {
	<span class='added added-field ' data-is-non-breaking="">CropSourceToCleanAperture = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Letterbox = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Trim = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTScalingMode -->
<div> <!-- start type VTSession -->
<h3>New Type VideoToolbox.VTSession</h3>
<pre class='added' data-is-non-breaking="">
public class VTSession : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VTSession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTPropertyOptions GetProperties ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSObject GetProperty (Foundation.NSString propertyKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary GetSerializableProperties ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary GetSupportedProperties ();</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus SetProperties (VTPropertyOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public VTStatus SetProperty (Foundation.NSString propertyKey, Foundation.NSObject value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~VTSession ();</span>
}
</pre>
</div> <!-- end type VTSession -->
<div> <!-- start type VTStatus -->
<h3>New Type VideoToolbox.VTStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTStatus {
	<span class='added added-field ' data-is-non-breaking="">AllocationFailed = -12904,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorCorrectionImageRotationFailed = -12219,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorCorrectionPixelTransferFailed = -12212,</span>
	<span class='added added-field ' data-is-non-breaking="">ColorSyncTransformConvertFailed = -12919,</span>
	<span class='added added-field ' data-is-non-breaking="">CouldNotCreateColorCorrectionData = -12918,</span>
	<span class='added added-field ' data-is-non-breaking="">CouldNotCreateInstance = -12907,</span>
	<span class='added added-field ' data-is-non-breaking="">CouldNotFindTemporalFilter = -12217,</span>
	<span class='added added-field ' data-is-non-breaking="">CouldNotFindVideoDecoder = -12906,</span>
	<span class='added added-field ' data-is-non-breaking="">CouldNotFindVideoEncoder = -12908,</span>
	<span class='added added-field ' data-is-non-breaking="">FormatDescriptionChangeNotSupported = -12916,</span>
	<span class='added added-field ' data-is-non-breaking="">FrameSiloInvalidTimeRange = -12216,</span>
	<span class='added added-field ' data-is-non-breaking="">FrameSiloInvalidTimeStamp = -12215,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageRotationNotSupported = -12914,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientSourceColorData = -12917,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSession = -12903,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiPassStorageIdentifierMismatch = -12913,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiPassStorageInvalid = -12214,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Parameter = -12902,</span>
	<span class='added added-field ' data-is-non-breaking="">PixelTransferNotPermitted = -12218,</span>
	<span class='added added-field ' data-is-non-breaking="">PixelTransferNotSupported = -12905,</span>
	<span class='added added-field ' data-is-non-breaking="">PropertyNotSupported = -12900,</span>
	<span class='added added-field ' data-is-non-breaking="">PropertyReadOnly = -12901,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDecoderAuthorization = -12210,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDecoderBadData = -12909,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDecoderMalfunction = -12911,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDecoderNotAvailableNow = -12913,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDecoderUnsupportedDataFormat = -12910,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoEncoderAuthorization = -12211,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoEncoderMalfunction = -12912,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoEncoderNotAvailableNow = -12915,</span>
}
</pre>
</div> <!-- end type VTStatus -->
<div> <!-- start type VTTransferFunction -->
<h3>New Type VideoToolbox.VTTransferFunction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTTransferFunction {
	<span class='added added-field ' data-is-non-breaking="">ItuR7092 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Smpte240M1955 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseGamma = 3,</span>
}
</pre>
</div> <!-- end type VTTransferFunction -->
<div> <!-- start type VTUtilities -->
<h3>New Type VideoToolbox.VTUtilities</h3>
<pre class='added' data-is-non-breaking="">
public static class VTUtilities {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VTStatus ToCGImage (CoreVideo.CVPixelBuffer pixelBuffer, CoreGraphics.CGImage image);</span>
}
</pre>
</div> <!-- end type VTUtilities -->
<div> <!-- start type VTVideoDecoderSpecification -->
<h3>New Type VideoToolbox.VTVideoDecoderSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class VTVideoDecoderSpecification : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTVideoDecoderSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTVideoDecoderSpecification (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableHardwareAcceleratedVideoDecoder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? RequireHardwareAcceleratedVideoDecoder { get; set; }</span>
}
</pre>
</div> <!-- end type VTVideoDecoderSpecification -->
<div> <!-- start type VTVideoDecoderSpecificationKeys -->
<h3>New Type VideoToolbox.VTVideoDecoderSpecificationKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTVideoDecoderSpecificationKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }</span>
}
</pre>
</div> <!-- end type VTVideoDecoderSpecificationKeys -->
<div> <!-- start type VTVideoEncoder -->
<h3>New Type VideoToolbox.VTVideoEncoder</h3>
<pre class='added' data-is-non-breaking="">
public class VTVideoEncoder {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string CodecName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int CodecType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string EncoderId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string EncoderName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VTVideoEncoder[] GetEncoderList ();</span>
}
</pre>
</div> <!-- end type VTVideoEncoder -->
<div> <!-- start type VTVideoEncoderSpecification -->
<h3>New Type VideoToolbox.VTVideoEncoderSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class VTVideoEncoderSpecification : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VTVideoEncoderSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VTVideoEncoderSpecification (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string EncoderID { get; set; }</span>
}
</pre>
</div> <!-- end type VTVideoEncoderSpecification -->
<div> <!-- start type VTVideoEncoderSpecificationKeys -->
<h3>New Type VideoToolbox.VTVideoEncoderSpecificationKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VTVideoEncoderSpecificationKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EncoderID { get; }</span>
}
</pre>
</div> <!-- end type VTVideoEncoderSpecificationKeys -->
<div> <!-- start type VTYCbCrMatrix -->
<h3>New Type VideoToolbox.VTYCbCrMatrix</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VTYCbCrMatrix {
	<span class='added added-field ' data-is-non-breaking="">ItuR6014 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ItuR7092 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Smpte240M1955 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unset = 0,</span>
}
</pre>
</div> <!-- end type VTYCbCrMatrix -->
</div> <!-- end namespace VideoToolbox -->

</div>



   


 <hr>
