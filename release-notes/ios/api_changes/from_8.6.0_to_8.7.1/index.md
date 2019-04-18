---
id: A9230FAA-2152-4102-8985-3C83B8D405EF
title: "From 8.6.0 to 8.7.1"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.6.0" "8.7.1";
```

Added field:

```
public static const string WatchKitLibrary = "/System/Library/Frameworks/WatchKit.framework/WatchKit";
```

## Namespace MonoTouch.Accounts

### Type Changed: MonoTouch.Accounts.ACErrorCode

Obsoleted fields:

```
[Obsolete ("Use MissingTransportMessageId"]
	MissingMessageID = 21,
```

Added value:

```
MissingTransportMessageId = 21,
```

## Namespace MonoTouch.CoreFoundation

### New Type MonoTouch.CoreFoundation.CFNotificationCenter

```
public class CFNotificationCenter : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public static CFNotificationCenter Darwin { get; }
	public virtual IntPtr Handle { get; }
	public static CFNotificationCenter Local { get; }
	// methods
	protected override void ~CFNotificationCenter ();
	public CFNotificationObserverToken AddObserver (string name, MonoTouch.ObjCRuntime.INativeObject objectToObserve, System.Action<System.String,MonoTouch.Foundation.NSDictionary> notificationHandler, CFNotificationSuspensionBehavior suspensionBehavior);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void PostNotification (string notification, MonoTouch.ObjCRuntime.INativeObject objectToObserve, MonoTouch.Foundation.NSDictionary userInfo, bool deliverImmediately, bool postOnAllSessions);
	public void RemoveEveryObserver ();
	public void RemoveObserver (CFNotificationObserverToken token);
}
```

### New Type MonoTouch.CoreFoundation.CFNotificationObserverToken

```
public class CFNotificationObserverToken {
}
```

### New Type MonoTouch.CoreFoundation.CFNotificationSuspensionBehavior

```
[Serializable]
public enum CFNotificationSuspensionBehavior {
	Coalesce = 2,
	DeliverImmediately = 4,
	Drop = 1,
	Hold = 3,
}
```

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMError

Added values:

```
InvalidAction = 108,
	NotAuthorized = 111,
	NotAvailable = 109,
	NotEntitled = 110,
```

## Namespace MonoTouch.ExternalAccessory

### Type Changed: MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser

Added method:

```
public virtual void ConfigureAccessory (EAWiFiUnconfiguredAccessory accessory, MonoTouch.UIKit.UIViewController viewController);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSError

Added property:

```
public static NSString WatchKitErrorDomain { get; }
```

### Type Changed: MonoTouch.Foundation.NSExtensionContext

Added properties:

```
public static NSString HostDidBecomeActiveNotification { get; }
	public static NSString HostDidEnterBackgroundNotification { get; }
	public static NSString HostWillEnterForegroundNotification { get; }
	public static NSString HostWillResignActiveNotification { get; }
```

### Type Changed: MonoTouch.Foundation.NSProcessInfo

Added method:

```
public virtual void PerformExpiringActivity (string reason, System.Action<bool> block);
```

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKBiologicalSex

Added value:

```
Other = 3,
```

### Type Changed: MonoTouch.HealthKit.HKHealthStore

Added property:

```
public static MonoTouch.Foundation.NSString UserPreferencesDidChangeNotification { get; }
```

Added methods:

```
public virtual void GetPreferredUnits (MonoTouch.Foundation.NSSet quantityTypes, System.Action<MonoTouch.Foundation.NSDictionary,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<MonoTouch.Foundation.NSDictionary> GetPreferredUnitsAsync (MonoTouch.Foundation.NSSet quantityTypes);
```

### Type Changed: MonoTouch.HealthKit.HKUnit

Added interface:

```
MonoTouch.Foundation.INSCopying
```

Added method:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.HealthKit.HKWorkoutActivityType

Added value:

```
Other = 3000,
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPFeedbackCommand

Added property:

```
public virtual string LocalizedShortTitle { get; set; }
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added method:

```
public virtual void HandleWatchKitExtensionRequest (UIApplication application, MonoTouch.Foundation.NSDictionary userInfo, System.Action<MonoTouch.Foundation.NSDictionary> reply);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Added method:

```
public static void HandleWatchKitExtensionRequest (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSDictionary userInfo, System.Action<MonoTouch.Foundation.NSDictionary> reply);
```

### Type Changed: MonoTouch.UIKit.UIFont

Added methods:

```
public static UIFont SystemFontOfSize (float size, UIFontWeight weight);
	public static UIFont SystemFontOfSize (float size, float weight);
```

### Type Changed: MonoTouch.UIKit.UILocalNotification

Added property:

```
public virtual string AlertTitle { get; set; }
```

### New Type MonoTouch.UIKit.UIFontWeight

```
[Serializable]
public enum UIFontWeight {
	Black = 8,
	Bold = 6,
	Heavy = 7,
	Light = 2,
	Medium = 4,
	Regular = 3,
	Semibold = 5,
	Thin = 1,
	UltraLight = 0,
}
```

## New Namespace MonoTouch.WatchKit

### New Type MonoTouch.WatchKit.WKAccessibility

```
public static class WKAccessibility {
	// methods
	public static void SetAccessibilityHint (WKInterfaceObject This, string accessibilityHint);
	public static void SetAccessibilityImageRegions (WKInterfaceObject This, WKAccessibilityImageRegion[] accessibilityImageRegions);
	public static void SetAccessibilityLabel (WKInterfaceObject This, string accessibilityLabel);
	public static void SetAccessibilityTraits (WKInterfaceObject This, MonoTouch.UIKit.UIAccessibilityTrait accessibilityTraits);
	public static void SetAccessibilityValue (WKInterfaceObject This, string accessibilityValue);
	public static void SetIsAccessibilityElement (WKInterfaceObject This, bool isAccessibilityElement);
}
```

### New Type MonoTouch.WatchKit.WKAccessibilityImageRegion

```
public class WKAccessibilityImageRegion : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKAccessibilityImageRegion ();
	public WKAccessibilityImageRegion (MonoTouch.Foundation.NSCoder coder);
	public WKAccessibilityImageRegion (MonoTouch.Foundation.NSObjectFlag t);
	public WKAccessibilityImageRegion (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF Frame { get; set; }
	public virtual string Label { get; set; }
}
```

### New Type MonoTouch.WatchKit.WKErrorCode

```
[Serializable]
public enum WKErrorCode {
	None = 0,
	RequestReplyNotCalledError = 2,
	UnknownError = 1,
}
```

### New Type MonoTouch.WatchKit.WKInterfaceButton

```
public class WKInterfaceButton : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceButton (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceButton (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceButton (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetBackgroundColor (MonoTouch.UIKit.UIColor color);
	public virtual void SetBackgroundImage (MonoTouch.UIKit.UIImage image);
	public virtual void SetBackgroundImage (MonoTouch.Foundation.NSData imageData);
	public virtual void SetBackgroundImage (string imageName);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetTitle (string title);
	public virtual void SetTitle (MonoTouch.Foundation.NSAttributedString attributedTitle);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceController

```
public abstract class WKInterfaceController : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceController ();
	public WKInterfaceController (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceController (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF ContentFrame { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	// methods
	public virtual void AddMenuItem (WKMenuItemIcon itemIcon, string title, MonoTouch.ObjCRuntime.Selector action);
	public virtual void AddMenuItem (MonoTouch.UIKit.UIImage image, string title, MonoTouch.ObjCRuntime.Selector action);
	public virtual void AddMenuItem (string imageName, string title, MonoTouch.ObjCRuntime.Selector action);
	public virtual void Awake (MonoTouch.Foundation.NSObject context);
	public virtual void BecomeCurrentPage ();
	public virtual void ClearAllMenuItems ();
	public virtual void DidDeactivate ();
	public virtual void DidSelectRow (WKInterfaceTable table, int rowIndex);
	public virtual void DismissController ();
	public virtual void DismissTextInputController ();
	public virtual MonoTouch.Foundation.NSObject GetContextForSegue (string segueIdentifier, WKInterfaceTable table, int rowIndex);
	public virtual MonoTouch.Foundation.NSObject GetContextForSegue (string segueIdentifier);
	public virtual MonoTouch.Foundation.NSObject[] GetContextsForSegue (string segueIdentifier);
	public virtual MonoTouch.Foundation.NSObject[] GetContextsForSegue (string segueIdentifier, WKInterfaceTable table, int rowIndex);
	public virtual void HandleLocalNotificationAction (string identifier, MonoTouch.UIKit.UILocalNotification localNotification);
	public virtual void HandleRemoteNotificationAction (string identifier, MonoTouch.Foundation.NSDictionary remoteNotification);
	public virtual void HandleUserActivity (MonoTouch.Foundation.NSDictionary userActivity);
	public virtual void InvalidateUserActivity ();
	public static bool OpenParentApplication (MonoTouch.Foundation.NSDictionary userInfo, System.Action<MonoTouch.Foundation.NSDictionary,MonoTouch.Foundation.NSError> reply);
	public virtual void PopController ();
	public virtual void PopToRootController ();
	public virtual void PresentController (string[] names, MonoTouch.Foundation.NSObject[] contexts);
	public virtual void PresentController (string name, MonoTouch.Foundation.NSObject context);
	public void PresentController (string name, string context);
	public void PresentController (string[] names, string[] contexts);
	public virtual void PresentTextInputController (string[] suggestions, WKTextInputMode inputMode, System.Action<MonoTouch.Foundation.NSArray> completion);
	public virtual void PushController (string name, MonoTouch.Foundation.NSObject context);
	public static void ReloadRootControllers (string[] names, MonoTouch.Foundation.NSObject[] contexts);
	public virtual void SetTitle (string title);
	public virtual void UpdateUserActivity (string type, MonoTouch.Foundation.NSDictionary userInfo, MonoTouch.Foundation.NSUrl webpageURL);
	public virtual void WillActivate ();
}
```

### New Type MonoTouch.WatchKit.WKInterfaceDate

```
public class WKInterfaceDate : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceDate (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceDate (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceDate (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetCalendar (MonoTouch.Foundation.NSCalendar calendar);
	public virtual void SetTextColor (MonoTouch.UIKit.UIColor color);
	public virtual void SetTimeZone (MonoTouch.Foundation.NSTimeZone timeZone);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceDevice

```
public class WKInterfaceDevice : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceDevice (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceDevice (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceDevice (IntPtr handle);
	// properties
	public System.Collections.Generic.IReadOnlyDictionary<System.String,System.Int64> CachedImages { get; }
	public override IntPtr ClassHandle { get; }
	public static WKInterfaceDevice CurrentDevice { get; }
	public MonoTouch.UIKit.UIContentSizeCategory PreferredContentSizeCategory { get; }
	public virtual System.Drawing.RectangleF ScreenBounds { get; }
	public virtual float ScreenScale { get; }
	public virtual MonoTouch.Foundation.NSDictionary WeakCachedImages { get; }
	// methods
	public virtual bool AddCachedImage (MonoTouch.UIKit.UIImage image, string name);
	public virtual bool AddCachedImage (MonoTouch.Foundation.NSData imageData, string name);
	protected override void Dispose (bool disposing);
	public virtual void RemoveAllCachedImages ();
	public virtual void RemoveCachedImage (string name);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceGroup

```
public class WKInterfaceGroup : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceGroup (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceGroup (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetBackgroundColor (MonoTouch.UIKit.UIColor color);
	public virtual void SetBackgroundImage (string imageName);
	public virtual void SetBackgroundImage (MonoTouch.Foundation.NSData imageData);
	public virtual void SetBackgroundImage (MonoTouch.UIKit.UIImage image);
	public virtual void SetCornerRadius (float cornerRadius);
	public virtual void StartAnimating ();
	public virtual void StartAnimating (MonoTouch.Foundation.NSRange imageRange, double duration, int repeatCount);
	public virtual void StopAnimating ();
}
```

### New Type MonoTouch.WatchKit.WKInterfaceImage

```
public class WKInterfaceImage : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceImage (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceImage (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceImage (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetImage (MonoTouch.UIKit.UIImage image);
	public virtual void SetImage (MonoTouch.Foundation.NSData imageData);
	public virtual void SetImage (string imageName);
	public virtual void SetTintColor (MonoTouch.UIKit.UIColor color);
	public virtual void StartAnimating ();
	public virtual void StartAnimating (MonoTouch.Foundation.NSRange imageRange, double duration, int repeatCount);
	public virtual void StopAnimating ();
}
```

### New Type MonoTouch.WatchKit.WKInterfaceLabel

```
public class WKInterfaceLabel : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceLabel (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceLabel (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceLabel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetAttributedText (MonoTouch.Foundation.NSAttributedString attributedText);
	public virtual void SetText (string text);
	public virtual void SetTextColor (MonoTouch.UIKit.UIColor color);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceMap

```
public class WKInterfaceMap : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceMap (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceMap (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceMap (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddAnnotation (MonoTouch.CoreLocation.CLLocationCoordinate2D location, MonoTouch.UIKit.UIImage image, System.Drawing.PointF offset);
	public virtual void AddAnnotation (MonoTouch.CoreLocation.CLLocationCoordinate2D location, string name, System.Drawing.PointF offset);
	public virtual void AddAnnotation (MonoTouch.CoreLocation.CLLocationCoordinate2D location, WKInterfaceMapPinColor pinColor);
	public virtual void RemoveAllAnnotations ();
	public virtual void SetRegion (MonoTouch.MapKit.MKCoordinateRegion coordinateRegion);
	public virtual void SetVisible (MonoTouch.MapKit.MKMapRect mapRect);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceMapPinColor

```
[Serializable]
public enum WKInterfaceMapPinColor {
	Green = 1,
	Purple = 2,
	Red = 0,
}
```

### New Type MonoTouch.WatchKit.WKInterfaceObject

```
public class WKInterfaceObject : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceObject (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceObject (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceObject (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string InterfaceProperty { get; }
	// methods
	public virtual void SetAlpha (float alpha);
	public virtual void SetHeight (float height);
	public virtual void SetHidden (bool hidden);
	public virtual void SetWidth (float width);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceSeparator

```
public class WKInterfaceSeparator : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceSeparator (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceSeparator (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceSeparator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (MonoTouch.UIKit.UIColor color);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceSlider

```
public class WKInterfaceSlider : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceSlider (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceSlider (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceSlider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (MonoTouch.UIKit.UIColor color);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetNumberOfSteps (int numberOfSteps);
	public virtual void SetValue (float value);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceSwitch

```
public class WKInterfaceSwitch : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceSwitch (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceSwitch (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceSwitch (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (MonoTouch.UIKit.UIColor color);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetOn (bool on);
	public virtual void SetTitle (string title);
	public virtual void SetTitle (MonoTouch.Foundation.NSAttributedString attributedTitle);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceTable

```
public class WKInterfaceTable : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceTable (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceTable (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceTable (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual int NumberOfRows { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject GetRowController (int index);
	public virtual void InsertRows (MonoTouch.Foundation.NSIndexSet rowIndexes, string rowType);
	public virtual void RemoveRows (MonoTouch.Foundation.NSIndexSet rowIndexes);
	public virtual void ScrollToRow (int index);
	public virtual void SetNumberOfRows (int numberOfRows, string rowType);
	public virtual void SetRowTypes (string[] rowTypes);
}
```

### New Type MonoTouch.WatchKit.WKInterfaceTimer

```
public class WKInterfaceTimer : MonoTouch.WatchKit.WKInterfaceObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKInterfaceTimer (MonoTouch.Foundation.NSCoder coder);
	public WKInterfaceTimer (MonoTouch.Foundation.NSObjectFlag t);
	public WKInterfaceTimer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetDate (MonoTouch.Foundation.NSDate date);
	public virtual void SetTextColor (MonoTouch.UIKit.UIColor color);
	public virtual void Start ();
	public virtual void Stop ();
}
```

### New Type MonoTouch.WatchKit.WKMenuItemIcon

```
[Serializable]
public enum WKMenuItemIcon {
	Accept = 0,
	Add = 1,
	Block = 2,
	Decline = 3,
	Info = 4,
	Maybe = 5,
	More = 6,
	Mute = 7,
	Pause = 8,
	Play = 9,
	Repeat = 10,
	Resume = 11,
	Share = 12,
	Shuffle = 13,
	Speaker = 14,
	Trash = 15,
}
```

### New Type MonoTouch.WatchKit.WKTextInputMode

```
[Serializable]
public enum WKTextInputMode {
	AllowAnimatedEmoji = 2,
	AllowEmoji = 1,
	Plain = 0,
}
```

### New Type MonoTouch.WatchKit.WKUserNotificationInterfaceController

```
public class WKUserNotificationInterfaceController : MonoTouch.WatchKit.WKInterfaceController, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public WKUserNotificationInterfaceController ();
	public WKUserNotificationInterfaceController (MonoTouch.Foundation.NSCoder coder);
	public WKUserNotificationInterfaceController (MonoTouch.Foundation.NSObjectFlag t);
	public WKUserNotificationInterfaceController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void DidReceiveLocalNotification (MonoTouch.UIKit.UILocalNotification localNotification, System.Action<WKUserNotificationInterfaceType> completionHandler);
	public virtual void DidReceiveRemoteNotification (MonoTouch.Foundation.NSDictionary remoteNotification, System.Action<WKUserNotificationInterfaceType> completionHandler);
}
```

### New Type MonoTouch.WatchKit.WKUserNotificationInterfaceType

```
[Serializable]
public enum WKUserNotificationInterfaceType {
	Custom = 1,
	Default = 0,
}
```

   


 <hr>

# Xamarin.iOS.dll

## Namespace Accounts

### Type Changed: Accounts.ACErrorCode

Obsoleted fields:

```
[Obsolete ("Use MissingTransportMessageId"]
	MissingMessageID = 21,
```

Added value:

```
MissingTransportMessageId = 21,
```

## Namespace CoreFoundation

### New Type CoreFoundation.CFNotificationCenter

```
public class CFNotificationCenter : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public static CFNotificationCenter Darwin { get; }
	public virtual IntPtr Handle { get; }
	public static CFNotificationCenter Local { get; }
	// methods
	protected override void ~CFNotificationCenter ();
	public CFNotificationObserverToken AddObserver (string name, ObjCRuntime.INativeObject objectToObserve, System.Action<System.String,Foundation.NSDictionary> notificationHandler, CFNotificationSuspensionBehavior suspensionBehavior);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void PostNotification (string notification, ObjCRuntime.INativeObject objectToObserve, Foundation.NSDictionary userInfo, bool deliverImmediately, bool postOnAllSessions);
	public void RemoveEveryObserver ();
	public void RemoveObserver (CFNotificationObserverToken token);
}
```

### New Type CoreFoundation.CFNotificationObserverToken

```
public class CFNotificationObserverToken {
}
```

### New Type CoreFoundation.CFNotificationSuspensionBehavior

```
[Serializable]
public enum CFNotificationSuspensionBehavior {
	Coalesce = 2,
	DeliverImmediately = 4,
	Drop = 1,
	Hold = 3,
}
```

## Namespace CoreMotion

### Type Changed: CoreMotion.CMError

Added values:

```
InvalidAction = 108,
	NotAuthorized = 111,
	NotAvailable = 109,
	NotEntitled = 110,
```

## Namespace ExternalAccessory

### Type Changed: ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser

Added method:

```
public virtual void ConfigureAccessory (EAWiFiUnconfiguredAccessory accessory, UIKit.UIViewController viewController);
```

## Namespace Foundation

### Type Changed: Foundation.NSError

Added property:

```
public static NSString WatchKitErrorDomain { get; }
```

### Type Changed: Foundation.NSExtensionContext

Added properties:

```
public static NSString HostDidBecomeActiveNotification { get; }
	public static NSString HostDidEnterBackgroundNotification { get; }
	public static NSString HostWillEnterForegroundNotification { get; }
	public static NSString HostWillResignActiveNotification { get; }
```

### Type Changed: Foundation.NSProcessInfo

Added method:

```
public virtual void PerformExpiringActivity (string reason, System.Action<bool> block);
```

## Namespace HealthKit

### Type Changed: HealthKit.HKBiologicalSex

Added value:

```
Other = 3,
```

### Type Changed: HealthKit.HKHealthStore

Added property:

```
public static Foundation.NSString UserPreferencesDidChangeNotification { get; }
```

Added methods:

```
public virtual void GetPreferredUnits (Foundation.NSSet quantityTypes, System.Action<Foundation.NSDictionary,Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<Foundation.NSDictionary> GetPreferredUnitsAsync (Foundation.NSSet quantityTypes);
```

### Type Changed: HealthKit.HKUnit

Added interface:

```
Foundation.INSCopying
```

Added method:

```
public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
```

### Type Changed: HealthKit.HKWorkoutActivityType

Added value:

```
Other = 3000,
```

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPFeedbackCommand

Added property:

```
public virtual string LocalizedShortTitle { get; set; }
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.6.0" "8.7.1";
```

Added field:

```
public static const string WatchKitLibrary = "/System/Library/Frameworks/WatchKit.framework/WatchKit";
```

## Namespace UIKit

### Type Changed: UIKit.UIApplicationDelegate

Added method:

```
public virtual void HandleWatchKitExtensionRequest (UIApplication application, Foundation.NSDictionary userInfo, System.Action<Foundation.NSDictionary> reply);
```

### Type Changed: UIKit.UIApplicationDelegate_Extensions

Added method:

```
public static void HandleWatchKitExtensionRequest (IUIApplicationDelegate This, UIApplication application, Foundation.NSDictionary userInfo, System.Action<Foundation.NSDictionary> reply);
```

### Type Changed: UIKit.UIFont

Added methods:

```
public static UIFont SystemFontOfSize (nfloat size, UIFontWeight weight);
	public static UIFont SystemFontOfSize (nfloat size, nfloat weight);
```

### Type Changed: UIKit.UILocalNotification

Added property:

```
public virtual string AlertTitle { get; set; }
```

### New Type UIKit.UIFontWeight

```
[Serializable]
public enum UIFontWeight {
	Black = 8,
	Bold = 6,
	Heavy = 7,
	Light = 2,
	Medium = 4,
	Regular = 3,
	Semibold = 5,
	Thin = 1,
	UltraLight = 0,
}
```

## New Namespace WatchKit

### New Type WatchKit.WKAccessibility

```
public static class WKAccessibility {
	// methods
	public static void SetAccessibilityHint (WKInterfaceObject This, string accessibilityHint);
	public static void SetAccessibilityImageRegions (WKInterfaceObject This, WKAccessibilityImageRegion[] accessibilityImageRegions);
	public static void SetAccessibilityLabel (WKInterfaceObject This, string accessibilityLabel);
	public static void SetAccessibilityTraits (WKInterfaceObject This, UIKit.UIAccessibilityTrait accessibilityTraits);
	public static void SetAccessibilityValue (WKInterfaceObject This, string accessibilityValue);
	public static void SetIsAccessibilityElement (WKInterfaceObject This, bool isAccessibilityElement);
}
```

### New Type WatchKit.WKAccessibilityImageRegion

```
public class WKAccessibilityImageRegion : Foundation.NSObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public WKAccessibilityImageRegion ();
	protected WKAccessibilityImageRegion (Foundation.NSObjectFlag t);
	protected WKAccessibilityImageRegion (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGRect Frame { get; set; }
	public virtual string Label { get; set; }
}
```

### New Type WatchKit.WKErrorCode

```
[Serializable]
public enum WKErrorCode {
	None = 0,
	RequestReplyNotCalledError = 2,
	UnknownError = 1,
}
```

### New Type WatchKit.WKInterfaceButton

```
public class WKInterfaceButton : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceButton (Foundation.NSObjectFlag t);
	protected WKInterfaceButton (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetBackgroundColor (UIKit.UIColor color);
	public virtual void SetBackgroundImage (UIKit.UIImage image);
	public virtual void SetBackgroundImage (Foundation.NSData imageData);
	public virtual void SetBackgroundImage (string imageName);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetTitle (string title);
	public virtual void SetTitle (Foundation.NSAttributedString attributedTitle);
}
```

### New Type WatchKit.WKInterfaceController

```
public abstract class WKInterfaceController : Foundation.NSObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceController ();
	protected WKInterfaceController (Foundation.NSObjectFlag t);
	protected WKInterfaceController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGRect ContentFrame { get; }
	public static Foundation.NSString ErrorDomain { get; }
	// methods
	public virtual void AddMenuItem (WKMenuItemIcon itemIcon, string title, ObjCRuntime.Selector action);
	public virtual void AddMenuItem (UIKit.UIImage image, string title, ObjCRuntime.Selector action);
	public virtual void AddMenuItem (string imageName, string title, ObjCRuntime.Selector action);
	public virtual void Awake (Foundation.NSObject context);
	public virtual void BecomeCurrentPage ();
	public virtual void ClearAllMenuItems ();
	public virtual void DidDeactivate ();
	public virtual void DidSelectRow (WKInterfaceTable table, nint rowIndex);
	public virtual void DismissController ();
	public virtual void DismissTextInputController ();
	public virtual Foundation.NSObject GetContextForSegue (string segueIdentifier, WKInterfaceTable table, nint rowIndex);
	public virtual Foundation.NSObject GetContextForSegue (string segueIdentifier);
	public virtual Foundation.NSObject[] GetContextsForSegue (string segueIdentifier);
	public virtual Foundation.NSObject[] GetContextsForSegue (string segueIdentifier, WKInterfaceTable table, nint rowIndex);
	public virtual void HandleLocalNotificationAction (string identifier, UIKit.UILocalNotification localNotification);
	public virtual void HandleRemoteNotificationAction (string identifier, Foundation.NSDictionary remoteNotification);
	public virtual void HandleUserActivity (Foundation.NSDictionary userActivity);
	public virtual void InvalidateUserActivity ();
	public static bool OpenParentApplication (Foundation.NSDictionary userInfo, System.Action<Foundation.NSDictionary,Foundation.NSError> reply);
	public virtual void PopController ();
	public virtual void PopToRootController ();
	public virtual void PresentController (string[] names, Foundation.NSObject[] contexts);
	public virtual void PresentController (string name, Foundation.NSObject context);
	public void PresentController (string name, string context);
	public void PresentController (string[] names, string[] contexts);
	public virtual void PresentTextInputController (string[] suggestions, WKTextInputMode inputMode, System.Action<Foundation.NSArray> completion);
	public virtual void PushController (string name, Foundation.NSObject context);
	public static void ReloadRootControllers (string[] names, Foundation.NSObject[] contexts);
	public virtual void SetTitle (string title);
	public virtual void UpdateUserActivity (string type, Foundation.NSDictionary userInfo, Foundation.NSUrl webpageURL);
	public virtual void WillActivate ();
}
```

### New Type WatchKit.WKInterfaceDate

```
public class WKInterfaceDate : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceDate (Foundation.NSObjectFlag t);
	protected WKInterfaceDate (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetCalendar (Foundation.NSCalendar calendar);
	public virtual void SetTextColor (UIKit.UIColor color);
	public virtual void SetTimeZone (Foundation.NSTimeZone timeZone);
}
```

### New Type WatchKit.WKInterfaceDevice

```
public class WKInterfaceDevice : Foundation.NSObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceDevice (Foundation.NSObjectFlag t);
	protected WKInterfaceDevice (IntPtr handle);
	// properties
	public System.Collections.Generic.IReadOnlyDictionary<System.String,System.Int64> CachedImages { get; }
	public override IntPtr ClassHandle { get; }
	public static WKInterfaceDevice CurrentDevice { get; }
	public UIKit.UIContentSizeCategory PreferredContentSizeCategory { get; }
	public virtual CoreGraphics.CGRect ScreenBounds { get; }
	public virtual nfloat ScreenScale { get; }
	public virtual Foundation.NSDictionary WeakCachedImages { get; }
	// methods
	public virtual bool AddCachedImage (UIKit.UIImage image, string name);
	public virtual bool AddCachedImage (Foundation.NSData imageData, string name);
	protected override void Dispose (bool disposing);
	public virtual void RemoveAllCachedImages ();
	public virtual void RemoveCachedImage (string name);
}
```

### New Type WatchKit.WKInterfaceGroup

```
public class WKInterfaceGroup : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceGroup (Foundation.NSObjectFlag t);
	protected WKInterfaceGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetBackgroundColor (UIKit.UIColor color);
	public virtual void SetBackgroundImage (string imageName);
	public virtual void SetBackgroundImage (Foundation.NSData imageData);
	public virtual void SetBackgroundImage (UIKit.UIImage image);
	public virtual void SetCornerRadius (nfloat cornerRadius);
	public virtual void StartAnimating ();
	public virtual void StartAnimating (Foundation.NSRange imageRange, double duration, nint repeatCount);
	public virtual void StopAnimating ();
}
```

### New Type WatchKit.WKInterfaceImage

```
public class WKInterfaceImage : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceImage (Foundation.NSObjectFlag t);
	protected WKInterfaceImage (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetImage (UIKit.UIImage image);
	public virtual void SetImage (Foundation.NSData imageData);
	public virtual void SetImage (string imageName);
	public virtual void SetTintColor (UIKit.UIColor color);
	public virtual void StartAnimating ();
	public virtual void StartAnimating (Foundation.NSRange imageRange, double duration, nint repeatCount);
	public virtual void StopAnimating ();
}
```

### New Type WatchKit.WKInterfaceLabel

```
public class WKInterfaceLabel : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceLabel (Foundation.NSObjectFlag t);
	protected WKInterfaceLabel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetAttributedText (Foundation.NSAttributedString attributedText);
	public virtual void SetText (string text);
	public virtual void SetTextColor (UIKit.UIColor color);
}
```

### New Type WatchKit.WKInterfaceMap

```
public class WKInterfaceMap : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceMap (Foundation.NSObjectFlag t);
	protected WKInterfaceMap (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void AddAnnotation (CoreLocation.CLLocationCoordinate2D location, UIKit.UIImage image, CoreGraphics.CGPoint offset);
	public virtual void AddAnnotation (CoreLocation.CLLocationCoordinate2D location, string name, CoreGraphics.CGPoint offset);
	public virtual void AddAnnotation (CoreLocation.CLLocationCoordinate2D location, WKInterfaceMapPinColor pinColor);
	public virtual void RemoveAllAnnotations ();
	public virtual void SetRegion (MapKit.MKCoordinateRegion coordinateRegion);
	public virtual void SetVisible (MapKit.MKMapRect mapRect);
}
```

### New Type WatchKit.WKInterfaceMapPinColor

```
[Serializable]
public enum WKInterfaceMapPinColor {
	Green = 1,
	Purple = 2,
	Red = 0,
}
```

### New Type WatchKit.WKInterfaceObject

```
public class WKInterfaceObject : Foundation.NSObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceObject (Foundation.NSObjectFlag t);
	protected WKInterfaceObject (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string InterfaceProperty { get; }
	// methods
	public virtual void SetAlpha (nfloat alpha);
	public virtual void SetHeight (nfloat height);
	public virtual void SetHidden (bool hidden);
	public virtual void SetWidth (nfloat width);
}
```

### New Type WatchKit.WKInterfaceSeparator

```
public class WKInterfaceSeparator : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceSeparator (Foundation.NSObjectFlag t);
	protected WKInterfaceSeparator (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (UIKit.UIColor color);
}
```

### New Type WatchKit.WKInterfaceSlider

```
public class WKInterfaceSlider : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceSlider (Foundation.NSObjectFlag t);
	protected WKInterfaceSlider (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (UIKit.UIColor color);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetNumberOfSteps (nint numberOfSteps);
	public virtual void SetValue (float value);
}
```

### New Type WatchKit.WKInterfaceSwitch

```
public class WKInterfaceSwitch : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceSwitch (Foundation.NSObjectFlag t);
	protected WKInterfaceSwitch (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetColor (UIKit.UIColor color);
	public virtual void SetEnabled (bool enabled);
	public virtual void SetOn (bool on);
	public virtual void SetTitle (string title);
	public virtual void SetTitle (Foundation.NSAttributedString attributedTitle);
}
```

### New Type WatchKit.WKInterfaceTable

```
public class WKInterfaceTable : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceTable (Foundation.NSObjectFlag t);
	protected WKInterfaceTable (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint NumberOfRows { get; }
	// methods
	public virtual Foundation.NSObject GetRowController (nint index);
	public virtual void InsertRows (Foundation.NSIndexSet rowIndexes, string rowType);
	public virtual void RemoveRows (Foundation.NSIndexSet rowIndexes);
	public virtual void ScrollToRow (nint index);
	public virtual void SetNumberOfRows (nint numberOfRows, string rowType);
	public virtual void SetRowTypes (string[] rowTypes);
}
```

### New Type WatchKit.WKInterfaceTimer

```
public class WKInterfaceTimer : WatchKit.WKInterfaceObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	protected WKInterfaceTimer (Foundation.NSObjectFlag t);
	protected WKInterfaceTimer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SetDate (Foundation.NSDate date);
	public virtual void SetTextColor (UIKit.UIColor color);
	public virtual void Start ();
	public virtual void Stop ();
}
```

### New Type WatchKit.WKMenuItemIcon

```
[Serializable]
public enum WKMenuItemIcon {
	Accept = 0,
	Add = 1,
	Block = 2,
	Decline = 3,
	Info = 4,
	Maybe = 5,
	More = 6,
	Mute = 7,
	Pause = 8,
	Play = 9,
	Repeat = 10,
	Resume = 11,
	Share = 12,
	Shuffle = 13,
	Speaker = 14,
	Trash = 15,
}
```

### New Type WatchKit.WKTextInputMode

```
[Serializable]
public enum WKTextInputMode {
	AllowAnimatedEmoji = 2,
	AllowEmoji = 1,
	Plain = 0,
}
```

### New Type WatchKit.WKUserNotificationInterfaceController

```
public class WKUserNotificationInterfaceController : WatchKit.WKInterfaceController, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public WKUserNotificationInterfaceController ();
	protected WKUserNotificationInterfaceController (Foundation.NSObjectFlag t);
	protected WKUserNotificationInterfaceController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void DidReceiveLocalNotification (UIKit.UILocalNotification localNotification, System.Action<WKUserNotificationInterfaceType> completionHandler);
	public virtual void DidReceiveRemoteNotification (Foundation.NSDictionary remoteNotification, System.Action<WKUserNotificationInterfaceType> completionHandler);
}
```

### New Type WatchKit.WKUserNotificationInterfaceType

```
[Serializable]
public enum WKUserNotificationInterfaceType {
	Custom = 1,
	Default = 0,
}
```

   


 <hr>
