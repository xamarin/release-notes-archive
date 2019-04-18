---
id: C9AD6BD2-8805-4BC0-9E8D-1289BD4FAA40
title: "From 8.6.1 to 8.6.2"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.6.1" "8.6.2";
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

Added methods:

```
public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.CoreAudioKit

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.CoreAudioKit.CAInterAppAudioTransportView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSUrlSession

Obsoleted methods:

```
[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
	[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual System.Threading.Tasks.Task<NSUrlSessionActiveTasks> GetTasksAsync ();
```

Added methods:

```
public void GetTasks2 (NSUrlSessionPendingTasks2 completionHandler);
	public System.Threading.Tasks.Task<NSUrlSessionActiveTasks2> GetTasks2Async ();
```

### New Type MonoTouch.Foundation.NSUrlSessionActiveTasks2

```
public class NSUrlSessionActiveTasks2 {
	// constructors
	public NSUrlSessionActiveTasks2 (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
	// properties
	public NSUrlSessionTask[] DataTasks { get; set; }
	public NSUrlSessionTask[] DownloadTasks { get; set; }
	public NSUrlSessionTask[] UploadTasks { get; set; }
}
```

### New Type MonoTouch.Foundation.NSUrlSessionPendingTasks2

```
public sealed delegate NSUrlSessionPendingTasks2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionPendingTasks2 (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GLKView.GLKViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static GLKView.GLKViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static ADBannerView.ADBannerViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static ADBannerView.ADBannerViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKCircleView.MKCircleViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKCircleView.MKCircleViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKMapView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKMapView.MKMapViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MKMapView.MKMapViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKOverlayView.MKOverlayViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPolygonView.MKPolygonViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPolylineView.MKPolylineViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

Added methods:

```
public static MPVolumeView.MPVolumeViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

Added methods:

```
public static SCNView.SCNViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static SCNView.SCNViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static SKView.SKViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static SKView.SKViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIActionSheet

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIActionSheet.UIActionSheetAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIActionSheet.UIActionSheetAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIAlertView.UIAlertViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIAlertView.UIAlertViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance (UITraitCollection traits);
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIBarItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIBarItem.UIBarItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIBarItem.UIBarItemAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIButton

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UIButton.UIButtonAppearance GetAppearance (UITraitCollection traits);
	public static UIButton.UIButtonAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionView.UICollectionViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UICollectionView.UICollectionViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance (UITraitCollection traits);
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIControl.UIControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIControl.UIControlAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIDatePicker.UIDatePickerAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIDatePicker.UIDatePickerAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIImageView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIImageView.UIImageViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIImageView.UIImageViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIInputView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIInputView.UIInputViewAppearance GetAppearance (UITraitCollection traits);
	public static UIInputView.UIInputViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UILabel

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UILabel.UILabelAppearance GetAppearance (UITraitCollection traits);
	public static UILabel.UILabelAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UINavigationBar.UINavigationBarAppearance GetAppearance (UITraitCollection traits);
	public static UINavigationBar.UINavigationBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIPageControl.UIPageControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPageControl.UIPageControlAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UIPickerView.UIPickerViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPickerView.UIPickerViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIProgressView.UIProgressViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIProgressView.UIProgressViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIRefreshControl.UIRefreshControlAppearance GetAppearance (UITraitCollection traits);
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIScrollView.UIScrollViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIScrollView.UIScrollViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISearchBar.UISearchBarAppearance GetAppearance (UITraitCollection traits);
	public static UISearchBar.UISearchBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISegmentedControl.UISegmentedControlAppearance GetAppearance (UITraitCollection traits);
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISlider

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISlider.UISliderAppearance GetAppearance (UITraitCollection traits);
	public static UISlider.UISliderAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIStepper

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIStepper.UIStepperAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIStepper.UIStepperAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISwitch

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UISwitch.UISwitchAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UISwitch.UISwitchAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITabBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITabBar.UITabBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITabBar.UITabBarAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITabBarItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITabBarItem.UITabBarItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITabBarItem.UITabBarItemAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITableView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableView.UITableViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableView.UITableViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableViewCell.UITableViewCellAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableViewCell.UITableViewCellAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITextField

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITextField.UITextFieldAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITextField.UITextFieldAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UITextView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UITextView.UITextViewAppearance GetAppearance (UITraitCollection traits);
	public static UITextView.UITextViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIToolbar.UIToolbarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIToolbar.UIToolbarAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIView.UIViewAppearance GetAppearance (UITraitCollection traits);
	public static UIView.UIViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance (UITraitCollection traits);
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIWebView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIWebView.UIWebViewAppearance GetAppearance (UITraitCollection traits);
	public static UIWebView.UIWebViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIWindow

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIWindow.UIWindowAppearance GetAppearance (UITraitCollection traits);
	public static UIWindow.UIWindowAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.WebKit

### Type Changed: MonoTouch.WebKit.WKWebView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static WKWebView.WKWebViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static WKWebView.WKWebViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

   


 <hr>

# Xamarin.iOS.dll

## Namespace AddressBookUI

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
```

Added methods:

```
public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
```

## Namespace CoreAudioKit

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance (UIKit.UITraitCollection traits);
```

## Namespace EventKitUI

### Type Changed: EventKitUI.EKEventEditViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace Foundation

### Type Changed: Foundation.NSUrlSession

Obsoleted methods:

```
[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
	[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual System.Threading.Tasks.Task<NSUrlSessionActiveTasks> GetTasksAsync ();
```

Added methods:

```
public void GetTasks2 (NSUrlSessionPendingTasks2 completionHandler);
	public System.Threading.Tasks.Task<NSUrlSessionActiveTasks2> GetTasks2Async ();
```

### New Type Foundation.NSUrlSessionActiveTasks2

```
public class NSUrlSessionActiveTasks2 {
	// constructors
	public NSUrlSessionActiveTasks2 (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
	// properties
	public NSUrlSessionTask[] DataTasks { get; set; }
	public NSUrlSessionTask[] DownloadTasks { get; set; }
	public NSUrlSessionTask[] UploadTasks { get; set; }
}
```

### New Type Foundation.NSUrlSessionPendingTasks2

```
public sealed delegate NSUrlSessionPendingTasks2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionPendingTasks2 (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
}
```

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: GameKit.GKFriendRequestComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
```

### Type Changed: GameKit.GKLeaderboardViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace GLKit

### Type Changed: GLKit.GLKView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static GLKView.GLKViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static GLKView.GLKViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static GLKView.GLKViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static GLKView.GLKViewAppearance GetAppearance (UIKit.UITraitCollection traits);
```

## Namespace iAd

### Type Changed: iAd.ADBannerView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static ADBannerView.ADBannerViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static ADBannerView.ADBannerViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MapKit

### Type Changed: MapKit.MKAnnotationView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits);
```

### Type Changed: MapKit.MKCircleView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKCircleView.MKCircleViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKCircleView.MKCircleViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKMapView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
```

Added methods:

```
public static MKMapView.MKMapViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKMapView.MKMapViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKOverlayPathView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance (UIKit.UITraitCollection traits);
```

### Type Changed: MapKit.MKOverlayView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKOverlayView.MKOverlayViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKPinAnnotationView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKPolygonView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPolygonView.MKPolygonViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKPolylineView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKPolylineView.MKPolylineViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MapKit.MKUserTrackingBarButtonItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPVolumeView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
```

Added methods:

```
public static MPVolumeView.MPVolumeViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MessageUI

### Type Changed: MessageUI.MFMailComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
```

### Type Changed: MessageUI.MFMessageComposeViewController

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance (UIKit.UITraitCollection traits);
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.6.1" "8.6.2";
```

## Namespace SceneKit

### Type Changed: SceneKit.SCNView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static SCNView.SCNViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static SCNView.SCNViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
```

Added methods:

```
public static SCNView.SCNViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static SCNView.SCNViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace SpriteKit

### Type Changed: SpriteKit.SKView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static SKView.SKViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static SKView.SKViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static SKView.SKViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static SKView.SKViewAppearance GetAppearance (UIKit.UITraitCollection traits);
```

## Namespace UIKit

### Type Changed: UIKit.UIActionSheet

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIActionSheet.UIActionSheetAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIActionSheet.UIActionSheetAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIActivityIndicatorView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIAlertView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIAlertView.UIAlertViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIAlertView.UIAlertViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIBarButtonItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance (UITraitCollection traits);
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIBarItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIBarItem.UIBarItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIBarItem.UIBarItemAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIButton

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UIButton.UIButtonAppearance GetAppearance (UITraitCollection traits);
	public static UIButton.UIButtonAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UICollectionReusableView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UICollectionView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionView.UICollectionViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UICollectionView.UICollectionViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UICollectionViewCell

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance (UITraitCollection traits);
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIControl.UIControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIControl.UIControlAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIDatePicker

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIDatePicker.UIDatePickerAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIDatePicker.UIDatePickerAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIImageView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIImageView.UIImageViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIImageView.UIImageViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIInputView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIInputView.UIInputViewAppearance GetAppearance (UITraitCollection traits);
	public static UIInputView.UIInputViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UILabel

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UILabel.UILabelAppearance GetAppearance (UITraitCollection traits);
	public static UILabel.UILabelAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UINavigationBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UINavigationBar.UINavigationBarAppearance GetAppearance (UITraitCollection traits);
	public static UINavigationBar.UINavigationBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIPageControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIPageControl.UIPageControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPageControl.UIPageControlAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIPickerView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UIPickerView.UIPickerViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPickerView.UIPickerViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIPopoverBackgroundView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIProgressView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIProgressView.UIProgressViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIProgressView.UIProgressViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIRefreshControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIRefreshControl.UIRefreshControlAppearance GetAppearance (UITraitCollection traits);
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIScrollView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIScrollView.UIScrollViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIScrollView.UIScrollViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UISearchBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISearchBar.UISearchBarAppearance GetAppearance (UITraitCollection traits);
	public static UISearchBar.UISearchBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UISegmentedControl

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISegmentedControl.UISegmentedControlAppearance GetAppearance (UITraitCollection traits);
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UISlider

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UISlider.UISliderAppearance GetAppearance (UITraitCollection traits);
	public static UISlider.UISliderAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIStepper

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIStepper.UIStepperAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIStepper.UIStepperAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UISwitch

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UISwitch.UISwitchAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UISwitch.UISwitchAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITabBar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITabBar.UITabBarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITabBar.UITabBarAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITabBarItem

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITabBarItem.UITabBarItemAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITabBarItem.UITabBarItemAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITableView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableView.UITableViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableView.UITableViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITableViewCell

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableViewCell.UITableViewCellAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableViewCell.UITableViewCellAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITableViewHeaderFooterView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITextField

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UITextField.UITextFieldAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UITextField.UITextFieldAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UITextView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	[Obsolete ("Use the non-generic overload instead"]
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits);
```

Added methods:

```
public static UITextView.UITextViewAppearance GetAppearance (UITraitCollection traits);
	public static UITextView.UITextViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIToolbar

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIToolbar.UIToolbarAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
	public static UIToolbar.UIToolbarAppearance GetAppearance (UITraitCollection traits);
```

### Type Changed: UIKit.UIView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIView.UIViewAppearance GetAppearance (UITraitCollection traits);
	public static UIView.UIViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIVisualEffectView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance (UITraitCollection traits);
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIWebView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIWebView.UIWebViewAppearance GetAppearance (UITraitCollection traits);
	public static UIWebView.UIWebViewAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: UIKit.UIWindow

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static UIWindow.UIWindowAppearance GetAppearance (UITraitCollection traits);
	public static UIWindow.UIWindowAppearance GetAppearance (UITraitCollection traits, System.Type[] containers);
```

## Namespace WebKit

### Type Changed: WebKit.WKWebView

Obsoleted methods:

```
[Obsolete ("Use the non-generic overload instead"]
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits);
	[Obsolete ("Use the non-generic overload instead"]
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (UIKit.UITraitCollection traits, System.Type[] containers);
```

Added methods:

```
public static WKWebView.WKWebViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static WKWebView.WKWebViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
```

   


 <hr>
