---
id: 6241141C-61E3-4632-8F35-601C9EBE70ED
title: "watchOS 10.12.0 to 10.99.7"
---

# API diff

 [Xamarin.WatchOS.dll](#diff/xi/Xamarin.WatchOS/Xamarin.WatchOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.WatchOS/MonoTouch.NUnitLite.html)

   


   


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
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InManualRenderingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioFormat ManualRenderingFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ManualRenderingMaximumFrameCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingMode ManualRenderingMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long ManualRenderingSampleTime { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EnableManualRenderingMode (AVAudioEngineManualRenderingMode mode, AVAudioFormat pcmFormat, uint maximumFrameCount, Foundation.NSError outError);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual AVAudioEngineManualRenderingStatus RenderOffline (uint numberOfFrames, AVAudioPcmBuffer buffer, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AVAudioEngine -->
<!-- start type AVAudioNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Latency { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double OutputPresentationLatency { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioNode -->
<!-- start type AVAudioPlayerNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleFile (AVAudioFile file, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleFileAsync (AVAudioFile file, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScheduleSegment (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType, System.Action&lt;AVAudioPlayerNodeCompletionCallbackType&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;AVAudioPlayerNodeCompletionCallbackType&gt; ScheduleSegmentAsync (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, AVAudioPlayerNodeCompletionCallbackType callbackType);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayerNode -->
<!-- start type AVAudioSettings --> <div>
<h3>Type Changed: AVFoundation.AVAudioSettings</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileTypeKey { get; }</span>
</pre>
</div>

</div> <!-- end type AVAudioSettings -->
<div> <!-- start type AVAudioEngineManualRenderingError -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingError {
	<span class='added added-field ' data-is-non-breaking="">Initialized = -80801,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidMode = -80800,</span>
	<span class='added added-field ' data-is-non-breaking="">NotRunning = -80802,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingError -->
<div> <!-- start type AVAudioEngineManualRenderingMode -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingMode {
	<span class='added added-field ' data-is-non-breaking="">Offline = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Realtime = 1,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingMode -->
<div> <!-- start type AVAudioEngineManualRenderingStatus -->
<h3>New Type AVFoundation.AVAudioEngineManualRenderingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioEngineManualRenderingStatus {
	<span class='added added-field ' data-is-non-breaking="">CannotDoInCurrentContext = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Error = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientDataFromInputNode = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type AVAudioEngineManualRenderingStatus -->
<div> <!-- start type AVAudioInputNode -->
<h3>New Type AVFoundation.AVAudioInputNode</h3>
<pre class='added' data-is-non-breaking="">
public class AVAudioInputNode : AVFoundation.AVAudioIONode, IAVAudioMixing, IAVAudioStereoMixing, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioInputNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioInputNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pan { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Volume { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);</span>
}
</pre>
</div> <!-- end type AVAudioInputNode -->
<div> <!-- start type AVAudioPlayerNodeCompletionCallbackType -->
<h3>New Type AVFoundation.AVAudioPlayerNodeCompletionCallbackType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVAudioPlayerNodeCompletionCallbackType {
	<span class='added added-field ' data-is-non-breaking="">Consumed = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PlayedBack = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rendered = 1,</span>
}
</pre>
</div> <!-- end type AVAudioPlayerNodeCompletionCallbackType -->
<div> <!-- start type AVCaptureLensStabilizationStatus -->
<h3>New Type AVFoundation.AVCaptureLensStabilizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVCaptureLensStabilizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Active = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfRange = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unavailable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
}
</pre>
</div> <!-- end type AVCaptureLensStabilizationStatus -->
<div> <!-- start type AVFileTypes -->
<h3>New Type AVFoundation.AVFileTypes</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVFileTypes {
	<span class='added added-field ' data-is-non-breaking="">AC3 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Aifc = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Aiff = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Amr = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleM4V = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AppleM4a = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Avci = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">CoreAudioFormat = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Dng = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">EnhancedAC3 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Heic = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Heif = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Jpeg = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Mpeg4 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MpegLayer3 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">QuickTimeMovie = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SunAU = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreeGpp = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ThreeGpp2 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Tiff = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Wave = 6,</span>
}
</pre>
</div> <!-- end type AVFileTypes -->
<div> <!-- start type AVFileTypesExtensions -->
<h3>New Type AVFoundation.AVFileTypesExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVFileTypesExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (AVFileTypes self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVFileTypes GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type AVFileTypesExtensions -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type AudioChannelLabel --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLabel</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HoaAcn = 500,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn0 = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn1 = 131073,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn10 = 131082,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn11 = 131083,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn12 = 131084,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn13 = 131085,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn14 = 131086,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn15 = 131087,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn2 = 131074,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn3 = 131075,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn4 = 131076,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn5 = 131077,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn6 = 131078,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn65024 = 196096,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn7 = 131079,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn8 = 131080,</span>
	<span class='added added-field ' data-is-non-breaking="">HoaAcn9 = 131081,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLabel -->
<!-- start type AudioChannelLayoutTag --> <div>
<h3>Type Changed: AudioToolbox.AudioChannelLayoutTag</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_N3D = 12517376,</span>
	<span class='added added-field ' data-is-non-breaking="">HOA_ACN_SN3D = 12451840,</span>
</pre>
</div>

</div> <!-- end type AudioChannelLayoutTag -->
<!-- start type AudioFormatType --> <div>
<h3>Type Changed: AudioToolbox.AudioFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Flac = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">Opus = 1869641075,</span>
</pre>
</div>

</div> <!-- end type AudioFormatType -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKFetchRecordZoneChangesOptions --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZoneChangesOptions</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type CKFetchRecordZoneChangesOptions -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContact --> <div>
<h3>Type Changed: Contacts.CNContact</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderWriting</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] WritableTypeIdentifiersForItemProvider { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSItemProviderRepresentationVisibility GetItemProviderVisibility (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSProgress LoadData (string typeIdentifier, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync (string typeIdentifier, Foundation.NSProgress result);</span>
</pre>
</div>

</div> <!-- end type CNContact -->
<!-- start type CNErrorCode --> <div>
<h3>Type Changed: Contacts.CNErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierDoesNotExist = 601,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientIdentifierInvalid = 600,</span>
	<span class='added added-field ' data-is-non-breaking="">VCardMalformed = 700,</span>
</pre>
</div>

</div> <!-- end type CNErrorCode -->
<!-- start type CNLabelContactRelationKey --> <div>
<h3>Type Changed: Contacts.CNLabelContactRelationKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Daughter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Son { get; }</span>
</pre>
</div>

</div> <!-- end type CNLabelContactRelationKey -->
<!-- start type CNMutableContact --> <div>
<h3>Type Changed: Contacts.CNMutableContact</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderReading</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSItemProviderWriting</span>
</pre>
</div>

</div> <!-- end type CNMutableContact -->
<!-- start type CNPostalAddressKeyOption --> <div>
<h3>Type Changed: Contacts.CNPostalAddressKeyOption</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SubAdministrativeArea = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SubLocality = 6,</span>
</pre>
</div>

</div> <!-- end type CNPostalAddressKeyOption -->
<!-- start type CNSocialProfile --> <div>
<h3>Type Changed: Contacts.CNSocialProfile</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string LocalizeProperty (CNPostalAddressKeyOption key);</span>
</pre>
</div>

</div> <!-- end type CNSocialProfile -->
<div> <!-- start type CNPostalAddressKeyOptionExtensions -->
<h3>New Type Contacts.CNPostalAddressKeyOptionExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CNPostalAddressKeyOptionExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CNPostalAddressKeyOption self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CNPostalAddressKeyOption GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CNPostalAddressKeyOptionExtensions -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type MigrationErrorType --> <div>
<h3>Type Changed: CoreData.MigrationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HistoryTokenExpired = 134301,</span>
</pre>
</div>

</div> <!-- end type MigrationErrorType -->
<!-- start type NSAttributeType --> <div>
<h3>Type Changed: CoreData.NSAttributeType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Uri = 1200,</span>
	<span class='added added-field ' data-is-non-breaking="">Uuid = 1100,</span>
</pre>
</div>

</div> <!-- end type NSAttributeType -->
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression CoreSpotlightDisplayNameExpression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription[] Indexes { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionAuthor { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BinaryStoreInsecureDecodingCompatibilityOption { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BinaryStoreSecureDecodingClasses { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HistoryTrackingKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSQueryGenerationToken --> <div>
<h3>Type Changed: CoreData.NSQueryGenerationToken</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken (Foundation.NSCoder coder);</span>
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

</div> <!-- end type NSQueryGenerationToken -->
<!-- start type ValidationErrorType --> <div>
<h3>Type Changed: CoreData.ValidationErrorType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InvalidUri = 1690,</span>
</pre>
</div>

</div> <!-- end type ValidationErrorType -->
<div> <!-- start type NSFetchIndexDescription -->
<h3>New Type CoreData.NSFetchIndexDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexDescription (string name, NSFetchIndexElementDescription[] elements);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementDescription[] Elements { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSEntityDescription Entity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate PartialIndexPredicate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexDescription -->
<div> <!-- start type NSFetchIndexElementDescription -->
<h3>New Type CoreData.NSFetchIndexElementDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchIndexElementDescription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchIndexElementDescription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchIndexElementDescription (NSPropertyDescription property, NSFetchIndexElementType collationType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexElementType CollationType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFetchIndexDescription IndexDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsAscending { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPropertyDescription Property { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PropertyName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementDescription -->
<div> <!-- start type NSFetchIndexElementType -->
<h3>New Type CoreData.NSFetchIndexElementType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSFetchIndexElementType {
	<span class='added added-field ' data-is-non-breaking="">Binary = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RTree = 1,</span>
}
</pre>
</div> <!-- end type NSFetchIndexElementType -->
<div> <!-- start type NSPersistentHistoryChange -->
<h3>New Type CoreData.NSPersistentHistoryChange</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryChange : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual long ChangeId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChangeType ChangeType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectID ChangedObjectId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary Tombstone { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryTransaction Transaction { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;NSPropertyDescription&gt; UpdatedProperties { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChange -->
<div> <!-- start type NSPersistentHistoryChangeRequest -->
<h3>New Type CoreData.NSPersistentHistoryChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryChangeRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest DeleteHistoryBefore (Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryToken token);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (NSPersistentHistoryTransaction transaction);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentHistoryChangeRequest FetchHistoryAfter (Foundation.NSDate date);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeRequest -->
<div> <!-- start type NSPersistentHistoryChangeType -->
<h3>New Type CoreData.NSPersistentHistoryChangeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryChangeType {
	<span class='added added-field ' data-is-non-breaking="">Delete = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Insert = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Update = 1,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryChangeType -->
<div> <!-- start type NSPersistentHistoryResult -->
<h3>New Type CoreData.NSPersistentHistoryResult</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryResult : CoreData.NSPersistentStoreResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Result { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryResultType ResultType { get; }</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResult -->
<div> <!-- start type NSPersistentHistoryResultType -->
<h3>New Type CoreData.NSPersistentHistoryResultType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSPersistentHistoryResultType {
	<span class='added added-field ' data-is-non-breaking="">ChangesOnly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Count = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectIds = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusOnly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsAndChanges = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TransactionsOnly = 3,</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryResultType -->
<div> <!-- start type NSPersistentHistoryToken -->
<h3>New Type CoreData.NSPersistentHistoryToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentHistoryToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentHistoryToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryToken -->
<div> <!-- start type NSPersistentHistoryTransaction -->
<h3>New Type CoreData.NSPersistentHistoryTransaction</h3>
<pre class='added' data-is-non-breaking="">
public abstract class NSPersistentHistoryTransaction : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentHistoryTransaction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string BundleId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryChange[] Changes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContextName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNotification ObjectIdNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProcessId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StoreId { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Timestamp { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentHistoryToken Token { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long TransactionNumber { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSPersistentHistoryTransaction -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodePostalAddress (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodePostalAddressAsync (Contacts.CNPostalAddress postalAddress, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->
<!-- start type CLLocationManager --> <div>
<h3>Type Changed: CoreLocation.CLLocationManager</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CLActivityType ActivityType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsBackgroundLocationUpdates { get; set; }</span>
</pre>
</div>

</div> <!-- end type CLLocationManager -->
<!-- start type CLPlacemark --> <div>
<h3>Type Changed: CoreLocation.CLPlacemark</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Contacts.CNPostalAddress PostalAddress { get; }</span>
</pre>
</div>

</div> <!-- end type CLPlacemark -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMotion --> <div> 
<h2>Namespace CoreMotion</h2>
<!-- start type CMAltimeter --> <div>
<h3>Type Changed: CoreMotion.CMAltimeter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMAltimeter -->
<!-- start type CMDeviceMotion --> <div>
<h3>Type Changed: CoreMotion.CMDeviceMotion</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Heading { get; }</span>
</pre>
</div>

</div> <!-- end type CMDeviceMotion -->
<!-- start type CMMotionActivityManager --> <div>
<h3>Type Changed: CoreMotion.CMMotionActivityManager</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMMotionActivityManager -->
<!-- start type CMPedometer --> <div>
<h3>Type Changed: CoreMotion.CMPedometer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMPedometer -->
<!-- start type CMSensorRecorder --> <div>
<h3>Type Changed: CoreMotion.CMSensorRecorder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CMAuthorizationStatus AuthorizationStatus { get; }</span>
</pre>
</div>

</div> <!-- end type CMSensorRecorder -->
<div> <!-- start type CMAuthorizationStatus -->
<h3>New Type CoreMotion.CMAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CMAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type CMAuthorizationStatus -->

</div> <!-- end namespace CoreMotion -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<div> <!-- start type CVAttachmentMode -->
<h3>New Type CoreVideo.CVAttachmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVAttachmentMode {
	<span class='added added-field ' data-is-non-breaking="">ShouldNotPropagate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ShouldPropagate = 1,</span>
}
</pre>
</div> <!-- end type CVAttachmentMode -->
<div> <!-- start type CVBuffer -->
<h3>New Type CoreVideo.CVBuffer</h3>
<pre class='added' data-is-non-breaking="">
public class CVBuffer : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovieTimeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NonPropagatedAttachmentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropagatedAttachmentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeScaleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeValueKey { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public T GetAttachment&lt;T&gt; (Foundation.NSString key, CVAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary GetAttachments (CVAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PropogateAttachments (CVBuffer destinationBuffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAllAttachments ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAttachment (Foundation.NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAttachment (Foundation.NSString key, ObjCRuntime.INativeObject value, CVAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAttachments (Foundation.NSDictionary theAttachments, CVAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~CVBuffer ();</span>
}
</pre>
</div> <!-- end type CVBuffer -->
<div> <!-- start type CVFillExtendedPixelsCallBack -->
<h3>New Type CoreVideo.CVFillExtendedPixelsCallBack</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CVFillExtendedPixelsCallBack : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVFillExtendedPixelsCallBack (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IntPtr pixelBuffer, IntPtr refCon, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (IntPtr pixelBuffer, IntPtr refCon);</span>
}
</pre>
</div> <!-- end type CVFillExtendedPixelsCallBack -->
<div> <!-- start type CVFillExtendedPixelsCallBackData -->
<h3>New Type CoreVideo.CVFillExtendedPixelsCallBackData</h3>
<pre class='added' data-is-non-breaking="">
public struct CVFillExtendedPixelsCallBackData {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVFillExtendedPixelsCallBack FillCallBack;</span>
	<span class='added added-field ' data-is-non-breaking="">public IntPtr UserInfo;</span>
	<span class='added added-field ' data-is-non-breaking="">public nint Version;</span>
}
</pre>
</div> <!-- end type CVFillExtendedPixelsCallBackData -->
<div> <!-- start type CVImageBuffer -->
<h3>New Type CoreVideo.CVImageBuffer</h3>
<pre class='added' data-is-non-breaking="">
public class CVImageBuffer : CoreVideo.CVBuffer, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlphaChannelIsOpaque { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CGColorSpaceKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocationBottomFieldKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocationTopFieldKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_Bottom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_Center { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_DV420 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_Left { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_Top { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaLocation_TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaSubsamplingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaSubsampling_411 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaSubsampling_420 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ChromaSubsampling_422 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanApertureHeightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanApertureHorizontalOffsetKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanApertureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanApertureVerticalOffsetKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CleanApertureWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGRect CleanRect { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimariesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_DCI_P3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_ITU_R_2020 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_P22 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_P3_D65 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayDimensionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayHeightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGSize DisplaySize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DisplayWidthKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGSize EncodedSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldCountKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetailKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetailSpatialFirstLineEarly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetailSpatialFirstLineLate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetailTemporalBottomFirst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FieldDetailTemporalTopFirst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GammaLevelKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsFlipped { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovieTimeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NonPropagatedAttachmentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelAspectRatioHorizontalSpacingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelAspectRatioKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelAspectRatioVerticalSpacingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PreferredCleanApertureKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropagatedAttachmentsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeScaleKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TimeValueKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunctionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_ITU_R_2020 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_ITU_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_240M_1995 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_428_1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_UseGamma { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrixKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_DCI_P3 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_2020 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_601_4 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_ITU_R_709_2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_P3_D65 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString YCbCrMatrix_SMPTE_240M_1995 { get; }</span>
}
</pre>
</div> <!-- end type CVImageBuffer -->
<div> <!-- start type CVOptionFlags -->
<h3>New Type CoreVideo.CVOptionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVOptionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type CVOptionFlags -->
<div> <!-- start type CVPixelBuffer -->
<h3>New Type CoreVideo.CVPixelBuffer</h3>
<pre class='added' data-is-non-breaking="">
public class CVPixelBuffer : CoreVideo.CVImageBuffer, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBuffer (nint width, nint height, CVPixelFormatType pixelFormat);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBuffer (nint width, nint height, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BytesPerRowAlignmentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CGBitmapContextCompatibilityKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CGImageCompatibilityKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint DataSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedPixelsBottomKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedPixelsLeftKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedPixelsRightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedPixelsTopKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HeightKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IOSurfacePropertiesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsPlanar { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MemoryAllocatorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MetalCompatibilityKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OpenGLCompatibilityKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CVPixelFormatType PixelFormatType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormatTypeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaneAlignmentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint PlaneCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint Width { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString WidthKey { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (nint width, nint height, CVPixelFormatType pixelFormatType, byte[] data, nint bytesPerRow, CVPixelBufferAttributes pixelBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (nint width, nint height, CVPixelFormatType pixelFormatType, byte[] data, nint bytesPerRow, CVPixelBufferAttributes pixelBufferAttributes, CVReturn status);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (nint width, nint height, CVPixelFormatType pixelFormatType, byte[][] planes, nint[] planeWidths, nint[] planeHeights, nint[] planeBytesPerRow, CVPixelBufferAttributes pixelBufferAttributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CVPixelBuffer Create (nint width, nint height, CVPixelFormatType pixelFormatType, byte[][] planes, nint[] planeWidths, nint[] planeHeights, nint[] planeBytesPerRow, CVPixelBufferAttributes pixelBufferAttributes, CVReturn status);</span>
	<span class='added added-method ' data-is-non-breaking="">public CVReturn FillExtendedPixels ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary GetAttributes (Foundation.NSDictionary[] attributes);</span>
	<span class='added added-method ' data-is-non-breaking="">public IntPtr GetBaseAddress (nint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public nint GetBytesPerRowOfPlane (nint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public void GetExtendedPixels (uint extraColumnsOnLeft, uint extraColumnsOnRight, uint extraRowsOnTop, uint extraRowsOnBottom);</span>
	<span class='added added-method ' data-is-non-breaking="">public nint GetHeightOfPlane (nint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public static nint GetTypeID ();</span>
	<span class='added added-method ' data-is-non-breaking="">public nint GetWidthOfPlane (nint planeIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public CVReturn Lock (CVPixelBufferLock lockFlags);</span>
	<span class='added added-method ' data-is-non-breaking="">public CVReturn Unlock (CVPixelBufferLock unlockFlags);</span>
}
</pre>
</div> <!-- end type CVPixelBuffer -->
<div> <!-- start type CVPixelBufferAttributes -->
<h3>New Type CoreVideo.CVPixelBufferAttributes</h3>
<pre class='added' data-is-non-breaking="">
public class CVPixelBufferAttributes : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferAttributes ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferAttributes (Foundation.NSDictionary dictionary);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferAttributes (CVPixelFormatType pixelFormatType, nint width, nint height);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? AllocateWithIOSurface { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? BytesPerRowAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? CGBitmapContextCompatibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? CGImageCompatibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ExtendedPixelsBottom { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ExtendedPixelsLeft { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ExtendedPixelsRight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ExtendedPixelsTop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreFoundation.CFAllocator MemoryAllocator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? OpenGLCompatibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CVPixelFormatType? PixelFormatType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? PlaneAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Width { get; set; }</span>
}
</pre>
</div> <!-- end type CVPixelBufferAttributes -->
<div> <!-- start type CVPixelBufferLock -->
<h3>New Type CoreVideo.CVPixelBufferLock</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CVPixelBufferLock {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnly = 1,</span>
}
</pre>
</div> <!-- end type CVPixelBufferLock -->
<div> <!-- start type CVPixelBufferPool -->
<h3>New Type CoreVideo.CVPixelBufferPool</h3>
<pre class='added' data-is-non-breaking="">
public class CVPixelBufferPool : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPool (CVPixelBufferPoolSettings settings, CVPixelBufferAttributes pixelBufferAttributes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPool (Foundation.NSDictionary poolAttributes, Foundation.NSDictionary pixelBufferAttributes);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MaximumBufferAgeKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MinimumBufferCountKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary PixelBufferAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CVPixelBufferPoolSettings Settings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint TypeID { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public CVPixelBuffer CreatePixelBuffer ();</span>
	<span class='added added-method ' data-is-non-breaking="">public CVPixelBuffer CreatePixelBuffer (CVPixelBufferPoolAllocationSettings allocationSettings, CVReturn error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Flush (CVPixelBufferPoolFlushFlags options);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~CVPixelBufferPool ();</span>
}
</pre>
</div> <!-- end type CVPixelBufferPool -->
<div> <!-- start type CVPixelBufferPoolAllocationSettings -->
<h3>New Type CoreVideo.CVPixelBufferPoolAllocationSettings</h3>
<pre class='added' data-is-non-breaking="">
public class CVPixelBufferPoolAllocationSettings : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPoolAllocationSettings ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPoolAllocationSettings (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int? Threshold { get; set; }</span>
}
</pre>
</div> <!-- end type CVPixelBufferPoolAllocationSettings -->
<div> <!-- start type CVPixelBufferPoolFlushFlags -->
<h3>New Type CoreVideo.CVPixelBufferPoolFlushFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVPixelBufferPoolFlushFlags {
	<span class='added added-field ' data-is-non-breaking="">FlushExcessBuffers = 1,</span>
}
</pre>
</div> <!-- end type CVPixelBufferPoolFlushFlags -->
<div> <!-- start type CVPixelBufferPoolSettings -->
<h3>New Type CoreVideo.CVPixelBufferPoolSettings</h3>
<pre class='added' data-is-non-breaking="">
public class CVPixelBufferPoolSettings : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPoolSettings ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CVPixelBufferPoolSettings (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public double? MaximumBufferAgeInSeconds { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? MinimumBufferCount { get; set; }</span>
}
</pre>
</div> <!-- end type CVPixelBufferPoolSettings -->
<div> <!-- start type CVPixelFormatDescription -->
<h3>New Type CoreVideo.CVPixelFormatDescription</h3>
<pre class='added' data-is-non-breaking="">
public static class CVPixelFormatDescription {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BitsPerBlockKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BlackBlockKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BlockHeightKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BlockHorizontalAlignmentKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BlockVerticalAlignmentKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BlockWidthKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString CGBitmapContextCompatibilityKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString CGBitmapInfoKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString CGImageCompatibilityKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString CodecTypeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ComponentRangeFullRangeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ComponentRangeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ComponentRangeVideoRangeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ComponentRangeWideRangeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ConstantKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ContainsRgb;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString ContainsYCbCr;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString FillExtendedPixelsCallbackKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString FourCCKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString HorizontalSubsamplingKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString NameKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString OpenGLCompatibilityKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString OpenGLFormatKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString OpenGLInternalFormatKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString OpenGLTypeKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString PlanesKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString QDCompatibilityKey;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString VerticalSubsamplingKey;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSNumber[] AllTypes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary Create (CVPixelFormatType pixelFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Register (Foundation.NSDictionary description, CVPixelFormatType pixelFormat);</span>
}
</pre>
</div> <!-- end type CVPixelFormatDescription -->
<div> <!-- start type CVPlanarComponentInfo -->
<h3>New Type CoreVideo.CVPlanarComponentInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct CVPlanarComponentInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public int Offset;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint RowBytes;</span>
}
</pre>
</div> <!-- end type CVPlanarComponentInfo -->
<div> <!-- start type CVPlanarPixelBufferInfo -->
<h3>New Type CoreVideo.CVPlanarPixelBufferInfo</h3>
<pre class='added' data-is-non-breaking="">
public struct CVPlanarPixelBufferInfo {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo[] ComponentInfo;</span>
}
</pre>
</div> <!-- end type CVPlanarPixelBufferInfo -->
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
<div> <!-- start type CVPlanarPixelBufferInfo_YCbCrPlanar -->
<h3>New Type CoreVideo.CVPlanarPixelBufferInfo_YCbCrPlanar</h3>
<pre class='added' data-is-non-breaking="">
public struct CVPlanarPixelBufferInfo_YCbCrPlanar {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoCb;</span>
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoCr;</span>
	<span class='added added-field ' data-is-non-breaking="">public CVPlanarComponentInfo ComponentInfoY;</span>
}
</pre>
</div> <!-- end type CVPlanarPixelBufferInfo_YCbCrPlanar -->
<div> <!-- start type CVReturn -->
<h3>New Type CoreVideo.CVReturn</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVReturn {
	<span class='added added-field ' data-is-non-breaking="">AllocationFailed = -6662,</span>
	<span class='added added-field ' data-is-non-breaking="">DisplayLinkAlreadyRunning = -6671,</span>
	<span class='added added-field ' data-is-non-breaking="">DisplayLinkCallbacksNotSet = -6673,</span>
	<span class='added added-field ' data-is-non-breaking="">DisplayLinkNotRunning = -6672,</span>
	<span class='added added-field ' data-is-non-breaking="">Error = -6660,</span>
	<span class='added added-field ' data-is-non-breaking="">First = -6660,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = -6661,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDisplay = -6670,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPixelBufferAttributes = -6682,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPixelFormat = -6680,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPoolAttributes = -6691,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSize = -6681,</span>
	<span class='added added-field ' data-is-non-breaking="">Last = -6699,</span>
	<span class='added added-field ' data-is-non-breaking="">PixelBufferNotMetalCompatible = -6684,</span>
	<span class='added added-field ' data-is-non-breaking="">PixelBufferNotOpenGLCompatible = -6683,</span>
	<span class='added added-field ' data-is-non-breaking="">PoolAllocationFailed = -6690,</span>
	<span class='added added-field ' data-is-non-breaking="">Retry = -6692,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = -6663,</span>
	<span class='added added-field ' data-is-non-breaking="">WouldExceedAllocationThreshold = -6689,</span>
}
</pre>
</div> <!-- end type CVReturn -->
<div> <!-- start type CVSMPTETime -->
<h3>New Type CoreVideo.CVSMPTETime</h3>
<pre class='added' data-is-non-breaking="">
public struct CVSMPTETime {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint Counter;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Flags;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Frames;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Hours;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Minutes;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Seconds;</span>
	<span class='added added-field ' data-is-non-breaking="">public short SubframeDivisor;</span>
	<span class='added added-field ' data-is-non-breaking="">public short Subframes;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Type;</span>
}
</pre>
</div> <!-- end type CVSMPTETime -->
<div> <!-- start type CVSMPTETimeFlags -->
<h3>New Type CoreVideo.CVSMPTETimeFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CVSMPTETimeFlags {
	<span class='added added-field ' data-is-non-breaking="">Running = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Valid = 1,</span>
}
</pre>
</div> <!-- end type CVSMPTETimeFlags -->
<div> <!-- start type CVSMPTETimeType -->
<h3>New Type CoreVideo.CVSMPTETimeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CVSMPTETimeType {
	<span class='added added-field ' data-is-non-breaking="">Type24 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Type25 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Type2997 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Type2997Drop = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Type30 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Type30Drop = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Type5994 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Type60 = 6,</span>
}
</pre>
</div> <!-- end type CVSMPTETimeType -->
<div> <!-- start type CVTime -->
<h3>New Type CoreVideo.CVTime</h3>
<pre class='added' data-is-non-breaking="">
public struct CVTime {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CVTimeFlags TimeFlags;</span>
	<span class='added added-field ' data-is-non-breaking="">public long TimeScale;</span>
	<span class='added added-field ' data-is-non-breaking="">public long TimeValue;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int Flags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CVTime IndefiniteTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CVTime ZeroTime { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object other);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetCurrentHostTime ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static double GetHostClockFrequency ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetHostClockMinimumTimeDelta ();</span>
}
</pre>
</div> <!-- end type CVTime -->
<div> <!-- start type CVTimeFlags -->
<h3>New Type CoreVideo.CVTimeFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CVTimeFlags {
	<span class='added added-field ' data-is-non-breaking="">IsIndefinite = 1,</span>
}
</pre>
</div> <!-- end type CVTimeFlags -->
<div> <!-- start type CVTimeStamp -->
<h3>New Type CoreVideo.CVTimeStamp</h3>
<pre class='added' data-is-non-breaking="">
public struct CVTimeStamp {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ulong Flags;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong HostTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public double RateScalar;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong Reserved;</span>
	<span class='added added-field ' data-is-non-breaking="">public CVSMPTETime SMPTETime;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Version;</span>
	<span class='added added-field ' data-is-non-breaking="">public long VideoRefreshPeriod;</span>
	<span class='added added-field ' data-is-non-breaking="">public long VideoTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public int VideoTimeScale;</span>
}
</pre>
</div> <!-- end type CVTimeStamp -->
<div> <!-- start type CVTimeStampFlags -->
<h3>New Type CoreVideo.CVTimeStampFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CVTimeStampFlags {
	<span class='added added-field ' data-is-non-breaking="">BottomField = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">HostTimeValid = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">IsInterlaced = 196608,</span>
	<span class='added added-field ' data-is-non-breaking="">RateScalarValid = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SMPTETimeValid = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">TopField = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoHostTimeValid = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoRefreshPeriodValid = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoTimeValid = 1,</span>
}
</pre>
</div> <!-- end type CVTimeStampFlags -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace EventKit --> <div> 
<h2>Namespace EventKit</h2>
<!-- start type EKAlarm --> <div>
<h3>Type Changed: EventKit.EKAlarm</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the static methods FromDate or FromTimeInterval to create alarms")]
	public EKAlarm ();</span>
</div></pre>

</div> <!-- end type EKAlarm -->

</div> <!-- end namespace EventKit -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSArray --> <div>
<h3>Type Changed: Foundation.NSArray</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSArray FromUrl (NSUrl url, NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Write (NSUrl url, NSError error);</span>
</pre>
</div>

</div> <!-- end type NSArray -->
<!-- start type NSCocoaError --> <div>
<h3>Type Changed: Foundation.NSCocoaError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CoderInvalidValueError = 4866,</span>
</pre>
</div>

</div> <!-- end type NSCocoaError -->
<!-- start type NSDateComponentsFormatter --> <div>
<h3>Type Changed: Foundation.NSDateComponentsFormatter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ReferenceDate { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDateComponentsFormatter -->
<!-- start type NSDateFormatter --> <div>
<h3>Type Changed: Foundation.NSDateFormatter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFormattingContext FormattingContext { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSDateFormatter -->
<!-- start type NSDictionary --> <div>
<h3>Type Changed: Foundation.NSDictionary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDictionary (NSUrl url, NSError error);</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;NSString,Foundation.NSObject&gt; FromUrl (NSUrl url, NSError error);</span>
</pre>
</div>

</div> <!-- end type NSDictionary -->
<!-- start type NSDimension --> <div>
<h3>Type Changed: Foundation.NSDimension</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDimension (string symbol);</span>
</pre>
</div>

</div> <!-- end type NSDimension -->
<!-- start type NSError --> <div>
<h3>Type Changed: Foundation.NSError</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DebugDescriptionErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString LocalizedFailureErrorKey { get; }</span>
</pre>
</div>

</div> <!-- end type NSError -->
<!-- start type NSIso8601DateFormatOptions --> <div>
<h3>Type Changed: Foundation.NSIso8601DateFormatOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FractionalSeconds = 2048,</span>
</pre>
</div>

</div> <!-- end type NSIso8601DateFormatOptions -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSItemProvider (INSItemProviderWriting object);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanLoadObject (ObjCRuntime.Class aClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool CanLoadObject (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetRegisteredTypeIdentifiers (NSItemProviderFileOptions fileOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool HasConformingRepresentation (string typeIdentifier, NSItemProviderFileOptions fileOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadDataRepresentation (string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSData&gt; LoadDataRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadFileRepresentation (string typeIdentifier, System.Action&lt;NSUrl,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrl&gt; LoadFileRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrl&gt; LoadFileRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadInPlaceFileRepresentation (string typeIdentifier, LoadInPlaceFileRepresentationHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;LoadInPlaceResult&gt; LoadInPlaceFileRepresentationAsync (string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;LoadInPlaceResult&gt; LoadInPlaceFileRepresentationAsync (string typeIdentifier, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress LoadObject (ObjCRuntime.Class aClass, System.Action&lt;INSItemProviderReading,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public NSProgress LoadObject (System.Type type, System.Action&lt;INSItemProviderReading,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (ObjCRuntime.Class aClass);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (System.Type type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (ObjCRuntime.Class aClass, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;INSItemProviderReading&gt; LoadObjectAsync (System.Type type, NSProgress result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterDataRepresentation (string typeIdentifier, NSItemProviderRepresentationVisibility visibility, RegisterDataRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterFileRepresentation (string typeIdentifier, NSItemProviderFileOptions fileOptions, NSItemProviderRepresentationVisibility visibility, RegisterFileRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterObject (INSItemProviderWriting object, NSItemProviderRepresentationVisibility visibility);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterObject (ObjCRuntime.Class aClass, NSItemProviderRepresentationVisibility visibility, RegisterObjectRepresentationLoadHandler loadHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RegisterObject (System.Type type, NSItemProviderRepresentationVisibility visibility, RegisterObjectRepresentationLoadHandler loadHandler);</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSJsonWritingOptions --> <div>
<h3>Type Changed: Foundation.NSJsonWritingOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SortedKeys = 2,</span>
</pre>
</div>

</div> <!-- end type NSJsonWritingOptions -->
<!-- start type NSLinguisticTagger --> <div>
<h3>Type Changed: Foundation.NSLinguisticTagger</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DominantLanguage { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateTags (NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, LinguisticTagEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EnumerateTags (string str, NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSOrthography orthography, LinguisticTagEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetAvailableTagSchemes (NSLinguisticTaggerUnit unit, string language);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetDominantLanguage (string str);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetTag (uint charIndex, NSLinguisticTaggerUnit unit, string scheme, NSRange tokenRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetTag (string str, uint charIndex, NSLinguisticTaggerUnit unit, string scheme, NSOrthography orthography, NSRange tokenRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string[] GetTags (NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSValue[] tokenRanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetTags (string str, NSRange range, NSLinguisticTaggerUnit unit, string scheme, NSLinguisticTaggerOptions options, NSOrthography orthography, NSValue[] tokenRanges);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetTokenRange (uint charIndex, NSLinguisticTaggerUnit unit);</span>
</pre>
</div>

</div> <!-- end type NSLinguisticTagger -->
<!-- start type NSProgress --> <div>
<h3>Type Changed: Foundation.NSProgress</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public nint? EstimatedTimeRemaining { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FileCompletedCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FileOperationKind { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? FileTotalCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrl FileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Finished { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public nint? Throughput { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformAsCurrent (long unitCount, System.Action work);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PerformAsCurrentAsync (long unitCount);</span>
</pre>
</div>

</div> <!-- end type NSProgress -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiers { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSString FromItemProviderData (NSData itemProviderData, string typeIdentifier, NSError outError);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSTextCheckingResult --> <div>
<h3>Type Changed: Foundation.NSTextCheckingResult</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetRange (string name);</span>
</pre>
</div>

</div> <!-- end type NSTextCheckingResult -->
<!-- start type NSUnit --> <div>
<h3>Type Changed: Foundation.NSUnit</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string)")]
	public NSUnit ();</span>
</div></pre>

</div> <!-- end type NSUnit -->
<!-- start type NSUnitAcceleration --> <div>
<h3>Type Changed: Foundation.NSUnitAcceleration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAcceleration ();</span>
</div></pre>

</div> <!-- end type NSUnitAcceleration -->
<!-- start type NSUnitAngle --> <div>
<h3>Type Changed: Foundation.NSUnitAngle</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitAngle ();</span>
</div></pre>

</div> <!-- end type NSUnitAngle -->
<!-- start type NSUnitArea --> <div>
<h3>Type Changed: Foundation.NSUnitArea</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitArea ();</span>
</div></pre>

</div> <!-- end type NSUnitArea -->
<!-- start type NSUnitConcentrationMass --> <div>
<h3>Type Changed: Foundation.NSUnitConcentrationMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitConcentrationMass ();</span>
</div></pre>

</div> <!-- end type NSUnitConcentrationMass -->
<!-- start type NSUnitDispersion --> <div>
<h3>Type Changed: Foundation.NSUnitDispersion</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDispersion ();</span>
</div></pre>

</div> <!-- end type NSUnitDispersion -->
<!-- start type NSUnitDuration --> <div>
<h3>Type Changed: Foundation.NSUnitDuration</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitDuration ();</span>
</div></pre>

</div> <!-- end type NSUnitDuration -->
<!-- start type NSUnitElectricCharge --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCharge</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCharge ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCharge -->
<!-- start type NSUnitElectricCurrent --> <div>
<h3>Type Changed: Foundation.NSUnitElectricCurrent</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricCurrent ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricCurrent -->
<!-- start type NSUnitElectricPotentialDifference --> <div>
<h3>Type Changed: Foundation.NSUnitElectricPotentialDifference</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricPotentialDifference ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricPotentialDifference -->
<!-- start type NSUnitElectricResistance --> <div>
<h3>Type Changed: Foundation.NSUnitElectricResistance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitElectricResistance ();</span>
</div></pre>

</div> <!-- end type NSUnitElectricResistance -->
<!-- start type NSUnitEnergy --> <div>
<h3>Type Changed: Foundation.NSUnitEnergy</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitEnergy ();</span>
</div></pre>

</div> <!-- end type NSUnitEnergy -->
<!-- start type NSUnitFrequency --> <div>
<h3>Type Changed: Foundation.NSUnitFrequency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFrequency ();</span>
</div></pre>

</div> <!-- end type NSUnitFrequency -->
<!-- start type NSUnitFuelEfficiency --> <div>
<h3>Type Changed: Foundation.NSUnitFuelEfficiency</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitFuelEfficiency ();</span>
</div></pre>

</div> <!-- end type NSUnitFuelEfficiency -->
<!-- start type NSUnitIlluminance --> <div>
<h3>Type Changed: Foundation.NSUnitIlluminance</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitIlluminance ();</span>
</div></pre>

</div> <!-- end type NSUnitIlluminance -->
<!-- start type NSUnitLength --> <div>
<h3>Type Changed: Foundation.NSUnitLength</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitLength ();</span>
</div></pre>

</div> <!-- end type NSUnitLength -->
<!-- start type NSUnitMass --> <div>
<h3>Type Changed: Foundation.NSUnitMass</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitMass ();</span>
</div></pre>

</div> <!-- end type NSUnitMass -->
<!-- start type NSUnitPower --> <div>
<h3>Type Changed: Foundation.NSUnitPower</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPower ();</span>
</div></pre>

</div> <!-- end type NSUnitPower -->
<!-- start type NSUnitPressure --> <div>
<h3>Type Changed: Foundation.NSUnitPressure</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitPressure ();</span>
</div></pre>

</div> <!-- end type NSUnitPressure -->
<!-- start type NSUnitSpeed --> <div>
<h3>Type Changed: Foundation.NSUnitSpeed</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitSpeed ();</span>
</div></pre>

</div> <!-- end type NSUnitSpeed -->
<!-- start type NSUnitVolume --> <div>
<h3>Type Changed: Foundation.NSUnitVolume</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use .ctor(string, NSUnitConverter) or any of the static properties.")]
	public NSUnitVolume ();</span>
</div></pre>

</div> <!-- end type NSUnitVolume -->
<!-- start type NSUrl --> <div>
<h3>Type Changed: Foundation.NSUrl</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string[] ReadableTypeIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeIsEncryptedKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeIsRootFileSystemKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsAccessPermissionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsCompressionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsExclusiveRenamingKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsFileCloningKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsImmutableFilesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString VolumeSupportsSwapRenamingKey { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl FromItemProviderData (NSData itemProviderData, string typeIdentifier, NSError outError);</span>
</pre>
</div>

</div> <!-- end type NSUrl -->
<!-- start type NSUrlComponents --> <div>
<h3>Type Changed: Foundation.NSUrlComponents</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlQueryItem[] PercentEncodedQueryItems { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUrlComponents -->
<!-- start type NSUrlSessionConfiguration --> <div>
<h3>Type Changed: Foundation.NSUrlSessionConfiguration</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WaitsForConnectivity { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionConfiguration -->
<!-- start type NSUrlSessionDataTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionDataTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionDataTask -->
<!-- start type NSUrlSessionDownloadTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionDownloadTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionDownloadTask -->
<!-- start type NSUrlSessionStreamTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionStreamTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionStreamTask -->
<!-- start type NSUrlSessionTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual long CountOfBytesClientExpectsToReceive { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long CountOfBytesClientExpectsToSend { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate EarliestBeginDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSProgress Progress { get; }</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTask -->
<!-- start type NSUrlSessionTaskDelegate --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TaskIsWaitingForConnectivity (NSUrlSession session, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginDelayedRequest (NSUrlSession session, NSUrlSessionTask task, NSUrlRequest request, System.Action&lt;NSUrlSessionDelayedRequestDisposition,Foundation.NSUrlRequest&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate -->
<!-- start type NSUrlSessionTaskDelegate_Extensions --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void TaskIsWaitingForConnectivity (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginDelayedRequest (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlRequest request, System.Action&lt;NSUrlSessionDelayedRequestDisposition,Foundation.NSUrlRequest&gt; completionHandler);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate_Extensions -->
<!-- start type NSUrlSessionUploadTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionUploadTask</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSProgressReporting</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionUploadTask -->
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrl ReferrerUrl { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSUserActivity -->
<!-- start type NSValue --> <div>
<h3>Type Changed: Foundation.NSValue</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.NSDirectionalEdgeInsets DirectionalEdgeInsetsValue { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSValue FromDirectionalEdgeInsets (UIKit.NSDirectionalEdgeInsets insets);</span>
</pre>
</div>

</div> <!-- end type NSValue -->
<div> <!-- start type INSItemProviderReading -->
<h3>New Type Foundation.INSItemProviderReading</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderReading : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderReading -->
<div> <!-- start type INSItemProviderWriting -->
<h3>New Type Foundation.INSItemProviderWriting</h3>
<pre class='added' data-is-non-breaking="">
public interface INSItemProviderWriting : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSItemProviderWriting -->
<div> <!-- start type ItemProviderDataCompletionHandler -->
<h3>New Type Foundation.ItemProviderDataCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate ItemProviderDataCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ItemProviderDataCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSData data, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSData data, NSError error);</span>
}
</pre>
</div> <!-- end type ItemProviderDataCompletionHandler -->
<div> <!-- start type LinguisticTagEnumerator -->
<h3>New Type Foundation.LinguisticTagEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate LinguisticTagEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LinguisticTagEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string tag, NSRange tokenRange, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string tag, NSRange tokenRange, bool stop);</span>
}
</pre>
</div> <!-- end type LinguisticTagEnumerator -->
<div> <!-- start type LoadInPlaceFileRepresentationHandler -->
<h3>New Type Foundation.LoadInPlaceFileRepresentationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate LoadInPlaceFileRepresentationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LoadInPlaceFileRepresentationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSUrl fileUrl, bool isInPlace, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSUrl fileUrl, bool isInPlace, NSError error);</span>
}
</pre>
</div> <!-- end type LoadInPlaceFileRepresentationHandler -->
<div> <!-- start type LoadInPlaceResult -->
<h3>New Type Foundation.LoadInPlaceResult</h3>
<pre class='added' data-is-non-breaking="">
public class LoadInPlaceResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LoadInPlaceResult (NSUrl fileUrl, bool isInPlace);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NSUrl FileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsInPlace { get; set; }</span>
}
</pre>
</div> <!-- end type LoadInPlaceResult -->
<div> <!-- start type NSItemProviderFileOptions -->
<h3>New Type Foundation.NSItemProviderFileOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSItemProviderFileOptions {
	<span class='added added-field ' data-is-non-breaking="">OpenInPlace = 1,</span>
}
</pre>
</div> <!-- end type NSItemProviderFileOptions -->
<div> <!-- start type NSItemProviderRepresentationVisibility -->
<h3>New Type Foundation.NSItemProviderRepresentationVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSItemProviderRepresentationVisibility {
	<span class='added added-field ' data-is-non-breaking="">All = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Group = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">OwnProcess = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Team = 1,</span>
}
</pre>
</div> <!-- end type NSItemProviderRepresentationVisibility -->
<div> <!-- start type NSItemProviderWriting_Extensions -->
<h3>New Type Foundation.NSItemProviderWriting_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemProviderWriting_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSItemProviderRepresentationVisibility GetItemProviderVisibility (INSItemProviderWriting This, string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string[] GetWritableTypeIdentifiersForItemProvider (INSItemProviderWriting This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSProgress LoadData (INSItemProviderWriting This, string typeIdentifier, System.Action&lt;NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (INSItemProviderWriting This, string typeIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSData&gt; LoadDataAsync (INSItemProviderWriting This, string typeIdentifier, NSProgress result);</span>
}
</pre>
</div> <!-- end type NSItemProviderWriting_Extensions -->
<div> <!-- start type NSLinguisticTaggerUnit -->
<h3>New Type Foundation.NSLinguisticTaggerUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSLinguisticTaggerUnit {
	<span class='added added-field ' data-is-non-breaking="">Document = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Paragraph = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Sentence = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Word = 0,</span>
}
</pre>
</div> <!-- end type NSLinguisticTaggerUnit -->
<div> <!-- start type NSUrlSessionDelayedRequestDisposition -->
<h3>New Type Foundation.NSUrlSessionDelayedRequestDisposition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSUrlSessionDelayedRequestDisposition {
	<span class='added added-field ' data-is-non-breaking="">Cancel = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ContinueLoading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UseNewRequest = 1,</span>
}
</pre>
</div> <!-- end type NSUrlSessionDelayedRequestDisposition -->
<div> <!-- start type NSUrlSessionMultipathServiceType -->
<h3>New Type Foundation.NSUrlSessionMultipathServiceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSUrlSessionMultipathServiceType {
	<span class='added added-field ' data-is-non-breaking="">Aggregate = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Handover = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Interactive = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type NSUrlSessionMultipathServiceType -->
<div> <!-- start type RegisterDataRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterDataRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterDataRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterDataRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ItemProviderDataCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (ItemProviderDataCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterDataRepresentationLoadHandler -->
<div> <!-- start type RegisterFileRepresentationCompletionHandler -->
<h3>New Type Foundation.RegisterFileRepresentationCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterFileRepresentationCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterFileRepresentationCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSUrl fileUrl, bool coordinated, NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (NSUrl fileUrl, bool coordinated, NSError error);</span>
}
</pre>
</div> <!-- end type RegisterFileRepresentationCompletionHandler -->
<div> <!-- start type RegisterFileRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterFileRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterFileRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterFileRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (RegisterFileRepresentationCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (RegisterFileRepresentationCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterFileRepresentationLoadHandler -->
<div> <!-- start type RegisterObjectRepresentationCompletionHandler -->
<h3>New Type Foundation.RegisterObjectRepresentationCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterObjectRepresentationCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterObjectRepresentationCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (INSItemProviderWriting object, NSError error, System.AsyncCallback callback, object _object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (INSItemProviderWriting object, NSError error);</span>
}
</pre>
</div> <!-- end type RegisterObjectRepresentationCompletionHandler -->
<div> <!-- start type RegisterObjectRepresentationLoadHandler -->
<h3>New Type Foundation.RegisterObjectRepresentationLoadHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate RegisterObjectRepresentationLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RegisterObjectRepresentationLoadHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (RegisterObjectRepresentationCompletionHandler completionHandler, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSProgress Invoke (RegisterObjectRepresentationCompletionHandler completionHandler);</span>
}
</pre>
</div> <!-- end type RegisterObjectRepresentationLoadHandler -->

</div> <!-- end namespace Foundation -->
<!-- start namespace HomeKit --> <div> 
<h2>Namespace HomeKit</h2>
<!-- start type HMAccessory --> <div>
<h3>Type Changed: HomeKit.HMAccessory</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FirmwareVersion { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Model { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessoryProfile[] Profiles { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidAddProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryProfileEventArgs&gt; DidRemoveProfile;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryFirmwareVersionEventArgs&gt; DidUpdateFirmwareVersion;</span>
</pre>
</div>

</div> <!-- end type HMAccessory -->
<!-- start type HMAccessoryDelegate --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveProfile (HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFirmwareVersion (HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate -->
<!-- start type HMAccessoryDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMAccessoryDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveProfile (IHMAccessoryDelegate This, HMAccessory accessory, HMAccessoryProfile profile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateFirmwareVersion (IHMAccessoryDelegate This, HMAccessory accessory, string firmwareVersion);</span>
</pre>
</div>

</div> <!-- end type HMAccessoryDelegate_Extensions -->
<!-- start type HMCharacteristicEvent --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicEvent</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual HMCharacteristic Characteristic { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public virtual Foundation.INSCopying TriggerValue { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type HMCharacteristicEvent -->
<!-- start type HMCharacteristicType --> <div>
<h3>Type Changed: HomeKit.HMCharacteristicType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ColorTemperature = 115,</span>
</pre>
</div>

</div> <!-- end type HMCharacteristicType -->
<!-- start type HMError --> <div>
<h3>Type Changed: HomeKit.HMError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">IncompatibleHomeHub = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">NoHomeHub = 91,</span>
</pre>
</div>

</div> <!-- end type HMError -->
<!-- start type HMEvent --> <div>
<h3>Type Changed: HomeKit.HMEvent</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsSupported (HMHome home);</span>
</pre>
</div>

</div> <!-- end type HMEvent -->
<!-- start type HMEventTrigger --> <div>
<h3>Type Changed: HomeKit.HMEventTrigger</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEvent[] EndEvents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ExecuteOnce { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents[] Recurrences { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEventTriggerActivationState TriggerActivationState { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTrigger (HMPresenceEvent presenceEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringAfterSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBeforeSignificantEvent (HMSignificantTimeEvent significantEvent);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenDates (Foundation.NSDateComponents firstDateComponents, Foundation.NSDateComponents secondDateComponents);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBetweenSignificantEvent (HMSignificantTimeEvent firstSignificantEvent, HMSignificantTimeEvent secondSignificantEvent);</span>
</pre>
</div>

</div> <!-- end type HMEventTrigger -->
<!-- start type HMHome --> <div>
<h3>Type Changed: HomeKit.HMHome</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMHomeHubState HomeHubState { get; }</span>
</pre>
</div>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateAccessControlForCurrentUser;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeHubStateEventArgs&gt; DidUpdateHomeHubState;</span>
</pre>
</div>

</div> <!-- end type HMHome -->
<!-- start type HMHomeDelegate --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateAccessControlForCurrentUser (HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateHomeHubState (HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate -->
<!-- start type HMHomeDelegate_Extensions --> <div>
<h3>Type Changed: HomeKit.HMHomeDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateAccessControlForCurrentUser (IHMHomeDelegate This, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateHomeHubState (IHMHomeDelegate This, HMHome home, HMHomeHubState homeHubState);</span>
</pre>
</div>

</div> <!-- end type HMHomeDelegate_Extensions -->
<!-- start type HMLocationEvent --> <div>
<h3>Type Changed: HomeKit.HMLocationEvent</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSMutableCopying</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual CoreLocation.CLRegion Region { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type HMLocationEvent -->
<div> <!-- start type HMAccessoryFirmwareVersionEventArgs -->
<h3>New Type HomeKit.HMAccessoryFirmwareVersionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryFirmwareVersionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryFirmwareVersionEventArgs (string firmwareVersion);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FirmwareVersion { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryFirmwareVersionEventArgs -->
<div> <!-- start type HMAccessoryProfileEventArgs -->
<h3>New Type HomeKit.HMAccessoryProfileEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryProfileEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryProfileEventArgs (HMAccessoryProfile profile);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessoryProfile Profile { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryProfileEventArgs -->
<div> <!-- start type HMCalendarEvent -->
<h3>New Type HomeKit.HMCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCalendarEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents FireDateComponents { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCalendarEvent -->
<div> <!-- start type HMCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicThresholdRangeEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMNumberRange ThresholdRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMDurationEvent -->
<h3>New Type HomeKit.HMDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMDurationEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMDurationEvent -->
<div> <!-- start type HMEventTriggerActivationState -->
<h3>New Type HomeKit.HMEventTriggerActivationState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMEventTriggerActivationState {
	<span class='added added-field ' data-is-non-breaking="">Disabled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoCompatibleHomeHub = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoHomeHub = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">DisabledNoLocationServicesAuthorization = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Enabled = 4,</span>
}
</pre>
</div> <!-- end type HMEventTriggerActivationState -->
<div> <!-- start type HMHomeHubState -->
<h3>New Type HomeKit.HMHomeHubState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMHomeHubState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAvailable = 0,</span>
}
</pre>
</div> <!-- end type HMHomeHubState -->
<div> <!-- start type HMHomeHubStateEventArgs -->
<h3>New Type HomeKit.HMHomeHubStateEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeHubStateEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeHubStateEventArgs (HMHomeHubState homeHubState);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMHomeHubState HomeHubState { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeHubStateEventArgs -->
<div> <!-- start type HMMutableCalendarEvent -->
<h3>New Type HomeKit.HMMutableCalendarEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCalendarEvent : HomeKit.HMCalendarEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCalendarEvent (Foundation.NSDateComponents fireDateComponents);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCalendarEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents FireDateComponents { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCalendarEvent -->
<div> <!-- start type HMMutableCharacteristicEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicEvent : HomeKit.HMCharacteristicEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicEvent (HMCharacteristic characteristic, Foundation.INSCopying triggerValue);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.INSCopying TriggerValue { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicEvent -->
<div> <!-- start type HMMutableCharacteristicThresholdRangeEvent -->
<h3>New Type HomeKit.HMMutableCharacteristicThresholdRangeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableCharacteristicThresholdRangeEvent : HomeKit.HMCharacteristicThresholdRangeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableCharacteristicThresholdRangeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableCharacteristicThresholdRangeEvent (HMCharacteristic characteristic, HMNumberRange thresholdRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override HMNumberRange ThresholdRange { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableCharacteristicThresholdRangeEvent -->
<div> <!-- start type HMMutableDurationEvent -->
<h3>New Type HomeKit.HMMutableDurationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableDurationEvent : HomeKit.HMDurationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableDurationEvent (double duration);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableDurationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override double Duration { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableDurationEvent -->
<div> <!-- start type HMMutableLocationEvent -->
<h3>New Type HomeKit.HMMutableLocationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableLocationEvent : HomeKit.HMLocationEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableLocationEvent (CoreLocation.CLRegion region);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableLocationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CoreLocation.CLRegion Region { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableLocationEvent -->
<div> <!-- start type HMMutablePresenceEvent -->
<h3>New Type HomeKit.HMMutablePresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutablePresenceEvent : HomeKit.HMPresenceEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutablePresenceEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventType PresenceEventType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventUserType PresenceUserType { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutablePresenceEvent -->
<div> <!-- start type HMMutableSignificantTimeEvent -->
<h3>New Type HomeKit.HMMutableSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMMutableSignificantTimeEvent : HomeKit.HMSignificantTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMMutableSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMMutableSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
}
</pre>
</div> <!-- end type HMMutableSignificantTimeEvent -->
<div> <!-- start type HMNumberRange -->
<h3>New Type HomeKit.HMNumberRange</h3>
<pre class='added' data-is-non-breaking="">
public class HMNumberRange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMNumberRange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Max { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Min { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMax (Foundation.NSNumber maxValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromMin (Foundation.NSNumber minValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMNumberRange FromRange (Foundation.NSNumber minValue, Foundation.NSNumber maxValue);</span>
}
</pre>
</div> <!-- end type HMNumberRange -->
<div> <!-- start type HMPresenceEvent -->
<h3>New Type HomeKit.HMPresenceEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMPresenceEvent : HomeKit.HMEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMPresenceEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMPresenceEvent (HMPresenceEventType presenceEventType, HMPresenceEventUserType presenceUserType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventType PresenceEventType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMPresenceEventUserType PresenceUserType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMPresenceEvent -->
<div> <!-- start type HMPresenceEventType -->
<h3>New Type HomeKit.HMPresenceEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMPresenceEventType {
	<span class='added added-field ' data-is-non-breaking="">AtHome = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">EveryEntry = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">EveryExit = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FirstEntry = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LastExit = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAtHome = 4,</span>
}
</pre>
</div> <!-- end type HMPresenceEventType -->
<div> <!-- start type HMPresenceEventUserType -->
<h3>New Type HomeKit.HMPresenceEventUserType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMPresenceEventUserType {
	<span class='added added-field ' data-is-non-breaking="">CurrentUser = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CustomUsers = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeUsers = 2,</span>
}
</pre>
</div> <!-- end type HMPresenceEventUserType -->
<div> <!-- start type HMSignificantEventExtensions -->
<h3>New Type HomeKit.HMSignificantEventExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMSignificantEventExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (HMSignificantEvent self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMSignificantEvent GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type HMSignificantEventExtensions -->
<div> <!-- start type HMSignificantTimeEvent -->
<h3>New Type HomeKit.HMSignificantTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMSignificantTimeEvent : HomeKit.HMTimeEvent, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMSignificantTimeEvent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (Foundation.NSString significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMSignificantTimeEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents Offset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMSignificantEvent SignificantEvent { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type HMSignificantTimeEvent -->
<div> <!-- start type HMTimeEvent -->
<h3>New Type HomeKit.HMTimeEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMTimeEvent : HomeKit.HMEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMTimeEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimeEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMTimeEvent -->

</div> <!-- end namespace HomeKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestination --> <div>
<h3>Type Changed: ImageIO.CGImageDestination</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAuxiliaryDataInfo (CGImageDestination dest, CGImageAuxiliaryDataType auxiliaryImageDataType, CGImageAuxiliaryDataInfo auxiliaryDataInfo);</span>
</pre>
</div>

</div> <!-- end type CGImageDestination -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AuxiliaryDataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FileContentsDictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ImageCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Images { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NamedColorSpace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Width { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->
<!-- start type CGImageSource --> <div>
<h3>Type Changed: ImageIO.CGImageSource</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo CopyAuxiliaryDataInfo (CGImageSource imageSource, uint index, CGImageAuxiliaryDataType auxiliaryImageDataType);</span>
</pre>
</div>

</div> <!-- end type CGImageSource -->
<div> <!-- start type CGImageAuxiliaryDataInfo -->
<h3>New Type ImageIO.CGImageAuxiliaryDataInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGImageAuxiliaryDataInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGImageAuxiliaryDataInfo ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData DepthData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary DepthDataDescription { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CGImageMetadata Metadata { get; set; }</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataInfo -->
<div> <!-- start type CGImageAuxiliaryDataType -->
<h3>New Type ImageIO.CGImageAuxiliaryDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGImageAuxiliaryDataType {
	<span class='added added-field ' data-is-non-breaking="">Depth = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disparity = 1,</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataType -->
<div> <!-- start type CGImageAuxiliaryDataTypeExtensions -->
<h3>New Type ImageIO.CGImageAuxiliaryDataTypeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CGImageAuxiliaryDataTypeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CGImageAuxiliaryDataType self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGImageAuxiliaryDataType GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CGImageAuxiliaryDataTypeExtensions -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace Intents --> <div> 
<h2>Namespace Intents</h2>
<!-- start type INAmountType --> <div>
<h3>Type Changed: Intents.INAmountType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MaximumTransferAmount = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MinimumTransferAmount = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">StatementBalance = 6,</span>
</pre>
</div>

</div> <!-- end type INAmountType -->
<!-- start type INCallRecordType --> <div>
<h3>Type Changed: Intents.INCallRecordType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Latest = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 5,</span>
</pre>
</div>

</div> <!-- end type INCallRecordType -->
<!-- start type INCancelWorkoutIntentResponseCode --> <div>
<h3>Type Changed: Intents.INCancelWorkoutIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandleInApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 6,</span>
</pre>
</div>

</div> <!-- end type INCancelWorkoutIntentResponseCode -->
<!-- start type INCarAirCirculationModeResolutionResult --> <div>
<h3>Type Changed: Intents.INCarAirCirculationModeResolutionResult</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult ConfirmationRequiredWithCarAirCirculationModeToConfirm (INCarAirCirculationMode carAirCirculationModeToConfirm);</span>
</pre>
</div>

</div> <!-- end type INCarAirCirculationModeResolutionResult -->
<!-- start type INDateComponentsRange --> <div>
<h3>Type Changed: Intents.INDateComponentsRange</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (EventKit.EKRecurrenceRule recurrenceRule);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSDateComponents startDateComponents, Foundation.NSDateComponents endDateComponents, INRecurrenceRule recurrenceRule);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual EventKit.EKRecurrenceRule EKRecurrenceRule { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRecurrenceRule RecurrenceRule { get; }</span>
</pre>
</div>

</div> <!-- end type INDateComponentsRange -->
<!-- start type INEndWorkoutIntentResponseCode --> <div>
<h3>Type Changed: Intents.INEndWorkoutIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandleInApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 6,</span>
</pre>
</div>

</div> <!-- end type INEndWorkoutIntentResponseCode -->
<!-- start type INImage --> <div>
<h3>Type Changed: Intents.INImage</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromUrl (Foundation.NSUrl url, double width, double height);</span>
</pre>
</div>

</div> <!-- end type INImage -->
<!-- start type INIntent --> <div>
<h3>Type Changed: Intents.INIntent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string IntentDescription { get; }</span>
</pre>
</div>

</div> <!-- end type INIntent -->
<!-- start type INInteraction --> <div>
<h3>Type Changed: Intents.INInteraction</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public T GetParameterValue&lt;T&gt; (INParameter parameter);</span>
</pre>
</div>

</div> <!-- end type INInteraction -->
<!-- start type INListRideOptionsIntentResponseCode --> <div>
<h3>Type Changed: Intents.INListRideOptionsIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailurePreviousRideNeedsFeedback = 10,</span>
</pre>
</div>

</div> <!-- end type INListRideOptionsIntentResponseCode -->
<!-- start type INMessage --> <div>
<h3>Type Changed: Intents.INMessage</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string conversationIdentifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients, INMessageType messageType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string conversationIdentifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients, INSpeakableString groupName, INMessageType messageType);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ConversationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessageType MessageType { get; }</span>
</pre>
</div>

</div> <!-- end type INMessage -->
<!-- start type INMessageAttribute --> <div>
<h3>Type Changed: Intents.INMessageAttribute</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Played = 5,</span>
</pre>
</div>

</div> <!-- end type INMessageAttribute -->
<!-- start type INMessageAttributeOptions --> <div>
<h3>Type Changed: Intents.INMessageAttributeOptions</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Played = 16,</span>
</pre>
</div>

</div> <!-- end type INMessageAttributeOptions -->
<!-- start type INPauseWorkoutIntentResponseCode --> <div>
<h3>Type Changed: Intents.INPauseWorkoutIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandleInApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 6,</span>
</pre>
</div>

</div> <!-- end type INPauseWorkoutIntentResponseCode -->
<!-- start type INPaymentAccount --> <div>
<h3>Type Changed: Intents.INPaymentAccount</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentAccount (INSpeakableString nickname, string accountNumber, INAccountType accountType, INSpeakableString organizationName, INBalanceAmount balance, INBalanceAmount secondaryBalance);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBalanceAmount Balance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBalanceAmount SecondaryBalance { get; }</span>
</pre>
</div>

</div> <!-- end type INPaymentAccount -->
<!-- start type INPerson --> <div>
<h3>Type Changed: Intents.INPerson</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IINSpeakable[] AlternativeSpeakableMatches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsMe { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VocabularyIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type INPerson -->
<!-- start type INRequestPaymentIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INRequestPaymentIntentHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCurrencyAmount (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INRequestPaymentCurrencyAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePayer (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INRequestPaymentPayerResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INRequestPaymentIntentHandling_Extensions -->
<!-- start type INRequestPaymentIntentResponseCode --> <div>
<h3>Type Changed: Intents.INRequestPaymentIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureNotEligible = 11,</span>
</pre>
</div>

</div> <!-- end type INRequestPaymentIntentResponseCode -->
<!-- start type INResumeWorkoutIntentResponseCode --> <div>
<h3>Type Changed: Intents.INResumeWorkoutIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandleInApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 6,</span>
</pre>
</div>

</div> <!-- end type INResumeWorkoutIntentResponseCode -->
<!-- start type INRideCompletionStatus --> <div>
<h3>Type Changed: Intents.INRideCompletionStatus</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;INCurrencyAmount&gt; DefaultTippingOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideFeedbackTypeOptions FeedbackType { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetCompleted (INRideFeedbackTypeOptions feedbackType);</span>
</pre>
</div>

</div> <!-- end type INRideCompletionStatus -->
<!-- start type INSearchCallHistoryIntent --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntent</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities, INCallRecordTypeOptions callTypes, Foundation.NSNumber unseen);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities, INCallRecordTypeOptions callTypes, bool unseen);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordTypeOptions CallTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Unseen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakUnseen { get; }</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntent -->
<!-- start type INSearchCallHistoryIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCallTypes (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INCallRecordTypeOptionsResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveUnseen (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INBooleanResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentHandling_Extensions -->
<!-- start type INSearchCallHistoryIntentResponse --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecord[] CallRecords { get; set; }</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentResponse -->
<!-- start type INSearchCallHistoryIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSearchCallHistoryIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">InProgress = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 7,</span>
</pre>
</div>

</div> <!-- end type INSearchCallHistoryIntentResponseCode -->
<!-- start type INSearchForMessagesIntent --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (INPerson[] recipients, INPerson[] senders, string[] searchTerms, INMessageAttributeOptions attributes, INDateComponentsRange dateTimeRange, string[] identifiers, string[] notificationIdentifiers, INSpeakableString[] speakableGroupNames);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString[] SpeakableGroupNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SpeakableGroupNamesOperator { get; }</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntent -->
<!-- start type INSearchForMessagesIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpeakableGroupNames (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INSpeakableStringResolutionResult[]&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntentHandling_Extensions -->
<!-- start type INSearchForMessagesIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSearchForMessagesIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureMessageTooManyResults = 7,</span>
</pre>
</div>

</div> <!-- end type INSearchForMessagesIntentResponseCode -->
<!-- start type INSearchForPhotosIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSearchForPhotosIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSearchTerms (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INStringResolutionResult[]&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSearchForPhotosIntentHandling_Extensions -->
<!-- start type INSendMessageIntent --> <div>
<h3>Type Changed: Intents.INSendMessageIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (INPerson[] recipients, string content, INSpeakableString speakableGroupName, string conversationIdentifier, string serviceName, INPerson sender);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ConversationIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString SpeakableGroupName { get; }</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntent -->
<!-- start type INSendMessageIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSendMessageIntentHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSendMessageRecipientResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpeakableGroupName (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntentHandling_Extensions -->
<!-- start type INSendMessageIntentResponse --> <div>
<h3>Type Changed: Intents.INSendMessageIntentResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessage SentMessage { get; set; }</span>
</pre>
</div>

</div> <!-- end type INSendMessageIntentResponse -->
<!-- start type INSendPaymentIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INSendPaymentIntentHandling_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCurrencyAmount (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INSendPaymentCurrencyAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePayee (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INSendPaymentPayeeResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INSendPaymentIntentHandling_Extensions -->
<!-- start type INSendPaymentIntentResponseCode --> <div>
<h3>Type Changed: Intents.INSendPaymentIntentResponseCode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureNotEligible = 12,</span>
</pre>
</div>

</div> <!-- end type INSendPaymentIntentResponseCode -->
<!-- start type INSpeakableString --> <div>
<h3>Type Changed: Intents.INSpeakableString</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IINSpeakable[] AlternativeSpeakableMatches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VocabularyIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type INSpeakableString -->
<!-- start type INStartAudioCallIntent --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (INCallDestinationType destinationType, INPerson[] contacts);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallDestinationType DestinationType { get; }</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntent -->
<!-- start type INStartAudioCallIntentHandling_Extensions --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntentHandling_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDestinationType (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INCallDestinationTypeResolutionResult&gt; completion);</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntentHandling_Extensions -->
<!-- start type INStartAudioCallIntentResponseCode --> <div>
<h3>Type Changed: Intents.INStartAudioCallIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FailureContactNotSupportedByApp = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoValidNumber = 8,</span>
</pre>
</div>

</div> <!-- end type INStartAudioCallIntentResponseCode -->
<!-- start type INStartWorkoutIntentResponseCode --> <div>
<h3>Type Changed: Intents.INStartWorkoutIntentResponseCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HandleInApp = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 7,</span>
</pre>
</div>

</div> <!-- end type INStartWorkoutIntentResponseCode -->
<div> <!-- start type IINAddTasksIntentHandling -->
<h3>New Type Intents.IINAddTasksIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINAddTasksIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleAddTasks (INAddTasksIntent intent, System.Action&lt;INAddTasksIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINAddTasksIntentHandling -->
<div> <!-- start type IINAppendToNoteIntentHandling -->
<h3>New Type Intents.IINAppendToNoteIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINAppendToNoteIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleAppendToNote (INAppendToNoteIntent intent, System.Action&lt;INAppendToNoteIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINAppendToNoteIntentHandling -->
<div> <!-- start type IINCreateNoteIntentHandling -->
<h3>New Type Intents.IINCreateNoteIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCreateNoteIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleCreateNote (INCreateNoteIntent intent, System.Action&lt;INCreateNoteIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINCreateNoteIntentHandling -->
<div> <!-- start type IINCreateTaskListIntentHandling -->
<h3>New Type Intents.IINCreateTaskListIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCreateTaskListIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleCreateTaskList (INCreateTaskListIntent intent, System.Action&lt;INCreateTaskListIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINCreateTaskListIntentHandling -->
<div> <!-- start type IINGetVisualCodeIntentHandling -->
<h3>New Type Intents.IINGetVisualCodeIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINGetVisualCodeIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleGetVisualCode (INGetVisualCodeIntent intent, System.Action&lt;INGetVisualCodeIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINGetVisualCodeIntentHandling -->
<div> <!-- start type IINNotebookDomainHandling -->
<h3>New Type Intents.IINNotebookDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINNotebookDomainHandling : IINAddTasksIntentHandling, IINAppendToNoteIntentHandling, IINCreateNoteIntentHandling, IINCreateTaskListIntentHandling, IINSearchForNotebookItemsIntentHandling, IINSetTaskAttributeIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINNotebookDomainHandling -->
<div> <!-- start type IINSearchForAccountsIntentHandling -->
<h3>New Type Intents.IINSearchForAccountsIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForAccountsIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchForAccounts (INSearchForAccountsIntent intent, System.Action&lt;INSearchForAccountsIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchForAccountsIntentHandling -->
<div> <!-- start type IINSearchForNotebookItemsIntentHandling -->
<h3>New Type Intents.IINSearchForNotebookItemsIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForNotebookItemsIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchForNotebookItems (INSearchForNotebookItemsIntent intent, System.Action&lt;INSearchForNotebookItemsIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchForNotebookItemsIntentHandling -->
<div> <!-- start type IINSetTaskAttributeIntentHandling -->
<h3>New Type Intents.IINSetTaskAttributeIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSetTaskAttributeIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSetTaskAttribute (INSetTaskAttributeIntent intent, System.Action&lt;INSetTaskAttributeIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSetTaskAttributeIntentHandling -->
<div> <!-- start type IINTransferMoneyIntentHandling -->
<h3>New Type Intents.IINTransferMoneyIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINTransferMoneyIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleTransferMoney (INTransferMoneyIntent intent, System.Action&lt;INTransferMoneyIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINTransferMoneyIntentHandling -->
<div> <!-- start type IINVisualCodeDomainHandling -->
<h3>New Type Intents.IINVisualCodeDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINVisualCodeDomainHandling : IINGetVisualCodeIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINVisualCodeDomainHandling -->
<div> <!-- start type INAccountTypeResolutionResult -->
<h3>New Type Intents.INAccountTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INAccountTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INAccountTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAccountTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INAccountTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INAccountTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INAccountTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INAccountTypeResolutionResult GetConfirmationRequired (INAccountType accountTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INAccountTypeResolutionResult GetSuccess (INAccountType resolvedAccountType);</span>
}
</pre>
</div> <!-- end type INAccountTypeResolutionResult -->
<div> <!-- start type INAddTasksIntent -->
<h3>New Type Intents.INAddTasksIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INAddTasksIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INAddTasksIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAddTasksIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAddTasksIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAddTasksIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAddTasksIntent (INTaskList targetTaskList, INSpeakableString[] taskTitles, INSpatialEventTrigger spatialEventTrigger, INTemporalEventTrigger temporalEventTrigger);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpatialEventTrigger SpatialEventTrigger { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskList TargetTaskList { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString[] TaskTitles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTemporalEventTrigger TemporalEventTrigger { get; }</span>
}
</pre>
</div> <!-- end type INAddTasksIntent -->
<div> <!-- start type INAddTasksIntentHandling_Extensions -->
<h3>New Type Intents.INAddTasksIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INAddTasksIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINAddTasksIntentHandling This, INAddTasksIntent intent, System.Action&lt;INAddTasksIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpatialEventTrigger (IINAddTasksIntentHandling This, INAddTasksIntent intent, System.Action&lt;INSpatialEventTriggerResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTargetTaskList (IINAddTasksIntentHandling This, INAddTasksIntent intent, System.Action&lt;INTaskListResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTaskTitles (IINAddTasksIntentHandling This, INAddTasksIntent intent, System.Action&lt;INSpeakableStringResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTemporalEventTrigger (IINAddTasksIntentHandling This, INAddTasksIntent intent, System.Action&lt;INTemporalEventTriggerResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INAddTasksIntentHandling_Extensions -->
<div> <!-- start type INAddTasksIntentResponse -->
<h3>New Type Intents.INAddTasksIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INAddTasksIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INAddTasksIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAddTasksIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAddTasksIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAddTasksIntentResponse (INAddTasksIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INTask[] AddedTasks { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INAddTasksIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskList ModifiedTaskList { get; set; }</span>
}
</pre>
</div> <!-- end type INAddTasksIntentResponse -->
<div> <!-- start type INAddTasksIntentResponseCode -->
<h3>New Type Intents.INAddTasksIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INAddTasksIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INAddTasksIntentResponseCode -->
<div> <!-- start type INAppendToNoteIntent -->
<h3>New Type Intents.INAppendToNoteIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INAppendToNoteIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INAppendToNoteIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAppendToNoteIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAppendToNoteIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAppendToNoteIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAppendToNoteIntent (INNote targetNote, INNoteContent content);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNoteContent Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNote TargetNote { get; }</span>
}
</pre>
</div> <!-- end type INAppendToNoteIntent -->
<div> <!-- start type INAppendToNoteIntentHandling_Extensions -->
<h3>New Type Intents.INAppendToNoteIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INAppendToNoteIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINAppendToNoteIntentHandling This, INAppendToNoteIntent intent, System.Action&lt;INAppendToNoteIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContentForAppend (IINAppendToNoteIntentHandling This, INAppendToNoteIntent intent, System.Action&lt;INNoteContentResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTargetNoteForAppend (IINAppendToNoteIntentHandling This, INAppendToNoteIntent intent, System.Action&lt;INNoteResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INAppendToNoteIntentHandling_Extensions -->
<div> <!-- start type INAppendToNoteIntentResponse -->
<h3>New Type Intents.INAppendToNoteIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INAppendToNoteIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INAppendToNoteIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAppendToNoteIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INAppendToNoteIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INAppendToNoteIntentResponse (INAppendToNoteIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INAppendToNoteIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNote Note { get; set; }</span>
}
</pre>
</div> <!-- end type INAppendToNoteIntentResponse -->
<div> <!-- start type INAppendToNoteIntentResponseCode -->
<h3>New Type Intents.INAppendToNoteIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INAppendToNoteIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCannotUpdatePasswordProtectedNote = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INAppendToNoteIntentResponseCode -->
<div> <!-- start type INBalanceAmount -->
<h3>New Type Intents.INBalanceAmount</h3>
<pre class='added' data-is-non-breaking="">
public class INBalanceAmount : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INBalanceAmount (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBalanceAmount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBalanceAmount (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INBalanceAmount (Foundation.NSDecimalNumber amount, INBalanceType balanceType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INBalanceAmount (Foundation.NSDecimalNumber amount, string currencyCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Amount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBalanceType BalanceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CurrencyCode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INBalanceAmount -->
<div> <!-- start type INBalanceType -->
<h3>New Type Intents.INBalanceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INBalanceType {
	<span class='added added-field ' data-is-non-breaking="">Miles = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Money = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Points = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INBalanceType -->
<div> <!-- start type INBalanceTypeResolutionResult -->
<h3>New Type Intents.INBalanceTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INBalanceTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INBalanceTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBalanceTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBalanceTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBalanceTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBalanceTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INBalanceTypeResolutionResult GetConfirmationRequired (INBalanceType balanceTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INBalanceTypeResolutionResult GetSuccess (INBalanceType resolvedBalanceType);</span>
}
</pre>
</div> <!-- end type INBalanceTypeResolutionResult -->
<div> <!-- start type INCallCapability -->
<h3>New Type Intents.INCallCapability</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallCapability {
	<span class='added added-field ' data-is-non-breaking="">AudioCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoCall = 2,</span>
}
</pre>
</div> <!-- end type INCallCapability -->
<div> <!-- start type INCallDestinationType -->
<h3>New Type Intents.INCallDestinationType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallDestinationType {
	<span class='added added-field ' data-is-non-breaking="">Emergency = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Redial = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 3,</span>
}
</pre>
</div> <!-- end type INCallDestinationType -->
<div> <!-- start type INCallDestinationTypeResolutionResult -->
<h3>New Type Intents.INCallDestinationTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallDestinationTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallDestinationTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallDestinationTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult GetConfirmationRequired (INCallDestinationType callDestinationTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallDestinationTypeResolutionResult GetSuccess (INCallDestinationType resolvedCallDestinationType);</span>
}
</pre>
</div> <!-- end type INCallDestinationTypeResolutionResult -->
<div> <!-- start type INCallRecord -->
<h3>New Type Intents.INCallRecord</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecord : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCallRecord (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecord (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecord (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCallRecord (string identifier, Foundation.NSDate dateCreated, INPerson caller, INCallRecordType callRecordType, INCallCapability callCapability, Foundation.NSNumber callDuration, Foundation.NSNumber unseen);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallCapability CallCapability { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? CallDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordType CallRecordType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Caller { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? Unseen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakCallDuration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSNumber WeakUnseen { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INCallRecord -->
<div> <!-- start type INCallRecordTypeOptions -->
<h3>New Type Intents.INCallRecordTypeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INCallRecordTypeOptions {
	<span class='added added-field ' data-is-non-breaking="">Latest = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Missed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Voicemail = 16,</span>
}
</pre>
</div> <!-- end type INCallRecordTypeOptions -->
<div> <!-- start type INCallRecordTypeOptionsResolutionResult -->
<h3>New Type Intents.INCallRecordTypeOptionsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecordTypeOptionsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeOptionsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeOptionsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult GetConfirmationRequired (INCallRecordTypeOptions callRecordTypeOptionsToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeOptionsResolutionResult GetSuccess (INCallRecordTypeOptions resolvedCallRecordTypeOptions);</span>
}
</pre>
</div> <!-- end type INCallRecordTypeOptionsResolutionResult -->
<div> <!-- start type INCreateNoteIntent -->
<h3>New Type Intents.INCreateNoteIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INCreateNoteIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateNoteIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateNoteIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateNoteIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateNoteIntent (INSpeakableString title, INNoteContent content, INSpeakableString groupName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNoteContent Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
}
</pre>
</div> <!-- end type INCreateNoteIntent -->
<div> <!-- start type INCreateNoteIntentHandling_Extensions -->
<h3>New Type Intents.INCreateNoteIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INCreateNoteIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINCreateNoteIntentHandling This, INCreateNoteIntent intent, System.Action&lt;INCreateNoteIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContent (IINCreateNoteIntentHandling This, INCreateNoteIntent intent, System.Action&lt;INNoteContentResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupName (IINCreateNoteIntentHandling This, INCreateNoteIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTitle (IINCreateNoteIntentHandling This, INCreateNoteIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INCreateNoteIntentHandling_Extensions -->
<div> <!-- start type INCreateNoteIntentResponse -->
<h3>New Type Intents.INCreateNoteIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INCreateNoteIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateNoteIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateNoteIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateNoteIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateNoteIntentResponse (INCreateNoteIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCreateNoteIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNote CreatedNote { get; set; }</span>
}
</pre>
</div> <!-- end type INCreateNoteIntentResponse -->
<div> <!-- start type INCreateNoteIntentResponseCode -->
<h3>New Type Intents.INCreateNoteIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCreateNoteIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INCreateNoteIntentResponseCode -->
<div> <!-- start type INCreateTaskListIntent -->
<h3>New Type Intents.INCreateTaskListIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INCreateTaskListIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateTaskListIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateTaskListIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateTaskListIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateTaskListIntent (INSpeakableString title, INSpeakableString[] taskTitles, INSpeakableString groupName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString[] TaskTitles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
}
</pre>
</div> <!-- end type INCreateTaskListIntent -->
<div> <!-- start type INCreateTaskListIntentHandling_Extensions -->
<h3>New Type Intents.INCreateTaskListIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INCreateTaskListIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINCreateTaskListIntentHandling This, INCreateTaskListIntent intent, System.Action&lt;INCreateTaskListIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupName (IINCreateTaskListIntentHandling This, INCreateTaskListIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTaskTitles (IINCreateTaskListIntentHandling This, INCreateTaskListIntent intent, System.Action&lt;INSpeakableStringResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTitle (IINCreateTaskListIntentHandling This, INCreateTaskListIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INCreateTaskListIntentHandling_Extensions -->
<div> <!-- start type INCreateTaskListIntentResponse -->
<h3>New Type Intents.INCreateTaskListIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INCreateTaskListIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateTaskListIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateTaskListIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCreateTaskListIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCreateTaskListIntentResponse (INCreateTaskListIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCreateTaskListIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskList CreatedTaskList { get; set; }</span>
}
</pre>
</div> <!-- end type INCreateTaskListIntentResponse -->
<div> <!-- start type INCreateTaskListIntentResponseCode -->
<h3>New Type Intents.INCreateTaskListIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCreateTaskListIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INCreateTaskListIntentResponseCode -->
<div> <!-- start type INDateSearchType -->
<h3>New Type Intents.INDateSearchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INDateSearchType {
	<span class='added added-field ' data-is-non-breaking="">ByCreatedDate = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ByDueDate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ByModifiedDate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INDateSearchType -->
<div> <!-- start type INDateSearchTypeResolutionResult -->
<h3>New Type Intents.INDateSearchTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INDateSearchTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateSearchTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateSearchTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateSearchTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateSearchTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateSearchTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INDateSearchTypeResolutionResult GetConfirmationRequired (INDateSearchType dateSearchTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateSearchTypeResolutionResult GetSuccess (INDateSearchType resolvedDateSearchType);</span>
}
</pre>
</div> <!-- end type INDateSearchTypeResolutionResult -->
<div> <!-- start type INGetVisualCodeIntent -->
<h3>New Type Intents.INGetVisualCodeIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INGetVisualCodeIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetVisualCodeIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetVisualCodeIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetVisualCodeIntent (INVisualCodeType visualCodeType);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetVisualCodeIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INVisualCodeType VisualCodeType { get; }</span>
}
</pre>
</div> <!-- end type INGetVisualCodeIntent -->
<div> <!-- start type INGetVisualCodeIntentHandling_Extensions -->
<h3>New Type Intents.INGetVisualCodeIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INGetVisualCodeIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINGetVisualCodeIntentHandling This, INGetVisualCodeIntent intent, System.Action&lt;INGetVisualCodeIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveVisualCodeType (IINGetVisualCodeIntentHandling This, INGetVisualCodeIntent intent, System.Action&lt;INVisualCodeTypeResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INGetVisualCodeIntentHandling_Extensions -->
<div> <!-- start type INGetVisualCodeIntentResponse -->
<h3>New Type Intents.INGetVisualCodeIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INGetVisualCodeIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetVisualCodeIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetVisualCodeIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetVisualCodeIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetVisualCodeIntentResponse (INGetVisualCodeIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INGetVisualCodeIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage VisualCodeImage { get; set; }</span>
}
</pre>
</div> <!-- end type INGetVisualCodeIntentResponse -->
<div> <!-- start type INGetVisualCodeIntentResponseCode -->
<h3>New Type Intents.INGetVisualCodeIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetVisualCodeIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INGetVisualCodeIntentResponseCode -->
<div> <!-- start type INImageNoteContent -->
<h3>New Type Intents.INImageNoteContent</h3>
<pre class='added' data-is-non-breaking="">
public class INImageNoteContent : Intents.INNoteContent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INImageNoteContent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INImageNoteContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImageNoteContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INImageNoteContent (INImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImageNoteContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage Image { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INImageNoteContent -->
<div> <!-- start type INLocationSearchType -->
<h3>New Type Intents.INLocationSearchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INLocationSearchType {
	<span class='added added-field ' data-is-non-breaking="">ByLocationTrigger = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INLocationSearchType -->
<div> <!-- start type INLocationSearchTypeResolutionResult -->
<h3>New Type Intents.INLocationSearchTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INLocationSearchTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INLocationSearchTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INLocationSearchTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INLocationSearchTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INLocationSearchTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INLocationSearchTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INLocationSearchTypeResolutionResult GetConfirmationRequired (INLocationSearchType locationSearchTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INLocationSearchTypeResolutionResult GetSuccess (INLocationSearchType resolvedLocationSearchType);</span>
}
</pre>
</div> <!-- end type INLocationSearchTypeResolutionResult -->
<div> <!-- start type INMessageType -->
<h3>New Type Intents.INMessageType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INMessageType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">DigitalTouch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Handwriting = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaAddressCard = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaAudio = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaCalendar = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaImage = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaLocation = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaPass = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">MediaVideo = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Sticker = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackDisliked = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackEmphasized = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLaughed = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLiked = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackLoved = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">TapbackQuestioned = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INMessageType -->
<div> <!-- start type INNote -->
<h3>New Type Intents.INNote</h3>
<pre class='added' data-is-non-breaking="">
public class INNote : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INNote ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INNote (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNote (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNote (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INNote (INSpeakableString title, INNoteContent[] contents, INSpeakableString groupName, Foundation.NSDateComponents createdDateComponents, Foundation.NSDateComponents modifiedDateComponents, string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNoteContent[] Contents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents CreatedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents ModifiedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INNote -->
<div> <!-- start type INNoteContent -->
<h3>New Type Intents.INNoteContent</h3>
<pre class='added' data-is-non-breaking="">
public class INNoteContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INNoteContent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INNoteContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INNoteContent -->
<div> <!-- start type INNoteContentResolutionResult -->
<h3>New Type Intents.INNoteContentResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INNoteContentResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContentResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContentResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INNoteContentResolutionResult GetConfirmationRequired (INNoteContent noteContentToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNoteContentResolutionResult GetDisambiguation (INNoteContent[] noteContentsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNoteContentResolutionResult GetSuccess (INNoteContent resolvedNoteContent);</span>
}
</pre>
</div> <!-- end type INNoteContentResolutionResult -->
<div> <!-- start type INNoteContentType -->
<h3>New Type Intents.INNoteContentType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INNoteContentType {
	<span class='added added-field ' data-is-non-breaking="">Image = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Text = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INNoteContentType -->
<div> <!-- start type INNoteContentTypeResolutionResult -->
<h3>New Type Intents.INNoteContentTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INNoteContentTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INNoteContentTypeResolutionResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContentTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteContentTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteContentTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INNoteContentTypeResolutionResult GetConfirmationRequired (INNoteContentType noteContentTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNoteContentTypeResolutionResult GetSuccess (INNoteContentType resolvedNoteContentType);</span>
}
</pre>
</div> <!-- end type INNoteContentTypeResolutionResult -->
<div> <!-- start type INNoteResolutionResult -->
<h3>New Type Intents.INNoteResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INNoteResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INNoteResolutionResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNoteResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNoteResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INNoteResolutionResult GetConfirmationRequired (INNote noteToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNoteResolutionResult GetDisambiguation (INNote[] notesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNoteResolutionResult GetSuccess (INNote resolvedNote);</span>
}
</pre>
</div> <!-- end type INNoteResolutionResult -->
<div> <!-- start type INNotebookItemType -->
<h3>New Type Intents.INNotebookItemType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INNotebookItemType {
	<span class='added added-field ' data-is-non-breaking="">Note = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Task = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">TaskList = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INNotebookItemType -->
<div> <!-- start type INNotebookItemTypeResolutionResult -->
<h3>New Type Intents.INNotebookItemTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INNotebookItemTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INNotebookItemTypeResolutionResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNotebookItemTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INNotebookItemTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult GetConfirmationRequired (INNotebookItemType notebookItemTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult GetDisambiguation (Foundation.NSNumber[] notebookItemTypesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INNotebookItemTypeResolutionResult GetSuccess (INNotebookItemType resolvedNotebookItemType);</span>
}
</pre>
</div> <!-- end type INNotebookItemTypeResolutionResult -->
<div> <!-- start type INParameter -->
<h3>New Type Intents.INParameter</h3>
<pre class='added' data-is-non-breaking="">
public class INParameter : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INParameter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INParameter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INParameter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ObjCRuntime.Class ParameterClass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ParameterKeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Type ParameterType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetIndex (string subKeyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INParameter GetParameter (ObjCRuntime.Class aClass, string keyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INParameter GetParameter (System.Type type, string keyPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqualTo (INParameter parameter);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetIndex (uint index, string subKeyPath);</span>
}
</pre>
</div> <!-- end type INParameter -->
<div> <!-- start type INRecurrenceFrequency -->
<h3>New Type Intents.INRecurrenceFrequency</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRecurrenceFrequency {
	<span class='added added-field ' data-is-non-breaking="">Daily = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Hourly = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Minute = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Monthly = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Weekly = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Yearly = 6,</span>
}
</pre>
</div> <!-- end type INRecurrenceFrequency -->
<div> <!-- start type INRecurrenceRule -->
<h3>New Type Intents.INRecurrenceRule</h3>
<pre class='added' data-is-non-breaking="">
public class INRecurrenceRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRecurrenceRule (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRecurrenceRule (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRecurrenceRule (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRecurrenceRule (uint interval, INRecurrenceFrequency frequency);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRecurrenceFrequency Frequency { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Interval { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRecurrenceRule -->
<div> <!-- start type INRequestPaymentCurrencyAmountResolutionResult -->
<h3>New Type Intents.INRequestPaymentCurrencyAmountResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestPaymentCurrencyAmountResolutionResult : Intents.INCurrencyAmountResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentCurrencyAmountResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentCurrencyAmountResolutionResult (INCurrencyAmountResolutionResult currencyAmountResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentCurrencyAmountResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentCurrencyAmountResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentCurrencyAmountResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentCurrencyAmountResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INRequestPaymentCurrencyAmountResolutionResult GetUnsupported (INRequestPaymentCurrencyAmountUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INRequestPaymentCurrencyAmountResolutionResult -->
<div> <!-- start type INRequestPaymentCurrencyAmountUnsupportedReason -->
<h3>New Type Intents.INRequestPaymentCurrencyAmountUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRequestPaymentCurrencyAmountUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">AmountAboveMaximum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AmountBelowMinimum = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrencyUnsupported = 3,</span>
}
</pre>
</div> <!-- end type INRequestPaymentCurrencyAmountUnsupportedReason -->
<div> <!-- start type INRequestPaymentPayerResolutionResult -->
<h3>New Type Intents.INRequestPaymentPayerResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestPaymentPayerResolutionResult : Intents.INPersonResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentPayerResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentPayerResolutionResult (INPersonResolutionResult personResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentPayerResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentPayerResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentPayerResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRequestPaymentPayerResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INRequestPaymentPayerResolutionResult GetUnsupported (INRequestPaymentPayerUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INRequestPaymentPayerResolutionResult -->
<div> <!-- start type INRequestPaymentPayerUnsupportedReason -->
<h3>New Type Intents.INRequestPaymentPayerUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRequestPaymentPayerUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">CredentialsUnverified = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAccount = 2,</span>
}
</pre>
</div> <!-- end type INRequestPaymentPayerUnsupportedReason -->
<div> <!-- start type INRideFeedbackTypeOptions -->
<h3>New Type Intents.INRideFeedbackTypeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRideFeedbackTypeOptions {
	<span class='added added-field ' data-is-non-breaking="">Rate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Tip = 2,</span>
}
</pre>
</div> <!-- end type INRideFeedbackTypeOptions -->
<div> <!-- start type INSearchForAccountsIntent -->
<h3>New Type Intents.INSearchForAccountsIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForAccountsIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForAccountsIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForAccountsIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForAccountsIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForAccountsIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForAccountsIntent (INSpeakableString accountNickname, INAccountType accountType, INSpeakableString organizationName, INBalanceType requestedBalanceType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString AccountNickname { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INAccountType AccountType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString OrganizationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INBalanceType RequestedBalanceType { get; }</span>
}
</pre>
</div> <!-- end type INSearchForAccountsIntent -->
<div> <!-- start type INSearchForAccountsIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForAccountsIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForAccountsIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINSearchForAccountsIntentHandling This, INSearchForAccountsIntent intent, System.Action&lt;INSearchForAccountsIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAccountNickname (IINSearchForAccountsIntentHandling This, INSearchForAccountsIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAccountType (IINSearchForAccountsIntentHandling This, INSearchForAccountsIntent intent, System.Action&lt;INAccountTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveOrganizationName (IINSearchForAccountsIntentHandling This, INSearchForAccountsIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRequestedBalanceType (IINSearchForAccountsIntentHandling This, INSearchForAccountsIntent intent, System.Action&lt;INBalanceTypeResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForAccountsIntentHandling_Extensions -->
<div> <!-- start type INSearchForAccountsIntentResponse -->
<h3>New Type Intents.INSearchForAccountsIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForAccountsIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForAccountsIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForAccountsIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForAccountsIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForAccountsIntentResponse (INSearchForAccountsIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount[] Accounts { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForAccountsIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSearchForAccountsIntentResponse -->
<div> <!-- start type INSearchForAccountsIntentResponseCode -->
<h3>New Type Intents.INSearchForAccountsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForAccountsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAccountNotFound = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCredentialsUnverified = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForAccountsIntentResponseCode -->
<div> <!-- start type INSearchForNotebookItemsIntent -->
<h3>New Type Intents.INSearchForNotebookItemsIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForNotebookItemsIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForNotebookItemsIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForNotebookItemsIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntent (INSpeakableString title, string content, INNotebookItemType itemType, INTaskStatus status, CoreLocation.CLPlacemark location, INLocationSearchType locationSearchType, INDateComponentsRange dateTime, INDateSearchType dateSearchType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateSearchType DateSearchType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNotebookItemType ItemType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INLocationSearchType LocationSearchType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
}
</pre>
</div> <!-- end type INSearchForNotebookItemsIntent -->
<div> <!-- start type INSearchForNotebookItemsIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForNotebookItemsIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForNotebookItemsIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INSearchForNotebookItemsIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContent (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateSearchType (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INDateSearchTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateTime (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveItemType (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INNotebookItemTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveLocation (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveLocationSearchType (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INLocationSearchTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveStatus (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INTaskStatusResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTitle (IINSearchForNotebookItemsIntentHandling This, INSearchForNotebookItemsIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForNotebookItemsIntentHandling_Extensions -->
<div> <!-- start type INSearchForNotebookItemsIntentResponse -->
<h3>New Type Intents.INSearchForNotebookItemsIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForNotebookItemsIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForNotebookItemsIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForNotebookItemsIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForNotebookItemsIntentResponse (INSearchForNotebookItemsIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForNotebookItemsIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INNote[] Notes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSortType SortType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskList[] TaskLists { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTask[] Tasks { get; set; }</span>
}
</pre>
</div> <!-- end type INSearchForNotebookItemsIntentResponse -->
<div> <!-- start type INSearchForNotebookItemsIntentResponseCode -->
<h3>New Type Intents.INSearchForNotebookItemsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForNotebookItemsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForNotebookItemsIntentResponseCode -->
<div> <!-- start type INSendMessageRecipientResolutionResult -->
<h3>New Type Intents.INSendMessageRecipientResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageRecipientResolutionResult : Intents.INPersonResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageRecipientResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageRecipientResolutionResult (INPersonResolutionResult personResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageRecipientResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSendMessageRecipientResolutionResult GetUnsupported (INSendMessageRecipientUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INSendMessageRecipientResolutionResult -->
<div> <!-- start type INSendMessageRecipientUnsupportedReason -->
<h3>New Type Intents.INSendMessageRecipientUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendMessageRecipientUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">MessagingServiceNotEnabledForRecipient = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAccount = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Offline = 2,</span>
}
</pre>
</div> <!-- end type INSendMessageRecipientUnsupportedReason -->
<div> <!-- start type INSendPaymentCurrencyAmountResolutionResult -->
<h3>New Type Intents.INSendPaymentCurrencyAmountResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSendPaymentCurrencyAmountResolutionResult : Intents.INCurrencyAmountResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentCurrencyAmountResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentCurrencyAmountResolutionResult (INCurrencyAmountResolutionResult currencyAmountResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentCurrencyAmountResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentCurrencyAmountResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentCurrencyAmountResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentCurrencyAmountResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSendPaymentCurrencyAmountResolutionResult GetUnsupported (INSendPaymentCurrencyAmountUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INSendPaymentCurrencyAmountResolutionResult -->
<div> <!-- start type INSendPaymentCurrencyAmountUnsupportedReason -->
<h3>New Type Intents.INSendPaymentCurrencyAmountUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendPaymentCurrencyAmountUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">AmountAboveMaximum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AmountBelowMinimum = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrencyUnsupported = 3,</span>
}
</pre>
</div> <!-- end type INSendPaymentCurrencyAmountUnsupportedReason -->
<div> <!-- start type INSendPaymentPayeeResolutionResult -->
<h3>New Type Intents.INSendPaymentPayeeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSendPaymentPayeeResolutionResult : Intents.INPersonResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentPayeeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentPayeeResolutionResult (INPersonResolutionResult personResolutionResult);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentPayeeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentPayeeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentPayeeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSendPaymentPayeeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSendPaymentPayeeResolutionResult GetUnsupported (INSendPaymentPayeeUnsupportedReason reason);</span>
}
</pre>
</div> <!-- end type INSendPaymentPayeeResolutionResult -->
<div> <!-- start type INSendPaymentPayeeUnsupportedReason -->
<h3>New Type Intents.INSendPaymentPayeeUnsupportedReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendPaymentPayeeUnsupportedReason {
	<span class='added added-field ' data-is-non-breaking="">CredentialsUnverified = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientFunds = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NoAccount = 3,</span>
}
</pre>
</div> <!-- end type INSendPaymentPayeeUnsupportedReason -->
<div> <!-- start type INSetTaskAttributeIntent -->
<h3>New Type Intents.INSetTaskAttributeIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSetTaskAttributeIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSetTaskAttributeIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSetTaskAttributeIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetTaskAttributeIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetTaskAttributeIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSetTaskAttributeIntent (INTask targetTask, INTaskStatus status, INSpatialEventTrigger spatialEventTrigger, INTemporalEventTrigger temporalEventTrigger);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpatialEventTrigger SpatialEventTrigger { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTask TargetTask { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTemporalEventTrigger TemporalEventTrigger { get; }</span>
}
</pre>
</div> <!-- end type INSetTaskAttributeIntent -->
<div> <!-- start type INSetTaskAttributeIntentHandling_Extensions -->
<h3>New Type Intents.INSetTaskAttributeIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSetTaskAttributeIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINSetTaskAttributeIntentHandling This, INSetTaskAttributeIntent intent, System.Action&lt;INSetTaskAttributeIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSpatialEventTrigger (IINSetTaskAttributeIntentHandling This, INSetTaskAttributeIntent intent, System.Action&lt;INSpatialEventTriggerResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveStatus (IINSetTaskAttributeIntentHandling This, INSetTaskAttributeIntent intent, System.Action&lt;INTaskStatusResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTargetTask (IINSetTaskAttributeIntentHandling This, INSetTaskAttributeIntent intent, System.Action&lt;INTaskResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTemporalEventTrigger (IINSetTaskAttributeIntentHandling This, INSetTaskAttributeIntent intent, System.Action&lt;INTemporalEventTriggerResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSetTaskAttributeIntentHandling_Extensions -->
<div> <!-- start type INSetTaskAttributeIntentResponse -->
<h3>New Type Intents.INSetTaskAttributeIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSetTaskAttributeIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSetTaskAttributeIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetTaskAttributeIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetTaskAttributeIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSetTaskAttributeIntentResponse (INSetTaskAttributeIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSetTaskAttributeIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTask ModifiedTask { get; set; }</span>
}
</pre>
</div> <!-- end type INSetTaskAttributeIntentResponse -->
<div> <!-- start type INSetTaskAttributeIntentResponseCode -->
<h3>New Type Intents.INSetTaskAttributeIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSetTaskAttributeIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSetTaskAttributeIntentResponseCode -->
<div> <!-- start type INSortType -->
<h3>New Type Intents.INSortType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSortType {
	<span class='added added-field ' data-is-non-breaking="">AsIs = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ByDate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INSortType -->
<div> <!-- start type INSpatialEvent -->
<h3>New Type Intents.INSpatialEvent</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSpatialEvent {
	<span class='added added-field ' data-is-non-breaking="">Arrive = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Depart = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INSpatialEvent -->
<div> <!-- start type INSpatialEventTrigger -->
<h3>New Type Intents.INSpatialEventTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class INSpatialEventTrigger : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpatialEventTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpatialEventTrigger (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpatialEventTrigger (CoreLocation.CLPlacemark placemark, INSpatialEvent event);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpatialEvent Event { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark Placemark { get; }</span>
}
</pre>
</div> <!-- end type INSpatialEventTrigger -->
<div> <!-- start type INSpatialEventTriggerResolutionResult -->
<h3>New Type Intents.INSpatialEventTriggerResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSpatialEventTriggerResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpatialEventTriggerResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpatialEventTriggerResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult GetConfirmationRequired (INSpatialEventTrigger spatialEventTriggerToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult GetDisambiguation (INSpatialEventTrigger[] spatialEventTriggersToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpatialEventTriggerResolutionResult GetSuccess (INSpatialEventTrigger resolvedSpatialEventTrigger);</span>
}
</pre>
</div> <!-- end type INSpatialEventTriggerResolutionResult -->
<div> <!-- start type INSpeakable_Extensions -->
<h3>New Type Intents.INSpeakable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSpeakable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IINSpeakable[] GetAlternativeSpeakableMatches (IINSpeakable This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetVocabularyIdentifier (IINSpeakable This);</span>
}
</pre>
</div> <!-- end type INSpeakable_Extensions -->
<div> <!-- start type INTask -->
<h3>New Type Intents.INTask</h3>
<pre class='added' data-is-non-breaking="">
public class INTask : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTask (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTask (INSpeakableString title, INTaskStatus status, INTaskType taskType, INSpatialEventTrigger spatialEventTrigger, INTemporalEventTrigger temporalEventTrigger, Foundation.NSDateComponents createdDateComponents, Foundation.NSDateComponents modifiedDateComponents, string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents CreatedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents ModifiedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpatialEventTrigger SpatialEventTrigger { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTaskType TaskType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTemporalEventTrigger TemporalEventTrigger { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INTask -->
<div> <!-- start type INTaskList -->
<h3>New Type Intents.INTaskList</h3>
<pre class='added' data-is-non-breaking="">
public class INTaskList : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTaskList (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskList (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTaskList (INSpeakableString title, INTask[] tasks, INSpeakableString groupName, Foundation.NSDateComponents createdDateComponents, Foundation.NSDateComponents modifiedDateComponents, string identifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents CreatedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents ModifiedDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTask[] Tasks { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INTaskList -->
<div> <!-- start type INTaskListResolutionResult -->
<h3>New Type Intents.INTaskListResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INTaskListResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskListResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskListResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskListResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskListResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskListResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INTaskListResolutionResult GetConfirmationRequired (INTaskList taskListToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTaskListResolutionResult GetDisambiguation (INTaskList[] taskListsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTaskListResolutionResult GetSuccess (INTaskList resolvedTaskList);</span>
}
</pre>
</div> <!-- end type INTaskListResolutionResult -->
<div> <!-- start type INTaskResolutionResult -->
<h3>New Type Intents.INTaskResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INTaskResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INTaskResolutionResult GetConfirmationRequired (INTask taskToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTaskResolutionResult GetDisambiguation (INTask[] tasksToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTaskResolutionResult GetSuccess (INTask resolvedTask);</span>
}
</pre>
</div> <!-- end type INTaskResolutionResult -->
<div> <!-- start type INTaskStatus -->
<h3>New Type Intents.INTaskStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INTaskStatus {
	<span class='added added-field ' data-is-non-breaking="">Completed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotCompleted = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INTaskStatus -->
<div> <!-- start type INTaskStatusResolutionResult -->
<h3>New Type Intents.INTaskStatusResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INTaskStatusResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskStatusResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTaskStatusResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskStatusResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskStatusResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTaskStatusResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INTaskStatusResolutionResult GetConfirmationRequired (INTaskStatus taskStatusToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTaskStatusResolutionResult GetSuccess (INTaskStatus resolvedTaskStatus);</span>
}
</pre>
</div> <!-- end type INTaskStatusResolutionResult -->
<div> <!-- start type INTaskType -->
<h3>New Type Intents.INTaskType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INTaskType {
	<span class='added added-field ' data-is-non-breaking="">Completable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotCompletable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INTaskType -->
<div> <!-- start type INTemporalEventTrigger -->
<h3>New Type Intents.INTemporalEventTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class INTemporalEventTrigger : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTemporalEventTrigger (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemporalEventTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTemporalEventTrigger (INDateComponentsRange dateComponentsRange);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemporalEventTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateComponentsRange { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INTemporalEventTrigger -->
<div> <!-- start type INTemporalEventTriggerResolutionResult -->
<h3>New Type Intents.INTemporalEventTriggerResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INTemporalEventTriggerResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemporalEventTriggerResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemporalEventTriggerResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult GetConfirmationRequired (INTemporalEventTrigger temporalEventTriggerToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult GetDisambiguation (INTemporalEventTrigger[] temporalEventTriggersToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTemporalEventTriggerResolutionResult GetSuccess (INTemporalEventTrigger resolvedTemporalEventTrigger);</span>
}
</pre>
</div> <!-- end type INTemporalEventTriggerResolutionResult -->
<div> <!-- start type INTextNoteContent -->
<h3>New Type Intents.INTextNoteContent</h3>
<pre class='added' data-is-non-breaking="">
public class INTextNoteContent : Intents.INNoteContent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTextNoteContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTextNoteContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTextNoteContent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTextNoteContent (string text);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Text { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INTextNoteContent -->
<div> <!-- start type INTransferMoneyIntent -->
<h3>New Type Intents.INTransferMoneyIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INTransferMoneyIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTransferMoneyIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTransferMoneyIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTransferMoneyIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTransferMoneyIntent (INPaymentAccount fromAccount, INPaymentAccount toAccount, INPaymentAmount transactionAmount, INDateComponentsRange transactionScheduledDate, string transactionNote);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount FromAccount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount ToAccount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAmount TransactionAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionNote { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange TransactionScheduledDate { get; }</span>
}
</pre>
</div> <!-- end type INTransferMoneyIntent -->
<div> <!-- start type INTransferMoneyIntentHandling_Extensions -->
<h3>New Type Intents.INTransferMoneyIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INTransferMoneyIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Confirm (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INTransferMoneyIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveFromAccount (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INPaymentAccountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveToAccount (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INPaymentAccountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionAmount (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INPaymentAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionNote (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveTransactionScheduledDate (IINTransferMoneyIntentHandling This, INTransferMoneyIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INTransferMoneyIntentHandling_Extensions -->
<div> <!-- start type INTransferMoneyIntentResponse -->
<h3>New Type Intents.INTransferMoneyIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INTransferMoneyIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INTransferMoneyIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTransferMoneyIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTransferMoneyIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INTransferMoneyIntentResponse (INTransferMoneyIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INTransferMoneyIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount FromAccount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAccount ToAccount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentAmount TransactionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string TransactionNote { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange TransactionScheduledDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount TransferFee { get; set; }</span>
}
</pre>
</div> <!-- end type INTransferMoneyIntentResponse -->
<div> <!-- start type INTransferMoneyIntentResponseCode -->
<h3>New Type Intents.INTransferMoneyIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INTransferMoneyIntentResponseCode {
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
</div> <!-- end type INTransferMoneyIntentResponseCode -->
<div> <!-- start type INVisualCodeType -->
<h3>New Type Intents.INVisualCodeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INVisualCodeType {
	<span class='added added-field ' data-is-non-breaking="">Contact = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestPayment = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SendPayment = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INVisualCodeType -->
<div> <!-- start type INVisualCodeTypeResolutionResult -->
<h3>New Type Intents.INVisualCodeTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INVisualCodeTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INVisualCodeTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INVisualCodeTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INVisualCodeTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INVisualCodeTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INVisualCodeTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INVisualCodeTypeResolutionResult GetConfirmationRequired (INVisualCodeType visualCodeTypeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INVisualCodeTypeResolutionResult GetSuccess (INVisualCodeType resolvedVisualCodeType);</span>
}
</pre>
</div> <!-- end type INVisualCodeTypeResolutionResult -->

</div> <!-- end namespace Intents -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<div> <!-- start type MKFeatureDisplayPriority -->
<h3>New Type MapKit.MKFeatureDisplayPriority</h3>
<pre class='added' data-is-non-breaking="">
public static class MKFeatureDisplayPriority {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultHigh;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float DefaultLow;</span>
	<span class='added added-field ' data-is-non-breaking="">public static const float Required;</span>
}
</pre>
</div> <!-- end type MKFeatureDisplayPriority -->

</div> <!-- end namespace MapKit -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"3.2"</span> <span class='added '>"4.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.12.0"</span> <span class='added '>"10.99.7"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreBluetoothLibrary = "/System/Library/Frameworks/CoreBluetooth.framework/CoreBluetooth";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreVideoLibrary = "/System/Library/Frameworks/CoreVideo.framework/CoreVideo";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VisionLibrary = "/System/Library/Frameworks/Vision.framework/Vision";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetUInt32 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ulong GetUInt64 (IntPtr handle, string symbol);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNFloat (IntPtr handle, string symbol, nfloat value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNInt (IntPtr handle, string symbol, nint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetNUInt (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt32 (IntPtr handle, string symbol, uint value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetUInt64 (IntPtr handle, string symbol, long value);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace PassKit --> <div> 
<h2>Namespace PassKit</h2>
<!-- start type PKPaymentAuthorizationControllerDelegate --> <div>
<h3>Type Changed: PassKit.PKPaymentAuthorizationControllerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAuthorizePayment (PKPaymentAuthorizationController controller, PKPayment payment, System.Action&lt;PKPaymentAuthorizationResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectPaymentMethod (PKPaymentAuthorizationController controller, PKPaymentMethod paymentMethod, System.Action&lt;PKPaymentRequestPaymentMethodUpdate&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectShippingContact (PKPaymentAuthorizationController controller, PKContact contact, System.Action&lt;PKPaymentRequestShippingContactUpdate&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidSelectShippingMethod (PKPaymentAuthorizationController controller, PKPaymentMethod paymentMethod, System.Action&lt;PKPaymentRequestPaymentMethodUpdate&gt; completion);</span>
</pre>
</div>

</div> <!-- end type PKPaymentAuthorizationControllerDelegate -->
<!-- start type PKPaymentAuthorizationControllerDelegate_Extensions --> <div>
<h3>Type Changed: PassKit.PKPaymentAuthorizationControllerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAuthorizePayment (IPKPaymentAuthorizationControllerDelegate This, PKPaymentAuthorizationController controller, PKPayment payment, System.Action&lt;PKPaymentAuthorizationResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectPaymentMethod (IPKPaymentAuthorizationControllerDelegate This, PKPaymentAuthorizationController controller, PKPaymentMethod paymentMethod, System.Action&lt;PKPaymentRequestPaymentMethodUpdate&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectShippingContact (IPKPaymentAuthorizationControllerDelegate This, PKPaymentAuthorizationController controller, PKContact contact, System.Action&lt;PKPaymentRequestShippingContactUpdate&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSelectShippingMethod (IPKPaymentAuthorizationControllerDelegate This, PKPaymentAuthorizationController controller, PKPaymentMethod paymentMethod, System.Action&lt;PKPaymentRequestPaymentMethodUpdate&gt; completion);</span>
</pre>
</div>

</div> <!-- end type PKPaymentAuthorizationControllerDelegate_Extensions -->
<!-- start type PKPaymentNetwork --> <div>
<h3>Type Changed: PassKit.PKPaymentNetwork</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CarteBancaires { get; }</span>
</pre>
</div>

</div> <!-- end type PKPaymentNetwork -->
<!-- start type PKPaymentRequest --> <div>
<h3>Type Changed: PassKit.PKPaymentRequest</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public PKContactFields RequiredBillingContactFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PKContactFields RequiredShippingContactFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; SupportedCountries { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet WeakRequiredBillingContactFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet WeakRequiredShippingContactFields { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentBillingAddressInvalidError (Contacts.CNPostalAddressKeyOption postalAddress, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentBillingAddressInvalidError (Foundation.NSString postalAddressKey, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentContactInvalidError (Foundation.NSString field, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentContactInvalidError (PKContactFields contactField, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentShippingAddressInvalidError (Contacts.CNPostalAddressKeyOption postalAddress, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentShippingAddressInvalidError (Foundation.NSString postalAddressKey, string localizedDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSError CreatePaymentShippingAddressUnserviceableError (string localizedDescription);</span>
</pre>
</div>

</div> <!-- end type PKPaymentRequest -->
<div> <!-- start type PKContactFields -->
<h3>New Type PassKit.PKContactFields</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PKContactFields {
	<span class='added added-field ' data-is-non-breaking="">EmailAddress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Name = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PhoneNumber = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PhoneticName = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">PostalAddress = 1,</span>
}
</pre>
</div> <!-- end type PKContactFields -->
<div> <!-- start type PKContactFieldsExtensions -->
<h3>New Type PassKit.PKContactFieldsExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PKContactFieldsExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (PKContactFields self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSSet GetSet (PKContactFields values);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PKContactFields GetValue (Foundation.NSSet set);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PKContactFields GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type PKContactFieldsExtensions -->
<div> <!-- start type PKPassKitErrorCodeExtensions -->
<h3>New Type PassKit.PKPassKitErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PKPassKitErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (PKPassKitErrorCode self);</span>
}
</pre>
</div> <!-- end type PKPassKitErrorCodeExtensions -->
<div> <!-- start type PKPaymentAuthorizationResult -->
<h3>New Type PassKit.PKPaymentAuthorizationResult</h3>
<pre class='added' data-is-non-breaking="">
public class PKPaymentAuthorizationResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentAuthorizationResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentAuthorizationResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKPaymentAuthorizationResult (PKPaymentAuthorizationStatus status, Foundation.NSError[] errors);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError[] Errors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PKPaymentAuthorizationStatus Status { get; set; }</span>
}
</pre>
</div> <!-- end type PKPaymentAuthorizationResult -->
<div> <!-- start type PKPaymentErrorCode -->
<h3>New Type PassKit.PKPaymentErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PKPaymentErrorCode {
	<span class='added added-field ' data-is-non-breaking="">BillingContactInvalid = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ShippingAddressUnserviceable = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ShippingContactInvalid = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = -1,</span>
}
</pre>
</div> <!-- end type PKPaymentErrorCode -->
<div> <!-- start type PKPaymentErrorCodeExtensions -->
<h3>New Type PassKit.PKPaymentErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PKPaymentErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (PKPaymentErrorCode self);</span>
}
</pre>
</div> <!-- end type PKPaymentErrorCodeExtensions -->
<div> <!-- start type PKPaymentErrorKeys -->
<h3>New Type PassKit.PKPaymentErrorKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PKPaymentErrorKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContactFieldUserInfoKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PostalAddressUserInfoKey { get; }</span>
}
</pre>
</div> <!-- end type PKPaymentErrorKeys -->
<div> <!-- start type PKPaymentRequestPaymentMethodUpdate -->
<h3>New Type PassKit.PKPaymentRequestPaymentMethodUpdate</h3>
<pre class='added' data-is-non-breaking="">
public class PKPaymentRequestPaymentMethodUpdate : PassKit.PKPaymentRequestUpdate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestPaymentMethodUpdate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKPaymentRequestPaymentMethodUpdate (PKPaymentSummaryItem[] paymentSummaryItems);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestPaymentMethodUpdate (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type PKPaymentRequestPaymentMethodUpdate -->
<div> <!-- start type PKPaymentRequestShippingContactUpdate -->
<h3>New Type PassKit.PKPaymentRequestShippingContactUpdate</h3>
<pre class='added' data-is-non-breaking="">
public class PKPaymentRequestShippingContactUpdate : PassKit.PKPaymentRequestUpdate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestShippingContactUpdate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestShippingContactUpdate (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKPaymentRequestShippingContactUpdate (Foundation.NSError[] errors, PKPaymentSummaryItem[] paymentSummaryItems, PKShippingMethod[] shippingMethods);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSError[] Errors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PKShippingMethod[] ShippingMethods { get; set; }</span>
}
</pre>
</div> <!-- end type PKPaymentRequestShippingContactUpdate -->
<div> <!-- start type PKPaymentRequestShippingMethodUpdate -->
<h3>New Type PassKit.PKPaymentRequestShippingMethodUpdate</h3>
<pre class='added' data-is-non-breaking="">
public class PKPaymentRequestShippingMethodUpdate : PassKit.PKPaymentRequestUpdate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestShippingMethodUpdate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKPaymentRequestShippingMethodUpdate (PKPaymentSummaryItem[] paymentSummaryItems);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestShippingMethodUpdate (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type PKPaymentRequestShippingMethodUpdate -->
<div> <!-- start type PKPaymentRequestUpdate -->
<h3>New Type PassKit.PKPaymentRequestUpdate</h3>
<pre class='added' data-is-non-breaking="">
public class PKPaymentRequestUpdate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestUpdate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PKPaymentRequestUpdate (PKPaymentSummaryItem[] paymentSummaryItems);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PKPaymentRequestUpdate (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PKPaymentSummaryItem[] PaymentSummaryItems { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PKPaymentAuthorizationStatus Status { get; set; }</span>
}
</pre>
</div> <!-- end type PKPaymentRequestUpdate -->

</div> <!-- end namespace PassKit -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNBlendMode --> <div>
<h3>Type Changed: SceneKit.SCNBlendMode</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Max = 6,</span>
</pre>
</div>

</div> <!-- end type SCNBlendMode -->
<!-- start type SCNDebugOptions --> <div>
<h3>Type Changed: SceneKit.SCNDebugOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">RenderAsWireframe = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowCameras = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowConstraints = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowCreases = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">ShowSkeletons = 128,</span>
</pre>
</div>

</div> <!-- end type SCNDebugOptions -->
<!-- start type SCNHitTest --> <div>
<h3>Type Changed: SceneKit.SCNHitTest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionSearchModeKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTest -->
<!-- start type SCNHitTestOptions --> <div>
<h3>Type Changed: SceneKit.SCNHitTestOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SCNHitTestSearchMode? OptionSearchMode { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTestOptions -->
<!-- start type SCNTransparencyMode --> <div>
<h3>Type Changed: SceneKit.SCNTransparencyMode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">DualLayer = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SingleLayer = 2,</span>
</pre>
</div>

</div> <!-- end type SCNTransparencyMode -->
<div> <!-- start type SCNColorMask -->
<h3>New Type SceneKit.SCNColorMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNColorMask {
	<span class='added added-field ' data-is-non-breaking="">All = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Alpha = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Blue = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Green = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Red = 8,</span>
}
</pre>
</div> <!-- end type SCNColorMask -->
<div> <!-- start type SCNFillMode -->
<h3>New Type SceneKit.SCNFillMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNFillMode {
	<span class='added added-field ' data-is-non-breaking="">Fill = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Lines = 1,</span>
}
</pre>
</div> <!-- end type SCNFillMode -->
<div> <!-- start type SCNHitTestSearchMode -->
<h3>New Type SceneKit.SCNHitTestSearchMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNHitTestSearchMode {
	<span class='added added-field ' data-is-non-breaking="">All = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Closest = 0,</span>
}
</pre>
</div> <!-- end type SCNHitTestSearchMode -->
<div> <!-- start type SCNInteractionMode -->
<h3>New Type SceneKit.SCNInteractionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNInteractionMode {
	<span class='added added-field ' data-is-non-breaking="">Fly = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitAngleMapping = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitArcball = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitCenteredArcball = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OrbitTurntable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Pan = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Truck = 6,</span>
}
</pre>
</div> <!-- end type SCNInteractionMode -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslCipherSuite --> <div>
<h3>Type Changed: Security.SslCipherSuite</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_8_SHA256 = 4869,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_CCM_SHA256 = 4868,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_128_GCM_SHA256 = 4865,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_AES_256_GCM_SHA384 = 4866,</span>
	<span class='added added-field ' data-is-non-breaking="">TLS_CHACHA20_POLY1305_SHA256 = 4867,</span>
</pre>
</div>

</div> <!-- end type SslCipherSuite -->

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
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSAttributedString AttributedText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILineBreakMode LineBreakMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLines { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat PreferredMaxLayoutWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKLabelNode FromText (Foundation.NSAttributedString attributedText);</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
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
<!-- start type SKUniform --> <div>
<h3>Type Changed: SpriteKit.SKUniform</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat2x2)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix2 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat3x3)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix3 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat4x4)' overload instead.")]
	public SKUniform (string name, OpenTK.Matrix4 value);</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, Simd.MatrixFloat2x2 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, Simd.MatrixFloat3x3 value);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKUniform (string name, Simd.MatrixFloat4x4 value);</span>
</pre>
</div>
<p>Obsoleted properties:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat2x2Value' instead.")]
	public virtual OpenTK.Matrix2 FloatMatrix2x2Value { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'MatrixFloat3x3Value' instead.")]
	public virtual OpenTK.Matrix3 FloatMatrix3x3Value { get; set; }</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-property' data-is-non-breaking="">[Obsolete ("Use 'FloatMatrix4x4Value' instead.")]
	public virtual OpenTK.Matrix4 FloatMatrix4x4Value { get; set; }</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Simd.MatrixFloat2x2 MatrixFloat2x2Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Simd.MatrixFloat3x3 MatrixFloat3x3Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Simd.MatrixFloat4x4 MatrixFloat4x4Value { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat2x2)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix2 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the '(string, MatrixFloat3x3)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix3 value);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'the '(string, MatrixFloat4x4)' overload instead.")]
	public static SKUniform Create (string name, OpenTK.Matrix4 value);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, Simd.MatrixFloat2x2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, Simd.MatrixFloat3x3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKUniform Create (string name, Simd.MatrixFloat4x4 value);</span>
</pre>
</div>

</div> <!-- end type SKUniform -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Simd.MatrixFloat3x3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->
<div> <!-- start type SKVideoNode -->
<h3>New Type SpriteKit.SKVideoNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKVideoNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKVideoNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKVideoNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKVideoNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKVideoNode (Foundation.NSUrl url);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKVideoNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKVideoNode (string videoFile);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKVideoNode VideoNodeWithFileNamed (string videoFile);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKVideoNode VideoNodeWithURL (Foundation.NSUrl videoURL);</span>
}
</pre>
</div> <!-- end type SKVideoNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSCoder_UIGeometryKeyedCoding --> <div>
<h3>Type Changed: UIKit.NSCoder_UIGeometryKeyedCoding</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSDirectionalEdgeInsets DecodeDirectionalEdgeInsets (Foundation.NSCoder This, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Encode (Foundation.NSCoder This, NSDirectionalEdgeInsets directionalEdgeInsets, string forKey);</span>
</pre>
</div>

</div> <!-- end type NSCoder_UIGeometryKeyedCoding -->
<!-- start type UIBezierPath --> <div>
<h3>Type Changed: UIKit.UIBezierPath</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type UIBezierPath -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name);</span>
</pre>
</div>

</div> <!-- end type UIColor -->
<!-- start type UIFontTextStyle --> <div>
<h3>Type Changed: UIKit.UIFontTextStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LargeTitle = 10,</span>
</pre>
</div>

</div> <!-- end type UIFontTextStyle -->
<div> <!-- start type NSDirectionalEdgeInsets -->
<h3>New Type UIKit.NSDirectionalEdgeInsets</h3>
<pre class='added' data-is-non-breaking="">
public struct NSDirectionalEdgeInsets {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSDirectionalEdgeInsets (nfloat top, nfloat leading, nfloat bottom, nfloat trailing);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public nfloat Bottom;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Leading;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Top;</span>
	<span class='added added-field ' data-is-non-breaking="">public nfloat Trailing;</span>
	<span class='added added-field ' data-is-non-breaking="">public static NSDirectionalEdgeInsets Zero;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (NSDirectionalEdgeInsets other);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSDirectionalEdgeInsets FromString (string s);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NSDirectionalEdgeInsets insets1, NSDirectionalEdgeInsets insets2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NSDirectionalEdgeInsets insets1, NSDirectionalEdgeInsets insets2);</span>
}
</pre>
</div> <!-- end type NSDirectionalEdgeInsets -->
<div> <!-- start type UIFontMetrics -->
<h3>New Type UIKit.UIFontMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class UIFontMetrics : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFontMetrics (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFontMetrics (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIFontMetrics (string textStyle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static UIFontMetrics DefaultMetrics { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIFontMetrics GetMetrics (string textStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIFont GetScaledFont (UIFont font, nfloat maximumPointSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetScaledValue (nfloat value);</span>
}
</pre>
</div> <!-- end type UIFontMetrics -->
<div> <!-- start type UIPreferredPresentationStyle -->
<h3>New Type UIKit.UIPreferredPresentationStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIPreferredPresentationStyle {
	<span class='added added-field ' data-is-non-breaking="">Attachment = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Inline = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type UIPreferredPresentationStyle -->

</div> <!-- end namespace UIKit -->
<!-- start namespace UserNotifications --> <div> 
<h2>Namespace UserNotifications</h2>
<!-- start type UNNotificationCategoryOptions --> <div>
<h3>Type Changed: UserNotifications.UNNotificationCategoryOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HiddenPreviewsShowSubtitle = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HiddenPreviewsShowTitle = 4,</span>
</pre>
</div>

</div> <!-- end type UNNotificationCategoryOptions -->

</div> <!-- end namespace UserNotifications -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKAccessibility --> <div>
<h3>Type Changed: WatchKit.WKAccessibility</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsReduceMotionEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReduceMotionStatusDidChangeNotification { get; }</span>
</pre>
</div>
<!-- start type WKAccessibility.Notifications --> <div>
<h3>Type Changed: WatchKit.WKAccessibility.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveReduceMotionStatusDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type WKAccessibility.Notifications -->

</div> <!-- end type WKAccessibility -->
<!-- start type WKExtension --> <div>
<h3>Type Changed: WatchKit.WKExtension</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Autorotating { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FrontmostTimeoutExtended { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsApplicationRunningInDock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKInterfaceController VisibleInterfaceController { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnableWaterLock ();</span>
</pre>
</div>

</div> <!-- end type WKExtension -->
<!-- start type WKExtensionDelegate --> <div>
<h3>Type Changed: WatchKit.WKExtensionDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DeviceOrientationDidChange ();</span>
</pre>
</div>

</div> <!-- end type WKExtensionDelegate -->
<!-- start type WKExtensionDelegate_Extensions --> <div>
<h3>Type Changed: WatchKit.WKExtensionDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DeviceOrientationDidChange (IWKExtensionDelegate This);</span>
</pre>
</div>

</div> <!-- end type WKExtensionDelegate_Extensions -->
<!-- start type WKInterfaceController --> <div>
<h3>Type Changed: WatchKit.WKInterfaceController</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>public</span> WKInterfaceController ()
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InterfaceDidScrollToTop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InterfaceOffsetDidScrollToBottom ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InterfaceOffsetDidScrollToTop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ReloadRootPageControllers (string[] names, Foundation.NSObject[] contexts, WKPageOrientation orientation, nint pageIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScrollTo (WKInterfaceObject object, WKInterfaceScrollPosition scrollPosition, bool animated);</span>
</pre>
</div>

</div> <!-- end type WKInterfaceController -->
<!-- start type WKInterfaceDevice --> <div>
<h3>Type Changed: WatchKit.WKInterfaceDevice</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual float BatteryLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool BatteryMonitoringEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKInterfaceDeviceBatteryState BatteryState { get; }</span>
</pre>
</div>

</div> <!-- end type WKInterfaceDevice -->
<!-- start type WKRefreshBackgroundTask --> <div>
<h3>Type Changed: WatchKit.WKRefreshBackgroundTask</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTaskCompleted (bool refreshSnapshot);</span>
</pre>
</div>

</div> <!-- end type WKRefreshBackgroundTask -->
<!-- start type WKSnapshotRefreshBackgroundTask --> <div>
<h3>Type Changed: WatchKit.WKSnapshotRefreshBackgroundTask</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual WKSnapshotReason ReasonForSnapshot { get; }</span>
</pre>
</div>

</div> <!-- end type WKSnapshotRefreshBackgroundTask -->
<div> <!-- start type WKInterfaceDeviceBatteryState -->
<h3>New Type WatchKit.WKInterfaceDeviceBatteryState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WKInterfaceDeviceBatteryState {
	<span class='added added-field ' data-is-non-breaking="">Charging = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Full = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unplugged = 1,</span>
}
</pre>
</div> <!-- end type WKInterfaceDeviceBatteryState -->
<div> <!-- start type WKInterfaceScrollPosition -->
<h3>New Type WatchKit.WKInterfaceScrollPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WKInterfaceScrollPosition {
	<span class='added added-field ' data-is-non-breaking="">Bottom = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">CenteredVertically = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Top = 0,</span>
}
</pre>
</div> <!-- end type WKInterfaceScrollPosition -->
<div> <!-- start type WKPageOrientation -->
<h3>New Type WatchKit.WKPageOrientation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WKPageOrientation {
	<span class='added added-field ' data-is-non-breaking="">Horizontal = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Vertical = 1,</span>
}
</pre>
</div> <!-- end type WKPageOrientation -->
<div> <!-- start type WKSnapshotReason -->
<h3>New Type WatchKit.WKSnapshotReason</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum WKSnapshotReason {
	<span class='added added-field ' data-is-non-breaking="">AppBackgrounded = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AppScheduled = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ComplicationUpdate = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Prelaunch = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">ReturnToDefaultState = 1,</span>
}
</pre>
</div> <!-- end type WKSnapshotReason -->

</div> <!-- end namespace WatchKit -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>New Namespace CoreBluetooth</h2>

<div> <!-- start type AdvertisementData -->
<h3>New Type CoreBluetooth.AdvertisementData</h3>
<pre class='added' data-is-non-breaking="">
public class AdvertisementData : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? IsConnectable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string LocalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ManufacturerData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] OverflowServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary&lt;CBUUID,Foundation.NSData&gt; ServiceData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] ServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] SolicitedServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber TxPowerLevel { get; set; }</span>
}
</pre>
</div> <!-- end type AdvertisementData -->
<div> <!-- start type CBATTError -->
<h3>New Type CoreBluetooth.CBATTError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBATTError {
	<span class='added added-field ' data-is-non-breaking="">AttributeNotFound = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">AttributeNotLong = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientAuthentication = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientAuthorization = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientEncryption = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientEncryptionKeySize = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientResources = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAttributeValueLength = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidHandle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOffset = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidPdu = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PrepareQueueFull = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadNotPermitted = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestNotSupported = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UnlikelyError = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedGroupType = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteNotPermitted = 3,</span>
}
</pre>
</div> <!-- end type CBATTError -->
<div> <!-- start type CBATTErrorExtensions -->
<h3>New Type CoreBluetooth.CBATTErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CBATTErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (CBATTError self);</span>
}
</pre>
</div> <!-- end type CBATTErrorExtensions -->
<div> <!-- start type CBATTRequest -->
<h3>New Type CoreBluetooth.CBATTRequest</h3>
<pre class='added' data-is-non-breaking="">
public class CBATTRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBATTRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBATTRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCentral Central { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCharacteristic Characteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Offset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Value { get; set; }</span>
}
</pre>
</div> <!-- end type CBATTRequest -->
<div> <!-- start type CBATTRequestEventArgs -->
<h3>New Type CoreBluetooth.CBATTRequestEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBATTRequestEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBATTRequestEventArgs (CBATTRequest request);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBATTRequest Request { get; set; }</span>
}
</pre>
</div> <!-- end type CBATTRequestEventArgs -->
<div> <!-- start type CBATTRequestsEventArgs -->
<h3>New Type CoreBluetooth.CBATTRequestsEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBATTRequestsEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBATTRequestsEventArgs (CBATTRequest[] requests);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBATTRequest[] Requests { get; set; }</span>
}
</pre>
</div> <!-- end type CBATTRequestsEventArgs -->
<div> <!-- start type CBAdvertisement -->
<h3>New Type CoreBluetooth.CBAdvertisement</h3>
<pre class='added' data-is-non-breaking="">
public static class CBAdvertisement {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataLocalNameKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataManufacturerDataKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataOverflowServiceUUIDsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataServiceDataKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataServiceUUIDsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataSolicitedServiceUUIDsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DataTxPowerLevelKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsConnectable { get; }</span>
}
</pre>
</div> <!-- end type CBAdvertisement -->
<div> <!-- start type CBAttribute -->
<h3>New Type CoreBluetooth.CBAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class CBAttribute : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBAttribute ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBAttribute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBAttribute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBUUID UUID { get; set; }</span>
}
</pre>
</div> <!-- end type CBAttribute -->
<div> <!-- start type CBAttributePermissions -->
<h3>New Type CoreBluetooth.CBAttributePermissions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CBAttributePermissions {
	<span class='added added-field ' data-is-non-breaking="">ReadEncryptionRequired = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Readable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteEncryptionRequired = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Writeable = 2,</span>
}
</pre>
</div> <!-- end type CBAttributePermissions -->
<div> <!-- start type CBCentral -->
<h3>New Type CoreBluetooth.CBCentral</h3>
<pre class='added' data-is-non-breaking="">
public class CBCentral : CoreBluetooth.CBPeer, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentral (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentral (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumUpdateValueLength { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type CBCentral -->
<div> <!-- start type CBCentralInitOptions -->
<h3>New Type CoreBluetooth.CBCentralInitOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CBCentralInitOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralInitOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralInitOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string RestoreIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? ShowPowerAlert { get; set; }</span>
}
</pre>
</div> <!-- end type CBCentralInitOptions -->
<div> <!-- start type CBCentralManager -->
<h3>New Type CoreBluetooth.CBCentralManager</h3>
<pre class='added' data-is-non-breaking="">
public class CBCentralManager : CoreBluetooth.CBManager, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralManager (CoreFoundation.DispatchQueue dispatchQueue);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentralManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentralManager (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, CBCentralInitOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ICBCentralManagerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsScanning { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionNotifyOnConnectionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionNotifyOnDisconnectionKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionNotifyOnNotificationKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionRestoreIdentifierKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionShowPowerAlertKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStatePeripheralsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateScanOptionsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateScanServicesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScanOptionAllowDuplicatesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ScanOptionSolicitedServiceUUIDsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralEventArgs&gt; ConnectedPeripheral;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralErrorEventArgs&gt; DisconnectedPeripheral;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBDiscoveredPeripheralEventArgs&gt; DiscoveredPeripheral;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralErrorEventArgs&gt; FailedToConnectPeripheral;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler UpdatedState;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelPeripheralConnection (CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ConnectPeripheral (CBPeripheral peripheral, PeripheralConnectionOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConnectPeripheral (CBPeripheral peripheral, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (Foundation.NSUuid[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScanForPeripherals (CBUUID serviceUuid);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScanForPeripherals (CBUUID[] peripheralUuids);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScanForPeripherals (CBUUID serviceUuid, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScanForPeripherals (CBUUID[] peripheralUuids, PeripheralScanningOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void ScanForPeripherals (CBUUID[] peripheralUuids, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopScan ();</span>
}
</pre>
</div> <!-- end type CBCentralManager -->
<div> <!-- start type CBCentralManagerDelegate -->
<h3>New Type CoreBluetooth.CBCentralManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CBCentralManagerDelegate : Foundation.NSObject, ICBCentralManagerDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentralManagerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentralManagerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCentralManagerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, Foundation.NSDictionary advertisementData, Foundation.NSNumber RSSI);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedState (CBCentralManager central);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillRestoreState (CBCentralManager central, Foundation.NSDictionary dict);</span>
}
</pre>
</div> <!-- end type CBCentralManagerDelegate -->
<div> <!-- start type CBCentralManagerDelegate_Extensions -->
<h3>New Type CoreBluetooth.CBCentralManagerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CBCentralManagerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DisconnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DiscoveredPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, Foundation.NSDictionary advertisementData, Foundation.NSNumber RSSI);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void FailedToConnectPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillRestoreState (ICBCentralManagerDelegate This, CBCentralManager central, Foundation.NSDictionary dict);</span>
}
</pre>
</div> <!-- end type CBCentralManagerDelegate_Extensions -->
<div> <!-- start type CBCharacteristic -->
<h3>New Type CoreBluetooth.CBCharacteristic</h3>
<pre class='added' data-is-non-breaking="">
public class CBCharacteristic : CoreBluetooth.CBAttribute, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCharacteristic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBCharacteristic (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBDescriptor[] Descriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsBroadcasted { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsNotifying { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCharacteristicProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBService Service { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Value { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type CBCharacteristic -->
<div> <!-- start type CBCharacteristicEventArgs -->
<h3>New Type CoreBluetooth.CBCharacteristicEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBCharacteristicEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBCharacteristicEventArgs (CBCharacteristic characteristic, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBCharacteristicEventArgs -->
<div> <!-- start type CBCharacteristicProperties -->
<h3>New Type CoreBluetooth.CBCharacteristicProperties</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CBCharacteristicProperties {
	<span class='added added-field ' data-is-non-breaking="">AuthenticatedSignedWrites = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Broadcast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtendedProperties = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Indicate = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">IndicateEncryptionRequired = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">Notify = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">NotifyEncryptionRequired = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Write = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteWithoutResponse = 4,</span>
}
</pre>
</div> <!-- end type CBCharacteristicProperties -->
<div> <!-- start type CBCharacteristicWriteType -->
<h3>New Type CoreBluetooth.CBCharacteristicWriteType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBCharacteristicWriteType {
	<span class='added added-field ' data-is-non-breaking="">WithResponse = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">WithoutResponse = 1,</span>
}
</pre>
</div> <!-- end type CBCharacteristicWriteType -->
<div> <!-- start type CBDescriptor -->
<h3>New Type CoreBluetooth.CBDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CBDescriptor : CoreBluetooth.CBAttribute, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCharacteristic Characteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Value { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type CBDescriptor -->
<div> <!-- start type CBDescriptorEventArgs -->
<h3>New Type CoreBluetooth.CBDescriptorEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBDescriptorEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBDescriptorEventArgs (CBDescriptor descriptor, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBDescriptor Descriptor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBDescriptorEventArgs -->
<div> <!-- start type CBDiscoveredPeripheralEventArgs -->
<h3>New Type CoreBluetooth.CBDiscoveredPeripheralEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBDiscoveredPeripheralEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBDiscoveredPeripheralEventArgs (CBPeripheral peripheral, Foundation.NSDictionary advertisementData, Foundation.NSNumber RSSI);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary AdvertisementData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral Peripheral { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber RSSI { get; set; }</span>
}
</pre>
</div> <!-- end type CBDiscoveredPeripheralEventArgs -->
<div> <!-- start type CBError -->
<h3>New Type CoreBluetooth.CBError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBError {
	<span class='added added-field ' data-is-non-breaking="">AlreadyAdvertising = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionFailed = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionLimitReached = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionTimeout = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidHandle = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidParameters = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConnected = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationCancelled = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfSpace = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PeripheralDisconnected = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">UUIDNotAllowed = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownDevice = 12,</span>
}
</pre>
</div> <!-- end type CBError -->
<div> <!-- start type CBErrorExtensions -->
<h3>New Type CoreBluetooth.CBErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CBErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (CBError self);</span>
}
</pre>
</div> <!-- end type CBErrorExtensions -->
<div> <!-- start type CBL2CapChannel -->
<h3>New Type CoreBluetooth.CBL2CapChannel</h3>
<pre class='added' data-is-non-breaking="">
public class CBL2CapChannel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBL2CapChannel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBL2CapChannel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBL2CapChannel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSInputStream InputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSOutputStream OutputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBPeer Peer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ushort Psm { get; }</span>
}
</pre>
</div> <!-- end type CBL2CapChannel -->
<div> <!-- start type CBManager -->
<h3>New Type CoreBluetooth.CBManager</h3>
<pre class='added' data-is-non-breaking="">
public class CBManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBManagerState State { get; }</span>
}
</pre>
</div> <!-- end type CBManager -->
<div> <!-- start type CBManagerState -->
<h3>New Type CoreBluetooth.CBManagerState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBManagerState {
	<span class='added added-field ' data-is-non-breaking="">PoweredOff = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PoweredOn = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Resetting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unauthorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 2,</span>
}
</pre>
</div> <!-- end type CBManagerState -->
<div> <!-- start type CBMutableCharacteristic -->
<h3>New Type CoreBluetooth.CBMutableCharacteristic</h3>
<pre class='added' data-is-non-breaking="">
public class CBMutableCharacteristic : CoreBluetooth.CBCharacteristic, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableCharacteristic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableCharacteristic (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CBDescriptor[] Descriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBAttributePermissions Permissions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CBCharacteristicProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCentral[] SubscribedCentrals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override Foundation.NSData Value { get; set; }</span>
}
</pre>
</div> <!-- end type CBMutableCharacteristic -->
<div> <!-- start type CBMutableDescriptor -->
<h3>New Type CoreBluetooth.CBMutableDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class CBMutableDescriptor : CoreBluetooth.CBDescriptor, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type CBMutableDescriptor -->
<div> <!-- start type CBMutableService -->
<h3>New Type CoreBluetooth.CBMutableService</h3>
<pre class='added' data-is-non-breaking="">
public class CBMutableService : CoreBluetooth.CBService, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableService (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBMutableService (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override CBCharacteristic[] Characteristics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override CBService[] IncludedServices { get; set; }</span>
}
</pre>
</div> <!-- end type CBMutableService -->
<div> <!-- start type CBPeer -->
<h3>New Type CoreBluetooth.CBPeer</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeer : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Identifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type CBPeer -->
<div> <!-- start type CBPeripheral -->
<h3>New Type CoreBluetooth.CBPeripheral</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheral : CoreBluetooth.CBPeer, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheral (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheral (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanSendWriteWithoutResponse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ICBPeripheralDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBService[] Services { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBPeripheralState State { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralOpenL2CapChannelEventArgs&gt; DidOpenL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBServiceEventArgs&gt; DiscoveredCharacteristic;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBCharacteristicEventArgs&gt; DiscoveredDescriptor;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBServiceEventArgs&gt; DiscoveredIncludedService;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;Foundation.NSErrorEventArgs&gt; DiscoveredService;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler IsReadyToSendWriteWithoutResponse;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralServicesEventArgs&gt; ModifiedServices;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBRssiEventArgs&gt; RssiRead;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;Foundation.NSErrorEventArgs&gt; RssiUpdated;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBCharacteristicEventArgs&gt; UpdatedCharacterteristicValue;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler UpdatedName;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBCharacteristicEventArgs&gt; UpdatedNotificationState;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBDescriptorEventArgs&gt; UpdatedValue;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBCharacteristicEventArgs&gt; WroteCharacteristicValue;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBDescriptorEventArgs&gt; WroteDescriptorValue;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DiscoverCharacteristics (CBService forService);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DiscoverCharacteristics (CBUUID[] charactersticUUIDs, CBService forService);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverDescriptors (CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DiscoverIncludedServices (CBUUID[] includedServiceUUIDs, CBService forService);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DiscoverServices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void DiscoverServices (CBUUID[] services);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetMaximumWriteValueLength (CBCharacteristicWriteType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenL2CapChannel (ushort psm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadRSSI ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadValue (CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadValue (CBDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNotifyValue (bool enabled, CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteValue (Foundation.NSData data, CBDescriptor descriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteValue (Foundation.NSData data, CBCharacteristic characteristic, CBCharacteristicWriteType type);</span>
}
</pre>
</div> <!-- end type CBPeripheral -->
<div> <!-- start type CBPeripheralDelegate -->
<h3>New Type CoreBluetooth.CBPeripheralDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralDelegate : Foundation.NSObject, ICBPeripheralDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOpenL2CapChannel (CBPeripheral peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoveredCharacteristic (CBPeripheral peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoveredDescriptor (CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoveredIncludedService (CBPeripheral peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoveredService (CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void IsReadyToSendWriteWithoutResponse (CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ModifiedServices (CBPeripheral peripheral, CBService[] services);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RssiRead (CBPeripheral peripheral, Foundation.NSNumber rssi, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RssiUpdated (CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedCharacterteristicValue (CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedName (CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedNotificationState (CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedValue (CBPeripheral peripheral, CBDescriptor descriptor, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WroteCharacteristicValue (CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WroteDescriptorValue (CBPeripheral peripheral, CBDescriptor descriptor, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CBPeripheralDelegate -->
<div> <!-- start type CBPeripheralDelegate_Extensions -->
<h3>New Type CoreBluetooth.CBPeripheralDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CBPeripheralDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidOpenL2CapChannel (ICBPeripheralDelegate This, CBPeripheral peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DiscoveredCharacteristic (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DiscoveredDescriptor (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DiscoveredIncludedService (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DiscoveredService (ICBPeripheralDelegate This, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsReadyToSendWriteWithoutResponse (ICBPeripheralDelegate This, CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ModifiedServices (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService[] services);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RssiRead (ICBPeripheralDelegate This, CBPeripheral peripheral, Foundation.NSNumber rssi, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RssiUpdated (ICBPeripheralDelegate This, CBPeripheral peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UpdatedCharacterteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UpdatedName (ICBPeripheralDelegate This, CBPeripheral peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UpdatedNotificationState (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void UpdatedValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WroteCharacteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WroteDescriptorValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CBPeripheralDelegate_Extensions -->
<div> <!-- start type CBPeripheralErrorEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralErrorEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralErrorEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralErrorEventArgs (CBPeripheral peripheral, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral Peripheral { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralErrorEventArgs -->
<div> <!-- start type CBPeripheralEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralEventArgs (CBPeripheral peripheral);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral Peripheral { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralEventArgs -->
<div> <!-- start type CBPeripheralManager -->
<h3>New Type CoreBluetooth.CBPeripheralManager</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManager : CoreBluetooth.CBManager, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Advertising { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CBPeripheralManagerAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ICBPeripheralManagerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionRestoreIdentifierKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionShowPowerAlertKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateAdvertisementDataKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RestoredStateServicesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;Foundation.NSErrorEventArgs&gt; AdvertisingStarted;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerSubscriptionEventArgs&gt; CharacteristicSubscribed;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerSubscriptionEventArgs&gt; CharacteristicUnsubscribed;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerOpenL2CapChannelEventArgs&gt; DidOpenL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerL2CapChannelOperationEventArgs&gt; DidPublishL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerL2CapChannelOperationEventArgs&gt; DidUnpublishL2CapChannel;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBATTRequestEventArgs&gt; ReadRequestReceived;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler ReadyToUpdateSubscribers;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBPeripheralManagerServiceEventArgs&gt; ServiceAdded;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler StateUpdated;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;CBATTRequestsEventArgs&gt; WriteRequestsReceived;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddService (CBMutableService service);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PublishL2CapChannel (bool encryptionRequired);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllServices ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveService (CBMutableService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RespondToRequest (CBATTRequest request, CBATTError result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDesiredConnectionLatency (CBPeripheralManagerConnectionLatency latency, CBCentral connectedCentral);</span>
	<span class='added added-method ' data-is-non-breaking="">public void StartAdvertising (StartAdvertisingOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartAdvertising (Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopAdvertising ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnpublishL2CapChannel (ushort psm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool UpdateValue (Foundation.NSData value, CBMutableCharacteristic characteristic, CBCentral[] subscribedCentrals);</span>
}
</pre>
</div> <!-- end type CBPeripheralManager -->
<div> <!-- start type CBPeripheralManagerAuthorizationStatus -->
<h3>New Type CoreBluetooth.CBPeripheralManagerAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBPeripheralManagerAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerAuthorizationStatus -->
<div> <!-- start type CBPeripheralManagerConnectionLatency -->
<h3>New Type CoreBluetooth.CBPeripheralManagerConnectionLatency</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBPeripheralManagerConnectionLatency {
	<span class='added added-field ' data-is-non-breaking="">High = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Low = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Medium = 1,</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerConnectionLatency -->
<div> <!-- start type CBPeripheralManagerDelegate -->
<h3>New Type CoreBluetooth.CBPeripheralManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CBPeripheralManagerDelegate : Foundation.NSObject, ICBPeripheralManagerDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralManagerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralManagerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBPeripheralManagerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AdvertisingStarted (CBPeripheralManager peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CharacteristicSubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CharacteristicUnsubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidOpenL2CapChannel (CBPeripheralManager peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidPublishL2CapChannel (CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnpublishL2CapChannel (CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadRequestReceived (CBPeripheralManager peripheral, CBATTRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadyToUpdateSubscribers (CBPeripheralManager peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ServiceAdded (CBPeripheralManager peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StateUpdated (CBPeripheralManager peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillRestoreState (CBPeripheralManager peripheral, Foundation.NSDictionary dict);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteRequestsReceived (CBPeripheralManager peripheral, CBATTRequest[] requests);</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerDelegate -->
<div> <!-- start type CBPeripheralManagerDelegate_Extensions -->
<h3>New Type CoreBluetooth.CBPeripheralManagerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CBPeripheralManagerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AdvertisingStarted (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CharacteristicSubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CharacteristicUnsubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidOpenL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBL2CapChannel channel, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidPublishL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnpublishL2CapChannel (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, ushort psm, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ReadRequestReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ReadyToUpdateSubscribers (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ServiceAdded (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBService service, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillRestoreState (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, Foundation.NSDictionary dict);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WriteRequestsReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest[] requests);</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerDelegate_Extensions -->
<div> <!-- start type CBPeripheralManagerL2CapChannelOperationEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerL2CapChannelOperationEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerL2CapChannelOperationEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerL2CapChannelOperationEventArgs (ushort psm, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ushort Psm { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerL2CapChannelOperationEventArgs -->
<div> <!-- start type CBPeripheralManagerOpenL2CapChannelEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerOpenL2CapChannelEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerOpenL2CapChannelEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerOpenL2CapChannelEventArgs (CBL2CapChannel channel, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBL2CapChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerOpenL2CapChannelEventArgs -->
<div> <!-- start type CBPeripheralManagerServiceEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerServiceEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerServiceEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerServiceEventArgs (CBService service, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBService Service { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerServiceEventArgs -->
<div> <!-- start type CBPeripheralManagerSubscriptionEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralManagerSubscriptionEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManagerSubscriptionEventArgs (CBCentral central, CBCharacteristic characteristic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBCentral Central { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBCharacteristic Characteristic { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralManagerSubscriptionEventArgs -->
<div> <!-- start type CBPeripheralOpenL2CapChannelEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralOpenL2CapChannelEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralOpenL2CapChannelEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralOpenL2CapChannelEventArgs (CBL2CapChannel channel, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBL2CapChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralOpenL2CapChannelEventArgs -->
<div> <!-- start type CBPeripheralServicesEventArgs -->
<h3>New Type CoreBluetooth.CBPeripheralServicesEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBPeripheralServicesEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralServicesEventArgs (CBService[] services);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBService[] Services { get; set; }</span>
}
</pre>
</div> <!-- end type CBPeripheralServicesEventArgs -->
<div> <!-- start type CBPeripheralState -->
<h3>New Type CoreBluetooth.CBPeripheralState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBPeripheralState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connecting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnected = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disconnecting = 3,</span>
}
</pre>
</div> <!-- end type CBPeripheralState -->
<div> <!-- start type CBRssiEventArgs -->
<h3>New Type CoreBluetooth.CBRssiEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBRssiEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBRssiEventArgs (Foundation.NSNumber rssi, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Rssi { get; set; }</span>
}
</pre>
</div> <!-- end type CBRssiEventArgs -->
<div> <!-- start type CBService -->
<h3>New Type CoreBluetooth.CBService</h3>
<pre class='added' data-is-non-breaking="">
public class CBService : CoreBluetooth.CBAttribute, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBService (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBService (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CBCharacteristic[] Characteristics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBService[] IncludedServices { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBPeripheral Peripheral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Primary { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type CBService -->
<div> <!-- start type CBServiceEventArgs -->
<h3>New Type CoreBluetooth.CBServiceEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBServiceEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBServiceEventArgs (CBService service, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBService Service { get; set; }</span>
}
</pre>
</div> <!-- end type CBServiceEventArgs -->
<div> <!-- start type CBUUID -->
<h3>New Type CoreBluetooth.CBUUID</h3>
<pre class='added' data-is-non-breaking="">
public class CBUUID : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;CBUUID&gt;, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBUUID (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBUUID (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicAggregateFormatString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicExtendedPropertiesString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicFormatString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicUserDescriptionString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicValidRangeString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClientCharacteristicConfigurationString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString L2CapPsmCharacteristicString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServerCharacteristicConfigurationString { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (CBUUID obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CBUUID FromBytes (byte[] bytes);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CBUUID FromData (Foundation.NSData theData);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CBUUID FromNSUuid (Foundation.NSUuid theUUID);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CBUUID FromPartial (ushort servicePart);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CBUUID FromString (string theString);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public string ToString (bool fullUuid);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (CBUUID a, CBUUID b);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (CBUUID a, CBUUID b);</span>
}
</pre>
</div> <!-- end type CBUUID -->
<div> <!-- start type CBWillRestoreEventArgs -->
<h3>New Type CoreBluetooth.CBWillRestoreEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class CBWillRestoreEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CBWillRestoreEventArgs (Foundation.NSDictionary dict);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary Dict { get; set; }</span>
}
</pre>
</div> <!-- end type CBWillRestoreEventArgs -->
<div> <!-- start type ICBCentralManagerDelegate -->
<h3>New Type CoreBluetooth.ICBCentralManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ICBCentralManagerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdatedState (CBCentralManager central);</span>
}
</pre>
</div> <!-- end type ICBCentralManagerDelegate -->
<div> <!-- start type ICBPeripheralDelegate -->
<h3>New Type CoreBluetooth.ICBPeripheralDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ICBPeripheralDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ICBPeripheralDelegate -->
<div> <!-- start type ICBPeripheralManagerDelegate -->
<h3>New Type CoreBluetooth.ICBPeripheralManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ICBPeripheralManagerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StateUpdated (CBPeripheralManager peripheral);</span>
}
</pre>
</div> <!-- end type ICBPeripheralManagerDelegate -->
<div> <!-- start type PeripheralConnectionOptions -->
<h3>New Type CoreBluetooth.PeripheralConnectionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PeripheralConnectionOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PeripheralConnectionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PeripheralConnectionOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? NotifyOnConnection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NotifyOnDisconnection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NotifyOnNotification { get; set; }</span>
}
</pre>
</div> <!-- end type PeripheralConnectionOptions -->
<div> <!-- start type PeripheralScanningOptions -->
<h3>New Type CoreBluetooth.PeripheralScanningOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PeripheralScanningOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PeripheralScanningOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PeripheralScanningOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool AllowDuplicatesKey { get; set; }</span>
}
</pre>
</div> <!-- end type PeripheralScanningOptions -->
<div> <!-- start type RestoredState -->
<h3>New Type CoreBluetooth.RestoredState</h3>
<pre class='added' data-is-non-breaking="">
public class RestoredState : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] Peripherals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PeripheralScanningOptions ScanOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] ScanServices { get; set; }</span>
}
</pre>
</div> <!-- end type RestoredState -->
<div> <!-- start type StartAdvertisingOptions -->
<h3>New Type CoreBluetooth.StartAdvertisingOptions</h3>
<pre class='added' data-is-non-breaking="">
public class StartAdvertisingOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public StartAdvertisingOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public StartAdvertisingOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string LocalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] ServicesUUID { get; set; }</span>
}
</pre>
</div> <!-- end type StartAdvertisingOptions -->
</div> <!-- end namespace CoreBluetooth -->

<!-- start namespace CoreML --> <div> 
<h2>New Namespace CoreML</h2>

<div> <!-- start type IMLFeatureProvider -->
<h3>New Type CoreML.IMLFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IMLFeatureProvider : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type IMLFeatureProvider -->
<div> <!-- start type MLDictionaryConstraint -->
<h3>New Type CoreML.MLDictionaryConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType KeyType { get; }</span>
}
</pre>
</div> <!-- end type MLDictionaryConstraint -->
<div> <!-- start type MLDictionaryFeatureProvider -->
<h3>New Type CoreML.MLDictionaryFeatureProvider</h3>
<pre class='added' data-is-non-breaking="">
public class MLDictionaryFeatureProvider : Foundation.NSObject, IMLFeatureProvider, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLDictionaryFeatureProvider (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLDictionaryFeatureProvider (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; dictionary, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureValue&gt; Dictionary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet&lt;Foundation.NSString&gt; FeatureNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLFeatureValue Item { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MLFeatureValue GetFeatureValue (string featureName);</span>
}
</pre>
</div> <!-- end type MLDictionaryFeatureProvider -->
<div> <!-- start type MLFeatureDescription -->
<h3>New Type CoreML.MLFeatureDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLDictionaryConstraint DictionaryConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLImageConstraint ImageConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayConstraint MultiArrayConstraint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Optional { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsAllowed (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureDescription -->
<div> <!-- start type MLFeatureType -->
<h3>New Type CoreML.MLFeatureType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLFeatureType {
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Double = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Int64 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">MultiArray = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 3,</span>
}
</pre>
</div> <!-- end type MLFeatureType -->
<div> <!-- start type MLFeatureValue -->
<h3>New Type CoreML.MLFeatureValue</h3>
<pre class='added' data-is-non-breaking="">
public class MLFeatureValue : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLFeatureValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLFeatureValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; DictionaryValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer ImageBufferValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual long Int64Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArray MultiArrayValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string StringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLFeatureType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Undefined { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue CreateUndefined (MLFeatureType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDictionary (Foundation.NSDictionary&lt;Foundation.NSObject,Foundation.NSNumber&gt; value, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromDouble (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromInt64 (long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromMultiArray (MLMultiArray value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromPixelBuffer (CoreVideo.CVPixelBuffer value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLFeatureValue FromString (string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqual (MLFeatureValue value);</span>
}
</pre>
</div> <!-- end type MLFeatureValue -->
<div> <!-- start type MLImageConstraint -->
<h3>New Type CoreML.MLImageConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLImageConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLImageConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelFormatType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsHigh { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PixelsWide { get; }</span>
}
</pre>
</div> <!-- end type MLImageConstraint -->
<div> <!-- start type MLModel -->
<h3>New Type CoreML.MLModel</h3>
<pre class='added' data-is-non-breaking="">
public class MLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLModelDescription ModelDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl CompileModel (Foundation.NSUrl modelUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MLModel FromUrl (Foundation.NSUrl url, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual IMLFeatureProvider GetPrediction (IMLFeatureProvider input, MLPredictionOptions options, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MLModel -->
<div> <!-- start type MLModelDescription -->
<h3>New Type CoreML.MLModelDescription</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelDescription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLModelDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; InputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MLModelMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,CoreML.MLFeatureDescription&gt; OutputDescriptionsByName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedFeatureName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PredictedProbabilitiesName { get; }</span>
}
</pre>
</div> <!-- end type MLModelDescription -->
<div> <!-- start type MLModelError -->
<h3>New Type CoreML.MLModelError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLModelError {
	<span class='added added-field ' data-is-non-breaking="">FeatureType = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Generic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">IO = 3,</span>
}
</pre>
</div> <!-- end type MLModelError -->
<div> <!-- start type MLModelErrorExtensions -->
<h3>New Type CoreML.MLModelErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MLModelErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MLModelError self);</span>
}
</pre>
</div> <!-- end type MLModelErrorExtensions -->
<div> <!-- start type MLModelMetadata -->
<h3>New Type CoreML.MLModelMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class MLModelMetadata : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLModelMetadata (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Author { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CreatorDefined { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Description { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string License { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string VersionString { get; }</span>
}
</pre>
</div> <!-- end type MLModelMetadata -->
<div> <!-- start type MLMultiArray -->
<h3>New Type CoreML.MLMultiArray</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArray : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArray (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSError error);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MLMultiArray (IntPtr dataPointer, Foundation.NSNumber[] shape, MLMultiArrayDataType dataType, Foundation.NSNumber[] strides, System.Action&lt;IntPtr&gt; deallocator, Foundation.NSError error);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr DataPointer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber Item { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Strides { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSNumber GetObject (nint idx);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, Foundation.NSNumber[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetObject (Foundation.NSNumber obj, nint idx);</span>
}
</pre>
</div> <!-- end type MLMultiArray -->
<div> <!-- start type MLMultiArrayConstraint -->
<h3>New Type CoreML.MLMultiArrayConstraint</h3>
<pre class='added' data-is-non-breaking="">
public class MLMultiArrayConstraint : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLMultiArrayConstraint (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MLMultiArrayDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] Shape { get; }</span>
}
</pre>
</div> <!-- end type MLMultiArrayConstraint -->
<div> <!-- start type MLMultiArrayDataType -->
<h3>New Type CoreML.MLMultiArrayDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MLMultiArrayDataType {
	<span class='added added-field ' data-is-non-breaking="">Double = 65600,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 65568,</span>
	<span class='added added-field ' data-is-non-breaking="">Int32 = 131104,</span>
}
</pre>
</div> <!-- end type MLMultiArrayDataType -->
<div> <!-- start type MLPredictionOptions -->
<h3>New Type CoreML.MLPredictionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class MLPredictionOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MLPredictionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MLPredictionOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
}
</pre>
</div> <!-- end type MLPredictionOptions -->
</div> <!-- end namespace CoreML -->

<!-- start namespace Simd --> <div> 
<h2>New Namespace Simd</h2>

<div> <!-- start type MatrixFloat2x2 -->
<h3>New Type Simd.MatrixFloat2x2</h3>
<pre class='added' data-is-non-breaking="">
public struct MatrixFloat2x2, System.IEquatable&lt;MatrixFloat2x2&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat2x2 (OpenTK.Vector2 column0, OpenTK.Vector2 column1);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat2x2 (float m11, float m12, float m21, float m22);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static MatrixFloat2x2 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (MatrixFloat2x2 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat2x2 Multiply (MatrixFloat2x2 left, MatrixFloat2x2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (MatrixFloat2x2 left, MatrixFloat2x2 right, MatrixFloat2x2 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat2x2 Transpose (MatrixFloat2x2 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (MatrixFloat2x2 mat, MatrixFloat2x2 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (MatrixFloat2x2 left, MatrixFloat2x2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat2x2 op_Explicit (OpenTK.Matrix2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.Matrix2 op_Explicit (MatrixFloat2x2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (MatrixFloat2x2 left, MatrixFloat2x2 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat2x2 op_Multiply (MatrixFloat2x2 left, MatrixFloat2x2 right);</span>
}
</pre>
</div> <!-- end type MatrixFloat2x2 -->
<div> <!-- start type MatrixFloat3x3 -->
<h3>New Type Simd.MatrixFloat3x3</h3>
<pre class='added' data-is-non-breaking="">
public struct MatrixFloat3x3, System.IEquatable&lt;MatrixFloat3x3&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat3x3 (OpenTK.Vector3 column0, OpenTK.Vector3 column1, OpenTK.Vector3 column2);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat3x3 (float m11, float m12, float m13, float m21, float m22, float m23, float m31, float m32, float m33);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static MatrixFloat3x3 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M33;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (MatrixFloat3x3 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat3x3 Multiply (MatrixFloat3x3 left, MatrixFloat3x3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (MatrixFloat3x3 left, MatrixFloat3x3 right, MatrixFloat3x3 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat3x3 Transpose (MatrixFloat3x3 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (MatrixFloat3x3 mat, MatrixFloat3x3 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (MatrixFloat3x3 left, MatrixFloat3x3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat3x3 op_Explicit (OpenTK.Matrix3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.Matrix3 op_Explicit (MatrixFloat3x3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (MatrixFloat3x3 left, MatrixFloat3x3 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat3x3 op_Multiply (MatrixFloat3x3 left, MatrixFloat3x3 right);</span>
}
</pre>
</div> <!-- end type MatrixFloat3x3 -->
<div> <!-- start type MatrixFloat4x4 -->
<h3>New Type Simd.MatrixFloat4x4</h3>
<pre class='added' data-is-non-breaking="">
public struct MatrixFloat4x4, System.IEquatable&lt;MatrixFloat4x4&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat4x4 (OpenTK.Vector4 column0, OpenTK.Vector4 column1, OpenTK.Vector4 column2, OpenTK.Vector4 column3);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MatrixFloat4x4 (float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static MatrixFloat4x4 Identity;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M11;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M12;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M13;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M14;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M21;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M22;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M23;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M24;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M31;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M32;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M33;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M34;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M41;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M42;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M43;</span>
	<span class='added added-field ' data-is-non-breaking="">public float M44;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Determinant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Equals (MatrixFloat4x4 other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat4x4 Multiply (MatrixFloat4x4 left, MatrixFloat4x4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Multiply (MatrixFloat4x4 left, MatrixFloat4x4 right, MatrixFloat4x4 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Transpose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat4x4 Transpose (MatrixFloat4x4 mat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Transpose (MatrixFloat4x4 mat, MatrixFloat4x4 result);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (MatrixFloat4x4 left, MatrixFloat4x4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat4x4 op_Explicit (OpenTK.Matrix4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static OpenTK.Matrix4 op_Explicit (MatrixFloat4x4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (MatrixFloat4x4 left, MatrixFloat4x4 right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MatrixFloat4x4 op_Multiply (MatrixFloat4x4 left, MatrixFloat4x4 right);</span>
}
</pre>
</div> <!-- end type MatrixFloat4x4 -->
</div> <!-- end namespace Simd -->

</div>



   


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
</script><h1 id='diff/xi/Xamarin.WatchOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.NUnit --> <div> 
<h2>Namespace MonoTouch.NUnit</h2>
<!-- start type NUnitOutputTextWriter --> <div>
<h3>Type Changed: MonoTouch.NUnit.NUnitOutputTextWriter</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitOutputTextWriter (UI.BaseTouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter, UI.XmlMode xmlMode);</span>
</pre>
</div>

</div> <!-- end type NUnitOutputTextWriter -->

</div> <!-- end namespace MonoTouch.NUnit -->
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string LogFile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public XmlMode XmlMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->
<div> <!-- start type XmlMode -->
<h3>New Type MonoTouch.NUnit.UI.XmlMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum XmlMode {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Wrapped = 1,</span>
}
</pre>
</div> <!-- end type XmlMode -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
</div>



   


 <hr>
