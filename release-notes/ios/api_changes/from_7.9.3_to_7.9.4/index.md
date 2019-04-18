---
id: AEA04F52-3AC2-4A9B-A8DA-35F1BB031913
title: "From 7.9.3 to 7.9.4"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "7.9.3";
```

Added field:

```
public static const string Version = "7.9.4";
```

### Removed Type MonoTouch.MonoTouchException ### New Type MonoTouch.RuntimeException

```
public class RuntimeException : System.Exception, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	public RuntimeException (string message, object[] args);
	public RuntimeException (int code, string message, object[] args);
	public RuntimeException (int code, bool error, string message, object[] args);
	public RuntimeException (int code, bool error, System.Exception innerException, string message, object[] args);
	// properties
	public int Code { get; }
	public bool Error { get; }
}
```



## Namespace MonoTouch.AddressBook

### Type Changed: MonoTouch.AddressBook.ABPerson

Added methods:

```
public static ABPropertyType GetPropertyType (int propertyId);
	public static string LocalizedPropertyName (int propertyId);
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate

Removed methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson);
	public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

Added methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson);
	public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions

Removed methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson);
	public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

Added methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson);
	public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingDataRequest

Added method:

```
public override string ToString ();
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Removed property:

```
public virtual bool SubjectAreaChangeMonitoringEnabled { get; }
```

Added property:

```
public virtual bool SubjectAreaChangeMonitoringEnabled { get; set; }
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBAttribute

Removed property:

```
public virtual CBUUID UUID { get; }
```

Added property:

```
public virtual CBUUID UUID { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBMutableCharacteristic

Removed property:

```
public virtual CBUUID UUID { get; }
```

Added property:

```
public override CBUUID UUID { get; set; }
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGVector

Added methods:

```
public static CGVector FromString (string s);
	public override string ToString ();
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIAccordionFoldTransition

Added properties:

```
public float BottomHeight { get; set; }
	public float FoldShadowAmount { get; set; }
	public int NumberOfFolds { get; set; }
	public CIImage TargetImage { get; set; }
	public float Time { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIAztecCodeGenerator

Added properties:

```
public bool CompactStyle { get; set; }
	public float CorrectionLevel { get; set; }
	public int Layers { get; set; }
	public MonoTouch.Foundation.NSData Message { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CICode128BarcodeGenerator

Added properties:

```
public MonoTouch.Foundation.NSData Message { get; set; }
	public float QuietSpace { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIGlassDistortion

Added property:

```
public CIVector Center { get; set; }
```

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLAuthorizationStatus

Added values:

```
AuthorizedAlways = 3,
	AuthorizedWhenInUse = 4,
```

Obsoleted field:

```
[Obsolete ("Value obsoleted, use AuthorizedAlways instead")]
	Authorized = 3,
```

### Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

Added interface:

```
ICLLocationManagerDelegate
```

### New Type MonoTouch.CoreLocation.CLLocationManagerDelegate_Extensions

```
public static class CLLocationManagerDelegate_Extensions {
	// methods
	public static void AuthorizationChanged (ICLLocationManagerDelegate This, CLLocationManager manager, CLAuthorizationStatus status);
	public static void DeferredUpdatesFinished (ICLLocationManagerDelegate This, CLLocationManager manager, MonoTouch.Foundation.NSError error);
	public static void DidDetermineState (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegionState state, CLRegion region);
	public static void DidRangeBeacons (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeacon[] beacons, CLBeaconRegion region);
	public static void DidStartMonitoringForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static void DidVisit (ICLLocationManagerDelegate This, CLLocationManager manager, CLVisit visit);
	public static void Failed (ICLLocationManagerDelegate This, CLLocationManager manager, MonoTouch.Foundation.NSError error);
	public static void LocationsUpdated (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation[] locations);
	public static void LocationUpdatesPaused (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void LocationUpdatesResumed (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void MonitoringFailed (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region, MonoTouch.Foundation.NSError error);
	public static void RangingBeaconsDidFailForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeaconRegion region, MonoTouch.Foundation.NSError error);
	public static void RegionEntered (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static void RegionLeft (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static bool ShouldDisplayHeadingCalibration (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void UpdatedHeading (ICLLocationManagerDelegate This, CLLocationManager manager, CLHeading newHeading);

	[Obsolete ("Deprecated in iOS 6.0")]
	public static void UpdatedLocation (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
}
```

### New Type MonoTouch.CoreLocation.ICLLocationManagerDelegate

```
public interface ICLLocationManagerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVImageBuffer

Added field:

```
public static MonoTouch.Foundation.NSString AlphaChannelIsOpaque;
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSComparisonPredicate

Removed methods:

```
public static NSPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
```

Added methods:

```
public static NSComparisonPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSComparisonPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
```

### Type Changed: MonoTouch.Foundation.NSCompoundPredicate

Removed methods:

```
public static NSPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

Added methods:

```
public static NSCompoundPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSCompoundPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSCompoundPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

### Type Changed: MonoTouch.Foundation.NSFileAccessIntent

Removed methods:

```
public static NSFileAccessIntent ReadingIntentWithURL (NSUrl url, NSFileCoordinatorReadingOptions options);
	public static NSFileAccessIntent WritingIntentWithURL (NSUrl url, NSFileCoordinatorWritingOptions options);
```

Added methods:

```
public static NSFileAccessIntent CreateReadingIntent (NSUrl url, NSFileCoordinatorReadingOptions options);
	public static NSFileAccessIntent CreateWritingIntent (NSUrl url, NSFileCoordinatorWritingOptions options);
```

### Type Changed: MonoTouch.Foundation.NSFileCoordinator

Removed method:

```
public virtual void CoordinateAccessWithIntents (NSFileAccessIntent[] intents, NSOperationQueue queue, System.Action<NSError> accessor);
```

Added method:

```
public virtual void CoordinateAccess (NSFileAccessIntent[] intents, NSOperationQueue executionQueue, System.Action<NSError> accessor);
```

### Type Changed: MonoTouch.Foundation.NSInputStream

Added method:

```
public int Read (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoTouch.Foundation.NSMutableCharacterSet

Removed method:

```
public static NSCharacterSet FromBitmap (NSData data);
```

Added method:

```
public static NSCharacterSet FromBitmapRepresentation (NSData data);
```

### Type Changed: MonoTouch.Foundation.NSObject

Added methods:

```
public System.IDisposable AddObserver (string key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public System.IDisposable AddObserver (NSString key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public void AddObserver (NSObject observer, string keyPath, NSKeyValueObservingOptions options, System.IntPtr context);
	public void RemoveObserver (NSObject observer, string keyPath, System.IntPtr context);
	public void RemoveObserver (NSObject observer, string keyPath);
```

### Type Changed: MonoTouch.Foundation.NSOutputStream

Removed method:

```
public static NSObject OutputStreamToMemory ();
```

Added methods:

```
public static NSOutputStream OutputStreamToMemory ();
	public int Write (byte[] buffer);
	public int Write (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoTouch.Foundation.NSString

Added methods:

```
public virtual void GetLineStart (out uint startPtr, out uint lineEndPtr, out uint contentsEndPtr, NSRange range);
	public virtual NSRange LineRangeForRange (NSRange range);
```

### Type Changed: MonoTouch.Foundation.NSUrlCredentialStorage

Added methods:

```
public virtual void GetCredentials (NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task, System.Action<NSDictionary> completionHandler);
	public virtual void GetDefaultCredential (NSUrlProtectionSpace space, NSUrlSessionTask task, System.Action<NSUrlCredential> completionHandler);
	public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSDictionary options, NSUrlSessionTask task);
	public virtual void SetCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
	public virtual void SetDefaultCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
```

### Type Changed: MonoTouch.Foundation.NSUrlError

Added values:

```
BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionRequiresSharedContainer = -995,
	BackgroundSessionWasDisconnected = -997,
```

### Type Changed: MonoTouch.Foundation.NSUrlErrorCancelledReason

Added value:

```
InsufficientSystemResources = 2,
```

### Type Changed: MonoTouch.Foundation.NSUrlSession

Removed methods:

```
public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionDownloadResponse completionHandler);
```

Added methods:

```
public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlDownloadSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlDownloadSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlDownloadSessionResponse completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionConfiguration

Added property:

```
public virtual string SharedContainerIdentifier { get; set; }
```

Added method:

```
public static NSUrlSessionConfiguration CreateBackgroundSessionConfiguration (string identifier);
```

Obsoleted method:

```
[Obsolete ("Starting with iOS 8, use CreateBackgroundSessionConfiguration")]
	public static NSUrlSessionConfiguration BackgroundSessionConfiguration (string identifier);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTaskRequest

Removed constructor:

```
public NSUrlSessionDownloadTaskRequest (NSUrl data, NSUrlResponse response);
```

Added constructor:

```
public NSUrlSessionDownloadTaskRequest (NSUrl location, NSUrlResponse response);
```

Removed property:

```
public NSUrl Data { get; set; }
```

Added properties:

```
[Obsolete ("Use the Location property")]
	public NSData Data { get; set; }
	public NSUrl Location { get; set; }
```

### Removed Type MonoTouch.Foundation.NSUrlSessionDownloadResponse ### New Type MonoTouch.Foundation.NSExtension

```
public class NSExtension {
	// methods
	public static void Initialize ();
}
```

### New Type MonoTouch.Foundation.NSObservedChange

```
public class NSObservedChange {
	// properties
	public NSKeyValueChange Change { get; }
	public NSIndexSet Indexes { get; }
	public bool IsPrior { get; }
	public NSObject NewValue { get; }
	public NSObject OldValue { get; }
}
```

### New Type MonoTouch.Foundation.NSUrlDownloadSessionResponse

```
public sealed delegate NSUrlDownloadSessionResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlDownloadSessionResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrl location, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrl location, NSUrlResponse response, NSError error);
}
```



## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMCharacteristic

Removed properties:

```
public virtual MonoTouch.Foundation.NSString[] _Properties { get; }
	public HMCharacteristicProperties Properties { get; }
```

Added properties:

```
public virtual MonoTouch.Foundation.NSString[] Properties { get; }
	public bool Readable { get; }
	public bool SupportsEventNotification { get; }
	public bool Writable { get; }
```

### Type Changed: MonoTouch.HomeKit.HMHome

Removed method:

```
public HMService[] ServicesWithTypes (HMServiceType serviceTypes);
```

Added method:

```
public HMService[] GetServices (HMServiceType serviceTypes);
```

## Namespace MonoTouch.LocalAuthentication

### Type Changed: MonoTouch.LocalAuthentication.LAContext

Removed method:

```
public virtual bool CanEvaluatePolicy (LAPolicy policy, MonoTouch.Foundation.NSError error);
```

Added method:

```
public virtual bool CanEvaluatePolicy (LAPolicy policy, out MonoTouch.Foundation.NSError error);
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaQuery

Added methods:

```
public MPMediaItemCollection GetCollection (int index);
	public MPMediaItem GetItem (int index);
	public MPMediaQuerySection GetSection (int index);
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Selector

Added interface:

```
System.IEquatable<Selector>
```

Removed method:

```
public bool Equals (Selector right);
```

Added methods:

```
public virtual bool Equals (Selector right);
	public static Selector Register (System.IntPtr handle);
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecAccessible

Added value:

```
WhenPasscodeSetThisDeviceOnly = 6,
```

### Type Changed: MonoTouch.Security.SecRecord

Added properties:

```
public SecAccessControl AccessControl { get; set; }
	public bool UseNoAuthenticationUI { get; set; }
	public string UseOperationPrompt { get; set; }
```

### New Type MonoTouch.Security.SecAccessControl

```
public class SecAccessControl {
	// constructors
	public SecAccessControl (SecAccessible accessible, SecAccessControlCreateFlags flags);
	// properties
	public SecAccessible Accessible { get; }
	public SecAccessControlCreateFlags Flags { get; }
}
```

### New Type MonoTouch.Security.SecAccessControlCreateFlags

```
[Serializable]
[Flags]
public enum SecAccessControlCreateFlags {
	UserPresence = 1,
}
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKNode

Removed method:

```
public static SKNode FromFile (string file);
```

Added method:

```
public static T FromFile<T> (string file);
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIInputViewController

Added constructor:

```
public UIInputViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added property:

```
public UIStringAttributes TitleTextAttributes { get; set; }
```

Obsoleted methods:

```
[Obsolete ("Use TitleTextAttributes property with UIStringAttributes")]
	public UITextAttributes GetTitleTextAttributes ();

	[Obsolete ("Use TitleTextAttributes with UIStringAttributes")]
	public void SetTitleTextAttributes (UITextAttributes attributes);
```

### Type Changed: MonoTouch.UIKit.UINavigationBar.UINavigationBarAppearance

Added property:

```
public UIStringAttributes TitleTextAttributes { get; set; }
```

### Type Changed: MonoTouch.UIKit.UISearchController

Removed property:

```
public virtual UISearchResultsUpdating SearchResultsUpdater { get; set; }
```

Added properties:

```
public UISearchResultsUpdating SearchResultsUpdater { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakSearchResultsUpdater { get; set; }
```

Added method:

```
public void SetSearchResultsUpdater (System.Action<UISearchController> updateSearchResults);
```

   


 <hr>
