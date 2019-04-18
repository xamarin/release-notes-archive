---
id: 2DE3E115-A611-4224-A4BB-357B7157ED08
title: "From 5.99.0 to 5.99.2"
---

 <html>
<head>
  <title>Comparison between MonoTouch 5.99.0 and 5.99.1</title>
<link href="prettify.css" type="text/css" rel="stylesheet">
<style type="text/css">
body {
color: #333;
  min-width: 80em;
  max-width: 120em;
}

.release-notes {
}

.release-notes p {
margin-left: 1em;
margin-right: 1em;
}
pre {
background-color: #eee;
padding-top: .5em;
padding-bottom: .5em;
margin-left: 1em;
margin-right: 1em;
overflow: auto;
}

p {
    max-width: 40em;
}
</style>
<script type="text/javascript" src="prettify.js">
</script>
</head>
<body onload="prettyPrint()">

<p>The changes in this release include updates to iOS 6.0 Beta 4 as
well as some additions that were still pending from the early betas.
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre class='prettyprint'>
    public const string Version = "5.99.0";
</pre>
<p>Added:</p><pre class='prettyprint'>
    public const string Version = "5.99.2";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriter</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual bool FinishWriting ();
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("This is a synchronous methods, use the asynchronous FinishWriting(NSAction completionHandler) instead")]
   public virtual bool FinishWriting ();
   public virtual void FinishWriting (MonoTouch.Foundation.NSAction completionHandler);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioRecorder</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void RecordAt (double time);
    public virtual void RecordAt (double time, float duration);
    public virtual double DeviceCurrentTime {
       get;
    }
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACFacebook</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString AppVersionKey {
    public static MonoTouch.Foundation.NSString PermissionGroupKey {
    public static MonoTouch.Foundation.NSString PermissionGroupRead {
    public static MonoTouch.Foundation.NSString PermissionGroupReadWrite {
       get;
    }
    public static MonoTouch.Foundation.NSString PermissionGroupWrite {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString AudienceEveryone {
    public static MonoTouch.Foundation.NSString AudienceFriends {
    public static MonoTouch.Foundation.NSString AudienceKey {
    public static MonoTouch.Foundation.NSString AudienceOnlyMe {
</pre>
<h2>Namespace: MonoTouch.AudioUnit</h2>
<h3>Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType</h3>
<p>Added:</p><pre class='prettyprint'>
    CPULoad,
    ParameterValueStrings,
    HostCallbacks,
    OfflineRender,
    DependentParameters,
    InputSampleInOutput,
    ParameterHistoryInfo,
    Nickname,
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBAdvertisement</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString DataOverflowServiceUUIDsKey {
       get;
    }
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Added:</p><pre class='prettyprint'>
    public void RetrievePeripherals (CBUUID[] peripheralUuids);
    public void ScanForPeripherals (CBUUID[] peripheralUuids, MonoTouch.Foundation.NSDictionary options);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Added:</p><pre class='prettyprint'>
    public void DiscoverCharacteristics (CBUUID[] charactersticUUIDs, CBService forService);
    public void DiscoverIncludedServices (CBUUID[] includedServiceUUIDs, CBService forService);
    public void DiscoverServices (CBUUID[] services);
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>Type Changed: MonoTouch.CoreLocation.CLActivityType</h3>
<p>Removed:</p><pre class='prettyprint'>
    VehicularNavigation,
    Fitness
</pre>
<p>Added:</p><pre class='prettyprint'>
    AutomotiveNavigation,
    Fitness,
    OtherNavigation
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>Type Changed: MonoTouch.CoreText.CTFont</h3>
<p>Added:</p><pre class='prettyprint'>
    public CTFontDescriptor[] DefaultCascadeList (string [] languages);
</pre>
<h3>New Type: MonoTouch.CoreText.CTFontDescriptorMatchingState</h3>
<pre class='prettyprint'>
[Serializable]
public enum CTFontDescriptorMatchingState {
   DidBegin,
   DidFinish,
   WillBeginQuerying,
   Stalled,
   WillBeginDownloading,
   Downloading,
   DidFinishDownloading,
   DidMatch,
   DidFailWithError
}
</pre>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKEventStore</h3>
<p>Removed:</p><pre class='prettyprint'>
    public EKEventStore (EKEntityMask entityTypes);
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString BluetoothAccessoryPickerErrorDomain {
       get;
    }
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSMutableUrlRequest</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool AllowsCellularAccess {
       get;
       set;
    }
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSString</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual string CapitalizeWithLocale (NSLocale locale);
    public virtual string LowercaseWithLocale (NSLocale locale);
    public virtual string UppercaseWithLocale (NSLocale locale);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeReason</h3>
<p>Removed:</p><pre class='prettyprint'>
    QuotaViolationChange
</pre>
<p>Added:</p><pre class='prettyprint'>
    QuotaViolationChange,
    AccountChange
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
 public class GKAchievementViewController : MonoTouch.UIKit.UINavigationController {
</pre>
<p>Added:</p><pre class='prettyprint'>
 public class GKAchievementViewController : GKGameCenterViewController {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKChallenge</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual string ResolveBundleID ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKGameCenterViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static GKGameCenterViewController Shared {
       get;
    }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboardViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
 public class GKLeaderboardViewController : MonoTouch.UIKit.UINavigationController {
</pre>
<p>Added:</p><pre class='prettyprint'>
 public class GKLeaderboardViewController : GKGameCenterViewController {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual bool CanBeShared {
       get;
    }
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKOverlay</h3>
<p>Added:</p><pre class='prettyprint'>
    public MKOverlay ();
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre class='prettyprint'>
    public static void void_objc_msgSend_Double_float (IntPtr receiver, IntPtr selector, double arg1, float arg2);
    public static void void_objc_msgSendSuper_Double_float (IntPtr receiver, IntPtr selector, double arg1, float arg2);
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>Type Changed: MonoTouch.PassKit.PKPassLibrary</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString RemovedPassesUserInfoKey {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString PassTypeIdentifierUserInfoKey {
       get;
    }
    public static MonoTouch.Foundation.NSString RemovedPassInfosUserInfoKey {
    public static MonoTouch.Foundation.NSString SerialNumberUserInfoKey {
       get;
    }
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayout</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
    public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedSupplementaryElement (string elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
    public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
    public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedSupplementaryELement (string elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINib</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
</pre>
<p>Added:</p><pre class='prettyprint'>
   public virtual MonoTouch.Foundation.NSObject[] Instantiate (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
   [Obsolete("Use Instantiate method")]
   public MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
</pre>
</body>
</html>
