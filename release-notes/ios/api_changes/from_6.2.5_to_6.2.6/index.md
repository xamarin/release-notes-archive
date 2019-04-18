---
id: C2E79DB8-F77A-4FCA-B7B8-40FFBE8A9434
title: "From 6.2.5 to 6.2.6"
---

<html><head><title>Comparison between monotouch-6.2.5.dll and monotouch-6.2.6.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.2.5";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.2.6";
</pre>
<h3>New Type: MonoTouch.MonoTouchException</h3>
<pre>
public class MonoTouchException : Exception {
	
	public MonoTouchException (string message, params object [] args);
	public MonoTouchException (int code, string message, params object [] args);
	public MonoTouchException (int code, bool error, string message, params object [] args);
	public MonoTouchException (int code, bool error, Exception innerException, string message, params object [] args);
	
	public int Code {
		get;
	}
	public bool Error {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task LoadValuesTaskAsync (string [] keys);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetExportSession</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;bool&gt; DetermineCompatibilityOfExportPresetAsync (string presetName, AVAsset asset, string outputFileType);
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; DetermineCompatibleFileTypesAsync ();
 	public virtual System.Threading.Tasks.Task ExportTaskAsync ();
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriter</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task FinishWritingAsync ();
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.CoreMedia.CMSampleBuffer&gt; CaptureStillImageTaskAsync (AVCaptureConnection connection);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadataItem</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task LoadValuesTaskAsync (string [] keys);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayer</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; PrerollAsync (float rate);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.CoreMedia.CMTime time);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.Foundation.NSDate date);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.CoreMedia.CMTime time);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.Foundation.NSDate date);
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController</h3>
<p>Added:</p><pre>
 	public static ABPeoplePickerNavigationControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioChannelDescription</h3>
<p>Removed:</p><pre>
 	public float [] Coords;
</pre>
<p>Added:</p><pre>
 	public float [] Coords {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioFileStream</h3>
<p>Added:</p><pre>
 	public AudioFileStreamStatus LastError {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioQueue</h3>
<p>Removed:</p><pre>
 	public T GetProperty&lt;T&gt; (AudioQueueProperty property);
</pre>
<p>Added:</p><pre>
 	public T GetProperty&lt;T&gt; (AudioQueueProperty property) where T : ValueType, struct, new ();
</pre>
<h2>Namespace: MonoTouch.CoreAnimation</h2>
<h3>Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation</h3>
<p>Removed:</p><pre>
 	public static CAPropertyAnimation FromKeyPath (string path);
</pre>
<p>Added:</p><pre>
 	[Obsolete("This method in the future will return a CAKeyFrameAnimation, update your source, or use GetFromKeyPath to avoid this warning for now")]
	public static CAPropertyAnimation FromKeyPath (string path);
 	public static CAKeyFrameAnimation GetFromKeyPath (string path);
</pre>
<h2>Namespace: MonoTouch.CoreGraphics</h2>
<h3>Type Changed: MonoTouch.CoreGraphics.CGContext</h3>
<p>Added:</p><pre>
 	public void DrawShading (CGShading shading);
</pre>
<h3>Type Changed: MonoTouch.CoreGraphics.CGPDFDocument</h3>
<p>Added:</p><pre>
 	public CGPDFDictionary GetInfo ();
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>Type Changed: MonoTouch.CoreLocation.CLGeocoder</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (MonoTouch.Foundation.NSDictionary addressDictionary);
 	public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString);
 	public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; GeocodeAddressAsync (string addressString, CLRegion region);
 	public virtual System.Threading.Tasks.Task&lt;CLPlacemark[]&gt; ReverseGeocodeLocationAsync (CLLocation location);
</pre>
<h2>Namespace: MonoTouch.CoreServices</h2>
<h3>Type Changed: MonoTouch.CoreServices.CFHTTPMessage</h3>
<p>Added:</p><pre>
 	public static CFHTTPMessage CreateEmpty (bool request);
 	public bool AppendBytes (byte [] bytes);
 	public bool AppendBytes (byte [] bytes, int count);
</pre>
<h2>Namespace: MonoTouch.EventKitUI</h2>
<h3>Type Changed: MonoTouch.EventKitUI.EKEventEditViewController</h3>
<p>Added:</p><pre>
 	public static EKEventEditViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.ExportAttribute</h3>
<p>Added:</p><pre>
 	public bool IsVariadic {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.FieldAttribute</h3>
<pre>
public class FieldAttribute : Attribute {
	
	public FieldAttribute (string symbolName);
	public FieldAttribute (string symbolName, string libraryName);
	
	public string LibraryName {
		get;
		set;
	}
	public string SymbolName {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSComparisonPredicateOptions</h3>
<p>Added:</p><pre>
 	None,
</pre>
<h3>New Type: MonoTouch.Foundation.NSErrorException</h3>
<pre>
public class NSErrorException : Exception {
	
	public NSErrorException (NSError error);
	
	public int Code {
		get;
	}
	public string Domain {
		get;
	}
	public NSError Error {
		get;
	}
	public NSDictionary UserInfo {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSInputStream</h3>
<p>Removed:</p><pre>
 	public virtual void ScheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
 	public virtual void UnscheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableUrlRequest</h3>
<p>Added:</p><pre>
 	public virtual NSUrlRequestNetworkServiceType NetworkServiceType {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Removed:</p><pre>
 	public virtual void Bind (string binding, NSObject observable, string keyPath, NSDictionary options);
 	public virtual NSDictionary BindingInfo (string binding);
 	public virtual NSObject[] BindingOptionDescriptions (string aBinding);
 	public virtual MonoTouch.ObjCRuntime.Class BindingValueClass (string binding);
 	public virtual bool CommitEditing ();
 	public virtual void CommitEditing (NSObject objDelegate, MonoTouch.ObjCRuntime.Selector didCommitSelector, IntPtr contextInfo);
 	public virtual NSString[] ExposedBindings ();
 	public virtual void ObjectDidEndEditing (NSObject editor);
 	public virtual void Unbind (string binding);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSProcessInfo</h3>
<p>Added:</p><pre>
 	public virtual void DisableAutomaticTermination (string reason);
 	public virtual void DisableSuddenTermination ();
 	public virtual void EnableAutomaticTermination (string reason);
 	public virtual void EnableSuddenTermination ();
 	public virtual bool AutomaticTerminationSupportEnabled {
 		get;
 		set;
 	}
 	public virtual double SystemUptime {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSStream</h3>
<p>Added:</p><pre>
 	public NSObject this [NSString key] {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSString</h3>
<p>Added:</p><pre>
 	public static string [] PathWithComponents (string [] components);
 	public virtual NSString AbbreviateTildeInPath ();
 	public virtual NSString AppendPathComponent (NSString str);
 	public virtual NSString AppendPathExtension (NSString str);
 	public virtual string [] AppendPaths (string [] paths);
 	public virtual NSString DeleteLastPathComponent ();
 	public virtual NSString DeletePathExtension ();
 	protected override void Dispose (bool disposing);
 	public virtual NSString ExpandTildeInPath ();
 	public virtual NSString ResolveSymlinksInPath ();
 	public virtual NSString StandarizePath ();
 	public virtual bool IsAbsolutePath {
 		get;
 	}
 	public virtual NSString LastPathComponent {
 		get;
 	}
 	public virtual string [] PathComponents {
 		get;
 	}
 	public virtual NSString PathExtension {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlAsyncResult</h3>
<pre>
public class NSUrlAsyncResult {
	
	public NSUrlAsyncResult (NSUrlResponse response, NSData data);
	
	public NSData Data {
		get;
		set;
	}
	public NSUrlResponse Response {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlConnection</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;NSUrlAsyncResult&gt; SendRequestAsync (NSUrlRequest request, NSOperationQueue queue);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlCredential</h3>
<p>Removed:</p><pre>
 	public NSUrlCredential (IntPtr SecTrustRef_trust, bool ignored);
</pre>
<p>Added:</p><pre>
 	public NSUrlCredential (IntPtr trust, bool ignored);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlRequest</h3>
<p>Added:</p><pre>
 	public virtual bool AllowsCellularAccess {
 		get;
 	}
 	public virtual NSUrlRequestNetworkServiceType NetworkServiceType {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlRequestNetworkServiceType</h3>
<pre>
[Serializable]
public enum NSUrlRequestNetworkServiceType {
	Default,
	VoIP,
	Video,
	Background,
	Voice
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSValue</h3>
<p>Added:</p><pre>
 	public static NSValue FromRange (NSRange range);
</pre>
<h3>New Type: MonoTouch.Foundation.ProtocolAttribute</h3>
<pre>
public sealed class ProtocolAttribute : Attribute {
	
	public ProtocolAttribute ();
}
</pre>
<h2>Namespace: MonoTouch.GLKit</h2>
<h3>Type Changed: MonoTouch.GLKit.GLKView</h3>
<p>Added:</p><pre>
 	public static GLKViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementViewController</h3>
<p>Added:</p><pre>
 	public static GKAchievementViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController</h3>
<p>Added:</p><pre>
 	public static GKFriendRequestComposeViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboardViewController</h3>
<p>Added:</p><pre>
 	public static GKLeaderboardViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController</h3>
<p>Added:</p><pre>
 	public static GKTurnBasedMatchmakerViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKAnnotationView</h3>
<p>Added:</p><pre>
 	public static MKAnnotationViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKCircleView</h3>
<p>Added:</p><pre>
 	public static MKCircleViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Added:</p><pre>
 	public static MKMapViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKOverlayPathView</h3>
<p>Added:</p><pre>
 	public static MKOverlayPathViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKOverlayView</h3>
<p>Added:</p><pre>
 	public static MKOverlayViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKPinAnnotationView</h3>
<p>Added:</p><pre>
 	public static MKPinAnnotationViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKPolygonView</h3>
<p>Added:</p><pre>
 	public static MKPolygonViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKPolylineView</h3>
<p>Added:</p><pre>
 	public static MKPolylineViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem</h3>
<p>Added:</p><pre>
 	public static MKUserTrackingBarButtonItemAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPVolumeView</h3>
<p>Added:</p><pre>
 	public static MPVolumeViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.MessageUI</h2>
<h3>Type Changed: MonoTouch.MessageUI.MFMailComposeViewController</h3>
<p>Added:</p><pre>
 	public static MFMailComposeViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController</h3>
<p>Added:</p><pre>
 	public static MFMessageComposeViewControllerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.LinkWithAttribute</h3>
<p>Added:</p><pre>
 	public bool SmartLink {
 		get;
 		set;
 	}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.UIAccessibility</h3>
<pre>
public static class UIAccessibility {
	
	public static void PostNotification (int notification, MonoTouch.Foundation.NSObject argument);
	public static void PostNotification (UIAccessibilityPostNotification notification, MonoTouch.Foundation.NSObject argument);
	public static void RegisterGestureConflictWithZoom ();
	public static void ZoomFocusChanged (UIAccessibilityZoomType type, System.Drawing.RectangleF frame, UIView view);
	
	public static bool IsClosedCaptioningEnabled {
		get;
	}
	public static bool IsGuidedAccessEnabled {
		get;
	}
	public static bool IsInvertColorsEnabled {
		get;
	}
	public static bool IsMonoAudioEnabled {
		get;
	}
	public static bool IsVoiceOverRunning {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIAccessibilityAnnouncementFinishedEventArgs</h3>
<pre>
public class UIAccessibilityAnnouncementFinishedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	
	public UIAccessibilityAnnouncementFinishedEventArgs (MonoTouch.Foundation.NSNotification notification);
	
	public string Announcement {
		get;
	}
	public bool WasSuccessful {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIAccessibilityPostNotification</h3>
<pre>
[Serializable]
public enum UIAccessibilityPostNotification {
	Announcement,
	LayoutChanged,
	PageScrolled,
	ScreenChanged
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAccessibilityScrollDirection</h3>
<p>Removed:</p><pre>
 	Down
</pre>
<p>Added:</p><pre>
 	Down,
 	Next,
 	Previous
</pre>
<h3>New Type: MonoTouch.UIKit.UIAccessibilityTrait</h3>
<pre>
[Serializable]
[Flags]
public enum UIAccessibilityTrait : long {
	None,
	Button,
	Link,
	Image,
	Selected,
	PlaysSound,
	KeyboardKey,
	StaticText,
	SummaryElement,
	NotEnabled,
	UpdatesFrequently,
	SearchField,
	StartsMediaSession,
	Adjustable,
	AllowsDirectInteraction,
	CausesPageTurn,
	Header
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIAccessibilityZoomType</h3>
<pre>
[Serializable]
public enum UIAccessibilityZoomType {
	InsertionPoint
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActionSheet</h3>
<p>Added:</p><pre>
 	public static UIActionSheetAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActivityIndicatorView</h3>
<p>Added:</p><pre>
 	public static UIActivityIndicatorViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAlertView</h3>
<p>Added:</p><pre>
 	public static UIAlertViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Added:</p><pre>
 	public virtual bool AccessibilityPerformMagicTap ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarButtonItem</h3>
<p>Added:</p><pre>
 	public static UIBarButtonItemAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarItem</h3>
<p>Added:</p><pre>
 	public static UIBarItemAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBezierPath</h3>
<p>Added:</p><pre>
 	public static UIBezierPathAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIButton</h3>
<p>Added:</p><pre>
 	public static UIButtonAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionReusableView</h3>
<p>Added:</p><pre>
 	public static UICollectionReusableViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Added:</p><pre>
 	public static UICollectionViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewCell</h3>
<p>Added:</p><pre>
 	public static UICollectionViewCellAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayout</h3>
<p>Removed:</p><pre>
 	public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
 	public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
 	public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
 	public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Added:</p><pre>
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForDecorationView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (UICollectionElementKindSection section, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIControl</h3>
<p>Added:</p><pre>
 	public static UIControlAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDatePicker</h3>
<p>Added:</p><pre>
 	public static UIDatePickerAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocumentInteractionController</h3>
<p>Removed:</p><pre>
 	public event EventHandler DidEndSendingToApplication;
 	public event EventHandler WillBeginSendingToApplication;
</pre>
<p>Added:</p><pre>
 	public event EventHandler&lt;UIDocumentSendingToApplicationEventArgs&gt; DidEndSendingToApplication;
 	public event EventHandler&lt;UIDocumentSendingToApplicationEventArgs&gt; WillBeginSendingToApplication;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocumentInteractionControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidEndSendingToApplication (UIDocumentInteractionController controller);
 	public virtual void WillBeginSendingToApplication (UIDocumentInteractionController controller);
</pre>
<p>Added:</p><pre>
 	public virtual void DidEndSendingToApplication (UIDocumentInteractionController controller, string application);
 	public virtual void WillBeginSendingToApplication (UIDocumentInteractionController controller, string application);
</pre>
<h3>New Type: MonoTouch.UIKit.UIDocumentSendingToApplicationEventArgs</h3>
<pre>
public class UIDocumentSendingToApplicationEventArgs : EventArgs {
	
	public UIDocumentSendingToApplicationEventArgs (string application);
	
	public string Application {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Added:</p><pre>
 	public static UIImage FromImage (MonoTouch.CoreGraphics.CGImage image, float scale, UIImageOrientation orientation);
 	public static UIImage FromImage (MonoTouch.CoreImage.CIImage image);
 	public UIImage Scale (System.Drawing.SizeF newSize, float scaleFactor);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImageView</h3>
<p>Added:</p><pre>
 	public static UIImageViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UILabel</h3>
<p>Added:</p><pre>
 	public static UILabelAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBar</h3>
<p>Added:</p><pre>
 	public static UINavigationBarAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageControl</h3>
<p>Added:</p><pre>
 	public static UIPageControlAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPickerView</h3>
<p>Added:</p><pre>
 	public static UIPickerViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView</h3>
<p>Added:</p><pre>
 	public static UIPopoverBackgroundViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIProgressView</h3>
<p>Added:</p><pre>
 	public static UIProgressViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIRefreshControl</h3>
<p>Added:</p><pre>
 	public static UIRefreshControlAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIResponder</h3>
<p>Added:</p><pre>
 	public virtual void AccessibilityDecrement ();
 	public virtual void AccessibilityIncrement ();
 	public virtual bool AccessibilityPerformEscape ();
 	public virtual bool AccessibilityPerformMagicTap ();
 	public virtual bool AccessibilityScroll (UIAccessibilityScrollDirection direction);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScrollView</h3>
<p>Added:</p><pre>
 	public static UIScrollViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Added:</p><pre>
 	public static UISearchBarAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISegmentedControl</h3>
<p>Added:</p><pre>
 	public static UISegmentedControlAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISlider</h3>
<p>Added:</p><pre>
 	public static UISliderAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStepper</h3>
<p>Added:</p><pre>
 	public static UIStepperAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISwitch</h3>
<p>Added:</p><pre>
 	public static UISwitchAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBar</h3>
<p>Added:</p><pre>
 	public static UITabBarAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarItem</h3>
<p>Added:</p><pre>
 	public static UITabBarItemAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Added:</p><pre>
 	public static UITableViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCell</h3>
<p>Added:</p><pre>
 	public static UITableViewCellAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewController</h3>
<p>Added:</p><pre>
 	public virtual void AccessoryButtonTapped (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UITableViewCellAccessory AccessoryForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanEditRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanMoveRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanPerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
 	public virtual void CellDisplayingEnded (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void CommitEditingStyle (UITableView tableView, UITableViewCellEditingStyle editingStyle, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual MonoTouch.Foundation.NSIndexPath CustomizeMoveTarget (UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath proposedIndexPath);
 	public virtual void DidEndEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UITableViewCellEditingStyle EditingStyleForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void FooterViewDisplayingEnded (UITableView tableView, UIView footerView, int section);
 	public virtual UITableViewCell GetCell (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float GetHeightForFooter (UITableView tableView, int section);
 	public virtual float GetHeightForHeader (UITableView tableView, int section);
 	public virtual float GetHeightForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UIView GetViewForFooter (UITableView tableView, int section);
 	public virtual UIView GetViewForHeader (UITableView tableView, int section);
 	public virtual void HeaderViewDisplayingEnded (UITableView tableView, UIView headerView, int section);
 	public virtual int IndentationLevel (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void MoveRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath destinationIndexPath);
 	public virtual int NumberOfSections (UITableView tableView);
 	public virtual void PerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
 	public virtual void RowDeselected (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void RowHighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual void RowSelected (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int RowsInSection (UITableView tableview, int section);
 	public virtual void RowUnhighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual int SectionFor (UITableView tableView, string title, int atIndex);
 	public virtual string [] SectionIndexTitles (UITableView tableView);
 	public virtual bool ShouldHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual bool ShouldIndentWhileEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool ShouldShowMenu (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowAtindexPath);
 	public virtual string TitleForDeleteConfirmation (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual string TitleForFooter (UITableView tableView, int section);
 	public virtual string TitleForHeader (UITableView tableView, int section);
 	public virtual void WillBeginEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void WillDisplay (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void WillDisplayFooterView (UITableView tableView, UIView footerView, int section);
 	public virtual void WillDisplayHeaderView (UITableView tableView, UIView headerView, int section);
 	public virtual MonoTouch.Foundation.NSIndexPath WillSelectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView</h3>
<p>Added:</p><pre>
 	public static UITableViewHeaderFooterViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewSource</h3>
<p>Removed:</p><pre>
 	public virtual void WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextField</h3>
<p>Added:</p><pre>
 	public static UITextFieldAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextView</h3>
<p>Added:</p><pre>
 	public static UITextViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbar</h3>
<p>Added:</p><pre>
 	public static UIToolbarAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Added:</p><pre>
 	public static UIViewAppearance GetAppearance&lt;T&gt; ();
 	public static MonoTouch.Foundation.NSString AnnouncementDidFinishNotification {
 		get;
 	}
 	public static int AnnouncementNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ClosedCaptioningStatusDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GuidedAccessStatusDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString InvertColorsStatusDidChangeNotification {
 		get;
 	}
 	public static int LayoutChangedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MonoAudioStatusDidChangeNotification {
 		get;
 	}
 	public static int PageScrolledNotification {
 		get;
 	}
 	public static int ScreenChangedNotification {
 		get;
 	}
 	public static long TraitAdjustable {
 		get;
 	}
 	public static long TraitAllowsDirectInteraction {
 		get;
 	}
 	public static long TraitButton {
 		get;
 	}
 	public static long TraitCausesPageTurn {
 		get;
 	}
 	public static long TraitHeader {
 		get;
 	}
 	public static long TraitImage {
 		get;
 	}
 	public static long TraitKeyboardKey {
 		get;
 	}
 	public static long TraitLink {
 		get;
 	}
 	public static long TraitNone {
 		get;
 	}
 	public static long TraitNotEnabled {
 		get;
 	}
 	public static long TraitPlaysSound {
 		get;
 	}
 	public static long TraitSearchField {
 		get;
 	}
 	public static long TraitSelected {
 		get;
 	}
 	public static long TraitStartsMediaSession {
 		get;
 	}
 	public static long TraitStaticText {
 		get;
 	}
 	public static long TraitSummaryElement {
 		get;
 	}
 	public static long TraitUpdatesFrequently {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString VoiceOverStatusChanged {
 		get;
 	}
 	public virtual System.Drawing.PointF AccessibilityActivationPoint {
 		get;
 		set;
 	}
 	public virtual bool AccessibilityElementsHidden {
 		get;
 		set;
 	}
 	public virtual System.Drawing.RectangleF AccessibilityFrame {
 		get;
 		set;
 	}
 	public virtual string AccessibilityHint {
 		get;
 		set;
 	}
 	public virtual string AccessibilityLabel {
 		get;
 		set;
 	}
 	public virtual string AccessibilityLanguage {
 		get;
 		set;
 	}
 	public virtual UIAccessibilityTrait AccessibilityTraits {
 		get;
 		set;
 	}
 	public virtual string AccessibilityValue {
 		get;
 		set;
 	}
 	public virtual bool AccessibilityViewIsModal {
 		get;
 		set;
 	}
 	public virtual bool IsAccessibilityElement {
 		get;
 		set;
 	}
 	public virtual bool ShouldGroupAccessibilityChildren {
 		get;
 		set;
 	}
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveAnnouncementDidFinish (EventHandler&lt;UIAccessibilityAnnouncementFinishedEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveClosedCaptioningStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveGuidedAccessStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveInvertColorsStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveMonoAudioStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIWebView</h3>
<p>Added:</p><pre>
 	public static UIWebViewAppearance GetAppearance&lt;T&gt; ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIWindow</h3>
<p>Added:</p><pre>
 	public static UIWindowAppearance GetAppearance&lt;T&gt; ();
</pre>
<h2>Namespace: MonoTouch.iAd</h2>
<h3>Type Changed: MonoTouch.iAd.ADBannerView</h3>
<p>Added:</p><pre>
 	public static ADBannerViewAppearance GetAppearance&lt;T&gt; ();
</pre>
</body>
</html>
