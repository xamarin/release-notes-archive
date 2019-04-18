---
id: 05D6F0F8-BAD3-41F1-852B-45D227F5AACB
title: "From 6.9.2 to 6.9.3"
---

<html><head><title>Comparison between monotouch-6.9.2.dll and monotouch-6.9.3.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.2";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.3";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemVideoOutput</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
</pre>
<p>Added:</p><pre>
 	public MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
 	protected virtual IntPtr WeakCopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechBoundary</h3>
<pre>
[Serializable]
public enum AVSpeechBoundary {
	Immediate,
	Word
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesisVoice</h3>
<pre>
public class AVSpeechSynthesisVoice : MonoTouch.Foundation.NSObject {
	
	public AVSpeechSynthesisVoice ();
	public AVSpeechSynthesisVoice (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesisVoice (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesisVoice (IntPtr handle);
	
	public static AVSpeechSynthesisVoice FromLanguage (string language);
	public static AVSpeechSynthesisVoice[] GetSpeechVoices ();
	
	public static string CurrentLanguageCode {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Language {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizer</h3>
<pre>
public class AVSpeechSynthesizer : MonoTouch.Foundation.NSObject {
	
	public AVSpeechSynthesizer ();
	public AVSpeechSynthesizer (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesizer (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesizer (IntPtr handle);
	
	public virtual bool ContinueSpeaking ();
	protected override void Dispose (bool disposing);
	public virtual bool PauseSpeaking (AVSpeechBoundary boundary);
	public virtual void SpeakUtterance (AVSpeechUtterance utterance);
	public virtual bool StopSpeaking (AVSpeechBoundary boundary);
	
	public override IntPtr ClassHandle {
		get;
	}
	public AVSpeechSynthesizerDelegate Delegate {
		get;
		set;
	}
	public virtual bool Paused {
		get;
	}
	public virtual bool Speaking {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidCancelSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidContinueSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidFinishSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidPauseSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidStartSpeechUtterance;
	public event EventHandler<avspeechsynthesizerwillspeakeventargs> WillSpeakRangeOfSpeechString;
}
</avspeechsynthesizerwillspeakeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerDelegate</h3>
<pre>
public class AVSpeechSynthesizerDelegate : MonoTouch.Foundation.NSObject {
	
	public AVSpeechSynthesizerDelegate ();
	public AVSpeechSynthesizerDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesizerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesizerDelegate (IntPtr handle);
	
	public virtual void DidCancelSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidContinueSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidFinishSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidPauseSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidStartSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void WillSpeakRangeOfSpeechString (AVSpeechSynthesizer synthesizer, MonoTouch.Foundation.NSRange characterRange, AVSpeechUtterance utterance);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerUteranceEventArgs</h3>
<pre>
public class AVSpeechSynthesizerUteranceEventArgs : EventArgs {
	
	public AVSpeechSynthesizerUteranceEventArgs (AVSpeechUtterance utterance);
	
	public AVSpeechUtterance Utterance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerWillSpeakEventArgs</h3>
<pre>
public class AVSpeechSynthesizerWillSpeakEventArgs : EventArgs {
	
	public AVSpeechSynthesizerWillSpeakEventArgs (MonoTouch.Foundation.NSRange characterRange, AVSpeechUtterance utterance);
	
	public MonoTouch.Foundation.NSRange CharacterRange {
		get;
		set;
	}
	public AVSpeechUtterance Utterance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechUtterance</h3>
<pre>
public class AVSpeechUtterance : MonoTouch.Foundation.NSObject {
	
	public AVSpeechUtterance ();
	public AVSpeechUtterance (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechUtterance (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechUtterance (IntPtr handle);
	public AVSpeechUtterance (string speechString);
	
	public static AVSpeechUtterance FromString (string speechString);
	protected override void Dispose (bool disposing);
	
	public static float DefaultSpeechRate {
		get;
	}
	public static float MaximumSpeechRate {
		get;
	}
	public static float MinimumSpeechRate {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float PitchMultiplier {
		get;
		set;
	}
	public virtual double PostUtteranceDelay {
		get;
		set;
	}
	public virtual double PreUtteranceDelay {
		get;
		set;
	}
	public virtual float Rate {
		get;
		set;
	}
	public virtual string SpeechString {
		get;
	}
	public virtual AVSpeechSynthesisVoice Voice {
		get;
		set;
	}
	public virtual float Volume {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ProfileLevelH264BaselineAutoLevel {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProfileLevelH264HighAutoLevel {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProfileLevelH264MainAutoLevel {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoScalingModeKey</h3>
<pre>
public static class AVVideoScalingModeKey {
	
	public static MonoTouch.Foundation.NSString Fit {
		get;
	}
	public static MonoTouch.Foundation.NSString Resize {
		get;
	}
	public static MonoTouch.Foundation.NSString ResizeAspect {
		get;
	}
	public static MonoTouch.Foundation.NSString ResizeAspectFill {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>New Type: MonoTouch.Accounts.ACFacebookAudienceValue</h3>
<pre>
public static class ACFacebookAudienceValue {
	
	public static MonoTouch.Foundation.NSString Everyone {
		get;
	}
	public static MonoTouch.Foundation.NSString Friends {
		get;
	}
	public static MonoTouch.Foundation.NSString OnlyMe {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Accounts.ACFacebookKey</h3>
<pre>
public static class ACFacebookKey {
	
	public static MonoTouch.Foundation.NSString AppId {
		get;
	}
	public static MonoTouch.Foundation.NSString Audience {
		get;
	}
	public static MonoTouch.Foundation.NSString Permissions {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Accounts.ACTencentWeiboKey</h3>
<pre>
public static class ACTencentWeiboKey {
	
	public static MonoTouch.Foundation.NSString AppId {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentral</h3>
<p>Removed:</p><pre>
 	public virtual IntPtr UUID {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual IntPtr UUID {
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Removed:</p><pre>
 	public virtual void RetrieveConnectedPeripherals ();
 	public void RetrievePeripherals (CBUUID[] peripheralUuids);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual void RetrieveConnectedPeripherals ();
 	[Obsolete("Deprecated in iOS7")]
	public void RetrievePeripherals (CBUUID[] peripheralUuids);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Removed:</p><pre>
 	public virtual bool IsConnected {
 	public virtual IntPtr UUID {
 	public event EventHandler InvalidatedService;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual bool IsConnected {
 	[Obsolete("Deprecated in iOS7")]
	public virtual IntPtr UUID {
 	[Obsolete("Deprecated in iOS7")]
	public event EventHandler InvalidatedService;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void InvalidatedService (CBPeripheral peripheral);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual void InvalidatedService (CBPeripheral peripheral);
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchQueue</h3>
<p>Added:</p><pre>
 	public static string CurrentQueueLabel {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h3>
<p>Removed:</p><pre>
 	protected override void Finalize ();
 	
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.DictionaryContainer</h3>
<p>Removed:</p><pre>
 	protected string GetNSStringValue (NSString key);
</pre>
<p>Added:</p><pre>
 	protected NSString GetNSStringValue (NSString key);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Added:</p><pre>
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary documentAttributes, out NSError error);
</pre>
<h3>New Type: MonoTouch.Foundation.NSAttributedStringDocumentAttributes</h3>
<pre>
public class NSAttributedStringDocumentAttributes : DictionaryContainer {
	
	public NSAttributedStringDocumentAttributes ();
	public NSAttributedStringDocumentAttributes (NSDictionary dictionary);
	
	public MonoTouch.UIKit.UIColor BackgroundColor {
		get;
		set;
	}
	public Nullable<float> DefaultTabInterval {
		get;
		set;
	}
	public NSDocumentType DocumentType {
		get;
		set;
	}
	public Nullable<float> HyphenationFactor {
		get;
		set;
	}
	public System.Nullable<monotouch.uikit.uiedgeinsets> PaperMargin {
		get;
		set;
	}
	public System.Nullable<system.drawing.sizef> PaperSize {
		get;
		set;
	}
	public bool ReadOnly {
		get;
		set;
	}
	public Nullable<nsstringencoding> StringEncoding {
		get;
		set;
	}
	public Nullable<nsdocumentviewmode> ViewMode {
		get;
		set;
	}
	public System.Nullable<system.drawing.sizef> ViewSize {
		get;
		set;
	}
	public Nullable<float> ViewZoom {
		get;
		set;
	}
	public NSString WeakDocumentType {
		get;
		set;
	}
}
</float></system.drawing.sizef></nsdocumentviewmode></nsstringencoding></system.drawing.sizef></monotouch.uikit.uiedgeinsets></float></float></pre>
<h3>New Type: MonoTouch.Foundation.NSDocumentType</h3>
<pre>
[Serializable]
public enum NSDocumentType {
	Unknown,
	PlainText,
	RTF,
	RTFD
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSDocumentViewMode</h3>
<pre>
[Serializable]
public enum NSDocumentViewMode {
	Normal,
	PageLayout
}
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static void void_objc_msgSend_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
</pre>
<h2>Namespace: MonoTouch.Social</h2>
<h3>New Type: MonoTouch.Social.SLServiceType</h3>
<pre>
public static class SLServiceType {
	
	public static MonoTouch.Foundation.NSString Facebook {
		get;
	}
	public static MonoTouch.Foundation.NSString LinkedIn {
		get;
	}
	public static MonoTouch.Foundation.NSString SinaWeibo {
		get;
	}
	public static MonoTouch.Foundation.NSString TencentWeibo {
		get;
	}
	public static MonoTouch.Foundation.NSString Twitter {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>New Type: MonoTouch.StoreKit.SKStoreProductParameterKey</h3>
<pre>
public static class SKStoreProductParameterKey {
	
	public static MonoTouch.Foundation.NSString ITunesItemIdentifier {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.NSTextEffect</h3>
<pre>
[Serializable]
public enum NSTextEffect {
	None,
	LetterPressStyle,
	UnknownUseWeakEffect
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBehavior</h3>
<p>Removed:</p><pre>
 	public UICollisionBehavior (MonoTouch.Foundation.NSObject items);
</pre>
<p>Added:</p><pre>
 	public UICollisionBehavior (MonoTouch.Foundation.NSObject[] items);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Removed:</p><pre>
 	public UIImage (UIImage image);
 	public UIImage (UIImage image, MonoTouch.Foundation.NSDictionary options);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerController</h3>
<p>Removed:</p><pre>
 	public UIInterfaceOrientationProbe GetPreferredInterfaceOrientation {
 	public UIInterfaceOrientationMaskProbe GetSupportedInterfaceOrientations {
</pre>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
</pre>
<h3>Type Removed: MonoTouch.UIKit.UIInterfaceOrientationMaskProbe</h3>
<h3>Type Removed: MonoTouch.UIKit.UIInterfaceOrientationProbe</h3>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributeKey</h3>
<p>Removed:</p><pre>
 	public static readonly MonoTouch.Foundation.NSString Font;
 	public static readonly MonoTouch.Foundation.NSString ForegroundColor;
 	public static readonly MonoTouch.Foundation.NSString BackgroundColor;
 	public static readonly MonoTouch.Foundation.NSString StrikethroughStyle;
 	public static readonly MonoTouch.Foundation.NSString StrokeColor;
 	public static readonly MonoTouch.Foundation.NSString Shadow;
 	public static readonly MonoTouch.Foundation.NSString ParagraphStyle;
 	public static readonly MonoTouch.Foundation.NSString Ligature;
 	public static readonly MonoTouch.Foundation.NSString KerningAdjustment;
 	public static readonly MonoTouch.Foundation.NSString UnderlineStyle;
 	public static readonly MonoTouch.Foundation.NSString StrokeWidth;
 	public static readonly MonoTouch.Foundation.NSString VerticalGlyphForm;
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Attachment {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BackgroundColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BaselineOffset {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Expansion {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Font {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ForegroundColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString KerningAdjustment {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Ligature {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Link {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Obliqueness {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ParagraphStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Shadow {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrikethroughColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrikethroughStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrokeColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrokeWidth {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextAlternatives {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextEffect {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UnderlineColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UnderlineStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString VerticalGlyphForm {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WritingDirection {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributes</h3>
<p>Added:</p><pre>
 	public Nullable&lt;float&gt; BaselineOffset {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; Expansion {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSUrl Link {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; Obliqueness {
 		get;
 		set;
 	}
 	public UIColor StrikethroughColor {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSObject TextAlternativesObject {
 		get;
 		set;
 	}
 	public NSTextAttachment TextAttachment {
 		get;
 		set;
 	}
 	public NSTextEffect TextEffect {
 		get;
 		set;
 	}
 	public UIColor UnderlineColor {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSString WeakTextEffect {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSNumber[] WritingDirectionInt {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarController</h3>
<p>Added:</p><pre>
 	public Func&lt;UITabBarController,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForTransition {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UITabBarController tabBarController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UITabBarController tabBarController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorController</h3>
<p>Removed:</p><pre>
 	public UIInterfaceOrientationProbe GetPreferredInterfaceOrientation {
 	public UIInterfaceOrientationMaskProbe GetSupportedInterfaceOrientations {
</pre>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
</pre>
</body>
</html>
