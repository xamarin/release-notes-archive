---
id: C3AC060A-B5B6-42A6-8307-5AD43EB336B5
title: "From 6.9.3 to 6.9.4"
---

<html><head><title>Comparison between monotouch-6.9.3.dll and monotouch-6.9.4.html</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.4";
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchObject</h3>
<p>Added:</p><pre>
 	public void SetTargetQueue (DispatchQueue queue);
</pre>
<h2>Namespace: MonoTouch.CoreTelephony</h2>
<h3>Type Changed: MonoTouch.CoreTelephony.CTSubscriber</h3>
<p>Removed:</p><pre>
 	public virtual void AuthenticateWithInfo (MonoTouch.Foundation.NSDictionary info, SimAuthenticationCallback callback);
</pre>
<h3>Type Removed: MonoTouch.CoreTelephony.CTSubscriberSimAuthentication</h3>
<h3>Type Removed: MonoTouch.CoreTelephony.CTSubscriberSimAuthenticationType</h3>
<h3>Type Changed: MonoTouch.CoreTelephony.CTTelephonyNetworkInfo</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString CellIdDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SignalStrengthDidChangeNotification {
 		get;
 	}
 	public virtual string CellId {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary SignalStrength {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveCellIdDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveSignalStrengthDidChange (EventHandler&lt;SignalStrengthChangedEventArgs&gt; handler);
 	}
</pre>
<h3>Type Removed: MonoTouch.CoreTelephony.SignalStrengthChangedEventArgs</h3>
<h3>Type Removed: MonoTouch.CoreTelephony.SimAuthenticationCallback</h3>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKSource</h3>
<p>Removed:</p><pre>
 	public static EKSource Create (EKEventStore eventStore);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSStringDrawingContext</h3>
<p>Removed:</p><pre>
 	public virtual float ActualTrackingAdjustment {
 	public virtual float MinimumTrackingAdjustment {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual float ActualTrackingAdjustment {
 	[Obsolete("Deprecated in iOS7")]
	public virtual float MinimumTrackingAdjustment {
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKDirections</h3>
<p>Added:</p><pre>
 	public virtual void CalculateETA (MKETAHandler completionHandler);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKDirectionsRequest</h3>
<p>Added:</p><pre>
 		set;
 		set;
</pre>
<h3>New Type: MonoTouch.MapKit.MKETAHandler</h3>
<pre>
[Serializable]
public delegate void MKETAHandler (MKETAResponse response, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.MapKit.MKETAResponse</h3>
<pre>
public class MKETAResponse : MonoTouch.Foundation.NSObject {
	
	public MKETAResponse ();
	public MKETAResponse (MonoTouch.Foundation.NSCoder coder);
	public MKETAResponse (MonoTouch.Foundation.NSObjectFlag t);
	public MKETAResponse (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKMapItem Destination {
		get;
	}
	public virtual double ExpectedTravelTime {
		get;
	}
	public virtual MKMapItem Source {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapSnapshotOptions</h3>
<p>Added:</p><pre>
 	public virtual bool ShowsBuildings {
 		get;
 		set;
 	}
 	public virtual bool ShowsPointsOfInterest {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Removed:</p><pre>
 	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of RendererForOverlay")]
	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual bool ShowsBuildings {
 		get;
 		set;
 	}
 	public virtual bool ShowsPointsOfInterest {
 		get;
 		set;
 	}
 	[Obsolete("Deprecated in iOS7 in favor of MapView::RendererForOverlay")]
	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of MapView::RendererForOverlay")]
	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	[Obsolete("Deprecated in iOS7 in favor of MapView::DidAddOverlayRenderers")]
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<h2>Namespace: MonoTouch.MultipeerConnectivity</h2>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistantDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidDismissInvitaiton (MCAdvertiserAssistant advertiserAssistant);
</pre>
<p>Added:</p><pre>
 	public virtual void DidDismissInvitation (MCAdvertiserAssistant advertiserAssistant);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Removed:</p><pre>
 	public static void void_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
</pre>
<p>Added:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_int_float_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_float_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3);
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>Type Changed: MonoTouch.PassKit.PKPassLibraryAddPassesStatus</h3>
<p>Removed:</p><pre>
 	ShouldReviewPasses
</pre>
<p>Added:</p><pre>
 	ShouldReviewPasses,
 	DidCancelAddPasses
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.NSMutableParagraphStyle</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	
 	public override float DefaultTabInterval {
 		get;
 		set;
 	}
 	public override NSTextTab TabStops {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSParagraphStyle</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	public virtual float DefaultTabInterval {
 		get;
 		set;
 	}
 	public virtual NSTextTab TabStops {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextTab</h3>
<pre>
public class NSTextTab : MonoTouch.Foundation.NSObject {
	
	public NSTextTab ();
	public NSTextTab (MonoTouch.Foundation.NSCoder coder);
	public NSTextTab (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextTab (IntPtr handle);
	public NSTextTab (UITextAlignment alignment, float location, MonoTouch.Foundation.NSDictionary options);
	
	public static MonoTouch.Foundation.NSCharacterSet GetColumnTerminators (MonoTouch.Foundation.NSLocale locale);
	protected override void Dispose (bool disposing);
	
	public static MonoTouch.Foundation.NSString ColumnTerminatorsAttributeName {
		get;
	}
	public virtual UITextAlignment Alignment {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Location {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary Options {
		get;
	}
}
</pre>
<h3>Type Removed: MonoTouch.UIKit.UIExtendedEdge</h3>
<h3>Type Changed: MonoTouch.UIKit.UIFontTextStyle</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString Headline1 {
 	public static MonoTouch.Foundation.NSString Headline2 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Subheadline1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Subheadline2 {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Headline {
 	public static MonoTouch.Foundation.NSString Subheadline {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGestureRecognizer</h3>
<p>Added:</p><pre>
 	public UIGesturesProbe ShouldBeRequiredToFailBy {
 		get;
 		set;
 	}
 	public UIGesturesProbe ShouldRequireFailureOf {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate</h3>
<p>Added:</p><pre>
 	public virtual bool ShouldBeRequiredToFailBy (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
 	public virtual bool ShouldRequireFailureOf (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
</pre>
<h3>New Type: MonoTouch.UIKit.UIInputView</h3>
<pre>
public class UIInputView : UIView {
	
	public UIInputView ();
	public UIInputView (MonoTouch.Foundation.NSCoder coder);
	public UIInputView (MonoTouch.Foundation.NSObjectFlag t);
	public UIInputView (IntPtr handle);
	public UIInputView (System.Drawing.RectangleF frame, UIInputViewStyle inputViewStyle);
	
	public static UIInputViewAppearance AppearanceWhenContainedIn (params Type [] containers);
	public static UIInputViewAppearance GetAppearance<t> ();
	
	public static UIInputViewAppearance Appearance {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIInputViewStyle InputViewStyle {
		get;
	}
	
	public class UIInputViewAppearance : UIViewAppearance {
	}
}
</t></pre>
<h3>New Type: MonoTouch.UIKit.UIInputViewStyle</h3>
<pre>
[Serializable]
public enum UIInputViewStyle {
	Default,
	Keyboard
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UILabel</h3>
<p>Removed:</p><pre>
 	public virtual bool AdjustsLetterSpacingToFitWidth {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of NSKernAttributeName")]
	public virtual bool AdjustsLetterSpacingToFitWidth {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverController</h3>
<p>Removed:</p><pre>
 	public virtual void PresentPopover (System.Drawing.RectangleF rect, UIView targetView, UIPopoverPreferredPresentationDirection preferredPresentationDirections);
 	public virtual void PresentPopover (UIBarButtonItem barButtonItem);
</pre>
<h3>Type Removed: MonoTouch.UIKit.UIPopoverPreferredPresentationDirection</h3>
<h3>New Type: MonoTouch.UIKit.UIRectEdge</h3>
<pre>
[Serializable]
public enum UIRectEdge {
	None,
	Top,
	Left,
	Bottom,
	Right,
	All
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIScreenEdgePanGestureRecognizer</h3>
<pre>
public class UIScreenEdgePanGestureRecognizer : UIPanGestureRecognizer {
	
	public UIScreenEdgePanGestureRecognizer ();
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSCoder coder);
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSObjectFlag t);
	public UIScreenEdgePanGestureRecognizer (IntPtr handle);
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIRectEdge Edges {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Added:</p><pre>
 	public virtual UISearchBarStyle SearchBarStyle {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UISearchBarStyle</h3>
<pre>
[Serializable]
public enum UISearchBarStyle : uint {
	Default,
	Prominent,
	Minimal
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBar</h3>
<p>Removed:</p><pre>
 	public virtual UIImage DividerImageForLeftItemState (UIControlState leftItemState, UIControlState rightItemState);
 	public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftItemState, UIControlState rightItemState);
 		public virtual UIImage DividerImageForLeftItemState (UIControlState leftItemState, UIControlState rightItemState);
 		public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftItemState, UIControlState rightItemState);
 		
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCellSelectionStyle</h3>
<p>Removed:</p><pre>
 	Gray
</pre>
<p>Added:</p><pre>
 	Gray,
 	Default
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextView</h3>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets TextContainerInset {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 	public virtual UIBezierPath OutlinePath ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewAnimationOptions</h3>
<p>Added:</p><pre>
 	OverrideInheritedOptions,
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	public virtual System.Drawing.SizeF ContentSizeForViewInPopover {
 	public virtual UIExtendedEdge EdgesForExtendedLayout {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of PreferredContentSize")]
	public virtual System.Drawing.SizeF ContentSizeForViewInPopover {
 	public virtual UIRectEdge EdgesForExtendedLayout {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewKeyframeAnimationOptions</h3>
<p>Added:</p><pre>
 	OverrideInheritedOptions,
</pre>
</body>
</html>
