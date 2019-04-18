---
id: DC27A8F7-D20D-4091-8B67-45D2794ED67B
title: "From 6.9.4 to 6.9.5"
---

<html><head><title>Comparison between monotouch-6.9.4.40.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.4";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.5";
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccount</h3>
<p>Added:</p><pre>
 	public virtual string UserFullName {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSession</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public static void AddListener (AudioSessionProperty property, PropertyListener listener);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public static AudioSessionErrors AddListener (AudioSessionProperty property, PropertyListener listener);
 	public event EventHandler&lt;bool&gt; AudioInputBecameAvailable;
 	public event EventHandler&lt;float&gt; CurrentHardwareOutputVolumeChanged;
 	public event EventHandler&lt;bool&gt; InputGainBecameAvailable;
 	public event EventHandler&lt;float&gt; InputGainScalarChanged;
 	public event EventHandler&lt;AccessoryInfo[]&gt; InputSourcesChanged;
 	public event EventHandler&lt;AccessoryInfo[]&gt; OutputDestinationsChanged;
 	public event EventHandler&lt;bool&gt; ServerDied;
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSessionRouteChangeReason</h3>
<p>Removed:</p><pre>
 	NoSuitableRouteForCategory
</pre>
<p>Added:</p><pre>
 	NoSuitableRouteForCategory,
 	RouteConfigurationChange
</pre>
<h3>New Type: MonoTouch.AudioToolbox.InputSourceInfo</h3>
<pre>
public class InputSourceInfo {
	
	public InputSourceInfo ();
	
	public string Description {
		get;
	}
	public int ID {
		get;
	}
}
</pre>
<h3>Type Removed: MonoTouch.CoreBluetooth.CBPeripheralAuthorizationStatus</h3>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void ModifiedServices (CBPeripheral peripheral, MonoTouch.Foundation.NSArray services);
</pre>
<p>Added:</p><pre>
 	public virtual void ModifiedServices (CBPeripheral peripheral, CBService[] services);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<p>Removed:</p><pre>
 	public static CBPeripheralAuthorizationStatus AuthorizationStatus {
</pre>
<p>Added:</p><pre>
 	public static CBPeripheralManagerAuthorizationStatus AuthorizationStatus {
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerAuthorizationStatus</h3>
<pre>
[Serializable]
public enum CBPeripheralManagerAuthorizationStatus {
	NotDetermined,
	Restricted,
	Denied,
	Authorized
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralServicesEventArgs</h3>
<p>Removed:</p><pre>
 	public CBPeripheralServicesEventArgs (MonoTouch.Foundation.NSArray services);
 	public MonoTouch.Foundation.NSArray Services {
</pre>
<p>Added:</p><pre>
 	public CBPeripheralServicesEventArgs (CBService[] services);
 	public CBService[] Services {
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousPeerTokenOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousTransitionTypeKey {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.CoreData.NSPersistentStoreUbiquitousTransitionType</h3>
<pre>
[Serializable]
public enum NSPersistentStoreUbiquitousTransitionType {
	AccountAdded,
	AccountRemoved,
	ContentRemoved,
	InitialImportCompleted
}
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.CFStream</h3>
<p>Added:</p><pre>
 	public DispatchQueue ReadDispatchQueue {
 		get;
 		set;
 	}
 	public DispatchQueue WriteDispatchQueue {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.CFUrl</h3>
<p>Added:</p><pre>
 	public bool IsFileReference {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchQueue</h3>
<p>Removed:</p><pre>
 public class DispatchQueue : DispatchObject {
</pre>
<p>Added:</p><pre>
 public sealed class DispatchQueue : DispatchObject {
 	public override bool Equals (object other);
 	public override int GetHashCode ();
 	public static bool operator == (DispatchQueue left, DispatchQueue right);
 	public static bool operator != (DispatchQueue left, DispatchQueue right);
 	
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSArray</h3>
<p>Added:</p><pre>
 	public static NSArray FromObjects (int count, params object [] items);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Removed:</p><pre>
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary documentAttributes, out NSError error);
</pre>
<p>Added:</p><pre>
 	public NSAttributedString (NSUrl url, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSData GetDataFromRange (NSRange range, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public virtual NSData GetDataFromRange (NSRange range, NSDictionary attributes, ref NSError error);
 	public NSFileWrapper GetFileWrapperFromRange (NSRange range, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public virtual NSFileWrapper GetFileWrapperFromRange (NSRange range, NSDictionary attributes, ref NSError error);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedStringDocumentAttributes</h3>
<p>Added:</p><pre>
 	public NSDictionary WeakDefaultAttributes {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFileManager</h3>
<p>Added:</p><pre>
 	public virtual NSUrl GetContainerUrl (string securityApplicationGroupIdentifier);
</pre>
<h3>New Type: MonoTouch.Foundation.NSInvocation</h3>
<pre>
public class NSInvocation : NSObject {
	
	public NSInvocation (NSCoder coder);
	public NSInvocation (NSObjectFlag t);
	public NSInvocation (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual void Invoke ();
	public virtual void Invoke (NSObject target);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSMethodSignature MethodSignature {
		get;
	}
	public virtual MonoTouch.ObjCRuntime.Selector Selector {
		get;
		set;
	}
	public virtual NSObject Target {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPort</h3>
<pre>
public class NSMachPort : NSPort {
	
	public NSMachPort ();
	public NSMachPort (NSCoder coder);
	public NSMachPort (NSObjectFlag t);
	public NSMachPort (IntPtr handle);
	
	public static NSPort FromMachPort (uint port);
	public static NSPort FromMachPort (uint port, NSMachPortRights options);
	protected override void Dispose (bool disposing);
	public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString mode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString mode);
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSMachPortDelegate Delegate {
		get;
		set;
	}
	public virtual uint MachPort {
		get;
	}
	public virtual NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPortDelegate</h3>
<pre>
public class NSMachPortDelegate : NSPortDelegate {
	
	public NSMachPortDelegate ();
	public NSMachPortDelegate (NSCoder coder);
	public NSMachPortDelegate (NSObjectFlag t);
	public NSMachPortDelegate (IntPtr handle);
	
	public virtual void MachMessageReceived (IntPtr msgHeader);
	public override void MessageReceived (NSPortMessage message);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPortRights</h3>
<pre>
[Serializable]
[Flags]
public enum NSMachPortRights {
	None,
	SendRight,
	ReceiveRight
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMethodSignature</h3>
<pre>
public class NSMethodSignature : NSObject {
	
	public NSMethodSignature (NSCoder coder);
	public NSMethodSignature (NSObjectFlag t);
	public NSMethodSignature (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint FrameLength {
		get;
	}
	public virtual bool IsOneway {
		get;
	}
	public virtual uint MethodReturnLength {
		get;
	}
	public virtual uint NumberOfArguments {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h3>
<p>Added:</p><pre>
 	public bool ReadFromData (NSData data, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);
 	public virtual bool ReadFromData (NSData data, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);
 	public bool ReadFromFile (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);
 	public virtual bool ReadFromFile (NSUrl url, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Added:</p><pre>
 	public NSObject Autorelease ();
 	public void Release ();
 	public NSObject Retain ();
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSOrderedSet</h3>
<p>Added:</p><pre>
 	public override bool Equals (object other);
 	public override int GetHashCode ();
</pre>
<h3>New Type: MonoTouch.Foundation.NSPort</h3>
<pre>
public class NSPort : NSObject {
	
	public NSPort (NSCoder coder);
	public NSPort (NSObjectFlag t);
	public NSPort (IntPtr handle);
	
	public static NSPort Create ();
	protected override void Dispose (bool disposing);
	public virtual void Invalidate ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSPortDelegate Delegate {
		get;
		set;
	}
	public virtual bool IsValid {
		get;
	}
	public virtual NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSPortDelegate</h3>
<pre>
public class NSPortDelegate : NSObject {
	
	public NSPortDelegate ();
	public NSPortDelegate (NSCoder coder);
	public NSPortDelegate (NSObjectFlag t);
	public NSPortDelegate (IntPtr handle);
	
	public virtual void MessageReceived (NSPortMessage message);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSPortMessage</h3>
<pre>
public class NSPortMessage : NSObject {
	
	public NSPortMessage ();
	public NSPortMessage (NSCoder coder);
	public NSPortMessage (NSObjectFlag t);
	public NSPortMessage (IntPtr handle);
	public NSPortMessage (NSPort sendPort, NSPort recvPort, NSArray components);
	
	protected override void Dispose (bool disposing);
	public virtual bool SendBefore (NSDate date);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSArray Components {
		get;
	}
	public virtual uint MsgId {
		get;
		set;
	}
	public virtual NSPort ReceivePort {
		get;
	}
	public virtual NSPort SendPort {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSProgress</h3>
<pre>
public class NSProgress : NSObject {
	
	public NSProgress ();
	public NSProgress (NSCoder coder);
	public NSProgress (NSObjectFlag t);
	public NSProgress (IntPtr handle);
	public NSProgress (NSProgress parentProgress, NSDictionary userInfo);
	
	public static NSProgress FromTotalUnitCount (long unitCount);
	public virtual void BecomeCurrent (long pendingUnitCount);
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void Pause ();
	public virtual void ResignCurrent ();
	public virtual void SetCancellationHandler (NSAction handler);
	public virtual void SetPauseHandler (NSAction handler);
	public virtual void SetUserInfo (NSObject obj, NSString key);
	
	public static NSProgress CurrentProgress {
		get;
	}
	public static NSString EstimatedTimeRemainingKey {
		get;
	}
	public static NSString FileCompletedCountKey {
		get;
	}
	public static NSString FileOperationKindCopying {
		get;
	}
	public static NSString FileOperationKindDecompressingAfterDownloading {
		get;
	}
	public static NSString FileOperationKindDownloading {
		get;
	}
	public static NSString FileOperationKindKey {
		get;
	}
	public static NSString FileOperationKindReceiving {
		get;
	}
	public static NSString FileTotalCountKey {
		get;
	}
	public static NSString FileURLKey {
		get;
	}
	public static NSString KindFile {
		get;
	}
	public static NSString ThroughputKey {
		get;
	}
	public virtual bool Cancellable {
		get;
		set;
	}
	public virtual bool Cancelled {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual long CompletedUnitCount {
		get;
		set;
	}
	public virtual double FractionCompleted {
		get;
	}
	public virtual bool Indeterminate {
		get;
	}
	public virtual NSString Kind {
		get;
		set;
	}
	public virtual string LocalizedAdditionalDescription {
		get;
		set;
	}
	public virtual string LocalizedDescription {
		get;
		set;
	}
	public virtual bool Pausable {
		get;
		set;
	}
	public virtual bool Paused {
		get;
	}
	public virtual long TotalUnitCount {
		get;
		set;
	}
	public virtual NSDictionary UserInfo {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSTextWritingDirection</h3>
<pre>
[Serializable]
[Flags]
public enum NSTextWritingDirection {
	Embedding,
	Override
}
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKGameCenterViewController</h3>
<p>Removed:</p><pre>
 	public virtual string LeaderboardCategory {
 	public virtual GKLeaderboardTimeScope LeaderboardTimeScope {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use LeaderboardIdentifier instead")]
	public virtual string LeaderboardCategory {
 	public virtual string LeaderboardIdentifier {
 		get;
 		set;
 	}
 	[Obsolete("This class no longer support Leaderboard Time Scopes, will always default to AllTime")]
	public virtual GKLeaderboardTimeScope LeaderboardTimeScope {
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of RendererForOverlay")]
	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	[Obsolete("Deprecated in iOS7 in favor of MapView::RendererForOverlay")]
	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Starting with iOS 7 it is recommnended to use RendererForOverlay")]
	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	[Obsolete("Since iOS 7 it is recommended that you use DidAddOverlayRenderers")]
	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of MapView::RendererForOverlay")]
	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	[Obsolete("Deprecated in iOS7 in favor of MapView::DidAddOverlayRenderers")]
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Since iOS 7 it is recommended that you use DidAddOverlayRenderers")]
	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	[Obsolete("Since iOS 7 it is recommnended that you use GetRendererForOverlay")]
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<h2>Namespace: MonoTouch.MobileCoreServices</h2>
<h3>Type Changed: MonoTouch.MobileCoreServices.UTType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString PICT;
</pre>
<h2>Namespace: MonoTouch.MultipeerConnectivity</h2>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCError</h3>
<p>Removed:</p><pre>
 	Cancelled
</pre>
<p>Added:</p><pre>
 	Cancelled,
 	Unavailable
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSessionDelegate</h3>
<p>Removed:</p><pre>
 public class MCSessionDelegate : MonoTouch.Foundation.NSObject {
 	public virtual void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);
 	public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
 	public virtual void DidReceiveData (MCSession session, MonoTouch.Foundation.NSData data, MCPeerID peerID);
 	public virtual void DidReceiveStream (MCSession session, MonoTouch.Foundation.NSInputStream stream, string streamName, MCPeerID peerID);
 	public virtual void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSObject progress);
</pre>
<p>Added:</p><pre>
 public abstract class MCSessionDelegate : MonoTouch.Foundation.NSObject {
 	public abstract void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);
 	public abstract void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
 	public abstract void DidReceiveData (MCSession session, MonoTouch.Foundation.NSData data, MCPeerID peerID);
 	public abstract void DidReceiveStream (MCSession session, MonoTouch.Foundation.NSInputStream stream, string streamName, MCPeerID peerID);
 	public abstract void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSProgress progress);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Removed:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
</pre>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static bool bool_objc_msgSendSuper_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UIOffset_IntPtr_UIOffset (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, IntPtr arg3, MonoTouch.UIKit.UIOffset arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UIOffset_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_bool_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2, MonoTouch.UIKit.UIEdgeInsets arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIOffset_IntPtr_UIOffset (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, IntPtr arg3, MonoTouch.UIKit.UIOffset arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIOffset_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_bool_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2, MonoTouch.UIKit.UIEdgeInsets arg3);
 	public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void UIOffset_objc_msgSend_stret_IntPtr (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void UIOffset_objc_msgSendSuper_stret_IntPtr (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void void_objc_msgSend_UIOffset_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_UIOffset_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, IntPtr arg2);
</pre>
<h2>Namespace: MonoTouch.Security</h2>
<h3>Type Changed: MonoTouch.Security.SecRecord</h3>
<p>Added:</p><pre>
 	public bool Synchronizable {
 		get;
 		set;
 	}
 	public bool SynchronizableAny {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Security.SecStatusCode</h3>
<p>Removed:</p><pre>
 	AuthFailed,
 	Decode
</pre>
<p>Added:</p><pre>
 	IO,
 	OpWr,
 	UserCanceled,
 	BadReq,
 	InternalComponent,
 	Decode,
 	AuthFailed
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.NSLayoutManagerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, MonoTouch.Foundation.NSObject textContainer, float oldSize);
</pre>
<p>Added:</p><pre>
 	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, float oldSize);
</pre>
<h3>New Type: MonoTouch.UIKit.NSMutableAttributedStringKitAdditions</h3>
<pre>
public static class NSMutableAttributedStringKitAdditions {
	
	public static void FixAttributesInRange (MonoTouch.Foundation.NSMutableAttributedString This, MonoTouch.Foundation.NSRange range);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString UserDidTakeScreenshotNotification {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveUserDidTakeScreenshot (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAttachmentBehavior</h3>
<p>Removed:</p><pre>
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF point, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF point, MonoTouch.Foundation.NSObject attachedToItem, System.Drawing.PointF attachedPoint);
</pre>
<p>Added:</p><pre>
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, UIOffset offset, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, UIOffset offsetFromCenter, MonoTouch.Foundation.NSObject attachedToItem, UIOffset attachOffsetFromCenter);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewTransitionLayout</h3>
<p>Added:</p><pre>
 	public virtual float TransitionProgress {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicAnimator</h3>
<p>Removed:</p><pre>
 	public virtual void UpdateItemFromCurrentState (MonoTouch.Foundation.NSObject uiDynamicItem);
</pre>
<p>Added:</p><pre>
 	public virtual void UpdateItemUsingCurrentState (MonoTouch.Foundation.NSObject uiDynamicItem);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicBehavior</h3>
<p>Added:</p><pre>
 	public virtual void WillMoveToAnimator (UIDynamicAnimator targetAnimator);
 	public virtual UIDynamicAnimator DynamicAnimator {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontAttributes</h3>
<p>Removed:</p><pre>
 	public MonoTouch.Foundation.NSDictionary[] FeatureSettings {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public MonoTouch.Foundation.NSDictionary[] WeakFeatureSettings {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGravityBehavior</h3>
<p>Removed:</p><pre>
 	public virtual void SetComponents (float xComponent, float yComponent);
 	public override IntPtr ClassHandle {
 	public virtual MonoTouch.Foundation.NSObject[] Items {
 	public virtual float XComponent {
 	public virtual float YComponent {
</pre>
<p>Added:</p><pre>
 	public virtual void SetAngleAndMagnitude (float angle, float magnitude);
 	public virtual float Angle {
 		set;
 	public override IntPtr ClassHandle {
 	public virtual System.Drawing.SizeF GravityDirection {
 	public virtual MonoTouch.Foundation.NSObject[] Items {
 		get;
 	}
 	public virtual float Magnitude {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverController</h3>
<p>Added:</p><pre>
 	public virtual UIColor BackgroundColor {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPushBehavior</h3>
<p>Removed:</p><pre>
 	public virtual System.Drawing.PointF GetTargetPoint (UIDynamicItem item);
 	public virtual void SetComponents (float x, float y);
 	public virtual void SetTargetPoint (System.Drawing.PointF point, UIDynamicItem item);
 	public virtual float XComponent {
 		get;
 		set;
 	}
 	public virtual float YComponent {
</pre>
<p>Added:</p><pre>
 	public virtual UIOffset GetTargetOffsetFromCenter (UIDynamicItem item);
 	public virtual void SetTargetOffset (UIOffset offset, UIDynamicItem item);
 	public virtual System.Drawing.SizeF PushDirection {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScreen</h3>
<p>Removed:</p><pre>
 	public virtual UIView SnapshotView ();
</pre>
<p>Added:</p><pre>
 	public virtual UIView SnapshotView (bool afterScreenUpdates);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScreenEdgePanGestureRecognizer</h3>
<p>Added:</p><pre>
 	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSAction action);
 	public UIScreenEdgePanGestureRecognizer (Action&lt;UIScreenEdgePanGestureRecognizer&gt; action);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 	public virtual bool DrawViewHierarchy (System.Drawing.RectangleF rect);
 	public virtual UIView ResizableSnapshotView (System.Drawing.RectangleF rect, UIEdgeInsets capInsets);
 	public virtual UIView SnapshotView ();
</pre>
<p>Added:</p><pre>
 	public virtual bool DrawViewHierarchy (System.Drawing.RectangleF rect, bool afterScreenUpdates);
 	public virtual UIView ResizableSnapshotView (System.Drawing.RectangleF rect, bool afterScreenUpdates, UIEdgeInsets capInsets);
 	public virtual UIView SnapshotView (bool afterScreenUpdates);
</pre>
<h2>Namespace: MonoTouch.iAd</h2>
<h3>Type Changed: MonoTouch.iAd.ADInterstitialAd</h3>
<p>Removed:</p><pre>
 	public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Obsolete in iOS 7. Use extension method UIViewController.requestInterstitialAdPresentation instead")]
	public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
</pre>
</body>
</html>
