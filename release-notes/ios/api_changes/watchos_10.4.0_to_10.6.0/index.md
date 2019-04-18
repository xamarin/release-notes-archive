---
id: 78E22909-B17E-45E2-8FC0-161E3DE63224
title: "watchOS 10.4.0 to 10.6.0"
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
<div> <!-- start type AVAudioPlayer -->
<h3>New Type AVFoundation.AVAudioPlayer</h3>
<pre class='added' data-is-non-breaking="">
public class AVAudioPlayer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioPlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioPlayer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioPlayer (Foundation.NSData data, string fileTypeHint, Foundation.NSError outError);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioPlayer (Foundation.NSUrl url, string fileTypeHint, Foundation.NSError outError);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioSessionChannelDescription[] ChannelAssignments { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double CurrentTime { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IAVAudioPlayerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DeviceCurrentTime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EnableRate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVAudioFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MeteringEnabled { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfLoops { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pan { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Playing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Rate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public AudioSettings SoundSetting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Volume { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSDictionary WeakSettings { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual float AveragePower (uint channelNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Pause ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float PeakPower (uint channelNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Play ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PlayAtTime (double time);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PrepareToPlay ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetVolume (float volume, double duration);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stop ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateMeters ();</span>
}
</pre>
</div> <!-- end type AVAudioPlayer -->
<div> <!-- start type AVAudioPlayerDelegate -->
<h3>New Type AVFoundation.AVAudioPlayerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVAudioPlayerDelegate : Foundation.NSObject, IAVAudioPlayerDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioPlayerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioPlayerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVAudioPlayerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginInterruption (AVAudioPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DecoderError (AVAudioPlayer player, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInterruption (AVAudioPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishedPlaying (AVAudioPlayer player, bool flag);</span>
}
</pre>
</div> <!-- end type AVAudioPlayerDelegate -->
<div> <!-- start type AVAudioPlayerDelegate_Extensions -->
<h3>New Type AVFoundation.AVAudioPlayerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVAudioPlayerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void BeginInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DecoderError (IAVAudioPlayerDelegate This, AVAudioPlayer player, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EndInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void EndInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void FinishedPlaying (IAVAudioPlayerDelegate This, AVAudioPlayer player, bool flag);</span>
}
</pre>
</div> <!-- end type AVAudioPlayerDelegate_Extensions -->
<div> <!-- start type AVAudioSessionInterruptionFlags -->
<h3>New Type AVFoundation.AVAudioSessionInterruptionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum AVAudioSessionInterruptionFlags {
	<span class='added added-field ' data-is-non-breaking="">ShouldResume = 1,</span>
}
</pre>
</div> <!-- end type AVAudioSessionInterruptionFlags -->
<div> <!-- start type IAVAudioPlayerDelegate -->
<h3>New Type AVFoundation.IAVAudioPlayerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVAudioPlayerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVAudioPlayerDelegate -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKFetchWebAuthTokenOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchWebAuthTokenOperation</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchWebAuthTokenOperation ();</span>
</pre>
</div>

</div> <!-- end type CKFetchWebAuthTokenOperation -->

</div> <!-- end namespace CloudKit -->
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
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGPoint --> <div>
<h3>Type Changed: CoreGraphics.CGPoint</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.Point op_Explicit (CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.PointF op_Explicit (CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGPoint op_Implicit (System.Drawing.Point point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGPoint op_Implicit (System.Drawing.PointF point);</span>
</pre>
</div>

</div> <!-- end type CGPoint -->
<!-- start type CGRect --> <div>
<h3>Type Changed: CoreGraphics.CGRect</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.Rectangle op_Explicit (CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.RectangleF op_Explicit (CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGRect op_Implicit (System.Drawing.Rectangle rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGRect op_Implicit (System.Drawing.RectangleF rect);</span>
</pre>
</div>

</div> <!-- end type CGRect -->
<!-- start type CGSize --> <div>
<h3>Type Changed: CoreGraphics.CGSize</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.Size op_Explicit (CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Drawing.SizeF op_Explicit (CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGSize op_Implicit (System.Drawing.Size size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CGSize op_Implicit (System.Drawing.SizeF size);</span>
</pre>
</div>

</div> <!-- end type CGSize -->

</div> <!-- end namespace CoreGraphics -->
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

</div> <!-- end namespace CoreVideo -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSAttributedString --> <div>
<h3>Type Changed: Foundation.NSAttributedString</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAttributedString (string str, CoreText.CTStringAttributes attributes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAttributedString (string str, UIKit.UIStringAttributes attributes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSAttributedString (string str, UIKit.UIFont font, UIKit.UIColor foregroundColor, UIKit.UIColor backgroundColor, UIKit.UIColor strokeColor, UIKit.NSParagraphStyle paragraphStyle, NSLigatureType ligatures, float kerning, NSUnderlineStyle underlineStyle, float strokeWidth, NSUnderlineStyle strikethroughStyle);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string Value { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public NSDictionary GetAttributes (nint location, NSRange effectiveRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreText.CTStringAttributes GetCoreTextAttributes (nint location, NSRange effectiveRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public CoreText.CTStringAttributes GetCoreTextAttributes (nint location, NSRange longestEffectiveRange, NSRange rangeLimit);</span>
	<span class='added added-method ' data-is-non-breaking="">public UIKit.UIStringAttributes GetUIKitAttributes (nint location, NSRange effectiveRange);</span>
	<span class='added added-method ' data-is-non-breaking="">public UIKit.UIStringAttributes GetUIKitAttributes (nint location, NSRange longestEffectiveRange, NSRange rangeLimit);</span>
	<span class='added added-method ' data-is-non-breaking="">public NSAttributedString Substring (nint start, nint len);</span>
</pre>
</div>

</div> <!-- end type NSAttributedString -->
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
<!-- start type NSValue --> <div>
<h3>Type Changed: Foundation.NSValue</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Drawing.PointF PointFValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Drawing.RectangleF RectangleFValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Drawing.SizeF SizeFValue { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSValue FromPointF (System.Drawing.PointF point);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSValue FromRectangleF (System.Drawing.RectangleF rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSValue FromSizeF (System.Drawing.SizeF size);</span>
</pre>
</div>

</div> <!-- end type NSValue -->
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
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"3.1"</span> <span class='added '>"3.2"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.3.1"</span> <span class='added '>"10.6.0"</span>;
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string IntentsLibrary = "/System/Library/Frameworks/Intents.framework/Intents";</span>
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
	<span class='added added-method ' data-is-non-breaking="">public virtual void Pause ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Play ();</span>
}
</pre>
</div> <!-- end type SKVideoNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type UIFont --> <div>
<h3>Type Changed: UIKit.UIFont</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
</pre>
</div>

</div> <!-- end type UIFont -->
<!-- start type UIFontDescriptor --> <div>
<h3>Type Changed: UIKit.UIFontDescriptor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (UIFontTextStyle uiFontTextStyle);</span>
</pre>
</div>

</div> <!-- end type UIFontDescriptor -->
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

</div> <!-- end namespace UIKit -->
<!-- start namespace WatchKit --> <div> 
<h2>Namespace WatchKit</h2>
<!-- start type WKAudioFilePlayerItem --> <div>
<h3>Type Changed: WatchKit.WKAudioFilePlayerItem</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCurrentTime (double time);</span>
</pre>
</div>

</div> <!-- end type WKAudioFilePlayerItem -->
<!-- start type WKExtensionDelegate --> <div>
<h3>Type Changed: WatchKit.WKExtensionDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleUserActivity (Foundation.NSUserActivity userActivity);</span>
</pre>
</div>

</div> <!-- end type WKExtensionDelegate -->
<!-- start type WKExtensionDelegate_Extensions --> <div>
<h3>Type Changed: WatchKit.WKExtensionDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void HandleUserActivity (IWKExtensionDelegate This, Foundation.NSUserActivity userActivity);</span>
</pre>
</div>

</div> <!-- end type WKExtensionDelegate_Extensions -->
<!-- start type WKInterfaceDevice --> <div>
<h3>Type Changed: WatchKit.WKInterfaceDevice</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string PreferredContentSizeCategoryString { get; }</span>
</pre>
</div>

</div> <!-- end type WKInterfaceDevice -->

</div> <!-- end namespace WatchKit -->
<!-- start namespace Intents --> <div> 
<h2>New Namespace Intents</h2>

<div> <!-- start type IINActivateCarSignalIntentHandling -->
<h3>New Type Intents.IINActivateCarSignalIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINActivateCarSignalIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleActivateCarSignal (INActivateCarSignalIntent intent, System.Action&lt;INActivateCarSignalIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINActivateCarSignalIntentHandling -->
<div> <!-- start type IINCallsDomainHandling -->
<h3>New Type Intents.IINCallsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCallsDomainHandling : IINSearchCallHistoryIntentHandling, IINStartAudioCallIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINCallsDomainHandling -->
<div> <!-- start type IINCancelWorkoutIntentHandling -->
<h3>New Type Intents.IINCancelWorkoutIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCancelWorkoutIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleCancelWorkout (INCancelWorkoutIntent intent, System.Action&lt;INCancelWorkoutIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINCancelWorkoutIntentHandling -->
<div> <!-- start type IINCarCommandsDomainHandling -->
<h3>New Type Intents.IINCarCommandsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINCarCommandsDomainHandling : IINActivateCarSignalIntentHandling, IINGetCarLockStatusIntentHandling, IINGetCarPowerLevelStatusIntentHandling, IINSetCarLockStatusIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINCarCommandsDomainHandling -->
<div> <!-- start type IINEndWorkoutIntentHandling -->
<h3>New Type Intents.IINEndWorkoutIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINEndWorkoutIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleEndWorkout (INEndWorkoutIntent intent, System.Action&lt;INEndWorkoutIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINEndWorkoutIntentHandling -->
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
<div> <!-- start type IINGetRideStatusIntentHandling -->
<h3>New Type Intents.IINGetRideStatusIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINGetRideStatusIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleRideStatus (INGetRideStatusIntent intent, System.Action&lt;INGetRideStatusIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartSendingUpdates (INGetRideStatusIntent intent, IINGetRideStatusIntentResponseObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopSendingUpdates (INGetRideStatusIntent intent);</span>
}
</pre>
</div> <!-- end type IINGetRideStatusIntentHandling -->
<div> <!-- start type IINGetRideStatusIntentResponseObserver -->
<h3>New Type Intents.IINGetRideStatusIntentResponseObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IINGetRideStatusIntentResponseObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateRideStatus (INGetRideStatusIntentResponse response);</span>
}
</pre>
</div> <!-- end type IINGetRideStatusIntentResponseObserver -->
<div> <!-- start type IINIntentHandlerProviding -->
<h3>New Type Intents.IINIntentHandlerProviding</h3>
<pre class='added' data-is-non-breaking="">
public interface IINIntentHandlerProviding : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetHandler (INIntent intent);</span>
}
</pre>
</div> <!-- end type IINIntentHandlerProviding -->
<div> <!-- start type IINListRideOptionsIntentHandling -->
<h3>New Type Intents.IINListRideOptionsIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINListRideOptionsIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleListRideOptions (INListRideOptionsIntent intent, System.Action&lt;INListRideOptionsIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINListRideOptionsIntentHandling -->
<div> <!-- start type IINMessagesDomainHandling -->
<h3>New Type Intents.IINMessagesDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINMessagesDomainHandling : IINSearchForMessagesIntentHandling, IINSendMessageIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINMessagesDomainHandling -->
<div> <!-- start type IINPauseWorkoutIntentHandling -->
<h3>New Type Intents.IINPauseWorkoutIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINPauseWorkoutIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandlePauseWorkout (INPauseWorkoutIntent intent, System.Action&lt;INPauseWorkoutIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINPauseWorkoutIntentHandling -->
<div> <!-- start type IINPayBillIntentHandling -->
<h3>New Type Intents.IINPayBillIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINPayBillIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINPayBillIntentHandling -->
<div> <!-- start type IINPaymentsDomainHandling -->
<h3>New Type Intents.IINPaymentsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINPaymentsDomainHandling : IINPayBillIntentHandling, IINRequestPaymentIntentHandling, IINSearchForBillsIntentHandling, IINSendPaymentIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINPaymentsDomainHandling -->
<div> <!-- start type IINPhotosDomainHandling -->
<h3>New Type Intents.IINPhotosDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINPhotosDomainHandling : IINSearchForPhotosIntentHandling, IINStartPhotoPlaybackIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINPhotosDomainHandling -->
<div> <!-- start type IINRequestPaymentIntentHandling -->
<h3>New Type Intents.IINRequestPaymentIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINRequestPaymentIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleRequestPayment (INRequestPaymentIntent intent, System.Action&lt;INRequestPaymentIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINRequestPaymentIntentHandling -->
<div> <!-- start type IINRequestRideIntentHandling -->
<h3>New Type Intents.IINRequestRideIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINRequestRideIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleRequestRide (INRequestRideIntent intent, System.Action&lt;INRequestRideIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINRequestRideIntentHandling -->
<div> <!-- start type IINResumeWorkoutIntentHandling -->
<h3>New Type Intents.IINResumeWorkoutIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINResumeWorkoutIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleResumeWorkout (INResumeWorkoutIntent intent, System.Action&lt;INResumeWorkoutIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINResumeWorkoutIntentHandling -->
<div> <!-- start type IINRidesharingDomainHandling -->
<h3>New Type Intents.IINRidesharingDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINRidesharingDomainHandling : IINGetRideStatusIntentHandling, IINListRideOptionsIntentHandling, IINRequestRideIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINRidesharingDomainHandling -->
<div> <!-- start type IINSearchCallHistoryIntentHandling -->
<h3>New Type Intents.IINSearchCallHistoryIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchCallHistoryIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchCallHistory (INSearchCallHistoryIntent intent, System.Action&lt;INSearchCallHistoryIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchCallHistoryIntentHandling -->
<div> <!-- start type IINSearchForBillsIntentHandling -->
<h3>New Type Intents.IINSearchForBillsIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForBillsIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINSearchForBillsIntentHandling -->
<div> <!-- start type IINSearchForMessagesIntentHandling -->
<h3>New Type Intents.IINSearchForMessagesIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForMessagesIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchForMessages (INSearchForMessagesIntent intent, System.Action&lt;INSearchForMessagesIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchForMessagesIntentHandling -->
<div> <!-- start type IINSearchForPhotosIntentHandling -->
<h3>New Type Intents.IINSearchForPhotosIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSearchForPhotosIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSearchForPhotos (INSearchForPhotosIntent intent, System.Action&lt;INSearchForPhotosIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSearchForPhotosIntentHandling -->
<div> <!-- start type IINSendMessageIntentHandling -->
<h3>New Type Intents.IINSendMessageIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSendMessageIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSendMessage (INSendMessageIntent intent, System.Action&lt;INSendMessageIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSendMessageIntentHandling -->
<div> <!-- start type IINSendPaymentIntentHandling -->
<h3>New Type Intents.IINSendPaymentIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSendPaymentIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSendPayment (INSendPaymentIntent intent, System.Action&lt;INSendPaymentIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSendPaymentIntentHandling -->
<div> <!-- start type IINSetCarLockStatusIntentHandling -->
<h3>New Type Intents.IINSetCarLockStatusIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSetCarLockStatusIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleSetCarLockStatus (INSetCarLockStatusIntent intent, System.Action&lt;INSetCarLockStatusIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINSetCarLockStatusIntentHandling -->
<div> <!-- start type IINSpeakable -->
<h3>New Type Intents.IINSpeakable</h3>
<pre class='added' data-is-non-breaking="">
public interface IINSpeakable : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
}
</pre>
</div> <!-- end type IINSpeakable -->
<div> <!-- start type IINStartAudioCallIntentHandling -->
<h3>New Type Intents.IINStartAudioCallIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINStartAudioCallIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleStartAudioCall (INStartAudioCallIntent intent, System.Action&lt;INStartAudioCallIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINStartAudioCallIntentHandling -->
<div> <!-- start type IINStartPhotoPlaybackIntentHandling -->
<h3>New Type Intents.IINStartPhotoPlaybackIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINStartPhotoPlaybackIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleStartPhotoPlayback (INStartPhotoPlaybackIntent intent, System.Action&lt;INStartPhotoPlaybackIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINStartPhotoPlaybackIntentHandling -->
<div> <!-- start type IINStartWorkoutIntentHandling -->
<h3>New Type Intents.IINStartWorkoutIntentHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINStartWorkoutIntentHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleStartWorkout (INStartWorkoutIntent intent, System.Action&lt;INStartWorkoutIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type IINStartWorkoutIntentHandling -->
<div> <!-- start type IINWorkoutsDomainHandling -->
<h3>New Type Intents.IINWorkoutsDomainHandling</h3>
<pre class='added' data-is-non-breaking="">
public interface IINWorkoutsDomainHandling : IINCancelWorkoutIntentHandling, IINEndWorkoutIntentHandling, IINPauseWorkoutIntentHandling, IINResumeWorkoutIntentHandling, IINStartWorkoutIntentHandling, ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IINWorkoutsDomainHandling -->
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
<div> <!-- start type INBooleanResolutionResult -->
<h3>New Type Intents.INBooleanResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INBooleanResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INBooleanResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INBooleanResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBooleanResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBooleanResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INBooleanResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INBooleanResolutionResult GetConfirmationRequired (Foundation.NSNumber valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INBooleanResolutionResult GetSuccess (bool resolvedValue);</span>
}
</pre>
</div> <!-- end type INBooleanResolutionResult -->
<div> <!-- start type INCallCapabilityOptions -->
<h3>New Type Intents.INCallCapabilityOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INCallCapabilityOptions {
	<span class='added added-field ' data-is-non-breaking="">AudioCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoCall = 2,</span>
}
</pre>
</div> <!-- end type INCallCapabilityOptions -->
<div> <!-- start type INCallRecordType -->
<h3>New Type Intents.INCallRecordType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCallRecordType {
	<span class='added added-field ' data-is-non-breaking="">Missed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INCallRecordType -->
<div> <!-- start type INCallRecordTypeResolutionResult -->
<h3>New Type Intents.INCallRecordTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCallRecordTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCallRecordTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult GetConfirmationRequired (INCallRecordType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCallRecordTypeResolutionResult GetSuccess (INCallRecordType resolvedValue);</span>
}
</pre>
</div> <!-- end type INCallRecordTypeResolutionResult -->
<div> <!-- start type INCancelWorkoutIntent -->
<h3>New Type Intents.INCancelWorkoutIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INCancelWorkoutIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCancelWorkoutIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCancelWorkoutIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCancelWorkoutIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCancelWorkoutIntent (INSpeakableString workoutName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCancelWorkoutIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString WorkoutName { get; }</span>
}
</pre>
</div> <!-- end type INCancelWorkoutIntent -->
<div> <!-- start type INCancelWorkoutIntentHandling_Extensions -->
<h3>New Type Intents.INCancelWorkoutIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INCancelWorkoutIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmCancelWorkout (IINCancelWorkoutIntentHandling This, INCancelWorkoutIntent intent, System.Action&lt;INCancelWorkoutIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutName (IINCancelWorkoutIntentHandling This, INCancelWorkoutIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INCancelWorkoutIntentHandling_Extensions -->
<div> <!-- start type INCancelWorkoutIntentResponse -->
<h3>New Type Intents.INCancelWorkoutIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INCancelWorkoutIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCancelWorkoutIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCancelWorkoutIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCancelWorkoutIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCancelWorkoutIntentResponse (INCancelWorkoutIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCancelWorkoutIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INCancelWorkoutIntentResponse -->
<div> <!-- start type INCancelWorkoutIntentResponseCode -->
<h3>New Type Intents.INCancelWorkoutIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCancelWorkoutIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoMatchingWorkout = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INCancelWorkoutIntentResponseCode -->
<div> <!-- start type INCarAirCirculationMode -->
<h3>New Type Intents.INCarAirCirculationMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCarAirCirculationMode {
	<span class='added added-field ' data-is-non-breaking="">FreshAir = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RecirculateAir = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INCarAirCirculationMode -->
<div> <!-- start type INCarAirCirculationModeResolutionResult -->
<h3>New Type Intents.INCarAirCirculationModeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCarAirCirculationModeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarAirCirculationModeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarAirCirculationModeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult GetConfirmationRequired (INCarAirCirculationMode valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCarAirCirculationModeResolutionResult GetSuccess (INCarAirCirculationMode resolvedValue);</span>
}
</pre>
</div> <!-- end type INCarAirCirculationModeResolutionResult -->
<div> <!-- start type INCarAudioSource -->
<h3>New Type Intents.INCarAudioSource</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCarAudioSource {
	<span class='added added-field ' data-is-non-breaking="">Aux = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Bluetooth = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">CarPlay = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HardDrive = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">MemoryCard = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">OpticalDrive = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Radio = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Usb = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">iPod = 2,</span>
}
</pre>
</div> <!-- end type INCarAudioSource -->
<div> <!-- start type INCarAudioSourceResolutionResult -->
<h3>New Type Intents.INCarAudioSourceResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCarAudioSourceResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarAudioSourceResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarAudioSourceResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAudioSourceResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAudioSourceResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarAudioSourceResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCarAudioSourceResolutionResult GetConfirmationRequired (INCarAudioSource valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCarAudioSourceResolutionResult GetSuccess (INCarAudioSource resolvedValue);</span>
}
</pre>
</div> <!-- end type INCarAudioSourceResolutionResult -->
<div> <!-- start type INCarDefroster -->
<h3>New Type Intents.INCarDefroster</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCarDefroster {
	<span class='added added-field ' data-is-non-breaking="">All = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Front = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INCarDefroster -->
<div> <!-- start type INCarDefrosterResolutionResult -->
<h3>New Type Intents.INCarDefrosterResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCarDefrosterResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarDefrosterResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarDefrosterResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarDefrosterResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarDefrosterResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarDefrosterResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCarDefrosterResolutionResult GetConfirmationRequired (INCarDefroster valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCarDefrosterResolutionResult GetSuccess (INCarDefroster resolvedValue);</span>
}
</pre>
</div> <!-- end type INCarDefrosterResolutionResult -->
<div> <!-- start type INCarSeat -->
<h3>New Type Intents.INCarSeat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INCarSeat {
	<span class='added added-field ' data-is-non-breaking="">All = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Driver = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Front = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FrontLeft = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FrontRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Passenger = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rear = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">RearLeft = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">RearRight = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ThirdRow = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ThirdRowLeft = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">ThirdRowRight = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INCarSeat -->
<div> <!-- start type INCarSeatResolutionResult -->
<h3>New Type Intents.INCarSeatResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCarSeatResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarSeatResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCarSeatResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSeatResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSeatResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCarSeatResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCarSeatResolutionResult GetConfirmationRequired (INCarSeat valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCarSeatResolutionResult GetSuccess (INCarSeat resolvedValue);</span>
}
</pre>
</div> <!-- end type INCarSeatResolutionResult -->
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
<div> <!-- start type INConditionalOperator -->
<h3>New Type Intents.INConditionalOperator</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INConditionalOperator {
	<span class='added added-field ' data-is-non-breaking="">All = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 2,</span>
}
</pre>
</div> <!-- end type INConditionalOperator -->
<div> <!-- start type INCurrencyAmount -->
<h3>New Type Intents.INCurrencyAmount</h3>
<pre class='added' data-is-non-breaking="">
public class INCurrencyAmount : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INCurrencyAmount (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCurrencyAmount (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCurrencyAmount (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INCurrencyAmount (Foundation.NSDecimalNumber amount, string currencyCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Amount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CurrencyCode { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INCurrencyAmount -->
<div> <!-- start type INCurrencyAmountResolutionResult -->
<h3>New Type Intents.INCurrencyAmountResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INCurrencyAmountResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INCurrencyAmountResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INCurrencyAmountResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult GetConfirmationRequired (INCurrencyAmount currencyAmountToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult GetDisambiguation (INCurrencyAmount[] currencyAmountsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INCurrencyAmountResolutionResult GetSuccess (INCurrencyAmount resolvedCurrencyAmount);</span>
}
</pre>
</div> <!-- end type INCurrencyAmountResolutionResult -->
<div> <!-- start type INDateComponentsRange -->
<h3>New Type Intents.INDateComponentsRange</h3>
<pre class='added' data-is-non-breaking="">
public class INDateComponentsRange : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRange (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INDateComponentsRange (Foundation.NSDateComponents startDateComponents, Foundation.NSDateComponents endDateComponents);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents EndDateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents StartDateComponents { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INDateComponentsRange -->
<div> <!-- start type INDateComponentsRangeResolutionResult -->
<h3>New Type Intents.INDateComponentsRangeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INDateComponentsRangeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRangeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsRangeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetConfirmationRequired (INDateComponentsRange dateComponentsRangeToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetDisambiguation (INDateComponentsRange[] dateComponentsRangesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsRangeResolutionResult GetSuccess (INDateComponentsRange resolvedDateComponentsRange);</span>
}
</pre>
</div> <!-- end type INDateComponentsRangeResolutionResult -->
<div> <!-- start type INDateComponentsResolutionResult -->
<h3>New Type Intents.INDateComponentsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INDateComponentsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDateComponentsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDateComponentsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsResolutionResult GetConfirmationRequired (Foundation.NSDateComponents componentsToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsResolutionResult GetDisambiguation (Foundation.NSDateComponents[] componentsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDateComponentsResolutionResult GetSuccess (Foundation.NSDateComponents resolvedDateComponents);</span>
}
</pre>
</div> <!-- end type INDateComponentsResolutionResult -->
<div> <!-- start type INDoubleResolutionResult -->
<h3>New Type Intents.INDoubleResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INDoubleResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INDoubleResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INDoubleResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDoubleResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDoubleResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INDoubleResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INDoubleResolutionResult GetConfirmationRequired (Foundation.NSNumber valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INDoubleResolutionResult GetSuccess (double resolvedValue);</span>
}
</pre>
</div> <!-- end type INDoubleResolutionResult -->
<div> <!-- start type INEndWorkoutIntent -->
<h3>New Type Intents.INEndWorkoutIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INEndWorkoutIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INEndWorkoutIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INEndWorkoutIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INEndWorkoutIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INEndWorkoutIntent (INSpeakableString workoutName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INEndWorkoutIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString WorkoutName { get; }</span>
}
</pre>
</div> <!-- end type INEndWorkoutIntent -->
<div> <!-- start type INEndWorkoutIntentHandling_Extensions -->
<h3>New Type Intents.INEndWorkoutIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INEndWorkoutIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmEndWorkout (IINEndWorkoutIntentHandling This, INEndWorkoutIntent intent, System.Action&lt;INEndWorkoutIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutName (IINEndWorkoutIntentHandling This, INEndWorkoutIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INEndWorkoutIntentHandling_Extensions -->
<div> <!-- start type INEndWorkoutIntentResponse -->
<h3>New Type Intents.INEndWorkoutIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INEndWorkoutIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INEndWorkoutIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INEndWorkoutIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INEndWorkoutIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INEndWorkoutIntentResponse (INEndWorkoutIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INEndWorkoutIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INEndWorkoutIntentResponse -->
<div> <!-- start type INEndWorkoutIntentResponseCode -->
<h3>New Type Intents.INEndWorkoutIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INEndWorkoutIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoMatchingWorkout = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INEndWorkoutIntentResponseCode -->
<div> <!-- start type INExtension -->
<h3>New Type Intents.INExtension</h3>
<pre class='added' data-is-non-breaking="">
public class INExtension : Foundation.NSObject, Foundation.INSObjectProtocol, IINIntentHandlerProviding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INExtension ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INExtension (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INExtension (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetHandler (INIntent intent);</span>
}
</pre>
</div> <!-- end type INExtension -->
<div> <!-- start type INGetAvailableRestaurantReservationBookingDefaultsIntentResponseCode -->
<h3>New Type Intents.INGetAvailableRestaurantReservationBookingDefaultsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetAvailableRestaurantReservationBookingDefaultsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 2,</span>
}
</pre>
</div> <!-- end type INGetAvailableRestaurantReservationBookingDefaultsIntentResponseCode -->
<div> <!-- start type INGetAvailableRestaurantReservationBookingsIntentCode -->
<h3>New Type Intents.INGetAvailableRestaurantReservationBookingsIntentCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetAvailableRestaurantReservationBookingsIntentCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequestUnsatisfiable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequestUnspecified = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type INGetAvailableRestaurantReservationBookingsIntentCode -->
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
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INGetCarPowerLevelStatusIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;Foundation.NSUnitLength&gt; DistanceRemaining { get; set; }</span>
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
<div> <!-- start type INGetRestaurantGuestIntentResponseCode -->
<h3>New Type Intents.INGetRestaurantGuestIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetRestaurantGuestIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
}
</pre>
</div> <!-- end type INGetRestaurantGuestIntentResponseCode -->
<div> <!-- start type INGetRideStatusIntent -->
<h3>New Type Intents.INGetRideStatusIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INGetRideStatusIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetRideStatusIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetRideStatusIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetRideStatusIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetRideStatusIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type INGetRideStatusIntent -->
<div> <!-- start type INGetRideStatusIntentHandling_Extensions -->
<h3>New Type Intents.INGetRideStatusIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INGetRideStatusIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmRideStatus (IINGetRideStatusIntentHandling This, INGetRideStatusIntent intent, System.Action&lt;INGetRideStatusIntentResponse&gt; completion);</span>
}
</pre>
</div> <!-- end type INGetRideStatusIntentHandling_Extensions -->
<div> <!-- start type INGetRideStatusIntentResponse -->
<h3>New Type Intents.INGetRideStatusIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INGetRideStatusIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INGetRideStatusIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetRideStatusIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INGetRideStatusIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INGetRideStatusIntentResponse (INGetRideStatusIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INGetRideStatusIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideStatus RideStatus { get; set; }</span>
}
</pre>
</div> <!-- end type INGetRideStatusIntentResponse -->
<div> <!-- start type INGetRideStatusIntentResponseCode -->
<h3>New Type Intents.INGetRideStatusIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetRideStatusIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchMustVerifyCredentials = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchServiceTemporarilyUnavailable = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INGetRideStatusIntentResponseCode -->
<div> <!-- start type INGetUserCurrentRestaurantReservationBookingsIntentResponseCode -->
<h3>New Type Intents.INGetUserCurrentRestaurantReservationBookingsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INGetUserCurrentRestaurantReservationBookingsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequestUnsatisfiable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 3,</span>
}
</pre>
</div> <!-- end type INGetUserCurrentRestaurantReservationBookingsIntentResponseCode -->
<div> <!-- start type INImage -->
<h3>New Type Intents.INImage</h3>
<pre class='added' data-is-non-breaking="">
public class INImage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INImage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INImage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromData (Foundation.NSData imageData);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INImage FromUrl (Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type INImage -->
<div> <!-- start type INIntegerResolutionResult -->
<h3>New Type Intents.INIntegerResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INIntegerResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntegerResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntegerResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntegerResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntegerResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntegerResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INIntegerResolutionResult GetConfirmationRequired (Foundation.NSNumber valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INIntegerResolutionResult GetSuccess (nint resolvedValue);</span>
}
</pre>
</div> <!-- end type INIntegerResolutionResult -->
<div> <!-- start type INIntent -->
<h3>New Type Intents.INIntent</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public INIntentIdentifier? Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString IdentifierString { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INIntent -->
<div> <!-- start type INIntentErrorCode -->
<h3>New Type Intents.INIntentErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentErrorCode {
	<span class='added added-field ' data-is-non-breaking="">DeletingAllInteractions = 1902,</span>
	<span class='added added-field ' data-is-non-breaking="">DeletingInteractionWithGroupIdentifier = 1904,</span>
	<span class='added added-field ' data-is-non-breaking="">DeletingInteractionWithIdentifiers = 1903,</span>
	<span class='added added-field ' data-is-non-breaking="">DonatingInteraction = 1901,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtensionBringUpFailed = 5001,</span>
	<span class='added added-field ' data-is-non-breaking="">ExtensionLaunchingTimeout = 5000,</span>
	<span class='added added-field ' data-is-non-breaking="">IntentSupportedByMultipleExtension = 2001,</span>
	<span class='added added-field ' data-is-non-breaking="">InteractionOperationNotSupported = 1900,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidIntentName = 2004,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidUserVocabularyFileLocation = 4000,</span>
	<span class='added added-field ' data-is-non-breaking="">NoHandlerProvidedForIntent = 2003,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestTimedOut = 3001,</span>
	<span class='added added-field ' data-is-non-breaking="">RestrictedIntentsNotSupportedByExtension = 2002,</span>
}
</pre>
</div> <!-- end type INIntentErrorCode -->
<div> <!-- start type INIntentErrorCodeExtensions -->
<h3>New Type Intents.INIntentErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INIntentErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (INIntentErrorCode self);</span>
}
</pre>
</div> <!-- end type INIntentErrorCodeExtensions -->
<div> <!-- start type INIntentHandlingStatus -->
<h3>New Type Intents.INIntentHandlingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentHandlingStatus {
	<span class='added added-field ' data-is-non-breaking="">DeferredToApplication = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INIntentHandlingStatus -->
<div> <!-- start type INIntentIdentifier -->
<h3>New Type Intents.INIntentIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INIntentIdentifier {
	<span class='added added-field ' data-is-non-breaking="">CancelWorkout = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">EndWorkout = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">GetRideStatus = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">ListRideOptions = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">PauseWorkout = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestPayment = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestRide = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">ResumeWorkout = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">SaveProfileInCar = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchCallHistory = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchForMessages = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">SearchForPhotos = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">SendMessage = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">SendPayment = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">SetAudioSourceInCar = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SetClimateSettingsInCar = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">SetDefrosterSettingsInCar = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">SetMessageAttribute = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">SetProfileInCar = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SetRadioStation = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">SetSeatSettingsInCar = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">StartAudioCall = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">StartPhotoPlayback = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">StartVideoCall = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">StartWorkout = 9,</span>
}
</pre>
</div> <!-- end type INIntentIdentifier -->
<div> <!-- start type INIntentIdentifierExtensions -->
<h3>New Type Intents.INIntentIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INIntentIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INIntentIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INIntentIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INIntentIdentifierExtensions -->
<div> <!-- start type INIntentResolutionResult -->
<h3>New Type Intents.INIntentResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntentResolutionResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INIntentResolutionResult Unsupported { get; }</span>
}
</pre>
</div> <!-- end type INIntentResolutionResult -->
<div> <!-- start type INIntentResolutionResult`1 -->
<h3>New Type Intents.INIntentResolutionResult`1</h3>
<pre class='added' data-is-non-breaking="">
public sealed class INIntentResolutionResult`1 : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
}
</pre>
</div> <!-- end type INIntentResolutionResult`1 -->
<div> <!-- start type INIntentResponse -->
<h3>New Type Intents.INIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public abstract class INIntentResponse : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INIntentResponse (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity UserActivity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INIntentResponse -->
<div> <!-- start type INInteraction -->
<h3>New Type Intents.INInteraction</h3>
<pre class='added' data-is-non-breaking="">
public class INInteraction : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INInteraction (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INInteraction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INInteraction (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INInteraction (INIntent intent, INIntentResponse response);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateInterval DateInterval { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INInteractionDirection Direction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GroupIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntent Intent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntentHandlingStatus IntentHandlingStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INIntentResponse IntentResponse { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteAllInteractions (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteAllInteractionsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteGroupedInteractions (string groupIdentifier, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteGroupedInteractionsAsync (string groupIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteInteractions (string[] identifiers, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task DeleteInteractionsAsync (string[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DonateInteraction (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DonateInteractionAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INInteraction -->
<div> <!-- start type INInteractionDirection -->
<h3>New Type Intents.INInteractionDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INInteractionDirection {
	<span class='added added-field ' data-is-non-breaking="">Incoming = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outgoing = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INInteractionDirection -->
<div> <!-- start type INListRideOptionsIntent -->
<h3>New Type Intents.INListRideOptionsIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INListRideOptionsIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INListRideOptionsIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INListRideOptionsIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INListRideOptionsIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INListRideOptionsIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INListRideOptionsIntent (CoreLocation.CLPlacemark pickupLocation, CoreLocation.CLPlacemark dropOffLocation);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark DropOffLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark PickupLocation { get; }</span>
}
</pre>
</div> <!-- end type INListRideOptionsIntent -->
<div> <!-- start type INListRideOptionsIntentHandling_Extensions -->
<h3>New Type Intents.INListRideOptionsIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INListRideOptionsIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmListRideOptions (IINListRideOptionsIntentHandling This, INListRideOptionsIntent intent, System.Action&lt;INListRideOptionsIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDropOffLocation (IINListRideOptionsIntentHandling This, INListRideOptionsIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePickupLocation (IINListRideOptionsIntentHandling This, INListRideOptionsIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INListRideOptionsIntentHandling_Extensions -->
<div> <!-- start type INListRideOptionsIntentResponse -->
<h3>New Type Intents.INListRideOptionsIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INListRideOptionsIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INListRideOptionsIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INListRideOptionsIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INListRideOptionsIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INListRideOptionsIntentResponse (INListRideOptionsIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INListRideOptionsIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ExpirationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentMethod[] PaymentMethods { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideOption[] RideOptions { get; set; }</span>
}
</pre>
</div> <!-- end type INListRideOptionsIntentResponse -->
<div> <!-- start type INListRideOptionsIntentResponseCode -->
<h3>New Type Intents.INListRideOptionsIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INListRideOptionsIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchMustVerifyCredentials = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchNoServiceInArea = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchPreviousRideNeedsCompletion = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchServiceTemporarilyUnavailable = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INListRideOptionsIntentResponseCode -->
<div> <!-- start type INMessage -->
<h3>New Type Intents.INMessage</h3>
<pre class='added' data-is-non-breaking="">
public class INMessage : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INMessage (string identifier, string content, Foundation.NSDate dateSent, INPerson sender, INPerson[] recipients);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate DateSent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Sender { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INMessage -->
<div> <!-- start type INMessageAttribute -->
<h3>New Type Intents.INMessageAttribute</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INMessageAttribute {
	<span class='added added-field ' data-is-non-breaking="">Flagged = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unflagged = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unread = 2,</span>
}
</pre>
</div> <!-- end type INMessageAttribute -->
<div> <!-- start type INMessageAttributeOptions -->
<h3>New Type Intents.INMessageAttributeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INMessageAttributeOptions {
	<span class='added added-field ' data-is-non-breaking="">Flagged = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Read = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unflagged = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Unread = 2,</span>
}
</pre>
</div> <!-- end type INMessageAttributeOptions -->
<div> <!-- start type INMessageAttributeOptionsResolutionResult -->
<h3>New Type Intents.INMessageAttributeOptionsResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INMessageAttributeOptionsResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeOptionsResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeOptionsResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult GetConfirmationRequired (INMessageAttributeOptions valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeOptionsResolutionResult GetSuccess (INMessageAttributeOptions resolvedValue);</span>
}
</pre>
</div> <!-- end type INMessageAttributeOptionsResolutionResult -->
<div> <!-- start type INMessageAttributeResolutionResult -->
<h3>New Type Intents.INMessageAttributeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INMessageAttributeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INMessageAttributeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INMessageAttributeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeResolutionResult GetConfirmationRequired (INMessageAttribute valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INMessageAttributeResolutionResult GetSuccess (INMessageAttribute resolvedValue);</span>
}
</pre>
</div> <!-- end type INMessageAttributeResolutionResult -->
<div> <!-- start type INPauseWorkoutIntent -->
<h3>New Type Intents.INPauseWorkoutIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INPauseWorkoutIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPauseWorkoutIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPauseWorkoutIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPauseWorkoutIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPauseWorkoutIntent (INSpeakableString workoutName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPauseWorkoutIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString WorkoutName { get; }</span>
}
</pre>
</div> <!-- end type INPauseWorkoutIntent -->
<div> <!-- start type INPauseWorkoutIntentHandling_Extensions -->
<h3>New Type Intents.INPauseWorkoutIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPauseWorkoutIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmPauseWorkout (IINPauseWorkoutIntentHandling This, INPauseWorkoutIntent intent, System.Action&lt;INPauseWorkoutIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutName (IINPauseWorkoutIntentHandling This, INPauseWorkoutIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INPauseWorkoutIntentHandling_Extensions -->
<div> <!-- start type INPauseWorkoutIntentResponse -->
<h3>New Type Intents.INPauseWorkoutIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INPauseWorkoutIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPauseWorkoutIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPauseWorkoutIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPauseWorkoutIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPauseWorkoutIntentResponse (INPauseWorkoutIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPauseWorkoutIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INPauseWorkoutIntentResponse -->
<div> <!-- start type INPauseWorkoutIntentResponseCode -->
<h3>New Type Intents.INPauseWorkoutIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPauseWorkoutIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoMatchingWorkout = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INPauseWorkoutIntentResponseCode -->
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
<div> <!-- start type INPaymentMethod -->
<h3>New Type Intents.INPaymentMethod</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentMethod : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentMethod (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentMethod (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentMethod (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentMethod (INPaymentMethodType type, string name, string identificationHint, INImage icon);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static INPaymentMethod ApplePayPaymentMethod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage Icon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string IdentificationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentMethodType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPaymentMethod -->
<div> <!-- start type INPaymentMethodType -->
<h3>New Type Intents.INPaymentMethodType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPaymentMethodType {
	<span class='added added-field ' data-is-non-breaking="">ApplePay = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Brokerage = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Checking = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Credit = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Debit = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Prepaid = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Savings = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Store = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INPaymentMethodType -->
<div> <!-- start type INPaymentRecord -->
<h3>New Type Intents.INPaymentRecord</h3>
<pre class='added' data-is-non-breaking="">
public class INPaymentRecord : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentRecord (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentRecord (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPaymentRecord (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentRecord (INPerson payee, INPerson payer, INCurrencyAmount currencyAmount, INPaymentMethod paymentMethod, string note, INPaymentStatus status);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPaymentRecord (INPerson payee, INPerson payer, INCurrencyAmount currencyAmount, INPaymentMethod paymentMethod, string note, INPaymentStatus status, INCurrencyAmount feeAmount);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount CurrencyAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount FeeAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Note { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Payee { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Payer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentMethod PaymentMethod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentStatus Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPaymentRecord -->
<div> <!-- start type INPaymentStatus -->
<h3>New Type Intents.INPaymentStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPaymentStatus {
	<span class='added added-field ' data-is-non-breaking="">Canceled = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Completed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Pending = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unpaid = 5,</span>
}
</pre>
</div> <!-- end type INPaymentStatus -->
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
<div> <!-- start type INPerson -->
<h3>New Type Intents.INPerson</h3>
<pre class='added' data-is-non-breaking="">
public class INPerson : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IINSpeakable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPerson (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPerson (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (INPersonHandle personHandle, Foundation.NSPersonNameComponents nameComponents, string displayName, INImage image, string contactIdentifier, string customIdentifier);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPerson (INPersonHandle personHandle, Foundation.NSPersonNameComponents nameComponents, string displayName, INImage image, string contactIdentifier, string customIdentifier, INPersonHandle[] aliases, INPersonSuggestionType suggestionType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandle[] Aliases { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContactIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CustomIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPersonNameComponents NameComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandle PersonHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public INPersonRelationship Relationship { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] SiriMatches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonSuggestionType SuggestionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakRelationship { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPerson -->
<div> <!-- start type INPersonHandle -->
<h3>New Type Intents.INPersonHandle</h3>
<pre class='added' data-is-non-breaking="">
public class INPersonHandle : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (string value, INPersonHandleType type);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonHandle (string value, INPersonHandleType type, Foundation.NSString stringLabel);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPersonHandle (string value, INPersonHandleType type, INPersonHandleLabel label);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public INPersonHandleLabel Label { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPersonHandleType Type { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakLabel { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPersonHandle -->
<div> <!-- start type INPersonHandleLabel -->
<h3>New Type Intents.INPersonHandleLabel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonHandleLabel {
	<span class='added added-field ' data-is-non-breaking="">Home = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeFax = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Main = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Mobile = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Other = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Pager = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Work = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WorkFax = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">iPhone = 3,</span>
}
</pre>
</div> <!-- end type INPersonHandleLabel -->
<div> <!-- start type INPersonHandleLabelExtensions -->
<h3>New Type Intents.INPersonHandleLabelExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPersonHandleLabelExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INPersonHandleLabel self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonHandleLabel GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INPersonHandleLabelExtensions -->
<div> <!-- start type INPersonHandleType -->
<h3>New Type Intents.INPersonHandleType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonHandleType {
	<span class='added added-field ' data-is-non-breaking="">EmailAddress = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PhoneNumber = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INPersonHandleType -->
<div> <!-- start type INPersonRelationship -->
<h3>New Type Intents.INPersonRelationship</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonRelationship {
	<span class='added added-field ' data-is-non-breaking="">Assistant = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Brother = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Child = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Father = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Friend = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Manager = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Mother = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Parent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Partner = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Sister = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Spouse = 8,</span>
}
</pre>
</div> <!-- end type INPersonRelationship -->
<div> <!-- start type INPersonRelationshipExtensions -->
<h3>New Type Intents.INPersonRelationshipExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INPersonRelationshipExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INPersonRelationship self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonRelationship GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INPersonRelationshipExtensions -->
<div> <!-- start type INPersonResolutionResult -->
<h3>New Type Intents.INPersonResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPersonResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPersonResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPersonResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetConfirmationRequired (INPerson personToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetDisambiguation (INPerson[] peopleToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPersonResolutionResult GetSuccess (INPerson resolvedPerson);</span>
}
</pre>
</div> <!-- end type INPersonResolutionResult -->
<div> <!-- start type INPersonSuggestionType -->
<h3>New Type Intents.INPersonSuggestionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INPersonSuggestionType {
	<span class='added added-field ' data-is-non-breaking="">InstantMessageAddress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SocialProfile = 1,</span>
}
</pre>
</div> <!-- end type INPersonSuggestionType -->
<div> <!-- start type INPhotoAttributeOptions -->
<h3>New Type Intents.INPhotoAttributeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum INPhotoAttributeOptions {
	<span class='added added-field ' data-is-non-breaking="">BurstPhoto = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">ChromeFilter = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">FadeFilter = 4194304,</span>
	<span class='added added-field ' data-is-non-breaking="">Favorite = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Flash = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FrontFacingCamera = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Gif = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HdrPhoto = 2048,</span>
	<span class='added added-field ' data-is-non-breaking="">InstantFilter = 262144,</span>
	<span class='added added-field ' data-is-non-breaking="">LandscapeOrientation = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">MonoFilter = 2097152,</span>
	<span class='added added-field ' data-is-non-breaking="">NoirFilter = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">PanoramaPhoto = 8192,</span>
	<span class='added added-field ' data-is-non-breaking="">Photo = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PortraitOrientation = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">ProcessFilter = 8388608,</span>
	<span class='added added-field ' data-is-non-breaking="">Screenshot = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">Selfie = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">SlowMotionVideo = 32768,</span>
	<span class='added added-field ' data-is-non-breaking="">SquarePhoto = 4096,</span>
	<span class='added added-field ' data-is-non-breaking="">TimeLapseVideo = 16384,</span>
	<span class='added added-field ' data-is-non-breaking="">TonalFilter = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">TransferFilter = 1048576,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type INPhotoAttributeOptions -->
<div> <!-- start type INPlacemarkResolutionResult -->
<h3>New Type Intents.INPlacemarkResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INPlacemarkResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPlacemarkResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPlacemarkResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INPlacemarkResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetConfirmationRequired (CoreLocation.CLPlacemark placemarkToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetDisambiguation (CoreLocation.CLPlacemark[] placemarksToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INPlacemarkResolutionResult GetSuccess (CoreLocation.CLPlacemark resolvedPlacemark);</span>
}
</pre>
</div> <!-- end type INPlacemarkResolutionResult -->
<div> <!-- start type INPreferences -->
<h3>New Type Intents.INPreferences</h3>
<pre class='added' data-is-non-breaking="">
public class INPreferences : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INPreferences (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPreferences (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string SiriLanguageCode { get; }</span>
}
</pre>
</div> <!-- end type INPreferences -->
<div> <!-- start type INPriceRange -->
<h3>New Type Intents.INPriceRange</h3>
<pre class='added' data-is-non-breaking="">
public class INPriceRange : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INPriceRange (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPriceRange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INPriceRange (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPriceRange (Foundation.NSDecimalNumber price, string currencyCode);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INPriceRange (Foundation.NSDecimalNumber firstPrice, Foundation.NSDecimalNumber secondPrice, string currencyCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CurrencyCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber MaximumPrice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber MinimumPrice { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INPriceRange -->
<div> <!-- start type INRadioType -->
<h3>New Type Intents.INRadioType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRadioType {
	<span class='added added-field ' data-is-non-breaking="">AM = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Dab = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FM = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HD = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Satellite = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INRadioType -->
<div> <!-- start type INRadioTypeResolutionResult -->
<h3>New Type Intents.INRadioTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INRadioTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INRadioTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRadioTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRadioTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRadioTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRadioTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INRadioTypeResolutionResult GetConfirmationRequired (INRadioType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRadioTypeResolutionResult GetSuccess (INRadioType resolvedValue);</span>
}
</pre>
</div> <!-- end type INRadioTypeResolutionResult -->
<div> <!-- start type INRelativeReference -->
<h3>New Type Intents.INRelativeReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRelativeReference {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INRelativeReference -->
<div> <!-- start type INRelativeReferenceResolutionResult -->
<h3>New Type Intents.INRelativeReferenceResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INRelativeReferenceResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INRelativeReferenceResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRelativeReferenceResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeReferenceResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeReferenceResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeReferenceResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INRelativeReferenceResolutionResult GetConfirmationRequired (INRelativeReference valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRelativeReferenceResolutionResult GetSuccess (INRelativeReference resolvedValue);</span>
}
</pre>
</div> <!-- end type INRelativeReferenceResolutionResult -->
<div> <!-- start type INRelativeSetting -->
<h3>New Type Intents.INRelativeSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRelativeSetting {
	<span class='added added-field ' data-is-non-breaking="">Higher = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Highest = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Lower = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Lowest = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INRelativeSetting -->
<div> <!-- start type INRelativeSettingResolutionResult -->
<h3>New Type Intents.INRelativeSettingResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INRelativeSettingResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INRelativeSettingResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRelativeSettingResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeSettingResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeSettingResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INRelativeSettingResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INRelativeSettingResolutionResult GetConfirmationRequired (INRelativeSetting valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRelativeSettingResolutionResult GetSuccess (INRelativeSetting resolvedValue);</span>
}
</pre>
</div> <!-- end type INRelativeSettingResolutionResult -->
<div> <!-- start type INRequestPaymentIntent -->
<h3>New Type Intents.INRequestPaymentIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestPaymentIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentIntent (INPerson payer, INCurrencyAmount currencyAmount, string note);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount CurrencyAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Note { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Payer { get; }</span>
}
</pre>
</div> <!-- end type INRequestPaymentIntent -->
<div> <!-- start type INRequestPaymentIntentHandling_Extensions -->
<h3>New Type Intents.INRequestPaymentIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INRequestPaymentIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmRequestPayment (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INRequestPaymentIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCurrencyAmount (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INCurrencyAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveNote (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePayer (IINRequestPaymentIntentHandling This, INRequestPaymentIntent intent, System.Action&lt;INPersonResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INRequestPaymentIntentHandling_Extensions -->
<div> <!-- start type INRequestPaymentIntentResponse -->
<h3>New Type Intents.INRequestPaymentIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestPaymentIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestPaymentIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestPaymentIntentResponse (INRequestPaymentIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRequestPaymentIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentRecord PaymentRecord { get; set; }</span>
}
</pre>
</div> <!-- end type INRequestPaymentIntentResponse -->
<div> <!-- start type INRequestPaymentIntentResponseCode -->
<h3>New Type Intents.INRequestPaymentIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRequestPaymentIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCredentialsUnverified = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoBankAccount = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsAmountAboveMaximum = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsAmountBelowMinimum = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsCurrencyUnsupported = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INRequestPaymentIntentResponseCode -->
<div> <!-- start type INRequestRideIntent -->
<h3>New Type Intents.INRequestRideIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestRideIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestRideIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestRideIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntent (CoreLocation.CLPlacemark pickupLocation, CoreLocation.CLPlacemark dropOffLocation, INSpeakableString rideOptionName, Foundation.NSNumber partySize, INPaymentMethod paymentMethod, INDateComponentsRange scheduledPickupTime);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark DropOffLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber PartySize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentMethod PaymentMethod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark PickupLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString RideOptionName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange ScheduledPickupTime { get; }</span>
}
</pre>
</div> <!-- end type INRequestRideIntent -->
<div> <!-- start type INRequestRideIntentHandling_Extensions -->
<h3>New Type Intents.INRequestRideIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INRequestRideIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmRequestRide (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INRequestRideIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDropOffLocation (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePartySize (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INIntegerResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePickupLocation (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRideOptionName (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveScheduledPickupTime (IINRequestRideIntentHandling This, INRequestRideIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INRequestRideIntentHandling_Extensions -->
<div> <!-- start type INRequestRideIntentResponse -->
<h3>New Type Intents.INRequestRideIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INRequestRideIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestRideIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRequestRideIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRequestRideIntentResponse (INRequestRideIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRequestRideIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideStatus RideStatus { get; set; }</span>
}
</pre>
</div> <!-- end type INRequestRideIntentResponse -->
<div> <!-- start type INRequestRideIntentResponseCode -->
<h3>New Type Intents.INRequestRideIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRequestRideIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchMustVerifyCredentials = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchNoServiceInArea = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchPreviousRideNeedsCompletion = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunchServiceTemporarilyUnavailable = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INRequestRideIntentResponseCode -->
<div> <!-- start type INRestaurantReservationUserBookingStatus -->
<h3>New Type Intents.INRestaurantReservationUserBookingStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRestaurantReservationUserBookingStatus {
	<span class='added added-field ' data-is-non-breaking="">Confirmed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Pending = 0,</span>
}
</pre>
</div> <!-- end type INRestaurantReservationUserBookingStatus -->
<div> <!-- start type INResumeWorkoutIntent -->
<h3>New Type Intents.INResumeWorkoutIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INResumeWorkoutIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INResumeWorkoutIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INResumeWorkoutIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INResumeWorkoutIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INResumeWorkoutIntent (INSpeakableString workoutName);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INResumeWorkoutIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString WorkoutName { get; }</span>
}
</pre>
</div> <!-- end type INResumeWorkoutIntent -->
<div> <!-- start type INResumeWorkoutIntentHandling_Extensions -->
<h3>New Type Intents.INResumeWorkoutIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INResumeWorkoutIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmResumeWorkout (IINResumeWorkoutIntentHandling This, INResumeWorkoutIntent intent, System.Action&lt;INResumeWorkoutIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutName (IINResumeWorkoutIntentHandling This, INResumeWorkoutIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INResumeWorkoutIntentHandling_Extensions -->
<div> <!-- start type INResumeWorkoutIntentResponse -->
<h3>New Type Intents.INResumeWorkoutIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INResumeWorkoutIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INResumeWorkoutIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INResumeWorkoutIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INResumeWorkoutIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INResumeWorkoutIntentResponse (INResumeWorkoutIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INResumeWorkoutIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INResumeWorkoutIntentResponse -->
<div> <!-- start type INResumeWorkoutIntentResponseCode -->
<h3>New Type Intents.INResumeWorkoutIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INResumeWorkoutIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoMatchingWorkout = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INResumeWorkoutIntentResponseCode -->
<div> <!-- start type INRideCompletionStatus -->
<h3>New Type Intents.INRideCompletionStatus</h3>
<pre class='added' data-is-non-breaking="">
public class INRideCompletionStatus : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideCompletionStatus (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideCompletionStatus (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideCompletionStatus (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Canceled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Completed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity CompletionUserActivity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MissedPickup { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Outstanding { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount PaymentAmount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetCanceledByService ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetCanceledByUser ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetCanceledMissedPickup ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetCompleted ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetOutstandingPaymentAmount (INCurrencyAmount outstandingPaymentAmount);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INRideCompletionStatus GetSettledPaymentAmount (INCurrencyAmount settledPaymentAmount);</span>
}
</pre>
</div> <!-- end type INRideCompletionStatus -->
<div> <!-- start type INRideDriver -->
<h3>New Type Intents.INRideDriver</h3>
<pre class='added' data-is-non-breaking="">
public class INRideDriver : Intents.INPerson, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, IINSpeakable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideDriver (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideDriver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideDriver (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRideDriver (string phoneNumber, Foundation.NSPersonNameComponents nameComponents, string displayName, INImage image, string rating);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PhoneNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Rating { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRideDriver -->
<div> <!-- start type INRideFareLineItem -->
<h3>New Type Intents.INRideFareLineItem</h3>
<pre class='added' data-is-non-breaking="">
public class INRideFareLineItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideFareLineItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideFareLineItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideFareLineItem (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRideFareLineItem (string title, Foundation.NSDecimalNumber price, string currencyCode);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CurrencyCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDecimalNumber Price { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRideFareLineItem -->
<div> <!-- start type INRideOption -->
<h3>New Type Intents.INRideOption</h3>
<pre class='added' data-is-non-breaking="">
public class INRideOption : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideOption (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideOption (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideOption (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRideOption (string name, Foundation.NSDate estimatedPickupDate);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INRidePartySizeOption[] AvailablePartySizeOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AvailablePartySizeOptionsSelectionPrompt { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisclaimerMessage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EstimatedPickupDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideFareLineItem[] FareLineItems { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPriceRange PriceRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpecialPricing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage SpecialPricingBadgeImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity UserActivityForBookingInApplication { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRideOption -->
<div> <!-- start type INRidePartySizeOption -->
<h3>New Type Intents.INRidePartySizeOption</h3>
<pre class='added' data-is-non-breaking="">
public class INRidePartySizeOption : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRidePartySizeOption (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRidePartySizeOption (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRidePartySizeOption (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRidePartySizeOption (Foundation.NSRange partySizeRange, string sizeDescription, INPriceRange priceRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSRange PartySizeRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPriceRange PriceRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SizeDescription { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRidePartySizeOption -->
<div> <!-- start type INRidePhase -->
<h3>New Type Intents.INRidePhase</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INRidePhase {
	<span class='added added-field ' data-is-non-breaking="">ApproachingPickup = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Completed = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Confirmed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ongoing = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Pickup = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Received = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INRidePhase -->
<div> <!-- start type INRideStatus -->
<h3>New Type Intents.INRideStatus</h3>
<pre class='added' data-is-non-breaking="">
public class INRideStatus : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideStatus (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideStatus (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideStatus (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity[] AdditionalActionActivities { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideCompletionStatus CompletionStatus { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideDriver Driver { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark DropOffLocation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EstimatedDropOffDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EstimatedPickupDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EstimatedPickupEndDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRidePhase Phase { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark PickupLocation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RideIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideOption RideOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange ScheduledPickupTime { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUserActivity UserActivityForCancelingInApplication { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INRideVehicle Vehicle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark[] Waypoints { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRideStatus -->
<div> <!-- start type INRideVehicle -->
<h3>New Type Intents.INRideVehicle</h3>
<pre class='added' data-is-non-breaking="">
public class INRideVehicle : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INRideVehicle ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INRideVehicle (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideVehicle (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INRideVehicle (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INImage MapAnnotationImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Model { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RegistrationPlate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type INRideVehicle -->
<div> <!-- start type INSearchCallHistoryIntent -->
<h3>New Type Intents.INSearchCallHistoryIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchCallHistoryIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntent (INCallRecordType callType, INDateComponentsRange dateCreated, INPerson recipient, INCallCapabilityOptions callCapabilities);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallCapabilityOptions CallCapabilities { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCallRecordType CallType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Recipient { get; }</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntent -->
<div> <!-- start type INSearchCallHistoryIntentHandling_Extensions -->
<h3>New Type Intents.INSearchCallHistoryIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchCallHistoryIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearchCallHistory (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INSearchCallHistoryIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCallType (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INCallRecordTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateCreated (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipient (IINSearchCallHistoryIntentHandling This, INSearchCallHistoryIntent intent, System.Action&lt;INPersonResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentHandling_Extensions -->
<div> <!-- start type INSearchCallHistoryIntentResponse -->
<h3>New Type Intents.INSearchCallHistoryIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchCallHistoryIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchCallHistoryIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchCallHistoryIntentResponse (INSearchCallHistoryIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchCallHistoryIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentResponse -->
<div> <!-- start type INSearchCallHistoryIntentResponseCode -->
<h3>New Type Intents.INSearchCallHistoryIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchCallHistoryIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchCallHistoryIntentResponseCode -->
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
<div> <!-- start type INSearchForMessagesIntent -->
<h3>New Type Intents.INSearchForMessagesIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForMessagesIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntent (INPerson[] recipients, INPerson[] senders, string[] searchTerms, INMessageAttributeOptions attributes, INDateComponentsRange dateTimeRange, string[] identifiers, string[] notificationIdentifiers, string[] groupNames);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessageAttributeOptions Attributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateTimeRange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] GroupNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator GroupNamesOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] Identifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator IdentifiersOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] NotificationIdentifiers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator NotificationIdentifiersOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator RecipientsOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SearchTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SearchTermsOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Senders { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SendersOperator { get; }</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntent -->
<div> <!-- start type INSearchForMessagesIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForMessagesIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForMessagesIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearchForMessages (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INSearchForMessagesIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAttributes (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INMessageAttributeOptionsResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateTimeRange (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupNames (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INStringResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveSenders (IINSearchForMessagesIntentHandling This, INSearchForMessagesIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentHandling_Extensions -->
<div> <!-- start type INSearchForMessagesIntentResponse -->
<h3>New Type Intents.INSearchForMessagesIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForMessagesIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForMessagesIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForMessagesIntentResponse (INSearchForMessagesIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForMessagesIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INMessage[] Messages { get; set; }</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentResponse -->
<div> <!-- start type INSearchForMessagesIntentResponseCode -->
<h3>New Type Intents.INSearchForMessagesIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForMessagesIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForMessagesIntentResponseCode -->
<div> <!-- start type INSearchForPhotosIntent -->
<h3>New Type Intents.INSearchForPhotosIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForPhotosIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForPhotosIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForPhotosIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForPhotosIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForPhotosIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForPhotosIntent (INDateComponentsRange dateCreated, CoreLocation.CLPlacemark locationCreated, string albumName, string[] searchTerms, INPhotoAttributeOptions includedAttributes, INPhotoAttributeOptions excludedAttributes, INPerson[] peopleInPhoto);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AlbumName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPhotoAttributeOptions ExcludedAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPhotoAttributeOptions IncludedAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark LocationCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] PeopleInPhoto { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator PeopleInPhotoOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SearchTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SearchTermsOperator { get; }</span>
}
</pre>
</div> <!-- end type INSearchForPhotosIntent -->
<div> <!-- start type INSearchForPhotosIntentHandling_Extensions -->
<h3>New Type Intents.INSearchForPhotosIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSearchForPhotosIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSearchForPhotos (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INSearchForPhotosIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAlbumName (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateCreated (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveLocationCreated (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePeopleInPhoto (IINSearchForPhotosIntentHandling This, INSearchForPhotosIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INSearchForPhotosIntentHandling_Extensions -->
<div> <!-- start type INSearchForPhotosIntentResponse -->
<h3>New Type Intents.INSearchForPhotosIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSearchForPhotosIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForPhotosIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForPhotosIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSearchForPhotosIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSearchForPhotosIntentResponse (INSearchForPhotosIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSearchForPhotosIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SearchResultsCount { get; set; }</span>
}
</pre>
</div> <!-- end type INSearchForPhotosIntentResponse -->
<div> <!-- start type INSearchForPhotosIntentResponseCode -->
<h3>New Type Intents.INSearchForPhotosIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSearchForPhotosIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSearchForPhotosIntentResponseCode -->
<div> <!-- start type INSendMessageIntent -->
<h3>New Type Intents.INSendMessageIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntent (INPerson[] recipients, string content, string groupName, string serviceName, INPerson sender);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GroupName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Recipients { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Sender { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ServiceName { get; }</span>
}
</pre>
</div> <!-- end type INSendMessageIntent -->
<div> <!-- start type INSendMessageIntentHandling_Extensions -->
<h3>New Type Intents.INSendMessageIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSendMessageIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSendMessage (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INSendMessageIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContent (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGroupName (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveRecipients (IINSendMessageIntentHandling This, INSendMessageIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INSendMessageIntentHandling_Extensions -->
<div> <!-- start type INSendMessageIntentResponse -->
<h3>New Type Intents.INSendMessageIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSendMessageIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendMessageIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendMessageIntentResponse (INSendMessageIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSendMessageIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INSendMessageIntentResponse -->
<div> <!-- start type INSendMessageIntentResponseCode -->
<h3>New Type Intents.INSendMessageIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendMessageIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureMessageServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSendMessageIntentResponseCode -->
<div> <!-- start type INSendPaymentIntent -->
<h3>New Type Intents.INSendPaymentIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSendPaymentIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentIntent (INPerson payee, INCurrencyAmount currencyAmount, string note);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INCurrencyAmount CurrencyAmount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Note { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson Payee { get; }</span>
}
</pre>
</div> <!-- end type INSendPaymentIntent -->
<div> <!-- start type INSendPaymentIntentHandling_Extensions -->
<h3>New Type Intents.INSendPaymentIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INSendPaymentIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmSendPayment (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INSendPaymentIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveCurrencyAmount (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INCurrencyAmountResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveNote (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePayee (IINSendPaymentIntentHandling This, INSendPaymentIntent intent, System.Action&lt;INPersonResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INSendPaymentIntentHandling_Extensions -->
<div> <!-- start type INSendPaymentIntentResponse -->
<h3>New Type Intents.INSendPaymentIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INSendPaymentIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSendPaymentIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSendPaymentIntentResponse (INSendPaymentIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSendPaymentIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPaymentRecord PaymentRecord { get; set; }</span>
}
</pre>
</div> <!-- end type INSendPaymentIntentResponse -->
<div> <!-- start type INSendPaymentIntentResponseCode -->
<h3>New Type Intents.INSendPaymentIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSendPaymentIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">Failure = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCredentialsUnverified = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureInsufficientFunds = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoBankAccount = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsAmountAboveMaximum = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsAmountBelowMinimum = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">FailurePaymentsCurrencyUnsupported = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InProgress = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INSendPaymentIntentResponseCode -->
<div> <!-- start type INSetCarLockStatusIntent -->
<h3>New Type Intents.INSetCarLockStatusIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INSetCarLockStatusIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INSetCarLockStatusIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSetCarLockStatusIntent (Foundation.NSNumber locked, INSpeakableString carName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString CarName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
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
<div> <!-- start type INSiriAuthorizationStatus -->
<h3>New Type Intents.INSiriAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INSiriAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type INSiriAuthorizationStatus -->
<div> <!-- start type INSpeakableString -->
<h3>New Type Intents.INSpeakableString</h3>
<pre class='added' data-is-non-breaking="">
public class INSpeakableString : Foundation.NSObject, Foundation.INSObjectProtocol, IINSpeakable, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableString (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableString (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (string spokenPhrase);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INSpeakableString (string identifier, string spokenPhrase, string pronunciationHint);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PronunciationHint { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SpokenPhrase { get; }</span>
}
</pre>
</div> <!-- end type INSpeakableString -->
<div> <!-- start type INSpeakableStringResolutionResult -->
<h3>New Type Intents.INSpeakableStringResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INSpeakableStringResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableStringResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INSpeakableStringResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INSpeakableStringResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetConfirmationRequired (INSpeakableString stringToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetDisambiguation (INSpeakableString[] stringsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INSpeakableStringResolutionResult GetSuccess (INSpeakableString resolvedString);</span>
}
</pre>
</div> <!-- end type INSpeakableStringResolutionResult -->
<div> <!-- start type INStartAudioCallIntent -->
<h3>New Type Intents.INStartAudioCallIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INStartAudioCallIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntent (INPerson[] contacts);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] Contacts { get; }</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntent -->
<div> <!-- start type INStartAudioCallIntentHandling_Extensions -->
<h3>New Type Intents.INStartAudioCallIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INStartAudioCallIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmStartAudioCall (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INStartAudioCallIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveContacts (IINStartAudioCallIntentHandling This, INStartAudioCallIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentHandling_Extensions -->
<div> <!-- start type INStartAudioCallIntentResponse -->
<h3>New Type Intents.INStartAudioCallIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INStartAudioCallIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartAudioCallIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartAudioCallIntentResponse (INStartAudioCallIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INStartAudioCallIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentResponse -->
<div> <!-- start type INStartAudioCallIntentResponseCode -->
<h3>New Type Intents.INStartAudioCallIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INStartAudioCallIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureCallingServiceNotAvailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INStartAudioCallIntentResponseCode -->
<div> <!-- start type INStartPhotoPlaybackIntent -->
<h3>New Type Intents.INStartPhotoPlaybackIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INStartPhotoPlaybackIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartPhotoPlaybackIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartPhotoPlaybackIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartPhotoPlaybackIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartPhotoPlaybackIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartPhotoPlaybackIntent (INDateComponentsRange dateCreated, CoreLocation.CLPlacemark locationCreated, string albumName, string[] searchTerms, INPhotoAttributeOptions includedAttributes, INPhotoAttributeOptions excludedAttributes, INPerson[] peopleInPhoto);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AlbumName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INDateComponentsRange DateCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPhotoAttributeOptions ExcludedAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPhotoAttributeOptions IncludedAttributes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLPlacemark LocationCreated { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INPerson[] PeopleInPhoto { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator PeopleInPhotoOperator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SearchTerms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INConditionalOperator SearchTermsOperator { get; }</span>
}
</pre>
</div> <!-- end type INStartPhotoPlaybackIntent -->
<div> <!-- start type INStartPhotoPlaybackIntentHandling_Extensions -->
<h3>New Type Intents.INStartPhotoPlaybackIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INStartPhotoPlaybackIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmStartPhotoPlayback (IINStartPhotoPlaybackIntentHandling This, INStartPhotoPlaybackIntent intent, System.Action&lt;INStartPhotoPlaybackIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveAlbumName (IINStartPhotoPlaybackIntentHandling This, INStartPhotoPlaybackIntent intent, System.Action&lt;INStringResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveDateCreated (IINStartPhotoPlaybackIntentHandling This, INStartPhotoPlaybackIntent intent, System.Action&lt;INDateComponentsRangeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveLocationCreated (IINStartPhotoPlaybackIntentHandling This, INStartPhotoPlaybackIntent intent, System.Action&lt;INPlacemarkResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolvePeopleInPhoto (IINStartPhotoPlaybackIntentHandling This, INStartPhotoPlaybackIntent intent, System.Action&lt;INPersonResolutionResult[]&gt; completion);</span>
}
</pre>
</div> <!-- end type INStartPhotoPlaybackIntentHandling_Extensions -->
<div> <!-- start type INStartPhotoPlaybackIntentResponse -->
<h3>New Type Intents.INStartPhotoPlaybackIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INStartPhotoPlaybackIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartPhotoPlaybackIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartPhotoPlaybackIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartPhotoPlaybackIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartPhotoPlaybackIntentResponse (INStartPhotoPlaybackIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INStartPhotoPlaybackIntentResponseCode Code { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber SearchResultsCount { get; set; }</span>
}
</pre>
</div> <!-- end type INStartPhotoPlaybackIntentResponse -->
<div> <!-- start type INStartPhotoPlaybackIntentResponseCode -->
<h3>New Type Intents.INStartPhotoPlaybackIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INStartPhotoPlaybackIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureAppConfigurationRequired = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INStartPhotoPlaybackIntentResponseCode -->
<div> <!-- start type INStartWorkoutIntent -->
<h3>New Type Intents.INStartWorkoutIntent</h3>
<pre class='added' data-is-non-breaking="">
public class INStartWorkoutIntent : Intents.INIntent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartWorkoutIntent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartWorkoutIntent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartWorkoutIntent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartWorkoutIntent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartWorkoutIntent (INSpeakableString workoutName, Foundation.NSNumber goalValue, INWorkoutGoalUnitType workoutGoalUnitType, INWorkoutLocationType workoutLocationType, Foundation.NSNumber isOpenEnded);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber GoalValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INWorkoutGoalUnitType WorkoutGoalUnitType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INWorkoutLocationType WorkoutLocationType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INSpeakableString WorkoutName { get; }</span>
}
</pre>
</div> <!-- end type INStartWorkoutIntent -->
<div> <!-- start type INStartWorkoutIntentHandling_Extensions -->
<h3>New Type Intents.INStartWorkoutIntentHandling_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INStartWorkoutIntentHandling_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void ConfirmStartWorkout (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INStartWorkoutIntentResponse&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveGoalValue (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INDoubleResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveIsOpenEnded (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INBooleanResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutGoalUnitType (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INWorkoutGoalUnitTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutLocationType (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INWorkoutLocationTypeResolutionResult&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResolveWorkoutName (IINStartWorkoutIntentHandling This, INStartWorkoutIntent intent, System.Action&lt;INSpeakableStringResolutionResult&gt; completion);</span>
}
</pre>
</div> <!-- end type INStartWorkoutIntentHandling_Extensions -->
<div> <!-- start type INStartWorkoutIntentResponse -->
<h3>New Type Intents.INStartWorkoutIntentResponse</h3>
<pre class='added' data-is-non-breaking="">
public class INStartWorkoutIntentResponse : Intents.INIntentResponse, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public INStartWorkoutIntentResponse (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartWorkoutIntentResponse (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStartWorkoutIntentResponse (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public INStartWorkoutIntentResponse (INStartWorkoutIntentResponseCode code, Foundation.NSUserActivity userActivity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual INStartWorkoutIntentResponseCode Code { get; }</span>
}
</pre>
</div> <!-- end type INStartWorkoutIntentResponse -->
<div> <!-- start type INStartWorkoutIntentResponseCode -->
<h3>New Type Intents.INStartWorkoutIntentResponseCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INStartWorkoutIntentResponseCode {
	<span class='added added-field ' data-is-non-breaking="">ContinueInApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failure = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureNoMatchingWorkout = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureOngoingWorkout = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FailureRequiringAppLaunch = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Ready = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type INStartWorkoutIntentResponseCode -->
<div> <!-- start type INStringResolutionResult -->
<h3>New Type Intents.INStringResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INStringResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INStringResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INStringResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INStringResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetConfirmationRequired (string stringToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetDisambiguation (string[] stringsToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INStringResolutionResult GetSuccess (string resolvedString);</span>
}
</pre>
</div> <!-- end type INStringResolutionResult -->
<div> <!-- start type INTemperatureResolutionResult -->
<h3>New Type Intents.INTemperatureResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INTemperatureResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemperatureResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INTemperatureResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemperatureResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemperatureResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INTemperatureResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INTemperatureResolutionResult GetConfirmationRequired (Foundation.NSMeasurement&lt;Foundation.NSUnitTemperature&gt; temperatureToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTemperatureResolutionResult GetDisambiguation (Foundation.NSMeasurement&lt;Foundation.NSUnitTemperature&gt;[] temperaturesToDisambiguate);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INTemperatureResolutionResult GetSuccess (Foundation.NSMeasurement&lt;Foundation.NSUnitTemperature&gt; resolvedTemperature);</span>
}
</pre>
</div> <!-- end type INTemperatureResolutionResult -->
<div> <!-- start type INWorkoutGoalUnitType -->
<h3>New Type Intents.INWorkoutGoalUnitType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INWorkoutGoalUnitType {
	<span class='added added-field ' data-is-non-breaking="">Foot = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Hour = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Inch = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Joule = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">KiloCalorie = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Meter = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Mile = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Minute = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Second = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Yard = 5,</span>
}
</pre>
</div> <!-- end type INWorkoutGoalUnitType -->
<div> <!-- start type INWorkoutGoalUnitTypeResolutionResult -->
<h3>New Type Intents.INWorkoutGoalUnitTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INWorkoutGoalUnitTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INWorkoutGoalUnitTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INWorkoutGoalUnitTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutGoalUnitTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutGoalUnitTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutGoalUnitTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INWorkoutGoalUnitTypeResolutionResult GetConfirmationRequired (INWorkoutGoalUnitType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INWorkoutGoalUnitTypeResolutionResult GetSuccess (INWorkoutGoalUnitType resolvedValue);</span>
}
</pre>
</div> <!-- end type INWorkoutGoalUnitTypeResolutionResult -->
<div> <!-- start type INWorkoutLocationType -->
<h3>New Type Intents.INWorkoutLocationType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INWorkoutLocationType {
	<span class='added added-field ' data-is-non-breaking="">Indoor = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Outdoor = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type INWorkoutLocationType -->
<div> <!-- start type INWorkoutLocationTypeResolutionResult -->
<h3>New Type Intents.INWorkoutLocationTypeResolutionResult</h3>
<pre class='added' data-is-non-breaking="">
public class INWorkoutLocationTypeResolutionResult : Intents.INIntentResolutionResult, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected INWorkoutLocationTypeResolutionResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected INWorkoutLocationTypeResolutionResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutLocationTypeResolutionResult NeedsValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutLocationTypeResolutionResult NotRequired { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static INWorkoutLocationTypeResolutionResult Unsupported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INWorkoutLocationTypeResolutionResult GetConfirmationRequired (INWorkoutLocationType valueToConfirm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INWorkoutLocationTypeResolutionResult GetSuccess (INWorkoutLocationType resolvedValue);</span>
}
</pre>
</div> <!-- end type INWorkoutLocationTypeResolutionResult -->
<div> <!-- start type INWorkoutNameIdentifier -->
<h3>New Type Intents.INWorkoutNameIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum INWorkoutNameIdentifier {
	<span class='added added-field ' data-is-non-breaking="">Crosstraining = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Cycle = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Dance = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Elliptical = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Exercise = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Indoorcycle = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Indoorrun = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Indoorwalk = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">Move = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Other = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Rower = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Run = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sit = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Stairs = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Stand = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Steps = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Walk = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Yoga = 6,</span>
}
</pre>
</div> <!-- end type INWorkoutNameIdentifier -->
<div> <!-- start type INWorkoutNameIdentifierExtensions -->
<h3>New Type Intents.INWorkoutNameIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class INWorkoutNameIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (INWorkoutNameIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static INWorkoutNameIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type INWorkoutNameIdentifierExtensions -->
<div> <!-- start type NSUserActivity_IntentsAdditions -->
<h3>New Type Intents.NSUserActivity_IntentsAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_IntentsAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static INInteraction GetInteraction (Foundation.NSUserActivity This);</span>
}
</pre>
</div> <!-- end type NSUserActivity_IntentsAdditions -->
</div> <!-- end namespace Intents -->

<!-- start namespace System.Drawing --> <div> 
<h2>New Namespace System.Drawing</h2>

<div> <!-- start type Color -->
<h3>New Type System.Drawing.Color</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct Color {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static Color Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public byte A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color AliceBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color AntiqueWhite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Aqua { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Aquamarine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Azure { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Beige { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Bisque { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Black { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color BlanchedAlmond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Blue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color BlueViolet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Brown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color BurlyWood { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color CadetBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Chartreuse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Chocolate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Coral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color CornflowerBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Cornsilk { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Crimson { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Cyan { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkCyan { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkGoldenrod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkKhaki { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkMagenta { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkOliveGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkOrange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkOrchid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkRed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkSalmon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkSeaGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkSlateBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkSlateGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkTurquoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DarkViolet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DeepPink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DeepSkyBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DimGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color DodgerBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Firebrick { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color FloralWhite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color ForestGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Fuchsia { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte G { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Gainsboro { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color GhostWhite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Gold { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Goldenrod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Gray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Green { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color GreenYellow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Honeydew { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color HotPink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color IndianRed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Indigo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsKnownColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsNamedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsSystemColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Ivory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Khaki { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Lavender { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LavenderBlush { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LawnGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LemonChiffon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightCoral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightCyan { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightGoldenrodYellow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightPink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightSalmon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightSeaGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightSkyBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightSlateGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightSteelBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LightYellow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Lime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color LimeGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Linen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Magenta { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Maroon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumAquamarine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumOrchid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumPurple { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumSeaGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumSlateBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumSpringGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumTurquoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MediumVioletRed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MidnightBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MintCream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color MistyRose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Moccasin { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color NavajoWhite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Navy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color OldLace { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Olive { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color OliveDrab { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Orange { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color OrangeRed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Orchid { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PaleGoldenrod { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PaleGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PaleTurquoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PaleVioletRed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PapayaWhip { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PeachPuff { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Peru { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Pink { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Plum { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color PowderBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Purple { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte R { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Red { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color RosyBrown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color RoyalBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SaddleBrown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Salmon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SandyBrown { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SeaGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SeaShell { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Sienna { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Silver { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SkyBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SlateBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SlateGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Snow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SpringGreen { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color SteelBlue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Tan { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Teal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Thistle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Tomato { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Transparent { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Turquoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Violet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Wheat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color White { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color WhiteSmoke { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color Yellow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Color YellowGreen { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromArgb (int argb);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromArgb (int alpha, Color baseColor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromArgb (int red, int green, int blue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromArgb (int alpha, int red, int green, int blue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromKnownColor (KnownColor color);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Color FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public float GetBrightness ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float GetHue ();</span>
	<span class='added added-method ' data-is-non-breaking="">public float GetSaturation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public int ToArgb ();</span>
	<span class='added added-method ' data-is-non-breaking="">public KnownColor ToKnownColor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Color left, Color right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Color left, Color right);</span>
}
</pre>
</div> <!-- end type Color -->
<div> <!-- start type KnownColor -->
<h3>New Type System.Drawing.KnownColor</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum KnownColor {
	<span class='added added-field ' data-is-non-breaking="">ActiveBorder = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveCaption = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ActiveCaptionText = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AliceBlue = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">AntiqueWhite = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">AppWorkspace = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Aqua = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">Aquamarine = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">Azure = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Beige = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">Bisque = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">Black = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">BlanchedAlmond = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">Blue = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">BlueViolet = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">Brown = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">BurlyWood = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">ButtonFace = 168,</span>
	<span class='added added-field ' data-is-non-breaking="">ButtonHighlight = 169,</span>
	<span class='added added-field ' data-is-non-breaking="">ButtonShadow = 170,</span>
	<span class='added added-field ' data-is-non-breaking="">CadetBlue = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">Chartreuse = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">Chocolate = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">Control = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlDark = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlDarkDark = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlLight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlLightLight = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">ControlText = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Coral = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">CornflowerBlue = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">Cornsilk = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">Crimson = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">Cyan = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkBlue = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkCyan = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkGoldenrod = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkGray = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkGreen = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkKhaki = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkMagenta = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkOliveGreen = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkOrange = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkOrchid = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkRed = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkSalmon = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkSeaGreen = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkSlateBlue = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkSlateGray = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkTurquoise = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">DarkViolet = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">DeepPink = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">DeepSkyBlue = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">Desktop = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">DimGray = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">DodgerBlue = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">Firebrick = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">FloralWhite = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">ForestGreen = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">Fuchsia = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">Gainsboro = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">GhostWhite = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">Gold = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">Goldenrod = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">GradientActiveCaption = 171,</span>
	<span class='added added-field ' data-is-non-breaking="">GradientInactiveCaption = 172,</span>
	<span class='added added-field ' data-is-non-breaking="">Gray = 78,</span>
	<span class='added added-field ' data-is-non-breaking="">GrayText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Green = 79,</span>
	<span class='added added-field ' data-is-non-breaking="">GreenYellow = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">Highlight = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">HighlightText = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Honeydew = 81,</span>
	<span class='added added-field ' data-is-non-breaking="">HotPink = 82,</span>
	<span class='added added-field ' data-is-non-breaking="">HotTrack = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InactiveBorder = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">InactiveCaption = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InactiveCaptionText = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">IndianRed = 83,</span>
	<span class='added added-field ' data-is-non-breaking="">Indigo = 84,</span>
	<span class='added added-field ' data-is-non-breaking="">Info = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">InfoText = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Ivory = 85,</span>
	<span class='added added-field ' data-is-non-breaking="">Khaki = 86,</span>
	<span class='added added-field ' data-is-non-breaking="">Lavender = 87,</span>
	<span class='added added-field ' data-is-non-breaking="">LavenderBlush = 88,</span>
	<span class='added added-field ' data-is-non-breaking="">LawnGreen = 89,</span>
	<span class='added added-field ' data-is-non-breaking="">LemonChiffon = 90,</span>
	<span class='added added-field ' data-is-non-breaking="">LightBlue = 91,</span>
	<span class='added added-field ' data-is-non-breaking="">LightCoral = 92,</span>
	<span class='added added-field ' data-is-non-breaking="">LightCyan = 93,</span>
	<span class='added added-field ' data-is-non-breaking="">LightGoldenrodYellow = 94,</span>
	<span class='added added-field ' data-is-non-breaking="">LightGray = 95,</span>
	<span class='added added-field ' data-is-non-breaking="">LightGreen = 96,</span>
	<span class='added added-field ' data-is-non-breaking="">LightPink = 97,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSalmon = 98,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSeaGreen = 99,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSkyBlue = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSlateGray = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSteelBlue = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">LightYellow = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">Lime = 104,</span>
	<span class='added added-field ' data-is-non-breaking="">LimeGreen = 105,</span>
	<span class='added added-field ' data-is-non-breaking="">Linen = 106,</span>
	<span class='added added-field ' data-is-non-breaking="">Magenta = 107,</span>
	<span class='added added-field ' data-is-non-breaking="">Maroon = 108,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumAquamarine = 109,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumBlue = 110,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumOrchid = 111,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumPurple = 112,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumSeaGreen = 113,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumSlateBlue = 114,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumSpringGreen = 115,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumTurquoise = 116,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumVioletRed = 117,</span>
	<span class='added added-field ' data-is-non-breaking="">Menu = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">MenuBar = 173,</span>
	<span class='added added-field ' data-is-non-breaking="">MenuHighlight = 174,</span>
	<span class='added added-field ' data-is-non-breaking="">MenuText = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">MidnightBlue = 118,</span>
	<span class='added added-field ' data-is-non-breaking="">MintCream = 119,</span>
	<span class='added added-field ' data-is-non-breaking="">MistyRose = 120,</span>
	<span class='added added-field ' data-is-non-breaking="">Moccasin = 121,</span>
	<span class='added added-field ' data-is-non-breaking="">NavajoWhite = 122,</span>
	<span class='added added-field ' data-is-non-breaking="">Navy = 123,</span>
	<span class='added added-field ' data-is-non-breaking="">OldLace = 124,</span>
	<span class='added added-field ' data-is-non-breaking="">Olive = 125,</span>
	<span class='added added-field ' data-is-non-breaking="">OliveDrab = 126,</span>
	<span class='added added-field ' data-is-non-breaking="">Orange = 127,</span>
	<span class='added added-field ' data-is-non-breaking="">OrangeRed = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Orchid = 129,</span>
	<span class='added added-field ' data-is-non-breaking="">PaleGoldenrod = 130,</span>
	<span class='added added-field ' data-is-non-breaking="">PaleGreen = 131,</span>
	<span class='added added-field ' data-is-non-breaking="">PaleTurquoise = 132,</span>
	<span class='added added-field ' data-is-non-breaking="">PaleVioletRed = 133,</span>
	<span class='added added-field ' data-is-non-breaking="">PapayaWhip = 134,</span>
	<span class='added added-field ' data-is-non-breaking="">PeachPuff = 135,</span>
	<span class='added added-field ' data-is-non-breaking="">Peru = 136,</span>
	<span class='added added-field ' data-is-non-breaking="">Pink = 137,</span>
	<span class='added added-field ' data-is-non-breaking="">Plum = 138,</span>
	<span class='added added-field ' data-is-non-breaking="">PowderBlue = 139,</span>
	<span class='added added-field ' data-is-non-breaking="">Purple = 140,</span>
	<span class='added added-field ' data-is-non-breaking="">Red = 141,</span>
	<span class='added added-field ' data-is-non-breaking="">RosyBrown = 142,</span>
	<span class='added added-field ' data-is-non-breaking="">RoyalBlue = 143,</span>
	<span class='added added-field ' data-is-non-breaking="">SaddleBrown = 144,</span>
	<span class='added added-field ' data-is-non-breaking="">Salmon = 145,</span>
	<span class='added added-field ' data-is-non-breaking="">SandyBrown = 146,</span>
	<span class='added added-field ' data-is-non-breaking="">ScrollBar = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">SeaGreen = 147,</span>
	<span class='added added-field ' data-is-non-breaking="">SeaShell = 148,</span>
	<span class='added added-field ' data-is-non-breaking="">Sienna = 149,</span>
	<span class='added added-field ' data-is-non-breaking="">Silver = 150,</span>
	<span class='added added-field ' data-is-non-breaking="">SkyBlue = 151,</span>
	<span class='added added-field ' data-is-non-breaking="">SlateBlue = 152,</span>
	<span class='added added-field ' data-is-non-breaking="">SlateGray = 153,</span>
	<span class='added added-field ' data-is-non-breaking="">Snow = 154,</span>
	<span class='added added-field ' data-is-non-breaking="">SpringGreen = 155,</span>
	<span class='added added-field ' data-is-non-breaking="">SteelBlue = 156,</span>
	<span class='added added-field ' data-is-non-breaking="">Tan = 157,</span>
	<span class='added added-field ' data-is-non-breaking="">Teal = 158,</span>
	<span class='added added-field ' data-is-non-breaking="">Thistle = 159,</span>
	<span class='added added-field ' data-is-non-breaking="">Tomato = 160,</span>
	<span class='added added-field ' data-is-non-breaking="">Transparent = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">Turquoise = 161,</span>
	<span class='added added-field ' data-is-non-breaking="">Violet = 162,</span>
	<span class='added added-field ' data-is-non-breaking="">Wheat = 163,</span>
	<span class='added added-field ' data-is-non-breaking="">White = 164,</span>
	<span class='added added-field ' data-is-non-breaking="">WhiteSmoke = 165,</span>
	<span class='added added-field ' data-is-non-breaking="">Window = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowFrame = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowText = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Yellow = 166,</span>
	<span class='added added-field ' data-is-non-breaking="">YellowGreen = 167,</span>
}
</pre>
</div> <!-- end type KnownColor -->
<div> <!-- start type Point -->
<h3>New Type System.Drawing.Point</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct Point {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Point (Size sz);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Point (int dw);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Point (int x, int y);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static Point Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Point Add (Point pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point Ceiling (PointF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (Point p);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (int dx, int dy);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point Round (PointF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point Subtract (Point pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point Truncate (PointF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point op_Addition (Point pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Point left, Point right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size op_Explicit (Point p);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Implicit (Point p);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Point left, Point right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point op_Subtraction (Point pt, Size sz);</span>
}
</pre>
</div> <!-- end type Point -->
<div> <!-- start type PointF -->
<h3>New Type System.Drawing.PointF</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct PointF {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PointF (float x, float y);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static PointF Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PointF Add (PointF pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF Add (PointF pt, SizeF sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF Subtract (PointF pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF Subtract (PointF pt, SizeF sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Addition (PointF pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Addition (PointF pt, SizeF sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (PointF left, PointF right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (PointF left, PointF right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Subtraction (PointF pt, Size sz);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Subtraction (PointF pt, SizeF sz);</span>
}
</pre>
</div> <!-- end type PointF -->
<div> <!-- start type Rectangle -->
<h3>New Type System.Drawing.Rectangle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct Rectangle {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Rectangle (Point location, Size size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Rectangle (int x, int y, int width, int height);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static Rectangle Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int Bottom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Left { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Point Location { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Right { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Size Size { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Top { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Width { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Ceiling (RectangleF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (Point pt);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (Rectangle rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (int x, int y);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle FromLTRB (int left, int top, int right, int bottom);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Inflate (Size size);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Inflate (int width, int height);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Inflate (Rectangle rect, int x, int y);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Intersect (Rectangle rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Intersect (Rectangle a, Rectangle b);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IntersectsWith (Rectangle rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (Point pos);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (int x, int y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Round (RectangleF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Truncate (RectangleF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Rectangle Union (Rectangle a, Rectangle b);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Rectangle left, Rectangle right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Rectangle left, Rectangle right);</span>
}
</pre>
</div> <!-- end type Rectangle -->
<div> <!-- start type RectangleF -->
<h3>New Type System.Drawing.RectangleF</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct RectangleF {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RectangleF (PointF location, SizeF size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RectangleF (float x, float y, float width, float height);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static RectangleF Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Bottom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Left { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PointF Location { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Right { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SizeF Size { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Top { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Width { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float X { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Y { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (PointF pt);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (RectangleF rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (float x, float y);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RectangleF FromLTRB (float left, float top, float right, float bottom);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Inflate (SizeF size);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Inflate (float x, float y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RectangleF Inflate (RectangleF rect, float x, float y);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Intersect (RectangleF rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RectangleF Intersect (RectangleF a, RectangleF b);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool IntersectsWith (RectangleF rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (PointF pos);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Offset (float x, float y);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static RectangleF Union (RectangleF a, RectangleF b);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (RectangleF left, RectangleF right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RectangleF op_Implicit (Rectangle r);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (RectangleF left, RectangleF right);</span>
}
</pre>
</div> <!-- end type RectangleF -->
<div> <!-- start type Size -->
<h3>New Type System.Drawing.Size</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct Size {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public Size (Point pt);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public Size (int width, int height);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static Size Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public int Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int Width { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Size Add (Size sz1, Size sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size Ceiling (SizeF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size Round (SizeF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size Subtract (Size sz1, Size sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size Truncate (SizeF value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size op_Addition (Size sz1, Size sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (Size sz1, Size sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Point op_Explicit (Size size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SizeF op_Implicit (Size p);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (Size sz1, Size sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Size op_Subtraction (Size sz1, Size sz2);</span>
}
</pre>
</div> <!-- end type Size -->
<div> <!-- start type SizeF -->
<h3>New Type System.Drawing.SizeF</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public struct SizeF {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SizeF (PointF pt);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SizeF (SizeF size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SizeF (float width, float height);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static SizeF Empty;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public float Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEmpty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Width { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SizeF Add (SizeF sz1, SizeF sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static SizeF Subtract (SizeF sz1, SizeF sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public PointF ToPointF ();</span>
	<span class='added added-method ' data-is-non-breaking="">public Size ToSize ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static SizeF op_Addition (SizeF sz1, SizeF sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (SizeF sz1, SizeF sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PointF op_Explicit (SizeF size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (SizeF sz1, SizeF sz2);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SizeF op_Subtraction (SizeF sz1, SizeF sz2);</span>
}
</pre>
</div> <!-- end type SizeF -->
</div> <!-- end namespace System.Drawing -->

</div>



   


 <hr>
