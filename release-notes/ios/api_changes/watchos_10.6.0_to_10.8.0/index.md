---
id: 7C3A4568-6211-4660-9E03-85190964650D
title: "watchOS 10.6.0 to 10.8.0"
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
<!-- start namespace ClockKit --> <div> 
<h2>Namespace ClockKit</h2>
<!-- start type CLKComplicationServer --> <div>
<h3>Type Changed: ClockKit.CLKComplicationServer</h3>
<!-- start type CLKComplicationServer.Notifications --> <div>
<h3>Type Changed: ClockKit.CLKComplicationServer.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveActiveComplicationsDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type CLKComplicationServer.Notifications -->

</div> <!-- end type CLKComplicationServer -->

</div> <!-- end namespace ClockKit -->
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
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStoresWillChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;NSPersistentStoreCoordinatorStoreChangeEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveWillRemoveStore (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator.Notifications -->

</div> <!-- end type NSPersistentStoreCoordinator -->

</div> <!-- end namespace CoreData -->
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
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKAccessibility --> <div>
<h3>Type Changed: WatchKit.WKAccessibility</h3>
<!-- start type WKAccessibility.Notifications --> <div>
<h3>Type Changed: WatchKit.WKAccessibility.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveVoiceOverStatusChanged (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WKAccessibility.Notifications -->

</div> <!-- end type WKAccessibility -->
<!-- start type WKAudioFilePlayerItem --> <div>
<h3>Type Changed: WatchKit.WKAudioFilePlayerItem</h3>
<!-- start type WKAudioFilePlayerItem.Notifications --> <div>
<h3>Type Changed: WatchKit.WKAudioFilePlayerItem.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFailedToPlayToEndTime (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveTimeJumped (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WKAudioFilePlayerItem.Notifications -->

</div> <!-- end type WKAudioFilePlayerItem -->
<!-- start type WKInterfaceObject --> <div>
<h3>Type Changed: WatchKit.WKInterfaceObject</h3>
<!-- start type WKInterfaceObject.Notifications --> <div>
<h3>Type Changed: WatchKit.WKInterfaceObject.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAnnouncementDidFinish (Foundation.NSObject objectToObserve, System.EventHandler&lt;UIKit.UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTechnologyKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveElementFocused (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveFocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveUnfocusedElementKey (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceObject.Notifications -->

</div> <!-- end type WKInterfaceObject -->
<!-- start type WKInterfaceSCNScene --> <div>
<h3>Type Changed: WatchKit.WKInterfaceSCNScene</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceSCNScene -->

</div> <!-- end namespace WatchKit -->
</div>



   


 <hr>
