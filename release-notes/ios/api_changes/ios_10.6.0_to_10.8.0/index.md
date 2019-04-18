---
id: 3B9C17B3-A9F6-4404-9AAF-031F728598C8
title: "iOS 10.6.0 to 10.8.0"
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
<!-- start type AVAsset --> <div>
<h3>Type Changed: AVFoundation.AVAsset</h3>
<!-- start type AVAsset.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAsset.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChapterMetadataGroupsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDurationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMediaSelectionGroupsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAsset.Notifications -->

</div> <!-- end type AVAsset -->
<!-- start type AVAssetDownloadUrlSession --> <div>
<h3>Type Changed: AVFoundation.AVAssetDownloadUrlSession</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a `INSUrlSessionDelegate` parameter.")]
	public static Foundation.NSUrlSession FromConfiguration (Foundation.NSUrlSessionConfiguration configuration, Foundation.NSUrlSessionDelegate sessionDelegate, Foundation.NSOperationQueue delegateQueue);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrlSession FromConfiguration (Foundation.NSUrlSessionConfiguration configuration, Foundation.INSUrlSessionDelegate sessionDelegate, Foundation.NSOperationQueue delegateQueue);</span>
</pre>
</div>

</div> <!-- end type AVAssetDownloadUrlSession -->
<!-- start type AVAssetTrack --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack</h3>
<!-- start type AVAssetTrack.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAssetTrack.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSegmentsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimeRangeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTrackAssociationsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAssetTrack.Notifications -->

</div> <!-- end type AVAssetTrack -->
<!-- start type AVAudioEngine --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine</h3>
<!-- start type AVAudioEngine.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAudioEngine.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioEngine.Notifications -->

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioSession --> <div>
<h3>Type Changed: AVFoundation.AVAudioSession</h3>
<!-- start type AVAudioSession.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAudioSession.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInterruption (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVAudioSessionInterruptionEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMediaServicesWereLost (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMediaServicesWereReset (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRouteChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVAudioSessionRouteChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSilenceSecondaryAudioHint (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVAudioSessionSecondaryAudioHintEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioSession.Notifications -->

</div> <!-- end type AVAudioSession -->
<!-- start type AVAudioUnitComponent --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponent</h3>
<!-- start type AVAudioUnitComponent.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnitComponent.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTagsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVAudioUnitComponent.Notifications -->

</div> <!-- end type AVAudioUnitComponent -->
<!-- start type AVCaptureAudioDataOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureAudioDataOutput</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegateQueue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureAudioDataOutput -->
<!-- start type AVCaptureDevice --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice</h3>
<!-- start type AVCaptureDevice.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureDevice.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSubjectAreaDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasConnected (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasDisconnected (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureDevice.Notifications -->

</div> <!-- end type AVCaptureDevice -->
<!-- start type AVCaptureInput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureInput</h3>
<!-- start type AVCaptureInput.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureInput.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePortFormatDescriptionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureInput.Notifications -->

</div> <!-- end type AVCaptureInput -->
<!-- start type AVCaptureSession --> <div>
<h3>Type Changed: AVFoundation.AVCaptureSession</h3>
<!-- start type AVCaptureSession.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVCaptureSession.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidStartRunning (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidStopRunning (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInterruptionEnded (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRuntimeError (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVCaptureSessionRuntimeErrorEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWasInterrupted (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVCaptureSession.Notifications -->

</div> <!-- end type AVCaptureSession -->
<!-- start type AVCaptureVideoDataOutput --> <div>
<h3>Type Changed: AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use overload accepting a IAVCaptureVideoDataOutputSampleBufferDelegate")]
	public virtual void SetSampleBufferDelegate (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackQueue);</span>
</div></pre>

</div> <!-- end type AVCaptureVideoDataOutput -->
<!-- start type AVPlayerItem --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem</h3>
<!-- start type AVPlayerItem.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVPlayerItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveItemFailedToPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;AVPlayerItemErrorEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNewAccessLogEntry (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNewErrorLogEntry (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePlaybackStalled (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimeJumped (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVPlayerItem.Notifications -->

</div> <!-- end type AVPlayerItem -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<!-- start type AVSampleBufferDisplayLayer.Notifications --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFailedToDecode (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer.Notifications -->

</div> <!-- end type AVSampleBufferDisplayLayer -->
<div> <!-- start type AVSampleCursorChunkInfo -->
<h3>New Type AVFoundation.AVSampleCursorChunkInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorChunkInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformFormatDescriptions;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformSampleDurations;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasUniformSampleSizes;</span>
	<span class='added added-field ' data-is-non-breaking="">public long SampleCount;</span>
}
</pre>
</div> <!-- end type AVSampleCursorChunkInfo -->
<div> <!-- start type AVSampleCursorDependencyInfo -->
<h3>New Type AVFoundation.AVSampleCursorDependencyInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorDependencyInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool DependsOnOthers;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasDependentSamples;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool HasRedundantCoding;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItDependsOnOthers;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItHasDependentSamples;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IndicatesWhetherItHasRedundantCoding;</span>
}
</pre>
</div> <!-- end type AVSampleCursorDependencyInfo -->
<div> <!-- start type AVSampleCursorStorageRange -->
<h3>New Type AVFoundation.AVSampleCursorStorageRange</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorStorageRange {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public long Length;</span>
	<span class='added added-field ' data-is-non-breaking="">public long Offset;</span>
}
</pre>
</div> <!-- end type AVSampleCursorStorageRange -->
<div> <!-- start type AVSampleCursorSyncInfo -->
<h3>New Type AVFoundation.AVSampleCursorSyncInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct AVSampleCursorSyncInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public bool IsDroppable;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IsFullSync;</span>
	<span class='added added-field ' data-is-non-breaking="">public bool IsPartialSync;</span>
}
</pre>
</div> <!-- end type AVSampleCursorSyncInfo -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace Accounts --> <div> 
<h2>Namespace Accounts</h2>
<!-- start type ACAccountStore --> <div>
<h3>Type Changed: Accounts.ACAccountStore</h3>
<!-- start type ACAccountStore.Notifications --> <div>
<h3>Type Changed: Accounts.ACAccountStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type ACAccountStore.Notifications -->

</div> <!-- end type ACAccountStore -->

</div> <!-- end namespace Accounts -->
<!-- start namespace AssetsLibrary --> <div> 
<h2>Namespace AssetsLibrary</h2>
<!-- start type ALAssetsLibrary --> <div>
<h3>Type Changed: AssetsLibrary.ALAssetsLibrary</h3>
<!-- start type ALAssetsLibrary.Notifications --> <div>
<h3>Type Changed: AssetsLibrary.ALAssetsLibrary.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;ALAssetLibraryChangedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type ALAssetsLibrary.Notifications -->

</div> <!-- end type ALAssetsLibrary -->

</div> <!-- end namespace AssetsLibrary -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<!-- start type AUAudioUnit.Notifications --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioComponentInstanceInvalidation (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAudioComponentRegistrationsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit.Notifications -->

</div> <!-- end type AUAudioUnit -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKContainer --> <div>
<h3>Type Changed: CloudKit.CKContainer</h3>
<!-- start type CKContainer.Notifications --> <div>
<h3>Type Changed: CloudKit.CKContainer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAccountChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type CKContainer.Notifications -->

</div> <!-- end type CKContainer -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContactStore --> <div>
<h3>Type Changed: Contacts.CNContactStore</h3>
<!-- start type CNContactStore.Notifications --> <div>
<h3>Type Changed: Contacts.CNContactStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNotificationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type CNContactStore.Notifications -->

</div> <!-- end type CNContactStore -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollBoth { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollHorizontally { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollNone { get; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use CAScroll enum")]
	public static Foundation.NSString ScrollVertically { get; }</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CAScroll Scroll { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<div> <!-- start type CAScroll -->
<h3>New Type CoreAnimation.CAScroll</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CAScroll {
	<span class='added added-field ' data-is-non-breaking="">Both = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Horizontally = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertically = 1,</span>
}
</pre>
</div> <!-- end type CAScroll -->
<div> <!-- start type CAScrollExtensions -->
<h3>New Type CoreAnimation.CAScrollExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CAScrollExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CAScroll self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CAScroll GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CAScrollExtensions -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<!-- start type NSManagedObjectContext.Notifications --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidSave (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveObjectsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSManagedObjectChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillSave (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext.Notifications -->

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<!-- start type NSPersistentStoreCoordinator.Notifications --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidImportUbiquitousContentChanges (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresWillChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPersistentStoreCoordinatorStoreChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillRemoveStore (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator.Notifications -->

</div> <!-- end type NSPersistentStoreCoordinator -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreMidi --> <div> 
<h2>Namespace CoreMidi</h2>
<!-- start type Midi --> <div>
<h3>Type Changed: CoreMidi.Midi</h3>
<!-- start type Midi.Notifications --> <div>
<h3>Type Changed: CoreMidi.Midi.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNetworkNotificationContactsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNetworkNotificationSessionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type Midi.Notifications -->

</div> <!-- end type Midi -->
<!-- start type MidiObject --> <div>
<h3>Type Changed: CoreMidi.MidiObject</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MidiError FindByUniqueId (int uniqueId, MidiObject result);</span>
</pre>
</div>

</div> <!-- end type MidiObject -->

</div> <!-- end namespace CoreMidi -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKEventStore --> <div>
<h3>Type Changed: EventKit.EKEventStore</h3>
<!-- start type EKEventStore.Notifications --> <div>
<h3>Type Changed: EventKit.EKEventStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type EKEventStore.Notifications -->

</div> <!-- end type EKEventStore -->

</div> <!-- end namespace EventKit -->
<!-- start namespace ExternalAccessory --> <div> 
<h2>Namespace ExternalAccessory</h2>
<!-- start type EAAccessoryManager --> <div>
<h3>Type Changed: ExternalAccessory.EAAccessoryManager</h3>
<!-- start type EAAccessoryManager.Notifications --> <div>
<h3>Type Changed: ExternalAccessory.EAAccessoryManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type EAAccessoryManager.Notifications -->

</div> <!-- end type EAAccessoryManager -->

</div> <!-- end namespace ExternalAccessory -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSArray --> <div>
<h3>Type Changed: Foundation.NSArray</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSArray FromNSObjects&lt;T&gt; (System.Func&lt;T,Foundation.NSObject&gt; nsobjectificator, T[] items);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSBundleResourceRequest --> <div>
<h3>Type Changed: Foundation.NSBundleResourceRequest</h3>
<!-- start type NSBundleResourceRequest.Notifications --> <div>
<h3>Type Changed: Foundation.NSBundleResourceRequest.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveLowDiskSpace (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSBundleResourceRequest.Notifications -->

</div> <!-- end type NSBundleResourceRequest -->
<!-- start type NSCalendar --> <div>
<h3>Type Changed: Foundation.NSCalendar</h3>
<!-- start type NSCalendar.Notifications --> <div>
<h3>Type Changed: Foundation.NSCalendar.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDayChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSCalendar.Notifications -->

</div> <!-- end type NSCalendar -->
<!-- start type NSExtensionContext --> <div>
<h3>Type Changed: Foundation.NSExtensionContext</h3>
<!-- start type NSExtensionContext.Notifications --> <div>
<h3>Type Changed: Foundation.NSExtensionContext.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveHostDidBecomeActive (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveHostDidEnterBackground (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveHostWillEnterForeground (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveHostWillResignActive (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSExtensionContext.Notifications -->

</div> <!-- end type NSExtensionContext -->
<!-- start type NSFileCoordinator --> <div>
<h3>Type Changed: Foundation.NSFileCoordinator</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(INSFilePresenter) instead")]
	public NSFileCoordinator (NSFilePresenter filePresenterOrNil);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFileCoordinator (INSFilePresenter filePresenterOrNil);</span>
</pre>
</div>

</div> <!-- end type NSFileCoordinator -->
<!-- start type NSFileHandle --> <div>
<h3>Type Changed: Foundation.NSFileHandle</h3>
<!-- start type NSFileHandle.Notifications --> <div>
<h3>Type Changed: Foundation.NSFileHandle.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveConnectionAccepted (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleConnectionAcceptedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDataAvailable (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveReadCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveReadToEndOfFileCompletion (NSObject objectToObserve, System.EventHandler&lt;NSFileHandleReadEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileHandle.Notifications -->

</div> <!-- end type NSFileHandle -->
<!-- start type NSFileManager --> <div>
<h3>Type Changed: Foundation.NSFileManager</h3>
<!-- start type NSFileManager.Notifications --> <div>
<h3>Type Changed: Foundation.NSFileManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveUbiquityIdentityDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSFileManager.Notifications -->

</div> <!-- end type NSFileManager -->
<!-- start type NSFormatter --> <div>
<h3>Type Changed: Foundation.NSFormatter</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use IsPartialStringValid (ref string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out string error) instead")]
	public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, NSString error);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsPartialStringValid (string partialString, NSRange proposedSelRange, string origString, NSRange origSelRange, string error);</span>
</pre>
</div>

</div> <!-- end type NSFormatter -->
<!-- start type NSHttpCookieStorage --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage</h3>
<!-- start type NSHttpCookieStorage.Notifications --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveAcceptPolicyChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCookiesChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSHttpCookieStorage.Notifications -->

</div> <!-- end type NSHttpCookieStorage -->
<!-- start type NSLocale --> <div>
<h3>Type Changed: Foundation.NSLocale</h3>
<!-- start type NSLocale.Notifications --> <div>
<h3>Type Changed: Foundation.NSLocale.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCurrentLocaleDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSLocale.Notifications -->

</div> <!-- end type NSLocale -->
<!-- start type NSMetadataQuery --> <div>
<h3>Type Changed: Foundation.NSMetadataQuery</h3>
<!-- start type NSMetadataQuery.Notifications --> <div>
<h3>Type Changed: Foundation.NSMetadataQuery.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidFinishGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidStartGathering (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidUpdate (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveGatheringProgress (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSMetadataQuery.Notifications -->

</div> <!-- end type NSMetadataQuery -->
<!-- start type NSProcessInfo --> <div>
<h3>Type Changed: Foundation.NSProcessInfo</h3>
<!-- start type NSProcessInfo.Notifications --> <div>
<h3>Type Changed: Foundation.NSProcessInfo.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObservePowerStateDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSProcessInfo.Notifications -->

</div> <!-- end type NSProcessInfo -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool IsEqualTo (IntPtr handle);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSUbiquitousKeyValueStore --> <div>
<h3>Type Changed: Foundation.NSUbiquitousKeyValueStore</h3>
<!-- start type NSUbiquitousKeyValueStore.Notifications --> <div>
<h3>Type Changed: Foundation.NSUbiquitousKeyValueStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChangeExternally (NSObject objectToObserve, System.EventHandler&lt;NSUbiquitousKeyValueStoreChangeEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUbiquitousKeyValueStore.Notifications -->

</div> <!-- end type NSUbiquitousKeyValueStore -->
<!-- start type NSUndoManager --> <div>
<h3>Type Changed: Foundation.NSUndoManager</h3>
<!-- start type NSUndoManager.Notifications --> <div>
<h3>Type Changed: Foundation.NSUndoManager.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCheckpoint (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidOpenUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillCloseUndoGroup (NSObject objectToObserve, System.EventHandler&lt;NSUndoManagerCloseUndoGroupEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillRedoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveWillUndoChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUndoManager.Notifications -->

</div> <!-- end type NSUndoManager -->
<!-- start type NSUrlCredentialStorage --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage</h3>
<!-- start type NSUrlCredentialStorage.Notifications --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveChanged (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUrlCredentialStorage.Notifications -->

</div> <!-- end type NSUrlCredentialStorage -->
<!-- start type NSUrlSession --> <div>
<h3>Type Changed: Foundation.NSUrlSession</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload with a `INSUrlSessionDelegate` parameter.")]
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, INSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);</span>
</pre>
</div>

</div> <!-- end type NSUrlSession -->
<!-- start type NSUserDefaults --> <div>
<h3>Type Changed: Foundation.NSUserDefaults</h3>
<!-- start type NSUserDefaults.Notifications --> <div>
<h3>Type Changed: Foundation.NSUserDefaults.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCompletedInitialSync (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChangeAccounts (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveNoCloudAccount (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveSizeLimitExceeded (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSUserDefaults.Notifications -->

</div> <!-- end type NSUserDefaults -->
<!-- start type NSValueTransformer --> <div>
<h3>Type Changed: Foundation.NSValueTransformer</h3>
<!-- start type NSValueTransformer.Notifications --> <div>
<h3>Type Changed: Foundation.NSValueTransformer.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveCompletedInitialSync (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveDidChangeAccounts (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveSizeLimitExceeded (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSObject ObserveUserDefaultsDidChange (NSObject objectToObserve, System.EventHandler&lt;NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSValueTransformer.Notifications -->

</div> <!-- end type NSValueTransformer -->
<div> <!-- start type NSStringTransformExtensions -->
<h3>New Type Foundation.NSStringTransformExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSStringTransformExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSString GetConstant (NSStringTransform self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSStringTransform GetValue (NSString constant);</span>
}
</pre>
</div> <!-- end type NSStringTransformExtensions -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCController --> <div>
<h3>Type Changed: GameController.GCController</h3>
<!-- start type GCController.Notifications --> <div>
<h3>Type Changed: GameController.GCController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GCController.Notifications -->

</div> <!-- end type GCController -->
<!-- start type GCControllerButtonInput --> <div>
<h3>Type Changed: GameController.GCControllerButtonInput</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonValueChanged PressedChangedHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GCControllerButtonValueChanged ValueChangedHandler { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the PressedChangedHandler property")]
	public virtual void SetPressedChangedHandler (GCControllerButtonValueChanged handler);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ValueChangedHandler property")]
	public virtual void SetValueChangedHandler (GCControllerButtonValueChanged handler);</span>
</div></pre>

</div> <!-- end type GCControllerButtonInput -->
<!-- start type GCMotion --> <div>
<h3>Type Changed: GameController.GCMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;GCMotion&gt; ValueChangedHandler { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the ValueChangedHandler property")]
	public virtual void SetValueChangedHandler (System.Action&lt;GCMotion&gt; handler);</span>
</div></pre>

</div> <!-- end type GCMotion -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<!-- start type GKLocalPlayer.Notifications --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAuthenticationDidChangeNotificationName (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer.Notifications -->

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: GameKit.GKPlayer</h3>
<!-- start type GKPlayer.Notifications --> <div>
<h3>Type Changed: GameKit.GKPlayer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeNotificationName (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type GKPlayer.Notifications -->

</div> <!-- end type GKPlayer -->

</div> <!-- end namespace GameKit -->
<!-- start namespace HealthKit --> <div> 
<h2>Namespace HealthKit</h2>
<!-- start type HKHealthStore --> <div>
<h3>Type Changed: HealthKit.HKHealthStore</h3>
<!-- start type HKHealthStore.Notifications --> <div>
<h3>Type Changed: HealthKit.HKHealthStore.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUserPreferencesDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type HKHealthStore.Notifications -->

</div> <!-- end type HKHealthStore -->

</div> <!-- end namespace HealthKit -->
<!-- start namespace MediaAccessibility --> <div> 
<h2>Namespace MediaAccessibility</h2>
<!-- start type MAAudibleMedia --> <div>
<h3>Type Changed: MediaAccessibility.MAAudibleMedia</h3>
<!-- start type MAAudibleMedia.Notifications --> <div>
<h3>Type Changed: MediaAccessibility.MAAudibleMedia.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSettingsChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MAAudibleMedia.Notifications -->

</div> <!-- end type MAAudibleMedia -->

</div> <!-- end namespace MediaAccessibility -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPMediaLibrary --> <div>
<h3>Type Changed: MediaPlayer.MPMediaLibrary</h3>
<!-- start type MPMediaLibrary.Notifications --> <div>
<h3>Type Changed: MediaPlayer.MPMediaLibrary.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MPMediaLibrary.Notifications -->

</div> <!-- end type MPMediaLibrary -->
<!-- start type MPMoviePlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMoviePlayerController</h3>
<!-- start type MPMoviePlayerController.Notifications --> <div>
<h3>Type Changed: MediaPlayer.MPMoviePlayerController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEnterFullscreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidExitFullscreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDurationAvailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveLoadStateDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMPMoviePlayerIsAirPlayVideoActiveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMediaPlaybackIsPreparedToPlayDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMoviePlayerReadyForDisplayDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNaturalSizeAvailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNowPlayingMovieDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePlaybackDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;MPMoviePlayerFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePlaybackStateDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveScalingModeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSourceTypeAvailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveThumbnailImageRequestDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;MPMoviePlayerThumbnailEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimedMetadataUpdated (Foundation.NSObject objectToObserve, System.EventHandler&lt;MPMoviePlayerTimedMetadataEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTypesAvailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillEnterFullscreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillEnterFullscreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillExitFullscreen (Foundation.NSObject objectToObserve, System.EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MPMoviePlayerController.Notifications -->

</div> <!-- end type MPMoviePlayerController -->
<!-- start type MPMusicPlayerController --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerController</h3>
<!-- start type MPMusicPlayerController.Notifications --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveNowPlayingItemDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObservePlaybackStateDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVolumeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerController.Notifications -->

</div> <!-- end type MPMusicPlayerController -->
<!-- start type MPMusicPlayerControllerQueue --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerControllerQueue</h3>
<!-- start type MPMusicPlayerControllerQueue.Notifications --> <div>
<h3>Type Changed: MediaPlayer.MPMusicPlayerControllerQueue.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MPMusicPlayerControllerQueue.Notifications -->

</div> <!-- end type MPMusicPlayerControllerQueue -->
<!-- start type MPVolumeView --> <div>
<h3>Type Changed: MediaPlayer.MPVolumeView</h3>
<div> <!-- start type Notifications -->
<h3>New Type MediaPlayer.Notifications</h3>
<pre class='added' data-is-non-breaking="">
public static class Notifications {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWirelessRouteActiveDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWirelessRouteActiveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWirelessRoutesAvailableDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWirelessRoutesAvailableDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
}
</pre>
</div> <!-- end type Notifications -->

</div> <!-- end type MPVolumeView -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace MessageUI --> <div> 
<h2>Namespace MessageUI</h2>
<!-- start type MFMessageComposeViewController --> <div>
<h3>Type Changed: MessageUI.MFMessageComposeViewController</h3>
<!-- start type MFMessageComposeViewController.Notifications --> <div>
<h3>Type Changed: MessageUI.MFMessageComposeViewController.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextMessageAvailabilityDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;MFMessageAvailabilityChangedEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type MFMessageComposeViewController.Notifications -->

</div> <!-- end type MFMessageComposeViewController -->

</div> <!-- end namespace MessageUI -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromTextureAsync (ModelIO.MDLTexture texture, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromTextureAsync (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload that takes an 'MDLLightProbeIrradianceDataSource' instead.")]
	public static MDLLightProbe[] PlaceLightProbes (float density, MDLProbePlacement type, MDLLightProbeIrradianceDataSource dataSource);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLLightProbe[] PlaceLightProbes (float density, MDLProbePlacement type, IMDLLightProbeIrradianceDataSource dataSource);</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NEFilterManager --> <div>
<h3>Type Changed: NetworkExtension.NEFilterManager</h3>
<!-- start type NEFilterManager.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEFilterManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEFilterManager.Notifications -->

</div> <!-- end type NEFilterManager -->
<!-- start type NEPacketTunnelProvider --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelProvider</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload accepting a INWTcpConnectionAuthenticationDelegate argument")]
	public virtual NWTcpConnection CreateTcpConnection (NWEndpoint remoteEndpoint, bool enableTls, NWTlsParameters tlsParameters, NWTcpConnectionAuthenticationDelegate delegate);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NWTcpConnection CreateTcpConnection (NWEndpoint remoteEndpoint, bool enableTls, NWTlsParameters tlsParameters, INWTcpConnectionAuthenticationDelegate delegate);</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelProvider -->
<!-- start type NEVpnConnection --> <div>
<h3>Type Changed: NetworkExtension.NEVpnConnection</h3>
<!-- start type NEVpnConnection.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEVpnConnection.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEVpnConnection.Notifications -->

</div> <!-- end type NEVpnConnection -->
<!-- start type NEVpnManager --> <div>
<h3>Type Changed: NetworkExtension.NEVpnManager</h3>
<!-- start type NEVpnManager.Notifications --> <div>
<h3>Type Changed: NetworkExtension.NEVpnManager.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveConfigurationChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NEVpnManager.Notifications -->

</div> <!-- end type NEVpnManager -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace NewsstandKit --> <div> 
<h2>Namespace NewsstandKit</h2>
<!-- start type NKIssue --> <div>
<h3>Type Changed: NewsstandKit.NKIssue</h3>
<!-- start type NKIssue.Notifications --> <div>
<h3>Type Changed: NewsstandKit.NKIssue.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDownloadCompleted (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NKIssue.Notifications -->

</div> <!-- end type NKIssue -->

</div> <!-- end namespace NewsstandKit -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.6.0"</span> <span class='added '>"10.8.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static IntPtr CachePointer (IntPtr handle, string constant, IntPtr* storage);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKAddPaymentPassViewController --> <div>
<h3>Type Changed: PassKit.PKAddPaymentPassViewController</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the overload accepting a IPKAddPaymentPassViewControllerDelegate")]
	public PKAddPaymentPassViewController (PKAddPaymentPassRequestConfiguration configuration, PKAddPaymentPassViewControllerDelegate viewControllerDelegate);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public PKAddPaymentPassViewController (PKAddPaymentPassRequestConfiguration configuration, IPKAddPaymentPassViewControllerDelegate viewControllerDelegate);</span>
</pre>
</div>

</div> <!-- end type PKAddPaymentPassViewController -->
<!-- start type PKPassLibrary --> <div>
<h3>Type Changed: PassKit.PKPassLibrary</h3>
<!-- start type PKPassLibrary.Notifications --> <div>
<h3>Type Changed: PassKit.PKPassLibrary.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRemotePaymentPassesDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type PKPassLibrary.Notifications -->

</div> <!-- end type PKPassLibrary -->

</div> <!-- end namespace PassKit -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNView -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<!-- start type SKCloudServiceController.Notifications --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCloudServiceCapabilitiesDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontIdentifierDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceController.Notifications -->

</div> <!-- end type SKCloudServiceController -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSTextStorage --> <div>
<h3>Type Changed: UIKit.NSTextStorage</h3>
<!-- start type NSTextStorage.Notifications --> <div>
<h3>Type Changed: UIKit.NSTextStorage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidProcessEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillProcessEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSTextStorage.Notifications -->

</div> <!-- end type NSTextStorage -->
<!-- start type UIActionSheet --> <div>
<h3>Type Changed: UIKit.UIActionSheet</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use overload with a IUIActionSheetDelegate parameter")]
	public UIActionSheet (string title, UIActionSheetDelegate del);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use overload with a IUIActionSheetDelegate parameter")]
	public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, string[] other);</span>
</div></pre>

</div> <!-- end type UIActionSheet -->
<!-- start type UIAlertView --> <div>
<h3>Type Changed: UIKit.UIAlertView</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use overload with a IUIAlertViewDelegate parameter")]
	public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, string[] otherButtons);</span>
</div></pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAlertView (string title, string message, IUIAlertViewDelegate del, string cancelButtonTitle, string[] otherButtons);</span>
</pre>
</div>

</div> <!-- end type UIAlertView -->
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<!-- start type UIApplication.Notifications --> <div>
<h3>Type Changed: UIKit.UIApplication.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveContentSizeCategoryChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIContentSizeCategoryChangedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeStatusBarFrame (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIStatusBarFrameChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeStatusBarOrientation (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIStatusBarOrientationChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidEnterBackground (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidFinishLaunching (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIApplicationLaunchEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidReceiveMemoryWarning (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveProtectedDataDidBecomeAvailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveProtectedDataWillBecomeUnavailable (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSignificantTimeChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUserDidTakeScreenshot (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillChangeStatusBarFrame (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIStatusBarFrameChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillChangeStatusBarOrientation (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIStatusBarOrientationChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillEnterForeground (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillResignActive (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillTerminate (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIApplication.Notifications -->

</div> <!-- end type UIApplication -->
<!-- start type UIBarItem --> <div>
<h3>Type Changed: UIKit.UIBarItem</h3>
<!-- start type UIBarItem.Notifications --> <div>
<h3>Type Changed: UIKit.UIBarItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTechnologyKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBoldTextStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveClosedCaptioningStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveElementFocused (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGrayscaleStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGuidedAccessStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHearingDevicePairedEarDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInvertColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMonoAudioStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceTransparencyStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveShakeToUndoDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakScreenStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakSelectionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSwitchControlStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnfocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIBarItem.Notifications -->

</div> <!-- end type UIBarItem -->
<!-- start type UIDevice --> <div>
<h3>Type Changed: UIKit.UIDevice</h3>
<!-- start type UIDevice.Notifications --> <div>
<h3>Type Changed: UIKit.UIDevice.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBatteryLevelDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBatteryStateDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveOrientationDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveProximityStateDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIDevice.Notifications -->

</div> <!-- end type UIDevice -->
<!-- start type UIDocument --> <div>
<h3>Type Changed: UIKit.UIDocument</h3>
<!-- start type UIDocument.Notifications --> <div>
<h3>Type Changed: UIKit.UIDocument.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStateChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIDocument.Notifications -->

</div> <!-- end type UIDocument -->
<!-- start type UIImage --> <div>
<h3>Type Changed: UIKit.UIImage</h3>
<!-- start type UIImage.Notifications --> <div>
<h3>Type Changed: UIKit.UIImage.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTechnologyKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBoldTextStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveClosedCaptioningStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveElementFocused (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGrayscaleStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGuidedAccessStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHearingDevicePairedEarDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInvertColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMonoAudioStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceTransparencyStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveShakeToUndoDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakScreenStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakSelectionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSwitchControlStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnfocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIImage.Notifications -->

</div> <!-- end type UIImage -->
<!-- start type UIKeyboard --> <div>
<h3>Type Changed: UIKit.UIKeyboard</h3>
<!-- start type UIKeyboard.Notifications --> <div>
<h3>Type Changed: UIKit.UIKeyboard.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidChangeFrame (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidHide (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidShow (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillChangeFrame (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillHide (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillShow (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKeyboardEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIKeyboard.Notifications -->

</div> <!-- end type UIKeyboard -->
<!-- start type UIMenuController --> <div>
<h3>Type Changed: UIKit.UIMenuController</h3>
<!-- start type UIMenuController.Notifications --> <div>
<h3>Type Changed: UIKit.UIMenuController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidHideMenu (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidShowMenu (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMenuFrameDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillHideMenu (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillShowMenu (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIMenuController.Notifications -->

</div> <!-- end type UIMenuController -->
<!-- start type UIPasteboard --> <div>
<h3>Type Changed: UIKit.UIPasteboard</h3>
<!-- start type UIPasteboard.Notifications --> <div>
<h3>Type Changed: UIKit.UIPasteboard.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIPasteboardChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveRemoved (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIPasteboardChangeEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIPasteboard.Notifications -->

</div> <!-- end type UIPasteboard -->
<!-- start type UIPreviewInteraction --> <div>
<h3>Type Changed: UIKit.UIPreviewInteraction</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use overload accepting a IUICoordinateSpace")]
	public virtual CoreGraphics.CGPoint GetLocationInCoordinateSpace (UICoordinateSpace coordinateSpace);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetLocationInCoordinateSpace (IUICoordinateSpace coordinateSpace);</span>
</pre>
</div>

</div> <!-- end type UIPreviewInteraction -->
<!-- start type UIScreen --> <div>
<h3>Type Changed: UIKit.UIScreen</h3>
<!-- start type UIScreen.Notifications --> <div>
<h3>Type Changed: UIKit.UIScreen.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBrightnessDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveModeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIScreen.Notifications -->

</div> <!-- end type UIScreen -->
<!-- start type UISegmentedControl --> <div>
<h3>Type Changed: UIKit.UISegmentedControl</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public UISegmentedControl (Foundation.NSArray items);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISegmentedControl (Foundation.NSString[] strings);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISegmentedControl (string[] strings);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISegmentedControl (UIImage[] images);</span>
</pre>
</div>

</div> <!-- end type UISegmentedControl -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<!-- start type UITableView.Notifications --> <div>
<h3>Type Changed: UIKit.UITableView.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSelectionDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UITableView.Notifications -->

</div> <!-- end type UITableView -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<!-- start type UITextField.Notifications --> <div>
<h3>Type Changed: UIKit.UITextField.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCurrentInputModeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidBeginEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidEndEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextFieldTextDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UITextField.Notifications -->

</div> <!-- end type UITextField -->
<!-- start type UITextFieldDidEndEditingReason --> <div>
<h3>Type Changed: UIKit.UITextFieldDidEndEditingReason</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Unknown = -1,</span>
</pre>
</div>

</div> <!-- end type UITextFieldDidEndEditingReason -->
<!-- start type UITextInputMode --> <div>
<h3>Type Changed: UIKit.UITextInputMode</h3>
<!-- start type UITextInputMode.Notifications --> <div>
<h3>Type Changed: UIKit.UITextInputMode.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCurrentInputModeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UITextInputMode.Notifications -->

</div> <!-- end type UITextInputMode -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<!-- start type UITextView.Notifications --> <div>
<h3>Type Changed: UIKit.UITextView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveCurrentInputModeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidBeginEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTextDidEndEditing (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UITextView.Notifications -->

</div> <!-- end type UITextView -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<!-- start type UIView.Notifications --> <div>
<h3>Type Changed: UIKit.UIView.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTechnologyKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBoldTextStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveClosedCaptioningStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveElementFocused (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGrayscaleStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGuidedAccessStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHearingDevicePairedEarDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInvertColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMonoAudioStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceTransparencyStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveShakeToUndoDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakScreenStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakSelectionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSwitchControlStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnfocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIView.Notifications -->

</div> <!-- end type UIView -->
<!-- start type UIViewController --> <div>
<h3>Type Changed: UIKit.UIViewController</h3>
<!-- start type UIViewController.Notifications --> <div>
<h3>Type Changed: UIKit.UIViewController.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveShowDetailTargetDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIViewController.Notifications -->

</div> <!-- end type UIViewController -->
<!-- start type UIWindow --> <div>
<h3>Type Changed: UIKit.UIWindow</h3>
<!-- start type UIWindow.Notifications --> <div>
<h3>Type Changed: UIKit.UIWindow.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeHidden (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidBecomeVisible (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidResignKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIWindow.Notifications -->

</div> <!-- end type UIWindow -->

</div> <!-- end namespace UIKit -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKInterfaceObject --> <div>
<h3>Type Changed: WatchKit.WKInterfaceObject</h3>
<!-- start type WKInterfaceObject.Notifications --> <div>
<h3>Type Changed: WatchKit.WKInterfaceObject.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKit.UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTechnologyKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveBoldTextStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveClosedCaptioningStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveElementFocused (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGrayscaleStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveGuidedAccessStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveHearingDevicePairedEarDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveInvertColorsStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveMonoAudioStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceTransparencyStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveShakeToUndoDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakScreenStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSpeakSelectionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveSwitchControlStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnfocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceObject.Notifications -->

</div> <!-- end type WKInterfaceObject -->

</div> <!-- end namespace WatchKit -->
</div>



   


 <hr>
