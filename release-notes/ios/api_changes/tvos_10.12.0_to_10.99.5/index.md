---
id: 360F5030-8424-4539-B603-81DB19EF3747
title: "tvOS 10.12.0 to 10.99.5"
---

# API diff

 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html)

   


   


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
<!-- start type AVPlayerLayer --> <div>
<h3>Type Changed: AVFoundation.AVPlayerLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVPlayerLayer -->
<!-- start type AVSampleBufferDisplayLayer --> <div>
<h3>Type Changed: AVFoundation.AVSampleBufferDisplayLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSampleBufferDisplayLayer -->
<!-- start type AVSynchronizedLayer --> <div>
<h3>Type Changed: AVFoundation.AVSynchronizedLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type AVSynchronizedLayer -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AVKit --> <div> 
<h2>Namespace AVKit</h2>
<!-- start type AVKitMetadataIdentifier --> <div>
<h3>Type Changed: AVKit.AVKitMetadataIdentifier</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ApproximateStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExactStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type AVKitMetadataIdentifier -->
<!-- start type AVPlayerViewController --> <div>
<h3>Type Changed: AVKit.AVPlayerViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIViewController CustomInfoViewController { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeInfoViews { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PlaybackControlsIncludeTransportBar { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UILayoutGuide UnobscuredContentGuide { get; }</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewController -->
<!-- start type AVPlayerViewControllerDelegate --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldDismiss (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginDismissalTransition (AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillTransitionToVisibilityOfTransportBar (AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate -->
<!-- start type AVPlayerViewControllerDelegate_Extensions --> <div>
<h3>Type Changed: AVKit.AVPlayerViewControllerDelegate_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldDismiss (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginDismissalTransition (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillTransitionToVisibilityOfTransportBar (IAVPlayerViewControllerDelegate This, AVPlayerViewController playerViewController, bool visible, IAVPlayerViewControllerAnimationCoordinator coordinator);</span>
</pre>
</div>

</div> <!-- end type AVPlayerViewControllerDelegate_Extensions -->
<div> <!-- start type AVRoutePickerView -->
<h3>New Type AVKit.AVRoutePickerView</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor ActiveTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IAVRoutePickerViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVRoutePickerViewButtonStyle RoutePickerButtonStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AVRoutePickerView.AVRoutePickerViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class AVRoutePickerViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type AVRoutePickerView -->
<div> <!-- start type AVRoutePickerViewButtonStyle -->
<h3>New Type AVKit.AVRoutePickerViewButtonStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVRoutePickerViewButtonStyle {
	<span class='added added-field ' data-is-non-breaking="">Custom = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Plain = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">System = 0,</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewButtonStyle -->
<div> <!-- start type AVRoutePickerViewDelegate -->
<h3>New Type AVKit.AVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class AVRoutePickerViewDelegate : Foundation.NSObject, IAVRoutePickerViewDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AVRoutePickerViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected AVRoutePickerViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPresentingRoutes (AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPresentingRoutes (AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate -->
<div> <!-- start type AVRoutePickerViewDelegate_Extensions -->
<h3>New Type AVKit.AVRoutePickerViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class AVRoutePickerViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPresentingRoutes (IAVRoutePickerViewDelegate This, AVRoutePickerView routePickerView);</span>
}
</pre>
</div> <!-- end type AVRoutePickerViewDelegate_Extensions -->
<div> <!-- start type IAVPlayerViewControllerAnimationCoordinator -->
<h3>New Type AVKit.IAVPlayerViewControllerAnimationCoordinator</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVPlayerViewControllerAnimationCoordinator : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedAnimations (System.Action animations, System.Action&lt;bool&gt; completion);</span>
}
</pre>
</div> <!-- end type IAVPlayerViewControllerAnimationCoordinator -->
<div> <!-- start type IAVRoutePickerViewDelegate -->
<h3>New Type AVKit.IAVRoutePickerViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IAVRoutePickerViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IAVRoutePickerViewDelegate -->

</div> <!-- end namespace AVKit -->
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
<!-- start type AudioFileType --> <div>
<h3>Type Changed: AudioToolbox.AudioFileType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">FLAC = 1718378851,</span>
	<span class='added added-field ' data-is-non-breaking="">RF64 = 1380333108,</span>
</pre>
</div>

</div> <!-- end type AudioFileType -->
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
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MidiOutputBufferSizeHint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUMidiOutputEventBlock MidiOutputEventBlock { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] MidiOutputNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ProvidesUserInterface { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ShortName { get; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUAudioUnitBus --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnitBus</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldAllocateBuffer { get; set; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnitBus -->
<!-- start type AUAudioUnit_AUAudioInputOutputUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit_AUAudioInputOutputUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsRunning (AUAudioUnit This);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit_AUAudioInputOutputUnit -->
<!-- start type AUSpatializationAlgorithm --> <div>
<h3>Type Changed: AudioUnit.AUSpatializationAlgorithm</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">HrtfHQ = 6,</span>
</pre>
</div>

</div> <!-- end type AUSpatializationAlgorithm -->
<!-- start type AudioComponent --> <div>
<h3>Type Changed: AudioUnit.AudioComponent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public AudioComponentInfo[] ComponentList { get; set; }</span>
</pre>
</div>

</div> <!-- end type AudioComponent -->
<!-- start type AudioUnit --> <div>
<h3>Type Changed: AudioUnit.AudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AudioUnitStatus ScheduleParameter (AudioUnitParameterEvent inParameterEvent, uint inNumParamEvents);</span>
</pre>
</div>

</div> <!-- end type AudioUnit -->
<!-- start type AudioUnitStatus --> <div>
<h3>Type Changed: AudioUnit.AudioUnitStatus</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExtensionNotFound = -66744,</span>
	<span class='added added-field ' data-is-non-breaking="">MidiOutputBufferFull = -66753,</span>
</pre>
</div>

</div> <!-- end type AudioUnitStatus -->
<div> <!-- start type AUMidiOutputEventBlock -->
<h3>New Type AudioUnit.AUMidiOutputEventBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUMidiOutputEventBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUMidiOutputEventBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (long eventSampleTime, byte cable, nint length, IntPtr midiBytes, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int Invoke (long eventSampleTime, byte cable, nint length, IntPtr midiBytes);</span>
}
</pre>
</div> <!-- end type AUMidiOutputEventBlock -->
<div> <!-- start type AUParameterEventType -->
<h3>New Type AudioUnit.AUParameterEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AUParameterEventType {
	<span class='added added-field ' data-is-non-breaking="">Immediate = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Ramped = 2,</span>
}
</pre>
</div> <!-- end type AUParameterEventType -->
<div> <!-- start type AudioComponentInfo -->
<h3>New Type AudioUnit.AudioComponentInfo</h3>
<pre class='added' data-is-non-breaking="">
public class AudioComponentInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AudioComponentInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AudioComponentInfo (Foundation.NSDictionary dic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string FactoryFunction { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Manufacturer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ResourceUsageInfo ResourceUsage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? SandboxSafe { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Subtype { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] Tags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public uint? Version { get; set; }</span>
}
</pre>
</div> <!-- end type AudioComponentInfo -->
<div> <!-- start type AudioUnitParameterEvent -->
<h3>New Type AudioUnit.AudioUnitParameterEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AudioUnitParameterEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public uint Element;</span>
	<span class='added added-field ' data-is-non-breaking="">public AUParameterEventType EventType;</span>
	<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct EventValues;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Parameter;</span>
	<span class='added added-field ' data-is-non-breaking="">public uint Scope;</span>

	// inner types
	public struct EventValuesStruct {
		// fields
		<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct.ImmediateStruct Immediate;</span>
		<span class='added added-field ' data-is-non-breaking="">public AudioUnitParameterEvent.EventValuesStruct.RampStruct Ramp;</span>

		// inner types
		public struct ImmediateStruct {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public uint BufferOffset;</span>
			<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
		}
		public struct RampStruct {
			// fields
			<span class='added added-field ' data-is-non-breaking="">public uint DurationInFrames;</span>
			<span class='added added-field ' data-is-non-breaking="">public float EndValue;</span>
			<span class='added added-field ' data-is-non-breaking="">public int StartBufferOffset;</span>
			<span class='added added-field ' data-is-non-breaking="">public float StartValue;</span>
		}
	}
}
</pre>
</div> <!-- end type AudioUnitParameterEvent -->
<div> <!-- start type ResourceUsageInfo -->
<h3>New Type AudioUnit.ResourceUsageInfo</h3>
<pre class='added' data-is-non-breaking="">
public class ResourceUsageInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ResourceUsageInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ResourceUsageInfo (Foundation.NSDictionary dic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string[] IOKitUserClient { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] MachLookUpGlobalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? NetworkClient { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? TemporaryExceptionReadWrite { get; set; }</span>
}
</pre>
</div> <!-- end type ResourceUsageInfo -->

</div> <!-- end namespace AudioUnit -->
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
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimation -->
<!-- start type CAAnimationGroup --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationGroup</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAAnimationGroup -->
<!-- start type CABasicAnimation --> <div>
<h3>Type Changed: CoreAnimation.CABasicAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CABasicAnimation -->
<!-- start type CAEAGLLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEAGLLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEAGLLayer -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CAEmitterCell --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterCell</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterCell -->
<!-- start type CAEmitterLayer --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAEmitterLayer -->
<!-- start type CAGradientLayer --> <div>
<h3>Type Changed: CoreAnimation.CAGradientLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAGradientLayer -->
<!-- start type CAKeyFrameAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAKeyFrameAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAKeyFrameAnimation -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CACornerMask MaskedCorners { get; set; }</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CAMediaTimingFunction --> <div>
<h3>Type Changed: CoreAnimation.CAMediaTimingFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAMediaTimingFunction -->
<!-- start type CAMetalLayer --> <div>
<h3>Type Changed: CoreAnimation.CAMetalLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsNextDrawableTimeout { get; set; }</span>
</pre>
</div>

</div> <!-- end type CAMetalLayer -->
<!-- start type CAPropertyAnimation --> <div>
<h3>Type Changed: CoreAnimation.CAPropertyAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAPropertyAnimation -->
<!-- start type CAReplicatorLayer --> <div>
<h3>Type Changed: CoreAnimation.CAReplicatorLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAReplicatorLayer -->
<!-- start type CAScrollLayer --> <div>
<h3>Type Changed: CoreAnimation.CAScrollLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAScrollLayer -->
<!-- start type CAShapeLayer --> <div>
<h3>Type Changed: CoreAnimation.CAShapeLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAShapeLayer -->
<!-- start type CASpringAnimation --> <div>
<h3>Type Changed: CoreAnimation.CASpringAnimation</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CASpringAnimation -->
<!-- start type CATextLayer --> <div>
<h3>Type Changed: CoreAnimation.CATextLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATextLayer -->
<!-- start type CATiledLayer --> <div>
<h3>Type Changed: CoreAnimation.CATiledLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATiledLayer -->
<!-- start type CATransformLayer --> <div>
<h3>Type Changed: CoreAnimation.CATransformLayer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransformLayer -->
<!-- start type CATransition --> <div>
<h3>Type Changed: CoreAnimation.CATransition</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CATransition -->
<!-- start type CAValueFunction --> <div>
<h3>Type Changed: CoreAnimation.CAValueFunction</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type CAValueFunction -->
<div> <!-- start type CACornerMask -->
<h3>New Type CoreAnimation.CACornerMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum CACornerMask {
	<span class='added added-field ' data-is-non-breaking="">MaxXMaxYCorner = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">MaxXMinYCorner = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMaxYCorner = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">MinXMinYCorner = 1,</span>
}
</pre>
</div> <!-- end type CACornerMask -->

</div> <!-- end namespace CoreAnimation -->
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
<p>Added property:</p>
<pre>
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
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIImageAccumulator --> <div>
<h3>Type Changed: CoreImage.CIImageAccumulator</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("The default initializer does not work in recent iOS version (11b4).")]
	public CIImageAccumulator ();</span>
</div></pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect rectangle, CIFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageAccumulator (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect rect, CIFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIImageAccumulator FromRectangle (CoreGraphics.CGRect extent, CIFormat format, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIImageAccumulator -->
<!-- start type CIQRCodeFeature --> <div>
<h3>Type Changed: CoreImage.CIQRCodeFeature</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIQRCodeFeature (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type CIQRCodeFeature -->
<div> <!-- start type CIAreaMinMaxRed -->
<h3>New Type CoreImage.CIAreaMinMaxRed</h3>
<pre class='added' data-is-non-breaking="">
public class CIAreaMinMaxRed : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAreaMinMaxRed (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAreaMinMaxRed (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAreaMinMaxRed -->
<div> <!-- start type CIAttributedTextImageGenerator -->
<h3>New Type CoreImage.CIAttributedTextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIAttributedTextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIAttributedTextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIAttributedTextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIAttributedTextImageGenerator -->
<div> <!-- start type CIBarcodeDescriptor -->
<h3>New Type CoreImage.CIBarcodeDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public abstract class CIBarcodeDescriptor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CIBarcodeDescriptor -->
<div> <!-- start type CIBarcodeGenerator -->
<h3>New Type CoreImage.CIBarcodeGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CIBarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBarcodeGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBarcodeGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBarcodeGenerator -->
<div> <!-- start type CIBicubicScaleTransform -->
<h3>New Type CoreImage.CIBicubicScaleTransform</h3>
<pre class='added' data-is-non-breaking="">
public class CIBicubicScaleTransform : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBicubicScaleTransform (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBicubicScaleTransform (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBicubicScaleTransform -->
<div> <!-- start type CIBlendWithBlueMask -->
<h3>New Type CoreImage.CIBlendWithBlueMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithBlueMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithBlueMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithBlueMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithBlueMask -->
<div> <!-- start type CIBlendWithRedMask -->
<h3>New Type CoreImage.CIBlendWithRedMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIBlendWithRedMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBlendWithRedMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBlendWithRedMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBlendWithRedMask -->
<div> <!-- start type CIBokehBlur -->
<h3>New Type CoreImage.CIBokehBlur</h3>
<pre class='added' data-is-non-breaking="">
public class CIBokehBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIBokehBlur (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIBokehBlur (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIBokehBlur -->
<div> <!-- start type CIColorCubesMixedWithMask -->
<h3>New Type CoreImage.CIColorCubesMixedWithMask</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCubesMixedWithMask : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCubesMixedWithMask (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCubesMixedWithMask (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCubesMixedWithMask -->
<div> <!-- start type CIColorCurves -->
<h3>New Type CoreImage.CIColorCurves</h3>
<pre class='added' data-is-non-breaking="">
public class CIColorCurves : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColorCurves (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIColorCurves (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIColorCurves -->
<div> <!-- start type CIDepthBlurEffect -->
<h3>New Type CoreImage.CIDepthBlurEffect</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthBlurEffect : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthBlurEffect (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthBlurEffect (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthBlurEffect -->
<div> <!-- start type CIDepthToDisparity -->
<h3>New Type CoreImage.CIDepthToDisparity</h3>
<pre class='added' data-is-non-breaking="">
public class CIDepthToDisparity : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDepthToDisparity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDepthToDisparity (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDepthToDisparity -->
<div> <!-- start type CIDisparityToDepth -->
<h3>New Type CoreImage.CIDisparityToDepth</h3>
<pre class='added' data-is-non-breaking="">
public class CIDisparityToDepth : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIDisparityToDepth (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIDisparityToDepth (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIDisparityToDepth -->
<div> <!-- start type CIEdgePreserveUpsampleFilter -->
<h3>New Type CoreImage.CIEdgePreserveUpsampleFilter</h3>
<pre class='added' data-is-non-breaking="">
public class CIEdgePreserveUpsampleFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIEdgePreserveUpsampleFilter (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIEdgePreserveUpsampleFilter (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIEdgePreserveUpsampleFilter -->
<div> <!-- start type CILabDeltaE -->
<h3>New Type CoreImage.CILabDeltaE</h3>
<pre class='added' data-is-non-breaking="">
public class CILabDeltaE : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CILabDeltaE (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CILabDeltaE (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CILabDeltaE -->
<div> <!-- start type CIMorphologyGradient -->
<h3>New Type CoreImage.CIMorphologyGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyGradient (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyGradient -->
<div> <!-- start type CIMorphologyMaximum -->
<h3>New Type CoreImage.CIMorphologyMaximum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMaximum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMaximum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMaximum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMaximum -->
<div> <!-- start type CIMorphologyMinimum -->
<h3>New Type CoreImage.CIMorphologyMinimum</h3>
<pre class='added' data-is-non-breaking="">
public class CIMorphologyMinimum : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIMorphologyMinimum (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIMorphologyMinimum (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIMorphologyMinimum -->
<div> <!-- start type CITextImageGenerator -->
<h3>New Type CoreImage.CITextImageGenerator</h3>
<pre class='added' data-is-non-breaking="">
public class CITextImageGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CITextImageGenerator (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CITextImageGenerator (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CITextImageGenerator -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLGeocoder --> <div>
<h3>Type Changed: CoreLocation.CLGeocoder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GeocodeAddress (string addressString, CLRegion region, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region, Foundation.NSLocale locale);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReverseGeocodeLocation (CLLocation location, Foundation.NSLocale locale, CLGeocodeCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location, Foundation.NSLocale locale);</span>
</pre>
</div>

</div> <!-- end type CLGeocoder -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMAttachmentBearer --> <div>
<h3>Type Changed: CoreMedia.CMAttachmentBearer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVBuffer --> <div>
<h3>Type Changed: CoreVideo.CVBuffer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSDictionary&lt;TKey,TValue&gt; GetAttachments&lt;TKey, TValue&gt; (CVAttachmentMode attachmentMode);</span>
</pre>
</div>

</div> <!-- end type CVBuffer -->

</div> <!-- end namespace CoreVideo -->
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
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">[Obsolete ("Not intended to be directly instantiated, this is an abstract class.")]
	public NSDimension ();</span>
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
<!-- start type NSUrlSessionTask --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTask</h3>
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
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKAnnotationView --> <div>
<h3>Type Changed: MapKit.MKAnnotationView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationView ClusterAnnotationView { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ClusteringIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKAnnotationViewCollisionMode CollisionMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float DisplayPriority { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareForDisplay ();</span>
</pre>
</div>

</div> <!-- end type MKAnnotationView -->
<!-- start type MKMapItem --> <div>
<h3>Type Changed: MapKit.MKMapItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MKMapItem -->
<!-- start type MKMapType --> <div>
<h3>Type Changed: MapKit.MKMapType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">MutedStandard = 5,</span>
</pre>
</div>

</div> <!-- end type MKMapType -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MKCreateClusterAnnotation CreateClusterAnnotation { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKAnnotationView DequeueReusableAnnotation (string identifier, IMKAnnotation annotation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Register (ObjCRuntime.Class viewClass, string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Register (System.Type viewType, string identifier);</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKMapViewDelegate --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation CreateClusterAnnotation (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate -->
<!-- start type MKMapViewDelegate_Extensions --> <div>
<h3>Type Changed: MapKit.MKMapViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MKClusterAnnotation CreateClusterAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
</pre>
</div>

</div> <!-- end type MKMapViewDelegate_Extensions -->
<div> <!-- start type MKAnnotationViewCollisionMode -->
<h3>New Type MapKit.MKAnnotationViewCollisionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKAnnotationViewCollisionMode {
	<span class='added added-field ' data-is-non-breaking="">Circle = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Rectangle = 0,</span>
}
</pre>
</div> <!-- end type MKAnnotationViewCollisionMode -->
<div> <!-- start type MKClusterAnnotation -->
<h3>New Type MapKit.MKClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public class MKClusterAnnotation : Foundation.NSObject, Foundation.INSObjectProtocol, IMKAnnotation, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKClusterAnnotation (IMKAnnotation[] memberAnnotations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKClusterAnnotation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IMKAnnotation[] MemberAnnotations { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Subtitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);</span>
}
</pre>
</div> <!-- end type MKClusterAnnotation -->
<div> <!-- start type MKCreateClusterAnnotation -->
<h3>New Type MapKit.MKCreateClusterAnnotation</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MKCreateClusterAnnotation : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKCreateClusterAnnotation (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation[] memberAnnotations, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MKClusterAnnotation Invoke (MKMapView mapView, IMKAnnotation[] memberAnnotations);</span>
}
</pre>
</div> <!-- end type MKCreateClusterAnnotation -->
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
<div> <!-- start type MKFeatureVisibility -->
<h3>New Type MapKit.MKFeatureVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKFeatureVisibility {
	<span class='added added-field ' data-is-non-breaking="">Adaptive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hidden = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Visible = 2,</span>
}
</pre>
</div> <!-- end type MKFeatureVisibility -->
<div> <!-- start type MKMapViewDefault -->
<h3>New Type MapKit.MKMapViewDefault</h3>
<pre class='added' data-is-non-breaking="">
public static class MKMapViewDefault {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnnotationViewReuseIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ClusterAnnotationViewReuseIdentifier { get; }</span>
}
</pre>
</div> <!-- end type MKMapViewDefault -->
<div> <!-- start type MKMarkerAnnotationView -->
<h3>New Type MapKit.MKMarkerAnnotationView</h3>
<pre class='added' data-is-non-breaking="">
public class MKMarkerAnnotationView : MapKit.MKAnnotationView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MKMarkerAnnotationView (IMKAnnotation annotation, string reuseIdentifier);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AnimatesWhenAdded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility SubtitleVisibility { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility TitleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKMarkerAnnotationView.MKMarkerAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKMarkerAnnotationViewAppearance : MapKit.MKAnnotationView+MKAnnotationViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKMarkerAnnotationView (IntPtr handle);</span>
		// properties
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage GlyphImage { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual string GlyphText { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor GlyphTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor MarkerTintColor { get; set; }</span>
		<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage SelectedGlyphImage { get; set; }</span>
	}
}
</pre>
</div> <!-- end type MKMarkerAnnotationView -->
<div> <!-- start type MKScaleView -->
<h3>New Type MapKit.MKScaleView</h3>
<pre class='added' data-is-non-breaking="">
public class MKScaleView : UIKit.UIView, CoreAnimation.ICALayerDelegate, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKScaleView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKScaleViewAlignment LegendAlignment { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKMapView MapView { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MKFeatureVisibility ScaleVisibility { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView FromMapView (MKMapView mapView);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MKScaleView.MKScaleViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class MKScaleViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected MKScaleView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type MKScaleView -->
<div> <!-- start type MKScaleViewAlignment -->
<h3>New Type MapKit.MKScaleViewAlignment</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MKScaleViewAlignment {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type MKScaleViewAlignment -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfo NowPlaying { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyServiceIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<!-- start type MPRemoteCommandHandlerStatus --> <div>
<h3>Type Changed: MediaPlayer.MPRemoteCommandHandlerStatus</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">DeviceNotFound = 120,</span>
</pre>
</div>

</div> <!-- end type MPRemoteCommandHandlerStatus -->
<div> <!-- start type MPMediaItem -->
<h3>New Type MediaPlayer.MPMediaItem</h3>
<pre class='added' data-is-non-breaking="">
public class MPMediaItem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItem (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumArtistPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumArtistProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTrackCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AlbumTrackNumberProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtistPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtistProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ArtworkProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetURLProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BeatsPerMinuteProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString BookmarkTimeProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CommentsProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ComposerPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ComposerProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DateAddedProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DiscCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DiscNumberProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GenrePersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GenreProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HasProtectedAssetProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsCloudItemProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsCompilationProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsExplicitProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LastPlayedDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LyricsProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MediaTypeProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlayCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackDurationProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PlaybackStoreIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PodcastPersistentIDProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PodcastTitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPersistentID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RatingProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ReleaseDateProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SkipCountProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TitleProperty { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserGroupingProperty { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool CanFilterByProperty (Foundation.NSString property);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject GetObject (Foundation.NSObject key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);</span>
}
</pre>
</div> <!-- end type MPMediaItem -->
<div> <!-- start type MPMediaItemEnumerator -->
<h3>New Type MediaPlayer.MPMediaItemEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MPMediaItemEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string property, Foundation.NSObject value, bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string property, Foundation.NSObject value, bool stop);</span>
}
</pre>
</div> <!-- end type MPMediaItemEnumerator -->
<div> <!-- start type MPNowPlayingInfo -->
<h3>New Type MediaPlayer.MPNowPlayingInfo</h3>
<pre class='added' data-is-non-breaking="">
public class MPNowPlayingInfo {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MPNowPlayingInfo ();</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public string AlbumTitle;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? AlbumTrackCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? AlbumTrackNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Artist;</span>
	<span class='added added-field ' data-is-non-breaking="">public MPMediaItemArtwork Artwork;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? ChapterCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? ChapterNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Composer;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? DefaultPlaybackRate;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? DiscCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? DiscNumber;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? ElapsedPlaybackTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Genre;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong? PersistentID;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? PlaybackDuration;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? PlaybackQueueCount;</span>
	<span class='added added-field ' data-is-non-breaking="">public int? PlaybackQueueIndex;</span>
	<span class='added added-field ' data-is-non-breaking="">public double? PlaybackRate;</span>
	<span class='added added-field ' data-is-non-breaking="">public string Title;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl AssetUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOptionGroup[] AvailableLanguageOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string CollectionIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoLanguageOption[] CurrentLanguageOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExternalContentIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string ExternalUserProfileIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IsLiveStream { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MPNowPlayingInfoMediaType? MediaType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? PlaybackProgress { get; set; }</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfo -->
<div> <!-- start type NSUserActivity_MediaPlayerAdditions -->
<h3>New Type MediaPlayer.NSUserActivity_MediaPlayerAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_MediaPlayerAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetExternalMediaContentIdentifier (Foundation.NSUserActivity This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetExternalMediaContentIdentifier (Foundation.NSUserActivity This, Foundation.NSString identifier);</span>
}
</pre>
</div> <!-- end type NSUserActivity_MediaPlayerAdditions -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<!-- start type MPSBinaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSBinaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSBinaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSBinaryImageKernel -->
<!-- start type MPSCnnConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnConvolution -->
<!-- start type MPSCnnConvolutionDescriptor --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolutionDescriptor (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSCnnConvolutionDescriptor -->
<!-- start type MPSCnnCrossChannelNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnCrossChannelNormalization -->
<!-- start type MPSCnnFullyConnected --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnFullyConnected -->
<!-- start type MPSCnnKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnKernel -->
<!-- start type MPSCnnLocalContrastNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLocalContrastNormalization -->
<!-- start type MPSCnnLogSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnLogSoftMax -->
<!-- start type MPSCnnNeuron --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuron</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuron -->
<!-- start type MPSCnnNeuronAbsolute --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronAbsolute -->
<!-- start type MPSCnnNeuronLinear --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronLinear -->
<!-- start type MPSCnnNeuronReLU --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronReLU -->
<!-- start type MPSCnnNeuronSigmoid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronSigmoid -->
<!-- start type MPSCnnNeuronTanH --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnNeuronTanH -->
<!-- start type MPSCnnPooling --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPooling</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPooling -->
<!-- start type MPSCnnPoolingAverage --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingAverage -->
<!-- start type MPSCnnPoolingMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnPoolingMax -->
<!-- start type MPSCnnSoftMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSoftMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSoftMax -->
<!-- start type MPSCnnSpatialNormalization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSCnnSpatialNormalization -->
<!-- start type MPSImageAreaMax --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMax</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMax (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMax -->
<!-- start type MPSImageAreaMin --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageAreaMin</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageAreaMin (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageAreaMin -->
<!-- start type MPSImageBox --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageBox</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageBox (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageBox -->
<!-- start type MPSImageConversion --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConversion</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConversion -->
<!-- start type MPSImageConvolution --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageConvolution</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConvolution (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageConvolution -->
<!-- start type MPSImageDilate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageDilate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageDilate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageDilate -->
<!-- start type MPSImageErode --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageErode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageErode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageErode -->
<!-- start type MPSImageGaussianBlur --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianBlur</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianBlur (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianBlur -->
<!-- start type MPSImageGaussianPyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageGaussianPyramid -->
<!-- start type MPSImageHistogram --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogram</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogram (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogram -->
<!-- start type MPSImageHistogramEqualization --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramEqualization</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramEqualization (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramEqualization -->
<!-- start type MPSImageHistogramSpecification --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageHistogramSpecification</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageHistogramSpecification (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageHistogramSpecification -->
<!-- start type MPSImageIntegral --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegral</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegral (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegral -->
<!-- start type MPSImageIntegralOfSquares --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageIntegralOfSquares</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageIntegralOfSquares (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageIntegralOfSquares -->
<!-- start type MPSImageLanczosScale --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLanczosScale</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLanczosScale (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLanczosScale -->
<!-- start type MPSImageLaplacian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageLaplacian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageLaplacian -->
<!-- start type MPSImageMedian --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageMedian</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageMedian (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageMedian -->
<!-- start type MPSImagePyramid --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImagePyramid</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImagePyramid -->
<!-- start type MPSImageSobel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageSobel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageSobel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageSobel -->
<!-- start type MPSImageTent --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTent -->
<!-- start type MPSImageThresholdBinary --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinary</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinary (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinary -->
<!-- start type MPSImageThresholdBinaryInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdBinaryInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdBinaryInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdBinaryInverse -->
<!-- start type MPSImageThresholdToZero --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZero</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZero (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZero -->
<!-- start type MPSImageThresholdToZeroInverse --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdToZeroInverse</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdToZeroInverse (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdToZeroInverse -->
<!-- start type MPSImageThresholdTruncate --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageThresholdTruncate</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageThresholdTruncate (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageThresholdTruncate -->
<!-- start type MPSImageTranspose --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSImageTranspose</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageTranspose (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSImageTranspose -->
<!-- start type MPSKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSKernel (Foundation.NSCoder coder);</span>
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

</div> <!-- end type MPSKernel -->
<!-- start type MPSMatrixMultiplication --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSMatrixMultiplication -->
<!-- start type MPSUnaryImageKernel --> <div>
<h3>Type Changed: MetalPerformanceShaders.MPSUnaryImageKernel</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSUnaryImageKernel (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type MPSUnaryImageKernel -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"10.2"</span> <span class='added '>"11.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"10.12.0"</span> <span class='added '>"10.99.5"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string CoreMLLibrary = "/System/Library/Frameworks/CoreML.framework/CoreML";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string DeviceCheckLibrary = "/System/Library/Frameworks/DeviceCheck.framework/DeviceCheck";</span>
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
<!-- start namespace Photos --> <div> 
<h2>Namespace Photos</h2>
<!-- start type PHAsset --> <div>
<h3>Type Changed: Photos.PHAsset</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHAsset -->
<!-- start type PHAssetCollectionSubtype --> <div>
<h3>Type Changed: Photos.PHAssetCollectionSubtype</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAnimated = 214,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumLongExposures = 215,</span>
</pre>
</div>

</div> <!-- end type PHAssetCollectionSubtype -->
<!-- start type PHContentEditingInput --> <div>
<h3>Type Changed: Photos.PHContentEditingInput</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetPlaybackStyle PlaybackStyle { get; }</span>
</pre>
</div>

</div> <!-- end type PHContentEditingInput -->
<!-- start type PHLivePhotoEditingContext --> <div>
<h3>Type Changed: Photos.PHLivePhotoEditingContext</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, PHLivePhotoEditingOption options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SaveLivePhoto (PHContentEditingOutput output, PHLivePhotoEditingOption options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, PHLivePhotoEditingOption options);</span>
</pre>
</div>

</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type PHAssetPlaybackStyle -->
<h3>New Type Photos.PHAssetPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageAnimated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LivePhoto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoLooping = 5,</span>
}
</pre>
</div> <!-- end type PHAssetPlaybackStyle -->
<div> <!-- start type PHLivePhotoEditingOption -->
<h3>New Type Photos.PHLivePhotoEditingOption</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingOption : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingOption (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? ShouldRenderAtPlaybackTime { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingOption -->

</div> <!-- end namespace Photos -->
<!-- start namespace ReplayKit --> <div> 
<h2>Namespace ReplayKit</h2>
<!-- start type NSExtensionContext_RPBroadcastExtension --> <div>
<h3>Type Changed: ReplayKit.NSExtensionContext_RPBroadcastExtension</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void CompleteRequest (Foundation.NSExtensionContext This, Foundation.NSUrl broadcastURL, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.INSCoding&gt; setupInfo);</span>
</pre>
</div>

</div> <!-- end type NSExtensionContext_RPBroadcastExtension -->
<!-- start type RPBroadcastControllerDelegate --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastControllerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateBroadcastUrl (RPBroadcastController broadcastController, Foundation.NSUrl broadcastUrl);</span>
</pre>
</div>

</div> <!-- end type RPBroadcastControllerDelegate -->
<!-- start type RPBroadcastControllerDelegate_Extensions --> <div>
<h3>Type Changed: ReplayKit.RPBroadcastControllerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateBroadcastUrl (IRPBroadcastControllerDelegate This, RPBroadcastController broadcastController, Foundation.NSUrl broadcastUrl);</span>
</pre>
</div>

</div> <!-- end type RPBroadcastControllerDelegate_Extensions -->
<!-- start type RPRecordingError --> <div>
<h3>Type Changed: ReplayKit.RPRecordingError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ActivePhoneCall = -5811,</span>
	<span class='added added-field ' data-is-non-breaking="">CarPlay = -5813,</span>
	<span class='added added-field ' data-is-non-breaking="">Entitlements = -5810,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedToSave = -5812,</span>
</pre>
</div>

</div> <!-- end type RPRecordingError -->
<!-- start type RPScreenRecorder --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorder</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCapture (System.Action&lt;CoreMedia.CMSampleBuffer,ReplayKit.RPSampleBufferType,Foundation.NSError&gt; captureHandler, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StartCaptureAsync (System.Action&lt;CoreMedia.CMSampleBuffer,ReplayKit.RPSampleBufferType,Foundation.NSError&gt; captureHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopCapture (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StopCaptureAsync ();</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorder -->
<!-- start type RPScreenRecorderDelegate --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorderDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStopRecording (RPScreenRecorder screenRecorder, RPPreviewViewController previewViewController, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorderDelegate -->
<!-- start type RPScreenRecorderDelegate_Extensions --> <div>
<h3>Type Changed: ReplayKit.RPScreenRecorderDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStopRecording (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder, RPPreviewViewController previewViewController, Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type RPScreenRecorderDelegate_Extensions -->

</div> <!-- end namespace ReplayKit -->
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
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKNodeFocusBehavior FocusBehavior { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIKit.UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<div> <!-- start type SKNodeFocusBehavior -->
<h3>New Type SpriteKit.SKNodeFocusBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKNodeFocusBehavior {
	<span class='added added-field ' data-is-non-breaking="">Focusable = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occluding = 1,</span>
}
</pre>
</div> <!-- end type SKNodeFocusBehavior -->
<div> <!-- start type SKRenderer -->
<h3>New Type SpriteKit.SKRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class SKRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKRenderer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IgnoresSiblingOrder { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKScene Scene { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldCullNonVisibleNodes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsDrawCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsFields { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsNodeCount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsPhysics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsQuadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKRenderer FromDevice (Metal.IMTLDevice device);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLCommandBuffer commandBuffer, Metal.MTLRenderPassDescriptor renderPassDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Render (CoreGraphics.CGRect viewport, Metal.IMTLRenderCommandEncoder renderCommandEncoder, Metal.MTLRenderPassDescriptor renderPassDescriptor, Metal.IMTLCommandQueue commandQueue);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (double currentTime);</span>
}
</pre>
</div> <!-- end type SKRenderer -->
<div> <!-- start type SKTransformNode -->
<h3>New Type SpriteKit.SKTransformNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTransformNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTransformNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTransformNode (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 EulerAngles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Quaternion Quaternion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 RotationMatrix { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat XRotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat YRotation { get; set; }</span>
}
</pre>
</div> <!-- end type SKTransformNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace StoreKit --> <div> 
<h2>Namespace StoreKit</h2>
<!-- start type SKCloudServiceController --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StorefrontCountryCodeDidChangeNotification { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestStorefrontCountryCode (System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestStorefrontCountryCodeAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestUserToken (string developerToken, System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestUserTokenAsync (string developerToken);</span>
</pre>
</div>
<!-- start type SKCloudServiceController.Notifications --> <div>
<h3>Type Changed: StoreKit.SKCloudServiceController.Notifications</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveStorefrontCountryCodeDidChange (Foundation.NSObject objectToObserve, System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type SKCloudServiceController.Notifications -->

</div> <!-- end type SKCloudServiceController -->
<!-- start type SKPaymentTransactionObserver --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAddStorePayment (SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver -->
<!-- start type SKPaymentTransactionObserver_Extensions --> <div>
<h3>Type Changed: StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAddStorePayment (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKPayment payment, SKProduct product);</span>
</pre>
</div>

</div> <!-- end type SKPaymentTransactionObserver_Extensions -->
<!-- start type SKStoreProductParameterKey --> <div>
<h3>Type Changed: StoreKit.SKStoreProductParameterKey</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ProductIdentifier { get; }</span>
</pre>
</div>

</div> <!-- end type SKStoreProductParameterKey -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifier -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKCloudServiceSetupMessageIdentifier {
	<span class='added added-field ' data-is-non-breaking="">AddMusic = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connect = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Join = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PlayMusic = 3,</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifier -->
<div> <!-- start type SKCloudServiceSetupMessageIdentifierExtensions -->
<h3>New Type StoreKit.SKCloudServiceSetupMessageIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKCloudServiceSetupMessageIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (SKCloudServiceSetupMessageIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKCloudServiceSetupMessageIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type SKCloudServiceSetupMessageIdentifierExtensions -->
<div> <!-- start type SKProductStorePromotionController -->
<h3>New Type StoreKit.SKProductStorePromotionController</h3>
<pre class='added' data-is-non-breaking="">
public class SKProductStorePromotionController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKProductStorePromotionController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static SKProductStorePromotionController Default { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionOrder (System.Action&lt;SKProduct[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProduct[]&gt; FetchStorePromotionOrderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchStorePromotionVisibility (SKProduct product, System.Action&lt;SKProductStorePromotionVisibility,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;SKProductStorePromotionVisibility&gt; FetchStorePromotionVisibilityAsync (SKProduct product);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProduct[] storePromotionOrder, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SKProductStorePromotionVisibility promotionVisibility, SKProduct product, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProduct[] storePromotionOrder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task UpdateAsync (SKProductStorePromotionVisibility promotionVisibility, SKProduct product);</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionController -->
<div> <!-- start type SKProductStorePromotionVisibility -->
<h3>New Type StoreKit.SKProductStorePromotionVisibility</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKProductStorePromotionVisibility {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Hide = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Show = 1,</span>
}
</pre>
</div> <!-- end type SKProductStorePromotionVisibility -->

</div> <!-- end namespace StoreKit -->
<!-- start namespace TVMLKit --> <div> 
<h2>Namespace TVMLKit</h2>
<!-- start type TVElementAlignment --> <div>
<h3>Type Changed: TVMLKit.TVElementAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type TVElementAlignment -->
<!-- start type TVElementPosition --> <div>
<h3>Type Changed: TVMLKit.TVElementPosition</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BottomLeading = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">BottomTrailing = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">Leading = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeading = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">TopTrailing = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 13,</span>
</pre>
</div>

</div> <!-- end type TVElementPosition -->

</div> <!-- end namespace TVMLKit -->
<!-- start namespace TVServices --> <div> 
<h2>Namespace TVServices</h2>
<!-- start type TVContentItem --> <div>
<h3>Type Changed: TVServices.TVContentItem</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl GetImageUrl (TVContentItemImageTrait traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetImageUrl (Foundation.NSUrl aUrl, TVContentItemImageTrait traits);</span>
</pre>
</div>

</div> <!-- end type TVContentItem -->
<div> <!-- start type TVContentItemImageTrait -->
<h3>New Type TVServices.TVContentItemImageTrait</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum TVContentItemImageTrait {
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleDark = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">UserInterfaceStyleLight = 256,</span>
}
</pre>
</div> <!-- end type TVContentItemImageTrait -->

</div> <!-- end namespace TVServices -->
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
<!-- start type NSLayoutFormatOptions --> <div>
<h3>Type Changed: UIKit.NSLayoutFormatOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">SpacingBaselineToBaseline = 524288,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingEdgeToEdge = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SpacingMask = 524288,</span>
</pre>
</div>

</div> <!-- end type NSLayoutFormatOptions -->
<!-- start type UIBezierPath --> <div>
<h3>Type Changed: UIKit.UIBezierPath</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type UIBezierPath -->
<!-- start type UIButtonType --> <div>
<h3>Type Changed: UIKit.UIButtonType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Plain = 6,</span>
</pre>
</div>

</div> <!-- end type UIButtonType -->
<!-- start type UICollectionView --> <div>
<h3>Type Changed: UIKit.UICollectionView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UICollectionView -->
<!-- start type UICollectionViewFlowLayout --> <div>
<h3>Type Changed: UIKit.UICollectionViewFlowLayout</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICollectionViewFlowLayoutSectionInsetReference SectionInsetReference { get; set; }</span>
</pre>
</div>

</div> <!-- end type UICollectionViewFlowLayout -->
<!-- start type UICollectionViewFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UICollectionViewFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UICollectionViewFocusUpdateContext ();</span>
</div></pre>

</div> <!-- end type UICollectionViewFocusUpdateContext -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromName (string name, Foundation.NSBundle inBundle, UITraitCollection compatibleWithTraitCollection);</span>
</pre>
</div>

</div> <!-- end type UIColor -->
<!-- start type UIControlContentHorizontalAlignment --> <div>
<h3>Type Changed: UIKit.UIControlContentHorizontalAlignment</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Leading = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 5,</span>
</pre>
</div>

</div> <!-- end type UIControlContentHorizontalAlignment -->
<!-- start type UIFocusAnimationCoordinator --> <div>
<h3>Type Changed: UIKit.UIFocusAnimationCoordinator</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedFocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedFocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCoordinatedUnfocusingAnimations (System.Action&lt;IUIFocusAnimationContext&gt; animations, System.Action completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddCoordinatedUnfocusingAnimationsAsync (System.Action&lt;IUIFocusAnimationContext&gt; animations);</span>
</pre>
</div>

</div> <!-- end type UIFocusAnimationCoordinator -->
<!-- start type UIFocusEnvironment_Extensions --> <div>
<h3>Type Changed: UIKit.UIFocusEnvironment_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetSoundIdentifier (IUIFocusEnvironment This, UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type UIFocusEnvironment_Extensions -->
<!-- start type UIFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UIFocusUpdateContext</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("This cannot be directly created.")]
	public UIFocusUpdateContext ();</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AnimationCoordinatorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidUpdateNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Key { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MovementDidFailNotification { get; }</span>
</pre>
</div>

</div> <!-- end type UIFocusUpdateContext -->
<!-- start type UIFontTextStyle --> <div>
<h3>Type Changed: UIKit.UIFontTextStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">LargeTitle = 10,</span>
</pre>
</div>

</div> <!-- end type UIFontTextStyle -->
<!-- start type UIImageView --> <div>
<h3>Type Changed: UIKit.UIImageView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool MasksFocusEffectToContents { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIView OverlayContentView { get; }</span>
</pre>
</div>

</div> <!-- end type UIImageView -->
<!-- start type UIModalPresentationStyle --> <div>
<h3>Type Changed: UIKit.UIModalPresentationStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">BlurOverFullScreen = 8,</span>
</pre>
</div>

</div> <!-- end type UIModalPresentationStyle -->
<!-- start type UIPresentationController --> <div>
<h3>Type Changed: UIKit.UIPresentationController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
</pre>
</div>

</div> <!-- end type UIPresentationController -->
<!-- start type UIScrollView --> <div>
<h3>Type Changed: UIKit.UIScrollView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets AdjustedContentInset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIScrollViewContentInsetAdjustmentBehavior ContentInsetAdjustmentBehavior { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide ContentLayoutGuide { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide FrameLayoutGuide { get; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidChangeAdjustedContentInset;</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AdjustedContentInsetDidChange ();</span>
</pre>
</div>

</div> <!-- end type UIScrollView -->
<!-- start type UIScrollViewDelegate --> <div>
<h3>Type Changed: UIKit.UIScrollViewDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeAdjustedContentInset (UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewDelegate -->
<!-- start type UIScrollViewDelegate_Extensions --> <div>
<h3>Type Changed: UIKit.UIScrollViewDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeAdjustedContentInset (IUIScrollViewDelegate This, UIScrollView scrollView);</span>
</pre>
</div>

</div> <!-- end type UIScrollViewDelegate_Extensions -->
<!-- start type UISearchBar --> <div>
<h3>Type Changed: UIKit.UISearchBar</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISearchBar -->
<!-- start type UISplitViewController --> <div>
<h3>Type Changed: UIKit.UISplitViewController</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISplitViewControllerPrimaryEdge PrimaryEdge { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISplitViewController -->
<!-- start type UIStackView --> <div>
<h3>Type Changed: UIKit.UIStackView</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual nfloat GetCustomSpacing (UIView arrangedSubview);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCustomSpacing (nfloat spacing, UIView arrangedSubview);</span>
</pre>
</div>

</div> <!-- end type UIStackView -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIDataSourceTranslating</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasUncommittedUpdates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InsetsContentViewsToSafeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITableViewSeparatorInsetReference SeparatorInsetReference { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformBatchUpdates (System.Action updates, System.Action&lt;bool&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; PerformBatchUpdatesAsync (System.Action updates);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
</pre>
</div>

</div> <!-- end type UITableView -->
<!-- start type UITextContentType --> <div>
<h3>Type Changed: UIKit.UITextContentType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Password { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Username { get; }</span>
</pre>
</div>

</div> <!-- end type UITextContentType -->
<!-- start type UITextDocumentProxy --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid DocumentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SelectedText { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy -->
<!-- start type UITextDocumentProxy_Extensions --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUuid GetDocumentIdentifier (IUITextDocumentProxy This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetSelectedText (IUITextDocumentProxy This);</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy_Extensions -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextInputTraits_Extensions --> <div>
<h3>Type Changed: UIKit.UITextInputTraits_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartDashesType GetSmartDashesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartInsertDeleteType GetSmartInsertDeleteType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITextSmartQuotesType GetSmartQuotesType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartDashesType (IUITextInputTraits This, UITextSmartDashesType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartInsertDeleteType (IUITextInputTraits This, UITextSmartInsertDeleteType value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSmartQuotesType (IUITextInputTraits This, UITextSmartQuotesType value);</span>
</pre>
</div>

</div> <!-- end type UITextInputTraits_Extensions -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartDashesType SmartDashesType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartInsertDeleteType SmartInsertDeleteType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextSmartQuotesType SmartQuotesType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDirectionalEdgeInsets DirectionalLayoutMargins { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InsetsLayoutMarginsFromSafeArea { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets SafeAreaInsets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UILayoutGuide SafeAreaLayoutGuide { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SafeAreaInsetsDidChange ();</span>
</pre>
</div>

</div> <!-- end type UIView -->
<!-- start type UIViewController --> <div>
<h3>Type Changed: UIKit.UIViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIEdgeInsets AdditionalSafeAreaInsets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIViewController ChildViewControllerForUserInterfaceStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIUserInterfaceStyle PreferredUserInterfaceStyle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDirectionalEdgeInsets SystemMinimumLayoutMargins { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ViewRespectsSystemMinimumLayoutMargins { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSString GetSoundIdentifier (UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeedsUserInterfaceAppearanceUpdate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ViewLayoutMarginsDidChange ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ViewSafeAreaInsetsDidChange ();</span>
</pre>
</div>

</div> <!-- end type UIViewController -->
<div> <!-- start type IUIDataSourceTranslating -->
<h3>New Type UIKit.IUIDataSourceTranslating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIDataSourceTranslating : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
}
</pre>
</div> <!-- end type IUIDataSourceTranslating -->
<div> <!-- start type IUIFocusAnimationContext -->
<h3>New Type UIKit.IUIFocusAnimationContext</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusAnimationContext : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
}
</pre>
</div> <!-- end type IUIFocusAnimationContext -->
<div> <!-- start type IUIFocusDebuggerOutput -->
<h3>New Type UIKit.IUIFocusDebuggerOutput</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusDebuggerOutput : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUIFocusDebuggerOutput -->
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
<div> <!-- start type NSItemProvider_UIKitAdditions -->
<h3>New Type UIKit.NSItemProvider_UIKitAdditions</h3>
<pre class='added' data-is-non-breaking="">
public static class NSItemProvider_UIKitAdditions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIPreferredPresentationStyle GetPreferredPresentationStyle (Foundation.NSItemProvider This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIPreferredPresentationStyle SetPreferredPresentationStyle (Foundation.NSItemProvider This);</span>
}
</pre>
</div> <!-- end type NSItemProvider_UIKitAdditions -->
<div> <!-- start type UIAccessibilityContainerType -->
<h3>New Type UIKit.UIAccessibilityContainerType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityContainerType {
	<span class='added added-field ' data-is-non-breaking="">DataTable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIAccessibilityContainerType -->
<div> <!-- start type UIAccessibilityCustomSystemRotorType -->
<h3>New Type UIKit.UIAccessibilityCustomSystemRotorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityCustomSystemRotorType {
	<span class='added added-field ' data-is-non-breaking="">BoldText = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Heading = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel1 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel2 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel3 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel4 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel5 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HeadingLevel6 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">ItalicText = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Landmark = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">Link = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">List = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">MisspelledWord = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Table = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TextField = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">UnderlineText = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">VisitedLink = 2,</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomSystemRotorType -->
<div> <!-- start type UICollectionViewFlowLayoutSectionInsetReference -->
<h3>New Type UIKit.UICollectionViewFlowLayoutSectionInsetReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UICollectionViewFlowLayoutSectionInsetReference {
	<span class='added added-field ' data-is-non-breaking="">ContentInset = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">LayoutMargins = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SafeArea = 1,</span>
}
</pre>
</div> <!-- end type UICollectionViewFlowLayoutSectionInsetReference -->
<div> <!-- start type UIDataSourceTranslating -->
<h3>New Type UIKit.UIDataSourceTranslating</h3>
<pre class='added' data-is-non-breaking="">
public abstract class UIDataSourceTranslating : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIDataSourceTranslating {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIDataSourceTranslating (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetDataSourceIndexPath (Foundation.NSIndexPath presentationIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetDataSourceSectionIndex (nint presentationSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSIndexPath GetPresentationIndexPath (Foundation.NSIndexPath dataSourceIndexPath);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint GetPresentationSectionIndex (nint dataSourceSectionIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformUsingPresentationValues (System.Action actionsToTranslate);</span>
}
</pre>
</div> <!-- end type UIDataSourceTranslating -->
<div> <!-- start type UIFocusDebugger -->
<h3>New Type UIKit.UIFocusDebugger</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusDebugger : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIFocusDebugger ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusDebugger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Help { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static IUIFocusDebuggerOutput Status { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput CheckFocusability (IUIFocusItem item);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusDebuggerOutput SimulateFocusUpdateRequest (IUIFocusEnvironment environment);</span>
}
</pre>
</div> <!-- end type UIFocusDebugger -->
<div> <!-- start type UIFocusSoundIdentifier -->
<h3>New Type UIKit.UIFocusSoundIdentifier</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIFocusSoundIdentifier {
	<span class='added added-field ' data-is-non-breaking="">Default = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type UIFocusSoundIdentifier -->
<div> <!-- start type UIFocusSoundIdentifierExtensions -->
<h3>New Type UIKit.UIFocusSoundIdentifierExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIFocusSoundIdentifierExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (UIFocusSoundIdentifier self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIFocusSoundIdentifier GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type UIFocusSoundIdentifierExtensions -->
<div> <!-- start type UIFocusSystem -->
<h3>New Type UIKit.UIFocusSystem</h3>
<pre class='added' data-is-non-breaking="">
public class UIFocusSystem : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIFocusSystem (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool Contains (IUIFocusEnvironment environment, IUIFocusEnvironment otherEnvironment);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RegisterUrl (Foundation.NSUrl soundFileUrl, Foundation.NSString identifier);</span>
}
</pre>
</div> <!-- end type UIFocusSystem -->
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
<div> <!-- start type UIScrollViewContentInsetAdjustmentBehavior -->
<h3>New Type UIKit.UIScrollViewContentInsetAdjustmentBehavior</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIScrollViewContentInsetAdjustmentBehavior {
	<span class='added added-field ' data-is-non-breaking="">Always = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Never = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScrollableAxes = 1,</span>
}
</pre>
</div> <!-- end type UIScrollViewContentInsetAdjustmentBehavior -->
<div> <!-- start type UISplitViewControllerPrimaryEdge -->
<h3>New Type UIKit.UISplitViewControllerPrimaryEdge</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UISplitViewControllerPrimaryEdge {
	<span class='added added-field ' data-is-non-breaking="">Leading = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Trailing = 1,</span>
}
</pre>
</div> <!-- end type UISplitViewControllerPrimaryEdge -->
<div> <!-- start type UITableViewSeparatorInsetReference -->
<h3>New Type UIKit.UITableViewSeparatorInsetReference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITableViewSeparatorInsetReference {
	<span class='added added-field ' data-is-non-breaking="">AutomaticInsets = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CellEdges = 0,</span>
}
</pre>
</div> <!-- end type UITableViewSeparatorInsetReference -->
<div> <!-- start type UITextSmartDashesType -->
<h3>New Type UIKit.UITextSmartDashesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartDashesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartDashesType -->
<div> <!-- start type UITextSmartInsertDeleteType -->
<h3>New Type UIKit.UITextSmartInsertDeleteType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartInsertDeleteType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartInsertDeleteType -->
<div> <!-- start type UITextSmartQuotesType -->
<h3>New Type UIKit.UITextSmartQuotesType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextSmartQuotesType {
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">No = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Yes = 2,</span>
}
</pre>
</div> <!-- end type UITextSmartQuotesType -->

</div> <!-- end namespace UIKit -->
<!-- start namespace VideoSubscriberAccount --> <div> 
<h2>Namespace VideoSubscriberAccount</h2>
<!-- start type VSAccountManagerDelegate --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountManagerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldAuthenticateAccountProvider (VSAccountManager accountManager, string accountProviderIdentifier);</span>
</pre>
</div>

</div> <!-- end type VSAccountManagerDelegate -->
<!-- start type VSAccountMetadataRequest --> <div>
<h3>Type Changed: VideoSubscriberAccount.VSAccountMetadataRequest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] FeaturedAccountProviderIdentifiers { get; set; }</span>
</pre>
</div>

</div> <!-- end type VSAccountMetadataRequest -->
<div> <!-- start type VSAccountManagerDelegate_Extensions -->
<h3>New Type VideoSubscriberAccount.VSAccountManagerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VSAccountManagerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldAuthenticateAccountProvider (IVSAccountManagerDelegate This, VSAccountManager accountManager, string accountProviderIdentifier);</span>
}
</pre>
</div> <!-- end type VSAccountManagerDelegate_Extensions -->
<div> <!-- start type VSSubscription -->
<h3>New Type VideoSubscriberAccount.VSSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class VSSubscription : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSSubscription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VSSubscriptionAccessLevel AccessLevel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ExpirationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] TierIdentifiers { get; set; }</span>
}
</pre>
</div> <!-- end type VSSubscription -->
<div> <!-- start type VSSubscriptionAccessLevel -->
<h3>New Type VideoSubscriberAccount.VSSubscriptionAccessLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VSSubscriptionAccessLevel {
	<span class='added added-field ' data-is-non-breaking="">FreeWithAccount = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Paid = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type VSSubscriptionAccessLevel -->
<div> <!-- start type VSSubscriptionRegistrationCenter -->
<h3>New Type VideoSubscriberAccount.VSSubscriptionRegistrationCenter</h3>
<pre class='added' data-is-non-breaking="">
public class VSSubscriptionRegistrationCenter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscriptionRegistrationCenter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSSubscriptionRegistrationCenter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static VSSubscriptionRegistrationCenter Default { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetCurrentSubscription (VSSubscription currentSubscription);</span>
}
</pre>
</div> <!-- end type VSSubscriptionRegistrationCenter -->

</div> <!-- end namespace VideoSubscriberAccount -->
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

<!-- start namespace DeviceCheck --> <div> 
<h2>New Namespace DeviceCheck</h2>

<div> <!-- start type DCDevice -->
<h3>New Type DeviceCheck.DCDevice</h3>
<pre class='added' data-is-non-breaking="">
public class DCDevice : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DCDevice ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected DCDevice (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static DCDevice CurrentDevice { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Supported { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void GenerateToken (DCDeviceGenerateTokenCompletionHandler completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; GenerateTokenAsync ();</span>
}
</pre>
</div> <!-- end type DCDevice -->
<div> <!-- start type DCDeviceGenerateTokenCompletionHandler -->
<h3>New Type DeviceCheck.DCDeviceGenerateTokenCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate DCDeviceGenerateTokenCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public DCDeviceGenerateTokenCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData token, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData token, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type DCDeviceGenerateTokenCompletionHandler -->
<div> <!-- start type DCError -->
<h3>New Type DeviceCheck.DCError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum DCError {
	<span class='added added-field ' data-is-non-breaking="">FeatureUnsupported = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownSystemFailure = 0,</span>
}
</pre>
</div> <!-- end type DCError -->
<div> <!-- start type DCErrorExtensions -->
<h3>New Type DeviceCheck.DCErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class DCErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (DCError self);</span>
}
</pre>
</div> <!-- end type DCErrorExtensions -->
</div> <!-- end namespace DeviceCheck -->

<!-- start namespace Vision --> <div> 
<h2>New Namespace Vision</h2>

<div> <!-- start type IVNFaceObservationAccepting -->
<h3>New Type Vision.IVNFaceObservationAccepting</h3>
<pre class='added' data-is-non-breaking="">
public interface IVNFaceObservationAccepting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type IVNFaceObservationAccepting -->
<div> <!-- start type VNBarcodeObservation -->
<h3>New Type Vision.VNBarcodeObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNBarcodeObservation : Vision.VNRectangleObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNBarcodeObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNBarcodeObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIBarcodeDescriptor BarcodeDescriptor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PayloadStringValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology Symbology { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString WeakSymbology { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNBarcodeObservation -->
<div> <!-- start type VNBarcodeSymbology -->
<h3>New Type Vision.VNBarcodeSymbology</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNBarcodeSymbology {
	<span class='added added-field ' data-is-non-breaking="">Aztec = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Code128 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39Checksum = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAscii = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Code39FullAsciiChecksum = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93 = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Code93i = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DataMatrix = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean13 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Ean8 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5 = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">I2OF5Checksum = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">Itf14 = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">Pdf417 = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">QR = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Upce = 16,</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbology -->
<div> <!-- start type VNBarcodeSymbologyExtensions -->
<h3>New Type Vision.VNBarcodeSymbologyExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNBarcodeSymbologyExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (VNBarcodeSymbology self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString[] GetConstants (VNBarcodeSymbology[] self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology GetValue (Foundation.NSString constant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static VNBarcodeSymbology[] GetValues (Foundation.NSString[] constants);</span>
}
</pre>
</div> <!-- end type VNBarcodeSymbologyExtensions -->
<div> <!-- start type VNClassificationObservation -->
<h3>New Type Vision.VNClassificationObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNClassificationObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNClassificationObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNClassificationObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
}
</pre>
</div> <!-- end type VNClassificationObservation -->
<div> <!-- start type VNCoreMLFeatureValueObservation -->
<h3>New Type Vision.VNCoreMLFeatureValueObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLFeatureValueObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLFeatureValueObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLFeatureValueObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreML.MLFeatureValue FeatureValue { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLFeatureValueObservation -->
<div> <!-- start type VNCoreMLModel -->
<h3>New Type Vision.VNCoreMLModel</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLModel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLModel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNCoreMLModel FromMLModel (CoreML.MLModel model, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNCoreMLModel -->
<div> <!-- start type VNCoreMLRequest -->
<h3>New Type Vision.VNCoreMLRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNCoreMLRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNCoreMLRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNCoreMLRequest (VNCoreMLModel model, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNImageCropAndScaleOption ImageCropAndScaleOption { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNCoreMLModel Model { get; }</span>
}
</pre>
</div> <!-- end type VNCoreMLRequest -->
<div> <!-- start type VNDetectBarcodesRequest -->
<h3>New Type Vision.VNDetectBarcodesRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNDetectBarcodesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectBarcodesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectBarcodesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static VNBarcodeSymbology[] SupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public VNBarcodeSymbology[] Symbologies { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected static Foundation.NSString[] WeakSupportedSymbologies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected virtual Foundation.NSString[] WeakSymbologies { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectBarcodesRequest -->
<div> <!-- start type VNDetectFaceLandmarksRequest -->
<h3>New Type Vision.VNDetectFaceLandmarksRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceLandmarksRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVNFaceObservationAccepting {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceLandmarksRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceLandmarksRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceObservation[] InputFaceObservations { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceLandmarksRequest -->
<div> <!-- start type VNDetectFaceRectanglesRequest -->
<h3>New Type Vision.VNDetectFaceRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectFaceRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectFaceRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectFaceRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectFaceRectanglesRequest -->
<div> <!-- start type VNDetectHorizonRequest -->
<h3>New Type Vision.VNDetectHorizonRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectHorizonRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectHorizonRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectHorizonRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNDetectHorizonRequest -->
<div> <!-- start type VNDetectRectanglesRequest -->
<h3>New Type Vision.VNDetectRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MaximumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumObservations { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumAspectRatio { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumConfidence { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float MinimumSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float QuadratureTolerance { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectRectanglesRequest -->
<div> <!-- start type VNDetectTextRectanglesRequest -->
<h3>New Type Vision.VNDetectTextRectanglesRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectTextRectanglesRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectTextRectanglesRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectTextRectanglesRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReportCharacterBoxes { get; set; }</span>
}
</pre>
</div> <!-- end type VNDetectTextRectanglesRequest -->
<div> <!-- start type VNDetectedObjectObservation -->
<h3>New Type Vision.VNDetectedObjectObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNDetectedObjectObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNDetectedObjectObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNDetectedObjectObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect BoundingBox { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNDetectedObjectObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNDetectedObjectObservation -->
<div> <!-- start type VNErrorCode -->
<h3>New Type Vision.VNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">IOError = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InternalError = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidArgument = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidImage = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidModel = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOperation = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOption = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingOption = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">NotImplemented = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Ok = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationFailed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfBoundsError = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">OutOfMemory = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">RequestCancelled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UnknownError = 11,</span>
}
</pre>
</div> <!-- end type VNErrorCode -->
<div> <!-- start type VNErrorCodeExtensions -->
<h3>New Type Vision.VNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VNErrorCode self);</span>
}
</pre>
</div> <!-- end type VNErrorCodeExtensions -->
<div> <!-- start type VNFaceLandmarkRegion -->
<h3>New Type Vision.VNFaceLandmarkRegion</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarkRegion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PointCount { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion -->
<div> <!-- start type VNFaceLandmarkRegion2D -->
<h3>New Type Vision.VNFaceLandmarkRegion2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarkRegion2D : Vision.VNFaceLandmarkRegion, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarkRegion2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] NormalizedPoints { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint[] GetPointsInImage (CoreGraphics.CGSize imageSize);</span>
}
</pre>
</div> <!-- end type VNFaceLandmarkRegion2D -->
<div> <!-- start type VNFaceLandmarks -->
<h3>New Type Vision.VNFaceLandmarks</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNFaceLandmarks : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks -->
<div> <!-- start type VNFaceLandmarks2D -->
<h3>New Type Vision.VNFaceLandmarks2D</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceLandmarks2D : Vision.VNFaceLandmarks, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceLandmarks2D (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D AllPoints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D FaceContour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D InnerLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D LeftPupil { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D MedianLine { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D Nose { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D NoseCrest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D OuterLips { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightEyebrow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarkRegion2D RightPupil { get; }</span>
}
</pre>
</div> <!-- end type VNFaceLandmarks2D -->
<div> <!-- start type VNFaceObservation -->
<h3>New Type Vision.VNFaceObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNFaceObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNFaceObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNFaceObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNFaceLandmarks2D Landmarks { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNFaceObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNFaceObservation -->
<div> <!-- start type VNHomographicImageRegistrationRequest -->
<h3>New Type Vision.VNHomographicImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNHomographicImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHomographicImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNHomographicImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNHomographicImageRegistrationRequest -->
<div> <!-- start type VNHorizonObservation -->
<h3>New Type Vision.VNHorizonObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNHorizonObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNHorizonObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNHorizonObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Angle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform Transform { get; }</span>
}
</pre>
</div> <!-- end type VNHorizonObservation -->
<div> <!-- start type VNImageAlignmentObservation -->
<h3>New Type Vision.VNImageAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageAlignmentObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageAlignmentObservation -->
<div> <!-- start type VNImageBasedRequest -->
<h3>New Type Vision.VNImageBasedRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageBasedRequest : Vision.VNRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageBasedRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageBasedRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect RegionOfInterest { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageBasedRequest -->
<div> <!-- start type VNImageCropAndScaleOption -->
<h3>New Type Vision.VNImageCropAndScaleOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNImageCropAndScaleOption {
	<span class='added added-field ' data-is-non-breaking="">CenterCrop = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFill = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ScaleFit = 1,</span>
}
</pre>
</div> <!-- end type VNImageCropAndScaleOption -->
<div> <!-- start type VNImageHomographicAlignmentObservation -->
<h3>New Type Vision.VNImageHomographicAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageHomographicAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageHomographicAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageHomographicAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Matrix3 WarpTransform { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageHomographicAlignmentObservation -->
<div> <!-- start type VNImageOptions -->
<h3>New Type Vision.VNImageOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreImage.CIContext CIContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData CameraIntrinsics { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGImageProperties Properties { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary WeakProperties { get; set; }</span>
}
</pre>
</div> <!-- end type VNImageOptions -->
<div> <!-- start type VNImageRegistrationRequest -->
<h3>New Type Vision.VNImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNImageRegistrationRequest : Vision.VNTargetedImageRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageRegistrationRequest -->
<div> <!-- start type VNImageRequestHandler -->
<h3>New Type Vision.VNImageRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageRequestHandler (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageRequestHandler (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions imageOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNImageRequestHandler -->
<div> <!-- start type VNImageTranslationAlignmentObservation -->
<h3>New Type Vision.VNImageTranslationAlignmentObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNImageTranslationAlignmentObservation : Vision.VNImageAlignmentObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNImageTranslationAlignmentObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNImageTranslationAlignmentObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGAffineTransform AlignmentTransform { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNImageTranslationAlignmentObservation -->
<div> <!-- start type VNObservation -->
<h3>New Type Vision.VNObservation</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNObservation : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Confidence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid Uuid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type VNObservation -->
<div> <!-- start type VNPixelBufferObservation -->
<h3>New Type Vision.VNPixelBufferObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNPixelBufferObservation : Vision.VNObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNPixelBufferObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNPixelBufferObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
}
</pre>
</div> <!-- end type VNPixelBufferObservation -->
<div> <!-- start type VNRectangleObservation -->
<h3>New Type Vision.VNRectangleObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNRectangleObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRectangleObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRectangleObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint BottomRight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopLeft { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint TopRight { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNRectangleObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNRectangleObservation -->
<div> <!-- start type VNRequest -->
<h3>New Type Vision.VNRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNRequest : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestCompletionHandler CompletionHandler { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreferBackgroundProcessing { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice PreferredMetalContext { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UsesCpuOnly { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual T[] GetResults&lt;T&gt; ();</span>
}
</pre>
</div> <!-- end type VNRequest -->
<div> <!-- start type VNRequestCompletionHandler -->
<h3>New Type Vision.VNRequestCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate VNRequestCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNRequestCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (VNRequest request, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (VNRequest request, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNRequestCompletionHandler -->
<div> <!-- start type VNRequestTrackingLevel -->
<h3>New Type Vision.VNRequestTrackingLevel</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VNRequestTrackingLevel {
	<span class='added added-field ' data-is-non-breaking="">Accurate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
}
</pre>
</div> <!-- end type VNRequestTrackingLevel -->
<div> <!-- start type VNSequenceRequestHandler -->
<h3>New Type Vision.VNSequenceRequestHandler</h3>
<pre class='added' data-is-non-breaking="">
public class VNSequenceRequestHandler : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNSequenceRequestHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNSequenceRequestHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreGraphics.CGImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreImage.CIImage image, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Perform (VNRequest[] requests, Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type VNSequenceRequestHandler -->
<div> <!-- start type VNTargetedImageRequest -->
<h3>New Type Vision.VNTargetedImageRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTargetedImageRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTargetedImageRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreGraphics.CGImage cgImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreImage.CIImage ciImage, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (CoreVideo.CVPixelBuffer pixelBuffer, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSData imageData, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, Foundation.NSDictionary optionsDict, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTargetedImageRequest (Foundation.NSUrl imageUrl, ImageIO.CGImagePropertyOrientation orientation, VNImageOptions options, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTargetedImageRequest -->
<div> <!-- start type VNTextObservation -->
<h3>New Type Vision.VNTextObservation</h3>
<pre class='added' data-is-non-breaking="">
public class VNTextObservation : Vision.VNDetectedObjectObservation, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTextObservation (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTextObservation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRectangleObservation[] CharacterBoxes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static VNTextObservation FromBoundingBox (CoreGraphics.CGRect boundingBox);</span>
}
</pre>
</div> <!-- end type VNTextObservation -->
<div> <!-- start type VNTrackObjectRequest -->
<h3>New Type Vision.VNTrackObjectRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackObjectRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackObjectRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackObjectRequest (VNDetectedObjectObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackObjectRequest -->
<div> <!-- start type VNTrackRectangleRequest -->
<h3>New Type Vision.VNTrackRectangleRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTrackRectangleRequest : Vision.VNTrackingRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackRectangleRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackRectangleRequest (VNRectangleObservation observation, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTrackRectangleRequest -->
<div> <!-- start type VNTrackingRequest -->
<h3>New Type Vision.VNTrackingRequest</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VNTrackingRequest : Vision.VNImageBasedRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTrackingRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTrackingRequest (VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNDetectedObjectObservation InputObservation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool LastFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual VNRequestTrackingLevel TrackingLevel { get; set; }</span>
}
</pre>
</div> <!-- end type VNTrackingRequest -->
<div> <!-- start type VNTranslationalImageRegistrationRequest -->
<h3>New Type Vision.VNTranslationalImageRegistrationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VNTranslationalImageRegistrationRequest : Vision.VNImageRegistrationRequest, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VNTranslationalImageRegistrationRequest (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreGraphics.CGImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreImage.CIImage image, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (CoreVideo.CVPixelBuffer pixelBuffer, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSData imageData, VNRequestCompletionHandler completionHandler);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VNTranslationalImageRegistrationRequest (Foundation.NSUrl imageUrl, VNRequestCompletionHandler completionHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type VNTranslationalImageRegistrationRequest -->
<div> <!-- start type VNUtils -->
<h3>New Type Vision.VNUtils</h3>
<pre class='added' data-is-non-breaking="">
public static class VNUtils {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGRect NormalizedIdentityRect { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (CoreGraphics.CGPoint normalizedPoint, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetImagePoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetImageRect (CoreGraphics.CGRect normalizedRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGPoint GetNormalizedFaceBoundingBoxPoint (OpenTK.Vector2 faceLandmarkPoint, CoreGraphics.CGRect faceBoundingBox, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetNormalizedRect (CoreGraphics.CGRect imageRect, uint imageWidth, uint imageHeight);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool IsIdentityRect (CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type VNUtils -->
</div> <!-- end namespace Vision -->

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
</script><h1 id='diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

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
