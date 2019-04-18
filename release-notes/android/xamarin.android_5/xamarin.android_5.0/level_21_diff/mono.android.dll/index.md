---
id: 317EC8AF-A49D-484D-8E66-F3BA470D1D59
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android

### New Type Android.LinkerSafeAttribute

```
public sealed class LinkerSafeAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public LinkerSafeAttribute ();
}
```

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Accounts

### Type Changed: Android.Accounts.Account

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Accounts.AccountAuthenticatorResponse

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Accounts.AccountManager

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual IAccountManagerFuture GetAuthToken (Account account, string authTokenType, bool notifyAuthFailure, IAccountManagerCallback callback, Android.OS.Handler handler);
```

### Type Changed: Android.Accounts.AuthenticatorDescription

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Animation

### Type Changed: Android.Animation.LayoutTransition

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void HideChild (Android.Views.ViewGroup parent, Android.Views.View child);

	[Obsolete ("deprecated")]
	public virtual void ShowChild (Android.Views.ViewGroup parent, Android.Views.View child);
```

## Namespace Android.App

### Type Changed: Android.App.Activity

Removed property:

```
protected static System.Collections.Generic.IList<int> FocusedStateSet { get; set; }
```

Added property:

```
protected static System.Collections.Generic.IList<int> FocusedStateSet { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public void DismissDialog (int id);

	[Obsolete ("deprecated")]
	public Android.Database.ICursor ManagedQuery (Android.Net.Uri uri, string[] projection, string selection, string[] selectionArgs, string sortOrder);

	[Obsolete ("deprecated")]
	protected virtual Dialog OnCreateDialog (int id);

	[Obsolete ("deprecated")]
	protected virtual Dialog OnCreateDialog (int id, Android.OS.Bundle args);

	[Obsolete ("deprecated")]
	protected virtual void OnPrepareDialog (int id, Dialog dialog);

	[Obsolete ("deprecated")]
	protected virtual void OnPrepareDialog (int id, Dialog dialog, Android.OS.Bundle args);

	[Obsolete ("deprecated")]
	public virtual Java.Lang.Object OnRetainNonConfigurationInstance ();

	[Obsolete ("deprecated")]
	public void RemoveDialog (int id);

	[Obsolete ("deprecated")]
	public virtual void SetPersistent (bool isPersistent);

	[Obsolete ("deprecated")]
	public void ShowDialog (int id);

	[Obsolete ("deprecated")]
	public bool ShowDialog (int id, Android.OS.Bundle args);

	[Obsolete ("deprecated")]
	public virtual void StartManagingCursor (Android.Database.ICursor c);

	[Obsolete ("deprecated")]
	public virtual void StopManagingCursor (Android.Database.ICursor c);
```

### Type Changed: Android.App.ActivityAttribute

Added property:

```
public bool Immersive { get; set; }
```

### Type Changed: Android.App.ActivityManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.IList<ActivityManager.RecentTaskInfo> GetRecentTasks (int maxNum, RecentTaskFlags flags);

	[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.IList<ActivityManager.RunningTaskInfo> GetRunningTasks (int maxNum);

	[Obsolete ("deprecated")]
	public virtual void RestartPackage (string packageName);
```

### Type Changed: Android.App.ActivityManager.MemoryInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.ProcessErrorStateInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.RecentTaskInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.RunningAppProcessInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.RunningServiceInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.RunningTaskInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.ActivityManager.TaskDescription

Removed properties:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual int PrimaryColor { get; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public virtual Android.Graphics.Color PrimaryColor { get; }
```

### Type Changed: Android.App.AlarmManager

### Type Changed: Android.App.AlarmManager.AlarmClockInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.AlertDialog

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetButton (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);

	[Obsolete ("deprecated")]
	public virtual void SetButton (Java.Lang.ICharSequence text, Android.OS.Message msg);

	[Obsolete ("deprecated")]
	public virtual void SetButton2 (Java.Lang.ICharSequence text, Android.OS.Message msg);

	[Obsolete ("deprecated")]
	public virtual void SetButton2 (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);

	[Obsolete ("deprecated")]
	public virtual void SetButton3 (Java.Lang.ICharSequence text, Android.OS.Message msg);

	[Obsolete ("deprecated")]
	public virtual void SetButton3 (Java.Lang.ICharSequence text, Android.Content.IDialogInterfaceOnClickListener listener);
```

### Type Changed: Android.App.ApplicationErrorReport

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.DownloadManager

### Type Changed: Android.App.DownloadManager.Request

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual DownloadManager.Request SetShowRunningNotification (bool show);
```

### Type Changed: Android.App.Fragment

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void OnInflate (Android.Util.IAttributeSet attrs, Android.OS.Bundle savedInstanceState);
```

### Type Changed: Android.App.Fragment.SavedState

Removed property:

```
public static Android.OS.IParcelableClassLoaderCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableClassLoaderCreator Creator { get; }
```

### Type Changed: Android.App.KeyguardManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void ExitKeyguardSecurely (KeyguardManager.IOnKeyguardExitResult callback);

	[Obsolete ("deprecated")]
	public virtual KeyguardManager.KeyguardLock NewKeyguardLock (string tag);
```

### Type Changed: Android.App.MediaRouteActionProvider

Obsoleted method:

```
[Obsolete ("deprecated")]
	public override Android.Views.View OnCreateActionView ();
```

### Type Changed: Android.App.Notification

Removed properties:

```
public static Android.Media.AudioAttributes AudioAttributesDefault { get; set; }
	public int Color { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public static Android.Media.AudioAttributes AudioAttributesDefault { get; }
	public Android.Graphics.Color Color { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetLatestEventInfo (Android.Content.Context context, Java.Lang.ICharSequence contentTitle, Java.Lang.ICharSequence contentText, PendingIntent contentIntent);
```

### Type Changed: Android.App.Notification.Action

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.Notification.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Notification.Builder SetSound (Android.Net.Uri sound, Android.Media.Stream streamType);

	[Obsolete ("deprecated")]
	public virtual Notification.Builder SetTicker (Java.Lang.ICharSequence tickerText, Android.Widget.RemoteViews views);
```

### Type Changed: Android.App.PendingIntent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.RemoteInput

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.SearchableInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.SearchManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnCancel (Android.Content.IDialogInterface dialog);

	[Obsolete ("deprecated")]
	public virtual void OnDismiss (Android.Content.IDialogInterface dialog);
```

### Type Changed: Android.App.Service

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnStart (Android.Content.Intent intent, int startId);

	[Obsolete ("deprecated")]
	public virtual StartCommandResult OnStartCommand (Android.Content.Intent intent, StartCommandFlags flags, int startId);

	[Obsolete ("deprecated")]
	public void SetForeground (bool isForeground);
```

### Type Changed: Android.App.WallpaperInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.DeviceAdminInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.App.Job

### Type Changed: Android.App.Job.JobInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.Job.JobParameters

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.App.Usage

### Type Changed: Android.App.Usage.ConfigurationStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.Usage.UsageEvents

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.App.Usage.UsageStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Appwidget

### Type Changed: Android.Appwidget.AppWidgetProviderInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothAdapter

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public bool Disable ();

	[Obsolete ("deprecated")]
	public bool Enable ();

	[Obsolete ("deprecated")]
	public bool StartLeScan (BluetoothAdapter.ILeScanCallback callback);

	[Obsolete ("deprecated")]
	public bool StartLeScan (Java.Util.UUID[] serviceUuids, BluetoothAdapter.ILeScanCallback callback);

	[Obsolete ("deprecated")]
	public void StopLeScan (BluetoothAdapter.ILeScanCallback callback);
```

### Type Changed: Android.Bluetooth.BluetoothClass

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.BluetoothDevice

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.BluetoothGatt

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void AbortReliableWrite (BluetoothDevice mDevice);
```

### Type Changed: Android.Bluetooth.BluetoothGattDescriptor

Removed properties:

```
public static System.Collections.Generic.IList<byte> DisableNotificationValue { get; set; }
	public static System.Collections.Generic.IList<byte> EnableIndicationValue { get; set; }
	public static System.Collections.Generic.IList<byte> EnableNotificationValue { get; set; }
```

Added properties:

```
public static System.Collections.Generic.IList<byte> DisableNotificationValue { get; }
	public static System.Collections.Generic.IList<byte> EnableIndicationValue { get; }
	public static System.Collections.Generic.IList<byte> EnableNotificationValue { get; }
```

### Type Changed: Android.Bluetooth.BluetoothHealthAppConfiguration

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Bluetooth.LE

### Type Changed: Android.Bluetooth.LE.AdvertiseData

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.LE.AdvertiseSettings

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.LE.ScanFilter

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.LE.ScanResult

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Bluetooth.LE.ScanSettings

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Content

### Type Changed: Android.Content.ClipData

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ClipDescription

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ComponentName

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ContentProviderOperation

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ContentProviderResult

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ContentResolver

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void CancelSync (Android.Net.Uri uri);

	[Obsolete ("deprecated")]
	public virtual void StartSync (Android.Net.Uri uri, Android.OS.Bundle extras);
```

### Type Changed: Android.Content.ContentValues

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.ContextWrapper

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override void ClearWallpaper ();

	[Obsolete ("deprecated")]
	public override Android.Graphics.Drawables.Drawable PeekWallpaper ();

	[Obsolete ("deprecated")]
	public override void RemoveStickyBroadcast (Intent intent);

	[Obsolete ("deprecated")]
	public override void RemoveStickyBroadcastAsUser (Intent intent, Android.OS.UserHandle user);

	[Obsolete ("deprecated")]
	public override void SendStickyBroadcast (Intent intent);

	[Obsolete ("deprecated")]
	public override void SendStickyBroadcastAsUser (Intent intent, Android.OS.UserHandle user);

	[Obsolete ("deprecated")]
	public override void SendStickyOrderedBroadcast (Intent intent, BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);

	[Obsolete ("deprecated")]
	public override void SendStickyOrderedBroadcastAsUser (Intent intent, Android.OS.UserHandle user, BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);

	[Obsolete ("deprecated")]
	public override void SetWallpaper (Android.Graphics.Bitmap bitmap);

	[Obsolete ("deprecated")]
	public override void SetWallpaper (System.IO.Stream data);
```

### Type Changed: Android.Content.Intent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static Intent GetIntent (string uri);

	[Obsolete ("deprecated")]
	public virtual string ToURI ();
```

### Type Changed: Android.Content.Intent.ShortcutIconResource

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.IntentFilter

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.IntentSender

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PeriodicSync

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.RestrictionEntry

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.SyncAdapterType

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.SyncRequest

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.SyncResult

Removed properties:

```
public static SyncResult AlreadyInProgress { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public static SyncResult AlreadyInProgress { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.SyncStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.UriPermission

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ActivityInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.ApplicationInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.ConfigurationInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.FeatureGroupInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.FeatureInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.InstrumentationInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.LabeledIntent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PackageInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PackageInstaller

### Type Changed: Android.Content.PM.PackageInstaller.SessionInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PackageInstaller.SessionParams

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PackageStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PathPermission

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PermissionGroupInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.PermissionInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.ProviderInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.ResolveInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.ServiceInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.PM.Signature

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.AssetFileDescriptor

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.Res.ColorStateList

Removed properties:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
	public virtual int DefaultColor { get; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public virtual Android.Graphics.Color DefaultColor { get; }
```

Removed method:

```
public virtual int GetColorForState (int[] stateSet, Android.Graphics.Color defaultColor);
```

Added method:

```
public virtual Android.Graphics.Color GetColorForState (int[] stateSet, Android.Graphics.Color defaultColor);
```

### Type Changed: Android.Content.Res.Configuration

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Content.Res.ObbInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Database

### Type Changed: Android.Database.AbstractCursor

Obsoleted methods:

```
[Obsolete ("deprecated")]
	protected virtual Java.Lang.Object GetUpdatedField (int columnIndex);

	[Obsolete ("deprecated")]
	protected virtual bool IsFieldUpdated (int columnIndex);
```

### Type Changed: Android.Database.AbstractWindowedCursor

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool IsBlob (int columnIndex);

	[Obsolete ("deprecated")]
	public virtual bool IsFloat (int columnIndex);

	[Obsolete ("deprecated")]
	public virtual bool IsLong (int columnIndex);

	[Obsolete ("deprecated")]
	public virtual bool IsString (int columnIndex);
```

### Type Changed: Android.Database.ContentObservable

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void DispatchChange (bool selfChange);

	[Obsolete ("deprecated")]
	public virtual void NotifyChange (bool selfChange);
```

### Type Changed: Android.Database.ContentObserver

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void DispatchChange (bool selfChange);
```

### Type Changed: Android.Database.CursorJoiner

### Type Changed: Android.Database.CursorJoiner.Result

Removed properties:

```
public static CursorJoiner.Result Both { get; set; }
	public static CursorJoiner.Result Left { get; set; }
	public static CursorJoiner.Result Right { get; set; }
```

Added properties:

```
public static CursorJoiner.Result Both { get; }
	public static CursorJoiner.Result Left { get; }
	public static CursorJoiner.Result Right { get; }
```

### Type Changed: Android.Database.CursorWindow

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool IsBlob (int row, int column);

	[Obsolete ("deprecated")]
	public virtual bool IsFloat (int row, int column);

	[Obsolete ("deprecated")]
	public virtual bool IsLong (int row, int column);

	[Obsolete ("deprecated")]
	public virtual bool IsNull (int row, int column);

	[Obsolete ("deprecated")]
	public virtual bool IsString (int row, int column);
```

## Namespace Android.Database.Sqlite

### Type Changed: Android.Database.Sqlite.SQLiteClosable

Obsoleted methods:

```
[Obsolete ("deprecated")]
	protected virtual void OnAllReferencesReleasedFromContainer ();

	[Obsolete ("deprecated")]
	public virtual void ReleaseReferenceFromContainer ();
```

### Type Changed: Android.Database.Sqlite.SQLiteDatabase

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void MarkTableSyncable (string table, string foreignKey, string updateTable);

	[Obsolete ("deprecated")]
	public virtual void MarkTableSyncable (string table, string deletedTable);

	[Obsolete ("deprecated")]
	public virtual void SetLockingEnabled (bool lockingEnabled);

	[Obsolete ("deprecated")]
	public virtual bool YieldIfContended ();
```

### Type Changed: Android.Database.Sqlite.SQLiteProgram

Obsoleted methods:

```
[Obsolete ("deprecated")]
	protected virtual void Compile (string sql, bool forceCompilation);

	[Obsolete ("deprecated")]
	protected void Native_compile (string sql);

	[Obsolete ("deprecated")]
	protected void Native_finalize ();
```

### Type Changed: Android.Database.Sqlite.SQLiteQueryBuilder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual string BuildQuery (string[] projectionIn, string selection, string[] selectionArgs, string groupBy, string having, string sortOrder, string limit);

	[Obsolete ("deprecated")]
	public virtual string BuildUnionSubQuery (string typeDiscriminatorColumn, string[] unionColumns, System.Collections.Generic.ICollection<string> columnsPresentInTable, int computedColumnsOffset, string typeDiscriminatorValue, string selection, string[] selectionArgs, string groupBy, string having);
```

## Namespace Android.Gestures

### Type Changed: Android.Gestures.Gesture

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Graphics

### Type Changed: Android.Graphics.AvoidXfermode

### Type Changed: Android.Graphics.AvoidXfermode.Mode

Removed properties:

```
public static AvoidXfermode.Mode Avoid { get; set; }
	public static AvoidXfermode.Mode Target { get; set; }
```

Added properties:

```
public static AvoidXfermode.Mode Avoid { get; }
	public static AvoidXfermode.Mode Target { get; }
```

### Type Changed: Android.Graphics.Bitmap

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public bool IsPremultiplied { get; }
```

Obsoleted property:

```
[Obsolete ("Use the IsPremultiplied property getter or the SetPremultiplied(bool) method.")]
	public bool Premultiplied { get; set; }
```

Added method:

```
public void SetPremultiplied (bool premultiplied);
```

### Type Changed: Android.Graphics.Bitmap.CompressFormat

Removed properties:

```
public static Bitmap.CompressFormat Jpeg { get; set; }
	public static Bitmap.CompressFormat Png { get; set; }
	public static Bitmap.CompressFormat Webp { get; set; }
```

Added properties:

```
public static Bitmap.CompressFormat Jpeg { get; }
	public static Bitmap.CompressFormat Png { get; }
	public static Bitmap.CompressFormat Webp { get; }
```

### Type Changed: Android.Graphics.Bitmap.Config

Removed properties:

```
public static Bitmap.Config Alpha8 { get; set; }
	public static Bitmap.Config Argb4444 { get; set; }
	public static Bitmap.Config Argb8888 { get; set; }
	public static Bitmap.Config Rgb565 { get; set; }
```

Added properties:

```
public static Bitmap.Config Alpha8 { get; }
	public static Bitmap.Config Argb4444 { get; }
	public static Bitmap.Config Argb8888 { get; }
	public static Bitmap.Config Rgb565 { get; }
```

### Type Changed: Android.Graphics.BlurMaskFilter

### Type Changed: Android.Graphics.BlurMaskFilter.Blur

Removed properties:

```
public static BlurMaskFilter.Blur Inner { get; set; }
	public static BlurMaskFilter.Blur Normal { get; set; }
	public static BlurMaskFilter.Blur Outer { get; set; }
	public static BlurMaskFilter.Blur Solid { get; set; }
```

Added properties:

```
public static BlurMaskFilter.Blur Inner { get; }
	public static BlurMaskFilter.Blur Normal { get; }
	public static BlurMaskFilter.Blur Outer { get; }
	public static BlurMaskFilter.Blur Solid { get; }
```

### Type Changed: Android.Graphics.Canvas

Obsoleted constructor:

```
[Obsolete ("This method does not exist in API-11+.")]
	public Canvas (Javax.Microedition.Khronos.Opengles.IGL gl);
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool ClipRegion (Region region);

	[Obsolete ("deprecated")]
	public virtual bool ClipRegion (Region region, Region.Op op);

	[Obsolete ("deprecated")]
	public virtual void DrawBitmap (int[] colors, int offset, int stride, int x, int y, int width, int height, bool hasAlpha, Paint paint);

	[Obsolete ("deprecated")]
	public virtual void DrawBitmap (int[] colors, int offset, int stride, float x, float y, int width, int height, bool hasAlpha, Paint paint);

	[Obsolete ("deprecated")]
	public virtual void DrawPosText (string text, float[] pos, Paint paint);

	[Obsolete ("deprecated")]
	public virtual void DrawPosText (char[] text, int index, int count, float[] pos, Paint paint);

	[Obsolete ("deprecated")]
	public virtual void GetMatrix (Matrix ctm);
```

### Type Changed: Android.Graphics.Canvas.EdgeType

Removed properties:

```
public static Canvas.EdgeType Aa { get; set; }
	public static Canvas.EdgeType Bw { get; set; }
```

Added properties:

```
public static Canvas.EdgeType Aa { get; }
	public static Canvas.EdgeType Bw { get; }
```

### Type Changed: Android.Graphics.Canvas.VertexMode

Removed properties:

```
public static Canvas.VertexMode TriangleFan { get; set; }
	public static Canvas.VertexMode Triangles { get; set; }
	public static Canvas.VertexMode TriangleStrip { get; set; }
```

Added properties:

```
public static Canvas.VertexMode TriangleFan { get; }
	public static Canvas.VertexMode Triangles { get; }
	public static Canvas.VertexMode TriangleStrip { get; }
```

### Type Changed: Android.Graphics.Interpolator

### Type Changed: Android.Graphics.Interpolator.Result

Removed properties:

```
public static Interpolator.Result FreezeEnd { get; set; }
	public static Interpolator.Result FreezeStart { get; set; }
	public static Interpolator.Result Normal { get; set; }
```

Added properties:

```
public static Interpolator.Result FreezeEnd { get; }
	public static Interpolator.Result FreezeStart { get; }
	public static Interpolator.Result Normal { get; }
```

### Type Changed: Android.Graphics.Matrix

### Type Changed: Android.Graphics.Matrix.ScaleToFit

Removed properties:

```
public static Matrix.ScaleToFit Center { get; set; }
	public static Matrix.ScaleToFit End { get; set; }
	public static Matrix.ScaleToFit Fill { get; set; }
	public static Matrix.ScaleToFit Start { get; set; }
```

Added properties:

```
public static Matrix.ScaleToFit Center { get; }
	public static Matrix.ScaleToFit End { get; }
	public static Matrix.ScaleToFit Fill { get; }
	public static Matrix.ScaleToFit Start { get; }
```

### Type Changed: Android.Graphics.Paint

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual Rasterizer SetRasterizer (Rasterizer rasterizer);
```

### Type Changed: Android.Graphics.Paint.Align

Removed properties:

```
public static Paint.Align Center { get; set; }
	public static Paint.Align Left { get; set; }
	public static Paint.Align Right { get; set; }
```

Added properties:

```
public static Paint.Align Center { get; }
	public static Paint.Align Left { get; }
	public static Paint.Align Right { get; }
```

### Type Changed: Android.Graphics.Paint.Cap

Removed properties:

```
public static Paint.Cap Butt { get; set; }
	public static Paint.Cap Round { get; set; }
	public static Paint.Cap Square { get; set; }
```

Added properties:

```
public static Paint.Cap Butt { get; }
	public static Paint.Cap Round { get; }
	public static Paint.Cap Square { get; }
```

### Type Changed: Android.Graphics.Paint.Join

Removed properties:

```
public static Paint.Join Bevel { get; set; }
	public static Paint.Join Miter { get; set; }
	public static Paint.Join Round { get; set; }
```

Added properties:

```
public static Paint.Join Bevel { get; }
	public static Paint.Join Miter { get; }
	public static Paint.Join Round { get; }
```

### Type Changed: Android.Graphics.Paint.Style

Removed properties:

```
public static Paint.Style Fill { get; set; }
	public static Paint.Style FillAndStroke { get; set; }
	public static Paint.Style Stroke { get; set; }
```

Added properties:

```
public static Paint.Style Fill { get; }
	public static Paint.Style FillAndStroke { get; }
	public static Paint.Style Stroke { get; }
```

### Type Changed: Android.Graphics.Path

### Type Changed: Android.Graphics.Path.Direction

Removed properties:

```
public static Path.Direction Ccw { get; set; }
	public static Path.Direction Cw { get; set; }
```

Added properties:

```
public static Path.Direction Ccw { get; }
	public static Path.Direction Cw { get; }
```

### Type Changed: Android.Graphics.Path.FillType

Removed properties:

```
public static Path.FillType EvenOdd { get; set; }
	public static Path.FillType InverseEvenOdd { get; set; }
	public static Path.FillType InverseWinding { get; set; }
	public static Path.FillType Winding { get; set; }
```

Added properties:

```
public static Path.FillType EvenOdd { get; }
	public static Path.FillType InverseEvenOdd { get; }
	public static Path.FillType InverseWinding { get; }
	public static Path.FillType Winding { get; }
```

### Type Changed: Android.Graphics.Path.Op

Removed properties:

```
public static Path.Op Difference { get; set; }
	public static Path.Op Intersect { get; set; }
	public static Path.Op ReverseDifference { get; set; }
	public static Path.Op Union { get; set; }
	public static Path.Op Xor { get; set; }
```

Added properties:

```
public static Path.Op Difference { get; }
	public static Path.Op Intersect { get; }
	public static Path.Op ReverseDifference { get; }
	public static Path.Op Union { get; }
	public static Path.Op Xor { get; }
```

### Type Changed: Android.Graphics.PathDashPathEffect

### Type Changed: Android.Graphics.PathDashPathEffect.Style

Removed properties:

```
public static PathDashPathEffect.Style Morph { get; set; }
	public static PathDashPathEffect.Style Rotate { get; set; }
	public static PathDashPathEffect.Style Translate { get; set; }
```

Added properties:

```
public static PathDashPathEffect.Style Morph { get; }
	public static PathDashPathEffect.Style Rotate { get; }
	public static PathDashPathEffect.Style Translate { get; }
```

### Type Changed: Android.Graphics.Picture

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static Picture CreateFromStream (System.IO.Stream stream);

	[Obsolete ("deprecated")]
	public virtual void WriteToStream (System.IO.Stream stream);
```

### Type Changed: Android.Graphics.Point

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.PointF

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.PorterDuff

### Type Changed: Android.Graphics.PorterDuff.Mode

Removed properties:

```
public static PorterDuff.Mode Add { get; set; }
	public static PorterDuff.Mode Clear { get; set; }
	public static PorterDuff.Mode Darken { get; set; }
	public static PorterDuff.Mode Dst { get; set; }
	public static PorterDuff.Mode DstAtop { get; set; }
	public static PorterDuff.Mode DstIn { get; set; }
	public static PorterDuff.Mode DstOut { get; set; }
	public static PorterDuff.Mode DstOver { get; set; }
	public static PorterDuff.Mode Lighten { get; set; }
	public static PorterDuff.Mode Multiply { get; set; }
	public static PorterDuff.Mode Overlay { get; set; }
	public static PorterDuff.Mode Screen { get; set; }
	public static PorterDuff.Mode Src { get; set; }
	public static PorterDuff.Mode SrcAtop { get; set; }
	public static PorterDuff.Mode SrcIn { get; set; }
	public static PorterDuff.Mode SrcOut { get; set; }
	public static PorterDuff.Mode SrcOver { get; set; }
	public static PorterDuff.Mode Xor { get; set; }
```

Added properties:

```
public static PorterDuff.Mode Add { get; }
	public static PorterDuff.Mode Clear { get; }
	public static PorterDuff.Mode Darken { get; }
	public static PorterDuff.Mode Dst { get; }
	public static PorterDuff.Mode DstAtop { get; }
	public static PorterDuff.Mode DstIn { get; }
	public static PorterDuff.Mode DstOut { get; }
	public static PorterDuff.Mode DstOver { get; }
	public static PorterDuff.Mode Lighten { get; }
	public static PorterDuff.Mode Multiply { get; }
	public static PorterDuff.Mode Overlay { get; }
	public static PorterDuff.Mode Screen { get; }
	public static PorterDuff.Mode Src { get; }
	public static PorterDuff.Mode SrcAtop { get; }
	public static PorterDuff.Mode SrcIn { get; }
	public static PorterDuff.Mode SrcOut { get; }
	public static PorterDuff.Mode SrcOver { get; }
	public static PorterDuff.Mode Xor { get; }
```

### Type Changed: Android.Graphics.Rect

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.RectF

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.Region

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Graphics.Region.Op

Removed properties:

```
public static Region.Op Difference { get; set; }
	public static Region.Op Intersect { get; set; }
	public static Region.Op Replace { get; set; }
	public static Region.Op ReverseDifference { get; set; }
	public static Region.Op Union { get; set; }
	public static Region.Op Xor { get; set; }
```

Added properties:

```
public static Region.Op Difference { get; }
	public static Region.Op Intersect { get; }
	public static Region.Op Replace { get; }
	public static Region.Op ReverseDifference { get; }
	public static Region.Op Union { get; }
	public static Region.Op Xor { get; }
```

### Type Changed: Android.Graphics.Shader

### Type Changed: Android.Graphics.Shader.TileMode

Removed properties:

```
public static Shader.TileMode Clamp { get; set; }
	public static Shader.TileMode Mirror { get; set; }
	public static Shader.TileMode Repeat { get; set; }
```

Added properties:

```
public static Shader.TileMode Clamp { get; }
	public static Shader.TileMode Mirror { get; }
	public static Shader.TileMode Repeat { get; }
```

### Type Changed: Android.Graphics.Typeface

Removed properties:

```
public static Typeface Default { get; set; }
	public static Typeface DefaultBold { get; set; }
	public static Typeface Monospace { get; set; }
	public static Typeface SansSerif { get; set; }
	public static Typeface Serif { get; set; }
```

Added properties:

```
public static Typeface Default { get; }
	public static Typeface DefaultBold { get; }
	public static Typeface Monospace { get; }
	public static Typeface SansSerif { get; }
	public static Typeface Serif { get; }
```

## Namespace Android.Graphics.Drawables

### Type Changed: Android.Graphics.Drawables.GradientDrawable

### Type Changed: Android.Graphics.Drawables.GradientDrawable.Orientation

Removed properties:

```
public static GradientDrawable.Orientation BlTr { get; set; }
	public static GradientDrawable.Orientation BottomTop { get; set; }
	public static GradientDrawable.Orientation BrTl { get; set; }
	public static GradientDrawable.Orientation LeftRight { get; set; }
	public static GradientDrawable.Orientation RightLeft { get; set; }
	public static GradientDrawable.Orientation TlBr { get; set; }
	public static GradientDrawable.Orientation TopBottom { get; set; }
	public static GradientDrawable.Orientation TrBl { get; set; }
```

Added properties:

```
public static GradientDrawable.Orientation BlTr { get; }
	public static GradientDrawable.Orientation BottomTop { get; }
	public static GradientDrawable.Orientation BrTl { get; }
	public static GradientDrawable.Orientation LeftRight { get; }
	public static GradientDrawable.Orientation RightLeft { get; }
	public static GradientDrawable.Orientation TlBr { get; }
	public static GradientDrawable.Orientation TopBottom { get; }
	public static GradientDrawable.Orientation TrBl { get; }
```

## Namespace Android.Hardware

### Type Changed: Android.Hardware.Camera

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static Camera Open (int cameraId);
```

### Type Changed: Android.Hardware.SensorManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool RegisterListener (ISensorListener listener, int sensors, SensorDelay rate);

	[Obsolete ("deprecated")]
	public virtual bool RegisterListener (ISensorListener listener, int sensors);

	[Obsolete ("deprecated")]
	public virtual void UnregisterListener (ISensorListener listener);

	[Obsolete ("deprecated")]
	public virtual void UnregisterListener (ISensorListener listener, int sensors);
```

## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.CameraCharacteristics

Removed properties:

```
public static CameraCharacteristics.Key ColorCorrectionAvailableAberrationModes { get; set; }
	public static CameraCharacteristics.Key ControlAeAvailableAntibandingModes { get; set; }
	public static CameraCharacteristics.Key ControlAeAvailableModes { get; set; }
	public static CameraCharacteristics.Key ControlAeAvailableTargetFpsRanges { get; set; }
	public static CameraCharacteristics.Key ControlAeCompensationRange { get; set; }
	public static CameraCharacteristics.Key ControlAeCompensationStep { get; set; }
	public static CameraCharacteristics.Key ControlAfAvailableModes { get; set; }
	public static CameraCharacteristics.Key ControlAvailableEffects { get; set; }
	public static CameraCharacteristics.Key ControlAvailableSceneModes { get; set; }
	public static CameraCharacteristics.Key ControlAvailableVideoStabilizationModes { get; set; }
	public static CameraCharacteristics.Key ControlAwbAvailableModes { get; set; }
	public static CameraCharacteristics.Key ControlMaxRegionsAe { get; set; }
	public static CameraCharacteristics.Key ControlMaxRegionsAf { get; set; }
	public static CameraCharacteristics.Key ControlMaxRegionsAwb { get; set; }
	public static CameraCharacteristics.Key EdgeAvailableEdgeModes { get; set; }
	public static CameraCharacteristics.Key FlashInfoAvailable { get; set; }
	public static CameraCharacteristics.Key HotPixelAvailableHotPixelModes { get; set; }
	public static CameraCharacteristics.Key InfoSupportedHardwareLevel { get; set; }
	public static CameraCharacteristics.Key JpegAvailableThumbnailSizes { get; set; }
	public static CameraCharacteristics.Key LensFacing { get; set; }
	public static CameraCharacteristics.Key LensInfoAvailableApertures { get; set; }
	public static CameraCharacteristics.Key LensInfoAvailableFilterDensities { get; set; }
	public static CameraCharacteristics.Key LensInfoAvailableFocalLengths { get; set; }
	public static CameraCharacteristics.Key LensInfoAvailableOpticalStabilization { get; set; }
	public static CameraCharacteristics.Key LensInfoFocusDistanceCalibration { get; set; }
	public static CameraCharacteristics.Key LensInfoHyperfocalDistance { get; set; }
	public static CameraCharacteristics.Key LensInfoMinimumFocusDistance { get; set; }
	public static CameraCharacteristics.Key NoiseReductionAvailableNoiseReductionModes { get; set; }
	public static CameraCharacteristics.Key RequestAvailableCapabilities { get; set; }
	public static CameraCharacteristics.Key RequestMaxNumOutputProc { get; set; }
	public static CameraCharacteristics.Key RequestMaxNumOutputProcStalling { get; set; }
	public static CameraCharacteristics.Key RequestMaxNumOutputRaw { get; set; }
	public static CameraCharacteristics.Key RequestPartialResultCount { get; set; }
	public static CameraCharacteristics.Key RequestPipelineMaxDepth { get; set; }
	public static CameraCharacteristics.Key ScalerAvailableMaxDigitalZoom { get; set; }
	public static CameraCharacteristics.Key ScalerCroppingType { get; set; }
	public static CameraCharacteristics.Key ScalerStreamConfigurationMap { get; set; }
	public static CameraCharacteristics.Key SensorAvailableTestPatternModes { get; set; }
	public static CameraCharacteristics.Key SensorBlackLevelPattern { get; set; }
	public static CameraCharacteristics.Key SensorCalibrationTransform1 { get; set; }
	public static CameraCharacteristics.Key SensorCalibrationTransform2 { get; set; }
	public static CameraCharacteristics.Key SensorColorTransform1 { get; set; }
	public static CameraCharacteristics.Key SensorColorTransform2 { get; set; }
	public static CameraCharacteristics.Key SensorForwardMatrix1 { get; set; }
	public static CameraCharacteristics.Key SensorForwardMatrix2 { get; set; }
	public static CameraCharacteristics.Key SensorInfoActiveArraySize { get; set; }
	public static CameraCharacteristics.Key SensorInfoColorFilterArrangement { get; set; }
	public static CameraCharacteristics.Key SensorInfoExposureTimeRange { get; set; }
	public static CameraCharacteristics.Key SensorInfoMaxFrameDuration { get; set; }
	public static CameraCharacteristics.Key SensorInfoPhysicalSize { get; set; }
	public static CameraCharacteristics.Key SensorInfoPixelArraySize { get; set; }
	public static CameraCharacteristics.Key SensorInfoSensitivityRange { get; set; }
	public static CameraCharacteristics.Key SensorInfoTimestampSource { get; set; }
	public static CameraCharacteristics.Key SensorInfoWhiteLevel { get; set; }
	public static CameraCharacteristics.Key SensorMaxAnalogSensitivity { get; set; }
	public static CameraCharacteristics.Key SensorOrientation { get; set; }
	public static CameraCharacteristics.Key SensorReferenceIlluminant1 { get; set; }
	public static CameraCharacteristics.Key SensorReferenceIlluminant2 { get; set; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableFaceDetectModes { get; set; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableHotPixelMapModes { get; set; }
	public static CameraCharacteristics.Key StatisticsInfoMaxFaceCount { get; set; }
	public static CameraCharacteristics.Key SyncMaxLatency { get; set; }
	public static CameraCharacteristics.Key TonemapAvailableToneMapModes { get; set; }
	public static CameraCharacteristics.Key TonemapMaxCurvePoints { get; set; }
```

Added properties:

```
public static CameraCharacteristics.Key ColorCorrectionAvailableAberrationModes { get; }
	public static CameraCharacteristics.Key ControlAeAvailableAntibandingModes { get; }
	public static CameraCharacteristics.Key ControlAeAvailableModes { get; }
	public static CameraCharacteristics.Key ControlAeAvailableTargetFpsRanges { get; }
	public static CameraCharacteristics.Key ControlAeCompensationRange { get; }
	public static CameraCharacteristics.Key ControlAeCompensationStep { get; }
	public static CameraCharacteristics.Key ControlAfAvailableModes { get; }
	public static CameraCharacteristics.Key ControlAvailableEffects { get; }
	public static CameraCharacteristics.Key ControlAvailableSceneModes { get; }
	public static CameraCharacteristics.Key ControlAvailableVideoStabilizationModes { get; }
	public static CameraCharacteristics.Key ControlAwbAvailableModes { get; }
	public static CameraCharacteristics.Key ControlMaxRegionsAe { get; }
	public static CameraCharacteristics.Key ControlMaxRegionsAf { get; }
	public static CameraCharacteristics.Key ControlMaxRegionsAwb { get; }
	public static CameraCharacteristics.Key EdgeAvailableEdgeModes { get; }
	public static CameraCharacteristics.Key FlashInfoAvailable { get; }
	public static CameraCharacteristics.Key HotPixelAvailableHotPixelModes { get; }
	public static CameraCharacteristics.Key InfoSupportedHardwareLevel { get; }
	public static CameraCharacteristics.Key JpegAvailableThumbnailSizes { get; }
	public static CameraCharacteristics.Key LensFacing { get; }
	public static CameraCharacteristics.Key LensInfoAvailableApertures { get; }
	public static CameraCharacteristics.Key LensInfoAvailableFilterDensities { get; }
	public static CameraCharacteristics.Key LensInfoAvailableFocalLengths { get; }
	public static CameraCharacteristics.Key LensInfoAvailableOpticalStabilization { get; }
	public static CameraCharacteristics.Key LensInfoFocusDistanceCalibration { get; }
	public static CameraCharacteristics.Key LensInfoHyperfocalDistance { get; }
	public static CameraCharacteristics.Key LensInfoMinimumFocusDistance { get; }
	public static CameraCharacteristics.Key NoiseReductionAvailableNoiseReductionModes { get; }
	public static CameraCharacteristics.Key RequestAvailableCapabilities { get; }
	public static CameraCharacteristics.Key RequestMaxNumOutputProc { get; }
	public static CameraCharacteristics.Key RequestMaxNumOutputProcStalling { get; }
	public static CameraCharacteristics.Key RequestMaxNumOutputRaw { get; }
	public static CameraCharacteristics.Key RequestPartialResultCount { get; }
	public static CameraCharacteristics.Key RequestPipelineMaxDepth { get; }
	public static CameraCharacteristics.Key ScalerAvailableMaxDigitalZoom { get; }
	public static CameraCharacteristics.Key ScalerCroppingType { get; }
	public static CameraCharacteristics.Key ScalerStreamConfigurationMap { get; }
	public static CameraCharacteristics.Key SensorAvailableTestPatternModes { get; }
	public static CameraCharacteristics.Key SensorBlackLevelPattern { get; }
	public static CameraCharacteristics.Key SensorCalibrationTransform1 { get; }
	public static CameraCharacteristics.Key SensorCalibrationTransform2 { get; }
	public static CameraCharacteristics.Key SensorColorTransform1 { get; }
	public static CameraCharacteristics.Key SensorColorTransform2 { get; }
	public static CameraCharacteristics.Key SensorForwardMatrix1 { get; }
	public static CameraCharacteristics.Key SensorForwardMatrix2 { get; }
	public static CameraCharacteristics.Key SensorInfoActiveArraySize { get; }
	public static CameraCharacteristics.Key SensorInfoColorFilterArrangement { get; }
	public static CameraCharacteristics.Key SensorInfoExposureTimeRange { get; }
	public static CameraCharacteristics.Key SensorInfoMaxFrameDuration { get; }
	public static CameraCharacteristics.Key SensorInfoPhysicalSize { get; }
	public static CameraCharacteristics.Key SensorInfoPixelArraySize { get; }
	public static CameraCharacteristics.Key SensorInfoSensitivityRange { get; }
	public static CameraCharacteristics.Key SensorInfoTimestampSource { get; }
	public static CameraCharacteristics.Key SensorInfoWhiteLevel { get; }
	public static CameraCharacteristics.Key SensorMaxAnalogSensitivity { get; }
	public static CameraCharacteristics.Key SensorOrientation { get; }
	public static CameraCharacteristics.Key SensorReferenceIlluminant1 { get; }
	public static CameraCharacteristics.Key SensorReferenceIlluminant2 { get; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableFaceDetectModes { get; }
	public static CameraCharacteristics.Key StatisticsInfoAvailableHotPixelMapModes { get; }
	public static CameraCharacteristics.Key StatisticsInfoMaxFaceCount { get; }
	public static CameraCharacteristics.Key SyncMaxLatency { get; }
	public static CameraCharacteristics.Key TonemapAvailableToneMapModes { get; }
	public static CameraCharacteristics.Key TonemapMaxCurvePoints { get; }
```

### Type Changed: Android.Hardware.Camera2.CaptureRequest

Removed properties:

```
public static CaptureRequest.Key BlackLevelLock { get; set; }
	public static CaptureRequest.Key ColorCorrectionAberrationMode { get; set; }
	public static CaptureRequest.Key ColorCorrectionGains { get; set; }
	public static CaptureRequest.Key ColorCorrectionMode { get; set; }
	public static CaptureRequest.Key ColorCorrectionTransform { get; set; }
	public static CaptureRequest.Key ControlAeAntibandingMode { get; set; }
	public static CaptureRequest.Key ControlAeExposureCompensation { get; set; }
	public static CaptureRequest.Key ControlAeLock { get; set; }
	public static CaptureRequest.Key ControlAeMode { get; set; }
	public static CaptureRequest.Key ControlAePrecaptureTrigger { get; set; }
	public static CaptureRequest.Key ControlAeRegions { get; set; }
	public static CaptureRequest.Key ControlAeTargetFpsRange { get; set; }
	public static CaptureRequest.Key ControlAfMode { get; set; }
	public static CaptureRequest.Key ControlAfRegions { get; set; }
	public static CaptureRequest.Key ControlAfTrigger { get; set; }
	public static CaptureRequest.Key ControlAwbLock { get; set; }
	public static CaptureRequest.Key ControlAwbMode { get; set; }
	public static CaptureRequest.Key ControlAwbRegions { get; set; }
	public static CaptureRequest.Key ControlCaptureIntent { get; set; }
	public static CaptureRequest.Key ControlEffectMode { get; set; }
	public static CaptureRequest.Key ControlMode { get; set; }
	public static CaptureRequest.Key ControlSceneMode { get; set; }
	public static CaptureRequest.Key ControlVideoStabilizationMode { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
	public static CaptureRequest.Key EdgeMode { get; set; }
	public static CaptureRequest.Key FlashMode { get; set; }
	public static CaptureRequest.Key HotPixelMode { get; set; }
	public static CaptureRequest.Key JpegGpsLocation { get; set; }
	public static CaptureRequest.Key JpegOrientation { get; set; }
	public static CaptureRequest.Key JpegQuality { get; set; }
	public static CaptureRequest.Key JpegThumbnailQuality { get; set; }
	public static CaptureRequest.Key JpegThumbnailSize { get; set; }
	public static CaptureRequest.Key LensAperture { get; set; }
	public static CaptureRequest.Key LensFilterDensity { get; set; }
	public static CaptureRequest.Key LensFocalLength { get; set; }
	public static CaptureRequest.Key LensFocusDistance { get; set; }
	public static CaptureRequest.Key LensOpticalStabilizationMode { get; set; }
	public static CaptureRequest.Key NoiseReductionMode { get; set; }
	public static CaptureRequest.Key ScalerCropRegion { get; set; }
	public static CaptureRequest.Key SensorExposureTime { get; set; }
	public static CaptureRequest.Key SensorFrameDuration { get; set; }
	public static CaptureRequest.Key SensorSensitivity { get; set; }
	public static CaptureRequest.Key SensorTestPatternData { get; set; }
	public static CaptureRequest.Key SensorTestPatternMode { get; set; }
	public static CaptureRequest.Key ShadingMode { get; set; }
	public static CaptureRequest.Key StatisticsFaceDetectMode { get; set; }
	public static CaptureRequest.Key StatisticsHotPixelMapMode { get; set; }
	public static CaptureRequest.Key StatisticsLensShadingMapMode { get; set; }
	public static CaptureRequest.Key TonemapCurve { get; set; }
	public static CaptureRequest.Key TonemapMode { get; set; }
```

Added properties:

```
public static CaptureRequest.Key BlackLevelLock { get; }
	public static CaptureRequest.Key ColorCorrectionAberrationMode { get; }
	public static CaptureRequest.Key ColorCorrectionGains { get; }
	public static CaptureRequest.Key ColorCorrectionMode { get; }
	public static CaptureRequest.Key ColorCorrectionTransform { get; }
	public static CaptureRequest.Key ControlAeAntibandingMode { get; }
	public static CaptureRequest.Key ControlAeExposureCompensation { get; }
	public static CaptureRequest.Key ControlAeLock { get; }
	public static CaptureRequest.Key ControlAeMode { get; }
	public static CaptureRequest.Key ControlAePrecaptureTrigger { get; }
	public static CaptureRequest.Key ControlAeRegions { get; }
	public static CaptureRequest.Key ControlAeTargetFpsRange { get; }
	public static CaptureRequest.Key ControlAfMode { get; }
	public static CaptureRequest.Key ControlAfRegions { get; }
	public static CaptureRequest.Key ControlAfTrigger { get; }
	public static CaptureRequest.Key ControlAwbLock { get; }
	public static CaptureRequest.Key ControlAwbMode { get; }
	public static CaptureRequest.Key ControlAwbRegions { get; }
	public static CaptureRequest.Key ControlCaptureIntent { get; }
	public static CaptureRequest.Key ControlEffectMode { get; }
	public static CaptureRequest.Key ControlMode { get; }
	public static CaptureRequest.Key ControlSceneMode { get; }
	public static CaptureRequest.Key ControlVideoStabilizationMode { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
	public static CaptureRequest.Key EdgeMode { get; }
	public static CaptureRequest.Key FlashMode { get; }
	public static CaptureRequest.Key HotPixelMode { get; }
	public static CaptureRequest.Key JpegGpsLocation { get; }
	public static CaptureRequest.Key JpegOrientation { get; }
	public static CaptureRequest.Key JpegQuality { get; }
	public static CaptureRequest.Key JpegThumbnailQuality { get; }
	public static CaptureRequest.Key JpegThumbnailSize { get; }
	public static CaptureRequest.Key LensAperture { get; }
	public static CaptureRequest.Key LensFilterDensity { get; }
	public static CaptureRequest.Key LensFocalLength { get; }
	public static CaptureRequest.Key LensFocusDistance { get; }
	public static CaptureRequest.Key LensOpticalStabilizationMode { get; }
	public static CaptureRequest.Key NoiseReductionMode { get; }
	public static CaptureRequest.Key ScalerCropRegion { get; }
	public static CaptureRequest.Key SensorExposureTime { get; }
	public static CaptureRequest.Key SensorFrameDuration { get; }
	public static CaptureRequest.Key SensorSensitivity { get; }
	public static CaptureRequest.Key SensorTestPatternData { get; }
	public static CaptureRequest.Key SensorTestPatternMode { get; }
	public static CaptureRequest.Key ShadingMode { get; }
	public static CaptureRequest.Key StatisticsFaceDetectMode { get; }
	public static CaptureRequest.Key StatisticsHotPixelMapMode { get; }
	public static CaptureRequest.Key StatisticsLensShadingMapMode { get; }
	public static CaptureRequest.Key TonemapCurve { get; }
	public static CaptureRequest.Key TonemapMode { get; }
```

### Type Changed: Android.Hardware.Camera2.CaptureResult

Removed properties:

```
public static CaptureResult.Key BlackLevelLock { get; set; }
	public static CaptureResult.Key ColorCorrectionAberrationMode { get; set; }
	public static CaptureResult.Key ColorCorrectionGains { get; set; }
	public static CaptureResult.Key ColorCorrectionMode { get; set; }
	public static CaptureResult.Key ColorCorrectionTransform { get; set; }
	public static CaptureResult.Key ControlAeAntibandingMode { get; set; }
	public static CaptureResult.Key ControlAeExposureCompensation { get; set; }
	public static CaptureResult.Key ControlAeLock { get; set; }
	public static CaptureResult.Key ControlAeMode { get; set; }
	public static CaptureResult.Key ControlAePrecaptureTrigger { get; set; }
	public static CaptureResult.Key ControlAeRegions { get; set; }
	public static CaptureResult.Key ControlAeState { get; set; }
	public static CaptureResult.Key ControlAeTargetFpsRange { get; set; }
	public static CaptureResult.Key ControlAfMode { get; set; }
	public static CaptureResult.Key ControlAfRegions { get; set; }
	public static CaptureResult.Key ControlAfState { get; set; }
	public static CaptureResult.Key ControlAfTrigger { get; set; }
	public static CaptureResult.Key ControlAwbLock { get; set; }
	public static CaptureResult.Key ControlAwbMode { get; set; }
	public static CaptureResult.Key ControlAwbRegions { get; set; }
	public static CaptureResult.Key ControlAwbState { get; set; }
	public static CaptureResult.Key ControlCaptureIntent { get; set; }
	public static CaptureResult.Key ControlEffectMode { get; set; }
	public static CaptureResult.Key ControlMode { get; set; }
	public static CaptureResult.Key ControlSceneMode { get; set; }
	public static CaptureResult.Key ControlVideoStabilizationMode { get; set; }
	public static CaptureResult.Key EdgeMode { get; set; }
	public static CaptureResult.Key FlashMode { get; set; }
	public static CaptureResult.Key FlashState { get; set; }
	public static CaptureResult.Key HotPixelMode { get; set; }
	public static CaptureResult.Key JpegGpsLocation { get; set; }
	public static CaptureResult.Key JpegOrientation { get; set; }
	public static CaptureResult.Key JpegQuality { get; set; }
	public static CaptureResult.Key JpegThumbnailQuality { get; set; }
	public static CaptureResult.Key JpegThumbnailSize { get; set; }
	public static CaptureResult.Key LensAperture { get; set; }
	public static CaptureResult.Key LensFilterDensity { get; set; }
	public static CaptureResult.Key LensFocalLength { get; set; }
	public static CaptureResult.Key LensFocusDistance { get; set; }
	public static CaptureResult.Key LensFocusRange { get; set; }
	public static CaptureResult.Key LensOpticalStabilizationMode { get; set; }
	public static CaptureResult.Key LensState { get; set; }
	public static CaptureResult.Key NoiseReductionMode { get; set; }
	public static CaptureResult.Key RequestPipelineDepth { get; set; }
	public static CaptureResult.Key ScalerCropRegion { get; set; }
	public static CaptureResult.Key SensorExposureTime { get; set; }
	public static CaptureResult.Key SensorFrameDuration { get; set; }
	public static CaptureResult.Key SensorGreenSplit { get; set; }
	public static CaptureResult.Key SensorNeutralColorPoint { get; set; }
	public static CaptureResult.Key SensorNoiseProfile { get; set; }
	public static CaptureResult.Key SensorRollingShutterSkew { get; set; }
	public static CaptureResult.Key SensorSensitivity { get; set; }
	public static CaptureResult.Key SensorTestPatternData { get; set; }
	public static CaptureResult.Key SensorTestPatternMode { get; set; }
	public static CaptureResult.Key SensorTimestamp { get; set; }
	public static CaptureResult.Key ShadingMode { get; set; }
	public static CaptureResult.Key StatisticsFaceDetectMode { get; set; }
	public static CaptureResult.Key StatisticsFaces { get; set; }
	public static CaptureResult.Key StatisticsHotPixelMap { get; set; }
	public static CaptureResult.Key StatisticsHotPixelMapMode { get; set; }
	public static CaptureResult.Key StatisticsLensShadingCorrectionMap { get; set; }
	public static CaptureResult.Key StatisticsLensShadingMapMode { get; set; }
	public static CaptureResult.Key StatisticsSceneFlicker { get; set; }
	public static CaptureResult.Key TonemapCurve { get; set; }
	public static CaptureResult.Key TonemapMode { get; set; }
```

Added properties:

```
public static CaptureResult.Key BlackLevelLock { get; }
	public static CaptureResult.Key ColorCorrectionAberrationMode { get; }
	public static CaptureResult.Key ColorCorrectionGains { get; }
	public static CaptureResult.Key ColorCorrectionMode { get; }
	public static CaptureResult.Key ColorCorrectionTransform { get; }
	public static CaptureResult.Key ControlAeAntibandingMode { get; }
	public static CaptureResult.Key ControlAeExposureCompensation { get; }
	public static CaptureResult.Key ControlAeLock { get; }
	public static CaptureResult.Key ControlAeMode { get; }
	public static CaptureResult.Key ControlAePrecaptureTrigger { get; }
	public static CaptureResult.Key ControlAeRegions { get; }
	public static CaptureResult.Key ControlAeState { get; }
	public static CaptureResult.Key ControlAeTargetFpsRange { get; }
	public static CaptureResult.Key ControlAfMode { get; }
	public static CaptureResult.Key ControlAfRegions { get; }
	public static CaptureResult.Key ControlAfState { get; }
	public static CaptureResult.Key ControlAfTrigger { get; }
	public static CaptureResult.Key ControlAwbLock { get; }
	public static CaptureResult.Key ControlAwbMode { get; }
	public static CaptureResult.Key ControlAwbRegions { get; }
	public static CaptureResult.Key ControlAwbState { get; }
	public static CaptureResult.Key ControlCaptureIntent { get; }
	public static CaptureResult.Key ControlEffectMode { get; }
	public static CaptureResult.Key ControlMode { get; }
	public static CaptureResult.Key ControlSceneMode { get; }
	public static CaptureResult.Key ControlVideoStabilizationMode { get; }
	public static CaptureResult.Key EdgeMode { get; }
	public static CaptureResult.Key FlashMode { get; }
	public static CaptureResult.Key FlashState { get; }
	public static CaptureResult.Key HotPixelMode { get; }
	public static CaptureResult.Key JpegGpsLocation { get; }
	public static CaptureResult.Key JpegOrientation { get; }
	public static CaptureResult.Key JpegQuality { get; }
	public static CaptureResult.Key JpegThumbnailQuality { get; }
	public static CaptureResult.Key JpegThumbnailSize { get; }
	public static CaptureResult.Key LensAperture { get; }
	public static CaptureResult.Key LensFilterDensity { get; }
	public static CaptureResult.Key LensFocalLength { get; }
	public static CaptureResult.Key LensFocusDistance { get; }
	public static CaptureResult.Key LensFocusRange { get; }
	public static CaptureResult.Key LensOpticalStabilizationMode { get; }
	public static CaptureResult.Key LensState { get; }
	public static CaptureResult.Key NoiseReductionMode { get; }
	public static CaptureResult.Key RequestPipelineDepth { get; }
	public static CaptureResult.Key ScalerCropRegion { get; }
	public static CaptureResult.Key SensorExposureTime { get; }
	public static CaptureResult.Key SensorFrameDuration { get; }
	public static CaptureResult.Key SensorGreenSplit { get; }
	public static CaptureResult.Key SensorNeutralColorPoint { get; }
	public static CaptureResult.Key SensorNoiseProfile { get; }
	public static CaptureResult.Key SensorRollingShutterSkew { get; }
	public static CaptureResult.Key SensorSensitivity { get; }
	public static CaptureResult.Key SensorTestPatternData { get; }
	public static CaptureResult.Key SensorTestPatternMode { get; }
	public static CaptureResult.Key SensorTimestamp { get; }
	public static CaptureResult.Key ShadingMode { get; }
	public static CaptureResult.Key StatisticsFaceDetectMode { get; }
	public static CaptureResult.Key StatisticsFaces { get; }
	public static CaptureResult.Key StatisticsHotPixelMap { get; }
	public static CaptureResult.Key StatisticsHotPixelMapMode { get; }
	public static CaptureResult.Key StatisticsLensShadingCorrectionMap { get; }
	public static CaptureResult.Key StatisticsLensShadingMapMode { get; }
	public static CaptureResult.Key StatisticsSceneFlicker { get; }
	public static CaptureResult.Key TonemapCurve { get; }
	public static CaptureResult.Key TonemapMode { get; }
```

## Namespace Android.Hardware.Camera2.Params

### Type Changed: Android.Hardware.Camera2.Params.LensShadingMap

Removed method:

```
public float GetGainFactor (int colorChannel, int column, int row);
```

Added method:

```
public float GetGainFactor (Android.Graphics.Color colorChannel, int column, int row);
```

### Type Changed: Android.Hardware.Camera2.Params.RggbChannelVector

Removed method:

```
public float GetComponent (int colorChannel);
```

Added method:

```
public float GetComponent (Android.Graphics.Color colorChannel);
```

### Type Changed: Android.Hardware.Camera2.Params.TonemapCurve

Removed methods:

```
public void CopyColorCurve (int colorChannel, float[] destination, int offset);
	public Android.Graphics.PointF GetPoint (int colorChannel, int index);
	public int GetPointCount (int colorChannel);
```

Added methods:

```
public void CopyColorCurve (Android.Graphics.Color colorChannel, float[] destination, int offset);
	public Android.Graphics.PointF GetPoint (Android.Graphics.Color colorChannel, int index);
	public int GetPointCount (Android.Graphics.Color colorChannel);
```

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbAccessory

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Hardware.Usb.UsbConfiguration

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Hardware.Usb.UsbDevice

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Hardware.Usb.UsbEndpoint

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Hardware.Usb.UsbInterface

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.InputMethodServices

### Type Changed: Android.InputMethodServices.InputMethodService

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool EnableHardwareAcceleration ();

	[Obsolete ("deprecated")]
	public virtual void OnUpdateCursor (Android.Graphics.Rect newCursor);
```

## Namespace Android.Locations

### Type Changed: Android.Locations.Address

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Locations.Criteria

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Locations.Location

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Locations.SettingInjectorService

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override void OnStart (Android.Content.Intent intent, int startId);

	[Obsolete ("deprecated")]
	public override Android.App.StartCommandResult OnStartCommand (Android.Content.Intent intent, Android.App.StartCommandFlags flags, int startId);
```

## Namespace Android.Media

### Type Changed: Android.Media.AudioAttributes

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.AudioManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Route GetRouting (Mode mode);

	[Obsolete ("deprecated")]
	public virtual VibrateSetting GetVibrateSetting (VibrateType vibrateType);

	[Obsolete ("deprecated")]
	public virtual void RegisterMediaButtonEventReceiver (Android.Content.ComponentName eventReceiver);

	[Obsolete ("deprecated")]
	public virtual void RegisterMediaButtonEventReceiver (Android.App.PendingIntent eventReceiver);

	[Obsolete ("deprecated")]
	public virtual void RegisterRemoteControlClient (RemoteControlClient rcClient);

	[Obsolete ("deprecated")]
	public virtual bool RegisterRemoteController (RemoteController rctlr);

	[Obsolete ("deprecated")]
	public virtual void SetRouting (Mode mode, Route routes, Route mask);

	[Obsolete ("deprecated")]
	public virtual void SetVibrateSetting (VibrateType vibrateType, VibrateSetting vibrateSetting);

	[Obsolete ("deprecated")]
	public virtual bool ShouldVibrate (VibrateType vibrateType);

	[Obsolete ("deprecated")]
	public virtual void UnregisterMediaButtonEventReceiver (Android.App.PendingIntent eventReceiver);

	[Obsolete ("deprecated")]
	public virtual void UnregisterMediaButtonEventReceiver (Android.Content.ComponentName eventReceiver);

	[Obsolete ("deprecated")]
	public virtual void UnregisterRemoteControlClient (RemoteControlClient rcClient);

	[Obsolete ("deprecated")]
	public virtual void UnregisterRemoteController (RemoteController rctlr);
```

### Type Changed: Android.Media.AudioTrack

Obsoleted methods:

```
[Obsolete ("deprecated")]
	protected virtual void SetState (int state);

	[Obsolete ("deprecated")]
	public virtual TrackStatus SetStereoVolume (float leftGain, float rightGain);
```

### Type Changed: Android.Media.MediaCodec

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public Java.Nio.ByteBuffer[] GetInputBuffers ();

	[Obsolete ("deprecated")]
	public Java.Nio.ByteBuffer[] GetOutputBuffers ();
```

### Type Changed: Android.Media.MediaCodecList

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static MediaCodecInfo GetCodecInfoAt (int index);
```

### Type Changed: Android.Media.MediaDescription

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.MediaMetadata

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.MediaRecorder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetAuxiliaryOutputFile (Java.IO.FileDescriptor fd);

	[Obsolete ("deprecated")]
	public virtual void SetAuxiliaryOutputFile (string path);

	[Obsolete ("deprecated")]
	public virtual void SetCamera (Android.Hardware.Camera c);
```

### Type Changed: Android.Media.Rating

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Media.Audiofx

### Type Changed: Android.Media.Audiofx.AudioEffect

Removed properties:

```
public static Java.Util.UUID EffectTypeAec { get; set; }
	public static Java.Util.UUID EffectTypeAgc { get; set; }
	public static Java.Util.UUID EffectTypeBassBoost { get; set; }
	public static Java.Util.UUID EffectTypeEnvReverb { get; set; }
	public static Java.Util.UUID EffectTypeEqualizer { get; set; }
	public static Java.Util.UUID EffectTypeLoudnessEnhancer { get; set; }
	public static Java.Util.UUID EffectTypeNs { get; set; }
	public static Java.Util.UUID EffectTypePresetReverb { get; set; }
	public static Java.Util.UUID EffectTypeVirtualizer { get; set; }
```

Added properties:

```
public static Java.Util.UUID EffectTypeAec { get; }
	public static Java.Util.UUID EffectTypeAgc { get; }
	public static Java.Util.UUID EffectTypeBassBoost { get; }
	public static Java.Util.UUID EffectTypeEnvReverb { get; }
	public static Java.Util.UUID EffectTypeEqualizer { get; }
	public static Java.Util.UUID EffectTypeLoudnessEnhancer { get; }
	public static Java.Util.UUID EffectTypeNs { get; }
	public static Java.Util.UUID EffectTypePresetReverb { get; }
	public static Java.Util.UUID EffectTypeVirtualizer { get; }
```

## Namespace Android.Media.Browse

### Type Changed: Android.Media.Browse.MediaBrowser

### Type Changed: Android.Media.Browse.MediaBrowser.MediaItem

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Media.Session

### Type Changed: Android.Media.Session.MediaSession

### Type Changed: Android.Media.Session.MediaSession.QueueItem

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.Session.MediaSession.Token

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.Session.PlaybackState

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.Session.PlaybackState.CustomAction

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Media.TV

### Type Changed: Android.Media.TV.TvContract

### Type Changed: Android.Media.TV.TvContract.Channels

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Media.TV.TvContract.Programs

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Media.TV.TvInputInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Media.TV.TvTrackInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Net

### Type Changed: Android.Net.ConnectivityManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool RequestRouteToHost (ConnectivityType networkType, int hostAddress);

	[Obsolete ("deprecated")]
	public virtual int StartUsingNetworkFeature (ConnectivityType networkType, string feature);

	[Obsolete ("deprecated")]
	public virtual int StopUsingNetworkFeature (ConnectivityType networkType, string feature);
```

### Type Changed: Android.Net.IpPrefix

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.LinkAddress

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.LinkProperties

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.LocalSocketAddress

### Type Changed: Android.Net.LocalSocketAddress.Namespace

Removed properties:

```
public static LocalSocketAddress.Namespace Abstract { get; set; }
	public static LocalSocketAddress.Namespace Filesystem { get; set; }
	public static LocalSocketAddress.Namespace Reserved { get; set; }
```

Added properties:

```
public static LocalSocketAddress.Namespace Abstract { get; }
	public static LocalSocketAddress.Namespace Filesystem { get; }
	public static LocalSocketAddress.Namespace Reserved { get; }
```

### Type Changed: Android.Net.Network

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.NetworkCapabilities

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.NetworkInfo

### Type Changed: Android.Net.NetworkInfo.DetailedState

Removed properties:

```
public static NetworkInfo.DetailedState Authenticating { get; set; }
	public static NetworkInfo.DetailedState Blocked { get; set; }
	public static NetworkInfo.DetailedState CaptivePortalCheck { get; set; }
	public static NetworkInfo.DetailedState Connected { get; set; }
	public static NetworkInfo.DetailedState Connecting { get; set; }
	public static NetworkInfo.DetailedState Disconnected { get; set; }
	public static NetworkInfo.DetailedState Disconnecting { get; set; }
	public static NetworkInfo.DetailedState Failed { get; set; }
	public static NetworkInfo.DetailedState Idle { get; set; }
	public static NetworkInfo.DetailedState ObtainingIpaddr { get; set; }
	public static NetworkInfo.DetailedState Scanning { get; set; }
	public static NetworkInfo.DetailedState Suspended { get; set; }
	public static NetworkInfo.DetailedState VerifyingPoorLink { get; set; }
```

Added properties:

```
public static NetworkInfo.DetailedState Authenticating { get; }
	public static NetworkInfo.DetailedState Blocked { get; }
	public static NetworkInfo.DetailedState CaptivePortalCheck { get; }
	public static NetworkInfo.DetailedState Connected { get; }
	public static NetworkInfo.DetailedState Connecting { get; }
	public static NetworkInfo.DetailedState Disconnected { get; }
	public static NetworkInfo.DetailedState Disconnecting { get; }
	public static NetworkInfo.DetailedState Failed { get; }
	public static NetworkInfo.DetailedState Idle { get; }
	public static NetworkInfo.DetailedState ObtainingIpaddr { get; }
	public static NetworkInfo.DetailedState Scanning { get; }
	public static NetworkInfo.DetailedState Suspended { get; }
	public static NetworkInfo.DetailedState VerifyingPoorLink { get; }
```

### Type Changed: Android.Net.NetworkInfo.State

Removed properties:

```
public static NetworkInfo.State Connected { get; set; }
	public static NetworkInfo.State Connecting { get; set; }
	public static NetworkInfo.State Disconnected { get; set; }
	public static NetworkInfo.State Disconnecting { get; set; }
	public static NetworkInfo.State Suspended { get; set; }
	public static NetworkInfo.State Unknown { get; set; }
```

Added properties:

```
public static NetworkInfo.State Connected { get; }
	public static NetworkInfo.State Connecting { get; }
	public static NetworkInfo.State Disconnected { get; }
	public static NetworkInfo.State Disconnecting { get; }
	public static NetworkInfo.State Suspended { get; }
	public static NetworkInfo.State Unknown { get; }
```

### Type Changed: Android.Net.NetworkRequest

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Proxy

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string GetHost (Android.Content.Context ctx);

	[Obsolete ("deprecated")]
	public static int GetPort (Android.Content.Context ctx);
```

### Type Changed: Android.Net.ProxyInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.RouteInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.SSLCertificateSocketFactory

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port, Java.Net.InetAddress localAddr, int localPort);

	[Obsolete ("deprecated")]
	public override Java.Net.Socket CreateSocket (Java.Net.InetAddress addr, int port);

	[Obsolete ("deprecated")]
	public static Javax.Net.Ssl.SSLSocketFactory GetInsecure (int handshakeTimeoutMillis, SSLSessionCache cache);
```

### Type Changed: Android.Net.TrafficStats

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static long GetUidTcpRxBytes (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidTcpRxSegments (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidTcpTxBytes (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidTcpTxSegments (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidUdpRxBytes (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidUdpRxPackets (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidUdpTxBytes (int uid);

	[Obsolete ("deprecated")]
	public static long GetUidUdpTxPackets (int uid);
```

### Type Changed: Android.Net.Uri

Removed properties:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
	public static Uri Empty { get; set; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public static Uri Empty { get; }
```

## Namespace Android.Net.Nsd

### Type Changed: Android.Net.Nsd.NsdServiceInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Net.Rtp

### Type Changed: Android.Net.Rtp.AudioCodec

Removed properties:

```
public static AudioCodec Amr { get; set; }
	public static AudioCodec Gsm { get; set; }
	public static AudioCodec GsmEfr { get; set; }
	public static AudioCodec Pcma { get; set; }
	public static AudioCodec Pcmu { get; set; }
```

Added properties:

```
public static AudioCodec Amr { get; }
	public static AudioCodec Gsm { get; }
	public static AudioCodec GsmEfr { get; }
	public static AudioCodec Pcma { get; }
	public static AudioCodec Pcmu { get; }
```

## Namespace Android.Net.Sip

### Type Changed: Android.Net.Sip.SipProfile

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Net.Wifi

### Type Changed: Android.Net.Wifi.SupplicantState

Removed properties:

```
public static SupplicantState Associated { get; set; }
	public static SupplicantState Associating { get; set; }
	public static SupplicantState Authenticating { get; set; }
	public static SupplicantState Completed { get; set; }
	public static SupplicantState Disconnected { get; set; }
	public static SupplicantState Dormant { get; set; }
	public static SupplicantState FourWayHandshake { get; set; }
	public static SupplicantState GroupHandshake { get; set; }
	public static SupplicantState Inactive { get; set; }
	public static SupplicantState InterfaceDisabled { get; set; }
	public static SupplicantState Invalid { get; set; }
	public static SupplicantState Scanning { get; set; }
	public static SupplicantState Uninitialized { get; set; }
```

Added properties:

```
public static SupplicantState Associated { get; }
	public static SupplicantState Associating { get; }
	public static SupplicantState Authenticating { get; }
	public static SupplicantState Completed { get; }
	public static SupplicantState Disconnected { get; }
	public static SupplicantState Dormant { get; }
	public static SupplicantState FourWayHandshake { get; }
	public static SupplicantState GroupHandshake { get; }
	public static SupplicantState Inactive { get; }
	public static SupplicantState InterfaceDisabled { get; }
	public static SupplicantState Invalid { get; }
	public static SupplicantState Scanning { get; }
	public static SupplicantState Uninitialized { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration

### Type Changed: Android.Net.Wifi.WifiConfiguration.AuthAlgorithm

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.GroupCipher

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.KeyMgmt

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.PairwiseCipher

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.Protocol

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiConfiguration.Status

Removed property:

```
public static System.Collections.Generic.IList<string> Strings { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Strings { get; }
```

### Type Changed: Android.Net.Wifi.WifiEnterpriseConfig

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Wifi.WpsInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Net.Wifi.P2p

### Type Changed: Android.Net.Wifi.P2p.WifiP2pConfig

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pDevice

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pDeviceList

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pGroup

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Net.Wifi.P2p.WifiP2pInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Nfc

### Type Changed: Android.Nfc.NdefMessage

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Nfc.NdefRecord

Removed properties:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
	public static System.Collections.Generic.IList<byte> RtdAlternativeCarrier { get; set; }
	public static System.Collections.Generic.IList<byte> RtdHandoverCarrier { get; set; }
	public static System.Collections.Generic.IList<byte> RtdHandoverRequest { get; set; }
	public static System.Collections.Generic.IList<byte> RtdHandoverSelect { get; set; }
	public static System.Collections.Generic.IList<byte> RtdSmartPoster { get; set; }
	public static System.Collections.Generic.IList<byte> RtdText { get; set; }
	public static System.Collections.Generic.IList<byte> RtdUri { get; set; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public static System.Collections.Generic.IList<byte> RtdAlternativeCarrier { get; }
	public static System.Collections.Generic.IList<byte> RtdHandoverCarrier { get; }
	public static System.Collections.Generic.IList<byte> RtdHandoverRequest { get; }
	public static System.Collections.Generic.IList<byte> RtdHandoverSelect { get; }
	public static System.Collections.Generic.IList<byte> RtdSmartPoster { get; }
	public static System.Collections.Generic.IList<byte> RtdText { get; }
	public static System.Collections.Generic.IList<byte> RtdUri { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public byte[] ToByteArray ();
```

### Type Changed: Android.Nfc.NfcAdapter

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public void DisableForegroundNdefPush (Android.App.Activity activity);

	[Obsolete ("deprecated")]
	public void EnableForegroundNdefPush (Android.App.Activity activity, NdefMessage message);
```

### Type Changed: Android.Nfc.Tag

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Nfc.Tech

### Type Changed: Android.Nfc.Tech.MifareClassic

Removed properties:

```
public static System.Collections.Generic.IList<byte> KeyDefault { get; set; }
	public static System.Collections.Generic.IList<byte> KeyMifareApplicationDirectory { get; set; }
	public static System.Collections.Generic.IList<byte> KeyNfcForum { get; set; }
```

Added properties:

```
public static System.Collections.Generic.IList<byte> KeyDefault { get; }
	public static System.Collections.Generic.IList<byte> KeyMifareApplicationDirectory { get; }
	public static System.Collections.Generic.IList<byte> KeyNfcForum { get; }
```

## Namespace Android.Opengl

### Type Changed: Android.Opengl.EGLObjectHandle

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual int GetHandle ();
```

## Namespace Android.OS

### Type Changed: Android.OS.AsyncTask

Removed properties:

```
public static Java.Util.Concurrent.IExecutor SerialExecutor { get; set; }
	public static Java.Util.Concurrent.IExecutor ThreadPoolExecutor { get; set; }
```

Added properties:

```
public static Java.Util.Concurrent.IExecutor SerialExecutor { get; }
	public static Java.Util.Concurrent.IExecutor ThreadPoolExecutor { get; }
```

### Type Changed: Android.OS.AsyncTask.Status

Removed properties:

```
public static AsyncTask.Status Finished { get; set; }
	public static AsyncTask.Status Pending { get; set; }
	public static AsyncTask.Status Running { get; set; }
```

Added properties:

```
public static AsyncTask.Status Finished { get; }
	public static AsyncTask.Status Pending { get; }
	public static AsyncTask.Status Running { get; }
```

### Type Changed: Android.OS.Build

Removed properties:

```
public static string Board { get; set; }
	public static string Bootloader { get; set; }
	public static string Brand { get; set; }
	public static string CpuAbi { get; set; }
	public static string CpuAbi2 { get; set; }
	public static string Device { get; set; }
	public static string Display { get; set; }
	public static string Fingerprint { get; set; }
	public static string Hardware { get; set; }
	public static string Host { get; set; }
	public static string Id { get; set; }
	public static string Manufacturer { get; set; }
	public static string Model { get; set; }
	public static string Product { get; set; }
	public static string Radio { get; set; }
	public static string Serial { get; set; }
	public static System.Collections.Generic.IList<string> Supported32BitAbis { get; set; }
	public static System.Collections.Generic.IList<string> Supported64BitAbis { get; set; }
	public static System.Collections.Generic.IList<string> SupportedAbis { get; set; }
	public static string Tags { get; set; }
	public static long Time { get; set; }
	public static string Type { get; set; }
	public static string User { get; set; }
```

Added properties:

```
public static string Board { get; }
	public static string Bootloader { get; }
	public static string Brand { get; }
	public static string CpuAbi { get; }
	public static string CpuAbi2 { get; }
	public static string Device { get; }
	public static string Display { get; }
	public static string Fingerprint { get; }
	public static string Hardware { get; }
	public static string Host { get; }
	public static string Id { get; }
	public static string Manufacturer { get; }
	public static string Model { get; }
	public static string Product { get; }
	public static string Radio { get; }
	public static string Serial { get; }
	public static System.Collections.Generic.IList<string> Supported32BitAbis { get; }
	public static System.Collections.Generic.IList<string> Supported64BitAbis { get; }
	public static System.Collections.Generic.IList<string> SupportedAbis { get; }
	public static string Tags { get; }
	public static long Time { get; }
	public static string Type { get; }
	public static string User { get; }
```

### Type Changed: Android.OS.Build.VERSION

Removed properties:

```
public static string Codename { get; set; }
	public static string Incremental { get; set; }
	public static string Release { get; set; }
	public static string Sdk { get; set; }
	public static BuildVersionCodes SdkInt { get; set; }
```

Added properties:

```
public static string Codename { get; }
	public static string Incremental { get; }
	public static string Release { get; }
	public static string Sdk { get; }
	public static BuildVersionCodes SdkInt { get; }
```

### Type Changed: Android.OS.Bundle

Removed properties:

```
public static IParcelableCreator Creator { get; set; }
	public static Bundle Empty { get; set; }
```

Added properties:

```
public static IParcelableCreator Creator { get; }
	public static Bundle Empty { get; }
```

### Type Changed: Android.OS.Debug

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static void ChangeDebugPort (int port);

	[Obsolete ("deprecated")]
	public static void ResetGlobalExternalAllocCount ();

	[Obsolete ("deprecated")]
	public static void ResetGlobalExternalAllocSize ();

	[Obsolete ("deprecated")]
	public static void ResetGlobalExternalFreedCount ();

	[Obsolete ("deprecated")]
	public static void ResetGlobalExternalFreedSize ();

	[Obsolete ("deprecated")]
	public static void ResetThreadExternalAllocCount ();

	[Obsolete ("deprecated")]
	public static void ResetThreadExternalAllocSize ();

	[Obsolete ("deprecated")]
	public static int SetAllocationLimit (int limit);

	[Obsolete ("deprecated")]
	public static int SetGlobalAllocationLimit (int limit);

	[Obsolete ("deprecated")]
	public static void StartAllocCounting ();

	[Obsolete ("deprecated")]
	public static void StopAllocCounting ();
```

### Type Changed: Android.OS.Debug.MemoryInfo

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.DropBoxManager

### Type Changed: Android.OS.DropBoxManager.Entry

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.Environment

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static string GetStorageState (Java.IO.File path);
```

### Type Changed: Android.OS.Message

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.Messenger

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.Parcel

Removed property:

```
public static IParcelableCreator StringCreator { get; set; }
```

Added property:

```
public static IParcelableCreator StringCreator { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public void WriteFileDescriptor (Java.IO.FileDescriptor val);

	[Obsolete ("deprecated")]
	public void WriteValue (Java.Lang.Object v);
```

### Type Changed: Android.OS.ParcelFileDescriptor

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.ParcelUuid

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.PatternMatcher

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.PersistableBundle

Removed properties:

```
public static IParcelableCreator Creator { get; set; }
	public static PersistableBundle Empty { get; set; }
```

Added properties:

```
public static IParcelableCreator Creator { get; }
	public static PersistableBundle Empty { get; }
```

### Type Changed: Android.OS.Process

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static bool SupportsProcesses ();
```

### Type Changed: Android.OS.ResultReceiver

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.StrictMode

### Type Changed: Android.OS.StrictMode.ThreadPolicy

Removed property:

```
public static StrictMode.ThreadPolicy Lax { get; set; }
```

Added property:

```
public static StrictMode.ThreadPolicy Lax { get; }
```

### Type Changed: Android.OS.StrictMode.VmPolicy

Removed property:

```
public static StrictMode.VmPolicy Lax { get; set; }
```

Added property:

```
public static StrictMode.VmPolicy Lax { get; }
```

### Type Changed: Android.OS.UserHandle

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

### Type Changed: Android.OS.UserManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetUserRestriction (string key, bool value);

	[Obsolete ("deprecated")]
	public virtual void SetUserRestrictions (Bundle restrictions, UserHandle userHandle);
```

### Type Changed: Android.OS.WorkSource

Removed property:

```
public static IParcelableCreator Creator { get; set; }
```

Added property:

```
public static IParcelableCreator Creator { get; }
```

## Namespace Android.Preferences

### Type Changed: Android.Preferences.CheckBoxPreference

Added properties:

```
public string SummaryOff { get; set; }
	public string SummaryOn { get; set; }
```

### Type Changed: Android.Preferences.Preference

### Type Changed: Android.Preferences.Preference.BaseSavedState

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Preferences.PreferenceActivity

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddPreferencesFromIntent (Android.Content.Intent intent);

	[Obsolete ("deprecated")]
	public virtual void AddPreferencesFromResource (int preferencesResId);

	[Obsolete ("deprecated")]
	public virtual Preference FindPreference (Java.Lang.ICharSequence key);

	[Obsolete ("deprecated")]
	public virtual bool OnPreferenceTreeClick (PreferenceScreen preferenceScreen, Preference preference);
```

### Type Changed: Android.Preferences.PreferenceActivity.Header

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Print

### Type Changed: Android.Print.PageRange

Removed properties:

```
public static PageRange AllPages { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public static PageRange AllPages { get; }
	public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrintAttributes

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrintAttributes.Margins

Removed property:

```
public static PrintAttributes.Margins NoMargins { get; set; }
```

Added property:

```
public static PrintAttributes.Margins NoMargins { get; }
```

### Type Changed: Android.Print.PrintAttributes.MediaSize

Removed properties:

```
public static PrintAttributes.MediaSize IsoA0 { get; set; }
	public static PrintAttributes.MediaSize IsoA1 { get; set; }
	public static PrintAttributes.MediaSize IsoA10 { get; set; }
	public static PrintAttributes.MediaSize IsoA2 { get; set; }
	public static PrintAttributes.MediaSize IsoA3 { get; set; }
	public static PrintAttributes.MediaSize IsoA4 { get; set; }
	public static PrintAttributes.MediaSize IsoA5 { get; set; }
	public static PrintAttributes.MediaSize IsoA6 { get; set; }
	public static PrintAttributes.MediaSize IsoA7 { get; set; }
	public static PrintAttributes.MediaSize IsoA8 { get; set; }
	public static PrintAttributes.MediaSize IsoA9 { get; set; }
	public static PrintAttributes.MediaSize IsoB0 { get; set; }
	public static PrintAttributes.MediaSize IsoB1 { get; set; }
	public static PrintAttributes.MediaSize IsoB10 { get; set; }
	public static PrintAttributes.MediaSize IsoB2 { get; set; }
	public static PrintAttributes.MediaSize IsoB3 { get; set; }
	public static PrintAttributes.MediaSize IsoB4 { get; set; }
	public static PrintAttributes.MediaSize IsoB5 { get; set; }
	public static PrintAttributes.MediaSize IsoB6 { get; set; }
	public static PrintAttributes.MediaSize IsoB7 { get; set; }
	public static PrintAttributes.MediaSize IsoB8 { get; set; }
	public static PrintAttributes.MediaSize IsoB9 { get; set; }
	public static PrintAttributes.MediaSize IsoC0 { get; set; }
	public static PrintAttributes.MediaSize IsoC1 { get; set; }
	public static PrintAttributes.MediaSize IsoC10 { get; set; }
	public static PrintAttributes.MediaSize IsoC2 { get; set; }
	public static PrintAttributes.MediaSize IsoC3 { get; set; }
	public static PrintAttributes.MediaSize IsoC4 { get; set; }
	public static PrintAttributes.MediaSize IsoC5 { get; set; }
	public static PrintAttributes.MediaSize IsoC6 { get; set; }
	public static PrintAttributes.MediaSize IsoC7 { get; set; }
	public static PrintAttributes.MediaSize IsoC8 { get; set; }
	public static PrintAttributes.MediaSize IsoC9 { get; set; }
	public static PrintAttributes.MediaSize JisB0 { get; set; }
	public static PrintAttributes.MediaSize JisB1 { get; set; }
	public static PrintAttributes.MediaSize JisB10 { get; set; }
	public static PrintAttributes.MediaSize JisB2 { get; set; }
	public static PrintAttributes.MediaSize JisB3 { get; set; }
	public static PrintAttributes.MediaSize JisB4 { get; set; }
	public static PrintAttributes.MediaSize JisB5 { get; set; }
	public static PrintAttributes.MediaSize JisB6 { get; set; }
	public static PrintAttributes.MediaSize JisB7 { get; set; }
	public static PrintAttributes.MediaSize JisB8 { get; set; }
	public static PrintAttributes.MediaSize JisB9 { get; set; }
	public static PrintAttributes.MediaSize JisExec { get; set; }
	public static PrintAttributes.MediaSize JpnChou2 { get; set; }
	public static PrintAttributes.MediaSize JpnChou3 { get; set; }
	public static PrintAttributes.MediaSize JpnChou4 { get; set; }
	public static PrintAttributes.MediaSize JpnHagaki { get; set; }
	public static PrintAttributes.MediaSize JpnKahu { get; set; }
	public static PrintAttributes.MediaSize JpnKaku2 { get; set; }
	public static PrintAttributes.MediaSize JpnOufuku { get; set; }
	public static PrintAttributes.MediaSize JpnYou4 { get; set; }
	public static PrintAttributes.MediaSize NaFoolscap { get; set; }
	public static PrintAttributes.MediaSize NaGovtLetter { get; set; }
	public static PrintAttributes.MediaSize NaIndex3x5 { get; set; }
	public static PrintAttributes.MediaSize NaIndex4x6 { get; set; }
	public static PrintAttributes.MediaSize NaIndex5x8 { get; set; }
	public static PrintAttributes.MediaSize NaJuniorLegal { get; set; }
	public static PrintAttributes.MediaSize NaLedger { get; set; }
	public static PrintAttributes.MediaSize NaLegal { get; set; }
	public static PrintAttributes.MediaSize NaLetter { get; set; }
	public static PrintAttributes.MediaSize NaMonarch { get; set; }
	public static PrintAttributes.MediaSize NaQuarto { get; set; }
	public static PrintAttributes.MediaSize NaTabloid { get; set; }
	public static PrintAttributes.MediaSize OmDaiPaKai { get; set; }
	public static PrintAttributes.MediaSize OmJuuroKuKai { get; set; }
	public static PrintAttributes.MediaSize OmPaKai { get; set; }
	public static PrintAttributes.MediaSize Prc1 { get; set; }
	public static PrintAttributes.MediaSize Prc10 { get; set; }
	public static PrintAttributes.MediaSize Prc16k { get; set; }
	public static PrintAttributes.MediaSize Prc2 { get; set; }
	public static PrintAttributes.MediaSize Prc3 { get; set; }
	public static PrintAttributes.MediaSize Prc4 { get; set; }
	public static PrintAttributes.MediaSize Prc5 { get; set; }
	public static PrintAttributes.MediaSize Prc6 { get; set; }
	public static PrintAttributes.MediaSize Prc7 { get; set; }
	public static PrintAttributes.MediaSize Prc8 { get; set; }
	public static PrintAttributes.MediaSize Prc9 { get; set; }
	public static PrintAttributes.MediaSize Roc16k { get; set; }
	public static PrintAttributes.MediaSize Roc8k { get; set; }
	public static PrintAttributes.MediaSize UnknownLandscape { get; set; }
	public static PrintAttributes.MediaSize UnknownPortrait { get; set; }
```

Added properties:

```
public static PrintAttributes.MediaSize IsoA0 { get; }
	public static PrintAttributes.MediaSize IsoA1 { get; }
	public static PrintAttributes.MediaSize IsoA10 { get; }
	public static PrintAttributes.MediaSize IsoA2 { get; }
	public static PrintAttributes.MediaSize IsoA3 { get; }
	public static PrintAttributes.MediaSize IsoA4 { get; }
	public static PrintAttributes.MediaSize IsoA5 { get; }
	public static PrintAttributes.MediaSize IsoA6 { get; }
	public static PrintAttributes.MediaSize IsoA7 { get; }
	public static PrintAttributes.MediaSize IsoA8 { get; }
	public static PrintAttributes.MediaSize IsoA9 { get; }
	public static PrintAttributes.MediaSize IsoB0 { get; }
	public static PrintAttributes.MediaSize IsoB1 { get; }
	public static PrintAttributes.MediaSize IsoB10 { get; }
	public static PrintAttributes.MediaSize IsoB2 { get; }
	public static PrintAttributes.MediaSize IsoB3 { get; }
	public static PrintAttributes.MediaSize IsoB4 { get; }
	public static PrintAttributes.MediaSize IsoB5 { get; }
	public static PrintAttributes.MediaSize IsoB6 { get; }
	public static PrintAttributes.MediaSize IsoB7 { get; }
	public static PrintAttributes.MediaSize IsoB8 { get; }
	public static PrintAttributes.MediaSize IsoB9 { get; }
	public static PrintAttributes.MediaSize IsoC0 { get; }
	public static PrintAttributes.MediaSize IsoC1 { get; }
	public static PrintAttributes.MediaSize IsoC10 { get; }
	public static PrintAttributes.MediaSize IsoC2 { get; }
	public static PrintAttributes.MediaSize IsoC3 { get; }
	public static PrintAttributes.MediaSize IsoC4 { get; }
	public static PrintAttributes.MediaSize IsoC5 { get; }
	public static PrintAttributes.MediaSize IsoC6 { get; }
	public static PrintAttributes.MediaSize IsoC7 { get; }
	public static PrintAttributes.MediaSize IsoC8 { get; }
	public static PrintAttributes.MediaSize IsoC9 { get; }
	public static PrintAttributes.MediaSize JisB0 { get; }
	public static PrintAttributes.MediaSize JisB1 { get; }
	public static PrintAttributes.MediaSize JisB10 { get; }
	public static PrintAttributes.MediaSize JisB2 { get; }
	public static PrintAttributes.MediaSize JisB3 { get; }
	public static PrintAttributes.MediaSize JisB4 { get; }
	public static PrintAttributes.MediaSize JisB5 { get; }
	public static PrintAttributes.MediaSize JisB6 { get; }
	public static PrintAttributes.MediaSize JisB7 { get; }
	public static PrintAttributes.MediaSize JisB8 { get; }
	public static PrintAttributes.MediaSize JisB9 { get; }
	public static PrintAttributes.MediaSize JisExec { get; }
	public static PrintAttributes.MediaSize JpnChou2 { get; }
	public static PrintAttributes.MediaSize JpnChou3 { get; }
	public static PrintAttributes.MediaSize JpnChou4 { get; }
	public static PrintAttributes.MediaSize JpnHagaki { get; }
	public static PrintAttributes.MediaSize JpnKahu { get; }
	public static PrintAttributes.MediaSize JpnKaku2 { get; }
	public static PrintAttributes.MediaSize JpnOufuku { get; }
	public static PrintAttributes.MediaSize JpnYou4 { get; }
	public static PrintAttributes.MediaSize NaFoolscap { get; }
	public static PrintAttributes.MediaSize NaGovtLetter { get; }
	public static PrintAttributes.MediaSize NaIndex3x5 { get; }
	public static PrintAttributes.MediaSize NaIndex4x6 { get; }
	public static PrintAttributes.MediaSize NaIndex5x8 { get; }
	public static PrintAttributes.MediaSize NaJuniorLegal { get; }
	public static PrintAttributes.MediaSize NaLedger { get; }
	public static PrintAttributes.MediaSize NaLegal { get; }
	public static PrintAttributes.MediaSize NaLetter { get; }
	public static PrintAttributes.MediaSize NaMonarch { get; }
	public static PrintAttributes.MediaSize NaQuarto { get; }
	public static PrintAttributes.MediaSize NaTabloid { get; }
	public static PrintAttributes.MediaSize OmDaiPaKai { get; }
	public static PrintAttributes.MediaSize OmJuuroKuKai { get; }
	public static PrintAttributes.MediaSize OmPaKai { get; }
	public static PrintAttributes.MediaSize Prc1 { get; }
	public static PrintAttributes.MediaSize Prc10 { get; }
	public static PrintAttributes.MediaSize Prc16k { get; }
	public static PrintAttributes.MediaSize Prc2 { get; }
	public static PrintAttributes.MediaSize Prc3 { get; }
	public static PrintAttributes.MediaSize Prc4 { get; }
	public static PrintAttributes.MediaSize Prc5 { get; }
	public static PrintAttributes.MediaSize Prc6 { get; }
	public static PrintAttributes.MediaSize Prc7 { get; }
	public static PrintAttributes.MediaSize Prc8 { get; }
	public static PrintAttributes.MediaSize Prc9 { get; }
	public static PrintAttributes.MediaSize Roc16k { get; }
	public static PrintAttributes.MediaSize Roc8k { get; }
	public static PrintAttributes.MediaSize UnknownLandscape { get; }
	public static PrintAttributes.MediaSize UnknownPortrait { get; }
```

### Type Changed: Android.Print.PrintDocumentInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrinterCapabilitiesInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrinterId

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrinterInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrintJobId

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Print.PrintJobInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Provider

### Type Changed: Android.Provider.Browser

Removed properties:

```
public static Android.Net.Uri BookmarksUri { get; set; }
	public static System.Collections.Generic.IList<string> HistoryProjection { get; set; }
	public static System.Collections.Generic.IList<string> SearchesProjection { get; set; }
	public static Android.Net.Uri SearchesUri { get; set; }
	public static System.Collections.Generic.IList<string> TruncateHistoryProjection { get; set; }
```

Added properties:

```
public static Android.Net.Uri BookmarksUri { get; }
	public static System.Collections.Generic.IList<string> HistoryProjection { get; }
	public static System.Collections.Generic.IList<string> SearchesProjection { get; }
	public static Android.Net.Uri SearchesUri { get; }
	public static System.Collections.Generic.IList<string> TruncateHistoryProjection { get; }
```

### Type Changed: Android.Provider.CalendarContract

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Attendees

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarAlerts

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ContentUriByInstance { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ContentUriByInstance { get; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarCache

Removed property:

```
public static Android.Net.Uri Uri { get; set; }
```

Added property:

```
public static Android.Net.Uri Uri { get; }
```

### Type Changed: Android.Provider.CalendarContract.CalendarEntity

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Calendars

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Colors

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.EventDays

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Events

Removed properties:

```
public static Android.Net.Uri ContentExceptionUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentExceptionUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.EventsEntity

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.ExtendedProperties

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Instances

Removed properties:

```
public static Android.Net.Uri ContentByDayUri { get; set; }
	public static Android.Net.Uri ContentSearchByDayUri { get; set; }
	public static Android.Net.Uri ContentSearchUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentByDayUri { get; }
	public static Android.Net.Uri ContentSearchByDayUri { get; }
	public static Android.Net.Uri ContentSearchUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.Reminders

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CalendarContract.SyncState

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CallLog

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.CallLog.Calls

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ContentUriWithVoicemail { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ContentUriWithVoicemail { get; }
```

### Type Changed: Android.Provider.Contacts

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Contacts.ContactMethods

Removed properties:

```
public static Android.Net.Uri ContentEmailUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentEmailUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public void AddPostalLocation (Android.Content.Context context, long postalId, double latitude, double longitude);

	[Obsolete ("deprecated")]
	public static Java.Lang.Object DecodeImProtocol (string encodedString);

	[Obsolete ("deprecated")]
	public static string EncodeCustomImProtocol (string protocolString);

	[Obsolete ("deprecated")]
	public static string EncodePredefinedImProtocol (int protocol);

	[Obsolete ("deprecated")]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactKind kind, ContactMethodColumn type, Java.Lang.ICharSequence label);
```

### Type Changed: Android.Provider.Contacts.Extensions

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Contacts.GroupMembership

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri RawContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri RawContentUri { get; }
```

### Type Changed: Android.Provider.Contacts.Groups

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri DeletedContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri DeletedContentUri { get; }
```

### Type Changed: Android.Provider.Contacts.Organizations

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactOrganizationColumn type, Java.Lang.ICharSequence label);
```

### Type Changed: Android.Provider.Contacts.People

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri DeletedContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri DeletedContentUri { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static Android.Net.Uri AddToGroup (Android.Content.ContentResolver resolver, long personId, string groupName);

	[Obsolete ("deprecated")]
	public static Android.Net.Uri AddToGroup (Android.Content.ContentResolver resolver, long personId, long groupId);

	[Obsolete ("deprecated")]
	public static Android.Net.Uri AddToMyContactsGroup (Android.Content.ContentResolver resolver, long personId);

	[Obsolete ("deprecated")]
	public static Android.Net.Uri CreatePersonInMyContactsGroup (Android.Content.ContentResolver resolver, Android.Content.ContentValues values);

	[Obsolete ("deprecated")]
	public static Android.Graphics.Bitmap LoadContactPhoto (Android.Content.Context context, Android.Net.Uri person, int placeholderImageResource, Android.Graphics.BitmapFactory.Options options);

	[Obsolete ("deprecated")]
	public static void MarkAsContacted (Android.Content.ContentResolver resolver, long personId);

	[Obsolete ("deprecated")]
	public static System.IO.Stream OpenContactPhotoInputStream (Android.Content.ContentResolver cr, Android.Net.Uri person);

	[Obsolete ("deprecated")]
	public static Android.Database.ICursor QueryGroups (Android.Content.ContentResolver resolver, long person);

	[Obsolete ("deprecated")]
	public static void SetPhotoData (Android.Content.ContentResolver cr, Android.Net.Uri person, byte[] data);
```

### Type Changed: Android.Provider.Contacts.Phones

Removed properties:

```
public static Android.Net.Uri ContentFilterUrl { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUrl { get; }
	public static Android.Net.Uri ContentUri { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactPhoneColumn type, Java.Lang.ICharSequence label);

	[Obsolete ("deprecated")]
	public static Java.Lang.ICharSequence GetDisplayLabelFormatted (Android.Content.Context context, ContactPhoneColumn type, Java.Lang.ICharSequence label, Java.Lang.ICharSequence[] labelArray);
```

### Type Changed: Android.Provider.Contacts.Photos

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Contacts.Settings

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string GetSetting (Android.Content.ContentResolver cr, string account, string key);

	[Obsolete ("deprecated")]
	public static void SetSetting (Android.Content.ContentResolver cr, string account, string key, string value);
```

### Type Changed: Android.Provider.ContactsContract

Removed property:

```
public static Android.Net.Uri AuthorityUri { get; set; }
```

Added property:

```
public static Android.Net.Uri AuthorityUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.AggregationExceptions

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.CommonDataKinds

### Type Changed: Android.Provider.ContactsContract.Callable

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Contactables

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Email

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentLookupUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentLookupUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Phone

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.StructuredPostal

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Contacts

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri ContentFrequentUri { get; set; }
	public static Android.Net.Uri ContentGroupUri { get; set; }
	public static Android.Net.Uri ContentLookupUri { get; set; }
	public static Android.Net.Uri ContentMultiVcardUri { get; set; }
	public static Android.Net.Uri ContentStrequentFilterUri { get; set; }
	public static Android.Net.Uri ContentStrequentUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ContentVcardUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri ContentFrequentUri { get; }
	public static Android.Net.Uri ContentGroupUri { get; }
	public static Android.Net.Uri ContentLookupUri { get; }
	public static Android.Net.Uri ContentMultiVcardUri { get; }
	public static Android.Net.Uri ContentStrequentFilterUri { get; }
	public static Android.Net.Uri ContentStrequentUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ContentVcardUri { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static void MarkAsContacted (Android.Content.ContentResolver resolver, long contactId);
```

### Type Changed: Android.Provider.ContactsContract.Data

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.DataUsageFeedback

Removed properties:

```
public static Android.Net.Uri DeleteUsageUri { get; set; }
	public static Android.Net.Uri FeedbackUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri DeleteUsageUri { get; }
	public static Android.Net.Uri FeedbackUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.DeletedContacts

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Directory

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.DisplayPhoto

Removed properties:

```
public static Android.Net.Uri ContentMaxDimensionsUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentMaxDimensionsUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Groups

Removed properties:

```
public static Android.Net.Uri ContentSummaryUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentSummaryUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.PhoneLookup

Removed properties:

```
public static Android.Net.Uri ContentFilterUri { get; set; }
	public static Android.Net.Uri EnterpriseContentFilterUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentFilterUri { get; }
	public static Android.Net.Uri EnterpriseContentFilterUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Profile

Removed properties:

```
public static Android.Net.Uri ContentRawContactsUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ContentVcardUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentRawContactsUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ContentVcardUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.ProfileSyncState

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.RawContacts

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.RawContactsEntity

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ProfileContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ProfileContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.Settings

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.StatusUpdates

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ProfileContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ProfileContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.StreamItems

Removed properties:

```
public static Android.Net.Uri ContentLimitUri { get; set; }
	public static Android.Net.Uri ContentPhotoUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentLimitUri { get; }
	public static Android.Net.Uri ContentPhotoUri { get; }
	public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.ContactsContract.SyncState

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore

### Type Changed: Android.Provider.MediaStore.Audio

### Type Changed: Android.Provider.MediaStore.Albums

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Artists

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Genres

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Media

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Playlists

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Images

### Type Changed: Android.Provider.MediaStore.Media

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Thumbnails

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Video

### Type Changed: Android.Provider.MediaStore.Media

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.MediaStore.Thumbnails

Removed properties:

```
public static Android.Net.Uri ExternalContentUri { get; set; }
	public static Android.Net.Uri InternalContentUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ExternalContentUri { get; }
	public static Android.Net.Uri InternalContentUri { get; }
```

### Type Changed: Android.Provider.SearchRecentSuggestions

Removed properties:

```
public static System.Collections.Generic.IList<string> QueriesProjection1line { get; set; }
	public static System.Collections.Generic.IList<string> QueriesProjection2line { get; set; }
```

Added properties:

```
public static System.Collections.Generic.IList<string> QueriesProjection1line { get; }
	public static System.Collections.Generic.IList<string> QueriesProjection2line { get; }
```

### Type Changed: Android.Provider.Settings

### Type Changed: Android.Provider.Settings.Global

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Settings.Secure

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static bool IsLocationProviderEnabled (Android.Content.ContentResolver cr, string provider);

	[Obsolete ("deprecated")]
	public static void SetLocationProviderEnabled (Android.Content.ContentResolver cr, string provider, bool enabled);
```

### Type Changed: Android.Provider.Settings.System

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri DefaultAlarmAlertUri { get; set; }
	public static Android.Net.Uri DefaultNotificationUri { get; set; }
	public static Android.Net.Uri DefaultRingtoneUri { get; set; }
	public static System.Collections.Generic.IList<string> VolumeSettings { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri DefaultAlarmAlertUri { get; }
	public static Android.Net.Uri DefaultNotificationUri { get; }
	public static Android.Net.Uri DefaultRingtoneUri { get; }
	public static System.Collections.Generic.IList<string> VolumeSettings { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static bool GetShowGTalkServiceStatus (Android.Content.ContentResolver cr);

	[Obsolete ("deprecated")]
	public static void SetShowGTalkServiceStatus (Android.Content.ContentResolver cr, bool flag);
```

### Type Changed: Android.Provider.Telephony

### Type Changed: Android.Provider.Telephony.Carriers

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Mms

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ReportRequestUri { get; set; }
	public static Android.Net.Uri ReportStatusUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ReportRequestUri { get; }
	public static Android.Net.Uri ReportStatusUri { get; }
```

### Type Changed: Android.Provider.Telephony.Draft

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Inbox

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Outbox

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Rate

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Sent

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.MmsSms

Removed properties:

```
public static Android.Net.Uri ContentConversationsUri { get; set; }
	public static Android.Net.Uri ContentDraftUri { get; set; }
	public static Android.Net.Uri ContentFilterByphoneUri { get; set; }
	public static Android.Net.Uri ContentLockedUri { get; set; }
	public static Android.Net.Uri ContentUndeliveredUri { get; set; }
	public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri SearchUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentConversationsUri { get; }
	public static Android.Net.Uri ContentDraftUri { get; }
	public static Android.Net.Uri ContentFilterByphoneUri { get; }
	public static Android.Net.Uri ContentLockedUri { get; }
	public static Android.Net.Uri ContentUndeliveredUri { get; }
	public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri SearchUri { get; }
```

### Type Changed: Android.Provider.Telephony.PendingMessages

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Sms

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Conversations

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Draft

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Inbox

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Outbox

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Sent

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.Telephony.Threads

Removed properties:

```
public static Android.Net.Uri ContentUri { get; set; }
	public static Android.Net.Uri ObsoleteThreadsUri { get; set; }
```

Added properties:

```
public static Android.Net.Uri ContentUri { get; }
	public static Android.Net.Uri ObsoleteThreadsUri { get; }
```

### Type Changed: Android.Provider.UserDictionary

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.UserDictionary.Words

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static void AddWord (Android.Content.Context context, string word, int frequency, LocaleType localeType);
```

### Type Changed: Android.Provider.VoicemailContract

### Type Changed: Android.Provider.VoicemailContract.Status

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

### Type Changed: Android.Provider.VoicemailContract.Voicemails

Removed property:

```
public static Android.Net.Uri ContentUri { get; set; }
```

Added property:

```
public static Android.Net.Uri ContentUri { get; }
```

## Namespace Android.Renderscripts

### Type Changed: Android.Renderscripts.Allocation

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void Resize (int dimX);
```

### Type Changed: Android.Renderscripts.Allocation.MipmapControl

Removed properties:

```
public static Allocation.MipmapControl MipmapFull { get; set; }
	public static Allocation.MipmapControl MipmapNone { get; set; }
	public static Allocation.MipmapControl MipmapOnSyncToTexture { get; set; }
```

Added properties:

```
public static Allocation.MipmapControl MipmapFull { get; }
	public static Allocation.MipmapControl MipmapNone { get; }
	public static Allocation.MipmapControl MipmapOnSyncToTexture { get; }
```

### Type Changed: Android.Renderscripts.Element

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static Element MATRIX4X4 (RenderScript rs);
```

### Type Changed: Android.Renderscripts.Element.DataKind

Removed properties:

```
public static Element.DataKind PixelA { get; set; }
	public static Element.DataKind PixelDepth { get; set; }
	public static Element.DataKind PixelL { get; set; }
	public static Element.DataKind PixelLa { get; set; }
	public static Element.DataKind PixelRgb { get; set; }
	public static Element.DataKind PixelRgba { get; set; }
	public static Element.DataKind PixelYuv { get; set; }
	public static Element.DataKind User { get; set; }
```

Added properties:

```
public static Element.DataKind PixelA { get; }
	public static Element.DataKind PixelDepth { get; }
	public static Element.DataKind PixelL { get; }
	public static Element.DataKind PixelLa { get; }
	public static Element.DataKind PixelRgb { get; }
	public static Element.DataKind PixelRgba { get; }
	public static Element.DataKind PixelYuv { get; }
	public static Element.DataKind User { get; }
```

### Type Changed: Android.Renderscripts.Element.DataType

Removed properties:

```
public static Element.DataType Boolean { get; set; }
	public static Element.DataType Float32 { get; set; }
	public static Element.DataType Float64 { get; set; }
	public static Element.DataType Matrix2x2 { get; set; }
	public static Element.DataType Matrix3x3 { get; set; }
	public static Element.DataType Matrix4x4 { get; set; }
	public static Element.DataType None { get; set; }
	public static Element.DataType RsAllocation { get; set; }
	public static Element.DataType RsElement { get; set; }
	public static Element.DataType RsFont { get; set; }
	public static Element.DataType RsMesh { get; set; }
	public static Element.DataType RsProgramFragment { get; set; }
	public static Element.DataType RsProgramRaster { get; set; }
	public static Element.DataType RsProgramStore { get; set; }
	public static Element.DataType RsProgramVertex { get; set; }
	public static Element.DataType RsSampler { get; set; }
	public static Element.DataType RsScript { get; set; }
	public static Element.DataType RsType { get; set; }
	public static Element.DataType Signed16 { get; set; }
	public static Element.DataType Signed32 { get; set; }
	public static Element.DataType Signed64 { get; set; }
	public static Element.DataType Signed8 { get; set; }
	public static Element.DataType Unsigned16 { get; set; }
	public static Element.DataType Unsigned32 { get; set; }
	public static Element.DataType Unsigned4444 { get; set; }
	public static Element.DataType Unsigned5551 { get; set; }
	public static Element.DataType Unsigned565 { get; set; }
	public static Element.DataType Unsigned64 { get; set; }
	public static Element.DataType Unsigned8 { get; set; }
```

Added properties:

```
public static Element.DataType Boolean { get; }
	public static Element.DataType Float32 { get; }
	public static Element.DataType Float64 { get; }
	public static Element.DataType Matrix2x2 { get; }
	public static Element.DataType Matrix3x3 { get; }
	public static Element.DataType Matrix4x4 { get; }
	public static Element.DataType None { get; }
	public static Element.DataType RsAllocation { get; }
	public static Element.DataType RsElement { get; }
	public static Element.DataType RsFont { get; }
	public static Element.DataType RsMesh { get; }
	public static Element.DataType RsProgramFragment { get; }
	public static Element.DataType RsProgramRaster { get; }
	public static Element.DataType RsProgramStore { get; }
	public static Element.DataType RsProgramVertex { get; }
	public static Element.DataType RsSampler { get; }
	public static Element.DataType RsScript { get; }
	public static Element.DataType RsType { get; }
	public static Element.DataType Signed16 { get; }
	public static Element.DataType Signed32 { get; }
	public static Element.DataType Signed64 { get; }
	public static Element.DataType Signed8 { get; }
	public static Element.DataType Unsigned16 { get; }
	public static Element.DataType Unsigned32 { get; }
	public static Element.DataType Unsigned4444 { get; }
	public static Element.DataType Unsigned5551 { get; }
	public static Element.DataType Unsigned565 { get; }
	public static Element.DataType Unsigned64 { get; }
	public static Element.DataType Unsigned8 { get; }
```

### Type Changed: Android.Renderscripts.FileA3D

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static FileA3D CreateFromAsset (RenderScript rs, Android.Content.Res.AssetManager mgr, string path);

	[Obsolete ("deprecated")]
	public static FileA3D CreateFromFile (RenderScript rs, Java.IO.File path);

	[Obsolete ("deprecated")]
	public static FileA3D CreateFromFile (RenderScript rs, string path);

	[Obsolete ("deprecated")]
	public static FileA3D CreateFromResource (RenderScript rs, Android.Content.Res.Resources res, int id);

	[Obsolete ("deprecated")]
	public virtual FileA3D.IndexEntry GetIndexEntry (int index);
```

### Type Changed: Android.Renderscripts.FileA3D.EntryType

Removed properties:

```
public static FileA3D.EntryType Mesh { get; set; }
	public static FileA3D.EntryType Unknown { get; set; }
```

Added properties:

```
public static FileA3D.EntryType Mesh { get; }
	public static FileA3D.EntryType Unknown { get; }
```

### Type Changed: Android.Renderscripts.Font

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static Font Create (RenderScript rs, Android.Content.Res.Resources res, string familyName, Font.Style fontStyle, float pointSize);

	[Obsolete ("deprecated")]
	public static Font CreateFromAsset (RenderScript rs, Android.Content.Res.Resources res, string path, float pointSize);

	[Obsolete ("deprecated")]
	public static Font CreateFromFile (RenderScript rs, Android.Content.Res.Resources res, Java.IO.File path, float pointSize);

	[Obsolete ("deprecated")]
	public static Font CreateFromFile (RenderScript rs, Android.Content.Res.Resources res, string path, float pointSize);

	[Obsolete ("deprecated")]
	public static Font CreateFromResource (RenderScript rs, Android.Content.Res.Resources res, int id, float pointSize);
```

### Type Changed: Android.Renderscripts.Font.Style

Removed properties:

```
public static Font.Style Bold { get; set; }
	public static Font.Style BoldItalic { get; set; }
	public static Font.Style Italic { get; set; }
	public static Font.Style Normal { get; set; }
```

Added properties:

```
public static Font.Style Bold { get; }
	public static Font.Style BoldItalic { get; }
	public static Font.Style Italic { get; }
	public static Font.Style Normal { get; }
```

### Type Changed: Android.Renderscripts.Mesh

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Allocation GetIndexSetAllocation (int slot);

	[Obsolete ("deprecated")]
	public virtual Mesh.Primitive GetPrimitive (int slot);

	[Obsolete ("deprecated")]
	public virtual Allocation GetVertexAllocation (int slot);
```

### Type Changed: Android.Renderscripts.Mesh.AllocationBuilder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Mesh.AllocationBuilder AddIndexSetAllocation (Allocation a, Mesh.Primitive p);

	[Obsolete ("deprecated")]
	public virtual Mesh.AllocationBuilder AddIndexSetType (Mesh.Primitive p);

	[Obsolete ("deprecated")]
	public virtual Mesh.AllocationBuilder AddVertexAllocation (Allocation a);

	[Obsolete ("deprecated")]
	public virtual Mesh Create ();
```

### Type Changed: Android.Renderscripts.Mesh.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Mesh.Builder AddIndexSetType (Element e, int size, Mesh.Primitive p);

	[Obsolete ("deprecated")]
	public virtual Mesh.Builder AddIndexSetType (Mesh.Primitive p);

	[Obsolete ("deprecated")]
	public virtual Mesh.Builder AddIndexSetType (Type t, Mesh.Primitive p);

	[Obsolete ("deprecated")]
	public virtual Mesh.Builder AddVertexType (Element e, int size);

	[Obsolete ("deprecated")]
	public virtual Mesh.Builder AddVertexType (Type t);

	[Obsolete ("deprecated")]
	public virtual Mesh Create ();
```

### Type Changed: Android.Renderscripts.Mesh.Primitive

Removed properties:

```
public static Mesh.Primitive Line { get; set; }
	public static Mesh.Primitive LineStrip { get; set; }
	public static Mesh.Primitive Point { get; set; }
	public static Mesh.Primitive Triangle { get; set; }
	public static Mesh.Primitive TriangleFan { get; set; }
	public static Mesh.Primitive TriangleStrip { get; set; }
```

Added properties:

```
public static Mesh.Primitive Line { get; }
	public static Mesh.Primitive LineStrip { get; }
	public static Mesh.Primitive Point { get; }
	public static Mesh.Primitive Triangle { get; }
	public static Mesh.Primitive TriangleFan { get; }
	public static Mesh.Primitive TriangleStrip { get; }
```

### Type Changed: Android.Renderscripts.Mesh.TriangleMeshBuilder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder AddTriangle (int idx1, int idx2, int idx3);

	[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder AddVertex (float x, float y);

	[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder AddVertex (float x, float y, float z);

	[Obsolete ("deprecated")]
	public virtual Mesh Create (bool uploadToBufferObject);

	[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder SetColor (float r, float g, float b, float a);

	[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder SetNormal (float x, float y, float z);

	[Obsolete ("deprecated")]
	public virtual Mesh.TriangleMeshBuilder SetTexture (float s, float t);
```

### Type Changed: Android.Renderscripts.Program

### Type Changed: Android.Renderscripts.Program.TextureType

Removed properties:

```
public static Program.TextureType Texture2d { get; set; }
	public static Program.TextureType TextureCube { get; set; }
```

Added properties:

```
public static Program.TextureType Texture2d { get; }
	public static Program.TextureType TextureCube { get; }
```

### Type Changed: Android.Renderscripts.ProgramFragment

### Type Changed: Android.Renderscripts.ProgramFragment.Builder

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual ProgramFragment Create ();
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual ProgramFragmentFixedFunction Create ();

	[Obsolete ("deprecated")]
	public virtual ProgramFragmentFixedFunction.Builder SetPointSpriteTexCoordinateReplacement (bool enable);

	[Obsolete ("deprecated")]
	public virtual ProgramFragmentFixedFunction.Builder SetTexture (ProgramFragmentFixedFunction.Builder.EnvMode env, ProgramFragmentFixedFunction.Builder.Format fmt, int slot);

	[Obsolete ("deprecated")]
	public virtual ProgramFragmentFixedFunction.Builder SetVaryingColor (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.EnvMode

Removed properties:

```
public static ProgramFragmentFixedFunction.Builder.EnvMode Decal { get; set; }
	public static ProgramFragmentFixedFunction.Builder.EnvMode Modulate { get; set; }
	public static ProgramFragmentFixedFunction.Builder.EnvMode Replace { get; set; }
```

Added properties:

```
public static ProgramFragmentFixedFunction.Builder.EnvMode Decal { get; }
	public static ProgramFragmentFixedFunction.Builder.EnvMode Modulate { get; }
	public static ProgramFragmentFixedFunction.Builder.EnvMode Replace { get; }
```

### Type Changed: Android.Renderscripts.ProgramFragmentFixedFunction.Format

Removed properties:

```
public static ProgramFragmentFixedFunction.Builder.Format Alpha { get; set; }
	public static ProgramFragmentFixedFunction.Builder.Format LuminanceAlpha { get; set; }
	public static ProgramFragmentFixedFunction.Builder.Format Rgb { get; set; }
	public static ProgramFragmentFixedFunction.Builder.Format Rgba { get; set; }
```

Added properties:

```
public static ProgramFragmentFixedFunction.Builder.Format Alpha { get; }
	public static ProgramFragmentFixedFunction.Builder.Format LuminanceAlpha { get; }
	public static ProgramFragmentFixedFunction.Builder.Format Rgb { get; }
	public static ProgramFragmentFixedFunction.Builder.Format Rgba { get; }
```

### Type Changed: Android.Renderscripts.ProgramRaster

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static ProgramRaster CULL_BACK (RenderScript rs);

	[Obsolete ("deprecated")]
	public static ProgramRaster CULL_FRONT (RenderScript rs);

	[Obsolete ("deprecated")]
	public static ProgramRaster CULL_NONE (RenderScript rs);

	[Obsolete ("deprecated")]
	public virtual ProgramRaster.CullMode GetCullMode ();
```

### Type Changed: Android.Renderscripts.ProgramRaster.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual ProgramRaster Create ();

	[Obsolete ("deprecated")]
	public virtual ProgramRaster.Builder SetCullMode (ProgramRaster.CullMode m);

	[Obsolete ("deprecated")]
	public virtual ProgramRaster.Builder SetPointSpriteEnabled (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramRaster.CullMode

Removed properties:

```
public static ProgramRaster.CullMode Back { get; set; }
	public static ProgramRaster.CullMode Front { get; set; }
	public static ProgramRaster.CullMode None { get; set; }
```

Added properties:

```
public static ProgramRaster.CullMode Back { get; }
	public static ProgramRaster.CullMode Front { get; }
	public static ProgramRaster.CullMode None { get; }
```

### Type Changed: Android.Renderscripts.ProgramStore

### Type Changed: Android.Renderscripts.ProgramStore.BlendDstFunc

Removed properties:

```
public static ProgramStore.BlendDstFunc DstAlpha { get; set; }
	public static ProgramStore.BlendDstFunc One { get; set; }
	public static ProgramStore.BlendDstFunc OneMinusDstAlpha { get; set; }
	public static ProgramStore.BlendDstFunc OneMinusSrcAlpha { get; set; }
	public static ProgramStore.BlendDstFunc OneMinusSrcColor { get; set; }
	public static ProgramStore.BlendDstFunc SrcAlpha { get; set; }
	public static ProgramStore.BlendDstFunc SrcColor { get; set; }
	public static ProgramStore.BlendDstFunc Zero { get; set; }
```

Added properties:

```
public static ProgramStore.BlendDstFunc DstAlpha { get; }
	public static ProgramStore.BlendDstFunc One { get; }
	public static ProgramStore.BlendDstFunc OneMinusDstAlpha { get; }
	public static ProgramStore.BlendDstFunc OneMinusSrcAlpha { get; }
	public static ProgramStore.BlendDstFunc OneMinusSrcColor { get; }
	public static ProgramStore.BlendDstFunc SrcAlpha { get; }
	public static ProgramStore.BlendDstFunc SrcColor { get; }
	public static ProgramStore.BlendDstFunc Zero { get; }
```

### Type Changed: Android.Renderscripts.ProgramStore.BlendSrcFunc

Removed properties:

```
public static ProgramStore.BlendSrcFunc DstAlpha { get; set; }
	public static ProgramStore.BlendSrcFunc DstColor { get; set; }
	public static ProgramStore.BlendSrcFunc One { get; set; }
	public static ProgramStore.BlendSrcFunc OneMinusDstAlpha { get; set; }
	public static ProgramStore.BlendSrcFunc OneMinusDstColor { get; set; }
	public static ProgramStore.BlendSrcFunc OneMinusSrcAlpha { get; set; }
	public static ProgramStore.BlendSrcFunc SrcAlpha { get; set; }
	public static ProgramStore.BlendSrcFunc SrcAlphaSaturate { get; set; }
	public static ProgramStore.BlendSrcFunc Zero { get; set; }
```

Added properties:

```
public static ProgramStore.BlendSrcFunc DstAlpha { get; }
	public static ProgramStore.BlendSrcFunc DstColor { get; }
	public static ProgramStore.BlendSrcFunc One { get; }
	public static ProgramStore.BlendSrcFunc OneMinusDstAlpha { get; }
	public static ProgramStore.BlendSrcFunc OneMinusDstColor { get; }
	public static ProgramStore.BlendSrcFunc OneMinusSrcAlpha { get; }
	public static ProgramStore.BlendSrcFunc SrcAlpha { get; }
	public static ProgramStore.BlendSrcFunc SrcAlphaSaturate { get; }
	public static ProgramStore.BlendSrcFunc Zero { get; }
```

### Type Changed: Android.Renderscripts.ProgramStore.DepthFunc

Removed properties:

```
public static ProgramStore.DepthFunc Always { get; set; }
	public static ProgramStore.DepthFunc Equal { get; set; }
	public static ProgramStore.DepthFunc Greater { get; set; }
	public static ProgramStore.DepthFunc GreaterOrEqual { get; set; }
	public static ProgramStore.DepthFunc Less { get; set; }
	public static ProgramStore.DepthFunc LessOrEqual { get; set; }
	public static ProgramStore.DepthFunc NotEqual { get; set; }
```

Added properties:

```
public static ProgramStore.DepthFunc Always { get; }
	public static ProgramStore.DepthFunc Equal { get; }
	public static ProgramStore.DepthFunc Greater { get; }
	public static ProgramStore.DepthFunc GreaterOrEqual { get; }
	public static ProgramStore.DepthFunc Less { get; }
	public static ProgramStore.DepthFunc LessOrEqual { get; }
	public static ProgramStore.DepthFunc NotEqual { get; }
```

### Type Changed: Android.Renderscripts.ProgramVertex

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual Element GetInput (int slot);
```

### Type Changed: Android.Renderscripts.ProgramVertex.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual ProgramVertex.Builder AddInput (Element e);

	[Obsolete ("deprecated")]
	public virtual ProgramVertex Create ();
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void BindConstants (ProgramVertexFixedFunction.Constants va);
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction.Builder

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual ProgramVertexFixedFunction Create ();

	[Obsolete ("deprecated")]
	public virtual ProgramVertexFixedFunction.Builder SetTextureMatrixEnable (bool enable);
```

### Type Changed: Android.Renderscripts.ProgramVertexFixedFunction.Constants

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void Destroy ();

	[Obsolete ("deprecated")]
	public virtual void SetModelview (Matrix4f m);

	[Obsolete ("deprecated")]
	public virtual void SetProjection (Matrix4f m);

	[Obsolete ("deprecated")]
	public virtual void SetTexture (Matrix4f m);
```

### Type Changed: Android.Renderscripts.RenderScript

### Type Changed: Android.Renderscripts.RenderScript.ContextType

Removed properties:

```
public static RenderScript.ContextType Debug { get; set; }
	public static RenderScript.ContextType Normal { get; set; }
	public static RenderScript.ContextType Profile { get; set; }
```

Added properties:

```
public static RenderScript.ContextType Debug { get; }
	public static RenderScript.ContextType Normal { get; }
	public static RenderScript.ContextType Profile { get; }
```

### Type Changed: Android.Renderscripts.RenderScript.Priority

Removed properties:

```
public static RenderScript.Priority Low { get; set; }
	public static RenderScript.Priority Normal { get; set; }
```

Added properties:

```
public static RenderScript.Priority Low { get; }
	public static RenderScript.Priority Normal { get; }
```

### Type Changed: Android.Renderscripts.RenderScriptGL

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void BindProgramFragment (ProgramFragment p);

	[Obsolete ("deprecated")]
	public virtual void BindProgramRaster (ProgramRaster p);

	[Obsolete ("deprecated")]
	public virtual void BindProgramStore (ProgramStore p);

	[Obsolete ("deprecated")]
	public virtual void BindProgramVertex (ProgramVertex p);

	[Obsolete ("deprecated")]
	public virtual void BindRootScript (Script s);

	[Obsolete ("deprecated")]
	public virtual void Pause ();

	[Obsolete ("deprecated")]
	public virtual void Resume ();

	[Obsolete ("deprecated")]
	public virtual void SetSurface (Android.Views.ISurfaceHolder sur, int w, int h);

	[Obsolete ("deprecated")]
	public virtual void SetSurfaceTexture (Android.Graphics.SurfaceTexture sur, int w, int h);
```

### Type Changed: Android.Renderscripts.RenderScriptGL.SurfaceConfig

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void SetAlpha (int minimum, int preferred);

	[Obsolete ("deprecated")]
	public virtual void SetColor (int minimum, int preferred);

	[Obsolete ("deprecated")]
	public virtual void SetDepth (int minimum, int preferred);

	[Obsolete ("deprecated")]
	public virtual void SetSamples (int minimum, int preferred, float Q);
```

### Type Changed: Android.Renderscripts.RSSurfaceView

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual RenderScriptGL CreateRenderScriptGL (RenderScriptGL.SurfaceConfig sc);

	[Obsolete ("deprecated")]
	public virtual void DestroyRenderScriptGL ();

	[Obsolete ("deprecated")]
	public virtual void Pause ();

	[Obsolete ("deprecated")]
	public virtual void Resume ();

	[Obsolete ("deprecated")]
	public virtual void SurfaceChanged (Android.Views.ISurfaceHolder holder, Android.Graphics.Format format, int w, int h);

	[Obsolete ("deprecated")]
	public virtual void SurfaceCreated (Android.Views.ISurfaceHolder holder);

	[Obsolete ("deprecated")]
	public virtual void SurfaceDestroyed (Android.Views.ISurfaceHolder holder);
```

### Type Changed: Android.Renderscripts.RSTextureView

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual RenderScriptGL CreateRenderScriptGL (RenderScriptGL.SurfaceConfig sc);

	[Obsolete ("deprecated")]
	public virtual void DestroyRenderScriptGL ();

	[Obsolete ("deprecated")]
	public virtual void OnSurfaceTextureAvailable (Android.Graphics.SurfaceTexture surface, int width, int height);

	[Obsolete ("deprecated")]
	public virtual bool OnSurfaceTextureDestroyed (Android.Graphics.SurfaceTexture surface);

	[Obsolete ("deprecated")]
	public virtual void OnSurfaceTextureSizeChanged (Android.Graphics.SurfaceTexture surface, int width, int height);

	[Obsolete ("deprecated")]
	public virtual void OnSurfaceTextureUpdated (Android.Graphics.SurfaceTexture surface);

	[Obsolete ("deprecated")]
	public virtual void Pause ();

	[Obsolete ("deprecated")]
	public virtual void Resume ();
```

### Type Changed: Android.Renderscripts.Sampler

### Type Changed: Android.Renderscripts.Sampler.Value

Removed properties:

```
public static Sampler.Value Clamp { get; set; }
	public static Sampler.Value Linear { get; set; }
	public static Sampler.Value LinearMipLinear { get; set; }
	public static Sampler.Value LinearMipNearest { get; set; }
	public static Sampler.Value MirroredRepeat { get; set; }
	public static Sampler.Value Nearest { get; set; }
	public static Sampler.Value Wrap { get; set; }
```

Added properties:

```
public static Sampler.Value Clamp { get; }
	public static Sampler.Value Linear { get; }
	public static Sampler.Value LinearMipLinear { get; }
	public static Sampler.Value LinearMipNearest { get; }
	public static Sampler.Value MirroredRepeat { get; }
	public static Sampler.Value Nearest { get; }
	public static Sampler.Value Wrap { get; }
```

### Type Changed: Android.Renderscripts.ScriptIntrinsicColorMatrix

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static ScriptIntrinsicColorMatrix Create (RenderScript rs, Element e);
```

### Type Changed: Android.Renderscripts.Type

### Type Changed: Android.Renderscripts.Type.CubemapFace

Removed properties:

```
public static Type.CubemapFace NegativeX { get; set; }
	public static Type.CubemapFace NegativeY { get; set; }
	public static Type.CubemapFace NegativeZ { get; set; }
	public static Type.CubemapFace PositiveX { get; set; }
	public static Type.CubemapFace PositiveY { get; set; }
	public static Type.CubemapFace PositiveZ { get; set; }
	public static Type.CubemapFace PositveX { get; set; }
	public static Type.CubemapFace PositveY { get; set; }
	public static Type.CubemapFace PositveZ { get; set; }
```

Added properties:

```
public static Type.CubemapFace NegativeX { get; }
	public static Type.CubemapFace NegativeY { get; }
	public static Type.CubemapFace NegativeZ { get; }
	public static Type.CubemapFace PositiveX { get; }
	public static Type.CubemapFace PositiveY { get; }
	public static Type.CubemapFace PositiveZ { get; }
	public static Type.CubemapFace PositveX { get; }
	public static Type.CubemapFace PositveY { get; }
	public static Type.CubemapFace PositveZ { get; }
```

## Namespace Android.Runtime

### Type Changed: Android.Runtime.JNIEnv

Added methods:

```
public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static bool CallBooleanMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static sbyte CallByteMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static char CallCharMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static double CallDoubleMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static float CallFloatMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static int CallIntMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static long CallLongMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static bool CallNonvirtualBooleanMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static sbyte CallNonvirtualByteMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static char CallNonvirtualCharMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static double CallNonvirtualDoubleMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static float CallNonvirtualFloatMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static int CallNonvirtualIntMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static long CallNonvirtualLongMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static System.IntPtr CallNonvirtualObjectMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static short CallNonvirtualShortMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static void CallNonvirtualVoidMethod (System.IntPtr jobject, System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static System.IntPtr CallObjectMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static short CallShortMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static bool CallStaticBooleanMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static sbyte CallStaticByteMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static char CallStaticCharMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static double CallStaticDoubleMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static float CallStaticFloatMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static int CallStaticIntMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static long CallStaticLongMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static System.IntPtr CallStaticObjectMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static short CallStaticShortMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static void CallStaticVoidMethod (System.IntPtr jclass, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7, JValue parms8, JValue parms9, JValue parms10, JValue parms11, JValue parms12, JValue parms13, JValue parms14);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6, JValue parms7);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2, JValue parms3, JValue parms4, JValue parms5, JValue parms6);
	public static void CallVoidMethod (System.IntPtr jobject, System.IntPtr jmethod, JValue parms0, JValue parms1, JValue parms2);
```

## Namespace Android.Service.Notification

### Type Changed: Android.Service.Notification.NotificationListenerService

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void CancelNotification (string pkg, string tag, int id);
```

### Type Changed: Android.Service.Notification.NotificationListenerService.RankingMap

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Service.Notification.StatusBarNotification

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Speech.Tts

### Type Changed: Android.Speech.Tts.TextToSpeech

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual OperationResult AddEarcon (string earcon, string filename);

	[Obsolete ("deprecated")]
	public virtual bool AreDefaultsEnforced ();

	[Obsolete ("deprecated")]
	public virtual System.Collections.Generic.ICollection<string> GetFeatures (Java.Util.Locale locale);

	[Obsolete ("deprecated")]
	public virtual OperationResult PlayEarcon (string earcon, QueueMode queueMode, System.Collections.Generic.IDictionary<System.String,System.String> params);

	[Obsolete ("deprecated")]
	public virtual OperationResult PlaySilence (long durationInMs, QueueMode queueMode, System.Collections.Generic.IDictionary<System.String,System.String> params);

	[Obsolete ("deprecated")]
	public virtual OperationResult SetEngineByPackageName (string enginePackageName);

	[Obsolete ("deprecated")]
	public virtual OperationResult SetOnUtteranceCompletedListener (TextToSpeech.IOnUtteranceCompletedListener listener);

	[Obsolete ("deprecated")]
	public virtual OperationResult Speak (string text, QueueMode queueMode, System.Collections.Generic.IDictionary<System.String,System.String> params);

	[Obsolete ("deprecated")]
	public virtual OperationResult SynthesizeToFile (string text, System.Collections.Generic.IDictionary<System.String,System.String> params, string filename);
```

### Type Changed: Android.Speech.Tts.Voice

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Systems

### Type Changed: Android.Systems.OsConstants

Removed properties:

```
public static int AfInet { get; set; }
	public static int AfInet6 { get; set; }
	public static int AfUnix { get; set; }
	public static int AfUnspec { get; set; }
	public static int AiAddrconfig { get; set; }
	public static int AiAll { get; set; }
	public static int AiCanonname { get; set; }
	public static int AiNumerichost { get; set; }
	public static int AiNumericserv { get; set; }
	public static int AiPassive { get; set; }
	public static int AiV4mapped { get; set; }
	public static int CapAuditControl { get; set; }
	public static int CapAuditWrite { get; set; }
	public static int CapBlockSuspend { get; set; }
	public static int CapChown { get; set; }
	public static int CapDacOverride { get; set; }
	public static int CapDacReadSearch { get; set; }
	public static int CapFowner { get; set; }
	public static int CapFsetid { get; set; }
	public static int CapIpcLock { get; set; }
	public static int CapIpcOwner { get; set; }
	public static int CapKill { get; set; }
	public static int CapLastCap { get; set; }
	public static int CapLease { get; set; }
	public static int CapLinuxImmutable { get; set; }
	public static int CapMacAdmin { get; set; }
	public static int CapMacOverride { get; set; }
	public static int CapMknod { get; set; }
	public static int CapNetAdmin { get; set; }
	public static int CapNetBindService { get; set; }
	public static int CapNetBroadcast { get; set; }
	public static int CapNetRaw { get; set; }
	public static int CapSetfcap { get; set; }
	public static int CapSetgid { get; set; }
	public static int CapSetpcap { get; set; }
	public static int CapSetuid { get; set; }
	public static int CapSysAdmin { get; set; }
	public static int CapSysBoot { get; set; }
	public static int CapSysChroot { get; set; }
	public static int CapSyslog { get; set; }
	public static int CapSysModule { get; set; }
	public static int CapSysNice { get; set; }
	public static int CapSysPacct { get; set; }
	public static int CapSysPtrace { get; set; }
	public static int CapSysRawio { get; set; }
	public static int CapSysResource { get; set; }
	public static int CapSysTime { get; set; }
	public static int CapSysTtyConfig { get; set; }
	public static int CapWakeAlarm { get; set; }
	public static int E2big { get; set; }
	public static int Eacces { get; set; }
	public static int Eaddrinuse { get; set; }
	public static int Eaddrnotavail { get; set; }
	public static int Eafnosupport { get; set; }
	public static int Eagain { get; set; }
	public static int EaiAgain { get; set; }
	public static int EaiBadflags { get; set; }
	public static int EaiFail { get; set; }
	public static int EaiFamily { get; set; }
	public static int EaiMemory { get; set; }
	public static int EaiNodata { get; set; }
	public static int EaiNoname { get; set; }
	public static int EaiOverflow { get; set; }
	public static int EaiService { get; set; }
	public static int EaiSocktype { get; set; }
	public static int EaiSystem { get; set; }
	public static int Ealready { get; set; }
	public static int Ebadf { get; set; }
	public static int Ebadmsg { get; set; }
	public static int Ebusy { get; set; }
	public static int Ecanceled { get; set; }
	public static int Echild { get; set; }
	public static int Econnaborted { get; set; }
	public static int Econnrefused { get; set; }
	public static int Econnreset { get; set; }
	public static int Edeadlk { get; set; }
	public static int Edestaddrreq { get; set; }
	public static int Edom { get; set; }
	public static int Edquot { get; set; }
	public static int Eexist { get; set; }
	public static int Efault { get; set; }
	public static int Efbig { get; set; }
	public static int Ehostunreach { get; set; }
	public static int Eidrm { get; set; }
	public static int Eilseq { get; set; }
	public static int Einprogress { get; set; }
	public static int Eintr { get; set; }
	public static int Einval { get; set; }
	public static int Eio { get; set; }
	public static int Eisconn { get; set; }
	public static int Eisdir { get; set; }
	public static int Eloop { get; set; }
	public static int Emfile { get; set; }
	public static int Emlink { get; set; }
	public static int Emsgsize { get; set; }
	public static int Emultihop { get; set; }
	public static int Enametoolong { get; set; }
	public static int Enetdown { get; set; }
	public static int Enetreset { get; set; }
	public static int Enetunreach { get; set; }
	public static int Enfile { get; set; }
	public static int Enobufs { get; set; }
	public static int Enodata { get; set; }
	public static int Enodev { get; set; }
	public static int Enoent { get; set; }
	public static int Enoexec { get; set; }
	public static int Enolck { get; set; }
	public static int Enolink { get; set; }
	public static int Enomem { get; set; }
	public static int Enomsg { get; set; }
	public static int Enoprotoopt { get; set; }
	public static int Enospc { get; set; }
	public static int Enosr { get; set; }
	public static int Enostr { get; set; }
	public static int Enosys { get; set; }
	public static int Enotconn { get; set; }
	public static int Enotdir { get; set; }
	public static int Enotempty { get; set; }
	public static int Enotsock { get; set; }
	public static int Enotsup { get; set; }
	public static int Enotty { get; set; }
	public static int Enxio { get; set; }
	public static int Eopnotsupp { get; set; }
	public static int Eoverflow { get; set; }
	public static int Eperm { get; set; }
	public static int Epipe { get; set; }
	public static int Eproto { get; set; }
	public static int Eprotonosupport { get; set; }
	public static int Eprototype { get; set; }
	public static int Erange { get; set; }
	public static int Erofs { get; set; }
	public static int Espipe { get; set; }
	public static int Esrch { get; set; }
	public static int Estale { get; set; }
	public static int Etime { get; set; }
	public static int Etimedout { get; set; }
	public static int Etxtbsy { get; set; }
	public static int Exdev { get; set; }
	public static int ExitFailure { get; set; }
	public static int ExitSuccess { get; set; }
	public static int FdCloexec { get; set; }
	public static int FDupfd { get; set; }
	public static int FGetfd { get; set; }
	public static int FGetfl { get; set; }
	public static int FGetlk { get; set; }
	public static int FGetlk64 { get; set; }
	public static int FGetown { get; set; }
	public static int Fionread { get; set; }
	public static int FOk { get; set; }
	public static int FRdlck { get; set; }
	public static int FSetfd { get; set; }
	public static int FSetfl { get; set; }
	public static int FSetlk { get; set; }
	public static int FSetlk64 { get; set; }
	public static int FSetlkw { get; set; }
	public static int FSetlkw64 { get; set; }
	public static int FSetown { get; set; }
	public static int FUnlck { get; set; }
	public static int FWrlck { get; set; }
	public static int IfaFDadfailed { get; set; }
	public static int IfaFDeprecated { get; set; }
	public static int IfaFHomeaddress { get; set; }
	public static int IfaFNodad { get; set; }
	public static int IfaFOptimistic { get; set; }
	public static int IfaFPermanent { get; set; }
	public static int IfaFSecondary { get; set; }
	public static int IfaFTemporary { get; set; }
	public static int IfaFTentative { get; set; }
	public static int IffAllmulti { get; set; }
	public static int IffAutomedia { get; set; }
	public static int IffBroadcast { get; set; }
	public static int IffDebug { get; set; }
	public static int IffDynamic { get; set; }
	public static int IffLoopback { get; set; }
	public static int IffMaster { get; set; }
	public static int IffMulticast { get; set; }
	public static int IffNoarp { get; set; }
	public static int IffNotrailers { get; set; }
	public static int IffPointopoint { get; set; }
	public static int IffPortsel { get; set; }
	public static int IffPromisc { get; set; }
	public static int IffRunning { get; set; }
	public static int IffSlave { get; set; }
	public static int IffUp { get; set; }
	public static int IpMulticastIf { get; set; }
	public static int IpMulticastLoop { get; set; }
	public static int IpMulticastTtl { get; set; }
	public static int IpprotoIcmp { get; set; }
	public static int IpprotoIcmpv6 { get; set; }
	public static int IpprotoIp { get; set; }
	public static int IpprotoIpv6 { get; set; }
	public static int IpprotoRaw { get; set; }
	public static int IpprotoTcp { get; set; }
	public static int IpprotoUdp { get; set; }
	public static int IpTos { get; set; }
	public static int IpTtl { get; set; }
	public static int Ipv6Checksum { get; set; }
	public static int Ipv6MulticastHops { get; set; }
	public static int Ipv6MulticastIf { get; set; }
	public static int Ipv6MulticastLoop { get; set; }
	public static int Ipv6Recvdstopts { get; set; }
	public static int Ipv6Recvhoplimit { get; set; }
	public static int Ipv6Recvhopopts { get; set; }
	public static int Ipv6Recvpktinfo { get; set; }
	public static int Ipv6Recvrthdr { get; set; }
	public static int Ipv6Recvtclass { get; set; }
	public static int Ipv6Tclass { get; set; }
	public static int Ipv6UnicastHops { get; set; }
	public static int Ipv6V6only { get; set; }
	public static int MapFixed { get; set; }
	public static int MapPrivate { get; set; }
	public static int MapShared { get; set; }
	public static int McastBlockSource { get; set; }
	public static int McastJoinGroup { get; set; }
	public static int McastJoinSourceGroup { get; set; }
	public static int McastLeaveGroup { get; set; }
	public static int McastLeaveSourceGroup { get; set; }
	public static int McastUnblockSource { get; set; }
	public static int MclCurrent { get; set; }
	public static int MclFuture { get; set; }
	public static int MsAsync { get; set; }
	public static int MsgCtrunc { get; set; }
	public static int MsgDontroute { get; set; }
	public static int MsgEor { get; set; }
	public static int MsgOob { get; set; }
	public static int MsgPeek { get; set; }
	public static int MsgTrunc { get; set; }
	public static int MsgWaitall { get; set; }
	public static int MsInvalidate { get; set; }
	public static int MsSync { get; set; }
	public static int NiDgram { get; set; }
	public static int NiNamereqd { get; set; }
	public static int NiNofqdn { get; set; }
	public static int NiNumerichost { get; set; }
	public static int NiNumericserv { get; set; }
	public static int OAccmode { get; set; }
	public static int OAppend { get; set; }
	public static int OCreat { get; set; }
	public static int OExcl { get; set; }
	public static int ONoctty { get; set; }
	public static int ONofollow { get; set; }
	public static int ONonblock { get; set; }
	public static int ORdonly { get; set; }
	public static int ORdwr { get; set; }
	public static int OSync { get; set; }
	public static int OTrunc { get; set; }
	public static int OWronly { get; set; }
	public static int Pollerr { get; set; }
	public static int Pollhup { get; set; }
	public static int Pollin { get; set; }
	public static int Pollnval { get; set; }
	public static int Pollout { get; set; }
	public static int Pollpri { get; set; }
	public static int Pollrdband { get; set; }
	public static int Pollrdnorm { get; set; }
	public static int Pollwrband { get; set; }
	public static int Pollwrnorm { get; set; }
	public static int PrGetDumpable { get; set; }
	public static int ProtExec { get; set; }
	public static int ProtNone { get; set; }
	public static int ProtRead { get; set; }
	public static int ProtWrite { get; set; }
	public static int PrSetDumpable { get; set; }
	public static int PrSetNoNewPrivs { get; set; }
	public static int ROk { get; set; }
	public static int RtScopeHost { get; set; }
	public static int RtScopeLink { get; set; }
	public static int RtScopeNowhere { get; set; }
	public static int RtScopeSite { get; set; }
	public static int RtScopeUniverse { get; set; }
	public static int Sc2CBind { get; set; }
	public static int Sc2CDev { get; set; }
	public static int Sc2CharTerm { get; set; }
	public static int Sc2CVersion { get; set; }
	public static int Sc2FortDev { get; set; }
	public static int Sc2FortRun { get; set; }
	public static int Sc2Localedef { get; set; }
	public static int Sc2SwDev { get; set; }
	public static int Sc2Upe { get; set; }
	public static int Sc2Version { get; set; }
	public static int ScAioListioMax { get; set; }
	public static int ScAioMax { get; set; }
	public static int ScAioPrioDeltaMax { get; set; }
	public static int ScArgMax { get; set; }
	public static int ScAsynchronousIo { get; set; }
	public static int ScAtexitMax { get; set; }
	public static int ScAvphysPages { get; set; }
	public static int ScBcBaseMax { get; set; }
	public static int ScBcDimMax { get; set; }
	public static int ScBcScaleMax { get; set; }
	public static int ScBcStringMax { get; set; }
	public static int ScChildMax { get; set; }
	public static int ScClkTck { get; set; }
	public static int ScCollWeightsMax { get; set; }
	public static int ScDelaytimerMax { get; set; }
	public static int ScExprNestMax { get; set; }
	public static int ScFsync { get; set; }
	public static int ScGetgrRSizeMax { get; set; }
	public static int ScGetpwRSizeMax { get; set; }
	public static int ScIovMax { get; set; }
	public static int ScJobControl { get; set; }
	public static int ScLineMax { get; set; }
	public static int ScLoginNameMax { get; set; }
	public static int ScMappedFiles { get; set; }
	public static int ScMemlock { get; set; }
	public static int ScMemlockRange { get; set; }
	public static int ScMemoryProtection { get; set; }
	public static int ScMessagePassing { get; set; }
	public static int ScMqOpenMax { get; set; }
	public static int ScMqPrioMax { get; set; }
	public static int ScNgroupsMax { get; set; }
	public static int ScNprocessorsConf { get; set; }
	public static int ScNprocessorsOnln { get; set; }
	public static int ScOpenMax { get; set; }
	public static int ScPagesize { get; set; }
	public static int ScPageSize { get; set; }
	public static int ScPassMax { get; set; }
	public static int ScPhysPages { get; set; }
	public static int ScPrioritizedIo { get; set; }
	public static int ScPriorityScheduling { get; set; }
	public static int ScRealtimeSignals { get; set; }
	public static int ScReDupMax { get; set; }
	public static int ScRtsigMax { get; set; }
	public static int ScSavedIds { get; set; }
	public static int ScSemaphores { get; set; }
	public static int ScSemNsemsMax { get; set; }
	public static int ScSemValueMax { get; set; }
	public static int ScSharedMemoryObjects { get; set; }
	public static int ScSigqueueMax { get; set; }
	public static int ScStreamMax { get; set; }
	public static int ScSynchronizedIo { get; set; }
	public static int ScThreadAttrStackaddr { get; set; }
	public static int ScThreadAttrStacksize { get; set; }
	public static int ScThreadDestructorIterations { get; set; }
	public static int ScThreadKeysMax { get; set; }
	public static int ScThreadPrioInherit { get; set; }
	public static int ScThreadPrioProtect { get; set; }
	public static int ScThreadPriorityScheduling { get; set; }
	public static int ScThreads { get; set; }
	public static int ScThreadSafeFunctions { get; set; }
	public static int ScThreadStackMin { get; set; }
	public static int ScThreadThreadsMax { get; set; }
	public static int ScTimerMax { get; set; }
	public static int ScTimers { get; set; }
	public static int ScTtyNameMax { get; set; }
	public static int ScTznameMax { get; set; }
	public static int ScVersion { get; set; }
	public static int ScXbs5Ilp32Off32 { get; set; }
	public static int ScXbs5Ilp32Offbig { get; set; }
	public static int ScXbs5Lp64Off64 { get; set; }
	public static int ScXbs5LpbigOffbig { get; set; }
	public static int ScXopenCrypt { get; set; }
	public static int ScXopenEnhI18n { get; set; }
	public static int ScXopenLegacy { get; set; }
	public static int ScXopenRealtime { get; set; }
	public static int ScXopenRealtimeThreads { get; set; }
	public static int ScXopenShm { get; set; }
	public static int ScXopenUnix { get; set; }
	public static int ScXopenVersion { get; set; }
	public static int ScXopenXcuVersion { get; set; }
	public static int SeekCur { get; set; }
	public static int SeekEnd { get; set; }
	public static int SeekSet { get; set; }
	public static int ShutRd { get; set; }
	public static int ShutRdwr { get; set; }
	public static int ShutWr { get; set; }
	public static int SIfblk { get; set; }
	public static int SIfchr { get; set; }
	public static int SIfdir { get; set; }
	public static int SIfifo { get; set; }
	public static int SIflnk { get; set; }
	public static int SIfmt { get; set; }
	public static int SIfreg { get; set; }
	public static int SIfsock { get; set; }
	public static int Sigabrt { get; set; }
	public static int Sigalrm { get; set; }
	public static int Sigbus { get; set; }
	public static int Sigchld { get; set; }
	public static int Sigcont { get; set; }
	public static int Sigfpe { get; set; }
	public static int Sighup { get; set; }
	public static int Sigill { get; set; }
	public static int Sigint { get; set; }
	public static int Sigio { get; set; }
	public static int Sigkill { get; set; }
	public static int Sigpipe { get; set; }
	public static int Sigprof { get; set; }
	public static int Sigpwr { get; set; }
	public static int Sigquit { get; set; }
	public static int Sigrtmax { get; set; }
	public static int Sigrtmin { get; set; }
	public static int Sigsegv { get; set; }
	public static int Sigstkflt { get; set; }
	public static int Sigstop { get; set; }
	public static int Sigsys { get; set; }
	public static int Sigterm { get; set; }
	public static int Sigtrap { get; set; }
	public static int Sigtstp { get; set; }
	public static int Sigttin { get; set; }
	public static int Sigttou { get; set; }
	public static int Sigurg { get; set; }
	public static int Sigusr1 { get; set; }
	public static int Sigusr2 { get; set; }
	public static int Sigvtalrm { get; set; }
	public static int Sigwinch { get; set; }
	public static int Sigxcpu { get; set; }
	public static int Sigxfsz { get; set; }
	public static int Siocgifaddr { get; set; }
	public static int Siocgifbrdaddr { get; set; }
	public static int Siocgifdstaddr { get; set; }
	public static int Siocgifnetmask { get; set; }
	public static int SIrgrp { get; set; }
	public static int SIroth { get; set; }
	public static int SIrusr { get; set; }
	public static int SIrwxg { get; set; }
	public static int SIrwxo { get; set; }
	public static int SIrwxu { get; set; }
	public static int SIsgid { get; set; }
	public static int SIsuid { get; set; }
	public static int SIsvtx { get; set; }
	public static int SIwgrp { get; set; }
	public static int SIwoth { get; set; }
	public static int SIwusr { get; set; }
	public static int SIxgrp { get; set; }
	public static int SIxoth { get; set; }
	public static int SIxusr { get; set; }
	public static int SoBindtodevice { get; set; }
	public static int SoBroadcast { get; set; }
	public static int SockDgram { get; set; }
	public static int SockRaw { get; set; }
	public static int SockSeqpacket { get; set; }
	public static int SockStream { get; set; }
	public static int SoDebug { get; set; }
	public static int SoDontroute { get; set; }
	public static int SoError { get; set; }
	public static int SoKeepalive { get; set; }
	public static int SoLinger { get; set; }
	public static int SolSocket { get; set; }
	public static int SoOobinline { get; set; }
	public static int SoPasscred { get; set; }
	public static int SoPeercred { get; set; }
	public static int SoRcvbuf { get; set; }
	public static int SoRcvlowat { get; set; }
	public static int SoRcvtimeo { get; set; }
	public static int SoReuseaddr { get; set; }
	public static int SoSndbuf { get; set; }
	public static int SoSndlowat { get; set; }
	public static int SoSndtimeo { get; set; }
	public static int SoType { get; set; }
	public static int StderrFileno { get; set; }
	public static int StdinFileno { get; set; }
	public static int StdoutFileno { get; set; }
	public static int TcpNodelay { get; set; }
	public static int Wcontinued { get; set; }
	public static int Wexited { get; set; }
	public static int Wnohang { get; set; }
	public static int Wnowait { get; set; }
	public static int WOk { get; set; }
	public static int Wstopped { get; set; }
	public static int Wuntraced { get; set; }
	public static int XOk { get; set; }
```

Added properties:

```
public static int AfInet { get; }
	public static int AfInet6 { get; }
	public static int AfUnix { get; }
	public static int AfUnspec { get; }
	public static int AiAddrconfig { get; }
	public static int AiAll { get; }
	public static int AiCanonname { get; }
	public static int AiNumerichost { get; }
	public static int AiNumericserv { get; }
	public static int AiPassive { get; }
	public static int AiV4mapped { get; }
	public static int CapAuditControl { get; }
	public static int CapAuditWrite { get; }
	public static int CapBlockSuspend { get; }
	public static int CapChown { get; }
	public static int CapDacOverride { get; }
	public static int CapDacReadSearch { get; }
	public static int CapFowner { get; }
	public static int CapFsetid { get; }
	public static int CapIpcLock { get; }
	public static int CapIpcOwner { get; }
	public static int CapKill { get; }
	public static int CapLastCap { get; }
	public static int CapLease { get; }
	public static int CapLinuxImmutable { get; }
	public static int CapMacAdmin { get; }
	public static int CapMacOverride { get; }
	public static int CapMknod { get; }
	public static int CapNetAdmin { get; }
	public static int CapNetBindService { get; }
	public static int CapNetBroadcast { get; }
	public static int CapNetRaw { get; }
	public static int CapSetfcap { get; }
	public static int CapSetgid { get; }
	public static int CapSetpcap { get; }
	public static int CapSetuid { get; }
	public static int CapSysAdmin { get; }
	public static int CapSysBoot { get; }
	public static int CapSysChroot { get; }
	public static int CapSyslog { get; }
	public static int CapSysModule { get; }
	public static int CapSysNice { get; }
	public static int CapSysPacct { get; }
	public static int CapSysPtrace { get; }
	public static int CapSysRawio { get; }
	public static int CapSysResource { get; }
	public static int CapSysTime { get; }
	public static int CapSysTtyConfig { get; }
	public static int CapWakeAlarm { get; }
	public static int E2big { get; }
	public static int Eacces { get; }
	public static int Eaddrinuse { get; }
	public static int Eaddrnotavail { get; }
	public static int Eafnosupport { get; }
	public static int Eagain { get; }
	public static int EaiAgain { get; }
	public static int EaiBadflags { get; }
	public static int EaiFail { get; }
	public static int EaiFamily { get; }
	public static int EaiMemory { get; }
	public static int EaiNodata { get; }
	public static int EaiNoname { get; }
	public static int EaiOverflow { get; }
	public static int EaiService { get; }
	public static int EaiSocktype { get; }
	public static int EaiSystem { get; }
	public static int Ealready { get; }
	public static int Ebadf { get; }
	public static int Ebadmsg { get; }
	public static int Ebusy { get; }
	public static int Ecanceled { get; }
	public static int Echild { get; }
	public static int Econnaborted { get; }
	public static int Econnrefused { get; }
	public static int Econnreset { get; }
	public static int Edeadlk { get; }
	public static int Edestaddrreq { get; }
	public static int Edom { get; }
	public static int Edquot { get; }
	public static int Eexist { get; }
	public static int Efault { get; }
	public static int Efbig { get; }
	public static int Ehostunreach { get; }
	public static int Eidrm { get; }
	public static int Eilseq { get; }
	public static int Einprogress { get; }
	public static int Eintr { get; }
	public static int Einval { get; }
	public static int Eio { get; }
	public static int Eisconn { get; }
	public static int Eisdir { get; }
	public static int Eloop { get; }
	public static int Emfile { get; }
	public static int Emlink { get; }
	public static int Emsgsize { get; }
	public static int Emultihop { get; }
	public static int Enametoolong { get; }
	public static int Enetdown { get; }
	public static int Enetreset { get; }
	public static int Enetunreach { get; }
	public static int Enfile { get; }
	public static int Enobufs { get; }
	public static int Enodata { get; }
	public static int Enodev { get; }
	public static int Enoent { get; }
	public static int Enoexec { get; }
	public static int Enolck { get; }
	public static int Enolink { get; }
	public static int Enomem { get; }
	public static int Enomsg { get; }
	public static int Enoprotoopt { get; }
	public static int Enospc { get; }
	public static int Enosr { get; }
	public static int Enostr { get; }
	public static int Enosys { get; }
	public static int Enotconn { get; }
	public static int Enotdir { get; }
	public static int Enotempty { get; }
	public static int Enotsock { get; }
	public static int Enotsup { get; }
	public static int Enotty { get; }
	public static int Enxio { get; }
	public static int Eopnotsupp { get; }
	public static int Eoverflow { get; }
	public static int Eperm { get; }
	public static int Epipe { get; }
	public static int Eproto { get; }
	public static int Eprotonosupport { get; }
	public static int Eprototype { get; }
	public static int Erange { get; }
	public static int Erofs { get; }
	public static int Espipe { get; }
	public static int Esrch { get; }
	public static int Estale { get; }
	public static int Etime { get; }
	public static int Etimedout { get; }
	public static int Etxtbsy { get; }
	public static int Exdev { get; }
	public static int ExitFailure { get; }
	public static int ExitSuccess { get; }
	public static int FdCloexec { get; }
	public static int FDupfd { get; }
	public static int FGetfd { get; }
	public static int FGetfl { get; }
	public static int FGetlk { get; }
	public static int FGetlk64 { get; }
	public static int FGetown { get; }
	public static int Fionread { get; }
	public static int FOk { get; }
	public static int FRdlck { get; }
	public static int FSetfd { get; }
	public static int FSetfl { get; }
	public static int FSetlk { get; }
	public static int FSetlk64 { get; }
	public static int FSetlkw { get; }
	public static int FSetlkw64 { get; }
	public static int FSetown { get; }
	public static int FUnlck { get; }
	public static int FWrlck { get; }
	public static int IfaFDadfailed { get; }
	public static int IfaFDeprecated { get; }
	public static int IfaFHomeaddress { get; }
	public static int IfaFNodad { get; }
	public static int IfaFOptimistic { get; }
	public static int IfaFPermanent { get; }
	public static int IfaFSecondary { get; }
	public static int IfaFTemporary { get; }
	public static int IfaFTentative { get; }
	public static int IffAllmulti { get; }
	public static int IffAutomedia { get; }
	public static int IffBroadcast { get; }
	public static int IffDebug { get; }
	public static int IffDynamic { get; }
	public static int IffLoopback { get; }
	public static int IffMaster { get; }
	public static int IffMulticast { get; }
	public static int IffNoarp { get; }
	public static int IffNotrailers { get; }
	public static int IffPointopoint { get; }
	public static int IffPortsel { get; }
	public static int IffPromisc { get; }
	public static int IffRunning { get; }
	public static int IffSlave { get; }
	public static int IffUp { get; }
	public static int IpMulticastIf { get; }
	public static int IpMulticastLoop { get; }
	public static int IpMulticastTtl { get; }
	public static int IpprotoIcmp { get; }
	public static int IpprotoIcmpv6 { get; }
	public static int IpprotoIp { get; }
	public static int IpprotoIpv6 { get; }
	public static int IpprotoRaw { get; }
	public static int IpprotoTcp { get; }
	public static int IpprotoUdp { get; }
	public static int IpTos { get; }
	public static int IpTtl { get; }
	public static int Ipv6Checksum { get; }
	public static int Ipv6MulticastHops { get; }
	public static int Ipv6MulticastIf { get; }
	public static int Ipv6MulticastLoop { get; }
	public static int Ipv6Recvdstopts { get; }
	public static int Ipv6Recvhoplimit { get; }
	public static int Ipv6Recvhopopts { get; }
	public static int Ipv6Recvpktinfo { get; }
	public static int Ipv6Recvrthdr { get; }
	public static int Ipv6Recvtclass { get; }
	public static int Ipv6Tclass { get; }
	public static int Ipv6UnicastHops { get; }
	public static int Ipv6V6only { get; }
	public static int MapFixed { get; }
	public static int MapPrivate { get; }
	public static int MapShared { get; }
	public static int McastBlockSource { get; }
	public static int McastJoinGroup { get; }
	public static int McastJoinSourceGroup { get; }
	public static int McastLeaveGroup { get; }
	public static int McastLeaveSourceGroup { get; }
	public static int McastUnblockSource { get; }
	public static int MclCurrent { get; }
	public static int MclFuture { get; }
	public static int MsAsync { get; }
	public static int MsgCtrunc { get; }
	public static int MsgDontroute { get; }
	public static int MsgEor { get; }
	public static int MsgOob { get; }
	public static int MsgPeek { get; }
	public static int MsgTrunc { get; }
	public static int MsgWaitall { get; }
	public static int MsInvalidate { get; }
	public static int MsSync { get; }
	public static int NiDgram { get; }
	public static int NiNamereqd { get; }
	public static int NiNofqdn { get; }
	public static int NiNumerichost { get; }
	public static int NiNumericserv { get; }
	public static int OAccmode { get; }
	public static int OAppend { get; }
	public static int OCreat { get; }
	public static int OExcl { get; }
	public static int ONoctty { get; }
	public static int ONofollow { get; }
	public static int ONonblock { get; }
	public static int ORdonly { get; }
	public static int ORdwr { get; }
	public static int OSync { get; }
	public static int OTrunc { get; }
	public static int OWronly { get; }
	public static int Pollerr { get; }
	public static int Pollhup { get; }
	public static int Pollin { get; }
	public static int Pollnval { get; }
	public static int Pollout { get; }
	public static int Pollpri { get; }
	public static int Pollrdband { get; }
	public static int Pollrdnorm { get; }
	public static int Pollwrband { get; }
	public static int Pollwrnorm { get; }
	public static int PrGetDumpable { get; }
	public static int ProtExec { get; }
	public static int ProtNone { get; }
	public static int ProtRead { get; }
	public static int ProtWrite { get; }
	public static int PrSetDumpable { get; }
	public static int PrSetNoNewPrivs { get; }
	public static int ROk { get; }
	public static int RtScopeHost { get; }
	public static int RtScopeLink { get; }
	public static int RtScopeNowhere { get; }
	public static int RtScopeSite { get; }
	public static int RtScopeUniverse { get; }
	public static int Sc2CBind { get; }
	public static int Sc2CDev { get; }
	public static int Sc2CharTerm { get; }
	public static int Sc2CVersion { get; }
	public static int Sc2FortDev { get; }
	public static int Sc2FortRun { get; }
	public static int Sc2Localedef { get; }
	public static int Sc2SwDev { get; }
	public static int Sc2Upe { get; }
	public static int Sc2Version { get; }
	public static int ScAioListioMax { get; }
	public static int ScAioMax { get; }
	public static int ScAioPrioDeltaMax { get; }
	public static int ScArgMax { get; }
	public static int ScAsynchronousIo { get; }
	public static int ScAtexitMax { get; }
	public static int ScAvphysPages { get; }
	public static int ScBcBaseMax { get; }
	public static int ScBcDimMax { get; }
	public static int ScBcScaleMax { get; }
	public static int ScBcStringMax { get; }
	public static int ScChildMax { get; }
	public static int ScClkTck { get; }
	public static int ScCollWeightsMax { get; }
	public static int ScDelaytimerMax { get; }
	public static int ScExprNestMax { get; }
	public static int ScFsync { get; }
	public static int ScGetgrRSizeMax { get; }
	public static int ScGetpwRSizeMax { get; }
	public static int ScIovMax { get; }
	public static int ScJobControl { get; }
	public static int ScLineMax { get; }
	public static int ScLoginNameMax { get; }
	public static int ScMappedFiles { get; }
	public static int ScMemlock { get; }
	public static int ScMemlockRange { get; }
	public static int ScMemoryProtection { get; }
	public static int ScMessagePassing { get; }
	public static int ScMqOpenMax { get; }
	public static int ScMqPrioMax { get; }
	public static int ScNgroupsMax { get; }
	public static int ScNprocessorsConf { get; }
	public static int ScNprocessorsOnln { get; }
	public static int ScOpenMax { get; }
	public static int ScPagesize { get; }
	public static int ScPageSize { get; }
	public static int ScPassMax { get; }
	public static int ScPhysPages { get; }
	public static int ScPrioritizedIo { get; }
	public static int ScPriorityScheduling { get; }
	public static int ScRealtimeSignals { get; }
	public static int ScReDupMax { get; }
	public static int ScRtsigMax { get; }
	public static int ScSavedIds { get; }
	public static int ScSemaphores { get; }
	public static int ScSemNsemsMax { get; }
	public static int ScSemValueMax { get; }
	public static int ScSharedMemoryObjects { get; }
	public static int ScSigqueueMax { get; }
	public static int ScStreamMax { get; }
	public static int ScSynchronizedIo { get; }
	public static int ScThreadAttrStackaddr { get; }
	public static int ScThreadAttrStacksize { get; }
	public static int ScThreadDestructorIterations { get; }
	public static int ScThreadKeysMax { get; }
	public static int ScThreadPrioInherit { get; }
	public static int ScThreadPrioProtect { get; }
	public static int ScThreadPriorityScheduling { get; }
	public static int ScThreads { get; }
	public static int ScThreadSafeFunctions { get; }
	public static int ScThreadStackMin { get; }
	public static int ScThreadThreadsMax { get; }
	public static int ScTimerMax { get; }
	public static int ScTimers { get; }
	public static int ScTtyNameMax { get; }
	public static int ScTznameMax { get; }
	public static int ScVersion { get; }
	public static int ScXbs5Ilp32Off32 { get; }
	public static int ScXbs5Ilp32Offbig { get; }
	public static int ScXbs5Lp64Off64 { get; }
	public static int ScXbs5LpbigOffbig { get; }
	public static int ScXopenCrypt { get; }
	public static int ScXopenEnhI18n { get; }
	public static int ScXopenLegacy { get; }
	public static int ScXopenRealtime { get; }
	public static int ScXopenRealtimeThreads { get; }
	public static int ScXopenShm { get; }
	public static int ScXopenUnix { get; }
	public static int ScXopenVersion { get; }
	public static int ScXopenXcuVersion { get; }
	public static int SeekCur { get; }
	public static int SeekEnd { get; }
	public static int SeekSet { get; }
	public static int ShutRd { get; }
	public static int ShutRdwr { get; }
	public static int ShutWr { get; }
	public static int SIfblk { get; }
	public static int SIfchr { get; }
	public static int SIfdir { get; }
	public static int SIfifo { get; }
	public static int SIflnk { get; }
	public static int SIfmt { get; }
	public static int SIfreg { get; }
	public static int SIfsock { get; }
	public static int Sigabrt { get; }
	public static int Sigalrm { get; }
	public static int Sigbus { get; }
	public static int Sigchld { get; }
	public static int Sigcont { get; }
	public static int Sigfpe { get; }
	public static int Sighup { get; }
	public static int Sigill { get; }
	public static int Sigint { get; }
	public static int Sigio { get; }
	public static int Sigkill { get; }
	public static int Sigpipe { get; }
	public static int Sigprof { get; }
	public static int Sigpwr { get; }
	public static int Sigquit { get; }
	public static int Sigrtmax { get; }
	public static int Sigrtmin { get; }
	public static int Sigsegv { get; }
	public static int Sigstkflt { get; }
	public static int Sigstop { get; }
	public static int Sigsys { get; }
	public static int Sigterm { get; }
	public static int Sigtrap { get; }
	public static int Sigtstp { get; }
	public static int Sigttin { get; }
	public static int Sigttou { get; }
	public static int Sigurg { get; }
	public static int Sigusr1 { get; }
	public static int Sigusr2 { get; }
	public static int Sigvtalrm { get; }
	public static int Sigwinch { get; }
	public static int Sigxcpu { get; }
	public static int Sigxfsz { get; }
	public static int Siocgifaddr { get; }
	public static int Siocgifbrdaddr { get; }
	public static int Siocgifdstaddr { get; }
	public static int Siocgifnetmask { get; }
	public static int SIrgrp { get; }
	public static int SIroth { get; }
	public static int SIrusr { get; }
	public static int SIrwxg { get; }
	public static int SIrwxo { get; }
	public static int SIrwxu { get; }
	public static int SIsgid { get; }
	public static int SIsuid { get; }
	public static int SIsvtx { get; }
	public static int SIwgrp { get; }
	public static int SIwoth { get; }
	public static int SIwusr { get; }
	public static int SIxgrp { get; }
	public static int SIxoth { get; }
	public static int SIxusr { get; }
	public static int SoBindtodevice { get; }
	public static int SoBroadcast { get; }
	public static int SockDgram { get; }
	public static int SockRaw { get; }
	public static int SockSeqpacket { get; }
	public static int SockStream { get; }
	public static int SoDebug { get; }
	public static int SoDontroute { get; }
	public static int SoError { get; }
	public static int SoKeepalive { get; }
	public static int SoLinger { get; }
	public static int SolSocket { get; }
	public static int SoOobinline { get; }
	public static int SoPasscred { get; }
	public static int SoPeercred { get; }
	public static int SoRcvbuf { get; }
	public static int SoRcvlowat { get; }
	public static int SoRcvtimeo { get; }
	public static int SoReuseaddr { get; }
	public static int SoSndbuf { get; }
	public static int SoSndlowat { get; }
	public static int SoSndtimeo { get; }
	public static int SoType { get; }
	public static int StderrFileno { get; }
	public static int StdinFileno { get; }
	public static int StdoutFileno { get; }
	public static int TcpNodelay { get; }
	public static int Wcontinued { get; }
	public static int Wexited { get; }
	public static int Wnohang { get; }
	public static int Wnowait { get; }
	public static int WOk { get; }
	public static int Wstopped { get; }
	public static int Wuntraced { get; }
	public static int XOk { get; }
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.CellIdentityCdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellIdentityGsm

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellIdentityLte

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellIdentityWcdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellInfoCdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellInfoGsm

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellInfoLte

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellInfoWcdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellSignalStrengthCdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellSignalStrengthGsm

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellSignalStrengthLte

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.CellSignalStrengthWcdma

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.IccOpenLogicalChannelResponse

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.NeighboringCellInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.PhoneNumberUtils

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static void FormatJapaneseNumber (Android.Text.IEditable text);

	[Obsolete ("deprecated")]
	public static void FormatNanpNumber (Android.Text.IEditable text);

	[Obsolete ("deprecated")]
	public static string FormatNumber (string source);

	[Obsolete ("deprecated")]
	public static void FormatNumber (Android.Text.IEditable text, PhoneNumberFormat defaultFormattingType);

	[Obsolete ("deprecated")]
	public static PhoneNumberFormat GetFormatTypeForLocale (Java.Util.Locale locale);
```

### Type Changed: Android.Telephony.PhoneStateListener

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void OnSignalStrengthChanged (int asu);
```

### Type Changed: Android.Telephony.ServiceState

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Telephony.SmsMessage

### Type Changed: Android.Telephony.SmsMessage.MessageClass

Removed properties:

```
public static SmsMessage.MessageClass Class0 { get; set; }
	public static SmsMessage.MessageClass Class1 { get; set; }
	public static SmsMessage.MessageClass Class2 { get; set; }
	public static SmsMessage.MessageClass Class3 { get; set; }
	public static SmsMessage.MessageClass Unknown { get; set; }
```

Added properties:

```
public static SmsMessage.MessageClass Class0 { get; }
	public static SmsMessage.MessageClass Class1 { get; }
	public static SmsMessage.MessageClass Class2 { get; }
	public static SmsMessage.MessageClass Class3 { get; }
	public static SmsMessage.MessageClass Unknown { get; }
```

### Type Changed: Android.Telephony.TelephonyManager

Removed properties:

```
public static string ExtraStateIdle { get; set; }
	public static string ExtraStateOffhook { get; set; }
	public static string ExtraStateRinging { get; set; }
```

Added properties:

```
public static string ExtraStateIdle { get; }
	public static string ExtraStateOffhook { get; }
	public static string ExtraStateRinging { get; }
```

## Namespace Android.Telephony.Gsm

### Type Changed: Android.Telephony.Gsm.SmsManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public System.Collections.Generic.IList<string> DivideMessage (string text);

	[Obsolete ("deprecated")]
	public void SendDataMessage (string destinationAddress, string scAddress, short destinationPort, byte[] data, Android.App.PendingIntent sentIntent, Android.App.PendingIntent deliveryIntent);

	[Obsolete ("deprecated")]
	public void SendMultipartTextMessage (string destinationAddress, string scAddress, System.Collections.Generic.IList<string> parts, System.Collections.Generic.IList<Android.App.PendingIntent> sentIntents, System.Collections.Generic.IList<Android.App.PendingIntent> deliveryIntents);

	[Obsolete ("deprecated")]
	public void SendTextMessage (string destinationAddress, string scAddress, string text, Android.App.PendingIntent sentIntent, Android.App.PendingIntent deliveryIntent);
```

### Type Changed: Android.Telephony.Gsm.SmsMessage

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static int[] CalculateLength (Java.Lang.ICharSequence messageBody, bool use7bitOnly);

	[Obsolete ("deprecated")]
	public static int[] CalculateLength (string messageBody, bool use7bitOnly);

	[Obsolete ("deprecated")]
	public static SmsMessage CreateFromPdu (byte[] pdu);

	[Obsolete ("deprecated")]
	public virtual SmsMessage.MessageClass GetMessageClass ();

	[Obsolete ("deprecated")]
	public virtual byte[] GetPdu ();

	[Obsolete ("deprecated")]
	public static SmsMessage.SubmitPdu GetSubmitPdu (string scAddress, string destinationAddress, string message, bool statusReportRequested);

	[Obsolete ("deprecated")]
	public static SmsMessage.SubmitPdu GetSubmitPdu (string scAddress, string destinationAddress, short destinationPort, byte[] data, bool statusReportRequested);

	[Obsolete ("deprecated")]
	public static int GetTPLayerLengthForPDU (string pdu);

	[Obsolete ("deprecated")]
	public virtual byte[] GetUserData ();
```

### Type Changed: Android.Telephony.Gsm.SmsMessage.MessageClass

Removed properties:

```
public static SmsMessage.MessageClass Class0 { get; set; }
	public static SmsMessage.MessageClass Class1 { get; set; }
	public static SmsMessage.MessageClass Class2 { get; set; }
	public static SmsMessage.MessageClass Class3 { get; set; }
	public static SmsMessage.MessageClass Unknown { get; set; }
```

Added properties:

```
public static SmsMessage.MessageClass Class0 { get; }
	public static SmsMessage.MessageClass Class1 { get; }
	public static SmsMessage.MessageClass Class2 { get; }
	public static SmsMessage.MessageClass Class3 { get; }
	public static SmsMessage.MessageClass Unknown { get; }
```

## Namespace Android.Test.Mock

### Type Changed: Android.Test.Mock.MockContext

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override void ClearWallpaper ();

	[Obsolete ("deprecated")]
	public override Android.Graphics.Drawables.Drawable PeekWallpaper ();

	[Obsolete ("deprecated")]
	public override void RemoveStickyBroadcast (Android.Content.Intent intent);

	[Obsolete ("deprecated")]
	public override void RemoveStickyBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user);

	[Obsolete ("deprecated")]
	public override void SendStickyBroadcast (Android.Content.Intent intent);

	[Obsolete ("deprecated")]
	public override void SendStickyBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user);

	[Obsolete ("deprecated")]
	public override void SendStickyOrderedBroadcast (Android.Content.Intent intent, Android.Content.BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);

	[Obsolete ("deprecated")]
	public override void SendStickyOrderedBroadcastAsUser (Android.Content.Intent intent, Android.OS.UserHandle user, Android.Content.BroadcastReceiver resultReceiver, Android.OS.Handler scheduler, Android.App.Result initialCode, string initialData, Android.OS.Bundle initialExtras);

	[Obsolete ("deprecated")]
	public override void SetWallpaper (Android.Graphics.Bitmap bitmap);

	[Obsolete ("deprecated")]
	public override void SetWallpaper (System.IO.Stream data);
```

### Type Changed: Android.Test.Mock.MockPackageManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override void AddPackageToPreferred (string packageName);

	[Obsolete ("deprecated")]
	public override void AddPreferredActivity (Android.Content.IntentFilter filter, Android.Content.MatchResults match, Android.Content.ComponentName[] set, Android.Content.ComponentName activity);

	[Obsolete ("deprecated")]
	public override void RemovePackageFromPreferred (string packageName);
```

## Namespace Android.Text

### Type Changed: Android.Text.Layout

### Type Changed: Android.Text.Layout.Alignment

Removed properties:

```
public static Layout.Alignment AlignCenter { get; set; }
	public static Layout.Alignment AlignNormal { get; set; }
	public static Layout.Alignment AlignOpposite { get; set; }
```

Added properties:

```
public static Layout.Alignment AlignCenter { get; }
	public static Layout.Alignment AlignNormal { get; }
	public static Layout.Alignment AlignOpposite { get; }
```

### Type Changed: Android.Text.Selection

Removed properties:

```
public static Java.Lang.Object SelectionEnd { get; set; }
	public static Java.Lang.Object SelectionStart { get; set; }
```

Added properties:

```
public static Java.Lang.Object SelectionEnd { get; }
	public static Java.Lang.Object SelectionStart { get; }
```

### Type Changed: Android.Text.SpannableStringBuilder

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual int GetTextRunCursor (int contextStart, int contextEnd, int dir, int offset, int cursorOpt, Android.Graphics.Paint p);
```

### Type Changed: Android.Text.TextDirectionHeuristics

Removed properties:

```
public static ITextDirectionHeuristic AnyrtlLtr { get; set; }
	public static ITextDirectionHeuristic FirststrongLtr { get; set; }
	public static ITextDirectionHeuristic FirststrongRtl { get; set; }
	public static ITextDirectionHeuristic Locale { get; set; }
	public static ITextDirectionHeuristic Ltr { get; set; }
	public static ITextDirectionHeuristic Rtl { get; set; }
```

Added properties:

```
public static ITextDirectionHeuristic AnyrtlLtr { get; }
	public static ITextDirectionHeuristic FirststrongLtr { get; }
	public static ITextDirectionHeuristic FirststrongRtl { get; }
	public static ITextDirectionHeuristic Locale { get; }
	public static ITextDirectionHeuristic Ltr { get; }
	public static ITextDirectionHeuristic Rtl { get; }
```

### Type Changed: Android.Text.TextPaint

Removed properties:

```
public int BgColor { get; set; }
	public int LinkColor { get; set; }
```

Added properties:

```
public Android.Graphics.Color BgColor { get; set; }
	public Android.Graphics.Color LinkColor { get; set; }
```

### Type Changed: Android.Text.TextUtils

Removed property:

```
public static Android.OS.IParcelableCreator CharSequenceCreator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator CharSequenceCreator { get; }
```

### Type Changed: Android.Text.TextUtils.TruncateAt

Removed properties:

```
public static TextUtils.TruncateAt End { get; set; }
	public static TextUtils.TruncateAt Marquee { get; set; }
	public static TextUtils.TruncateAt Middle { get; set; }
	public static TextUtils.TruncateAt Start { get; set; }
```

Added properties:

```
public static TextUtils.TruncateAt End { get; }
	public static TextUtils.TruncateAt Marquee { get; }
	public static TextUtils.TruncateAt Middle { get; }
	public static TextUtils.TruncateAt Start { get; }
```

## Namespace Android.Text.Format

### Type Changed: Android.Text.Format.DateUtils

Removed properties:

```
public static System.Collections.Generic.IList<int> SameMonthTable { get; set; }
	public static System.Collections.Generic.IList<int> SameYearTable { get; set; }
```

Added properties:

```
public static System.Collections.Generic.IList<int> SameMonthTable { get; }
	public static System.Collections.Generic.IList<int> SameYearTable { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string GetAMPMString (int ampm);

	[Obsolete ("deprecated")]
	public static string GetDayOfWeekString (int dayOfWeek, AbbreviationLength abbrev);

	[Obsolete ("deprecated")]
	public static string GetMonthString (int month, AbbreviationLength abbrev);
```

### Type Changed: Android.Text.Format.Formatter

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static string FormatIpAddress (int ipv4Address);
```

## Namespace Android.Text.Method

### Type Changed: Android.Text.Method.DateKeyListener

Removed property:

```
public static System.Collections.Generic.IList<char> Characters { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<char> Characters { get; }
```

### Type Changed: Android.Text.Method.DateTimeKeyListener

Removed property:

```
public static System.Collections.Generic.IList<char> Characters { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<char> Characters { get; }
```

### Type Changed: Android.Text.Method.DialerKeyListener

Removed property:

```
public static System.Collections.Generic.IList<char> Characters { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<char> Characters { get; }
```

### Type Changed: Android.Text.Method.TextKeyListener

### Type Changed: Android.Text.Method.TextKeyListener.Capitalize

Removed properties:

```
public static TextKeyListener.Capitalize Characters { get; set; }
	public static TextKeyListener.Capitalize None { get; set; }
	public static TextKeyListener.Capitalize Sentences { get; set; }
	public static TextKeyListener.Capitalize Words { get; set; }
```

Added properties:

```
public static TextKeyListener.Capitalize Characters { get; }
	public static TextKeyListener.Capitalize None { get; }
	public static TextKeyListener.Capitalize Sentences { get; }
	public static TextKeyListener.Capitalize Words { get; }
```

### Type Changed: Android.Text.Method.TimeKeyListener

Removed property:

```
public static System.Collections.Generic.IList<char> Characters { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<char> Characters { get; }
```

## Namespace Android.Text.Style

### Type Changed: Android.Text.Style.BackgroundColorSpan

Removed property:

```
public virtual int BackgroundColor { get; }
```

Added property:

```
public virtual Android.Graphics.Color BackgroundColor { get; }
```

### Type Changed: Android.Text.Style.ForegroundColorSpan

Removed property:

```
public virtual int ForegroundColor { get; }
```

Added property:

```
public virtual Android.Graphics.Color ForegroundColor { get; }
```

### Type Changed: Android.Text.Style.SuggestionSpan

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Text.Util

### Type Changed: Android.Text.Util.Linkify

Removed properties:

```
public static Linkify.IMatchFilter SPhoneNumberMatchFilter { get; set; }
	public static Linkify.ITransformFilter SPhoneNumberTransformFilter { get; set; }
	public static Linkify.IMatchFilter SUrlMatchFilter { get; set; }
```

Added properties:

```
public static Linkify.IMatchFilter SPhoneNumberMatchFilter { get; }
	public static Linkify.ITransformFilter SPhoneNumberTransformFilter { get; }
	public static Linkify.IMatchFilter SUrlMatchFilter { get; }
```

## Namespace Android.Transitions

### Type Changed: Android.Transitions.ChangeBounds

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetReparent (bool reparent);
```

## Namespace Android.Util

### Type Changed: Android.Util.Config

Removed properties:

```
public static bool Debug { get; set; }
	public static bool Release { get; set; }
```

Added properties:

```
public static bool Debug { get; }
	public static bool Release { get; }
```

### Type Changed: Android.Util.JsonToken

Removed properties:

```
public static JsonToken BeginArray { get; set; }
	public static JsonToken BeginObject { get; set; }
	public static JsonToken Boolean { get; set; }
	public static JsonToken EndArray { get; set; }
	public static JsonToken EndDocument { get; set; }
	public static JsonToken EndObject { get; set; }
	public static JsonToken Name { get; set; }
	public static JsonToken Null { get; set; }
	public static JsonToken Number { get; set; }
	public static JsonToken String { get; set; }
```

Added properties:

```
public static JsonToken BeginArray { get; }
	public static JsonToken BeginObject { get; }
	public static JsonToken Boolean { get; }
	public static JsonToken EndArray { get; }
	public static JsonToken EndDocument { get; }
	public static JsonToken EndObject { get; }
	public static JsonToken Name { get; }
	public static JsonToken Null { get; }
	public static JsonToken Number { get; }
	public static JsonToken String { get; }
```

### Type Changed: Android.Util.Patterns

Removed properties:

```
public static Java.Util.Regex.Pattern DomainName { get; set; }
	public static Java.Util.Regex.Pattern EmailAddress { get; set; }
	public static Java.Util.Regex.Pattern IpAddress { get; set; }
	public static Java.Util.Regex.Pattern Phone { get; set; }
	public static Java.Util.Regex.Pattern TopLevelDomain { get; set; }
	public static Java.Util.Regex.Pattern WebUrl { get; set; }
```

Added properties:

```
public static Java.Util.Regex.Pattern DomainName { get; }
	public static Java.Util.Regex.Pattern EmailAddress { get; }
	public static Java.Util.Regex.Pattern IpAddress { get; }
	public static Java.Util.Regex.Pattern Phone { get; }
	public static Java.Util.Regex.Pattern TopLevelDomain { get; }
	public static Java.Util.Regex.Pattern WebUrl { get; }
```

### Type Changed: Android.Util.Rational

Removed properties:

```
public static Rational NaN { get; set; }
	public static Rational NegativeInfinity { get; set; }
	public static Rational PositiveInfinity { get; set; }
	public static Rational Zero { get; set; }
```

Added properties:

```
public static Rational NaN { get; }
	public static Rational NegativeInfinity { get; }
	public static Rational PositiveInfinity { get; }
	public static Rational Zero { get; }
```

### Type Changed: Android.Util.StateSet

Removed properties:

```
public static System.Collections.Generic.IList<int> Nothing { get; set; }
	public static System.Collections.Generic.IList<int> WildCard { get; set; }
```

Added properties:

```
public static System.Collections.Generic.IList<int> Nothing { get; }
	public static System.Collections.Generic.IList<int> WildCard { get; }
```

### Type Changed: Android.Util.Xml

### Type Changed: Android.Util.Xml.Encoding

Removed properties:

```
public static Xml.Encoding Iso88591 { get; set; }
	public static Xml.Encoding UsAscii { get; set; }
	public static Xml.Encoding Utf16 { get; set; }
	public static Xml.Encoding Utf8 { get; set; }
```

Added properties:

```
public static Xml.Encoding Iso88591 { get; }
	public static Xml.Encoding UsAscii { get; }
	public static Xml.Encoding Utf16 { get; }
	public static Xml.Encoding Utf8 { get; }
```

## Namespace Android.Views

### Type Changed: Android.Views.AbsSavedState

Removed properties:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
	public static AbsSavedState EmptyState { get; set; }
```

Added properties:

```
public static Android.OS.IParcelableCreator Creator { get; }
	public static AbsSavedState EmptyState { get; }
```

### Type Changed: Android.Views.DragEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputDevice

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Added method:

```
[Obsolete ("Please use GetMotionRange(Android.Views.Axis)")]
	public InputDevice.MotionRange GetMotionRange (int rangeType);
```

### Type Changed: Android.Views.InputEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.KeyCharacterMap

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual bool GetKeyData (Keycode keyCode, KeyCharacterMap.KeyData results);
```

### Type Changed: Android.Views.KeyEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Added method:

```
[Obsolete ("Please use GetUnicodeChar(MetaKeyStates)")]
	public int GetUnicodeChar (int meta);
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public bool Dispatch (KeyEvent.ICallback receiver);

	[Obsolete ("deprecated")]
	public virtual bool GetKeyData (KeyCharacterMap.KeyData results);

	[Obsolete ("Please use GetMatch(char[], MetaKeyStates)")]
	public char GetMatch (char[] chars, int metaState);
```

### Type Changed: Android.Views.MotionEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointerCount, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);

	[Obsolete ("deprecated")]
	public static MotionEvent Obtain (long downTime, long eventTime, MotionEventActions action, int pointerCount, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, InputSourceType source, MotionEventFlags flags);
```

### Type Changed: Android.Views.Surface

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void UnlockCanvas (Android.Graphics.Canvas canvas);
```

### Type Changed: Android.Views.View

Removed properties:

```
protected static System.Collections.Generic.IList<int> EmptyStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> EnabledWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> FocusedSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> FocusedSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> FocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> FocusedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedEnabledWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedFocusedSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedFocusedSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedFocusedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedSelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedSelectedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> PressedWindowFocusedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> SelectedStateSet { get; set; }
	protected static System.Collections.Generic.IList<int> SelectedWindowFocusedStateSet { get; set; }
	public virtual int SolidColor { get; }
	protected static System.Collections.Generic.IList<int> WindowFocusedStateSet { get; set; }
	public static Android.Util.Property Z { get; set; }
```

Added properties:

```
protected static System.Collections.Generic.IList<int> EmptyStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledFocusedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledStateSet { get; }
	protected static System.Collections.Generic.IList<int> EnabledWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> FocusedSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> FocusedSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> FocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> FocusedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledFocusedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedEnabledWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedFocusedSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedFocusedSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedFocusedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedSelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedSelectedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedStateSet { get; }
	protected static System.Collections.Generic.IList<int> PressedWindowFocusedStateSet { get; }
	protected static System.Collections.Generic.IList<int> SelectedStateSet { get; }
	protected static System.Collections.Generic.IList<int> SelectedWindowFocusedStateSet { get; }
	public virtual Android.Graphics.Color SolidColor { get; }
	protected static System.Collections.Generic.IList<int> WindowFocusedStateSet { get; }
	public static Android.Util.Property Z { get; }
```

Obsoleted methods:

```
[Obsolete ("Please Use DispatchSystemUiVisibilityChanged(SystemUiFlags)")]
	public void DispatchSystemUiVisibilityChanged (int visibility);

	[Obsolete ("deprecated")]
	protected virtual bool FitSystemWindows (Android.Graphics.Rect insets);

	[Obsolete ("The View.fitsSystemWindows() method was REMOVED by Google in API-16. DO NOT USE.")]
	public virtual bool InvokeFitsSystemWindows ();

	[Obsolete ("deprecated")]
	public virtual void RequestFitSystemWindows ();

	[Obsolete ("deprecated")]
	public virtual void SetBackgroundDrawable (Android.Graphics.Drawables.Drawable background);
```

### Type Changed: Android.Views.View.BaseSavedState

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.ViewDebug

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static void StartHierarchyTracing (string prefix, View view);

	[Obsolete ("deprecated")]
	public static void StartRecyclerTracing (string prefix, View view);

	[Obsolete ("deprecated")]
	public static void StopHierarchyTracing ();

	[Obsolete ("deprecated")]
	public static void StopRecyclerTracing ();

	[Obsolete ("deprecated")]
	public static void Trace (View view, ViewDebug.HierarchyTraceType type);

	[Obsolete ("deprecated")]
	public static void Trace (View view, ViewDebug.RecyclerTraceType type, int[] parameters);
```

### Type Changed: Android.Views.ViewDebug.HierarchyTraceType

Removed properties:

```
public static ViewDebug.HierarchyTraceType BuildCache { get; set; }
	public static ViewDebug.HierarchyTraceType Draw { get; set; }
	public static ViewDebug.HierarchyTraceType Invalidate { get; set; }
	public static ViewDebug.HierarchyTraceType InvalidateChild { get; set; }
	public static ViewDebug.HierarchyTraceType InvalidateChildInParent { get; set; }
	public static ViewDebug.HierarchyTraceType OnLayout { get; set; }
	public static ViewDebug.HierarchyTraceType OnMeasure { get; set; }
	public static ViewDebug.HierarchyTraceType RequestLayout { get; set; }
```

Added properties:

```
public static ViewDebug.HierarchyTraceType BuildCache { get; }
	public static ViewDebug.HierarchyTraceType Draw { get; }
	public static ViewDebug.HierarchyTraceType Invalidate { get; }
	public static ViewDebug.HierarchyTraceType InvalidateChild { get; }
	public static ViewDebug.HierarchyTraceType InvalidateChildInParent { get; }
	public static ViewDebug.HierarchyTraceType OnLayout { get; }
	public static ViewDebug.HierarchyTraceType OnMeasure { get; }
	public static ViewDebug.HierarchyTraceType RequestLayout { get; }
```

### Type Changed: Android.Views.ViewDebug.RecyclerTraceType

Removed properties:

```
public static ViewDebug.RecyclerTraceType BindView { get; set; }
	public static ViewDebug.RecyclerTraceType MoveFromActiveToScrapHeap { get; set; }
	public static ViewDebug.RecyclerTraceType MoveToActiveHeap { get; set; }
	public static ViewDebug.RecyclerTraceType MoveToScrapHeap { get; set; }
	public static ViewDebug.RecyclerTraceType NewView { get; set; }
	public static ViewDebug.RecyclerTraceType RecycleFromActiveHeap { get; set; }
	public static ViewDebug.RecyclerTraceType RecycleFromScrapHeap { get; set; }
```

Added properties:

```
public static ViewDebug.RecyclerTraceType BindView { get; }
	public static ViewDebug.RecyclerTraceType MoveFromActiveToScrapHeap { get; }
	public static ViewDebug.RecyclerTraceType MoveToActiveHeap { get; }
	public static ViewDebug.RecyclerTraceType MoveToScrapHeap { get; }
	public static ViewDebug.RecyclerTraceType NewView { get; }
	public static ViewDebug.RecyclerTraceType RecycleFromActiveHeap { get; }
	public static ViewDebug.RecyclerTraceType RecycleFromScrapHeap { get; }
```

### Type Changed: Android.Views.ViewOutlineProvider

Removed properties:

```
public static ViewOutlineProvider Background { get; set; }
	public static ViewOutlineProvider Bounds { get; set; }
	public static ViewOutlineProvider PaddedBounds { get; set; }
```

Added properties:

```
public static ViewOutlineProvider Background { get; }
	public static ViewOutlineProvider Bounds { get; }
	public static ViewOutlineProvider PaddedBounds { get; }
```

### Type Changed: Android.Views.ViewTreeObserver

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void RemoveGlobalOnLayoutListener (ViewTreeObserver.IOnGlobalLayoutListener victim);
```

### Type Changed: Android.Views.Window

Removed properties:

```
public virtual int NavigationBarColor { get; }
	public virtual int StatusBarColor { get; }
```

Added properties:

```
public virtual Android.Graphics.Color NavigationBarColor { get; set; }
	public virtual Android.Graphics.Color StatusBarColor { get; set; }
```

Removed methods:

```
public virtual void SetNavigationBarColor (Android.Graphics.Color color);
	public virtual void SetStatusBarColor (Android.Graphics.Color color);
```

### Type Changed: Android.Views.WindowAnimationFrameStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.WindowContentFrameStats

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.WindowId

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.WindowManagerLayoutParams

Added field:

```
public static const int TypeKeyguard;
```

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.WindowManagerTypes

Removed value:

```
Keyguard = 2004,
```

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityEvent

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added properties:

```
public string BeforeText { get; set; }
	public string ClassName { get; set; }
	public string ContentDescription { get; set; }
	public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddAction (Action action);

	[Obsolete ("deprecated")]
	public virtual void RemoveAction (int action);
```

### Type Changed: Android.Views.Accessibility.AccessibilityNodeInfo.AccessibilityAction

Removed properties:

```
public static AccessibilityNodeInfo.AccessibilityAction ActionAccessibilityFocus { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearAccessibilityFocus { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearFocus { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearSelection { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClick { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCollapse { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCopy { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCut { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionDismiss { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionExpand { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionFocus { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionLongClick { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionNextAtMovementGranularity { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionNextHtmlElement { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPaste { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPreviousAtMovementGranularity { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPreviousHtmlElement { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollBackward { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollForward { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSelect { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSetSelection { get; set; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSetText { get; set; }
```

Added properties:

```
public static AccessibilityNodeInfo.AccessibilityAction ActionAccessibilityFocus { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearAccessibilityFocus { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearFocus { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClearSelection { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionClick { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCollapse { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCopy { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionCut { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionDismiss { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionExpand { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionFocus { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionLongClick { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionNextAtMovementGranularity { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionNextHtmlElement { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPaste { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPreviousAtMovementGranularity { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionPreviousHtmlElement { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollBackward { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionScrollForward { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSelect { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSetSelection { get; }
	public static AccessibilityNodeInfo.AccessibilityAction ActionSetText { get; }
```

### Type Changed: Android.Views.Accessibility.AccessibilityWindowInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Views.Animations

### Type Changed: Android.Views.Animations.Animation

Removed property:

```
public virtual int BackgroundColor { get; set; }
```

Added property:

```
public virtual Android.Graphics.Color BackgroundColor { get; set; }
```

## Namespace Android.Views.InputMethods

### Type Changed: Android.Views.InputMethods.CompletionInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.CorrectionInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.CursorAnchorInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.EditorInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.ExtractedText

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.ExtractedTextRequest

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.InputBinding

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.InputMethodInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.InputMethods.InputMethodManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public bool IsWatchingCursor (Android.Views.View view);

	[Obsolete ("deprecated")]
	public void UpdateCursor (Android.Views.View view, int left, int top, int right, int bottom);
```

### Type Changed: Android.Views.InputMethods.InputMethodSubtype

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Android.Views.TextService

### Type Changed: Android.Views.TextService.SentenceSuggestionsInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.TextService.SpellCheckerInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.TextService.SpellCheckerSession

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void GetSuggestions (TextInfo textInfo, int suggestionsLimit);

	[Obsolete ("deprecated")]
	public virtual void GetSuggestions (TextInfo[] textInfos, int suggestionsLimit, bool sequentialWords);
```

### Removed Type Android.Views.TextService.SpellCheckerSession.GetSuggestionsEventArgs ### New Type Android.Views.TextService.SpellCheckerSessionEventArgs

```
public class SpellCheckerSessionEventArgs : System.EventArgs {
	// constructors
	public SpellCheckerSession (SuggestionsInfo[] results);
	// properties
	public SuggestionsInfo[] Results { get; }
}
```

### Type Changed: Android.Views.TextService.SpellCheckerSubtype

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.TextService.SuggestionsInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

### Type Changed: Android.Views.TextService.TextInfo

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```



## Namespace Android.Webkit

### Type Changed: Android.Webkit.CacheManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static bool CacheDisabled ();

	[Obsolete ("deprecated")]
	public static bool EndCacheTransaction ();

	[Obsolete ("deprecated")]
	public static CacheManager.CacheResult GetCacheFile (string url, System.Collections.Generic.IDictionary<System.String,System.String> headers);

	[Obsolete ("deprecated")]
	public static void SaveCacheFile (string url, CacheManager.CacheResult cacheResult);

	[Obsolete ("deprecated")]
	public static bool StartCacheTransaction ();
```

### Type Changed: Android.Webkit.ConsoleMessage

### Type Changed: Android.Webkit.ConsoleMessage.MessageLevel

Removed properties:

```
public static ConsoleMessage.MessageLevel Debug { get; set; }
	public static ConsoleMessage.MessageLevel Error { get; set; }
	public static ConsoleMessage.MessageLevel Log { get; set; }
	public static ConsoleMessage.MessageLevel Tip { get; set; }
	public static ConsoleMessage.MessageLevel Warning { get; set; }
```

Added properties:

```
public static ConsoleMessage.MessageLevel Debug { get; }
	public static ConsoleMessage.MessageLevel Error { get; }
	public static ConsoleMessage.MessageLevel Log { get; }
	public static ConsoleMessage.MessageLevel Tip { get; }
	public static ConsoleMessage.MessageLevel Warning { get; }
```

### Type Changed: Android.Webkit.CookieManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void RemoveAllCookie ();

	[Obsolete ("deprecated")]
	public virtual void RemoveExpiredCookie ();

	[Obsolete ("deprecated")]
	public virtual void RemoveSessionCookie ();
```

### Type Changed: Android.Webkit.CookieSyncManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public override void ResetSync ();

	[Obsolete ("deprecated")]
	public override void StartSync ();

	[Obsolete ("deprecated")]
	public override void StopSync ();

	[Obsolete ("deprecated")]
	public override void Sync ();

	[Obsolete ("deprecated")]
	protected void SyncFromRamToFlash ();
```

### Type Changed: Android.Webkit.Plugin

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void DispatchClickEvent (Android.Content.Context context);
```

### Type Changed: Android.Webkit.PluginList

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void AddPlugin (Plugin plugin);

	[Obsolete ("deprecated")]
	public virtual void Clear ();

	[Obsolete ("deprecated")]
	public virtual void PluginClicked (Android.Content.Context context, int position);

	[Obsolete ("deprecated")]
	public virtual void RemovePlugin (Plugin plugin);
```

### Type Changed: Android.Webkit.UrlInterceptRegistry

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static bool RegisterHandler (IUrlInterceptHandler handler);

	[Obsolete ("deprecated")]
	public static void SetUrlInterceptDisabled (bool disabled);

	[Obsolete ("deprecated")]
	public static bool UnregisterHandler (IUrlInterceptHandler handler);

	[Obsolete ("deprecated")]
	public static bool UrlInterceptDisabled ();
```

### Type Changed: Android.Webkit.URLUtil

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static bool IsCookielessProxyUrl (string url);
```

### Type Changed: Android.Webkit.WebChromeClient

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnConsoleMessage (string message, int lineNumber, string sourceID);

	[Obsolete ("deprecated")]
	public virtual void OnExceededDatabaseQuota (string url, string databaseIdentifier, long quota, long estimatedDatabaseSize, long totalQuota, WebStorage.IQuotaUpdater quotaUpdater);

	[Obsolete ("deprecated")]
	public virtual bool OnJsTimeout ();

	[Obsolete ("deprecated")]
	public virtual void OnReachedMaxAppCacheSize (long requiredStorage, long quota, WebStorage.IQuotaUpdater quotaUpdater);

	[Obsolete ("deprecated")]
	public virtual void OnShowCustomView (Android.Views.View view, Android.Content.PM.ScreenOrientation requestedOrientation, WebChromeClient.ICustomViewCallback callback);
```

### Type Changed: Android.Webkit.WebSettings

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool EnableSmoothTransition ();

	[Obsolete ("deprecated")]
	public virtual WebSettings.PluginState GetPluginState ();

	[Obsolete ("deprecated")]
	public virtual WebSettings.TextSize GetTextSize ();

	[Obsolete ("deprecated")]
	public virtual void SetAppCacheMaxSize (long appCacheMaxSize);

	[Obsolete ("deprecated")]
	public virtual void SetEnableSmoothTransition (bool enable);

	[Obsolete ("deprecated")]
	public virtual void SetPluginState (WebSettings.PluginState state);

	[Obsolete ("deprecated")]
	public virtual void SetRenderPriority (WebSettings.RenderPriority priority);

	[Obsolete ("deprecated")]
	public virtual void SetTextSize (WebSettings.TextSize t);
```

### Type Changed: Android.Webkit.WebSettings.LayoutAlgorithm

Removed properties:

```
public static WebSettings.LayoutAlgorithm NarrowColumns { get; set; }
	public static WebSettings.LayoutAlgorithm Normal { get; set; }
	public static WebSettings.LayoutAlgorithm SingleColumn { get; set; }
	public static WebSettings.LayoutAlgorithm TextAutosizing { get; set; }
```

Added properties:

```
public static WebSettings.LayoutAlgorithm NarrowColumns { get; }
	public static WebSettings.LayoutAlgorithm Normal { get; }
	public static WebSettings.LayoutAlgorithm SingleColumn { get; }
	public static WebSettings.LayoutAlgorithm TextAutosizing { get; }
```

### Type Changed: Android.Webkit.WebSettings.PluginState

Removed properties:

```
public static WebSettings.PluginState Off { get; set; }
	public static WebSettings.PluginState On { get; set; }
	public static WebSettings.PluginState OnDemand { get; set; }
```

Added properties:

```
public static WebSettings.PluginState Off { get; }
	public static WebSettings.PluginState On { get; }
	public static WebSettings.PluginState OnDemand { get; }
```

### Type Changed: Android.Webkit.WebSettings.RenderPriority

Removed properties:

```
public static WebSettings.RenderPriority High { get; set; }
	public static WebSettings.RenderPriority Low { get; set; }
	public static WebSettings.RenderPriority Normal { get; set; }
```

Added properties:

```
public static WebSettings.RenderPriority High { get; }
	public static WebSettings.RenderPriority Low { get; }
	public static WebSettings.RenderPriority Normal { get; }
```

### Type Changed: Android.Webkit.WebSettings.TextSize

Removed properties:

```
public static WebSettings.TextSize Larger { get; set; }
	public static WebSettings.TextSize Largest { get; set; }
	public static WebSettings.TextSize Normal { get; set; }
	public static WebSettings.TextSize Smaller { get; set; }
	public static WebSettings.TextSize Smallest { get; set; }
```

Added properties:

```
public static WebSettings.TextSize Larger { get; }
	public static WebSettings.TextSize Largest { get; }
	public static WebSettings.TextSize Normal { get; }
	public static WebSettings.TextSize Smaller { get; }
	public static WebSettings.TextSize Smallest { get; }
```

### Type Changed: Android.Webkit.WebSettings.ZoomDensity

Removed properties:

```
public static WebSettings.ZoomDensity Close { get; set; }
	public static WebSettings.ZoomDensity Far { get; set; }
	public static WebSettings.ZoomDensity Medium { get; set; }
```

Added properties:

```
public static WebSettings.ZoomDensity Close { get; }
	public static WebSettings.ZoomDensity Far { get; }
	public static WebSettings.ZoomDensity Medium { get; }
```

### Type Changed: Android.Webkit.WebStorage

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetQuotaForOrigin (string origin, long quota);
```

### Type Changed: Android.Webkit.WebView

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool CanZoomIn ();

	[Obsolete ("deprecated")]
	public virtual bool CanZoomOut ();

	[Obsolete ("deprecated")]
	public virtual Android.Graphics.Picture CapturePicture ();

	[Obsolete ("deprecated")]
	public virtual void ClearView ();

	[Obsolete ("deprecated")]
	public virtual Android.Print.PrintDocumentAdapter CreatePrintDocumentAdapter ();

	[Obsolete ("deprecated")]
	public virtual void DebugDump ();

	[Obsolete ("deprecated")]
	public static void DisablePlatformNotifications ();

	[Obsolete ("deprecated")]
	public virtual void EmulateShiftHeld ();

	[Obsolete ("deprecated")]
	public static void EnablePlatformNotifications ();

	[Obsolete ("deprecated")]
	public virtual int FindAll (string find);

	[Obsolete ("deprecated")]
	public virtual void FreeMemory ();

	[Obsolete ("deprecated")]
	public virtual void OnChildViewAdded (Android.Views.View parent, Android.Views.View child);

	[Obsolete ("deprecated")]
	public virtual void OnChildViewRemoved (Android.Views.View p, Android.Views.View child);

	[Obsolete ("deprecated")]
	public virtual void OnGlobalFocusChanged (Android.Views.View oldFocus, Android.Views.View newFocus);

	[Obsolete ("deprecated")]
	public virtual void RefreshPlugins (bool reloadOpenPages);

	[Obsolete ("deprecated")]
	public virtual bool RestorePicture (Android.OS.Bundle b, Java.IO.File src);

	[Obsolete ("deprecated")]
	public virtual void SavePassword (string host, string username, string password);

	[Obsolete ("deprecated")]
	public virtual bool SavePicture (Android.OS.Bundle b, Java.IO.File dest);

	[Obsolete ("deprecated")]
	public virtual void SetMapTrackballToArrowKeys (bool setMap);

	[Obsolete ("deprecated")]
	public virtual void SetPictureListener (WebView.IPictureListener listener);

	[Obsolete ("deprecated")]
	public virtual bool ShowFindDialog (string text, bool showIme);
```

### Type Changed: Android.Webkit.WebViewClient

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void OnTooManyRedirects (WebView view, Android.OS.Message cancelMsg, Android.OS.Message continueMsg);

	[Obsolete ("deprecated")]
	public virtual void OnUnhandledKeyEvent (WebView view, Android.Views.KeyEvent e);

	[Obsolete ("deprecated")]
	public virtual WebResourceResponse ShouldInterceptRequest (WebView view, string url);
```

### Type Changed: Android.Webkit.WebViewDatabase

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void ClearUsernamePassword ();
```

## Namespace Android.Widget

### Type Changed: Android.Widget.CursorAdapter

Obsoleted method:

```
[Obsolete ("deprecated")]
	protected virtual void Init (Android.Content.Context context, Android.Database.ICursor c, bool autoRequery);
```

### Type Changed: Android.Widget.EdgeEffect

Removed property:

```
public virtual int Color { get; }
```

Added property:

```
public virtual Android.Graphics.Color Color { get; set; }
```

Removed method:

```
public virtual void SetColor (Android.Graphics.Color color);
```

### Type Changed: Android.Widget.GridLayout

Removed properties:

```
public static GridLayout.Alignment BaselineAlighment { get; set; }
	public static GridLayout.Alignment BottomAlighment { get; set; }
	public static GridLayout.Alignment Center { get; set; }
	public static GridLayout.Alignment End { get; set; }
	public static GridLayout.Alignment Fill { get; set; }
	public static GridLayout.Alignment LeftAlighment { get; set; }
	public static GridLayout.Alignment RightAlighment { get; set; }
	public static GridLayout.Alignment Start { get; set; }
	public static GridLayout.Alignment TopAlighment { get; set; }
```

Added properties:

```
public static GridLayout.Alignment BaselineAlighment { get; }
	public static GridLayout.Alignment BottomAlighment { get; }
	public static GridLayout.Alignment Center { get; }
	public static GridLayout.Alignment End { get; }
	public static GridLayout.Alignment Fill { get; }
	public static GridLayout.Alignment LeftAlighment { get; }
	public static GridLayout.Alignment RightAlighment { get; }
	public static GridLayout.Alignment Start { get; }
	public static GridLayout.Alignment TopAlighment { get; }
```

### Type Changed: Android.Widget.ImageView

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetAlpha (int alpha);
```

### Type Changed: Android.Widget.ImageView.ScaleType

Removed properties:

```
public static ImageView.ScaleType Center { get; set; }
	public static ImageView.ScaleType CenterCrop { get; set; }
	public static ImageView.ScaleType CenterInside { get; set; }
	public static ImageView.ScaleType FitCenter { get; set; }
	public static ImageView.ScaleType FitEnd { get; set; }
	public static ImageView.ScaleType FitStart { get; set; }
	public static ImageView.ScaleType FitXy { get; set; }
	public static ImageView.ScaleType Matrix { get; set; }
```

Added properties:

```
public static ImageView.ScaleType Center { get; }
	public static ImageView.ScaleType CenterCrop { get; }
	public static ImageView.ScaleType CenterInside { get; }
	public static ImageView.ScaleType FitCenter { get; }
	public static ImageView.ScaleType FitEnd { get; }
	public static ImageView.ScaleType FitStart { get; }
	public static ImageView.ScaleType FitXy { get; }
	public static ImageView.ScaleType Matrix { get; }
```

### Type Changed: Android.Widget.ListView

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual long[] GetCheckItemIds ();
```

### Type Changed: Android.Widget.RemoteViews

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void SetRemoteAdapter (int appWidgetId, int viewId, Android.Content.Intent intent);
```

### Type Changed: Android.Widget.ShareActionProvider

Obsoleted method:

```
[Obsolete ("deprecated")]
	public override Android.Views.View OnCreateActionView ();
```

### Type Changed: Android.Widget.TextClock

Removed properties:

```
public static Java.Lang.ICharSequence DefaultFormat12Hour { get; set; }
	public static Java.Lang.ICharSequence DefaultFormat24Hour { get; set; }
```

Added properties:

```
public static Java.Lang.ICharSequence DefaultFormat12Hour { get; }
	public static Java.Lang.ICharSequence DefaultFormat24Hour { get; }
```

### Type Changed: Android.Widget.TextView

Removed properties:

```
public int CurrentHintTextColor { get; }
	public int CurrentTextColor { get; }
```

Added properties:

```
public Android.Graphics.Color CurrentHintTextColor { get; }
	public Android.Graphics.Color CurrentTextColor { get; }
```

Removed method:

```
public static int GetTextColor (Android.Content.Context context, Android.Content.Res.TypedArray attrs, int def);
```

Added method:

```
public static Android.Graphics.Color GetTextColor (Android.Content.Context context, Android.Content.Res.TypedArray attrs, int def);
```

### Type Changed: Android.Widget.TextView.BufferType

Removed properties:

```
public static TextView.BufferType Editable { get; set; }
	public static TextView.BufferType Normal { get; set; }
	public static TextView.BufferType Spannable { get; set; }
```

Added properties:

```
public static TextView.BufferType Editable { get; }
	public static TextView.BufferType Normal { get; }
	public static TextView.BufferType Spannable { get; }
```

### Type Changed: Android.Widget.TextView.SavedState

Removed property:

```
public static Android.OS.IParcelableCreator Creator { get; set; }
```

Added property:

```
public static Android.OS.IParcelableCreator Creator { get; }
```

## Namespace Dalvik.Bytecode

### Type Changed: Dalvik.Bytecode.OpcodeInfo

Removed properties:

```
public static int MaximumPackedValue { get; set; }
	public static int MaximumValue { get; set; }
```

Added properties:

```
public static int MaximumPackedValue { get; }
	public static int MaximumValue { get; }
```

## Namespace Dalvik.SystemInterop

### Type Changed: Dalvik.SystemInterop.VMDebug

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static void StartMethodTracing ();
```

### Type Changed: Dalvik.SystemInterop.Zygote

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static int ForkAndSpecialize (int uid, int gid, int[] gids, bool enableDebugger, int[][] rlimits);

	[Obsolete ("deprecated")]
	public static int ForkSystemServer (int uid, int gid, int[] gids, bool enableDebugger, int[][] rlimits);
```

## Namespace Java.Awt.Font

### Type Changed: Java.Awt.Font.TextAttribute

Removed properties:

```
public static TextAttribute Background { get; set; }
	public static TextAttribute BidiEmbedding { get; set; }
	public static TextAttribute CharReplacement { get; set; }
	public static TextAttribute Family { get; set; }
	public static TextAttribute Font { get; set; }
	public static TextAttribute Foreground { get; set; }
	public static TextAttribute InputMethodHighlight { get; set; }
	public static TextAttribute InputMethodUnderline { get; set; }
	public static TextAttribute Justification { get; set; }
	public static Java.Lang.Float JustificationFull { get; set; }
	public static Java.Lang.Float JustificationNone { get; set; }
	public static TextAttribute Kerning { get; set; }
	public static Java.Lang.Integer KerningOn { get; set; }
	public static TextAttribute Ligatures { get; set; }
	public static Java.Lang.Integer LigaturesOn { get; set; }
	public static TextAttribute NumericShaping { get; set; }
	public static TextAttribute Posture { get; set; }
	public static Java.Lang.Float PostureOblique { get; set; }
	public static Java.Lang.Float PostureRegular { get; set; }
	public static TextAttribute RunDirection { get; set; }
	public static Java.Lang.Boolean RunDirectionLtr { get; set; }
	public static Java.Lang.Boolean RunDirectionRtl { get; set; }
	public static TextAttribute Size { get; set; }
	public static TextAttribute Strikethrough { get; set; }
	public static Java.Lang.Boolean StrikethroughOn { get; set; }
	public static TextAttribute Superscript { get; set; }
	public static Java.Lang.Integer SuperscriptSub { get; set; }
	public static Java.Lang.Integer SuperscriptSuper { get; set; }
	public static TextAttribute SwapColors { get; set; }
	public static Java.Lang.Boolean SwapColorsOn { get; set; }
	public static TextAttribute Tracking { get; set; }
	public static Java.Lang.Float TrackingLoose { get; set; }
	public static Java.Lang.Float TrackingTight { get; set; }
	public static TextAttribute Transform { get; set; }
	public static TextAttribute Underline { get; set; }
	public static Java.Lang.Integer UnderlineLowDashed { get; set; }
	public static Java.Lang.Integer UnderlineLowDotted { get; set; }
	public static Java.Lang.Integer UnderlineLowGray { get; set; }
	public static Java.Lang.Integer UnderlineLowOnePixel { get; set; }
	public static Java.Lang.Integer UnderlineLowTwoPixel { get; set; }
	public static Java.Lang.Integer UnderlineOn { get; set; }
	public static TextAttribute Weight { get; set; }
	public static Java.Lang.Float WeightBold { get; set; }
	public static Java.Lang.Float WeightDemibold { get; set; }
	public static Java.Lang.Float WeightDemilight { get; set; }
	public static Java.Lang.Float WeightExtrabold { get; set; }
	public static Java.Lang.Float WeightExtraLight { get; set; }
	public static Java.Lang.Float WeightHeavy { get; set; }
	public static Java.Lang.Float WeightLight { get; set; }
	public static Java.Lang.Float WeightMedium { get; set; }
	public static Java.Lang.Float WeightRegular { get; set; }
	public static Java.Lang.Float WeightSemibold { get; set; }
	public static Java.Lang.Float WeightUltrabold { get; set; }
	public static TextAttribute Width { get; set; }
	public static Java.Lang.Float WidthCondensed { get; set; }
	public static Java.Lang.Float WidthExtended { get; set; }
	public static Java.Lang.Float WidthRegular { get; set; }
	public static Java.Lang.Float WidthSemiCondensed { get; set; }
	public static Java.Lang.Float WidthSemiExtended { get; set; }
```

Added properties:

```
public static TextAttribute Background { get; }
	public static TextAttribute BidiEmbedding { get; }
	public static TextAttribute CharReplacement { get; }
	public static TextAttribute Family { get; }
	public static TextAttribute Font { get; }
	public static TextAttribute Foreground { get; }
	public static TextAttribute InputMethodHighlight { get; }
	public static TextAttribute InputMethodUnderline { get; }
	public static TextAttribute Justification { get; }
	public static Java.Lang.Float JustificationFull { get; }
	public static Java.Lang.Float JustificationNone { get; }
	public static TextAttribute Kerning { get; }
	public static Java.Lang.Integer KerningOn { get; }
	public static TextAttribute Ligatures { get; }
	public static Java.Lang.Integer LigaturesOn { get; }
	public static TextAttribute NumericShaping { get; }
	public static TextAttribute Posture { get; }
	public static Java.Lang.Float PostureOblique { get; }
	public static Java.Lang.Float PostureRegular { get; }
	public static TextAttribute RunDirection { get; }
	public static Java.Lang.Boolean RunDirectionLtr { get; }
	public static Java.Lang.Boolean RunDirectionRtl { get; }
	public static TextAttribute Size { get; }
	public static TextAttribute Strikethrough { get; }
	public static Java.Lang.Boolean StrikethroughOn { get; }
	public static TextAttribute Superscript { get; }
	public static Java.Lang.Integer SuperscriptSub { get; }
	public static Java.Lang.Integer SuperscriptSuper { get; }
	public static TextAttribute SwapColors { get; }
	public static Java.Lang.Boolean SwapColorsOn { get; }
	public static TextAttribute Tracking { get; }
	public static Java.Lang.Float TrackingLoose { get; }
	public static Java.Lang.Float TrackingTight { get; }
	public static TextAttribute Transform { get; }
	public static TextAttribute Underline { get; }
	public static Java.Lang.Integer UnderlineLowDashed { get; }
	public static Java.Lang.Integer UnderlineLowDotted { get; }
	public static Java.Lang.Integer UnderlineLowGray { get; }
	public static Java.Lang.Integer UnderlineLowOnePixel { get; }
	public static Java.Lang.Integer UnderlineLowTwoPixel { get; }
	public static Java.Lang.Integer UnderlineOn { get; }
	public static TextAttribute Weight { get; }
	public static Java.Lang.Float WeightBold { get; }
	public static Java.Lang.Float WeightDemibold { get; }
	public static Java.Lang.Float WeightDemilight { get; }
	public static Java.Lang.Float WeightExtrabold { get; }
	public static Java.Lang.Float WeightExtraLight { get; }
	public static Java.Lang.Float WeightHeavy { get; }
	public static Java.Lang.Float WeightLight { get; }
	public static Java.Lang.Float WeightMedium { get; }
	public static Java.Lang.Float WeightRegular { get; }
	public static Java.Lang.Float WeightSemibold { get; }
	public static Java.Lang.Float WeightUltrabold { get; }
	public static TextAttribute Width { get; }
	public static Java.Lang.Float WidthCondensed { get; }
	public static Java.Lang.Float WidthExtended { get; }
	public static Java.Lang.Float WidthRegular { get; }
	public static Java.Lang.Float WidthSemiCondensed { get; }
	public static Java.Lang.Float WidthSemiExtended { get; }
```

## Namespace Java.IO

### Type Changed: Java.IO.ByteArrayOutputStream

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual string ToString (int hibyte);
```

### Type Changed: Java.IO.DataInputStream

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual string ReadLine ();
```

### Type Changed: Java.IO.File

Removed properties:

```
public static string PathSeparator { get; set; }
	public static char PathSeparatorChar { get; set; }
	public static string Separator { get; set; }
	public static char SeparatorChar { get; set; }
```

Added properties:

```
public static string PathSeparator { get; }
	public static char PathSeparatorChar { get; }
	public static string Separator { get; }
	public static char SeparatorChar { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual Java.Net.URL ToURL ();
```

### Type Changed: Java.IO.FileDescriptor

Removed properties:

```
public static FileDescriptor Err { get; set; }
	public static FileDescriptor In { get; set; }
	public static FileDescriptor Out { get; set; }
```

Added properties:

```
public static FileDescriptor Err { get; }
	public static FileDescriptor In { get; }
	public static FileDescriptor Out { get; }
```

### Type Changed: Java.IO.ObjectInputStream

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual string ReadLine ();
```

### Type Changed: Java.IO.ObjectInputStream.InterfaceConsts

Removed properties:

```
public static SerializablePermission SubclassImplementationPermission { get; set; }
	public static SerializablePermission SubstitutionPermission { get; set; }
```

Added properties:

```
public static SerializablePermission SubclassImplementationPermission { get; }
	public static SerializablePermission SubstitutionPermission { get; }
```

### Type Changed: Java.IO.ObjectOutputStream

### Type Changed: Java.IO.ObjectOutputStream.InterfaceConsts

Removed properties:

```
public static SerializablePermission SubclassImplementationPermission { get; set; }
	public static SerializablePermission SubstitutionPermission { get; set; }
```

Added properties:

```
public static SerializablePermission SubclassImplementationPermission { get; }
	public static SerializablePermission SubstitutionPermission { get; }
```

### Type Changed: Java.IO.ObjectStreamClass

Removed property:

```
public static System.Collections.Generic.IList<ObjectStreamField> NoFields { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<ObjectStreamField> NoFields { get; }
```

### Type Changed: Java.IO.ObjectStreamConstants

Removed properties:

```
public static SerializablePermission SubclassImplementationPermission { get; set; }
	public static SerializablePermission SubstitutionPermission { get; set; }
```

Added properties:

```
public static SerializablePermission SubclassImplementationPermission { get; }
	public static SerializablePermission SubstitutionPermission { get; }
```

## Namespace Java.Lang

### Type Changed: Java.Lang.Boolean

Removed properties:

```
public static Boolean False { get; set; }
	public static Boolean True { get; set; }
	public static Class Type { get; set; }
```

Added properties:

```
public static Boolean False { get; }
	public static Boolean True { get; }
	public static Class Type { get; }
```

### Type Changed: Java.Lang.Byte

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

### Type Changed: Java.Lang.Character

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static bool IsJavaLetter (char c);

	[Obsolete ("deprecated")]
	public static bool IsJavaLetterOrDigit (char c);

	[Obsolete ("deprecated")]
	public static bool IsSpace (char c);
```

### Type Changed: Java.Lang.Character.UnicodeBlock

Removed properties:

```
public static Character.UnicodeBlock AegeanNumbers { get; set; }
	public static Character.UnicodeBlock AlchemicalSymbols { get; set; }
	public static Character.UnicodeBlock AlphabeticPresentationForms { get; set; }
	public static Character.UnicodeBlock AncientGreekMusicalNotation { get; set; }
	public static Character.UnicodeBlock AncientGreekNumbers { get; set; }
	public static Character.UnicodeBlock AncientSymbols { get; set; }
	public static Character.UnicodeBlock Arabic { get; set; }
	public static Character.UnicodeBlock ArabicPresentationFormsA { get; set; }
	public static Character.UnicodeBlock ArabicPresentationFormsB { get; set; }
	public static Character.UnicodeBlock ArabicSupplement { get; set; }
	public static Character.UnicodeBlock Armenian { get; set; }
	public static Character.UnicodeBlock Arrows { get; set; }
	public static Character.UnicodeBlock Avestan { get; set; }
	public static Character.UnicodeBlock Balinese { get; set; }
	public static Character.UnicodeBlock Bamum { get; set; }
	public static Character.UnicodeBlock BamumSupplement { get; set; }
	public static Character.UnicodeBlock BasicLatin { get; set; }
	public static Character.UnicodeBlock Batak { get; set; }
	public static Character.UnicodeBlock Bengali { get; set; }
	public static Character.UnicodeBlock BlockElements { get; set; }
	public static Character.UnicodeBlock Bopomofo { get; set; }
	public static Character.UnicodeBlock BopomofoExtended { get; set; }
	public static Character.UnicodeBlock BoxDrawing { get; set; }
	public static Character.UnicodeBlock Brahmi { get; set; }
	public static Character.UnicodeBlock BraillePatterns { get; set; }
	public static Character.UnicodeBlock Buginese { get; set; }
	public static Character.UnicodeBlock Buhid { get; set; }
	public static Character.UnicodeBlock ByzantineMusicalSymbols { get; set; }
	public static Character.UnicodeBlock Carian { get; set; }
	public static Character.UnicodeBlock Cham { get; set; }
	public static Character.UnicodeBlock Cherokee { get; set; }
	public static Character.UnicodeBlock CjkCompatibility { get; set; }
	public static Character.UnicodeBlock CjkCompatibilityForms { get; set; }
	public static Character.UnicodeBlock CjkCompatibilityIdeographs { get; set; }
	public static Character.UnicodeBlock CjkCompatibilityIdeographsSupplement { get; set; }
	public static Character.UnicodeBlock CjkRadicalsSupplement { get; set; }
	public static Character.UnicodeBlock CjkStrokes { get; set; }
	public static Character.UnicodeBlock CjkSymbolsAndPunctuation { get; set; }
	public static Character.UnicodeBlock CjkUnifiedIdeographs { get; set; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionA { get; set; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionB { get; set; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionC { get; set; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionD { get; set; }
	public static Character.UnicodeBlock CombiningDiacriticalMarks { get; set; }
	public static Character.UnicodeBlock CombiningDiacriticalMarksSupplement { get; set; }
	public static Character.UnicodeBlock CombiningHalfMarks { get; set; }
	public static Character.UnicodeBlock CombiningMarksForSymbols { get; set; }
	public static Character.UnicodeBlock CommonIndicNumberForms { get; set; }
	public static Character.UnicodeBlock ControlPictures { get; set; }
	public static Character.UnicodeBlock Coptic { get; set; }
	public static Character.UnicodeBlock CountingRodNumerals { get; set; }
	public static Character.UnicodeBlock Cuneiform { get; set; }
	public static Character.UnicodeBlock CuneiformNumbersAndPunctuation { get; set; }
	public static Character.UnicodeBlock CurrencySymbols { get; set; }
	public static Character.UnicodeBlock CypriotSyllabary { get; set; }
	public static Character.UnicodeBlock Cyrillic { get; set; }
	public static Character.UnicodeBlock CyrillicExtendedA { get; set; }
	public static Character.UnicodeBlock CyrillicExtendedB { get; set; }
	public static Character.UnicodeBlock CyrillicSupplementary { get; set; }
	public static Character.UnicodeBlock Deseret { get; set; }
	public static Character.UnicodeBlock Devanagari { get; set; }
	public static Character.UnicodeBlock DevanagariExtended { get; set; }
	public static Character.UnicodeBlock Dingbats { get; set; }
	public static Character.UnicodeBlock DominoTiles { get; set; }
	public static Character.UnicodeBlock EgyptianHieroglyphs { get; set; }
	public static Character.UnicodeBlock Emoticons { get; set; }
	public static Character.UnicodeBlock EnclosedAlphanumerics { get; set; }
	public static Character.UnicodeBlock EnclosedAlphanumericSupplement { get; set; }
	public static Character.UnicodeBlock EnclosedCjkLettersAndMonths { get; set; }
	public static Character.UnicodeBlock EnclosedIdeographicSupplement { get; set; }
	public static Character.UnicodeBlock Ethiopic { get; set; }
	public static Character.UnicodeBlock EthiopicExtended { get; set; }
	public static Character.UnicodeBlock EthiopicExtendedA { get; set; }
	public static Character.UnicodeBlock EthiopicSupplement { get; set; }
	public static Character.UnicodeBlock GeneralPunctuation { get; set; }
	public static Character.UnicodeBlock GeometricShapes { get; set; }
	public static Character.UnicodeBlock Georgian { get; set; }
	public static Character.UnicodeBlock GeorgianSupplement { get; set; }
	public static Character.UnicodeBlock Glagolitic { get; set; }
	public static Character.UnicodeBlock Gothic { get; set; }
	public static Character.UnicodeBlock Greek { get; set; }
	public static Character.UnicodeBlock GreekExtended { get; set; }
	public static Character.UnicodeBlock Gujarati { get; set; }
	public static Character.UnicodeBlock Gurmukhi { get; set; }
	public static Character.UnicodeBlock HalfwidthAndFullwidthForms { get; set; }
	public static Character.UnicodeBlock HangulCompatibilityJamo { get; set; }
	public static Character.UnicodeBlock HangulJamo { get; set; }
	public static Character.UnicodeBlock HangulJamoExtendedA { get; set; }
	public static Character.UnicodeBlock HangulJamoExtendedB { get; set; }
	public static Character.UnicodeBlock HangulSyllables { get; set; }
	public static Character.UnicodeBlock Hanunoo { get; set; }
	public static Character.UnicodeBlock Hebrew { get; set; }
	public static Character.UnicodeBlock HighPrivateUseSurrogates { get; set; }
	public static Character.UnicodeBlock HighSurrogates { get; set; }
	public static Character.UnicodeBlock Hiragana { get; set; }
	public static Character.UnicodeBlock IdeographicDescriptionCharacters { get; set; }
	public static Character.UnicodeBlock ImperialAramaic { get; set; }
	public static Character.UnicodeBlock InscriptionalPahlavi { get; set; }
	public static Character.UnicodeBlock InscriptionalParthian { get; set; }
	public static Character.UnicodeBlock IpaExtensions { get; set; }
	public static Character.UnicodeBlock Javanese { get; set; }
	public static Character.UnicodeBlock Kaithi { get; set; }
	public static Character.UnicodeBlock KanaSupplement { get; set; }
	public static Character.UnicodeBlock Kanbun { get; set; }
	public static Character.UnicodeBlock KangxiRadicals { get; set; }
	public static Character.UnicodeBlock Kannada { get; set; }
	public static Character.UnicodeBlock Katakana { get; set; }
	public static Character.UnicodeBlock KatakanaPhoneticExtensions { get; set; }
	public static Character.UnicodeBlock KayahLi { get; set; }
	public static Character.UnicodeBlock Kharoshthi { get; set; }
	public static Character.UnicodeBlock Khmer { get; set; }
	public static Character.UnicodeBlock KhmerSymbols { get; set; }
	public static Character.UnicodeBlock Lao { get; set; }
	public static Character.UnicodeBlock Latin1Supplement { get; set; }
	public static Character.UnicodeBlock LatinExtendedA { get; set; }
	public static Character.UnicodeBlock LatinExtendedAdditional { get; set; }
	public static Character.UnicodeBlock LatinExtendedB { get; set; }
	public static Character.UnicodeBlock LatinExtendedC { get; set; }
	public static Character.UnicodeBlock LatinExtendedD { get; set; }
	public static Character.UnicodeBlock Lepcha { get; set; }
	public static Character.UnicodeBlock LetterlikeSymbols { get; set; }
	public static Character.UnicodeBlock Limbu { get; set; }
	public static Character.UnicodeBlock LinearBIdeograms { get; set; }
	public static Character.UnicodeBlock LinearBSyllabary { get; set; }
	public static Character.UnicodeBlock Lisu { get; set; }
	public static Character.UnicodeBlock LowSurrogates { get; set; }
	public static Character.UnicodeBlock Lycian { get; set; }
	public static Character.UnicodeBlock Lydian { get; set; }
	public static Character.UnicodeBlock MahjongTiles { get; set; }
	public static Character.UnicodeBlock Malayalam { get; set; }
	public static Character.UnicodeBlock Mandaic { get; set; }
	public static Character.UnicodeBlock MathematicalAlphanumericSymbols { get; set; }
	public static Character.UnicodeBlock MathematicalOperators { get; set; }
	public static Character.UnicodeBlock MeeteiMayek { get; set; }
	public static Character.UnicodeBlock MiscellaneousMathematicalSymbolsA { get; set; }
	public static Character.UnicodeBlock MiscellaneousMathematicalSymbolsB { get; set; }
	public static Character.UnicodeBlock MiscellaneousSymbols { get; set; }
	public static Character.UnicodeBlock MiscellaneousSymbolsAndArrows { get; set; }
	public static Character.UnicodeBlock MiscellaneousSymbolsAndPictographs { get; set; }
	public static Character.UnicodeBlock MiscellaneousTechnical { get; set; }
	public static Character.UnicodeBlock ModifierToneLetters { get; set; }
	public static Character.UnicodeBlock Mongolian { get; set; }
	public static Character.UnicodeBlock MusicalSymbols { get; set; }
	public static Character.UnicodeBlock Myanmar { get; set; }
	public static Character.UnicodeBlock MyanmarExtendedA { get; set; }
	public static Character.UnicodeBlock NewTaiLue { get; set; }
	public static Character.UnicodeBlock Nko { get; set; }
	public static Character.UnicodeBlock NumberForms { get; set; }
	public static Character.UnicodeBlock Ogham { get; set; }
	public static Character.UnicodeBlock OlChiki { get; set; }
	public static Character.UnicodeBlock OldItalic { get; set; }
	public static Character.UnicodeBlock OldPersian { get; set; }
	public static Character.UnicodeBlock OldSouthArabian { get; set; }
	public static Character.UnicodeBlock OldTurkic { get; set; }
	public static Character.UnicodeBlock OpticalCharacterRecognition { get; set; }
	public static Character.UnicodeBlock Oriya { get; set; }
	public static Character.UnicodeBlock Osmanya { get; set; }
	public static Character.UnicodeBlock PhagsPa { get; set; }
	public static Character.UnicodeBlock PhaistosDisc { get; set; }
	public static Character.UnicodeBlock Phoenician { get; set; }
	public static Character.UnicodeBlock PhoneticExtensions { get; set; }
	public static Character.UnicodeBlock PhoneticExtensionsSupplement { get; set; }
	public static Character.UnicodeBlock PlayingCards { get; set; }
	public static Character.UnicodeBlock PrivateUseArea { get; set; }
	public static Character.UnicodeBlock Rejang { get; set; }
	public static Character.UnicodeBlock RumiNumeralSymbols { get; set; }
	public static Character.UnicodeBlock Runic { get; set; }
	public static Character.UnicodeBlock Samaritan { get; set; }
	public static Character.UnicodeBlock Saurashtra { get; set; }
	public static Character.UnicodeBlock Shavian { get; set; }
	public static Character.UnicodeBlock Sinhala { get; set; }
	public static Character.UnicodeBlock SmallFormVariants { get; set; }
	public static Character.UnicodeBlock SpacingModifierLetters { get; set; }
	public static Character.UnicodeBlock Specials { get; set; }
	public static Character.UnicodeBlock Sundanese { get; set; }
	public static Character.UnicodeBlock SuperscriptsAndSubscripts { get; set; }
	public static Character.UnicodeBlock SupplementalArrowsA { get; set; }
	public static Character.UnicodeBlock SupplementalArrowsB { get; set; }
	public static Character.UnicodeBlock SupplementalMathematicalOperators { get; set; }
	public static Character.UnicodeBlock SupplementalPunctuation { get; set; }
	public static Character.UnicodeBlock SupplementaryPrivateUseAreaA { get; set; }
	public static Character.UnicodeBlock SupplementaryPrivateUseAreaB { get; set; }
	public static Character.UnicodeBlock SurrogatesArea { get; set; }
	public static Character.UnicodeBlock SylotiNagri { get; set; }
	public static Character.UnicodeBlock Syriac { get; set; }
	public static Character.UnicodeBlock Tagalog { get; set; }
	public static Character.UnicodeBlock Tagbanwa { get; set; }
	public static Character.UnicodeBlock Tags { get; set; }
	public static Character.UnicodeBlock TaiLe { get; set; }
	public static Character.UnicodeBlock TaiTham { get; set; }
	public static Character.UnicodeBlock TaiViet { get; set; }
	public static Character.UnicodeBlock TaiXuanJingSymbols { get; set; }
	public static Character.UnicodeBlock Tamil { get; set; }
	public static Character.UnicodeBlock Telugu { get; set; }
	public static Character.UnicodeBlock Thaana { get; set; }
	public static Character.UnicodeBlock Thai { get; set; }
	public static Character.UnicodeBlock Tibetan { get; set; }
	public static Character.UnicodeBlock Tifinagh { get; set; }
	public static Character.UnicodeBlock TransportAndMapSymbols { get; set; }
	public static Character.UnicodeBlock Ugaritic { get; set; }
	public static Character.UnicodeBlock UnifiedCanadianAboriginalSyllabics { get; set; }
	public static Character.UnicodeBlock UnifiedCanadianAboriginalSyllabicsExtended { get; set; }
	public static Character.UnicodeBlock Vai { get; set; }
	public static Character.UnicodeBlock VariationSelectors { get; set; }
	public static Character.UnicodeBlock VariationSelectorsSupplement { get; set; }
	public static Character.UnicodeBlock VedicExtensions { get; set; }
	public static Character.UnicodeBlock VerticalForms { get; set; }
	public static Character.UnicodeBlock YijingHexagramSymbols { get; set; }
	public static Character.UnicodeBlock YiRadicals { get; set; }
	public static Character.UnicodeBlock YiSyllables { get; set; }
```

Added properties:

```
public static Character.UnicodeBlock AegeanNumbers { get; }
	public static Character.UnicodeBlock AlchemicalSymbols { get; }
	public static Character.UnicodeBlock AlphabeticPresentationForms { get; }
	public static Character.UnicodeBlock AncientGreekMusicalNotation { get; }
	public static Character.UnicodeBlock AncientGreekNumbers { get; }
	public static Character.UnicodeBlock AncientSymbols { get; }
	public static Character.UnicodeBlock Arabic { get; }
	public static Character.UnicodeBlock ArabicPresentationFormsA { get; }
	public static Character.UnicodeBlock ArabicPresentationFormsB { get; }
	public static Character.UnicodeBlock ArabicSupplement { get; }
	public static Character.UnicodeBlock Armenian { get; }
	public static Character.UnicodeBlock Arrows { get; }
	public static Character.UnicodeBlock Avestan { get; }
	public static Character.UnicodeBlock Balinese { get; }
	public static Character.UnicodeBlock Bamum { get; }
	public static Character.UnicodeBlock BamumSupplement { get; }
	public static Character.UnicodeBlock BasicLatin { get; }
	public static Character.UnicodeBlock Batak { get; }
	public static Character.UnicodeBlock Bengali { get; }
	public static Character.UnicodeBlock BlockElements { get; }
	public static Character.UnicodeBlock Bopomofo { get; }
	public static Character.UnicodeBlock BopomofoExtended { get; }
	public static Character.UnicodeBlock BoxDrawing { get; }
	public static Character.UnicodeBlock Brahmi { get; }
	public static Character.UnicodeBlock BraillePatterns { get; }
	public static Character.UnicodeBlock Buginese { get; }
	public static Character.UnicodeBlock Buhid { get; }
	public static Character.UnicodeBlock ByzantineMusicalSymbols { get; }
	public static Character.UnicodeBlock Carian { get; }
	public static Character.UnicodeBlock Cham { get; }
	public static Character.UnicodeBlock Cherokee { get; }
	public static Character.UnicodeBlock CjkCompatibility { get; }
	public static Character.UnicodeBlock CjkCompatibilityForms { get; }
	public static Character.UnicodeBlock CjkCompatibilityIdeographs { get; }
	public static Character.UnicodeBlock CjkCompatibilityIdeographsSupplement { get; }
	public static Character.UnicodeBlock CjkRadicalsSupplement { get; }
	public static Character.UnicodeBlock CjkStrokes { get; }
	public static Character.UnicodeBlock CjkSymbolsAndPunctuation { get; }
	public static Character.UnicodeBlock CjkUnifiedIdeographs { get; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionA { get; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionB { get; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionC { get; }
	public static Character.UnicodeBlock CjkUnifiedIdeographsExtensionD { get; }
	public static Character.UnicodeBlock CombiningDiacriticalMarks { get; }
	public static Character.UnicodeBlock CombiningDiacriticalMarksSupplement { get; }
	public static Character.UnicodeBlock CombiningHalfMarks { get; }
	public static Character.UnicodeBlock CombiningMarksForSymbols { get; }
	public static Character.UnicodeBlock CommonIndicNumberForms { get; }
	public static Character.UnicodeBlock ControlPictures { get; }
	public static Character.UnicodeBlock Coptic { get; }
	public static Character.UnicodeBlock CountingRodNumerals { get; }
	public static Character.UnicodeBlock Cuneiform { get; }
	public static Character.UnicodeBlock CuneiformNumbersAndPunctuation { get; }
	public static Character.UnicodeBlock CurrencySymbols { get; }
	public static Character.UnicodeBlock CypriotSyllabary { get; }
	public static Character.UnicodeBlock Cyrillic { get; }
	public static Character.UnicodeBlock CyrillicExtendedA { get; }
	public static Character.UnicodeBlock CyrillicExtendedB { get; }
	public static Character.UnicodeBlock CyrillicSupplementary { get; }
	public static Character.UnicodeBlock Deseret { get; }
	public static Character.UnicodeBlock Devanagari { get; }
	public static Character.UnicodeBlock DevanagariExtended { get; }
	public static Character.UnicodeBlock Dingbats { get; }
	public static Character.UnicodeBlock DominoTiles { get; }
	public static Character.UnicodeBlock EgyptianHieroglyphs { get; }
	public static Character.UnicodeBlock Emoticons { get; }
	public static Character.UnicodeBlock EnclosedAlphanumerics { get; }
	public static Character.UnicodeBlock EnclosedAlphanumericSupplement { get; }
	public static Character.UnicodeBlock EnclosedCjkLettersAndMonths { get; }
	public static Character.UnicodeBlock EnclosedIdeographicSupplement { get; }
	public static Character.UnicodeBlock Ethiopic { get; }
	public static Character.UnicodeBlock EthiopicExtended { get; }
	public static Character.UnicodeBlock EthiopicExtendedA { get; }
	public static Character.UnicodeBlock EthiopicSupplement { get; }
	public static Character.UnicodeBlock GeneralPunctuation { get; }
	public static Character.UnicodeBlock GeometricShapes { get; }
	public static Character.UnicodeBlock Georgian { get; }
	public static Character.UnicodeBlock GeorgianSupplement { get; }
	public static Character.UnicodeBlock Glagolitic { get; }
	public static Character.UnicodeBlock Gothic { get; }
	public static Character.UnicodeBlock Greek { get; }
	public static Character.UnicodeBlock GreekExtended { get; }
	public static Character.UnicodeBlock Gujarati { get; }
	public static Character.UnicodeBlock Gurmukhi { get; }
	public static Character.UnicodeBlock HalfwidthAndFullwidthForms { get; }
	public static Character.UnicodeBlock HangulCompatibilityJamo { get; }
	public static Character.UnicodeBlock HangulJamo { get; }
	public static Character.UnicodeBlock HangulJamoExtendedA { get; }
	public static Character.UnicodeBlock HangulJamoExtendedB { get; }
	public static Character.UnicodeBlock HangulSyllables { get; }
	public static Character.UnicodeBlock Hanunoo { get; }
	public static Character.UnicodeBlock Hebrew { get; }
	public static Character.UnicodeBlock HighPrivateUseSurrogates { get; }
	public static Character.UnicodeBlock HighSurrogates { get; }
	public static Character.UnicodeBlock Hiragana { get; }
	public static Character.UnicodeBlock IdeographicDescriptionCharacters { get; }
	public static Character.UnicodeBlock ImperialAramaic { get; }
	public static Character.UnicodeBlock InscriptionalPahlavi { get; }
	public static Character.UnicodeBlock InscriptionalParthian { get; }
	public static Character.UnicodeBlock IpaExtensions { get; }
	public static Character.UnicodeBlock Javanese { get; }
	public static Character.UnicodeBlock Kaithi { get; }
	public static Character.UnicodeBlock KanaSupplement { get; }
	public static Character.UnicodeBlock Kanbun { get; }
	public static Character.UnicodeBlock KangxiRadicals { get; }
	public static Character.UnicodeBlock Kannada { get; }
	public static Character.UnicodeBlock Katakana { get; }
	public static Character.UnicodeBlock KatakanaPhoneticExtensions { get; }
	public static Character.UnicodeBlock KayahLi { get; }
	public static Character.UnicodeBlock Kharoshthi { get; }
	public static Character.UnicodeBlock Khmer { get; }
	public static Character.UnicodeBlock KhmerSymbols { get; }
	public static Character.UnicodeBlock Lao { get; }
	public static Character.UnicodeBlock Latin1Supplement { get; }
	public static Character.UnicodeBlock LatinExtendedA { get; }
	public static Character.UnicodeBlock LatinExtendedAdditional { get; }
	public static Character.UnicodeBlock LatinExtendedB { get; }
	public static Character.UnicodeBlock LatinExtendedC { get; }
	public static Character.UnicodeBlock LatinExtendedD { get; }
	public static Character.UnicodeBlock Lepcha { get; }
	public static Character.UnicodeBlock LetterlikeSymbols { get; }
	public static Character.UnicodeBlock Limbu { get; }
	public static Character.UnicodeBlock LinearBIdeograms { get; }
	public static Character.UnicodeBlock LinearBSyllabary { get; }
	public static Character.UnicodeBlock Lisu { get; }
	public static Character.UnicodeBlock LowSurrogates { get; }
	public static Character.UnicodeBlock Lycian { get; }
	public static Character.UnicodeBlock Lydian { get; }
	public static Character.UnicodeBlock MahjongTiles { get; }
	public static Character.UnicodeBlock Malayalam { get; }
	public static Character.UnicodeBlock Mandaic { get; }
	public static Character.UnicodeBlock MathematicalAlphanumericSymbols { get; }
	public static Character.UnicodeBlock MathematicalOperators { get; }
	public static Character.UnicodeBlock MeeteiMayek { get; }
	public static Character.UnicodeBlock MiscellaneousMathematicalSymbolsA { get; }
	public static Character.UnicodeBlock MiscellaneousMathematicalSymbolsB { get; }
	public static Character.UnicodeBlock MiscellaneousSymbols { get; }
	public static Character.UnicodeBlock MiscellaneousSymbolsAndArrows { get; }
	public static Character.UnicodeBlock MiscellaneousSymbolsAndPictographs { get; }
	public static Character.UnicodeBlock MiscellaneousTechnical { get; }
	public static Character.UnicodeBlock ModifierToneLetters { get; }
	public static Character.UnicodeBlock Mongolian { get; }
	public static Character.UnicodeBlock MusicalSymbols { get; }
	public static Character.UnicodeBlock Myanmar { get; }
	public static Character.UnicodeBlock MyanmarExtendedA { get; }
	public static Character.UnicodeBlock NewTaiLue { get; }
	public static Character.UnicodeBlock Nko { get; }
	public static Character.UnicodeBlock NumberForms { get; }
	public static Character.UnicodeBlock Ogham { get; }
	public static Character.UnicodeBlock OlChiki { get; }
	public static Character.UnicodeBlock OldItalic { get; }
	public static Character.UnicodeBlock OldPersian { get; }
	public static Character.UnicodeBlock OldSouthArabian { get; }
	public static Character.UnicodeBlock OldTurkic { get; }
	public static Character.UnicodeBlock OpticalCharacterRecognition { get; }
	public static Character.UnicodeBlock Oriya { get; }
	public static Character.UnicodeBlock Osmanya { get; }
	public static Character.UnicodeBlock PhagsPa { get; }
	public static Character.UnicodeBlock PhaistosDisc { get; }
	public static Character.UnicodeBlock Phoenician { get; }
	public static Character.UnicodeBlock PhoneticExtensions { get; }
	public static Character.UnicodeBlock PhoneticExtensionsSupplement { get; }
	public static Character.UnicodeBlock PlayingCards { get; }
	public static Character.UnicodeBlock PrivateUseArea { get; }
	public static Character.UnicodeBlock Rejang { get; }
	public static Character.UnicodeBlock RumiNumeralSymbols { get; }
	public static Character.UnicodeBlock Runic { get; }
	public static Character.UnicodeBlock Samaritan { get; }
	public static Character.UnicodeBlock Saurashtra { get; }
	public static Character.UnicodeBlock Shavian { get; }
	public static Character.UnicodeBlock Sinhala { get; }
	public static Character.UnicodeBlock SmallFormVariants { get; }
	public static Character.UnicodeBlock SpacingModifierLetters { get; }
	public static Character.UnicodeBlock Specials { get; }
	public static Character.UnicodeBlock Sundanese { get; }
	public static Character.UnicodeBlock SuperscriptsAndSubscripts { get; }
	public static Character.UnicodeBlock SupplementalArrowsA { get; }
	public static Character.UnicodeBlock SupplementalArrowsB { get; }
	public static Character.UnicodeBlock SupplementalMathematicalOperators { get; }
	public static Character.UnicodeBlock SupplementalPunctuation { get; }
	public static Character.UnicodeBlock SupplementaryPrivateUseAreaA { get; }
	public static Character.UnicodeBlock SupplementaryPrivateUseAreaB { get; }
	public static Character.UnicodeBlock SurrogatesArea { get; }
	public static Character.UnicodeBlock SylotiNagri { get; }
	public static Character.UnicodeBlock Syriac { get; }
	public static Character.UnicodeBlock Tagalog { get; }
	public static Character.UnicodeBlock Tagbanwa { get; }
	public static Character.UnicodeBlock Tags { get; }
	public static Character.UnicodeBlock TaiLe { get; }
	public static Character.UnicodeBlock TaiTham { get; }
	public static Character.UnicodeBlock TaiViet { get; }
	public static Character.UnicodeBlock TaiXuanJingSymbols { get; }
	public static Character.UnicodeBlock Tamil { get; }
	public static Character.UnicodeBlock Telugu { get; }
	public static Character.UnicodeBlock Thaana { get; }
	public static Character.UnicodeBlock Thai { get; }
	public static Character.UnicodeBlock Tibetan { get; }
	public static Character.UnicodeBlock Tifinagh { get; }
	public static Character.UnicodeBlock TransportAndMapSymbols { get; }
	public static Character.UnicodeBlock Ugaritic { get; }
	public static Character.UnicodeBlock UnifiedCanadianAboriginalSyllabics { get; }
	public static Character.UnicodeBlock UnifiedCanadianAboriginalSyllabicsExtended { get; }
	public static Character.UnicodeBlock Vai { get; }
	public static Character.UnicodeBlock VariationSelectors { get; }
	public static Character.UnicodeBlock VariationSelectorsSupplement { get; }
	public static Character.UnicodeBlock VedicExtensions { get; }
	public static Character.UnicodeBlock VerticalForms { get; }
	public static Character.UnicodeBlock YijingHexagramSymbols { get; }
	public static Character.UnicodeBlock YiRadicals { get; }
	public static Character.UnicodeBlock YiSyllables { get; }
```

### Type Changed: Java.Lang.ClassLoader

Obsoleted method:

```
[Obsolete ("deprecated")]
	protected Class DefineClass (byte[] classRep, int offset, int length);
```

### Type Changed: Java.Lang.ClassNotFoundException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.Double

Removed properties:

```
public static int MaxExponent { get; set; }
	public static int MinExponent { get; set; }
	public static double MinNormal { get; set; }
	public static Class Type { get; set; }
```

Added properties:

```
public static int MaxExponent { get; }
	public static int MinExponent { get; }
	public static double MinNormal { get; }
	public static Class Type { get; }
```

### Type Changed: Java.Lang.Exception

Removed constructor:

```
protected Exception (string p0, Throwable p1, bool p2, bool p3);
```

### Type Changed: Java.Lang.Float

Removed properties:

```
public static int MaxExponent { get; set; }
	public static int MinExponent { get; set; }
	public static float MinNormal { get; set; }
	public static Class Type { get; set; }
```

Added properties:

```
public static int MaxExponent { get; }
	public static int MinExponent { get; }
	public static float MinNormal { get; }
	public static Class Type { get; }
```

### Type Changed: Java.Lang.IllegalAccessException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.InstantiationException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.Integer

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

### Type Changed: Java.Lang.JavaSystem

Removed properties:

```
public static Java.IO.PrintStream Err { get; set; }
	public static System.IO.Stream In { get; set; }
	public static Java.IO.PrintStream Out { get; set; }
```

Added properties:

```
public static Java.IO.PrintStream Err { get; }
	public static System.IO.Stream In { get; }
	public static Java.IO.PrintStream Out { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static void RunFinalizersOnExit (bool flag);
```

### Type Changed: Java.Lang.Long

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

### Type Changed: Java.Lang.NoSuchFieldException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.NoSuchMethodException

Added property:

```
[Obsolete ("Use the Cause property. The Clause property was bound in error, and DOES NOT EXIST.")]
	public virtual Throwable Clause { get; }
```

### Type Changed: Java.Lang.Runtime

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetLocalizedInputStream (System.IO.Stream stream);

	[Obsolete ("deprecated")]
	public virtual System.IO.Stream GetLocalizedOutputStream (System.IO.Stream stream);

	[Obsolete ("deprecated")]
	public static void RunFinalizersOnExit (bool run);
```

### Type Changed: Java.Lang.RuntimeException

Removed constructor:

```
protected RuntimeException (string p0, Throwable p1, bool p2, bool p3);
```

### Type Changed: Java.Lang.SecurityManager

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual void CheckMulticast (Java.Net.InetAddress maddr, sbyte ttl);

	[Obsolete ("deprecated")]
	protected virtual int ClassDepth (string name);

	[Obsolete ("deprecated")]
	protected virtual int ClassLoaderDepth ();

	[Obsolete ("deprecated")]
	protected virtual ClassLoader CurrentClassLoader ();

	[Obsolete ("deprecated")]
	protected virtual Class CurrentLoadedClass ();

	[Obsolete ("deprecated")]
	protected virtual bool InClass (string name);

	[Obsolete ("deprecated")]
	protected virtual bool InClassLoader ();
```

### Type Changed: Java.Lang.Short

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

### Type Changed: Java.Lang.String

Removed property:

```
public static Java.Util.IComparator CaseInsensitiveOrder { get; set; }
```

Added property:

```
public static Java.Util.IComparator CaseInsensitiveOrder { get; }
```

Obsoleted method:

```
[Obsolete ("deprecated")]
	public void GetBytes (int start, int end, byte[] data, int index);
```

### Type Changed: Java.Lang.Thread

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual int CountStackFrames ();

	[Obsolete ("deprecated")]
	public virtual void Destroy ();

	[Obsolete ("deprecated")]
	public void Resume ();

	[Obsolete ("deprecated")]
	public void Stop ();

	[Obsolete ("deprecated")]
	public void Stop (Throwable throwable);

	[Obsolete ("deprecated")]
	public void Suspend ();
```

### Type Changed: Java.Lang.Thread.State

Removed properties:

```
public static Thread.State Blocked { get; set; }
	public static Thread.State New { get; set; }
	public static Thread.State Runnable { get; set; }
	public static Thread.State Terminated { get; set; }
	public static Thread.State TimedWaiting { get; set; }
	public static Thread.State Waiting { get; set; }
```

Added properties:

```
public static Thread.State Blocked { get; }
	public static Thread.State New { get; }
	public static Thread.State Runnable { get; }
	public static Thread.State Terminated { get; }
	public static Thread.State TimedWaiting { get; }
	public static Thread.State Waiting { get; }
```

### Type Changed: Java.Lang.ThreadGroup

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual bool AllowThreadSuspension (bool b);

	[Obsolete ("deprecated")]
	public void Resume ();

	[Obsolete ("deprecated")]
	public void Stop ();

	[Obsolete ("deprecated")]
	public void Suspend ();
```

### Type Changed: Java.Lang.Void

Removed property:

```
public static Class Type { get; set; }
```

Added property:

```
public static Class Type { get; }
```

## Namespace Java.Lang.Annotation

### Type Changed: Java.Lang.Annotation.ElementType

Removed properties:

```
public static ElementType AnnotationType { get; set; }
	public static ElementType Constructor { get; set; }
	public static ElementType Field { get; set; }
	public static ElementType LocalVariable { get; set; }
	public static ElementType Method { get; set; }
	public static ElementType Package { get; set; }
	public static ElementType Parameter { get; set; }
	public static ElementType Type { get; set; }
```

Added properties:

```
public static ElementType AnnotationType { get; }
	public static ElementType Constructor { get; }
	public static ElementType Field { get; }
	public static ElementType LocalVariable { get; }
	public static ElementType Method { get; }
	public static ElementType Package { get; }
	public static ElementType Parameter { get; }
	public static ElementType Type { get; }
```

### Type Changed: Java.Lang.Annotation.RetentionPolicy

Removed properties:

```
public static RetentionPolicy Runtime { get; set; }
	public static RetentionPolicy Source { get; set; }
```

Added properties:

```
public static RetentionPolicy Runtime { get; }
	public static RetentionPolicy Source { get; }
```

## Namespace Java.Math

### Type Changed: Java.Math.BigDecimal

Removed properties:

```
public static BigDecimal One { get; set; }
	public static BigDecimal Ten { get; set; }
	public static BigDecimal Zero { get; set; }
```

Added properties:

```
public static BigDecimal One { get; }
	public static BigDecimal Ten { get; }
	public static BigDecimal Zero { get; }
```

### Type Changed: Java.Math.BigInteger

Removed properties:

```
public static BigInteger One { get; set; }
	public static BigInteger Ten { get; set; }
	public static BigInteger Zero { get; set; }
```

Added properties:

```
public static BigInteger One { get; }
	public static BigInteger Ten { get; }
	public static BigInteger Zero { get; }
```

### Type Changed: Java.Math.MathContext

Removed properties:

```
public static MathContext Decimal128 { get; set; }
	public static MathContext Decimal32 { get; set; }
	public static MathContext Decimal64 { get; set; }
	public static MathContext Unlimited { get; set; }
```

Added properties:

```
public static MathContext Decimal128 { get; }
	public static MathContext Decimal32 { get; }
	public static MathContext Decimal64 { get; }
	public static MathContext Unlimited { get; }
```

### Type Changed: Java.Math.RoundingMode

Removed properties:

```
public static RoundingMode Ceiling { get; set; }
	public static RoundingMode Down { get; set; }
	public static RoundingMode Floor { get; set; }
	public static RoundingMode HalfDown { get; set; }
	public static RoundingMode HalfEven { get; set; }
	public static RoundingMode HalfUp { get; set; }
	public static RoundingMode Unnecessary { get; set; }
	public static RoundingMode Up { get; set; }
```

Added properties:

```
public static RoundingMode Ceiling { get; }
	public static RoundingMode Down { get; }
	public static RoundingMode Floor { get; }
	public static RoundingMode HalfDown { get; }
	public static RoundingMode HalfEven { get; }
	public static RoundingMode HalfUp { get; }
	public static RoundingMode Unnecessary { get; }
	public static RoundingMode Up { get; }
```

## Namespace Java.Net

### Type Changed: Java.Net.Authenticator

### Type Changed: Java.Net.Authenticator.RequestorType

Removed properties:

```
public static Authenticator.RequestorType Proxy { get; set; }
	public static Authenticator.RequestorType Server { get; set; }
```

Added properties:

```
public static Authenticator.RequestorType Proxy { get; }
	public static Authenticator.RequestorType Server { get; }
```

### Type Changed: Java.Net.CookiePolicy

Removed properties:

```
public static ICookiePolicy AcceptAll { get; set; }
	public static ICookiePolicy AcceptNone { get; set; }
	public static ICookiePolicy AcceptOriginalServer { get; set; }
```

Added properties:

```
public static ICookiePolicy AcceptAll { get; }
	public static ICookiePolicy AcceptNone { get; }
	public static ICookiePolicy AcceptOriginalServer { get; }
```

### Type Changed: Java.Net.MulticastSocket

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void Send (DatagramPacket packet, sbyte ttl);
```

### Type Changed: Java.Net.Proxy

Removed property:

```
public static Proxy NoProxy { get; set; }
```

Added property:

```
public static Proxy NoProxy { get; }
```

### Type Changed: Java.Net.Proxy.Type

Removed properties:

```
public static Proxy.Type Direct { get; set; }
	public static Proxy.Type Http { get; set; }
	public static Proxy.Type Socks { get; set; }
```

Added properties:

```
public static Proxy.Type Direct { get; }
	public static Proxy.Type Http { get; }
	public static Proxy.Type Socks { get; }
```

### Type Changed: Java.Net.URLConnection

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public static string GetDefaultRequestProperty (string field);

	[Obsolete ("deprecated")]
	public static void SetDefaultRequestProperty (string field, string value);
```

### Type Changed: Java.Net.URLDecoder

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static string Decode (string s);
```

### Type Changed: Java.Net.URLEncoder

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static string Encode (string s);
```

### Type Changed: Java.Net.URLStreamHandler

Obsoleted method:

```
[Obsolete ("deprecated")]
	protected virtual void SetURL (URL u, string protocol, string host, int port, string file, string ref);
```

## Namespace Java.Nio

### Type Changed: Java.Nio.ByteOrder

Removed properties:

```
public static ByteOrder BigEndian { get; set; }
	public static ByteOrder LittleEndian { get; set; }
```

Added properties:

```
public static ByteOrder BigEndian { get; }
	public static ByteOrder LittleEndian { get; }
```

## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.FileChannel

### Type Changed: Java.Nio.Channels.FileChannel.MapMode

Removed properties:

```
public static FileChannel.MapMode Private { get; set; }
	public static FileChannel.MapMode ReadOnly { get; set; }
	public static FileChannel.MapMode ReadWrite { get; set; }
```

Added properties:

```
public static FileChannel.MapMode Private { get; }
	public static FileChannel.MapMode ReadOnly { get; }
	public static FileChannel.MapMode ReadWrite { get; }
```

## Namespace Java.Nio.Charset

### Type Changed: Java.Nio.Charset.CoderResult

Removed properties:

```
public static CoderResult Overflow { get; set; }
	public static CoderResult Underflow { get; set; }
```

Added properties:

```
public static CoderResult Overflow { get; }
	public static CoderResult Underflow { get; }
```

### Type Changed: Java.Nio.Charset.CodingErrorAction

Removed properties:

```
public static CodingErrorAction Ignore { get; set; }
	public static CodingErrorAction Replace { get; set; }
	public static CodingErrorAction Report { get; set; }
```

Added properties:

```
public static CodingErrorAction Ignore { get; }
	public static CodingErrorAction Replace { get; }
	public static CodingErrorAction Report { get; }
```

### Type Changed: Java.Nio.Charset.StandardCharsets

Removed properties:

```
public static Charset Iso88591 { get; set; }
	public static Charset UsAscii { get; set; }
	public static Charset Utf16 { get; set; }
	public static Charset Utf16be { get; set; }
	public static Charset Utf16le { get; set; }
	public static Charset Utf8 { get; set; }
```

Added properties:

```
public static Charset Iso88591 { get; }
	public static Charset UsAscii { get; }
	public static Charset Utf16 { get; }
	public static Charset Utf16be { get; }
	public static Charset Utf16le { get; }
	public static Charset Utf8 { get; }
```

## Namespace Java.Security

### Type Changed: Java.Security.KeyRep

### Type Changed: Java.Security.KeyRep.Type

Removed properties:

```
public static KeyRep.Type Private { get; set; }
	public static KeyRep.Type Public { get; set; }
	public static KeyRep.Type Secret { get; set; }
```

Added properties:

```
public static KeyRep.Type Private { get; }
	public static KeyRep.Type Public { get; }
	public static KeyRep.Type Secret { get; }
```

### Type Changed: Java.Security.Policy

Removed property:

```
public static PermissionCollection UnsupportedEmptyCollection { get; set; }
```

Added property:

```
public static PermissionCollection UnsupportedEmptyCollection { get; }
```

### Type Changed: Java.Security.Security

Obsoleted method:

```
[Obsolete ("deprecated")]
	public static string GetAlgorithmProperty (string algName, string propName);
```

### Type Changed: Java.Security.Signature

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public Java.Lang.Object GetParameter (string param);

	[Obsolete ("deprecated")]
	public void SetParameter (string param, Java.Lang.Object value);
```

## Namespace Java.Security.Spec

### Type Changed: Java.Security.Spec.ECPoint

Removed property:

```
public static ECPoint PointInfinity { get; set; }
```

Added property:

```
public static ECPoint PointInfinity { get; }
```

### Type Changed: Java.Security.Spec.MGF1ParameterSpec

Removed properties:

```
public static MGF1ParameterSpec Sha1 { get; set; }
	public static MGF1ParameterSpec Sha256 { get; set; }
	public static MGF1ParameterSpec Sha384 { get; set; }
	public static MGF1ParameterSpec Sha512 { get; set; }
```

Added properties:

```
public static MGF1ParameterSpec Sha1 { get; }
	public static MGF1ParameterSpec Sha256 { get; }
	public static MGF1ParameterSpec Sha384 { get; }
	public static MGF1ParameterSpec Sha512 { get; }
```

### Type Changed: Java.Security.Spec.PSSParameterSpec

Removed property:

```
public static PSSParameterSpec Default { get; set; }
```

Added property:

```
public static PSSParameterSpec Default { get; }
```

### Type Changed: Java.Security.Spec.RSAKeyGenParameterSpec

Removed properties:

```
public static Java.Math.BigInteger F0 { get; set; }
	public static Java.Math.BigInteger F4 { get; set; }
```

Added properties:

```
public static Java.Math.BigInteger F0 { get; }
	public static Java.Math.BigInteger F4 { get; }
```

## Namespace Java.Sql

### Type Changed: Java.Sql.ClientInfoStatus

Removed properties:

```
public static ClientInfoStatus ReasonUnknown { get; set; }
	public static ClientInfoStatus ReasonUnknownProperty { get; set; }
	public static ClientInfoStatus ReasonValueInvalid { get; set; }
	public static ClientInfoStatus ReasonValueTruncated { get; set; }
```

Added properties:

```
public static ClientInfoStatus ReasonUnknown { get; }
	public static ClientInfoStatus ReasonUnknownProperty { get; }
	public static ClientInfoStatus ReasonValueInvalid { get; }
	public static ClientInfoStatus ReasonValueTruncated { get; }
```

### Type Changed: Java.Sql.DatabaseMetaData

Removed properties:

```
public static int FunctionColumnIn { get; set; }
	public static int FunctionColumnInOut { get; set; }
	public static int FunctionColumnOut { get; set; }
	public static int FunctionColumnResult { get; set; }
	public static int FunctionColumnUnknown { get; set; }
	public static int FunctionNoNulls { get; set; }
	public static int FunctionNoTable { get; set; }
	public static int FunctionNullable { get; set; }
	public static int FunctionNullableUnknown { get; set; }
	public static int FunctionResultUnknown { get; set; }
	public static int FunctionReturn { get; set; }
	public static int FunctionReturnsTable { get; set; }
	public static int SqlStateSQL { get; set; }
```

Added properties:

```
public static int FunctionColumnIn { get; }
	public static int FunctionColumnInOut { get; }
	public static int FunctionColumnOut { get; }
	public static int FunctionColumnResult { get; }
	public static int FunctionColumnUnknown { get; }
	public static int FunctionNoNulls { get; }
	public static int FunctionNoTable { get; }
	public static int FunctionNullable { get; }
	public static int FunctionNullableUnknown { get; }
	public static int FunctionResultUnknown { get; }
	public static int FunctionReturn { get; }
	public static int FunctionReturnsTable { get; }
	public static int SqlStateSQL { get; }
```

### Type Changed: Java.Sql.RowIdLifetime

Removed properties:

```
public static RowIdLifetime RowidUnsupported { get; set; }
	public static RowIdLifetime RowidValidForever { get; set; }
	public static RowIdLifetime RowidValidOther { get; set; }
	public static RowIdLifetime RowidValidSession { get; set; }
	public static RowIdLifetime RowidValidTransaction { get; set; }
```

Added properties:

```
public static RowIdLifetime RowidUnsupported { get; }
	public static RowIdLifetime RowidValidForever { get; }
	public static RowIdLifetime RowidValidOther { get; }
	public static RowIdLifetime RowidValidSession { get; }
	public static RowIdLifetime RowidValidTransaction { get; }
```

### Type Changed: Java.Sql.Types

Removed properties:

```
public static int Longnvarchar { get; set; }
	public static int Nchar { get; set; }
	public static int Nclob { get; set; }
	public static int Nvarchar { get; set; }
	public static int Rowid { get; set; }
	public static int Sqlxml { get; set; }
```

Added properties:

```
public static int Longnvarchar { get; }
	public static int Nchar { get; }
	public static int Nclob { get; }
	public static int Nvarchar { get; }
	public static int Rowid { get; }
	public static int Sqlxml { get; }
```

## Namespace Java.Text

### Type Changed: Java.Text.AttributedCharacterIteratorAttribute

Removed properties:

```
public static AttributedCharacterIteratorAttribute InputMethodSegment { get; set; }
	public static AttributedCharacterIteratorAttribute Language { get; set; }
	public static AttributedCharacterIteratorAttribute Reading { get; set; }
```

Added properties:

```
public static AttributedCharacterIteratorAttribute InputMethodSegment { get; }
	public static AttributedCharacterIteratorAttribute Language { get; }
	public static AttributedCharacterIteratorAttribute Reading { get; }
```

### Type Changed: Java.Text.DateFormat

### Type Changed: Java.Text.DateFormat.Field

Removed properties:

```
public static DateFormat.Field AmPm { get; set; }
	public static DateFormat.Field DayOfMonth { get; set; }
	public static DateFormat.Field DayOfWeek { get; set; }
	public static DateFormat.Field DayOfWeekInMonth { get; set; }
	public static DateFormat.Field DayOfYear { get; set; }
	public static DateFormat.Field Era { get; set; }
	public static DateFormat.Field Hour0 { get; set; }
	public static DateFormat.Field Hour1 { get; set; }
	public static DateFormat.Field HourOfDay0 { get; set; }
	public static DateFormat.Field HourOfDay1 { get; set; }
	public static DateFormat.Field Millisecond { get; set; }
	public static DateFormat.Field Minute { get; set; }
	public static DateFormat.Field Month { get; set; }
	public static DateFormat.Field Second { get; set; }
	public static DateFormat.Field TimeZone { get; set; }
	public static DateFormat.Field WeekOfMonth { get; set; }
	public static DateFormat.Field WeekOfYear { get; set; }
	public static DateFormat.Field Year { get; set; }
```

Added properties:

```
public static DateFormat.Field AmPm { get; }
	public static DateFormat.Field DayOfMonth { get; }
	public static DateFormat.Field DayOfWeek { get; }
	public static DateFormat.Field DayOfWeekInMonth { get; }
	public static DateFormat.Field DayOfYear { get; }
	public static DateFormat.Field Era { get; }
	public static DateFormat.Field Hour0 { get; }
	public static DateFormat.Field Hour1 { get; }
	public static DateFormat.Field HourOfDay0 { get; }
	public static DateFormat.Field HourOfDay1 { get; }
	public static DateFormat.Field Millisecond { get; }
	public static DateFormat.Field Minute { get; }
	public static DateFormat.Field Month { get; }
	public static DateFormat.Field Second { get; }
	public static DateFormat.Field TimeZone { get; }
	public static DateFormat.Field WeekOfMonth { get; }
	public static DateFormat.Field WeekOfYear { get; }
	public static DateFormat.Field Year { get; }
```

### Type Changed: Java.Text.MessageFormat

### Type Changed: Java.Text.MessageFormat.Field

Removed property:

```
public static MessageFormat.Field Argument { get; set; }
```

Added property:

```
public static MessageFormat.Field Argument { get; }
```

### Type Changed: Java.Text.Normalizer

### Type Changed: Java.Text.Normalizer.Form

Removed properties:

```
public static Normalizer.Form Nfc { get; set; }
	public static Normalizer.Form Nfd { get; set; }
	public static Normalizer.Form Nfkc { get; set; }
	public static Normalizer.Form Nfkd { get; set; }
```

Added properties:

```
public static Normalizer.Form Nfc { get; }
	public static Normalizer.Form Nfd { get; }
	public static Normalizer.Form Nfkc { get; }
	public static Normalizer.Form Nfkd { get; }
```

### Type Changed: Java.Text.NumberFormat

### Type Changed: Java.Text.NumberFormat.Field

Removed properties:

```
public static NumberFormat.Field Currency { get; set; }
	public static NumberFormat.Field DecimalSeparator { get; set; }
	public static NumberFormat.Field Exponent { get; set; }
	public static NumberFormat.Field ExponentSign { get; set; }
	public static NumberFormat.Field ExponentSymbol { get; set; }
	public static NumberFormat.Field Fraction { get; set; }
	public static NumberFormat.Field GroupingSeparator { get; set; }
	public static NumberFormat.Field Integer { get; set; }
	public static NumberFormat.Field Percent { get; set; }
	public static NumberFormat.Field Permille { get; set; }
	public static NumberFormat.Field Sign { get; set; }
```

Added properties:

```
public static NumberFormat.Field Currency { get; }
	public static NumberFormat.Field DecimalSeparator { get; }
	public static NumberFormat.Field Exponent { get; }
	public static NumberFormat.Field ExponentSign { get; }
	public static NumberFormat.Field ExponentSymbol { get; }
	public static NumberFormat.Field Fraction { get; }
	public static NumberFormat.Field GroupingSeparator { get; }
	public static NumberFormat.Field Integer { get; }
	public static NumberFormat.Field Percent { get; }
	public static NumberFormat.Field Permille { get; }
	public static NumberFormat.Field Sign { get; }
```

## Namespace Java.Util

### Type Changed: Java.Util.Calendar

Removed properties:

```
public static CalendarStyle AllStyles { get; set; }
	public static CalendarStyle Long { get; set; }
	public static CalendarStyle Short { get; set; }
```

Added properties:

```
public static CalendarStyle AllStyles { get; }
	public static CalendarStyle Long { get; }
	public static CalendarStyle Short { get; }
```

### Type Changed: Java.Util.Date

Obsoleted methods:

```
[Obsolete ("deprecated")]
	public virtual int GetDate ();

	[Obsolete ("deprecated")]
	public static long Parse (string string);

	[Obsolete ("deprecated")]
	public virtual void SetDate (int day);

	[Obsolete ("deprecated")]
	public virtual string ToGMTString ();

	[Obsolete ("deprecated")]
	public virtual string ToLocaleString ();

	[Obsolete ("deprecated")]
	public static long UTC (int year, int month, int day, int hour, int minute, int second);
```

### Type Changed: Java.Util.Formatter

### Type Changed: Java.Util.Formatter.BigDecimalLayoutForm

Removed properties:

```
public static Formatter.BigDecimalLayoutForm DecimalFloat { get; set; }
	public static Formatter.BigDecimalLayoutForm Scientific { get; set; }
```

Added properties:

```
public static Formatter.BigDecimalLayoutForm DecimalFloat { get; }
	public static Formatter.BigDecimalLayoutForm Scientific { get; }
```

### Type Changed: Java.Util.Locale

Removed properties:

```
public static Locale Canada { get; set; }
	public static Locale CanadaFrench { get; set; }
	public static Locale China { get; set; }
	public static Locale Chinese { get; set; }
	public static Locale English { get; set; }
	public static Locale France { get; set; }
	public static Locale French { get; set; }
	public static Locale German { get; set; }
	public static Locale Germany { get; set; }
	public static Locale Italian { get; set; }
	public static Locale Italy { get; set; }
	public static Locale Japan { get; set; }
	public static Locale Japanese { get; set; }
	public static Locale Korea { get; set; }
	public static Locale Korean { get; set; }
	public static Locale Prc { get; set; }
	public static char PrivateUseExtension { get; set; }
	public static Locale Root { get; set; }
	public static Locale SimplifiedChinese { get; set; }
	public static Locale Taiwan { get; set; }
	public static Locale TraditionalChinese { get; set; }
	public static Locale Uk { get; set; }
	public static char UnicodeLocaleExtension { get; set; }
	public static Locale Us { get; set; }
```

Added properties:

```
public static Locale Canada { get; }
	public static Locale CanadaFrench { get; }
	public static Locale China { get; }
	public static Locale Chinese { get; }
	public static Locale English { get; }
	public static Locale France { get; }
	public static Locale French { get; }
	public static Locale German { get; }
	public static Locale Germany { get; }
	public static Locale Italian { get; }
	public static Locale Italy { get; }
	public static Locale Japan { get; }
	public static Locale Japanese { get; }
	public static Locale Korea { get; }
	public static Locale Korean { get; }
	public static Locale Prc { get; }
	public static char PrivateUseExtension { get; }
	public static Locale Root { get; }
	public static Locale SimplifiedChinese { get; }
	public static Locale Taiwan { get; }
	public static Locale TraditionalChinese { get; }
	public static Locale Uk { get; }
	public static char UnicodeLocaleExtension { get; }
	public static Locale Us { get; }
```

### Type Changed: Java.Util.Properties

Obsoleted method:

```
[Obsolete ("deprecated")]
	public virtual void Save (System.IO.Stream out, string comment);
```

### Type Changed: Java.Util.ResourceBundle

### Type Changed: Java.Util.ResourceBundle.Control

Removed properties:

```
public static System.Collections.IList FormatClass { get; set; }
	public static System.Collections.IList FormatDefault { get; set; }
	public static System.Collections.IList FormatProperties { get; set; }
```

Added properties:

```
public static System.Collections.IList FormatClass { get; }
	public static System.Collections.IList FormatDefault { get; }
	public static System.Collections.IList FormatProperties { get; }
```

## Namespace Java.Util.Concurrent

### Type Changed: Java.Util.Concurrent.ForkJoinPool

Removed property:

```
public static ForkJoinPool.IForkJoinWorkerThreadFactory DefaultForkJoinWorkerThreadFactory { get; set; }
```

Added property:

```
public static ForkJoinPool.IForkJoinWorkerThreadFactory DefaultForkJoinWorkerThreadFactory { get; }
```

### Type Changed: Java.Util.Concurrent.TimeUnit

Removed properties:

```
public static TimeUnit Days { get; set; }
	public static TimeUnit Hours { get; set; }
	public static TimeUnit Microseconds { get; set; }
	public static TimeUnit Milliseconds { get; set; }
	public static TimeUnit Minutes { get; set; }
	public static TimeUnit Nanoseconds { get; set; }
	public static TimeUnit Seconds { get; set; }
```

Added properties:

```
public static TimeUnit Days { get; }
	public static TimeUnit Hours { get; }
	public static TimeUnit Microseconds { get; }
	public static TimeUnit Milliseconds { get; }
	public static TimeUnit Minutes { get; }
	public static TimeUnit Nanoseconds { get; }
	public static TimeUnit Seconds { get; }
```

## Namespace Java.Util.Jar

### Type Changed: Java.Util.Jar.Attributes

### Type Changed: Java.Util.Jar.Attributes.Name

Removed properties:

```
public static Attributes.Name ClassPath { get; set; }
	public static Attributes.Name ContentType { get; set; }
	public static Attributes.Name ExtensionInstallation { get; set; }
	public static Attributes.Name ExtensionList { get; set; }
	public static Attributes.Name ExtensionName { get; set; }
	public static Attributes.Name ImplementationTitle { get; set; }
	public static Attributes.Name ImplementationUrl { get; set; }
	public static Attributes.Name ImplementationVendor { get; set; }
	public static Attributes.Name ImplementationVendorId { get; set; }
	public static Attributes.Name ImplementationVersion { get; set; }
	public static Attributes.Name MainClass { get; set; }
	public static Attributes.Name ManifestVersion { get; set; }
	public static Attributes.Name Sealed { get; set; }
	public static Attributes.Name SignatureVersion { get; set; }
	public static Attributes.Name SpecificationTitle { get; set; }
	public static Attributes.Name SpecificationVendor { get; set; }
	public static Attributes.Name SpecificationVersion { get; set; }
```

Added properties:

```
public static Attributes.Name ClassPath { get; }
	public static Attributes.Name ContentType { get; }
	public static Attributes.Name ExtensionInstallation { get; }
	public static Attributes.Name ExtensionList { get; }
	public static Attributes.Name ExtensionName { get; }
	public static Attributes.Name ImplementationTitle { get; }
	public static Attributes.Name ImplementationUrl { get; }
	public static Attributes.Name ImplementationVendor { get; }
	public static Attributes.Name ImplementationVendorId { get; }
	public static Attributes.Name ImplementationVersion { get; }
	public static Attributes.Name MainClass { get; }
	public static Attributes.Name ManifestVersion { get; }
	public static Attributes.Name Sealed { get; }
	public static Attributes.Name SignatureVersion { get; }
	public static Attributes.Name SpecificationTitle { get; }
	public static Attributes.Name SpecificationVendor { get; }
	public static Attributes.Name SpecificationVersion { get; }
```

## Namespace Java.Util.Logging

### Type Changed: Java.Util.Logging.Level

Removed properties:

```
public static Level All { get; set; }
	public static Level Config { get; set; }
	public static Level Fine { get; set; }
	public static Level Finer { get; set; }
	public static Level Finest { get; set; }
	public static Level Info { get; set; }
	public static Level Off { get; set; }
	public static Level Severe { get; set; }
	public static Level Warning { get; set; }
```

Added properties:

```
public static Level All { get; }
	public static Level Config { get; }
	public static Level Fine { get; }
	public static Level Finer { get; }
	public static Level Finest { get; }
	public static Level Info { get; }
	public static Level Off { get; }
	public static Level Severe { get; }
	public static Level Warning { get; }
```

### Type Changed: Java.Util.Logging.Logger

Removed property:

```
public static string GlobalLoggerName { get; set; }
```

Added property:

```
public static string GlobalLoggerName { get; }
```

## Namespace Java.Util.Regex

### Type Changed: Java.Util.Regex.Pattern

Removed property:

```
public static int UnicodeCharacterClass { get; set; }
```

Added property:

```
public static int UnicodeCharacterClass { get; }
```

## Namespace Java.Util.Zip

### Type Changed: Java.Util.Zip.Deflater

Removed properties:

```
public static int FullFlush { get; set; }
	public static int NoFlush { get; set; }
	public static int SyncFlush { get; set; }
```

Added properties:

```
public static int FullFlush { get; }
	public static int NoFlush { get; }
	public static int SyncFlush { get; }
```

## Namespace Javax.Crypto.Spec

### Type Changed: Javax.Crypto.Spec.OAEPParameterSpec

Removed property:

```
public static OAEPParameterSpec Default { get; set; }
```

Added property:

```
public static OAEPParameterSpec Default { get; }
```

### Type Changed: Javax.Crypto.Spec.PSource

### Type Changed: Javax.Crypto.Spec.PSource.PSpecified

Removed property:

```
public static PSource.PSpecified Default { get; set; }
```

Added property:

```
public static PSource.PSpecified Default { get; }
```

## Namespace Javax.Microedition.Khronos.Egl

### Type Changed: Javax.Microedition.Khronos.Egl.EGL10

Removed properties:

```
public static Java.Lang.Object EglDefaultDisplay { get; set; }
	public static EGLContext EglNoContext { get; set; }
	public static EGLDisplay EglNoDisplay { get; set; }
	public static EGLSurface EglNoSurface { get; set; }
```

Added properties:

```
public static Java.Lang.Object EglDefaultDisplay { get; }
	public static EGLContext EglNoContext { get; }
	public static EGLDisplay EglNoDisplay { get; }
	public static EGLSurface EglNoSurface { get; }
```

### Type Changed: Javax.Microedition.Khronos.Egl.EGL11

Removed properties:

```
public static Java.Lang.Object EglDefaultDisplay { get; set; }
	public static EGLContext EglNoContext { get; set; }
	public static EGLDisplay EglNoDisplay { get; set; }
	public static EGLSurface EglNoSurface { get; set; }
```

Added properties:

```
public static Java.Lang.Object EglDefaultDisplay { get; }
	public static EGLContext EglNoContext { get; }
	public static EGLDisplay EglNoDisplay { get; }
	public static EGLSurface EglNoSurface { get; }
```

## Namespace Javax.Net.Ssl

### Type Changed: Javax.Net.Ssl.SSLEngineResult

### Type Changed: Javax.Net.Ssl.SSLEngineResult.HandshakeStatus

Removed properties:

```
public static SSLEngineResult.HandshakeStatus Finished { get; set; }
	public static SSLEngineResult.HandshakeStatus NeedTask { get; set; }
	public static SSLEngineResult.HandshakeStatus NeedUnwrap { get; set; }
	public static SSLEngineResult.HandshakeStatus NeedWrap { get; set; }
	public static SSLEngineResult.HandshakeStatus NotHandshaking { get; set; }
```

Added properties:

```
public static SSLEngineResult.HandshakeStatus Finished { get; }
	public static SSLEngineResult.HandshakeStatus NeedTask { get; }
	public static SSLEngineResult.HandshakeStatus NeedUnwrap { get; }
	public static SSLEngineResult.HandshakeStatus NeedWrap { get; }
	public static SSLEngineResult.HandshakeStatus NotHandshaking { get; }
```

### Type Changed: Javax.Net.Ssl.SSLEngineResult.Status

Removed properties:

```
public static SSLEngineResult.Status BufferOverflow { get; set; }
	public static SSLEngineResult.Status BufferUnderflow { get; set; }
	public static SSLEngineResult.Status Closed { get; set; }
	public static SSLEngineResult.Status Ok { get; set; }
```

Added properties:

```
public static SSLEngineResult.Status BufferOverflow { get; }
	public static SSLEngineResult.Status BufferUnderflow { get; }
	public static SSLEngineResult.Status Closed { get; }
	public static SSLEngineResult.Status Ok { get; }
```

## Namespace Javax.Xml

### Type Changed: Javax.Xml.XMLConstants

Removed properties:

```
public static string AccessExternalDtd { get; set; }
	public static string AccessExternalSchema { get; set; }
	public static string AccessExternalStylesheet { get; set; }
```

Added properties:

```
public static string AccessExternalDtd { get; }
	public static string AccessExternalSchema { get; }
	public static string AccessExternalStylesheet { get; }
```

## Namespace Javax.Xml.Datatype

### Type Changed: Javax.Xml.Datatype.DatatypeConstants

Removed properties:

```
public static Javax.Xml.Namespace.QName Date { get; set; }
	public static Javax.Xml.Namespace.QName Datetime { get; set; }
	public static DatatypeConstants.Field Days { get; set; }
	public static Javax.Xml.Namespace.QName Duration { get; set; }
	public static Javax.Xml.Namespace.QName DurationDaytime { get; set; }
	public static Javax.Xml.Namespace.QName DurationYearmonth { get; set; }
	public static Javax.Xml.Namespace.QName Gday { get; set; }
	public static Javax.Xml.Namespace.QName Gmonth { get; set; }
	public static Javax.Xml.Namespace.QName Gmonthday { get; set; }
	public static Javax.Xml.Namespace.QName Gyear { get; set; }
	public static Javax.Xml.Namespace.QName Gyearmonth { get; set; }
	public static DatatypeConstants.Field Hours { get; set; }
	public static DatatypeConstants.Field Minutes { get; set; }
	public static DatatypeConstants.Field Months { get; set; }
	public static DatatypeConstants.Field Seconds { get; set; }
	public static Javax.Xml.Namespace.QName Time { get; set; }
	public static DatatypeConstants.Field Years { get; set; }
```

Added properties:

```
public static Javax.Xml.Namespace.QName Date { get; }
	public static Javax.Xml.Namespace.QName Datetime { get; }
	public static DatatypeConstants.Field Days { get; }
	public static Javax.Xml.Namespace.QName Duration { get; }
	public static Javax.Xml.Namespace.QName DurationDaytime { get; }
	public static Javax.Xml.Namespace.QName DurationYearmonth { get; }
	public static Javax.Xml.Namespace.QName Gday { get; }
	public static Javax.Xml.Namespace.QName Gmonth { get; }
	public static Javax.Xml.Namespace.QName Gmonthday { get; }
	public static Javax.Xml.Namespace.QName Gyear { get; }
	public static Javax.Xml.Namespace.QName Gyearmonth { get; }
	public static DatatypeConstants.Field Hours { get; }
	public static DatatypeConstants.Field Minutes { get; }
	public static DatatypeConstants.Field Months { get; }
	public static DatatypeConstants.Field Seconds { get; }
	public static Javax.Xml.Namespace.QName Time { get; }
	public static DatatypeConstants.Field Years { get; }
```

### Type Changed: Javax.Xml.Datatype.DatatypeFactory

Removed property:

```
public static string DatatypefactoryImplementationClass { get; set; }
```

Added property:

```
public static string DatatypefactoryImplementationClass { get; }
```

## Namespace Javax.Xml.Xpath

### Type Changed: Javax.Xml.Xpath.XPathConstants

Removed properties:

```
public static Javax.Xml.Namespace.QName Boolean { get; set; }
	public static Javax.Xml.Namespace.QName Node { get; set; }
	public static Javax.Xml.Namespace.QName Nodeset { get; set; }
	public static Javax.Xml.Namespace.QName Number { get; set; }
	public static Javax.Xml.Namespace.QName String { get; set; }
```

Added properties:

```
public static Javax.Xml.Namespace.QName Boolean { get; }
	public static Javax.Xml.Namespace.QName Node { get; }
	public static Javax.Xml.Namespace.QName Nodeset { get; }
	public static Javax.Xml.Namespace.QName Number { get; }
	public static Javax.Xml.Namespace.QName String { get; }
```

## Namespace Org.Apache.Http

### Type Changed: Org.Apache.Http.HttpVersion

Removed properties:

```
public static HttpVersion Http09 { get; set; }
	public static HttpVersion Http10 { get; set; }
	public static HttpVersion Http11 { get; set; }
```

Added properties:

```
public static HttpVersion Http09 { get; }
	public static HttpVersion Http10 { get; }
	public static HttpVersion Http11 { get; }
```

## Namespace Org.Apache.Http.Authentication

### Type Changed: Org.Apache.Http.Authentication.AuthScope

Removed properties:

```
public static AuthScope Any { get; set; }
	public static string AnyHost { get; set; }
	public static string AnyRealm { get; set; }
	public static string AnyScheme { get; set; }
```

Added properties:

```
public static AuthScope Any { get; }
	public static string AnyHost { get; }
	public static string AnyRealm { get; }
	public static string AnyScheme { get; }
```

## Namespace Org.Apache.Http.Conn.Params

### Type Changed: Org.Apache.Http.Conn.Params.ConnRouteParams

Removed properties:

```
public static Org.Apache.Http.HttpHost NoHost { get; set; }
	public static Org.Apache.Http.Conn.Routing.HttpRoute NoRoute { get; set; }
```

Added properties:

```
public static Org.Apache.Http.HttpHost NoHost { get; }
	public static Org.Apache.Http.Conn.Routing.HttpRoute NoRoute { get; }
```

## Namespace Org.Apache.Http.Conn.Routing

### Type Changed: Org.Apache.Http.Conn.Routing.RouteInfoLayerType

Removed properties:

```
public static RouteInfoLayerType Layered { get; set; }
	public static RouteInfoLayerType Plain { get; set; }
```

Added properties:

```
public static RouteInfoLayerType Layered { get; }
	public static RouteInfoLayerType Plain { get; }
```

### Type Changed: Org.Apache.Http.Conn.Routing.RouteInfoTunnelType

Removed properties:

```
public static RouteInfoTunnelType Plain { get; set; }
	public static RouteInfoTunnelType Tunnelled { get; set; }
```

Added properties:

```
public static RouteInfoTunnelType Plain { get; }
	public static RouteInfoTunnelType Tunnelled { get; }
```

## Namespace Org.Apache.Http.Conn.Ssl

### Type Changed: Org.Apache.Http.Conn.Ssl.SSLSocketFactory

Removed properties:

```
public static IX509HostnameVerifier AllowAllHostnameVerifier { get; set; }
	public static IX509HostnameVerifier BrowserCompatibleHostnameVerifier { get; set; }
	public static IX509HostnameVerifier StrictHostnameVerifier { get; set; }
```

Added properties:

```
public static IX509HostnameVerifier AllowAllHostnameVerifier { get; }
	public static IX509HostnameVerifier BrowserCompatibleHostnameVerifier { get; }
	public static IX509HostnameVerifier StrictHostnameVerifier { get; }
```

## Namespace Org.Apache.Http.Message

### Type Changed: Org.Apache.Http.Message.BasicHeaderValueFormatter

Removed property:

```
public static BasicHeaderValueFormatter Default { get; set; }
```

Added property:

```
public static BasicHeaderValueFormatter Default { get; }
```

### Type Changed: Org.Apache.Http.Message.BasicHeaderValueParser

Removed property:

```
public static BasicHeaderValueParser Default { get; set; }
```

Added property:

```
public static BasicHeaderValueParser Default { get; }
```

### Type Changed: Org.Apache.Http.Message.BasicLineFormatter

Removed property:

```
public static BasicLineFormatter Default { get; set; }
```

Added property:

```
public static BasicLineFormatter Default { get; }
```

### Type Changed: Org.Apache.Http.Message.BasicLineParser

Removed property:

```
public static BasicLineParser Default { get; set; }
```

Added property:

```
public static BasicLineParser Default { get; }
```

## Namespace Org.Apache.Http.Protocol

### Type Changed: Org.Apache.Http.Protocol.HttpDateGenerator

Removed property:

```
public static Java.Util.TimeZone Gmt { get; set; }
```

Added property:

```
public static Java.Util.TimeZone Gmt { get; }
```

### Type Changed: Org.Apache.Http.Protocol.HttpRequestHandlerRegistry

Obsoleted method:

```
[Obsolete ("deprecated")]
	protected virtual bool MatchUriRequestPattern (string pattern, string requestUri);
```

## Namespace Org.Json

### Type Changed: Org.Json.JSONObject

Removed property:

```
public static Java.Lang.Object Null { get; set; }
```

Added property:

```
public static Java.Lang.Object Null { get; }
```

## Namespace Org.W3c.Dom

### Type Changed: Org.W3c.Dom.DOMException

Removed properties:

```
public static short TypeMismatchErr { get; set; }
	public static short ValidationErr { get; set; }
```

Added properties:

```
public static short TypeMismatchErr { get; }
	public static short ValidationErr { get; }
```

### Type Changed: Org.W3c.Dom.Node

Removed properties:

```
public static short DocumentPositionContainedBy { get; set; }
	public static short DocumentPositionContains { get; set; }
	public static short DocumentPositionDisconnected { get; set; }
	public static short DocumentPositionFollowing { get; set; }
	public static short DocumentPositionImplementationSpecific { get; set; }
	public static short DocumentPositionPreceding { get; set; }
```

Added properties:

```
public static short DocumentPositionContainedBy { get; }
	public static short DocumentPositionContains { get; }
	public static short DocumentPositionDisconnected { get; }
	public static short DocumentPositionFollowing { get; }
	public static short DocumentPositionImplementationSpecific { get; }
	public static short DocumentPositionPreceding { get; }
```

## Namespace Org.XmlPull.V1

### Type Changed: Org.XmlPull.V1.XmlPullParser

Removed property:

```
public static System.Collections.Generic.IList<string> Types { get; set; }
```

Added property:

```
public static System.Collections.Generic.IList<string> Types { get; }
```

## Namespace System.Drawing

### Type Changed: System.Drawing.KnownColor

Added values:

```
ButtonFace = 168,
	ButtonHighlight = 169,
	ButtonShadow = 170,
	GradientActiveCaption = 171,
	GradientInactiveCaption = 172,
	MenuBar = 173,
	MenuHighlight = 174,
```

### Type Changed: System.Drawing.PointF

Added method:

```
public static PointF op_Subtraction (PointF pt, SizeF sz);
```

### Type Changed: System.Drawing.SystemColors

Added properties:

```
public static Color ButtonFace { get; }
	public static Color ButtonHighlight { get; }
	public static Color ButtonShadow { get; }
	public static Color GradientActiveCaption { get; }
	public static Color GradientInactiveCaption { get; }
	public static Color MenuBar { get; }
	public static Color MenuHighlight { get; }
```

### New Type System.Drawing.SizeFConverter

```
public class SizeFConverter : System.ComponentModel.TypeConverter {
	// constructors
	public SizeFConverter ();
	// methods
	public override bool CanConvertFrom (System.ComponentModel.ITypeDescriptorContext context, System.Type sourceType);
	public override bool CanConvertTo (System.ComponentModel.ITypeDescriptorContext context, System.Type destinationType);
	public override object ConvertFrom (System.ComponentModel.ITypeDescriptorContext context, System.Globalization.CultureInfo culture, object value);
	public override object ConvertTo (System.ComponentModel.ITypeDescriptorContext context, System.Globalization.CultureInfo culture, object value, System.Type destinationType);
	public override object CreateInstance (System.ComponentModel.ITypeDescriptorContext context, System.Collections.IDictionary propertyValues);
	public override bool GetCreateInstanceSupported (System.ComponentModel.ITypeDescriptorContext context);
	public override System.ComponentModel.PropertyDescriptorCollection GetProperties (System.ComponentModel.ITypeDescriptorContext context, object value, System.Attribute[] attributes);
	public override bool GetPropertiesSupported (System.ComponentModel.ITypeDescriptorContext context);
}
```
