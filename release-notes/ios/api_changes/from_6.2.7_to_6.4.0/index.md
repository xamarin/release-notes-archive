---
id: F06BB548-E159-41C0-BDE0-5E19215661AC
title: "From 6.2.7 to 6.4.0"
---

<html><head><title>Comparison between monotouch-6.2.7.dll and monotouch-6.4.0.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.2.7";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.4.0";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Removed:</p><pre>
 	public virtual AVPlayerItemOutput Outputs {
</pre>
<p>Added:</p><pre>
 	public virtual AVPlayerItemOutput[] Outputs {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemVideoOutput</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
</pre>
<p>Added:</p><pre>
 	public MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
 	protected virtual IntPtr WeakCopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccountStore</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;ACAccountCredentialRenewResult&gt; RenewCredentialsAsync (ACAccount account);
 	[Obsolete("Obsolete in iOS 6.0. Use overload with options instead")]
	public virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType);
 	public System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType, AccountStoreOptions options);
 	protected virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SaveAccountAsync (ACAccount account);
</pre>
<h2>Namespace: MonoTouch.AddressBook</h2>
<h3>Type Changed: MonoTouch.AddressBook.ABPerson</h3>
<p>Removed:</p><pre>
 	public void SetAddresses (ABMultiValue`1 addresses);
 	public void SetInstantMessages (ABMultiValue`1 value);
 	public void SetSocialProfile (ABMultiValue`1 value);
</pre>
<p>Added:</p><pre>
 	public void SetAddresses (ABMultiValue`1 addresses);
 	public void SetInstantMessages (ABMultiValue`1 value);
 	public void SetSocialProfile (ABMultiValue`1 value);
</pre>
<h2>Namespace: MonoTouch.AssetsLibrary</h2>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAsset</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; SetImageDataAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; SetVideoAtPathAsync (MonoTouch.Foundation.NSUrl videoPathURL);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteModifiedImageToSavedToPhotosAlbumAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteModifiedVideoToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSUrl videoPathURL);
</pre>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.CoreGraphics.CGImage imageData, ALAssetOrientation orientation);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.CoreGraphics.CGImage imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteVideoToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSUrl videoPathURL);
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioStreamBasicDescription</h3>
<p>Removed:</p><pre>
 	public const double AudioStreamAnyRate = 0;
</pre>
<p>Added:</p><pre>
 	public const double AudioStreamAnyRate = 0;
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Added:</p><pre>
 	public void ConnectPeripheral (CBPeripheral peripheral, PeripheralConnectionOptions options);
 	public void ScanForPeripherals (CBUUID[] peripheralUuids, PeripheralScanningOptions options);
 	public void ScanForPeripherals (Guid [] serviceUuids, PeripheralScanningOptions options);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.PeripheralConnectionOptions</h3>
<pre>
public class PeripheralConnectionOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public PeripheralConnectionOptions ();
	public PeripheralConnectionOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public bool NotifyOnConnectionKey {
		set;
	}
	public bool NotifyOnDisconnectionKey {
		set;
	}
	public bool NotifyOnNotificationKey {
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.PeripheralScanningOptions</h3>
<pre>
public class PeripheralScanningOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public PeripheralScanningOptions ();
	public PeripheralScanningOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public bool AllowDuplicatesKey {
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchObject</h3>
<p>Added:</p><pre>
 	public void SetTargetQueue (DispatchQueue queue);
</pre>
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>Type Changed: MonoTouch.CoreMedia.CMSampleBuffer</h3>
<p>Added:</p><pre>
 	public static CMSampleBuffer CreateWithNewTiming (CMSampleBuffer original, CMSampleTimingInfo[] timing);
 	public static CMSampleBuffer CreateWithNewTiming (CMSampleBuffer original, CMSampleTimingInfo[] timing, out int status);
 	public CMSampleTimingInfo[] GetSampleTimingInfo ();
 	public CMSampleTimingInfo[] GetSampleTimingInfo (out int status);
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMTime</h3>
<p>Removed:</p><pre>
 	public const int MaxTimeScale = 2147483647;
</pre>
<p>Added:</p><pre>
 	public const int MaxTimeScale = 2147483647;
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>Type Changed: MonoTouch.CoreText.CTFontDescriptor</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated")]
	public CTFontDescriptor WithFeature (Selector featureSelector);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated")]
	public CTFontDescriptor WithFeature (Selector featureSelector);
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h3>
<p>Removed:</p><pre>
 	protected override void Finalize ();
 	
</pre>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKEventStore</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;EKReminder[]&gt; FetchRemindersAsync (MonoTouch.Foundation.NSPredicate predicate);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (EKEntityType entityType);
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task ShowBluetoothAccessoryPickerAsync (MonoTouch.Foundation.NSPredicate predicate);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSComparisonPredicateOptions</h3>
<p>Removed:</p><pre>
 	DiacriticInsensitive
</pre>
<p>Added:</p><pre>
 	DiacriticInsensitive,
 	Normalized
</pre>
<h3>New Type: MonoTouch.Foundation.NSMutableOrderedSet</h3>
<pre>
public class NSMutableOrderedSet : NSOrderedSet {
	
	public NSMutableOrderedSet (params NSObject[] objs);
	public NSMutableOrderedSet (params object [] objs);
	public NSMutableOrderedSet (params string [] strings);
	public NSMutableOrderedSet ();
	public NSMutableOrderedSet (NSCoder coder);
	public NSMutableOrderedSet (NSObjectFlag t);
	public NSMutableOrderedSet (IntPtr handle);
	public NSMutableOrderedSet (NSObject start);
	public NSMutableOrderedSet (NSSet source);
	public NSMutableOrderedSet (NSOrderedSet source);
	public NSMutableOrderedSet (int capacity);
	
	public virtual void Add (NSObject obj);
	public virtual void AddObjects (NSObject[] source);
	public virtual void ExchangeObject (int first, int second);
	public virtual void Insert (NSObject obj, int atIndex);
	public virtual void InsertObjects (NSObject[] objects, NSIndexSet atIndexes);
	public virtual void Intersect (NSOrderedSet intersectWith);
	public virtual void MoveObjects (NSIndexSet indexSet, int destination);
	public virtual void Remove (int index);
	public virtual void RemoveAllObjects ();
	public virtual void RemoveObject (NSObject obj);
	public virtual void RemoveObjects (NSIndexSet indexSet);
	public virtual void RemoveObjects (NSObject[] objects);
	public virtual void RemoveObjects (NSRange range);
	public virtual void Replace (int objectAtIndex, NSObject newObject);
	public virtual void ReplaceObjects (NSIndexSet indexSet, NSObject[] replacementObjects);
	public virtual void SetObject (NSObject obj, int index);
	public virtual void Sort (NSComparator comparator);
	public virtual void Sort (NSSortOptions sortOptions, NSComparator comparator);
	public virtual void SortRange (NSRange range, NSSortOptions sortOptions, NSComparator comparator);
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSObject this [int idx] {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSOrderedSet</h3>
<pre>
public class NSOrderedSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<nsobject> {
	
	public NSOrderedSet (params NSObject[] objs);
	public NSOrderedSet (params object [] objs);
	public NSOrderedSet (params string [] strings);
	public NSOrderedSet ();
	public NSOrderedSet (NSCoder coder);
	public NSOrderedSet (NSObjectFlag t);
	public NSOrderedSet (IntPtr handle);
	public NSOrderedSet (NSObject start);
	public NSOrderedSet (NSSet source);
	public NSOrderedSet (NSOrderedSet source);
	
	public static NSOrderedSet MakeNSOrderedSet<t> (T[] values) where T : NSObject;
	public virtual NSSet AsSet ();
	public virtual bool Contains (NSObject obj);
	public bool Contains (object obj);
	public virtual NSObject FirstObject ();
	public System.Collections.Generic.IEnumerator<nsobject> GetEnumerator ();
	public virtual NSOrderedSet GetReverseOrderedSet ();
	public virtual int IndexOf (NSObject obj);
	public virtual bool Intersects (NSOrderedSet other);
	public virtual bool Intersects (NSSet other);
	public virtual bool IsEqualToOrderedSet (NSOrderedSet other);
	public virtual bool IsSubset (NSOrderedSet other);
	public virtual bool IsSubset (NSSet other);
	public virtual NSObject LastObject ();
	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
	public T[] ToArray<t> () where T : NSObject;
	
	public static NSOrderedSet operator + (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSSet second);
	public static bool operator == (NSOrderedSet first, NSOrderedSet second);
	public static bool operator != (NSOrderedSet first, NSOrderedSet second);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int Count {
		get;
	}
	public NSObject this [int idx] {
		get;
	}
}
</t></nsobject></t></nsobject></pre>
<h3>Type Changed: MonoTouch.Foundation.NSRange</h3>
<p>Removed:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<p>Added:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<h3>New Type: MonoTouch.Foundation.NSSortOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSSortOptions {
	Concurrent,
	Stable
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUserDefaults</h3>
<p>Added:</p><pre>
 	public static NSString ArgumentDomain {
 		get;
 	}
 	public static NSString GlobalDomain {
 		get;
 	}
 	public static NSString RegistrationDomain {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.GLKit</h2>
<h3>Type Changed: MonoTouch.GLKit.GLKTextureLoader</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginLoadCubeMapAsync (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginLoadCubeMapAsync (string fileName, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (string file, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievement</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKAchievement[]&gt; LoadAchievementsAsync ();
 	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements);
 	public static System.Threading.Tasks.Task ResetAchivementsAsync ();
 	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; SelectChallengeablePlayerIDsAsync (string [] playerIDs);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementDescription</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKAchievementDescription[]&gt; LoadAchievementDescriptionsAsync ();
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.UIKit.UIImage&gt; LoadImageAsync ();
</pre>
<h3>New Type: MonoTouch.GameKit.GKCategoryResult</h3>
<pre>
public class GKCategoryResult {
	
	public GKCategoryResult (string [] categories, string [] titles);
	
	public string [] Categories {
		get;
		set;
	}
	public string [] Titles {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKChallenge</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKChallenge[]&gt; LoadReceivedChallengesAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboard</h3>
<p>Added:</p><pre>
 	[Obsolete("Deprecated iOS 6.0, use loadLeaderboardsWithCompletionHandler")]
	public static System.Threading.Tasks.Task&lt;GKCategoryResult&gt; LoadCategoriesAsync ();
 	public static System.Threading.Tasks.Task&lt;GKLeaderboard[]&gt; LoadLeaderboardsAsync ();
 	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string categoryID);
 	public virtual System.Threading.Tasks.Task&lt;GKScore[]&gt; LoadScoresAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLocalPlayer</h3>
<p>Added:</p><pre>
 	[Obsolete("Replaced by AuthenticateHandler in iOS 6.0")]
	public virtual System.Threading.Tasks.Task AuthenticateAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string&gt; LoadDefaultLeaderboardCategoryIDAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; LoadFriendsAsync ();
 	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatch</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;string&gt; ChooseBestHostPlayerAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; RematchAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmaker</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task AddPlayersAsync (GKMatch toMatch, GKMatchRequest matchRequest);
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; FindMatchAsync (GKMatchRequest request);
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; FindPlayersAsync (GKMatchRequest request);
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; MatchAsync (GKInvite invite);
 	public virtual System.Threading.Tasks.Task&lt;int&gt; QueryActivityAsync ();
 	public virtual System.Threading.Tasks.Task&lt;int&gt; QueryPlayerGroupActivityAsync (int playerGroup);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKNotificationBanner</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task ShowAsync (string title, string message);
 	public static System.Threading.Tasks.Task ShowAsync (string title, string message, double durationSeconds);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKPlayer</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKPlayer[]&gt; LoadPlayersForIdentifiersAsync (string [] identifiers);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.UIKit.UIImage&gt; LoadPhotoAsync (GKPhotoSize size);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task ReportScoresAsync (GKScore[] scores);
 	public virtual System.Threading.Tasks.Task ReportScoreAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatch</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; FindMatchAsync (GKMatchRequest request);
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; LoadMatchAsync (string matchId);
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch[]&gt; LoadMatchesAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; AcceptInviteAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; DeclineInviteAsync ();
 	public virtual System.Threading.Tasks.Task EndMatchInTurnAsync (MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task EndTurnAsync (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData);
 	[Obsolete("Replaced by EndTurn in iOS 6.0")]
	public virtual System.Threading.Tasks.Task EndTurnWithNextParticipantAsync (GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSData&gt; LoadMatchDataAsync ();
 	[Obsolete("Replaced by ParticipantQuitInTurn (GKTurnBasedMatchOutcome, GKTurnBasedParticipant[], double, NSData, Action&lt;NSError&gt;) in iOS 6.0")]
	public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task ParticipantQuitOutOfTurnAsync (GKTurnBasedMatchOutcome matchOutcome);
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; RematchAsync ();
 	public virtual System.Threading.Tasks.Task RemoveAsync ();
 	public virtual System.Threading.Tasks.Task SaveCurrentTurnAsync (MonoTouch.Foundation.NSData matchData);
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKLocalSearch</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MKLocalSearchResponse&gt; StartAsync ();
 	public virtual System.Threading.Tasks.Task&lt;MKLocalSearchResponse&gt; StartAsync (System.Threading.CancellationToken token);
</pre>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty</h3>
<p>Removed:</p><pre>
 public static class MPMediaItemProperty {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public static class MPMediaItemProperty {
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Selector</h3>
<p>Added:</p><pre>
 	public static Selector FromHandle (IntPtr sel);
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewController</h3>
<p>Added:</p><pre>
 	public System.Threading.Tasks.Task&lt;bool&gt; LoadProductAsync (StoreProductParameters parameters);
</pre>
<h2>Namespace: MonoTouch.SystemConfiguration</h2>
<h3>Type Changed: MonoTouch.SystemConfiguration.NetworkReachability</h3>
<p>Added:</p><pre>
 	public bool Schedule ();
 	public bool SetDispatchQueue (MonoTouch.CoreFoundation.DispatchQueue queue);
 	public bool Unschedule ();
</pre>
<h2>Namespace: MonoTouch.Twitter</h2>
<h3>Type Changed: MonoTouch.Twitter.TWRequest</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;TWRequestResult&gt; PerformRequestAsync ();
</pre>
<h3>New Type: MonoTouch.Twitter.TWRequestResult</h3>
<pre>
public class TWRequestResult {
	
	public TWRequestResult (MonoTouch.Foundation.NSData responseData, MonoTouch.Foundation.NSHttpUrlResponse urlResponse);
	
	public MonoTouch.Foundation.NSData ResponseData {
		get;
		set;
	}
	public MonoTouch.Foundation.NSHttpUrlResponse UrlResponse {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; PerformBatchUpdatesAsync (MonoTouch.Foundation.NSAction updates);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Removed:</p><pre>
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForDecorationView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
</pre>
<p>Added:</p><pre>
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForDecorationView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDevice</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0")]
	public virtual string UniqueIdentifier {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0. Apple now reject application using it the selector is removed and an empty string is returned")]
	public virtual string UniqueIdentifier {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocument</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; AutoSaveAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; CloseAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; OpenAsync ();
 	public virtual System.Threading.Tasks.Task PerformAsynchronousFileAccessAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; RevertToContentsOfUrlAsync (MonoTouch.Foundation.NSUrl url);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SaveAsync (MonoTouch.Foundation.NSUrl url, UIDocumentSaveOperation saveOperation);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Removed:</p><pre>
 	public UIImage (UIImage image);
 	public UIImage (UIImage image, MonoTouch.Foundation.NSDictionary options);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SetViewControllersAsync (UIViewController[] viewControllers, UIPageViewControllerNavigationDirection direction, bool animated);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionController</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentAsync (bool animated);
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentFromBarButtonItemAsync (UIBarButtonItem item, bool animated);
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentFromRectInViewAsync (System.Drawing.RectangleF rect, UIView view, bool animated);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPrintInteractionResult</h3>
<pre>
public class UIPrintInteractionResult {
	
	public UIPrintInteractionResult (UIPrintInteractionController printInteractionController, bool completed);
	
	public bool Completed {
		get;
		set;
	}
	public UIPrintInteractionController PrintInteractionController {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateNotifyAsync (double duration, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateNotifyAsync (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; TransitionNotifyAsync (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; TransitionNotifyAsync (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task DismissViewControllerAsync (bool animated);
 	public virtual System.Threading.Tasks.Task PresentViewControllerAsync (UIViewController viewControllerToPresent, bool animated);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; TransitionAsync (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations);
</pre>
</body>
</html>
