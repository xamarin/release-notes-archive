---
id: E8EF6A54-47AA-4445-91DA-ACDA03DE3FCB
title: "From 3.0.2 to 3.0.3"
---

<html><head><title>Comparison between monotouch-302.dll and monotouch-303.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.0.0";
 	public const string AdLibLibrary = "/System/Library/Frameworks/AdLib.framework/AdLib";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.3";
 	public const string iAdLibrary = "/System/Library/Frameworks/AdLib.framework/AdLib";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>New Type: MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading</h2>
<pre>
public abstract class AVAsynchronousKeyValueLoading : MonoTouch.Foundation.NSObject {
	
	public AVAsynchronousKeyValueLoading ();
	public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSCoder coder);
	public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSObjectFlag t);
	public AVAsynchronousKeyValueLoading (IntPtr handle);
	
	public abstract void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
	public abstract AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioSessionDelegate</h2>
<p>Added:</p><pre>
 	public virtual void CurrentHardwareInputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareOutputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareSampleRateChanged (double sampleRate);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureConnection</h2>
<p>Added:</p><pre>
 	public virtual bool Active {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureDevice</h2>
<p>Removed:</p><pre>
 	public virtual bool InUseByAnotherApplication {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual AVCaptureDevicePosition Position {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureDevicePosition</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVCaptureDevicePosition
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum AVCaptureDevicePosition {
 	Back,
 	Front
 }
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h2>
<p>Removed:</p><pre>
 	public virtual string [] AvailableImageDataFormatTypes {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSData JpegStillToNSData (MonoTouch.CoreMedia.CMSampleBuffer buffer);
 	public virtual string [] AvailableImageDataCodecTypes {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSNumber[] AvailableImageDataCVPixelFormatTypes {
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h2>
<pre>
public class AVCaptureVideoPreviewLayer : MonoTouch.CoreAnimation.CALayer {
	
	public AVCaptureVideoPreviewLayer ();
	public AVCaptureVideoPreviewLayer (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureVideoPreviewLayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureVideoPreviewLayer (IntPtr handle);
	public AVCaptureVideoPreviewLayer (AVCaptureSession session);
	
	public static AVCaptureVideoPreviewLayer FromSession (AVCaptureSession session);
	
	public virtual bool AutomaticallyAdjustsMirroring {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Mirrored {
		get;
		set;
	}
	public virtual AVCaptureVideoOrientation Orientation {
		get;
		set;
	}
	public virtual AVCaptureSession Session {
		get;
		set;
	}
}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureWhiteBalanceMode</h2>
<p>Removed:</p><pre>
 	AutoWhiteBalance
</pre>
<p>Added:</p><pre>
 	AutoWhiteBalance,
 	ContinuousAutoWhiteBalance
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVError</h2>
<p>Removed:</p><pre>
 	UnsupportedOperation,
 	DeviceExcludedByAnotherDevice,
 	ServerDied
</pre>
<p>Added:</p><pre>
 	CompositionTrackSegmentsNotContiguous,
 	ContentIsProtected,
 	FailedToParse,
 	FormatNotRecognized,
 	InvalidCompositionTrackSegmentDuration,
 	InvalidCompositionTrackSegmentSourceStartTime,
 	InvalidCompositionTrackSegmentSourceDuration,
 	MaximumStillImageCaptureRequestsExceeded,
 	NoImageAtTime,
 	MediaServicesWereReset
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVFileType</h2>
<pre>
public class AVFileType : MonoTouch.Foundation.NSObject {
	
	public AVFileType ();
	public AVFileType (MonoTouch.Foundation.NSCoder coder);
	public AVFileType (MonoTouch.Foundation.NSObjectFlag t);
	public AVFileType (IntPtr handle);
	
	public static string Aifc {
		get;
	}
	public static string Aiff {
		get;
	}
	public static string Amr {
		get;
	}
	public static string AppleM4V {
		get;
	}
	public static string CoreAudioFormat {
		get;
	}
	public static string Mpeg4 {
		get;
	}
	public static string Mpeg4Audio {
		get;
	}
	public static string QuickTimeMovie {
		get;
	}
	public static string ThreeGpp {
		get;
	}
	public static string Wave {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVKeyValueStatus</h2>
<pre>
[Serializable]
public enum AVKeyValueStatus {
	Unknown,
	Loading,
	Loaded,
	Failed,
	Cancelled
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMediaCharacteristic</h2>
<pre>
public class AVMediaCharacteristic : MonoTouch.Foundation.NSObject {
	
	public AVMediaCharacteristic ();
	public AVMediaCharacteristic (MonoTouch.Foundation.NSCoder coder);
	public AVMediaCharacteristic (MonoTouch.Foundation.NSObjectFlag t);
	public AVMediaCharacteristic (IntPtr handle);
	
	public static string Audible {
		get;
	}
	public static string FrameBased {
		get;
	}
	public static string Legible {
		get;
	}
	public static string Visual {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMediaType</h2>
<pre>
public class AVMediaType : MonoTouch.Foundation.NSObject {
	
	public AVMediaType ();
	public AVMediaType (MonoTouch.Foundation.NSCoder coder);
	public AVMediaType (MonoTouch.Foundation.NSObjectFlag t);
	public AVMediaType (IntPtr handle);
	
	public static string Audio {
		get;
	}
	public static string ClosedCaption {
		get;
	}
	public static string Muxed {
		get;
	}
	public static string Subtitle {
		get;
	}
	public static string Text {
		get;
	}
	public static string Timecode {
		get;
	}
	public static string TimedMetadata {
		get;
	}
	public static string Video {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMutableAudioMix</h2>
<p>Added:</p><pre>
 	public static AVMutableAudioMix Create ();
 	
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters</h2>
<p>Removed:</p><pre>
 	public static AVMutableAudioMixInputParameters MutableAudioMixInputParametersWithTrack (AVAssetTrack track);
</pre>
<p>Added:</p><pre>
 	public static AVMutableAudioMixInputParameters Create ();
 	public static AVMutableAudioMixInputParameters FromTrack (AVAssetTrack track);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack</h2>
<p>Added:</p><pre>
 	public virtual string ExtendedLanguageTag {
 		get;
 		set;
 	}
 	public virtual string LanguageCode {
 		get;
 		set;
 	}
 	public virtual int NaturalTimeScale {
 		get;
 		set;
 	}
 	public virtual MonoTouch.CoreGraphics.CGAffineTransform PreferredTransform {
 		get;
 		set;
 	}
 	public virtual float PreferredVolume {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMutableVideoComposition</h2>
<p>Added:</p><pre>
 	public static AVMutableVideoComposition Create ();
 	
 	public virtual float RenderScale {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction</h2>
<p>Added:</p><pre>
 	public static AVMutableVideoCompositionLayerInstruction Create ();
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayer</h2>
<p>Removed:</p><pre>
 	public AVPlayer (AVPlayerQueue queue);
 	public static AVPlayer FromPlayerQueue (AVPlayerQueue queue);
 	public virtual void AdvanceToNextItem ();
 	public virtual bool Muted {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary PreferredLanguages {
 		get;
 		set;
 	}
 	public virtual AVPlayerQueue Queue {
 	public virtual bool SubtitleDisplayEnabled {
 		set;
 	}
 	public virtual float Volume {
 		get;
 		set;
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSError Error {
 	public virtual AVPlayerStatus Status {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerActionAtItemEnd</h2>
<p>Removed:</p><pre>
 	Advance,
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h2>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSError Error {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItemStatus</h2>
<p>Removed:</p><pre>
 	FailedToBecomeReadyToPlay
</pre>
<p>Added:</p><pre>
 	Failed
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h2>
<p>Added:</p><pre>
 	public static string VideoGravityResize {
 		get;
 	}
 	public static string VideoGravityResizeAspect {
 		get;
 	}
 	public static string VideoGravityResizeAspectFill {
 		get;
 	}
 	public virtual string VideoGravity {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerStatus</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVPlayerStatus
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum AVPlayerStatus {
 	Unknown,
 	ReadyToPlay,
 	Failed
 }
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVVideoComposition</h2>
<p>Added:</p><pre>
 	public virtual float RenderScale {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionInstruction</h2>
<p>Added:</p><pre>
 	public static AVVideoCompositionInstruction Create ();
 	
</pre>
<h1>Namespace: MonoTouch.AdLib</h1>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h2>Type Changed: MonoTouch.CoreFoundation.CFRunLoop</h2>
<p>Added:</p><pre>
 	public void Stop ();
</pre>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGLayer</h2>
<p>Added:</p><pre>
 	public CGContext Context {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h2>Type Changed: MonoTouch.EventKit.EKCalendar</h2>
<p>Added:</p><pre>
 	public virtual EKCalendarEventAvailability SupportedEventAvailabilities {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKCalendarEventAvailability</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.EventKit.EKCalendarEventAvailability
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum EKCalendarEventAvailability {
 	None,
 	Busy,
 	Free,
 	Tentative,
 	Unavailable
 }
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEvent</h2>
<p>Added:</p><pre>
 	public static EKEvent FromStore (EKEventStore eventStore);
 	public virtual EKEventAvailability Availability {
 		get;
 		set;
 	}
 	public virtual EKEventStatus Status {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventAvailability</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.EventKit.EKEventAvailability
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum EKEventAvailability {
 	NotSupported,
 	Busy,
 	Free,
 	Tentative,
 	Unavailable
 }
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventEditController</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.EventKit.EKEventEditController
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate EKCalendar EKEventEditController (EKEventEditViewController controller);
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventEditViewController</h2>
<p>Added:</p><pre>
 	public EKEventEditController GetDefaultCalendarForNewEvents {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventEditViewDelegate</h2>
<p>Added:</p><pre>
 	public virtual EKCalendar GetDefaultCalendarForNewEvents (EKEventEditViewController controller);
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventStatus</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.EventKit.EKEventStatus
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum EKEventStatus {
 	None,
 	Confirmed,
 	Tentative,
 	Cancelled
 }
</pre>
<h2>Type Changed: MonoTouch.EventKit.EKEventStore</h2>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSPredicate PredicateForEvents (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSPredicate PredicateForEvents (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
</pre>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h1>Namespace: MonoTouch.GameKit</h1>
<h2>New Type: MonoTouch.GameKit.GKAchievement</h2>
<pre>
public class GKAchievement : MonoTouch.Foundation.NSObject {
	
	public GKAchievement ();
	public GKAchievement (MonoTouch.Foundation.NSCoder coder);
	public GKAchievement (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievement (IntPtr handle);
	public GKAchievement (string identifier);
	
	public static void LoadAchievements (GKCompletionHandler completionHandler);
	public virtual void ReportAchievement (GKNotificationHandler handler);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Completed {
		get;
		set;
	}
	public virtual string Identifier {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDate LastReportedDate {
		get;
		set;
	}
	public virtual double PercentComplete {
		get;
		set;
	}
	public virtual int Points {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKAchievementDescription</h2>
<pre>
public class GKAchievementDescription : MonoTouch.Foundation.NSObject {
	
	public GKAchievementDescription ();
	public GKAchievementDescription (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementDescription (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementDescription (IntPtr handle);
	
	public static void LoadAchievementDescriptions (GKAchievementDescriptionHandler handler);
	public virtual void LoadImage (GKImageLoadedHandler imageLoadedHandler);
	
	public static MonoTouch.UIKit.UIImage PlaceholderCompletedAchievementImage {
		get;
	}
	public virtual string AchievedDescription {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Identifier {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIImage Image {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIImage IncompleteAchievementImage {
		get;
	}
	public virtual int MaximumPoints {
		get;
		set;
	}
	public virtual bool ShouldDisplayIfNotStarted {
		get;
		set;
	}
	public virtual string Title {
		get;
		set;
	}
	public virtual string UnachievedDescription {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKAchievementDescriptionHandler</h2>
<pre>
[Serializable]
public delegate void GKAchievementDescriptionHandler (GKAchievementDescription[] descriptions, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKAchievementViewController</h2>
<pre>
public class GKAchievementViewController : MonoTouch.UIKit.UINavigationController {
	
	public GKAchievementViewController ();
	public GKAchievementViewController (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementViewController (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementViewController (IntPtr handle);
	
	public virtual void SetDelegate (GKAchievementViewControllerDelegate target);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKAchievementViewControllerDelegate</h2>
<pre>
public class GKAchievementViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public GKAchievementViewControllerDelegate ();
	public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementViewControllerDelegate (IntPtr handle);
	
	public virtual void DidPressDismiss ();
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKCompletionHandler</h2>
<pre>
[Serializable]
public delegate void GKCompletionHandler (GKAchievement[] achivements, MonoTouch.Foundation.NSError error);
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKError</h2>
<p>Removed:</p><pre>
 	MatchRequestInvalid
</pre>
<p>Added:</p><pre>
 	MatchRequestInvalid,
 	FeatureNotAvailableInPreview
</pre>
<h2>New Type: MonoTouch.GameKit.GKImageLoadedHandler</h2>
<pre>
[Serializable]
public delegate void GKImageLoadedHandler (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSError error);
</pre>
<h2>Type Changed: MonoTouch.GameKit.GKMatchmakerViewController</h2>
<p>Added:</p><pre>
 	public GKMatchmakerViewController (GKMatchRequest request, GKPlayer[] players);
</pre>
<h1>Namespace: MonoTouch.MapKit</h1>
<h2>Type Changed: MonoTouch.MapKit.MKMapPoint</h2>
<p>Added:</p><pre>
 	public override bool Equals (object other);
 	
</pre>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h2>Type Changed: MonoTouch.MediaPlayer.ItemsPickedEventArgs</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Removed:</p><pre>
 	public static bool Boolean_objc_msgSend_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static bool Boolean_objc_msgSendSuper_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
</pre>
<p>Added:</p><pre>
 	public static void void_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIActionSheet</h2>
<p>Added:</p><pre>
 	public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
 	public virtual void ShowFrom (UIBarButtonItem item, bool animated);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIAlertView</h2>
<p>Removed:</p><pre>
 	public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
 	public virtual void ShowFrom (UIBarButtonItem item);
 	public virtual void ShowFrom (UIBarButtonItem item, bool animated);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIApplication</h2>
<p>Removed:</p><pre>
 	public virtual bool SetStatusBarHidden (bool state, UIStatusBarAnimation animation);
</pre>
<p>Added:</p><pre>
 	public virtual void SetStatusBarHidden (bool state, UIStatusBarAnimation animation);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIFont</h2>
<p>Added:</p><pre>
 	public override string ToString ();
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer</h2>
<p>Removed:</p><pre>
 	public virtual System.Drawing.PointF Translation {
 		get;
 		set;
 	}
 	public virtual System.Drawing.PointF Velocity {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual void SetTranslation (System.Drawing.PointF translation, UIView view);
 	public virtual System.Drawing.PointF TranslationInView (UIView view);
 	public virtual System.Drawing.PointF VelocityInView (UIView view);
 	
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIWebView</h2>
<p>Added:</p><pre>
 	public virtual bool AllowsInlineMediaPlayback {
 		get;
 		set;
 	}
 	public virtual bool MediaPlaybackRequiresUserAction {
 		get;
 		set;
 	}
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h2>Type Changed: MonoTouch.iAd.ADBannerView</h2>
<p>Removed:</p><pre>
 	public ADBannerViewDelegate Deleget {
 	public virtual MonoTouch.Foundation.NSSet RequiredContentSizes {
</pre>
<p>Added:</p><pre>
 	public static System.Drawing.SizeF SizeFromContentSizeIdentifier (string sizeIdentifier);
 	public static string SizeIdentifier320x50 {
 		get;
 	}
 	public static string SizeIdentifier480x32 {
 		get;
 	}
 	public virtual string CurrentContentSizeIdentifier {
 		get;
 	}
 	public ADBannerViewDelegate Delegate {
 	public virtual MonoTouch.Foundation.NSSet RequiredContentSizeIdentifiers {
</pre>
<h2>Type Changed: MonoTouch.iAd.ADManager</h2>
<p>Removed:</p><pre>
 	public static ADManager SharedAdManager ();
 	public virtual void DismissModalAd ();
 	public virtual void PresentModalAdFromViewController (MonoTouch.UIKit.UIViewController parentViewController);
 	
 	public virtual bool CanPresentModalAd {
 		get;
 	}
 	public virtual bool PresentingModalAd {
 		get;
 	}
 	public virtual bool UsesModalAds {
 		get;
 		set;
 	}
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
