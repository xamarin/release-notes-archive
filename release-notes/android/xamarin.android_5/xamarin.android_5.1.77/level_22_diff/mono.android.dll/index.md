---
id: 4E27927B-2A01-4FEE-8A7F-D51F53F4EB0F
---

## Namespace Android

### Type Changed: Android.Manifest

### Type Changed: Android.Manifest.Permission

Added field:

<pre style='color: green'>
	public static const string BindCarrierMessagingService = "android.permission.BIND_CARRIER_MESSAGING_SERVICE";
</pre>

### Type Changed: Android.Resource

### Type Changed: Android.Resource.Attribute

Added fields:

<pre style='color: green'>
	public static const int AccessibilityTraversalAfter;
	public static const int AccessibilityTraversalBefore;
	public static const int CollapseContentDescription;
	public static const int DialogPreferredPadding;
	public static const int ResizeClip;
	public static const int RevisionCode;
	public static const int SearchHintIcon;
</pre>

### Type Changed: Android.Resource.Style

Added fields:

<pre style='color: green'>
	public static const int ThemeDeviceDefaultDialogAlert;
	public static const int ThemeDeviceDefaultLightDialogAlert;
</pre>

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
</pre>

## Namespace Android.Accounts

### Type Changed: Android.Accounts.AccountManager

Obsoleted methods:

```
[Obsolete (]
	public virtual IAccountManagerFuture RemoveAccount (Account account, IAccountManagerCallback callback, Android.OS.Handler handler);
```

Added methods:

<pre style='color: green'>
	public virtual IAccountManagerFuture RemoveAccount (Account account, Android.App.Activity activity, IAccountManagerCallback callback, Android.OS.Handler handler);
	public virtual bool RemoveAccountExplicitly (Account account);
</pre>

## Namespace Android.Animation

### Type Changed: Android.Animation.StateListAnimator

Added interface:

<pre style='color: green'>
	Java.Lang.ICloneable
</pre>

Added method:

<pre style='color: green'>
	public virtual StateListAnimator Clone ();
</pre>

### Type Changed: Android.Animation.ValueAnimator

Added method:

<pre style='color: green'>
	public virtual void SetCurrentFraction (float fraction);
</pre>

## Namespace Android.App

### Type Changed: Android.App.Activity

Added property:

<pre style='color: green'>
	public virtual Android.Net.Uri Referrer { get; }
</pre>

### Type Changed: Android.App.KeyguardManager

Added property:

<pre style='color: green'>
	public virtual bool IsDeviceLocked { get; }
</pre>

### Type Changed: Android.App.Notification

### Type Changed: Android.App.Notification.Action

### Type Changed: Android.App.Notification.WearableExtender

Added properties:

<pre style='color: green'>
	public string CancelLabel { get; }
	public Java.Lang.ICharSequence CancelLabelFormatted { get; }
	public string ConfirmLabel { get; }
	public Java.Lang.ICharSequence ConfirmLabelFormatted { get; }
	public string InProgressLabel { get; }
	public Java.Lang.ICharSequence InProgressLabelFormatted { get; }
</pre>

Added methods:

<pre style='color: green'>
	public Notification.Action.WearableExtender SetCancelLabel (string label);
	public Notification.Action.WearableExtender SetCancelLabel (Java.Lang.ICharSequence label);
	public Notification.Action.WearableExtender SetConfirmLabel (Java.Lang.ICharSequence label);
	public Notification.Action.WearableExtender SetConfirmLabel (string label);
	public Notification.Action.WearableExtender SetInProgressLabel (Java.Lang.ICharSequence label);
	public Notification.Action.WearableExtender SetInProgressLabel (string label);
</pre>

### Type Changed: Android.App.Notification.WearableExtender

Added fields:

<pre style='color: green'>
	public static const int ScreenTimeoutLong;
	public static const int ScreenTimeoutShort;
</pre>

Added properties:

<pre style='color: green'>
	public bool HintAvoidBackgroundClipping { get; }
	public int HintScreenTimeout { get; }
</pre>

Added methods:

<pre style='color: green'>
	public Notification.WearableExtender SetHintAvoidBackgroundClipping (bool hintAvoidBackgroundClipping);
	public Notification.WearableExtender SetHintScreenTimeout (int timeout);
</pre>

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DevicePolicyManager

Added fields:

<pre style='color: green'>
	public static const string ExtraProvisioningAccountToMigrate = "android.app.extra.PROVISIONING_ACCOUNT_TO_MIGRATE";
	public static const string ExtraProvisioningLeaveAllSystemAppsEnabled = "android.app.extra.PROVISIONING_LEAVE_ALL_SYSTEM_APPS_ENABLED";

	[Obsolete]
	public static const WipeDataFlags WipeResetProtectionData;
</pre>

### Type Changed: Android.App.Admin.WipeDataFlags

Added value:

<pre style='color: green'>
	WipeResetProtectionData = 2,
</pre>

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothGattServerCallback

Added method:

<pre style='color: green'>
	public virtual void OnMtuChanged (BluetoothDevice device, int mtu);
</pre>

## Namespace Android.Content

### Type Changed: Android.Content.Context

Added fields:

<pre style='color: green'>
	public static const string TelephonySubscriptionService = "telephony_subscription_service";
	public static const string UsageStatsService = "usagestats";
</pre>

### Type Changed: Android.Content.Intent

Added fields:

<pre style='color: green'>
	public static const string ExtraChosenComponent = "android.intent.extra.CHOSEN_COMPONENT";
	public static const string ExtraChosenComponentIntentSender = "android.intent.extra.CHOSEN_COMPONENT_INTENT_SENDER";
	public static const string ExtraReferrerName = "android.intent.extra.REFERRER_NAME";

	[Obsolete]
	public static const IntentUriType UriAllowUnsafe;

	[Obsolete]
	public static const IntentUriType UriAndroidAppScheme;
</pre>

Added methods:

<pre style='color: green'>
	public static Intent CreateChooser (Intent target, Java.Lang.ICharSequence title, IntentSender sender);
	public static Intent CreateChooser (Intent target, string title, IntentSender sender);
</pre>

### Type Changed: Android.Content.IntentUriType

Added values:

<pre style='color: green'>
	AllowUnsafe = 4,
	AndroidAppScheme = 2,
</pre>

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.PackageInfo

Added properties:

<pre style='color: green'>
	public int BaseRevisionCode { get; set; }
	public System.Collections.Generic.IList&lt;int&gt; SplitRevisionCodes { get; set; }
</pre>

### Type Changed: Android.Content.PM.PackageItemInfo

Added method:

<pre style='color: green'>
	public virtual Android.Graphics.Drawables.Drawable LoadUnbadgedIcon (PackageManager pm);
</pre>

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.Resources

Obsoleted methods:

```
[Obsolete (]
	public virtual Android.Graphics.Drawables.Drawable GetDrawable (int id);
	[Obsolete (]
	public virtual Android.Graphics.Drawables.Drawable GetDrawableForDensity (int id, int density);
```

### Type Changed: Android.Content.Res.TypedArray

Added method:

<pre style='color: green'>
	public virtual bool HasValueOrEmpty (int index);
</pre>

## Namespace Android.Graphics

### Type Changed: Android.Graphics.Outline

Added method:

<pre style='color: green'>
	public void Offset (int dx, int dy);
</pre>

## Namespace Android.Hardware

### Type Changed: Android.Hardware.SensorManager

Modified methods:

```
public virtual bool RegisterListener (ISensorEventListener listener, Sensor sensor, SensorDelay rateUs samplingPeriodUs, int maxBatchReportLatencyUs maxReportLatencyUs, Android.OS.Handler handler)
	public virtual bool RegisterListener (ISensorEventListener listener, Sensor sensor, SensorDelay rateUs samplingPeriodUs, int maxBatchReportLatencyUs maxReportLatencyUs)
	public virtual bool RegisterListener (ISensorEventListener listener, Sensor sensor, SensorDelay rateUs samplingPeriodUs, Android.OS.Handler handler)
	public virtual bool RegisterListener (ISensorEventListener listener, Sensor sensor, SensorDelay rateUs samplingPeriodUs)
```

## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.ControlSceneMode

Added value:

<pre style='color: green'>
	Hdr = 18,
</pre>

### Type Changed: Android.Hardware.Camera2.RequestAvailableCapabilities

Added values:

<pre style='color: green'>
	BurstCapture = 6,
	ReadSensorSettings = 5,
</pre>

## Namespace Android.Media

### Type Changed: Android.Media.AudioAttributes

Added property:

<pre style='color: green'>
	public AudioUsageKind Usage { get; }
</pre>

### Type Changed: Android.Media.AudioAttributes.Builder

Added method:

<pre style='color: green'>
	public virtual AudioAttributes.Builder SetUsage (AudioUsageKind usage);
</pre>

### Type Changed: Android.Media.MediaDrm

Added methods:

<pre style='color: green'>
	public byte[] GetSecureStop (byte[] ssid);
	public void ReleaseAllSecureStops ();
</pre>

## Namespace Android.Media.Session

### Type Changed: Android.Media.Session.MediaSession

Added method:

<pre style='color: green'>
	public void SetRatingType (Android.Media.RatingStyle type);
</pre>

### Type Changed: Android.Media.Session.PlaybackState

Added property:

<pre style='color: green'>
	public Android.OS.Bundle Extras { get; }
</pre>

### Type Changed: Android.Media.Session.PlaybackState.Builder

Added method:

<pre style='color: green'>
	public PlaybackState.Builder SetExtras (Android.OS.Bundle extras);
</pre>

## Namespace Android.Media.TV

### Type Changed: Android.Media.TV.TvContract

### Type Changed: Android.Media.TV.TvContract.Programs

### Type Changed: Android.Media.TV.TvContract.Genres

Added fields:

<pre style='color: green'>
	public static const string Arts = "ARTS";
	public static const string Entertainment = "ENTERTAINMENT";
	public static const string LifeStyle = "LIFE_STYLE";
	public static const string Music = "MUSIC";
	public static const string Premier = "PREMIER";
	public static const string TechScience = "TECH_SCIENCE";
</pre>

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Added fields:

<pre style='color: green'>
	public static const string ExtraNetwork = "android.net.extra.NETWORK";
	public static const string ExtraNetworkRequest = "android.net.extra.NETWORK_REQUEST";
</pre>

Added methods:

<pre style='color: green'>
	public virtual void ReleaseNetworkRequest (Android.App.PendingIntent operation);
	public virtual void RequestNetwork (NetworkRequest request, Android.App.PendingIntent operation);
</pre>

### Type Changed: Android.Net.Network

Added method:

<pre style='color: green'>
	public virtual void BindSocket (Java.Net.DatagramSocket socket);
</pre>

### Type Changed: Android.Net.SSLCertificateSocketFactory

Obsoleted methods:

```
[Obsolete (]
	public static Org.Apache.Http.Conn.Ssl.SSLSocketFactory GetHttpSocketFactory (int handshakeTimeoutMillis, SSLSessionCache cache);
```

### Type Changed: Android.Net.VpnService

Added method:

<pre style='color: green'>
	public virtual bool SetUnderlyingNetworks (Network[] networks);
</pre>

### Type Changed: Android.Net.VpnService.Builder

Added method:

<pre style='color: green'>
	public virtual VpnService.Builder SetUnderlyingNetworks (Network[] networks);
</pre>

## Namespace Android.Net.Http

### Type Changed: Android.Net.Http.AndroidHttpClient

Obsoleted methods:

```
[Obsolete (]
	public static AndroidHttpClient NewInstance (string userAgent);
	[Obsolete (]
	public static AndroidHttpClient NewInstance (string userAgent, Android.Content.Context context);
```

## Namespace Android.Net.Wifi.P2p

### Type Changed: Android.Net.Wifi.P2p.WifiP2pManager

Added method:

<pre style='color: green'>
	public virtual void SetServiceResponseListener (WifiP2pManager.Channel c, WifiP2pManager.IServiceResponseListener listener);
</pre>

### New Type Android.Net.Wifi.P2p.IServiceResponseListener

<pre style='color: green'>
public interface IServiceResponseListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnServiceAvailable (Nsd.ServiceType protocolType, byte[] responseData, WifiP2pDevice srcDevice);
}
</pre>

### New Type Android.Net.Wifi.P2p.ServiceResponseEventArgs

<pre style='color: green'>
public class ServiceResponseEventArgs : System.EventArgs {
	// constructors
	public WifiP2pManager (Nsd.ServiceType protocolType, byte[] responseData, WifiP2pDevice srcDevice);
	// properties
	public Nsd.ServiceType ProtocolType { get; }
	public byte[] ResponseData { get; }
	public WifiP2pDevice SrcDevice { get; }
}
</pre>

## Namespace Android.Net.Wifi.P2p.Nsd

### Type Changed: Android.Net.Wifi.P2p.Nsd.WifiP2pServiceInfo

Obsoleted fields:

```
[Obsolete (]
	public static const ServiceType ServiceTypeAll;
	[Obsolete (]
	public static const ServiceType ServiceTypeBonjour;
	[Obsolete (]
	public static const ServiceType ServiceTypeUpnp;
	[Obsolete (]
	public static const ServiceType ServiceTypeVendorSpecific;
```

Modified fields:

```
public const int ServiceType ServiceTypeAll = 0;
	public const int ServiceType ServiceTypeBonjour = 1;
	public const int ServiceType ServiceTypeUpnp = 2;
	public const int ServiceType ServiceTypeVendorSpecific = 255;
```

### Type Changed: Android.Net.Wifi.P2p.Nsd.WifiP2pServiceRequest

Added methods:

<pre style='color: green'>
	public static WifiP2pServiceRequest NewInstance (ServiceType protocolType);
	public static WifiP2pServiceRequest NewInstance (ServiceType protocolType, string queryData);
</pre>

### New Type Android.Net.Wifi.P2p.Nsd.ServiceType

<pre style='color: green'>
[Serializable]
public enum ServiceType {
	All = 0,
	Bonjour = 1,
	Upnp = 2,
	VendorSpecific = 255,
}
</pre>

## Namespace Android.OS

### Type Changed: Android.OS.BaseBundle

Added methods:

<pre style='color: green'>
	public virtual bool GetBoolean (string key);
	public virtual bool GetBoolean (string key, bool defaultValue);
	public virtual bool[] GetBooleanArray (string key);
	public virtual void PutBoolean (string key, bool value);
	public virtual void PutBooleanArray (string key, bool[] value);
</pre>

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Modified fields:

```
public const BuildVersionCodes int L = 21;
```

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const BuildVersionCodes LollipopMr1;
</pre>

### Type Changed: Android.OS.BuildVersionCodes

Removed value:

<pre style='color: red'>
	L = 21,
</pre>

Added value:

<pre style='color: green'>
	LollipopMr1 = 22,
</pre>

### Type Changed: Android.OS.Bundle

Modified methods:

```
public override bool GetBoolean (string key)
	public override bool GetBoolean (string key, bool defaultValue)
	public override bool[] GetBooleanArray (string key)
	public override void PutBoolean (string key, bool value)
	public override void PutBooleanArray (string key, bool[] value)
```

### Type Changed: Android.OS.Message

Added property:

<pre style='color: green'>
	public bool Asynchronous { get; set; }
</pre>

### Type Changed: Android.OS.Parcel

Modified methods:

```
public void Unmarshall (byte[] data, int offest offset, int length)
```

### Type Changed: Android.OS.UserManager

Added fields:

<pre style='color: green'>
	public static const string DisallowOutgoingBeam = "no_outgoing_beam";
	public static const string KeyRestrictionsPending = "restrictions_pending";
</pre>

## Namespace Android.Provider

### Type Changed: Android.Provider.Settings

Added fields:

<pre style='color: green'>
	public static const string ActionBatterySaverSettings = "android.settings.BATTERY_SAVER_SETTINGS";
	public static const string ActionNotificationListenerSettings = "android.settings.ACTION_NOTIFICATION_LISTENER_SETTINGS";
</pre>

### Type Changed: Android.Provider.Telephony

### Type Changed: Android.Provider.Telephony.BaseMmsColumns

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Carriers

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Mms

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Draft

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Inbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Outbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Sent

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.MmsSms

### Type Changed: Android.Provider.Telephony.PendingMessages

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "pending_sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Sms

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Conversations

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Draft

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Inbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Outbox

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.Sent

### Type Changed: Android.Provider.Telephony.InterfaceConsts

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

### Type Changed: Android.Provider.Telephony.TextBasedSmsColumns

Added field:

<pre style='color: green'>
	public static const string SubscriptionId = "sub_id";
</pre>

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.AlwaysOnHotwordDetector

Added property:

<pre style='color: green'>
	public virtual RecognitionMode SupportedRecognitionModes { get; }
</pre>

### Type Changed: Android.Service.Voice.RecognitionMode

Added value:

<pre style='color: green'>
	None = 0,
</pre>

## Namespace Android.Telephony

### Type Changed: Android.Telephony.MmsError

Added value:

<pre style='color: green'>
	NoDataNetwork = 8,
</pre>

### Type Changed: Android.Telephony.SmsManager

Added fields:

<pre style='color: green'>
	public static const string ExtraMmsHttpStatus = "android.telephony.extra.MMS_HTTP_STATUS";
	public static const string MmsConfigShowCellBroadcastAppLinks = "config_cellBroadcastAppLinks";
</pre>

Added properties:

<pre style='color: green'>
	public static int DefaultSmsSubscriptionId { get; }
	public int SubscriptionId { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static SmsManager GetSmsManagerForSubscriptionId (int subId);
	public void InjectSmsPdu (byte[] pdu, string format, Android.App.PendingIntent receivedIntent);
</pre>

### Type Changed: Android.Telephony.TelephonyManager

Added properties:

<pre style='color: green'>
	public virtual bool HasCarrierPrivileges { get; }
	public virtual bool IsVoiceCapable { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool SetLine1NumberForDisplay (string alphaTag, string number);
	public virtual bool SetOperatorBrandOverride (string brand);
	public virtual bool SetPreferredNetworkTypeToGlobal ();
	public virtual bool SetVoiceMailNumber (string alphaTag, string number);
</pre>

### New Type Android.Telephony.DataRoamingMode

<pre style='color: green'>
[Serializable]
public enum DataRoamingMode {
	Disable = 0,
	Enable = 1,
}
</pre>

### New Type Android.Telephony.SubscriptionInfo

<pre style='color: green'>
public class SubscriptionInfo : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected SubscriptionInfo (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public string CarrierName { get; }
	public virtual Java.Lang.ICharSequence CarrierNameFormatted { get; }
	public virtual string CountryIso { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public virtual DataRoamingMode DataRoaming { get; }
	public string DisplayName { get; }
	public virtual Java.Lang.ICharSequence DisplayNameFormatted { get; }
	public virtual string IccId { get; }
	public virtual Android.Graphics.Color IconTint { get; }
	public virtual int Mcc { get; }
	public virtual int Mnc { get; }
	public virtual string Number { get; }
	public virtual int SimSlotIndex { get; }
	public virtual int SubscriptionId { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual Android.Graphics.Bitmap CreateIconBitmap (Android.Content.Context context);
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Telephony.SubscriptionManager

<pre style='color: green'>
public class SubscriptionManager : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
	// constructors
	protected SubscriptionManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	// properties
	public virtual int ActiveSubscriptionInfoCount { get; }
	public virtual int ActiveSubscriptionInfoCountMax { get; }
	public virtual System.Collections.Generic.IList&lt;SubscriptionInfo&gt; ActiveSubscriptionInfoList { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual void AddOnSubscriptionsChangedListener (SubscriptionManager.OnSubscriptionsChangedListener listener);
	public static SubscriptionManager From (Android.Content.Context context);
	public virtual SubscriptionInfo GetActiveSubscriptionInfo (int subId);
	public virtual SubscriptionInfo GetActiveSubscriptionInfoForSimSlotIndex (int slotIdx);
	public virtual bool IsNetworkRoaming (int subId);
	public virtual void RemoveOnSubscriptionsChangedListener (SubscriptionManager.OnSubscriptionsChangedListener listener);

	// inner types
	public class OnSubscriptionsChangedListener : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		protected SubscriptionManager (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SubscriptionManager ();
		// properties
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public virtual void OnSubscriptionsChanged ();
	}
}
</pre>

## Namespace Android.Transitions

### Type Changed: Android.Transitions.ChangeBounds

Added property:

<pre style='color: green'>
	public virtual bool ResizeClip { get; }
</pre>

## Namespace Android.Util

### Type Changed: Android.Util.DisplayMetrics

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const DisplayMetricsDensity Density280;
</pre>

### Type Changed: Android.Util.DisplayMetricsDensity

Added value:

<pre style='color: green'>
	D280 = 280,
</pre>

### Type Changed: Android.Util.TypedValue

Added fields:

<pre style='color: green'>
	public static const int DataNullEmpty;
	public static const int DataNullUndefined;
</pre>

Added property:

<pre style='color: green'>
	public virtual ComplexUnitType ComplexUnit { get; }
</pre>

## Namespace Android.Views

### Type Changed: Android.Views.IViewParent

Added method:

<pre style='color: green'>
	public virtual bool OnNestedPrePerformAccessibilityAction (View target, Accessibility.Action action, Android.OS.Bundle arguments);
</pre>

### Type Changed: Android.Views.View

Added properties:

<pre style='color: green'>
	public virtual int AccessibilityTraversalAfter { get; set; }
	public virtual int AccessibilityTraversalBefore { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DispatchDrawableHotspotChanged (float x, float y);
	public virtual bool DispatchNestedPrePerformAccessibilityAction (Accessibility.Action action, Android.OS.Bundle arguments);
</pre>

### Type Changed: Android.Views.ViewGroup

Added method:

<pre style='color: green'>
	public virtual bool OnNestedPrePerformAccessibilityAction (View target, Accessibility.Action action, Android.OS.Bundle args);
</pre>

### Type Changed: Android.Views.Window

Modified methods:

```
public virtual void SetBackgroundDrawableResource (int resid resId)
```

Added methods:

<pre style='color: green'>
	public static WindowFeatures GetDefaultFeatures (Android.Content.Context context);
	public virtual void SetClipToOutline (bool clipToOutline);
	public virtual void SetElevation (float elevation);
</pre>

### Type Changed: Android.Views.WindowManagerFlags

Added value:

<pre style='color: green'>
	LayoutAttachedInDecor = 1073741824,
</pre>

### Type Changed: Android.Views.WindowManagerTypes

Added value:

<pre style='color: green'>
	AccessibilityOverlay = 2032,
</pre>

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Added properties:

<pre style='color: green'>
	public virtual AccessibilityNodeInfo TraversalAfter { get; }
	public virtual AccessibilityNodeInfo TraversalBefore { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void SetTraversalAfter (Android.Views.View root, int virtualDescendantId);
	public virtual void SetTraversalAfter (Android.Views.View view);
	public virtual void SetTraversalBefore (Android.Views.View view);
	public virtual void SetTraversalBefore (Android.Views.View root, int virtualDescendantId);
</pre>

### Type Changed: Android.Views.Accessibility.AccessibilityWindowInfo

Added field:

<pre style='color: green'>
	[Obsolete]
	public static const AccessibilityWindowType TypeAccessibilityOverlay;
</pre>

### Type Changed: Android.Views.Accessibility.AccessibilityWindowType

Added value:

<pre style='color: green'>
	AccessibilityOverlay = 4,
</pre>

## Namespace Android.Views.Animations

### Type Changed: Android.Views.Animations.AccelerateDecelerateInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float input)
```

### Type Changed: Android.Views.Animations.AccelerateInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float input)
```

### Type Changed: Android.Views.Animations.AnticipateInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float t)
```

### Type Changed: Android.Views.Animations.AnticipateOvershootInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float t)
```

### Type Changed: Android.Views.Animations.BounceInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float t)
```

### Type Changed: Android.Views.Animations.CycleInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float input)
```

### Type Changed: Android.Views.Animations.DecelerateInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float input)
```

### Type Changed: Android.Views.Animations.LinearInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float input)
```

### Type Changed: Android.Views.Animations.OvershootInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float t)
```

### Type Changed: Android.Views.Animations.PathInterpolator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Java.Lang.Object</span></span>

 <span style='color:green'>Android.Views.Animations.BaseInterpolator</span>

Modified methods:

```
public virtual override float GetInterpolation (float t)
```

### New Type Android.Views.Animations.BaseInterpolator

<pre style='color: green'>
public abstract class BaseInterpolator : Java.Lang.Object, IInterpolator, Android.Animation.ITimeInterpolator, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected BaseInterpolator (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public BaseInterpolator ();
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual float GetInterpolation (float input);
}
</pre>

## Namespace Android.Webkit

### Type Changed: Android.Webkit.CookieManager

Added constructor:

<pre style='color: green'>
	public CookieManager ();
</pre>

Modified properties:

```
public abstract bool HasCookies { get; }
```

Modified methods:

```
public abstract bool AcceptCookie ()
	public abstract bool AcceptThirdPartyCookies (WebView webview)
	public abstract void Flush ()
	public abstract string GetCookie (string url)
	public abstract void RemoveAllCookie ()
	public abstract void RemoveAllCookies (IValueCallback callback)
	public abstract void RemoveExpiredCookie ()
	public abstract void RemoveSessionCookie ()
	public abstract void RemoveSessionCookies (IValueCallback callback)
	public abstract void SetAcceptCookie (bool accept)
	public abstract void SetAcceptThirdPartyCookies (WebView webview, bool accept)
	public abstract void SetCookie (string url, string value)
	public abstract void SetCookie (string url, string value, IValueCallback callback)
```

### Type Changed: Android.Webkit.WebBackForwardList

Added constructor:

<pre style='color: green'>
	public WebBackForwardList ();
</pre>

Modified properties:

```
public abstract int CurrentIndex { get; }
	public abstract WebHistoryItem CurrentItem { get; }
	public abstract int Size { get; }
```

Modified methods:

```
public abstract WebHistoryItem GetItemAtIndex (int index)
```

Added method:

<pre style='color: green'>
	protected virtual WebBackForwardList Clone ();
</pre>

### Type Changed: Android.Webkit.WebHistoryItem

Added constructor:

<pre style='color: green'>
	public WebHistoryItem ();
</pre>

Modified properties:

```
public abstract Android.Graphics.Bitmap Favicon { get; }
	public abstract string OriginalUrl { get; }
	public abstract string Title { get; }
	public abstract string Url { get; }
```

Added method:

<pre style='color: green'>
	protected virtual WebHistoryItem Clone ();
</pre>

### Type Changed: Android.Webkit.WebIconDatabase

Added constructor:

<pre style='color: green'>
	public WebIconDatabase ();
</pre>

Modified methods:

```
public abstract void Close ()
	public abstract void Open (string path)
	public abstract void ReleaseIconForPageUrl (string url)
	public abstract void RemoveAllIcons ()
	public abstract void RequestIconForPageUrl (string url, WebIconDatabase.IIconListener listener)
	public abstract void RetainIconForPageUrl (string url)
```

### Type Changed: Android.Webkit.WebSettings

Added constructor:

<pre style='color: green'>
	public WebSettings ();
</pre>

Modified properties:

```
public abstract bool AllowContentAccess { get; set; }
	public abstract bool AllowFileAccess { get; set; }
	public abstract bool BlockNetworkImage { get; set; }
	public abstract bool BlockNetworkLoads { get; set; }
	public abstract bool BuiltInZoomControls { get; set; }
	public abstract CacheModes CacheMode { get; set; }
	public abstract string CursiveFontFamily { get; set; }
	public abstract bool DatabaseEnabled { get; set; }
	public abstract string DatabasePath { get; set; }
	public abstract int DefaultFixedFontSize { get; set; }
	public abstract int DefaultFontSize { get; set; }
	public abstract string DefaultTextEncodingName { get; set; }
	public abstract WebSettings.ZoomDensity DefaultZoom { get; set; }
	public abstract bool DisplayZoomControls { get; set; }
	public abstract bool DomStorageEnabled { get; set; }
	public abstract string FantasyFontFamily { get; set; }
	public abstract string FixedFontFamily { get; set; }
	public abstract bool JavaScriptCanOpenWindowsAutomatically { get; set; }
	public abstract bool JavaScriptEnabled { get; set; }
	public abstract bool LightTouchEnabled { get; set; }
	public abstract bool LoadsImagesAutomatically { get; set; }
	public abstract bool LoadWithOverviewMode { get; set; }
	public abstract bool MediaPlaybackRequiresUserGesture { get; set; }
	public abstract int MinimumFontSize { get; set; }
	public abstract int MinimumLogicalFontSize { get; set; }
	public abstract string SansSerifFontFamily { get; set; }
	public abstract bool SaveFormData { get; set; }
	public abstract bool SavePassword { get; set; }
	public abstract string SerifFontFamily { get; set; }
	public abstract string StandardFontFamily { get; set; }
	public abstract int TextZoom { get; set; }
	public abstract string UserAgentString { get; set; }
	public abstract bool UseWideViewPort { get; set; }
```

Modified methods:

```
public abstract bool EnableSmoothTransition ()
	public abstract WebSettings.LayoutAlgorithm GetLayoutAlgorithm ()
	public abstract WebSettings.PluginState GetPluginState ()
	public abstract void SetAppCacheEnabled (bool flag)
	public abstract void SetAppCacheMaxSize (long appCacheMaxSize)
	public abstract void SetAppCachePath (string appCachePath)
	public abstract void SetEnableSmoothTransition (bool enable)
	public abstract void SetGeolocationDatabasePath (string databasePath)
	public abstract void SetGeolocationEnabled (bool flag)
	public abstract void SetLayoutAlgorithm (WebSettings.LayoutAlgorithm l)
	public abstract void SetNeedInitialFocus (bool flag)
	public abstract void SetPluginState (WebSettings.PluginState state)
	public abstract void SetRenderPriority (WebSettings.RenderPriority priority)
	public abstract void SetSupportMultipleWindows (bool support)
	public abstract void SetSupportZoom (bool support)
	public abstract bool SupportMultipleWindows ()
	public abstract bool SupportZoom ()
```

### Type Changed: Android.Webkit.WebViewDatabase

Added constructor:

<pre style='color: green'>
	public WebViewDatabase ();
</pre>

Modified properties:

```
public abstract bool HasFormData { get; }
	public abstract bool HasHttpAuthUsernamePassword { get; }
	public abstract bool HasUsernamePassword { get; }
```

Modified methods:

```
public abstract void ClearFormData ()
	public abstract void ClearHttpAuthUsernamePassword ()
	public abstract void ClearUsernamePassword ()
```

## Namespace Android.Widget

### Type Changed: Android.Widget.PopupMenu

Added constructor:

<pre style='color: green'>
	public PopupMenu (Android.Content.Context context, Android.Views.View anchor, Android.Views.GravityFlags gravity, int popupStyleAttr, int popupStyleRes);
</pre>

### Type Changed: Android.Widget.PopupWindow

Added property:

<pre style='color: green'>
	public virtual bool AttachedInDecor { get; set; }
</pre>

### Type Changed: Android.Widget.RemoteViews

Added methods:

<pre style='color: green'>
	public virtual void SetAccessibilityTraversalAfter (int viewId, int nextId);
	public virtual void SetAccessibilityTraversalBefore (int viewId, int nextId);
</pre>

## New Namespace Android.Service.Carrier

### New Type Android.Service.Carrier.CarrierMessagingService

<pre style='color: green'>
public abstract class CarrierMessagingService : Android.App.Service, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	protected CarrierMessagingService (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public CarrierMessagingService ();
	// fields
	public static const string ServiceInterface = "android.service.carrier.CarrierMessagingService";
	// properties
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public override Android.OS.IBinder OnBind (Android.Content.Intent intent);
	public virtual void OnDownloadMms (Android.Net.Uri contentUri, int subId, Android.Net.Uri location, CarrierMessagingService.IResultCallback callback);
	public virtual void OnFilterSms (MessagePdu pdu, string format, int destPort, int subId, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendDataSms (byte[] data, int subId, string destAddress, int destPort, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendMms (Android.Net.Uri pduUri, int subId, Android.Net.Uri location, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendMultipartTextSms (System.Collections.Generic.IList&lt;string&gt; parts, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);
	public virtual void OnSendTextSms (string text, int subId, string destAddress, CarrierMessagingService.IResultCallback callback);

	// inner types
	public interface IResultCallback : Android.Runtime.IJavaObject, System.IDisposable {
		// methods
		public virtual void OnReceiveResult (Java.Lang.Object result);
	}
	public sealed class SendMmsResult : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public CarrierMessagingService (MessageSendStatus sendStatus, byte[] sendConfPdu);
		// properties
		public MessageSendStatus SendStatus { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public byte[] GetSendConfPdu ();
	}
	public sealed class SendMultipartSmsResult : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public CarrierMessagingService (MessageSendStatus sendStatus, int[] messageRefs);
		// properties
		public MessageSendStatus SendStatus { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
		// methods
		public int[] GetMessageRefs ();
	}
	public sealed class SendSmsResult : Java.Lang.Object, System.IDisposable, Android.Runtime.IJavaObject {
		// constructors
		public CarrierMessagingService (MessageSendStatus sendStatus, int messageRef);
		// properties
		public int MessageRef { get; }
		public MessageSendStatus SendStatus { get; }
		protected override IntPtr ThresholdClass { get; }
		protected override System.Type ThresholdType { get; }
	}
}
</pre>

### New Type Android.Service.Carrier.MessageDownloadStatus

<pre style='color: green'>
[Serializable]
public enum MessageDownloadStatus {
	Error = 2,
	Ok = 0,
	RetryOnCarrierNetwork = 1,
}
</pre>

### New Type Android.Service.Carrier.MessagePdu

<pre style='color: green'>
public sealed class MessagePdu : Java.Lang.Object, Android.OS.IParcelable, Android.Runtime.IJavaObject, System.IDisposable {
	// constructors
	public MessagePdu (System.Collections.Generic.IList&lt;System.Byte[]&gt; pduList);
	// properties
	public static Android.OS.IParcelableCreator Creator { get; }
	public System.Collections.Generic.IList&lt;System.Byte[]&gt; Pdus { get; }
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
	// methods
	public virtual int DescribeContents ();
	public virtual void WriteToParcel (Android.OS.Parcel dest, Android.OS.ParcelableWriteFlags flags);

	// inner types
	public static class InterfaceConsts {
		// fields
		public static const int ContentsFileDescriptor;

		[Obsolete]
		public static const Android.OS.ParcelableWriteFlags ParcelableWriteReturnValue;
	}
}
</pre>

### New Type Android.Service.Carrier.MessageSendStatus

<pre style='color: green'>
[Serializable]
public enum MessageSendStatus {
	Error = 2,
	Ok = 0,
	RetryOnCarrierNetwork = 1,
}
</pre>
