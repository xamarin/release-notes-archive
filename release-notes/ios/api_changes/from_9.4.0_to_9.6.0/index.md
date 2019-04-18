---
id: B4C9124A-9C48-4093-B5D7-3EE7EB2ECB07
title: "From 9.4.0 to 9.6.0"
---

# API diff

 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string SdkVersion = "9.2" "9.3";
	public const string Version = "9.4.0" "9.5.99";
```

Added field:

<pre style='color: green'>
	public static const string HealthKitUILibrary = "/System/Library/Frameworks/HealthKitUI.framework/HealthKit";
</pre>

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVMetadata

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString KeySpaceHlsDateRange { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVMetadataGroup

Added properties:

<pre style='color: green'>
	public virtual string ClassifyingLabel { get; }
	public virtual string UniqueID { get; }
</pre>

### Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Added property:

<pre style='color: green'>
	public virtual AVPlayerItemMediaDataCollector[] MediaDataCollectors { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddMediaDataCollector (AVPlayerItemMediaDataCollector collector);
	public virtual void RemoveMediaDataCollector (AVPlayerItemMediaDataCollector collector);
</pre>

### New Type MonoTouch.AVFoundation.AVPlayerItemMediaDataCollector

<pre style='color: green'>
public abstract class AVPlayerItemMediaDataCollector : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMediaDataCollector (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemMediaDataCollector (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemMediaDataCollector (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataCollector

<pre style='color: green'>
public class AVPlayerItemMetadataCollector : MonoTouch.AVFoundation.AVPlayerItemMediaDataCollector, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataCollector ();
	public AVPlayerItemMetadataCollector (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemMetadataCollector (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataCollector (IntPtr handle);
	public AVPlayerItemMetadataCollector (string[] identifiers, string[] classifyingLabels);
	// properties
	public override IntPtr ClassHandle { get; }
	public IAVPlayerItemMetadataCollectorPushDelegate Delegate { get; }
	public virtual MonoTouch.CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (IAVPlayerItemMetadataCollectorPushDelegate pushDelegate, MonoTouch.CoreFoundation.DispatchQueue delegateQueue);
}
</pre>

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataCollectorPushDelegate

<pre style='color: green'>
public abstract class AVPlayerItemMetadataCollectorPushDelegate : MonoTouch.Foundation.NSObject, IAVPlayerItemMetadataCollectorPushDelegate, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataCollectorPushDelegate ();
	public AVPlayerItemMetadataCollectorPushDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemMetadataCollectorPushDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataCollectorPushDelegate (IntPtr handle);
	// methods
	public virtual void DidCollectDateRange (AVPlayerItemMetadataCollector metadataCollector, AVDateRangeMetadataGroup[] metadataGroups, MonoTouch.Foundation.NSIndexSet indexesOfNewGroups, MonoTouch.Foundation.NSIndexSet indexesOfModifiedGroups);
}
</pre>

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataCollectorPushDelegate_Extensions

<pre style='color: green'>
public static class AVPlayerItemMetadataCollectorPushDelegate_Extensions {
}
</pre>

### New Type MonoTouch.AVFoundation.IAVPlayerItemMetadataCollectorPushDelegate

<pre style='color: green'>
public interface IAVPlayerItemMetadataCollectorPushDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidCollectDateRange (AVPlayerItemMetadataCollector metadataCollector, AVDateRangeMetadataGroup[] metadataGroups, MonoTouch.Foundation.NSIndexSet indexesOfNewGroups, MonoTouch.Foundation.NSIndexSet indexesOfModifiedGroups);
}
</pre>

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKContainer

Added methods:

<pre style='color: green'>
	public virtual void FetchAllLongLivedOperationIDs (System.Action&lt;MonoTouch.Foundation.NSDictionary,MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSDictionary&gt; FetchAllLongLivedOperationIDsAsync ();
	public virtual void FetchLongLivedOperation (string[] operationID, System.Action&lt;MonoTouch.Foundation.NSDictionary,MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSDictionary&gt; FetchLongLivedOperationAsync (string[] operationID);
</pre>

### Type Changed: MonoTouch.CloudKit.CKOperation

Added properties:

<pre style='color: green'>
	public virtual bool LongLived { get; set; }
	public virtual System.Action LongLivedOperationWasPersistedCallback { get; set; }
	public virtual string OperationID { get; }
</pre>

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGBitmapFlags

Added value:

<pre style='color: green'>
	FloatInfoMask = 3840,
</pre>

### Type Changed: MonoTouch.CoreGraphics.CGColorSpaceNames

Added properties:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString Dcip3 { get; }
	public static MonoTouch.Foundation.NSString DisplayP3 { get; }
</pre>

### Type Changed: MonoTouch.CoreGraphics.CGDataProvider

Obsoleted constructors:

```
[Obsolete ()]
	public CGDataProvider (IntPtr memoryBlock, int size);
```

Added constructors:

<pre style='color: green'>
	public CGDataProvider (byte[] buffer);
	public CGDataProvider (IntPtr memoryBlock, int size, System.Action&lt;IntPtr&gt; releaseMemoryBlockCallback);
</pre>

### New Type MonoTouch.CoreGraphics.CGColorConverter

<pre style='color: green'>
public class CGColorConverter : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGColorConverter (MonoTouch.Foundation.NSDictionary options, CGColorConverterTriple[] triples);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~CGColorConverter ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.CoreGraphics.CGColorConverterTransformType

<pre style='color: green'>
[Serializable]
public enum CGColorConverterTransformType {
	ApplySpace = 2,
	FromSpace = 0,
	ToSpace = 1,
}
</pre>

### New Type MonoTouch.CoreGraphics.CGColorConverterTriple

<pre style='color: green'>
public struct CGColorConverterTriple {
	// fields
	public CGColorRenderingIntent Intent;
	public CGColorSpace Space;
	public CGColorConverterTransformType Transform;
}
</pre>

## Namespace MonoTouch.CoreImage

### New Type MonoTouch.CoreImage.CIMaskedVariableBlur

<pre style='color: green'>
public class CIMaskedVariableBlur : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIMaskedVariableBlur ();
	public CIMaskedVariableBlur (IntPtr handle);
	// properties
	public float Radius { get; set; }
}
</pre>

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMBufferQueue

Added properties:

<pre style='color: green'>
	public int BufferCount { get; }
	public bool ContainsEndOfData { get; }
	public CMTime Duration { get; }
	public bool IsAtEndOfData { get; }
	public bool IsEmpty { get; }
</pre>

Added methods:

<pre style='color: green'>
	public MonoTouch.ObjCRuntime.INativeObject DequeueIfDataReady ();
	public int MarkEndOfData ();
	public int Reset ();
</pre>

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMSensorRecorder

Obsoleted methods:

```
[Obsolete ()]
	public virtual CMSensorDataList GetAccelerometerDataSince (ulong identifier);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSDataDetector

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: MonoTouch.Foundation.NSOrthography

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: MonoTouch.Foundation.NSRegularExpression

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: MonoTouch.Foundation.NSTextCheckingResult

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: MonoTouch.Foundation.NSValueTransformer

Added properties:

<pre style='color: green'>
	public static NSString CompletedInitialSyncNotification { get; }
	public static NSString DidChangeAccountsNotification { get; }
	public static NSString SizeLimitExceededNotification { get; }
	public static NSString UserDefaultsDidChangeNotification { get; }
</pre>

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKObjectType

Added property:

<pre style='color: green'>
	public static HKActivitySummaryType ActivitySummaryType { get; }
</pre>

### Type Changed: MonoTouch.HealthKit.HKPredicateKeyPath

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString DateComponents { get; }
</pre>

### Type Changed: MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString AppleExerciseTime { get; }
</pre>

### Type Changed: MonoTouch.HealthKit.HKQuery

Added property:

<pre style='color: green'>
	public virtual HKObjectType ObjectType { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSPredicate GetPredicateForActivitySummariesBetween (MonoTouch.Foundation.NSDateComponents startDateComponents, MonoTouch.Foundation.NSDateComponents endDateComponents);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForActivitySummary (MonoTouch.Foundation.NSDateComponents dateComponents);
</pre>

### New Type MonoTouch.HealthKit.HKActivitySummary

<pre style='color: green'>
public class HKActivitySummary : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKActivitySummary ();
	public HKActivitySummary (MonoTouch.Foundation.NSCoder coder);
	public HKActivitySummary (MonoTouch.Foundation.NSObjectFlag t);
	public HKActivitySummary (IntPtr handle);
	// properties
	public virtual HKQuantity ActiveEnergyBurned { get; set; }
	public virtual HKQuantity ActiveEnergyBurnedGoal { get; set; }
	public virtual HKQuantity AppleExerciseTime { get; set; }
	public virtual HKQuantity AppleExerciseTimeGoal { get; set; }
	public virtual HKQuantity AppleStandHours { get; set; }
	public virtual HKQuantity AppleStandHoursGoal { get; set; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSDateComponents DateComponentsForCalendar (MonoTouch.Foundation.NSCalendar calendar);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.HealthKit.HKActivitySummaryQuery

<pre style='color: green'>
public class HKActivitySummaryQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKActivitySummaryQuery (MonoTouch.Foundation.NSCoder coder);
	public HKActivitySummaryQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKActivitySummaryQuery (IntPtr handle);
	public HKActivitySummaryQuery (MonoTouch.Foundation.NSPredicate predicate, System.Action&lt;HKActivitySummaryQuery,MonoTouch.HealthKit.HKActivitySummary[],MonoTouch.Foundation.NSError&gt; handler);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Action&lt;HKActivitySummaryQuery,MonoTouch.HealthKit.HKActivitySummary[],MonoTouch.Foundation.NSError&gt; UpdateHandler { get; set; }
}
</pre>

### New Type MonoTouch.HealthKit.HKActivitySummaryType

<pre style='color: green'>
public class HKActivitySummaryType : MonoTouch.HealthKit.HKObjectType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKActivitySummaryType (MonoTouch.Foundation.NSCoder coder);
	public HKActivitySummaryType (MonoTouch.Foundation.NSObjectFlag t);
	public HKActivitySummaryType (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMCharacteristic

Added property:

<pre style='color: green'>
	public bool Hidden { get; }
</pre>

### Type Changed: MonoTouch.HomeKit.HMCharacteristicMetadataUnits

Added value:

<pre style='color: green'>
	Lux = 6,
</pre>

### Type Changed: MonoTouch.HomeKit.HMError

Added value:

<pre style='color: green'>
	ReferToUserManual = 86,
</pre>

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADError

Added value:

<pre style='color: green'>
	AssetLoadFailure = 8,
</pre>

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKLocalSearchRequest

Added constructor:

<pre style='color: green'>
	public MKLocalSearchRequest (MKLocalSearchCompletion completion);
</pre>

### New Type MonoTouch.MapKit.IMKLocalSearchCompleterDelegate

<pre style='color: green'>
public interface IMKLocalSearchCompleterDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoTouch.MapKit.MKLocalSearchCompleter

<pre style='color: green'>
public class MKLocalSearchCompleter : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MKLocalSearchCompleter ();
	public MKLocalSearchCompleter (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearchCompleter (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearchCompleter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public MKLocalSearchCompleterDelegate Delegate { get; set; }
	public virtual MKSearchCompletionFilterType FilterType { get; set; }
	public virtual string QueryFragment { get; set; }
	public virtual MKCoordinateRegion Region { get; set; }
	public virtual MKLocalSearchCompletion[] Results { get; }
	public virtual bool Searching { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.MapKit.MKLocalSearchCompleterDelegate

<pre style='color: green'>
public class MKLocalSearchCompleterDelegate : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, IMKLocalSearchCompleterDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MKLocalSearchCompleterDelegate ();
	public MKLocalSearchCompleterDelegate (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearchCompleterDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearchCompleterDelegate (IntPtr handle);
	// methods
	public virtual void DidFail (MKLocalSearchCompleter completer, MonoTouch.Foundation.NSError error);
	public virtual void DidUpdateResults (MKLocalSearchCompleter completer);
}
</pre>

### New Type MonoTouch.MapKit.MKLocalSearchCompleterDelegate_Extensions

<pre style='color: green'>
public static class MKLocalSearchCompleterDelegate_Extensions {
	// methods
	public static void DidFail (IMKLocalSearchCompleterDelegate This, MKLocalSearchCompleter completer, MonoTouch.Foundation.NSError error);
	public static void DidUpdateResults (IMKLocalSearchCompleterDelegate This, MKLocalSearchCompleter completer);
}
</pre>

### New Type MonoTouch.MapKit.MKLocalSearchCompletion

<pre style='color: green'>
public class MKLocalSearchCompletion : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MKLocalSearchCompletion ();
	public MKLocalSearchCompletion (MonoTouch.Foundation.NSCoder coder);
	public MKLocalSearchCompletion (MonoTouch.Foundation.NSObjectFlag t);
	public MKLocalSearchCompletion (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Subtitle { get; }
	public virtual MonoTouch.Foundation.NSValue[] SubtitleHighlightRanges { get; }
	public virtual string Title { get; }
	public virtual MonoTouch.Foundation.NSValue[] TitleHighlightRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoTouch.MapKit.MKSearchCompletionFilterType

<pre style='color: green'>
[Serializable]
public enum MKSearchCompletionFilterType {
	AndQueries = 0,
	Only = 1,
}
</pre>

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaLibrary

Added property:

<pre style='color: green'>
	public static MPMediaLibraryAuthorizationStatus AuthorizationStatus { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddItem (string productID, System.Action&lt;MPMediaItem[],MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MPMediaItem[]&gt; AddItemAsync (string productID);
	public virtual void GetPlaylist (MonoTouch.Foundation.NSUuid uuid, MPMediaPlaylistCreationMetadata creationMetadata, System.Action&lt;MPMediaPlaylist,MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MPMediaPlaylist&gt; GetPlaylistAsync (MonoTouch.Foundation.NSUuid uuid, MPMediaPlaylistCreationMetadata creationMetadata);
	public static void RequestAuthorization (System.Action&lt;MPMediaLibraryAuthorizationStatus&gt; handler);
	public static System.Threading.Tasks.Task&lt;MPMediaLibraryAuthorizationStatus&gt; RequestAuthorizationAsync ();
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylist

Added methods:

<pre style='color: green'>
	public virtual void AddItem (string productID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task AddItemAsync (string productID);
	public virtual void AddMediaItems (MPMediaItem[] mediaItems, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task AddMediaItemsAsync (MPMediaItem[] mediaItems);
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylistProperty

Added properties:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString AuthorDisplayName { get; }
	public static MonoTouch.Foundation.NSString DescriptionText { get; }
</pre>

### Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added method:

<pre style='color: green'>
	public virtual void SetQueue (string[] storeIDs);
</pre>

### New Type MonoTouch.MediaPlayer.MPErrorCode

<pre style='color: green'>
[Serializable]
public enum MPErrorCode {
	CloudServiceCapabilityMissing = 2,
	NetworkConnectionFailed = 3,
	NotFound = 4,
	NotSupported = 5,
	PermissionDenied = 1,
	Unknown = 0,
}
</pre>

### New Type MonoTouch.MediaPlayer.MPMediaLibraryAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum MPMediaLibraryAuthorizationStatus {
	Authorized = 3,
	Denied = 1,
	NotDetermined = 0,
	Restricted = 2,
}
</pre>

### New Type MonoTouch.MediaPlayer.MPMediaPlaylistCreationMetadata

<pre style='color: green'>
public class MPMediaPlaylistCreationMetadata : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPMediaPlaylistCreationMetadata (MonoTouch.Foundation.NSCoder coder);
	public MPMediaPlaylistCreationMetadata (MonoTouch.Foundation.NSObjectFlag t);
	public MPMediaPlaylistCreationMetadata (IntPtr handle);
	public MPMediaPlaylistCreationMetadata (string name);
	// properties
	public virtual string AuthorDisplayName { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string DescriptionText { get; set; }
	public virtual string Name { get; }
}
</pre>

## Namespace MonoTouch.NetworkExtension

### Type Changed: MonoTouch.NetworkExtension.NEAppProxyFlowError

Added values:

<pre style='color: green'>
	DatagramTooLarge = 9,
	ReadAlreadyPending = 10,
</pre>

### Type Changed: MonoTouch.NetworkExtension.NEAppRule

Added property:

<pre style='color: green'>
	public virtual string MatchPath { get; set; }
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_STRET = 536870912,
</pre>

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added values:

<pre style='color: green'>
	iOS_9_3 = 590592,
	Mac_10_11_3 = 2826857279913984,
</pre>

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKError

Added values:

<pre style='color: green'>
	CloudServiceNetworkConnectionFailed = 7,
	CloudServicePermissionDenied = 6,
</pre>

### Type Changed: MonoTouch.StoreKit.SKStoreProductParameterKey

Added property:

<pre style='color: green'>
	public static MonoTouch.Foundation.NSString AdvertisingPartnerToken { get; }
</pre>

### New Type MonoTouch.StoreKit.SKCloudServiceAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum SKCloudServiceAuthorizationStatus {
	Authorized = 3,
	Denied = 1,
	NotDetermined = 0,
	Restricted = 2,
}
</pre>

### New Type MonoTouch.StoreKit.SKCloudServiceCapability

<pre style='color: green'>
[Serializable]
public enum SKCloudServiceCapability {
	AddToCloudMusicLibrary = 256,
	MusicCatalogPlayback = 1,
	None = 0,
}
</pre>

### New Type MonoTouch.StoreKit.SKCloudServiceController

<pre style='color: green'>
public class SKCloudServiceController : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKCloudServiceController ();
	public SKCloudServiceController (MonoTouch.Foundation.NSCoder coder);
	public SKCloudServiceController (MonoTouch.Foundation.NSObjectFlag t);
	public SKCloudServiceController (IntPtr handle);
	// properties
	public static SKCloudServiceAuthorizationStatus AuthorizationStatus { get; }
	public override IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString CloudServiceCapabilitiesDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString StorefrontIdentifierDidChangeNotification { get; }
	// methods
	public static void RequestAuthorization (System.Action&lt;SKCloudServiceAuthorizationStatus&gt; handler);
	public static System.Threading.Tasks.Task&lt;SKCloudServiceAuthorizationStatus&gt; RequestAuthorizationAsync ();
	public virtual void RequestCapabilities (System.Action&lt;SKCloudServiceCapability,MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;SKCloudServiceCapability&gt; RequestCapabilitiesAsync ();
	public virtual void RequestStorefrontIdentifier (System.Action&lt;MonoTouch.Foundation.NSString,MonoTouch.Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSString&gt; RequestStorefrontIdentifierAsync ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveCloudServiceCapabilitiesDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
		public static MonoTouch.Foundation.NSObject ObserveStorefrontIdentifierDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIUserInterfaceIdiom

Added value:

<pre style='color: green'>
	CarPlay = 3,
</pre>

## Namespace MonoTouch.WatchConnectivity

### Type Changed: MonoTouch.WatchConnectivity.WCErrorCode

Added values:

<pre style='color: green'>
	SessionInactive = 7016,
	TransferTimedOut = 7017,
</pre>

### Type Changed: MonoTouch.WatchConnectivity.WCSession

Added property:

<pre style='color: green'>
	public virtual WCSessionActivationState ActivationState { get; }
</pre>

### Type Changed: MonoTouch.WatchConnectivity.WCSessionDelegate

Added methods:

<pre style='color: green'>
	public virtual void ActivationDidComplete (WCSession session, WCSessionActivationState activationState, MonoTouch.Foundation.NSError error);
	public virtual void DidBecomeInactive (WCSession session);
	public virtual void DidDeactivate (WCSession session);
</pre>

### Type Changed: MonoTouch.WatchConnectivity.WCSessionDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void ActivationDidComplete (IWCSessionDelegate This, WCSession session, WCSessionActivationState activationState, MonoTouch.Foundation.NSError error);
	public static void DidBecomeInactive (IWCSessionDelegate This, WCSession session);
	public static void DidDeactivate (IWCSessionDelegate This, WCSession session);
</pre>

### New Type MonoTouch.WatchConnectivity.WCSessionActivationState

<pre style='color: green'>
[Serializable]
public enum WCSessionActivationState {
	Activated = 2,
	Inactive = 1,
	NotActivated = 0,
}
</pre>

## New Namespace MonoTouch.HealthKitUI

### New Type MonoTouch.HealthKitUI.HKActivityRingView

<pre style='color: green'>
public class HKActivityRingView : MonoTouch.UIKit.UIView, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUIAppearance, MonoTouch.UIKit.IUIAppearanceContainer, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUIFocusEnvironment, MonoTouch.UIKit.IUITraitEnvironment, System.Collections.IEnumerable, System.IDisposable {
	// constructors
	public HKActivityRingView (MonoTouch.Foundation.NSCoder coder);
	public HKActivityRingView (MonoTouch.Foundation.NSObjectFlag t);
	public HKActivityRingView (System.Drawing.RectangleF frame);
	public HKActivityRingView (IntPtr handle);
	// properties
	public virtual MonoTouch.HealthKit.HKActivitySummary ActivitySummary { get; set; }
	public static HKActivityRingView.HKActivityRingViewAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public static HKActivityRingView.HKActivityRingViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; ();
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; (MonoTouch.UIKit.UITraitCollection traits);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual void SetActivitySummary (MonoTouch.HealthKit.HKActivitySummary activitySummary, bool animated);

	// inner types
	public class HKActivityRingViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.Foundation.INSObjectProtocol, MonoTouch.ObjCRuntime.INativeObject, MonoTouch.UIKit.IUIAppearance, System.IDisposable {
		// constructors
		protected HKActivityRingView (IntPtr handle);
	}
}
</pre>

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace AVFoundation

### Type Changed: AVFoundation.AVMetadata

Added property:

<pre style='color: green'>
	public static Foundation.NSString KeySpaceHlsDateRange { get; }
</pre>

### Type Changed: AVFoundation.AVMetadataGroup

Added properties:

<pre style='color: green'>
	public virtual string ClassifyingLabel { get; }
	public virtual string UniqueID { get; }
</pre>

### Type Changed: AVFoundation.AVPlayerItem

Added property:

<pre style='color: green'>
	public virtual AVPlayerItemMediaDataCollector[] MediaDataCollectors { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddMediaDataCollector (AVPlayerItemMediaDataCollector collector);
	public virtual void RemoveMediaDataCollector (AVPlayerItemMediaDataCollector collector);
</pre>

### New Type AVFoundation.AVPlayerItemMediaDataCollector

<pre style='color: green'>
public abstract class AVPlayerItemMediaDataCollector : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVPlayerItemMediaDataCollector (Foundation.NSObjectFlag t);
	protected AVPlayerItemMediaDataCollector (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type AVFoundation.AVPlayerItemMetadataCollector

<pre style='color: green'>
public class AVPlayerItemMetadataCollector : AVFoundation.AVPlayerItemMediaDataCollector, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public AVPlayerItemMetadataCollector ();
	protected AVPlayerItemMetadataCollector (Foundation.NSObjectFlag t);
	protected AVPlayerItemMetadataCollector (IntPtr handle);
	public AVPlayerItemMetadataCollector (string[] identifiers, string[] classifyingLabels);
	// properties
	public override IntPtr ClassHandle { get; }
	public IAVPlayerItemMetadataCollectorPushDelegate Delegate { get; }
	public virtual CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (IAVPlayerItemMetadataCollectorPushDelegate pushDelegate, CoreFoundation.DispatchQueue delegateQueue);
}
</pre>

### New Type AVFoundation.AVPlayerItemMetadataCollectorPushDelegate

<pre style='color: green'>
public abstract class AVPlayerItemMetadataCollectorPushDelegate : Foundation.NSObject, IAVPlayerItemMetadataCollectorPushDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected AVPlayerItemMetadataCollectorPushDelegate ();
	protected AVPlayerItemMetadataCollectorPushDelegate (Foundation.NSObjectFlag t);
	protected AVPlayerItemMetadataCollectorPushDelegate (IntPtr handle);
	// methods
	public virtual void DidCollectDateRange (AVPlayerItemMetadataCollector metadataCollector, AVDateRangeMetadataGroup[] metadataGroups, Foundation.NSIndexSet indexesOfNewGroups, Foundation.NSIndexSet indexesOfModifiedGroups);
}
</pre>

### New Type AVFoundation.IAVPlayerItemMetadataCollectorPushDelegate

<pre style='color: green'>
public interface IAVPlayerItemMetadataCollectorPushDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidCollectDateRange (AVPlayerItemMetadataCollector metadataCollector, AVDateRangeMetadataGroup[] metadataGroups, Foundation.NSIndexSet indexesOfNewGroups, Foundation.NSIndexSet indexesOfModifiedGroups);
}
</pre>

## Namespace CloudKit

### Type Changed: CloudKit.CKContainer

Added methods:

<pre style='color: green'>
	public virtual void FetchAllLongLivedOperationIDs (System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; FetchAllLongLivedOperationIDsAsync ();
	public virtual void FetchLongLivedOperation (string[] operationID, System.Action&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSOperation&gt;&gt; FetchLongLivedOperationAsync (string[] operationID);
</pre>

### Type Changed: CloudKit.CKOperation

Added properties:

<pre style='color: green'>
	public virtual bool LongLived { get; set; }
	public virtual System.Action LongLivedOperationWasPersistedCallback { get; set; }
	public virtual string OperationID { get; }
</pre>

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGBitmapFlags

Added value:

<pre style='color: green'>
	FloatInfoMask = 3840,
</pre>

### Type Changed: CoreGraphics.CGColorSpaceNames

Added properties:

<pre style='color: green'>
	public static Foundation.NSString Dcip3 { get; }
	public static Foundation.NSString DisplayP3 { get; }
</pre>

### Type Changed: CoreGraphics.CGDataProvider

Obsoleted constructors:

```
[Obsolete ()]
	public CGDataProvider (IntPtr memoryBlock, int size);
```

Added constructors:

<pre style='color: green'>
	public CGDataProvider (byte[] buffer);
	public CGDataProvider (IntPtr memoryBlock, int size, System.Action&lt;IntPtr&gt; releaseMemoryBlockCallback);
</pre>

### New Type CoreGraphics.CGColorConverter

<pre style='color: green'>
public class CGColorConverter : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGColorConverter (Foundation.NSDictionary options, CGColorConverterTriple[] triples);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~CGColorConverter ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
</pre>

### New Type CoreGraphics.CGColorConverterTransformType

<pre style='color: green'>
[Serializable]
public enum CGColorConverterTransformType {
	ApplySpace = 2,
	FromSpace = 0,
	ToSpace = 1,
}
</pre>

### New Type CoreGraphics.CGColorConverterTriple

<pre style='color: green'>
public struct CGColorConverterTriple {
	// fields
	public CGColorRenderingIntent Intent;
	public CGColorSpace Space;
	public CGColorConverterTransformType Transform;
}
</pre>

## Namespace CoreImage

### New Type CoreImage.CIMaskedVariableBlur

<pre style='color: green'>
public class CIMaskedVariableBlur : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public CIMaskedVariableBlur ();
	public CIMaskedVariableBlur (IntPtr handle);
	// properties
	public float Radius { get; set; }
}
</pre>

## Namespace CoreMedia

### Type Changed: CoreMedia.CMBufferQueue

Added properties:

<pre style='color: green'>
	public nint BufferCount { get; }
	public bool ContainsEndOfData { get; }
	public CMTime Duration { get; }
	public bool IsAtEndOfData { get; }
	public bool IsEmpty { get; }
</pre>

Added methods:

<pre style='color: green'>
	public ObjCRuntime.INativeObject DequeueIfDataReady ();
	public int MarkEndOfData ();
	public int Reset ();
</pre>

## Namespace CoreMotion

### Type Changed: CoreMotion.CMSensorRecorder

Obsoleted methods:

```
[Obsolete ()]
	public virtual CMSensorDataList GetAccelerometerDataSince (ulong identifier);
```

## Namespace Foundation

### Type Changed: Foundation.NSDataDetector

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: Foundation.NSOrthography

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: Foundation.NSRegularExpression

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: Foundation.NSTextCheckingResult

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: Foundation.NSValueTransformer

Added properties:

<pre style='color: green'>
	public static NSString CompletedInitialSyncNotification { get; }
	public static NSString DidChangeAccountsNotification { get; }
	public static NSString SizeLimitExceededNotification { get; }
	public static NSString UserDefaultsDidChangeNotification { get; }
</pre>

## Namespace HealthKit

### Type Changed: HealthKit.HKObjectType

Added property:

<pre style='color: green'>
	public static HKActivitySummaryType ActivitySummaryType { get; }
</pre>

### Type Changed: HealthKit.HKPredicateKeyPath

Added property:

<pre style='color: green'>
	public static Foundation.NSString DateComponents { get; }
</pre>

### Type Changed: HealthKit.HKQuantityTypeIdentifierKey

Added property:

<pre style='color: green'>
	public static Foundation.NSString AppleExerciseTime { get; }
</pre>

### Type Changed: HealthKit.HKQuery

Added property:

<pre style='color: green'>
	public virtual HKObjectType ObjectType { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static Foundation.NSPredicate GetPredicateForActivitySummariesBetween (Foundation.NSDateComponents startDateComponents, Foundation.NSDateComponents endDateComponents);
	public static Foundation.NSPredicate GetPredicateForActivitySummary (Foundation.NSDateComponents dateComponents);
</pre>

### New Type HealthKit.HKActivitySummary

<pre style='color: green'>
public class HKActivitySummary : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public HKActivitySummary ();
	public HKActivitySummary (Foundation.NSCoder coder);
	protected HKActivitySummary (Foundation.NSObjectFlag t);
	protected HKActivitySummary (IntPtr handle);
	// properties
	public virtual HKQuantity ActiveEnergyBurned { get; set; }
	public virtual HKQuantity ActiveEnergyBurnedGoal { get; set; }
	public virtual HKQuantity AppleExerciseTime { get; set; }
	public virtual HKQuantity AppleExerciseTimeGoal { get; set; }
	public virtual HKQuantity AppleStandHours { get; set; }
	public virtual HKQuantity AppleStandHoursGoal { get; set; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual Foundation.NSDateComponents DateComponentsForCalendar (Foundation.NSCalendar calendar);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
</pre>

### New Type HealthKit.HKActivitySummaryQuery

<pre style='color: green'>
public class HKActivitySummaryQuery : HealthKit.HKQuery, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected HKActivitySummaryQuery (Foundation.NSObjectFlag t);
	protected HKActivitySummaryQuery (IntPtr handle);
	public HKActivitySummaryQuery (Foundation.NSPredicate predicate, System.Action&lt;HKActivitySummaryQuery,HealthKit.HKActivitySummary[],Foundation.NSError&gt; handler);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Action&lt;HKActivitySummaryQuery,HealthKit.HKActivitySummary[],Foundation.NSError&gt; UpdateHandler { get; set; }
}
</pre>

### New Type HealthKit.HKActivitySummaryType

<pre style='color: green'>
public class HKActivitySummaryType : HealthKit.HKObjectType, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public HKActivitySummaryType (Foundation.NSCoder coder);
	protected HKActivitySummaryType (Foundation.NSObjectFlag t);
	protected HKActivitySummaryType (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

## Namespace HomeKit

### Type Changed: HomeKit.HMCharacteristic

Added property:

<pre style='color: green'>
	public bool Hidden { get; }
</pre>

### Type Changed: HomeKit.HMCharacteristicMetadataUnits

Added value:

<pre style='color: green'>
	Lux = 6,
</pre>

### Type Changed: HomeKit.HMError

Added value:

<pre style='color: green'>
	ReferToUserManual = 86,
</pre>

## Namespace iAd

### Type Changed: iAd.ADError

Added value:

<pre style='color: green'>
	AssetLoadFailure = 8,
</pre>

## Namespace MapKit

### New Type MapKit.IMKLocalSearchCompleterDelegate

<pre style='color: green'>
public interface IMKLocalSearchCompleterDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MapKit.MKLocalSearchCompleter

<pre style='color: green'>
public class MKLocalSearchCompleter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MKLocalSearchCompleter ();
	protected MKLocalSearchCompleter (Foundation.NSObjectFlag t);
	protected MKLocalSearchCompleter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public IMKLocalSearchCompleterDelegate Delegate { get; set; }
	public virtual MKSearchCompletionFilterType FilterType { get; set; }
	public virtual string QueryFragment { get; set; }
	public virtual MKCoordinateRegion Region { get; set; }
	public virtual MKLocalSearchCompletion[] Results { get; }
	public virtual bool Searching { get; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MapKit.MKLocalSearchCompleterDelegate

<pre style='color: green'>
public class MKLocalSearchCompleterDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMKLocalSearchCompleterDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MKLocalSearchCompleterDelegate ();
	protected MKLocalSearchCompleterDelegate (Foundation.NSObjectFlag t);
	protected MKLocalSearchCompleterDelegate (IntPtr handle);
	// methods
	public virtual void DidFail (MKLocalSearchCompleter completer, Foundation.NSError error);
	public virtual void DidUpdateResults (MKLocalSearchCompleter completer);
}
</pre>

### New Type MapKit.MKLocalSearchCompleterDelegate_Extensions

<pre style='color: green'>
public static class MKLocalSearchCompleterDelegate_Extensions {
	// methods
	public static void DidFail (IMKLocalSearchCompleterDelegate This, MKLocalSearchCompleter completer, Foundation.NSError error);
	public static void DidUpdateResults (IMKLocalSearchCompleterDelegate This, MKLocalSearchCompleter completer);
}
</pre>

### New Type MapKit.MKLocalSearchCompletion

<pre style='color: green'>
public class MKLocalSearchCompletion : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public MKLocalSearchCompletion ();
	protected MKLocalSearchCompletion (Foundation.NSObjectFlag t);
	protected MKLocalSearchCompletion (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Subtitle { get; }
	public virtual Foundation.NSValue[] SubtitleHighlightRanges { get; }
	public virtual string Title { get; }
	public virtual Foundation.NSValue[] TitleHighlightRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MapKit.MKSearchCompletionFilterType

<pre style='color: green'>
[Serializable]
public enum MKSearchCompletionFilterType {
	AndQueries = 0,
	Only = 1,
}
</pre>

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPMediaLibrary

Added property:

<pre style='color: green'>
	public static MPMediaLibraryAuthorizationStatus AuthorizationStatus { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddItem (string productID, System.Action&lt;MPMediaEntity[],Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MPMediaEntity[]&gt; AddItemAsync (string productID);
	public virtual void GetPlaylist (Foundation.NSUuid uuid, MPMediaPlaylistCreationMetadata creationMetadata, System.Action&lt;MPMediaPlaylist,Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;MPMediaPlaylist&gt; GetPlaylistAsync (Foundation.NSUuid uuid, MPMediaPlaylistCreationMetadata creationMetadata);
	public static void RequestAuthorization (System.Action&lt;MPMediaLibraryAuthorizationStatus&gt; handler);
	public static System.Threading.Tasks.Task&lt;MPMediaLibraryAuthorizationStatus&gt; RequestAuthorizationAsync ();
</pre>

### Type Changed: MediaPlayer.MPMediaPlaylist

Added methods:

<pre style='color: green'>
	public virtual void AddItem (string productID, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task AddItemAsync (string productID);
	public virtual void AddMediaItems (MPMediaItem[] mediaItems, System.Action&lt;Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task AddMediaItemsAsync (MPMediaItem[] mediaItems);
</pre>

### Type Changed: MediaPlayer.MPMediaPlaylistProperty

Added properties:

<pre style='color: green'>
	public static Foundation.NSString AuthorDisplayName { get; }
	public static Foundation.NSString DescriptionText { get; }
</pre>

### Type Changed: MediaPlayer.MPMusicPlayerController

Added method:

<pre style='color: green'>
	public virtual void SetQueue (string[] storeIDs);
</pre>

### New Type MediaPlayer.MPErrorCode

<pre style='color: green'>
[Serializable]
public enum MPErrorCode {
	CloudServiceCapabilityMissing = 2,
	NetworkConnectionFailed = 3,
	NotFound = 4,
	NotSupported = 5,
	PermissionDenied = 1,
	Unknown = 0,
}
</pre>

### New Type MediaPlayer.MPMediaLibraryAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum MPMediaLibraryAuthorizationStatus {
	Authorized = 3,
	Denied = 1,
	NotDetermined = 0,
	Restricted = 2,
}
</pre>

### New Type MediaPlayer.MPMediaPlaylistCreationMetadata

<pre style='color: green'>
public class MPMediaPlaylistCreationMetadata : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	protected MPMediaPlaylistCreationMetadata (Foundation.NSObjectFlag t);
	protected MPMediaPlaylistCreationMetadata (IntPtr handle);
	public MPMediaPlaylistCreationMetadata (string name);
	// properties
	public virtual string AuthorDisplayName { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual string DescriptionText { get; set; }
	public virtual string Name { get; }
}
</pre>

## Namespace NetworkExtension

### Type Changed: NetworkExtension.NEAppProxyFlowError

Added values:

<pre style='color: green'>
	DatagramTooLarge = 9,
	ReadAlreadyPending = 10,
</pre>

### Type Changed: NetworkExtension.NEAppRule

Added property:

<pre style='color: green'>
	public virtual string MatchPath { get; set; }
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_STRET = 536870912,
</pre>

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string SdkVersion = "9.2" "9.3";
	public const string Version = "9.4.0" "9.5.99";
```

Added field:

<pre style='color: green'>
	public static const string HealthKitUILibrary = "/System/Library/Frameworks/HealthKitUI.framework/HealthKit";
</pre>

### Type Changed: ObjCRuntime.Platform

Added values:

<pre style='color: green'>
	iOS_9_3 = 590592,
	Mac_10_11_3 = 2826857279913984,
</pre>

## Namespace StoreKit

### Type Changed: StoreKit.SKError

Added values:

<pre style='color: green'>
	CloudServiceNetworkConnectionFailed = 7,
	CloudServicePermissionDenied = 6,
</pre>

### Type Changed: StoreKit.SKStoreProductParameterKey

Added property:

<pre style='color: green'>
	public static Foundation.NSString AdvertisingPartnerToken { get; }
</pre>

### New Type StoreKit.SKCloudServiceAuthorizationStatus

<pre style='color: green'>
[Serializable]
public enum SKCloudServiceAuthorizationStatus {
	Authorized = 3,
	Denied = 1,
	NotDetermined = 0,
	Restricted = 2,
}
</pre>

### New Type StoreKit.SKCloudServiceCapability

<pre style='color: green'>
[Serializable]
public enum SKCloudServiceCapability {
	AddToCloudMusicLibrary = 256,
	MusicCatalogPlayback = 1,
	None = 0,
}
</pre>

### New Type StoreKit.SKCloudServiceController

<pre style='color: green'>
public class SKCloudServiceController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public SKCloudServiceController ();
	protected SKCloudServiceController (Foundation.NSObjectFlag t);
	protected SKCloudServiceController (IntPtr handle);
	// properties
	public static SKCloudServiceAuthorizationStatus AuthorizationStatus { get; }
	public override IntPtr ClassHandle { get; }
	public static Foundation.NSString CloudServiceCapabilitiesDidChangeNotification { get; }
	public static Foundation.NSString StorefrontIdentifierDidChangeNotification { get; }
	// methods
	public static void RequestAuthorization (System.Action&lt;SKCloudServiceAuthorizationStatus&gt; handler);
	public static System.Threading.Tasks.Task&lt;SKCloudServiceAuthorizationStatus&gt; RequestAuthorizationAsync ();
	public virtual void RequestCapabilities (System.Action&lt;SKCloudServiceCapability,Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;SKCloudServiceCapability&gt; RequestCapabilitiesAsync ();
	public virtual void RequestStorefrontIdentifier (System.Action&lt;Foundation.NSString,Foundation.NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task&lt;Foundation.NSString&gt; RequestStorefrontIdentifierAsync ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveCloudServiceCapabilitiesDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
		public static Foundation.NSObject ObserveStorefrontIdentifierDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

## Namespace UIKit

### Type Changed: UIKit.UIUserInterfaceIdiom

Added value:

<pre style='color: green'>
	CarPlay = 3,
</pre>

## Namespace WatchConnectivity

### Type Changed: WatchConnectivity.WCErrorCode

Added values:

<pre style='color: green'>
	SessionInactive = 7016,
	TransferTimedOut = 7017,
</pre>

### Type Changed: WatchConnectivity.WCSession

Added property:

<pre style='color: green'>
	public virtual WCSessionActivationState ActivationState { get; }
</pre>

### Type Changed: WatchConnectivity.WCSessionDelegate

Added methods:

<pre style='color: green'>
	public virtual void ActivationDidComplete (WCSession session, WCSessionActivationState activationState, Foundation.NSError error);
	public virtual void DidBecomeInactive (WCSession session);
	public virtual void DidDeactivate (WCSession session);
</pre>

### Type Changed: WatchConnectivity.WCSessionDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void ActivationDidComplete (IWCSessionDelegate This, WCSession session, WCSessionActivationState activationState, Foundation.NSError error);
	public static void DidBecomeInactive (IWCSessionDelegate This, WCSession session);
	public static void DidDeactivate (IWCSessionDelegate This, WCSession session);
</pre>

### New Type WatchConnectivity.WCSessionActivationState

<pre style='color: green'>
[Serializable]
public enum WCSessionActivationState {
	Activated = 2,
	Inactive = 1,
	NotActivated = 0,
}
</pre>

## New Namespace HealthKitUI

### New Type HealthKitUI.HKActivityRingView

<pre style='color: green'>
public class HKActivityRingView : UIKit.UIView, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	public HKActivityRingView (CoreGraphics.CGRect frame);
	public HKActivityRingView (Foundation.NSCoder coder);
	protected HKActivityRingView (Foundation.NSObjectFlag t);
	protected HKActivityRingView (IntPtr handle);
	// properties
	public virtual HealthKit.HKActivitySummary ActivitySummary { get; set; }
	public static HKActivityRingView.HKActivityRingViewAppearance Appearance { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public static HKActivityRingView.HKActivityRingViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; ();
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance (UIKit.UITraitCollection traits);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);
	public static HKActivityRingView.HKActivityRingViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual void SetActivitySummary (HealthKit.HKActivitySummary activitySummary, bool animated);

	// inner types
	public class HKActivityRingViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		protected HKActivityRingView (IntPtr handle);
	}
}
</pre>

   


 <hr>
