---
id: 999D991B-1C73-4905-A615-8C2C7CBE90DD
title: "From 6.9.1 to 6.9.2"
---

<html><head><title>Comparison between monotouch-6.9.1.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.1";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.2";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Removed:</p><pre>
 	public virtual AVPlayerItemOutput Outputs {
</pre>
<p>Added:</p><pre>
 	public virtual AVPlayerItemOutput[] Outputs {
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate</h3>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Removed:</p><pre>
 	public event EventHandler&lt;CBPeripheralServicesEventArgs&gt; InvalidatedServices;
</pre>
<p>Added:</p><pre>
 	public event EventHandler&lt;CBPeripheralServicesEventArgs&gt; ModifiedServices;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void InvalidatedServices (CBPeripheral peripheral, MonoTouch.Foundation.NSArray services);
</pre>
<p>Added:</p><pre>
 	public virtual void ModifiedServices (CBPeripheral peripheral, MonoTouch.Foundation.NSArray services);
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator</h3>
<p>Added:</p><pre>
 	public static bool RemoveUbiquitousContentAndPersistentStore (MonoTouch.Foundation.NSUrl storeUrl, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
 	public static MonoTouch.Foundation.NSString eUbiquitousContainerIdentifierKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RebuildFromUbiquitousContentOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RemoveUbiquitousMetadataOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StoresWillChangeNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveDidImportUbiquitousContentChanges (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveStoresDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveStoresWillChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveWillRemoveStore (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h2>Namespace: MonoTouch.CoreImage</h2>
<h3>Type Changed: MonoTouch.CoreImage.CIDetector</h3>
<p>Added:</p><pre>
 	public static CIDetector CreateFaceDetector (CIContext context, CIDetectorOptions detectorOptions);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIDetectorKeys</h3>
<pre>
public static class CIDetectorKeys {
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIDetectorOptions</h3>
<pre>
public class CIDetectorOptions {
	
	public CIDetectorOptions ();
	
	public Nullable<facedetectoraccuracy> Accuracy {
		get;
		set;
	}
	public Nullable<bool> EyeBlink {
		get;
		set;
	}
	public Nullable<float> MinFeatureSize {
		get;
		set;
	}
	public Nullable<bool> Smile {
		get;
		set;
	}
	public Nullable<bool> TrackingEnabled {
		get;
		set;
	}
}
</bool></bool></float></bool></facedetectoraccuracy></pre>
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>Type Changed: MonoTouch.CoreMedia.CMFormatDescriptionError</h3>
<p>Removed:</p><pre>
 	AllocationFailed
</pre>
<p>Added:</p><pre>
 	AllocationFailed,
 	ValueNotAvailable
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSBundle</h3>
<p>Added:</p><pre>
 	public virtual NSUrl AppStoreReceiptUrl {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSData</h3>
<p>Added:</p><pre>
 	public NSData (string base64String, NSDataBase64DecodingOptions options);
 	public NSData (NSData base64Data, NSDataBase64DecodingOptions options);
 	public virtual NSData GetBase64EncodedData (NSDataBase64EncodingOptions options);
 	public virtual string GetBase64EncodedString (NSDataBase64EncodingOptions options);
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataBase64DecodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64DecodingOptions {
	None,
	IgnoreUnknownCharacters
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataBase64EncodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64EncodingOptions {
	None,
	SixtyFourCharacterLineLength,
	SeventySixCharacterLineLength,
	EndLineWithCarriageReturn,
	EndLineWithLineFeed
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSLocale</h3>
<p>Added:</p><pre>
 	public static NSLocale FromLocaleIdentifier (string ident);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSTimer</h3>
<p>Added:</p><pre>
 	public virtual double Tolerance {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUserDefaults</h3>
<p>Removed:</p><pre>
 	public NSUserDefaults (string username);
 	public virtual string [] PersistentDomainNames ();
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public NSUserDefaults (string username);
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public virtual string [] PersistentDomainNames ();
 	public static NSString ArgumentDomain {
 		get;
 	}
 	public static NSString GlobalDomain {
 		get;
 	}
 	public static NSString RegistrationDomain {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.GameController</h2>
<h3>Type Changed: MonoTouch.GameController.GCExtendedGamepadSnapshot</h3>
<p>Added:</p><pre>
 	public GCExtendedGamepadSnapshot (GCController controller, MonoTouch.Foundation.NSData data);
</pre>
<h3>Type Changed: MonoTouch.GameController.GCGamepadSnapshot</h3>
<p>Added:</p><pre>
 	public GCGamepadSnapshot (GCController controller, MonoTouch.Foundation.NSData data);
</pre>
<h2>Namespace: MonoTouch.ImageIO</h2>
<h3>Type Changed: MonoTouch.ImageIO.CGImageOptions</h3>
<p>Added:</p><pre>
 	public bool ShouldCacheImmediately {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageSource</h3>
<p>Added:</p><pre>
 	public void RemoveCache (int index);
</pre>
<h2>Namespace: MonoTouch.MessageUI</h2>
<h3>Type Changed: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate</h3>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
</pre>
<h2>Namespace: MonoTouch.MultipeerConnectivity</h2>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistant</h3>
<pre>
public class MCAdvertiserAssistant : MonoTouch.Foundation.NSObject {
	
	public MCAdvertiserAssistant ();
	public MCAdvertiserAssistant (MonoTouch.Foundation.NSCoder coder);
	public MCAdvertiserAssistant (MonoTouch.Foundation.NSObjectFlag t);
	public MCAdvertiserAssistant (IntPtr handle);
	public MCAdvertiserAssistant (string serviceType, MonoTouch.Foundation.NSDictionary info, MCSession session);
	
	protected override void Dispose (bool disposing);
	public virtual void Start ();
	public virtual void Stop ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public MCAdvertiserAssistantDelegate Delegate {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary DiscoveryInfo {
		get;
	}
	public virtual string ServiceType {
		get;
	}
	public virtual MCSession Session {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistantDelegate</h3>
<pre>
public class MCAdvertiserAssistantDelegate : MonoTouch.Foundation.NSObject {
	
	public MCAdvertiserAssistantDelegate ();
	public MCAdvertiserAssistantDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCAdvertiserAssistantDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCAdvertiserAssistantDelegate (IntPtr handle);
	
	public virtual void DidDismissInvitaiton (MCAdvertiserAssistant advertiserAssistant);
	public virtual void WillPresentInvitation (MCAdvertiserAssistant advertiserAssistant);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCBrowserViewController</h3>
<pre>
public class MCBrowserViewController : MonoTouch.UIKit.UIViewController {
	
	public MCBrowserViewController (MonoTouch.Foundation.NSCoder coder);
	public MCBrowserViewController (MonoTouch.Foundation.NSObjectFlag t);
	public MCBrowserViewController (IntPtr handle);
	public MCBrowserViewController (MCNearbyServiceBrowser browser, MCSession session);
	public MCBrowserViewController (string serviceType, MCSession session);
	
	protected override void Dispose (bool disposing);
	
	public virtual MCNearbyServiceBrowser Browser {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public MCBrowserViewControllerDelegate Delegate {
		get;
		set;
	}
	public virtual uint MaximumNumberOfPeers {
		get;
		set;
	}
	public virtual uint MinimumNumberOfPeers {
		get;
		set;
	}
	public virtual MCSession Session {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCBrowserViewControllerDelegate</h3>
<pre>
public class MCBrowserViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public MCBrowserViewControllerDelegate ();
	public MCBrowserViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCBrowserViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCBrowserViewControllerDelegate (IntPtr handle);
	
	public virtual void DidFinish (MCBrowserViewController browserViewController);
	public virtual bool ShouldPresentNearbyPeer (MCBrowserViewController browserViewController, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public virtual void WasCancelled (MCBrowserViewController browserViewController);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCError</h3>
<pre>
[Serializable]
public enum MCError {
	Unknown,
	NotConnected,
	InvalidParameter,
	Unsupported,
	TimedOut,
	Cancelled
}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiser</h3>
<p>Removed:</p><pre>
 	public virtual MCNearbyServiceAdvertiserDelegate Delegate {
</pre>
<p>Added:</p><pre>
 	public MCNearbyServiceAdvertiserDelegate Delegate {
 	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCNearbyServiceBrowser</h3>
<p>Removed:</p><pre>
 	public virtual void InvitePeer (MCPeerID peer, MCSession session, MonoTouch.Foundation.NSData context, double timeout);
 	public virtual MCNearbyServiceBrowserDelegate Delegate {
</pre>
<p>Added:</p><pre>
 	public virtual void InvitePeer (MCPeerID peerID, MCSession session, MonoTouch.Foundation.NSData context, double timeout);
 	public MCNearbyServiceBrowserDelegate Delegate {
 	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
 		get;
 		set;
 	}
</pre>
<h3>Type Removed: MonoTouch.MultipeerConnectivity.MCPeerPickerViewController</h3>
<h3>Type Removed: MonoTouch.MultipeerConnectivity.MCPeerPickerViewControllerDelegate</h3>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSession</h3>
<p>Removed:</p><pre>
 	public virtual void ConnectPeer (MCPeerID peerID, MonoTouch.Foundation.NSData data, double timeout);
 	public virtual void SendResource (MonoTouch.Foundation.NSUrl resourceUrl, MCPeerID peerID, double timeout, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual MCSessionDelegate Delegate {
</pre>
<p>Added:</p><pre>
 	public virtual void ConnectPeer (MCPeerID peerID, MonoTouch.Foundation.NSData data);
 	public virtual MonoTouch.Foundation.NSObject SendResource (MonoTouch.Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public static int MinimumNumberOfPeers {
 		get;
 	}
 	public MCSessionDelegate Delegate {
 	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSessionDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidReceiveResource (MCSession session, MonoTouch.Foundation.NSUrl resourceUrl, MCPeerID peerID);
 	public virtual bool ShouldAcceptCertificate (MCSession session, MonoTouch.Foundation.NSObject peerCert, MCPeerID peerID);
</pre>
<p>Added:</p><pre>
 	public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
 	public virtual bool DidReceiveCertificate (MCSession session, MonoTouch.Foundation.NSArray certificate, MCPeerID peerID, Action&lt;bool&gt; certificateHandler);
 	public virtual void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSObject progress);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Removed:</p><pre>
 	public static void void_objc_msgSend_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
</pre>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static float float_objc_msgSend_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static float float_objc_msgSendSuper_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static int int_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static int int_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static void RectangleF_objc_msgSend_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
 	public static void RectangleF_objc_msgSend_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
 	public static void RectangleF_objc_msgSendSuper_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoTouch.Foundation.NSRange arg6);
 	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoTouch.Foundation.NSRange arg6);
 	public static void void_objc_msgSend_Double_Double_float_float_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, float arg3, float arg4, int arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static void void_objc_msgSend_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_Double_Double_float_float_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, float arg3, float arg4, int arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static void void_objc_msgSendSuper_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.NSAttributedStringAttachmentConveniences</h3>
<pre>
public static class NSAttributedStringAttachmentConveniences {
	
	public static MonoTouch.Foundation.NSAttributedString FromTextAttachment (MonoTouch.Foundation.NSAttributedString This, NSTextAttachment attachment);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSExtendedStringDrawing</h3>
<pre>
public static class NSExtendedStringDrawing {
	
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSStringDrawingOptions options, UIStringAttributes attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static System.Drawing.RectangleF GetBoundingRect (MonoTouch.Foundation.NSString This, System.Drawing.SizeF size, MonoTouch.Foundation.NSStringDrawingOptions options, UIStringAttributes attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSStringDrawingOptions options, MonoTouch.Foundation.NSDictionary attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static System.Drawing.RectangleF WeakGetBoundingRect (MonoTouch.Foundation.NSString This, System.Drawing.SizeF size, MonoTouch.Foundation.NSStringDrawingOptions options, MonoTouch.Foundation.NSDictionary attributes, MonoTouch.Foundation.NSStringDrawingContext context);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSLayoutManager</h3>
<p>Added:</p><pre>
 	public virtual void EnumerateEnclosingRects (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSRange selectedRange, NSTextContainer textContainer, NSTextLayoutEnumerateEnclosingRects callback);
 	public virtual void EnumerateLineFragments (MonoTouch.Foundation.NSRange glyphRange, NSTextLayoutEnumerateLineFragments callback);
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSLayoutManagerDelegate</h3>
<p>Added:</p><pre>
 	
 	public virtual System.Drawing.RectangleF BoundingBoxForControlGlyph (NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, System.Drawing.RectangleF proposedRect, System.Drawing.PointF glyphPosition, uint charIndex);
 	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, MonoTouch.Foundation.NSObject textContainer, float oldSize);
 	public virtual void DidCompleteLayout (NSLayoutManager layoutManager, NSTextContainer textContainer, bool layoutFinishedFlag);
 	public virtual void DidInvalidatedLayout (NSLayoutManager sender);
 	public virtual float LineSpacingAfterGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
 	public virtual float ParagraphSpacingAfterGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
 	public virtual float ParagraphSpacingBeforeGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
 	public virtual bool ShouldBreakLineByHyphenatingBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
 	public virtual bool ShouldBreakLineByWordBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
 	public virtual uint ShouldGenerateGlyphs (NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, UIFont aFont, MonoTouch.Foundation.NSRange glyphRange);
 	public virtual NSControlCharacterAction ShouldUseAction (NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
</pre>
<h3>New Type: MonoTouch.UIKit.NSStringDrawing</h3>
<pre>
public static class NSStringDrawing {
	
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, UIStringAttributes attributes);
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, UIStringAttributes attributes);
	public static System.Drawing.SizeF GetSizeUsingAttributes (MonoTouch.Foundation.NSString This, UIStringAttributes attributes);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, MonoTouch.Foundation.NSDictionary attributes);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSDictionary attributes);
	public static System.Drawing.SizeF WeakGetSizeUsingAttributes (MonoTouch.Foundation.NSString This, MonoTouch.Foundation.NSDictionary attributes);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextLayoutEnumerateEnclosingRects</h3>
<pre>
[Serializable]
public delegate void NSTextLayoutEnumerateEnclosingRects (System.Drawing.RectangleF rect, ref bool stop);
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextLayoutEnumerateLineFragments</h3>
<pre>
[Serializable]
public delegate void NSTextLayoutEnumerateLineFragments (System.Drawing.RectangleF rect, System.Drawing.RectangleF usedRectangle, NSTextContainer textContainer, MonoTouch.Foundation.NSRange glyphRange, ref bool stop);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAccessibility</h3>
<p>Added:</p><pre>
 	public static void RequestGuidedAccessSession (bool enable, Action&lt;bool&gt; completionHandler);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString BackgroundRefreshStatusDidChangeNotification {
 		get;
 	}
 	public virtual UIBackgroundRefreshStatus BackgroundRefreshStatus {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h3>New Type: MonoTouch.UIKit.UIBackgroundRefreshStatus</h3>
<pre>
[Serializable]
public enum UIBackgroundRefreshStatus {
	Restricted,
	Denied,
	Available
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioningDelegate</h3>
<pre>
public class UIBarPositioningDelegate : MonoTouch.Foundation.NSObject {
	
	public UIBarPositioningDelegate ();
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIBarPositioningDelegate (IntPtr handle);
	
	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewController</h3>
<p>Added:</p><pre>
 	public virtual UICollectionViewLayout Layout {
 		get;
 	}
 	public virtual bool UseLayoutToLayoutNavigationTransitions {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewFlowLayoutInvalidationContext</h3>
<pre>
public class UICollectionViewFlowLayoutInvalidationContext : UICollectionViewLayoutInvalidationContext {
	
	public UICollectionViewFlowLayoutInvalidationContext ();
	public UICollectionViewFlowLayoutInvalidationContext (MonoTouch.Foundation.NSCoder coder);
	public UICollectionViewFlowLayoutInvalidationContext (MonoTouch.Foundation.NSObjectFlag t);
	public UICollectionViewFlowLayoutInvalidationContext (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool InvalidateFlowLayoutAttributes {
		get;
		set;
	}
	public virtual bool InvalidateFlowLayoutDelegateMetrics {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutInvalidationContext</h3>
<p>Added:</p><pre>
 	public virtual bool InvalidateEverything {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIColor</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS 7")]
	public static UIColor ScrollViewTexturedBackgroundColor {
 	[Obsolete("Deprecated in iOS 7")]
	public static UIColor UnderPageBackgroundColor {
 	[Obsolete("Deprecated in iOS 7")]
	public static UIColor ViewFlipsideBackgroundColor {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor ScrollViewTexturedBackgroundColor {
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor UnderPageBackgroundColor {
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor ViewFlipsideBackgroundColor {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicAnimator</h3>
<p>Added:</p><pre>
 	public virtual void UpdateItemFromCurrentState (MonoTouch.Foundation.NSObject uiDynamicItem);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFont</h3>
<p>Added:</p><pre>
 	public static UIFont FromDescriptor (UIFontDescriptor descriptor, float pointSize);
 	public static UIFont PreferredFontForTextStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	public virtual UIFontDescriptor GetFontDescriptor ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontDescriptor</h3>
<p>Removed:</p><pre>
 	public static UIFontDescriptor PreferredForStyle (MonoTouch.Foundation.NSString style);
 	public static MonoTouch.Foundation.NSString TextStyleBody {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleCaption1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleCaption2 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleFootnote {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleHeadline1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleHeadline2 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleSubheadline1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleSubheadline2 {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public static UIFontDescriptor PreferredForStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontDescriptorSymbolicTraits</h3>
<p>Added:</p><pre>
 	LooseLeading,
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontTextStyle</h3>
<pre>
public static class UIFontTextStyle {
	
	public static MonoTouch.Foundation.NSString Body {
		get;
	}
	public static MonoTouch.Foundation.NSString Caption1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Caption2 {
		get;
	}
	public static MonoTouch.Foundation.NSString Footnote {
		get;
	}
	public static MonoTouch.Foundation.NSString Headline1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Headline2 {
		get;
	}
	public static MonoTouch.Foundation.NSString Subheadline1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Subheadline2 {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIGuidedAccessRestriction</h3>
<pre>
public static class UIGuidedAccessRestriction {
	
	public static UIGuidedAccessRestrictionState GetState (string restrictionIdentifier);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIGuidedAccessRestrictionState</h3>
<pre>
[Serializable]
public enum UIGuidedAccessRestrictionState {
	Allow,
	Deny
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerController</h3>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerControllerDelegate</h3>
<p>Added:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIKeyboardAppearance</h3>
<p>Removed:</p><pre>
 	Alert
</pre>
<p>Added:</p><pre>
 	Alert,
 	Dark,
 	Light
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBarDelegate</h3>
<p>Removed:</p><pre>
 public class UINavigationBarDelegate : MonoTouch.Foundation.NSObject {
 	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 public class UINavigationBarDelegate : UIBarPositioningDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationController</h3>
<p>Added:</p><pre>
 	public virtual UIGestureRecognizer InteractivePopGestureRecognizer {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverArrowDirection</h3>
<p>Removed:</p><pre>
 [Obsolete]
public enum UIPopoverArrowDirection : uint {
</pre>
<p>Added:</p><pre>
 public enum UIPopoverArrowDirection : uint {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverController</h3>
<p>Added:</p><pre>
 	public virtual void PresentPopover (System.Drawing.RectangleF rect, UIView targetView, UIPopoverPreferredPresentationDirection preferredPresentationDirections);
 	public virtual void PresentPopover (UIBarButtonItem barButtonItem);
 	public event EventHandler&lt;UIPopoverControllerRepositionEventArgs&gt; WillReposition;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual void WillReposition (UIPopoverController popoverController, ref System.Drawing.RectangleF rect, ref UIView view);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPopoverControllerRepositionEventArgs</h3>
<pre>
public class UIPopoverControllerRepositionEventArgs : EventArgs {
	
	public UIPopoverControllerRepositionEventArgs (System.Drawing.RectangleF rect, UIView view);
	
	public System.Drawing.RectangleF Rect {
		get;
		set;
	}
	public UIView View {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionController</h3>
<p>Added:</p><pre>
 	public Func&lt;UIPrintInteractionController,UIPrintPaper,float&gt; CutLengthForPaper {
 		get;
 		set;
 	}
 	public virtual bool ShowsNumberOfCopies {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual float CutLengthForPaper (UIPrintInteractionController printInteractionController, UIPrintPaper paper);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScreen</h3>
<p>Removed:</p><pre>
 	public virtual UIView Snapshot ();
</pre>
<p>Added:</p><pre>
 	public virtual UIView SnapshotView ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Added:</p><pre>
 	public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
 	public virtual UIImage BackgroundImageForBarPosition (UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
 	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 	public System.Func&lt;MonoTouch.Foundation.NSObject,UIBarPosition&gt; GetPositionForBar {
 		get;
 		set;
 	}
 		public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
 		public virtual UIImage BackgroundImageForBarPosition (UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
 		public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBarDelegate</h3>
<p>Removed:</p><pre>
 public class UISearchBarDelegate : MonoTouch.Foundation.NSObject {
 	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 public class UISearchBarDelegate : UIBarPositioningDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISegmentedControl</h3>
<p>Removed:</p><pre>
 	[Obsolete("Obsoleted with iOS7")]
	public virtual UISegmentedControlStyle ControlStyle {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual UISegmentedControlStyle ControlStyle {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarItem</h3>
<p>Removed:</p><pre>
 	public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);
 	public virtual UIImage FinishedSelectedImage {
 	public virtual UIImage FinishedUnselectedImage {
</pre>
<p>Added:</p><pre>
 	public UITabBarItem (string title, UIImage image, UIImage selectedImage);
 	[Obsolete("Deprecated in iOS7")]
	public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);
 	[Obsolete("Deprecated in iOS7")]
	public virtual UIImage FinishedSelectedImage {
 	[Obsolete("Deprecated in iOS7")]
	public virtual UIImage FinishedUnselectedImage {
 	public virtual UIImage SelectedImage {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets SeparatorInset {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCell</h3>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets SeparatorInset {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextInputMode</h3>
<p>Removed:</p><pre>
 	[Obsolete("ios7: Obsoleted in ios7")]
	public static UITextInputMode CurrentInputMode {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in IOS7")]
	public static UITextInputMode CurrentInputMode {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbar</h3>
<p>Added:</p><pre>
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 	public UIToolbarDelegate Delegate {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
 		get;
 		set;
 	}
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>New Type: MonoTouch.UIKit.UIToolbarDelegate</h3>
<pre>
public class UIToolbarDelegate : UIBarPositioningDelegate {
	
	public UIToolbarDelegate ();
	public UIToolbarDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIToolbarDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIToolbarDelegate (IntPtr handle);
	
	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorController</h3>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorControllerDelegate</h3>
<p>Added:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 	public virtual UIView ResizableSnapshot (System.Drawing.RectangleF rect, UIEdgeInsets capInsets);
 	public virtual UIView Snapshot ();
</pre>
<p>Added:</p><pre>
 	public static void AnimateNotify (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completion);
 	public virtual bool DrawViewHierarchy (System.Drawing.RectangleF rect);
 	public virtual UIView ResizableSnapshotView (System.Drawing.RectangleF rect, UIEdgeInsets capInsets);
 	public virtual UIView SnapshotView ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	[Obsolete("Obsoleted with iOS7")]
	public virtual bool WantsFullScreenLayout {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject BottomLayoutGuide {
 		get;
 	}
 	public virtual bool ModalPresentationCapturesStatusBarAppearance {
 		get;
 		set;
 	}
 	public virtual UIStatusBarAnimation PreferredStatusBarUpdateAnimation {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSObject TopLayoutGuide {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual bool WantsFullScreenLayout {
</pre>
<h2>Namespace: MonoTouch.iAd</h2>
<h3>New Type: MonoTouch.iAd.ADInterstitialPresentationPolicy</h3>
<pre>
[Serializable]
public enum ADInterstitialPresentationPolicy {
	None,
	Automatic,
	Manual
}
</pre>
<h3>New Type: MonoTouch.iAd.IAdAdditions</h3>
<pre>
public static class IAdAdditions {
	
	public static bool DisplayingBannerAd (MonoTouch.UIKit.UIViewController This);
	public static bool GetCanDisplayBannerAds (MonoTouch.UIKit.UIViewController This);
	public static ADInterstitialPresentationPolicy GetInterstitialPresentationPolicy (MonoTouch.UIKit.UIViewController This);
	public static MonoTouch.UIKit.UIView GetOriginalContentView (MonoTouch.UIKit.UIViewController This);
	public static void PrepareInterstitialAds (MonoTouch.UIKit.UIViewController This);
	public static bool PresentingFullScreenAd (MonoTouch.UIKit.UIViewController This);
	public static bool RequestInterstitialAdPresentation (MonoTouch.UIKit.UIViewController This);
	public static void SetCanDisplayBannerAds (MonoTouch.UIKit.UIViewController This, bool value);
	public static void SetInterstitialPresentationPolicy (MonoTouch.UIKit.UIViewController This, ADInterstitialPresentationPolicy policy);
	public static bool ShouldPresentInterstitialAd (MonoTouch.UIKit.UIViewController This);
}
</pre>
<h3>New Type: MonoTouch.iAd.IAdPreroll</h3>
<pre>
public static class IAdPreroll {
	
	public static void PlayPrerollAd (MonoTouch.MediaPlayer.MPMoviePlayerController This, PlayPrerollAdCompletionHandler completionHandler);
	public static void PreparePrerollAds (MonoTouch.MediaPlayer.MPMoviePlayerController This);
}
</pre>
<h3>New Type: MonoTouch.iAd.PlayPrerollAdCompletionHandler</h3>
<pre>
[Serializable]
public delegate void PlayPrerollAdCompletionHandler (MonoTouch.Foundation.NSError error);
</pre>
</body>
</html>
