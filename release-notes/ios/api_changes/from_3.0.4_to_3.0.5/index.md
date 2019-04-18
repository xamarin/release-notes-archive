---
id: A03725AC-DFE4-4DCE-B171-4B31D4F46F6D
title: "From 3.0.4 to 3.0.5"
---

<html><head><title>Comparison between monotouch-304.dll and monotouch-305.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.0.4";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.5";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutput</h2>
<p>Removed:</p><pre>
 	public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, IntPtr sampleBufferCallbackDispatchQueue);
 	public virtual IntPtr SampleBufferCallbackQueue {
</pre>
<p>Added:</p><pre>
 	public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
 	public virtual MonoTouch.CoreFoundation.DispatchQueue SampleBufferCallbackQueue {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary OutputSettings ();
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary OutputSettings {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVFileType</h2>
<p>Removed:</p><pre>
 public class AVFileType : MonoTouch.Foundation.NSObject {
 	public AVFileType (MonoTouch.Foundation.NSCoder coder);
 	public AVFileType (MonoTouch.Foundation.NSObjectFlag t);
 	public AVFileType (IntPtr handle);
 	public static string Aifc {
 	public static string Aiff {
 	public static string Amr {
 	public static string AppleM4V {
 	public static string CoreAudioFormat {
 	public static string Mpeg4 {
 	public static string Mpeg4Audio {
 	public static string QuickTimeMovie {
 	public static string ThreeGpp {
 	public static string Wave {
 		get;
 	}
 	public override IntPtr ClassHandle {
</pre>
<p>Added:</p><pre>
 public class AVFileType {
 	public static MonoTouch.Foundation.NSString Aifc {
 	public static MonoTouch.Foundation.NSString Aiff {
 	public static MonoTouch.Foundation.NSString Amr {
 	public static MonoTouch.Foundation.NSString AppleM4V {
 	public static MonoTouch.Foundation.NSString CoreAudioFormat {
 	public static MonoTouch.Foundation.NSString Mpeg4 {
 	public static MonoTouch.Foundation.NSString Mpeg4Audio {
 	public static MonoTouch.Foundation.NSString QuickTimeMovie {
 	public static MonoTouch.Foundation.NSString ThreeGpp {
 	public static MonoTouch.Foundation.NSString Wave {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMediaCharacteristic</h2>
<p>Removed:</p><pre>
 public class AVMediaCharacteristic : MonoTouch.Foundation.NSObject {
 	public AVMediaCharacteristic (MonoTouch.Foundation.NSCoder coder);
 	public AVMediaCharacteristic (MonoTouch.Foundation.NSObjectFlag t);
 	public AVMediaCharacteristic (IntPtr handle);
 	public static string Audible {
 	public static string FrameBased {
 	public static string Legible {
 	public static string Visual {
 		get;
 	}
 	public override IntPtr ClassHandle {
</pre>
<p>Added:</p><pre>
 public class AVMediaCharacteristic {
 	public static MonoTouch.Foundation.NSString Audible {
 	public static MonoTouch.Foundation.NSString FrameBased {
 	public static MonoTouch.Foundation.NSString Legible {
 	public static MonoTouch.Foundation.NSString Visual {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMediaType</h2>
<p>Removed:</p><pre>
 public class AVMediaType : MonoTouch.Foundation.NSObject {
 	public AVMediaType (MonoTouch.Foundation.NSCoder coder);
 	public AVMediaType (MonoTouch.Foundation.NSObjectFlag t);
 	public AVMediaType (IntPtr handle);
 	public static string Audio {
 	public static string ClosedCaption {
 	public static string Muxed {
 	public static string Subtitle {
 	public static string Text {
 	public static string Timecode {
 	public static string TimedMetadata {
 	public static string Video {
 		get;
 	}
 	public override IntPtr ClassHandle {
</pre>
<p>Added:</p><pre>
 public class AVMediaType {
 	public static MonoTouch.Foundation.NSString Audio {
 	public static MonoTouch.Foundation.NSString ClosedCaption {
 	public static MonoTouch.Foundation.NSString Muxed {
 	public static MonoTouch.Foundation.NSString Subtitle {
 	public static MonoTouch.Foundation.NSString Text {
 	public static MonoTouch.Foundation.NSString Timecode {
 	public static MonoTouch.Foundation.NSString TimedMetadata {
 	public static MonoTouch.Foundation.NSString Video {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h2>
<p>Removed:</p><pre>
 	public static string VideoGravityResize {
 	public static string VideoGravityResizeAspect {
 	public static string VideoGravityResizeAspectFill {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString VideoGravityResize {
 	public static MonoTouch.Foundation.NSString VideoGravityResizeAspect {
 	public static MonoTouch.Foundation.NSString VideoGravityResizeAspectFill {
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVVideo</h2>
<pre>
public class AVVideo {
	
	public AVVideo ();
	
	public static MonoTouch.Foundation.NSString AverageBitRateKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureHeightKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureHorizontalOffsetKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureVerticalOffsetKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureWidthKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecH264 {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecJPEG {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CompressionPropertiesKey {
		get;
	}
	public static MonoTouch.Foundation.NSString HeightKey {
		get;
	}
	public static MonoTouch.Foundation.NSString MaxKeyFrameIntervalKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioHorizontalSpacingKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioVerticalSpacingKey {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Baseline30 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Baseline31 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Main30 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Main31 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelKey {
		get;
	}
	public static MonoTouch.Foundation.NSString WidthKey {
		get;
	}
}
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>New Type: MonoTouch.CoreAnimation.CATiledLayer</h2>
<pre>
public class CATiledLayer : CALayer {
	
	public CATiledLayer ();
	public CATiledLayer (MonoTouch.Foundation.NSCoder coder);
	public CATiledLayer (MonoTouch.Foundation.NSObjectFlag t);
	public CATiledLayer (IntPtr handle);
	
	public static double FadeDuration {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int LevelsOfDetail {
		get;
		set;
	}
	public virtual int LevelsOfDetailBias {
		get;
		set;
	}
	public virtual System.Drawing.SizeF TileSize {
		get;
		set;
	}
}
</pre>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h2>Type Changed: MonoTouch.CoreFoundation.DispatchQueue</h2>
<p>Added:</p><pre>
 	public DispatchQueue (IntPtr handle);
</pre>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGContext</h2>
<p>Added:</p><pre>
 	public void DrawLayer (CGLayer layer, System.Drawing.PointF point);
 	public void DrawLayer (CGLayer layer, System.Drawing.RectangleF rect);
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h2>Type Changed: MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs
</pre>
<p>Added:</p><pre>
 public class CLHeadingUpdatedEventArgs : EventArgs {
 	
 	public CLHeadingUpdatedEventArgs (CLHeading newHeading);
 	
 	public CLHeading NewHeading {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h2>
<p>Added:</p><pre>
 	public CLLocationManagerEventArgs ShouldDisplayHeadingCalibration {
 		get;
 		set;
 	}
 	
 	public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; Failed;
 	public event EventHandler&lt;CLRegionErrorEventArgs&gt; MonitoringFailed;
 	public event EventHandler&lt;CLRegionEventArgs&gt; RegionEntered;
 	public event EventHandler&lt;CLRegionEventArgs&gt; RegionLeft;
 	public event EventHandler&lt;CLHeadingUpdatedEventArgs&gt; UpdatedHeading;
 	public event EventHandler&lt;CLLocationUpdatedEventArgs&gt; UpdatedLocation;
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationManagerEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLLocationManagerEventArgs
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool CLLocationManagerEventArgs (CLLocationManager manager);
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationUpdatedEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLLocationUpdatedEventArgs
</pre>
<p>Added:</p><pre>
 public class CLLocationUpdatedEventArgs : EventArgs {
 	
 	public CLLocationUpdatedEventArgs (CLLocation newLocation, CLLocation oldLocation);
 	
 	public CLLocation NewLocation {
 		get;
 		set;
 	}
 	public CLLocation OldLocation {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLRegionErrorEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLRegionErrorEventArgs
</pre>
<p>Added:</p><pre>
 public class CLRegionErrorEventArgs : EventArgs {
 	
 	public CLRegionErrorEventArgs (CLRegion region, MonoTouch.Foundation.NSError error);
 	
 	public MonoTouch.Foundation.NSError Error {
 		get;
 		set;
 	}
 	public CLRegion Region {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLRegionEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLRegionEventArgs
</pre>
<p>Added:</p><pre>
 public class CLRegionEventArgs : EventArgs {
 	
 	public CLRegionEventArgs (CLRegion region);
 	
 	public CLRegion Region {
 		get;
 		set;
 	}
 }
</pre>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSAttributedString</h2>
<p>Removed:</p><pre>
 	public static string FontAttributeName {
 	public static string ParagraphStyleAttributeName {
</pre>
<p>Added:</p><pre>
 	public static NSString FontAttributeName {
 	public static NSString ParagraphStyleAttributeName {
</pre>
<h2>New Type: MonoTouch.Foundation.NSNull</h2>
<pre>
public class NSNull : NSObject {
	
	public NSNull ();
	public NSNull (NSCoder coder);
	public NSNull (NSObjectFlag t);
	public NSNull (IntPtr handle);
	
	public static NSNull Null {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrl</h2>
<p>Added:</p><pre>
 	public override string ToString ();
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h2>Type Changed: MonoTouch.MapKit.MKMapPoint</h2>
<p>Added:</p><pre>
 	public override int GetHashCode ();
</pre>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIApplication</h2>
<p>Removed:</p><pre>
 	public static string DidBecomeActiveNotification {
 	public static string DidChangeStatusBarFrameNotification {
 	public static string DidChangeStatusBarOrientationNotification {
 	public static string DidEnterBackgroundNotification {
 	public static string DidFinishLaunchingNotification {
 	public static string DidReceiveMemoryWarningNotification {
 	public static int InvalidBackgroundTaskIdentifier {
 	public static string LaunchOptionsAnnotationKey {
 	public static string LaunchOptionsLocalNotificationKey {
 	public static string LaunchOptionsLocationKey {
 	public static string LaunchOptionsRemoteNotificationKey {
 	public static string LaunchOptionsSourceApplicationKey {
 	public static string LaunchOptionsUrlKey {
 	public static double MinimumKeepAliveTimeout {
 	public static string ProtectedDataDidBecomeAvailable {
 	public static string ProtectedDataWillBecomeUnavailable {
 	public static string SignificantTimeChangeNotification {
 	public static string StatusBarFrameUserInfoKey {
 	public static string StatusBarOrientationUserInfoKey {
 	public static string WillChangeStatusBarFrameNotification {
 	public static string WillChangeStatusBarOrientationNotification {
 	public static string WillEnterForegroundNotification {
 	public static string WillResignActiveNotification {
 	public static string WillTerminateNotification {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString DidBecomeActiveNotification {
 	public static MonoTouch.Foundation.NSString DidChangeStatusBarFrameNotification {
 	public static MonoTouch.Foundation.NSString DidChangeStatusBarOrientationNotification {
 	public static MonoTouch.Foundation.NSString DidEnterBackgroundNotification {
 	public static MonoTouch.Foundation.NSString DidFinishLaunchingNotification {
 	public static MonoTouch.Foundation.NSString DidReceiveMemoryWarningNotification {
 	public static MonoTouch.Foundation.NSString InvalidBackgroundTaskIdentifier {
 	public static MonoTouch.Foundation.NSString LaunchOptionsAnnotationKey {
 	public static MonoTouch.Foundation.NSString LaunchOptionsLocalNotificationKey {
 	public static MonoTouch.Foundation.NSString LaunchOptionsLocationKey {
 	public static MonoTouch.Foundation.NSString LaunchOptionsRemoteNotificationKey {
 	public static MonoTouch.Foundation.NSString LaunchOptionsSourceApplicationKey {
 	public static MonoTouch.Foundation.NSString LaunchOptionsUrlKey {
 	public static MonoTouch.Foundation.NSString MinimumKeepAliveTimeout {
 	public static MonoTouch.Foundation.NSString ProtectedDataDidBecomeAvailable {
 	public static MonoTouch.Foundation.NSString ProtectedDataWillBecomeUnavailable {
 	public static MonoTouch.Foundation.NSString SignificantTimeChangeNotification {
 	public static MonoTouch.Foundation.NSString StatusBarFrameUserInfoKey {
 	public static MonoTouch.Foundation.NSString StatusBarOrientationUserInfoKey {
 	public static MonoTouch.Foundation.NSString WillChangeStatusBarFrameNotification {
 	public static MonoTouch.Foundation.NSString WillChangeStatusBarOrientationNotification {
 	public static MonoTouch.Foundation.NSString WillEnterForegroundNotification {
 	public static MonoTouch.Foundation.NSString WillResignActiveNotification {
 	public static MonoTouch.Foundation.NSString WillTerminateNotification {
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIControlState</h2>
<p>Added:</p><pre>
 [Flags]
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISearchBar</h2>
<p>Added:</p><pre>
 	public UISearchBarPredicate ShouldBeginEditing {
 		get;
 		set;
 	}
 	public UISearchBarRangeEventArgs ShouldChangeTextInRange {
 		get;
 		set;
 	}
 	public UISearchBarPredicate ShouldEndEditing {
 		get;
 		set;
 	}
 	
 	public event EventHandler BookmarkButtonClicked;
 	public event EventHandler CancelButtonClicked;
 	public event EventHandler ListButtonClicked;
 	public event EventHandler OnEditingStarted;
 	public event EventHandler OnEditingStopped;
 	public event EventHandler SearchButtonClicked;
 	public event EventHandler&lt;UISearchBarTextChangedEventArgs&gt; TextChanged;
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISearchBarPredicate</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarPredicate
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UISearchBarPredicate (UISearchBar searchBar);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISearchBarRangeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarRangeEventArgs
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UISearchBarRangeEventArgs (UISearchBar searchBar, MonoTouch.Foundation.NSRange range, string text);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISearchBarTextChangedEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarTextChangedEventArgs
</pre>
<p>Added:</p><pre>
 public class UISearchBarTextChangedEventArgs : EventArgs {
 	
 	public UISearchBarTextChangedEventArgs (string searchText);
 	
 	public string SearchText {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarController</h2>
<p>Added:</p><pre>
 	public UITabBarSelection ShouldSelectViewController {
 		get;
 		set;
 	}
 	
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; FinishedCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeEventArgs&gt; OnCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; OnEndCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarSelectionEventArgs&gt; ViewControllerSelected;
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeChangeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeChangeEventArgs (UIViewController[] viewControllers, bool changed);
 	
 	public bool Changed {
 		get;
 		set;
 	}
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarCustomizeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeEventArgs (UIViewController[] viewControllers);
 	
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarSelection</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelection
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UITabBarSelection (UITabBarController tabBarController, UIViewController viewController);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITabBarSelectionEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelectionEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarSelectionEventArgs : EventArgs {
 	
 	public UITabBarSelectionEventArgs (UIViewController viewController);
 	
 	public UIViewController ViewController {
 		get;
 		set;
 	}
 }
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h2>Type Changed: MonoTouch.iAd.ADBannerView</h2>
<p>Removed:</p><pre>
 	public static string SizeIdentifier320x50 {
 	public static string SizeIdentifier480x32 {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString SizeIdentifier320x50 {
 	public static MonoTouch.Foundation.NSString SizeIdentifier480x32 {
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
